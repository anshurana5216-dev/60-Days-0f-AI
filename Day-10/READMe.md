<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Anshu Rana | Frontend Developer & GenAI Enthusiast</title>

<!-- SEO -->
<meta name="description" content="Anshu Rana - Frontend Developer, DSA Enthusiast, AI Prompt Engineer, and Data Analysis Learner. Explore projects, skills, achievements, and contact information.">
<meta name="keywords" content="Anshu Rana, Frontend Developer, Portfolio, DSA, AI Prompt Engineering, Data Analysis, Web Developer">
<meta name="author" content="Anshu Rana">

<!-- Open Graph -->
<meta property="og:title" content="Anshu Rana Portfolio">
<meta property="og:description" content="Frontend Developer | DSA Enthusiast | AI Prompt Engineer">
<meta property="og:type" content="website">

<script src="https://cdn.tailwindcss.com"></script>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">

<style>
*{
font-family:'Inter',sans-serif;
scroll-behavior:smooth;
}

.gradient{
background:linear-gradient(135deg,#7c3aed,#06b6d4);
-webkit-background-clip:text;
-webkit-text-fill-color:transparent;
}

.glass{
backdrop-filter:blur(12px);
background:rgba(255,255,255,0.08);
border:1px solid rgba(255,255,255,0.1);
}

.project-card{
transition:all .4s ease;
}

.project-card:hover{
transform:translateY(-10px);
}

.reveal{
opacity:0;
transform:translateY(50px);
transition:all .8s ease;
}

.reveal.active{
opacity:1;
transform:translateY(0);
}

.skill-bar{
animation:fillBar 2s ease forwards;
}

@keyframes fillBar{
from{width:0}
}

.nav-active{
color:#06b6d4 !important;
}

.cursor{
display:inline-block;
animation:blink .7s infinite;
}

@keyframes blink{
50%{opacity:0}
}

.dark-mode{
background:#0f172a;
color:white;
}

.light-mode{
background:#f8fafc;
color:#111827;
}
</style>
</head>

<body id="body" class="dark-mode transition-all duration-500">

<!-- NAVBAR -->
<nav class="fixed top-0 left-0 w-full z-50 glass">
<div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">

<h1 class="font-bold text-2xl gradient">ANSHU RANA</h1>

<div class="hidden md:flex gap-8 font-medium">
<a href="#home" class="nav-link">Home</a>
<a href="#about" class="nav-link">About</a>
<a href="#skills" class="nav-link">Skills</a>
<a href="#projects" class="nav-link">Projects</a>
<a href="#achievements" class="nav-link">Achievements</a>
<a href="#contact" class="nav-link">Contact</a>
</div>

<button id="themeToggle"
class="px-4 py-2 rounded-lg bg-cyan-500 text-white">
🌙
</button>

</div>
</nav>

<!-- HERO -->
<section id="home" class="min-h-screen flex items-center justify-center px-6">

<div class="text-center">

<p class="text-cyan-400 uppercase tracking-widest mb-4">
Welcome To My Portfolio
</p>

<h1 class="text-5xl md:text-7xl font-extrabold mb-4">
ANSHU <span class="gradient">RANA</span>
</h1>

<h2 class="text-xl md:text-3xl font-semibold mb-6">
<span id="typing"></span><span class="cursor">|</span>
</h2>

<p class="max-w-2xl mx-auto text-gray-400 mb-8">
Passionate Frontend Developer, DSA Enthusiast, and AI Prompt Engineer.
I enjoy building modern web applications, solving coding challenges,
and exploring AI-powered solutions that create real-world impact.
</p>

<div class="flex justify-center gap-4 flex-wrap">

<a href="https://github.com/anshurana5216-dev"
target="_blank"
class="px-6 py-3 rounded-xl bg-gray-800 hover:bg-gray-700 transition">
GitHub
</a>

<a href="https://www.linkedin.com/in/anshu-rana-2767aa329"
target="_blank"
class="px-6 py-3 rounded-xl bg-cyan-500 hover:bg-cyan-600 text-white transition">
LinkedIn
</a>

<a href="#contact"
class="px-6 py-3 rounded-xl border border-cyan-500 hover:bg-cyan-500 hover:text-white transition">
Hire Me
</a>

</div>

</div>

</section>

<!-- ABOUT -->
<section id="about" class="py-24 px-6 reveal">

<div class="max-w-6xl mx-auto">

<h2 class="text-4xl font-bold mb-12 text-center">
About <span class="gradient">Me</span>
</h2>

<div class="glass rounded-3xl p-8">

<p class="text-lg leading-8">
I am Anshu Rana, a Computer Science student and aspiring Software Engineer
with a strong interest in Frontend Development, Data Structures &
Algorithms, AI Prompt Engineering, and Data Analysis.

I enjoy creating responsive websites, building practical projects,
participating in coding challenges, and continuously learning modern
technologies that prepare me for the future of software development.
</p>

</div>

</div>

</section>

<!-- SKILLS -->
<section id="skills" class="py-24 px-6 reveal">

<div class="max-w-6xl mx-auto">

<h2 class="text-4xl font-bold text-center mb-12">
Skills & <span class="gradient">Expertise</span>
</h2>

<div class="grid md:grid-cols-2 gap-10">

<div class="glass p-8 rounded-3xl">

<h3 class="text-2xl font-bold mb-6">Technical Skills</h3>

<div class="space-y-6">

<div>
<div class="flex justify-between mb-2">
<span>Frontend Development</span>
<span>90%</span>
</div>
<div class="bg-gray-700 h-3 rounded-full">
<div class="skill-bar bg-cyan-500 h-3 rounded-full w-[90%]"></div>
</div>
</div>

<div>
<div class="flex justify-between mb-2">
<span>DSA</span>
<span>85%</span>
</div>
<div class="bg-gray-700 h-3 rounded-full">
<div class="skill-bar bg-purple-500 h-3 rounded-full w-[85%]"></div>
</div>
</div>

<div>
<div class="flex justify-between mb-2">
<span>AI Prompt Engineering</span>
<span>80%</span>
</div>
<div class="bg-gray-700 h-3 rounded-full">
<div class="skill-bar bg-teal-500 h-3 rounded-full w-[80%]"></div>
</div>
</div>

<div>
<div class="flex justify-between mb-2">
<span>Data Analysis</span>
<span>75%</span>
</div>
<div class="bg-gray-700 h-3 rounded-full">
<div class="skill-bar bg-pink-500 h-3 rounded-full w-[75%]"></div>
</div>
</div>

</div>

</div>

<div class="glass p-8 rounded-3xl">

<h3 class="text-2xl font-bold mb-6">Tools & Soft Skills</h3>

<div class="flex flex-wrap gap-3">

<span class="px-4 py-2 rounded-full bg-cyan-500 text-white">VS Code</span>
<span class="px-4 py-2 rounded-full bg-purple-500 text-white">GitHub</span>
<span class="px-4 py-2 rounded-full bg-teal-500 text-white">Kaggle</span>
<span class="px-4 py-2 rounded-full bg-pink-500 text-white">Leadership</span>
<span class="px-4 py-2 rounded-full bg-orange-500 text-white">Communication</span>
<span class="px-4 py-2 rounded-full bg-blue-500 text-white">Problem Solving</span>
<span class="px-4 py-2 rounded-full bg-green-500 text-white">Teamwork</span>

</div>

</div>

</div>

</div>

</section>

<!-- PROJECTS -->
<section id="projects" class="py-24 px-6 reveal">

<div class="max-w-7xl mx-auto">

<h2 class="text-4xl font-bold text-center mb-16">
Featured <span class="gradient">Projects</span>
</h2>

<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">

<!-- Project 1 -->
<div class="project-card glass rounded-3xl p-6">

<h3 class="text-2xl font-bold mb-3">
College Events & Clubs Website
</h3>

<p class="text-gray-400 mb-4">
A modern platform for students to explore college events,
clubs, registrations, and announcements through an interactive UI.
</p>

<div class="flex flex-wrap gap-2">
<span class="bg-cyan-500 px-3 py-1 rounded-full text-sm">HTML</span>
<span class="bg-purple-500 px-3 py-1 rounded-full text-sm">CSS</span>
<span class="bg-teal-500 px-3 py-1 rounded-full text-sm">Tailwind</span>
<span class="bg-pink-500 px-3 py-1 rounded-full text-sm">JavaScript</span>
</div>

</div>

<!-- Project 2 -->
<div class="project-card glass rounded-3xl p-6">

<h3 class="text-2xl font-bold mb-3">
Portfolio Website
</h3>

<p class="text-gray-400 mb-4">
A personal branding website showcasing skills,
projects, achievements, and professional journey.
</p>

<div class="flex flex-wrap gap-2">
<span class="bg-cyan-500 px-3 py-1 rounded-full text-sm">HTML</span>
<span class="bg-purple-500 px-3 py-1 rounded-full text-sm">CSS</span>
<span class="bg-teal-500 px-3 py-1 rounded-full text-sm">Tailwind</span>
</div>

</div>

<!-- Project 3 -->
<div class="project-card glass rounded-3xl p-6">

<h3 class="text-2xl font-bold mb-3">
To-Do List Application
</h3>

<p class="text-gray-400 mb-4">
Task management application with add, edit,
delete, and completion tracking functionality.
</p>

<div class="flex flex-wrap gap-2">
<span class="bg-cyan-500 px-3 py-1 rounded-full text-sm">HTML</span>
<span class="bg-purple-500 px-3 py-1 rounded-full text-sm">CSS</span>
<span class="bg-pink-500 px-3 py-1 rounded-full text-sm">JavaScript</span>
</div>

</div>

</div>

</div>

</section>

<!-- ACHIEVEMENTS -->
<section id="achievements" class="py-24 px-6 reveal">

<div class="max-w-6xl mx-auto">

<h2 class="text-4xl font-bold text-center mb-12">
Achievements & <span class="gradient">Certifications</span>
</h2>

<div class="glass rounded-3xl p-8">

<ul class="space-y-4 text-lg">

<li>🏆 Active DSA Learner solving coding problems regularly.</li>

<li>🚀 Building AI and Frontend projects through self-learning and internships.</li>

<li>📚 Participated in coding challenges and project-based learning programs.</li>

<li>💡 Exploring Generative AI, Data Analysis, and Full-Stack Development.</li>

<li>🎯 Consistently improving problem-solving and software engineering skills.</li>

</ul>

</div>

</div>

</section>

<!-- CONTACT -->
<section id="contact" class="py-24 px-6 reveal">

<div class="max-w-5xl mx-auto">

<h2 class="text-4xl font-bold text-center mb-12">
Get In <span class="gradient">Touch</span>
</h2>

<div class="grid md:grid-cols-2 gap-10">

<div class="glass rounded-3xl p-8">

<h3 class="text-2xl font-bold mb-6">Contact Information</h3>

<p class="mb-4">📍 Ghaziabad, India</p>

<p class="mb-4">
📧
<a href="mailto:anshurana5216@gmail.com" class="text-cyan-400">
anshurana5216@gmail.com
</a>
</p>

<p class="mb-4">
💼
<a href="https://www.linkedin.com/in/anshu-rana-2767aa329"
target="_blank"
class="text-cyan-400">
LinkedIn Profile
</a>
</p>

<p>
🐙
<a href="https://github.com/anshurana5216-dev"
target="_blank"
class="text-cyan-400">
GitHub Profile
</a>
</p>

</div>

<form class="glass rounded-3xl p-8">

<input
type="text"
placeholder="Your Name"
class="w-full mb-4 p-3 rounded-lg bg-gray-800 text-white border border-gray-700">

<input
type="email"
placeholder="Your Email"
class="w-full mb-4 p-3 rounded-lg bg-gray-800 text-white border border-gray-700">

<textarea
rows="5"
placeholder="Your Message"
class="w-full mb-4 p-3 rounded-lg bg-gray-800 text-white border border-gray-700"></textarea>

<button
type="submit"
class="w-full bg-cyan-500 hover:bg-cyan-600 text-white py-3 rounded-lg font-semibold">
Send Message
</button>

</form>

</div>

</div>

</section>

<!-- FOOTER -->
<footer class="py-8 text-center border-t border-gray-700">
<p>
© 2026 Anshu Rana. Built with HTML, Tailwind CSS & JavaScript.
</p>
</footer>

<script>

// Typing Animation
const texts = [
"Frontend Developer",
"DSA Enthusiast",
"AI Prompt Engineer",
"Data Analysis Learner"
];

let count = 0;
let index = 0;
let currentText = "";
let letter = "";

(function type(){

if(count === texts.length){
count = 0;
}

currentText = texts[count];
letter = currentText.slice(0, ++index);

document.getElementById("typing").textContent = letter;

if(letter.length === currentText.length){
count++;
index = 0;
setTimeout(type,1500);
}
else{
setTimeout(type,100);
}

})();

// Theme Toggle
const toggle = document.getElementById("themeToggle");
const body = document.getElementById("body");

toggle.addEventListener("click",()=>{

body.classList.toggle("dark-mode");
body.classList.toggle("light-mode");

toggle.textContent =
body.classList.contains("dark-mode")
? "🌙"
: "☀️";

});

// Reveal Animations
const reveals = document.querySelectorAll(".reveal");

window.addEventListener("scroll",()=>{

reveals.forEach(reveal=>{

const top = reveal.getBoundingClientRect().top;
const visible = 150;

if(top < window.innerHeight - visible){
reveal.classList.add("active");
}

});

});

// Active Navigation
const sections = document.querySelectorAll("section");
const navLinks = document.querySelectorAll(".nav-link");

window.addEventListener("scroll",()=>{

let current = "";

sections.forEach(section=>{

const sectionTop = section.offsetTop;

if(pageYOffset >= sectionTop - 200){
current = section.getAttribute("id");
}

});

navLinks.forEach(link=>{

link.classList.remove("nav-active");

if(link.getAttribute("href").includes(current)){
link.classList.add("nav-active");
}

});

});

</script>

</body>
</html>
