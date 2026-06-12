<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NutriScope MVP</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>

body{
    /* font-family:Arial,
    sans-serif;
    background:#111520;
    color:#fff;
    margin:0;padding:20px */
    
    background:
    radial-gradient(circle at top left,#4e1515,#020617);
    color:white;
    min-height:100vh;

}
.card{background:#cd6060;
    padding:16px;
    border-radius:12px;
    margin-bottom:16px
}
input,select,button{padding:8px;
    margin:4px;
    border-radius:8px;
    border:none
}
button{
    background:#3b82f6;
    color:white;
    cursor:pointer
}
table{width:100%;
    border-collapse:collapse
}
th,td{
    border:1px solid #0e1115;
    padding:8px;
    text-align:center
}
.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
    gap:16px
}

.container{
  max-width:1000px;
  margin:auto;
}

.dashboard{
  display:grid;
  grid-template-columns:300px 1fr;
  gap:24px;
}


</style>
</head>
<body>
<h1>🥗 NutriScope MVP</h1>

<div class="card">

<h2>Profile</h2>

<input id="age" type="number" placeholder="Age">
<select id="gender">
    <option>Male</option>
    <option>Female</option>
</select>

<input id="height" type="number" placeholder="Height cm">
<input id="weight" type="number" placeholder="Weight kg">
<select id="activity">

<option>Sedentary</option>
<option>Moderate</option>
<option>Active</option>
</select>
<select id="diet">
<option>Vegetarian</option>
<option>Non-Vegetarian</option>
<option>Eggetarian</option>
</select>
<button onclick="updateTargets()">Calculate Targets</button>
<p id="targets"></p>
</div>

<div class="card">
<h2>Food Log</h2>
<select id="food"></select>
<input id="qty" type="number" value="100">
<button onclick="addFood()">Add Food</button>

<table>
<thead>
<tr><th>Food</th>
    <th>Qty(g)</th>
    <th>Calories</th>
    <th>Protein</th>
    <th>Action</th>
</tr>
</thead>
<tbody id="tbody"></tbody>
</table>
</div>

<div class="grid">
<div class="card">
<h2>Calories</h2>
<h3 id="calories">0</h3>
</div>

<div class="card">
<h2>Recommendations</h2>
<ul id="recommendations"></ul>
</div>
</div>

<div class="card">
<canvas id="macroChart"></canvas>
</div>

<script>
const foods={
Rice:{cal:130,protein:2.7,carbs:28,fat:0.3},
Roti:{cal:120,protein:3.5,carbs:20,fat:2},
Dal:{cal:116,protein:9,carbs:20,fat:0.4},
Paneer:{cal:265,protein:18,carbs:1.2,fat:20},
Curd:{cal:98,protein:3.5,carbs:4.7,fat:4.3},
Chana:{cal:164,protein:9,carbs:27,fat:2.6},
Rajma:{cal:127,protein:8.7,carbs:22,fat:0.5},
Banana:{cal:89,protein:1.1,carbs:23,fat:0.3},
Apple:{cal:52,protein:0.3,carbs:14,fat:0.2},
Milk:{cal:61,protein:3.2,carbs:5,fat:3.3},
Oats:{cal:389,protein:17,carbs:66,fat:7},
Bread:{cal:265,protein:9,carbs:49,fat:3.2},
Egg:{cal:155,protein:13,carbs:1.1,fat:11},
Chicken:{cal:239,protein:27,carbs:0,fat:14},
Fish:{cal:206,protein:22,carbs:0,fat:12},
Potato:{cal:77,protein:2,carbs:17,fat:0.1},
Poha:{cal:130,protein:2.5,carbs:25,fat:2},
Idli:{cal:58,protein:2,carbs:12,fat:0.4},
Dosa:{cal:168,protein:4,carbs:28,fat:4},
Spinach:{cal:23,protein:2.9,carbs:3.6,fat:0.4}
};

const foodSelect=document.getElementById("food");
Object.keys(foods).forEach(f=>{
 let o=document.createElement("option");
 o.text=f;
 foodSelect.add(o);
});

let logs=[];
let targetCalories=2000;

function updateTargets(){
 let weight=+document.getElementById("weight").value||70;
 targetCalories=Math.round(weight*30);
 document.getElementById("targets").innerText=
 "Target Calories: "+targetCalories+" kcal";
 updateDashboard();
}

function addFood(){
 let food=document.getElementById("food").value;
 let qty=+document.getElementById("qty").value;
 logs.push({food,qty});
 render();
}

function removeFood(i){
 logs.splice(i,1);
 render();
}

function render(){
 let tbody=document.getElementById("tbody");
 tbody.innerHTML="";
 logs.forEach((l,i)=>{
 let f=foods[l.food];
 let factor=l.qty/100;
 tbody.innerHTML+=`
 <tr>
 <td>${l.food}</td>
 <td>${l.qty}</td>
 <td>${(f.cal*factor).toFixed(1)}</td>
 <td>${(f.protein*factor).toFixed(1)}</td>
 <td><button onclick="removeFood(${i})">Delete</button></td>
 </tr>`;
 });
 updateDashboard();
}

let chart=new Chart(document.getElementById("macroChart"),{
 type:'doughnut',
 data:{
 labels:['Protein','Carbs','Fat'],
 datasets:[{data:[0,0,0]}]
 }
});

function updateDashboard(){
 let cal=0,p=0,c=0,f=0;
 logs.forEach(l=>{
 let x=foods[l.food];
 let m=l.qty/100;
 cal+=x.cal*m;
 p+=x.protein*m;
 c+=x.carbs*m;
 f+=x.fat*m;
 });

 document.getElementById("calories").innerText=
 `${cal.toFixed(0)} / ${targetCalories}`;

 chart.data.datasets[0].data=[p,c,f];
 chart.update();

 let rec=[];
 let diet=document.getElementById("diet").value;

 if(p<60){
   if(diet==="Vegetarian") rec.push("Increase Paneer, Dal, Chana");
   else rec.push("Increase Eggs, Chicken, Fish");
 }
 if(cal<targetCalories*0.8) rec.push("Increase portions to meet calorie goal");
 if(cal>targetCalories*1.2) rec.push("Reduce high calorie foods");

 document.getElementById("recommendations").innerHTML=
 rec.map(x=>`<li>${x}</li>`).join("");
}
</script>
</body>
</html>
