
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Soumadip Biswas - Young Developer, Web Creator and Future Tech Innovator.">
<title>Soumadip Biswas | SOUL</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;800&family=Inter:wght@400;500;600;700;800&display=swap');

:root {
    --bg: #050816;
    --panel: #0b1428;
    --cyan: #00d9ff;
    --purple: #9b5cff;
    --white: #f4f7ff;
    --muted: #a5b2cc;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    background: var(--bg);
    color: var(--white);
    font-family: Inter, sans-serif;
    overflow-x: hidden;
}

a {
    text-decoration: none;
    color: inherit;
}

button {
    font: inherit;
}

#particles {
    position: fixed;
    inset: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: -1;
}

nav {
    height: 75px;
    padding: 0 8%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: #070d1de8;
    border-bottom: 1px solid #18375d;
    position: sticky;
    top: 0;
    z-index: 100;
    backdrop-filter: blur(15px);
}

.logo {
    font-family: Orbitron, sans-serif;
    font-size: 27px;
    font-weight: 800;
    color: var(--cyan);
    text-shadow: 0 0 18px var(--cyan);
}

.nav-links {
    display: flex;
    gap: 30px;
    align-items: center;
}

.nav-links a {
    color: #d4def1;
    transition: .3s;
    font-size: 14px;
}

.nav-links a:hover {
    color: var(--cyan);
}

.github-btn, .primary-btn {
    padding: 12px 21px;
    border: 1px solid var(--cyan);
    border-radius: 30px;
    color: white;
    background: #06162c;
    transition: .3s;
    display: inline-block;
}

.github-btn:hover, .primary-btn:hover {
    box-shadow: 0 0 25px #00d9ff70;
    transform: translateY(-3px);
}

.menu {
    display: none;
    border: 0;
    background: none;
    color: white;
    font-size: 26px;
    cursor: pointer;
}

.hero {
    min-height: 620px;
    padding: 120px 10%;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
    background:
        radial-gradient(ellipse at 78% 45%, #173a78 0%, transparent 35%),
        radial-gradient(ellipse at 90% 85%, #481a75 0%, transparent 35%);
}

.hero::before {
    content: "";
    position: absolute;
    width: 400px;
    height: 400px;
    right: 10%;
    top: 15%;
    border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, #76dfff, #1454b0 45%, #090d35 75%);
    box-shadow: 0 0 80px #087cff70;
    animation: float 6s ease-in-out infinite;
}

.hero-content {
    max-width: 680px;
    z-index: 2;
}

.hero-tag {
    color: var(--cyan);
    letter-spacing: 4px;
    font-size: 13px;
}

.hero h1 {
    font-size: clamp(40px, 7vw, 76px);
    line-height: 1.15;
    margin: 20px 0;
    letter-spacing: -3px;
}

.gradient {
    background: linear-gradient(90deg, var(--cyan), var(--purple));
    -webkit-background-clip: text;
    color: transparent;
}

.hero h3 {
    font-size: 19px;
    margin-bottom: 20px;
    color: #d6e2f8;
}

.hero p {
    color: var(--muted);
    line-height: 1.9;
    max-width: 550px;
}

.hero-actions {
    display: flex;
    gap: 15px;
    margin-top: 30px;
    flex-wrap: wrap;
}

.secondary-btn {
    padding: 12px 21px;
    border: 1px solid #344765;
    border-radius: 30px;
    color: white;
    transition: .3s;
}

.secondary-btn:hover {
    border-color: var(--purple);
    color: var(--cyan);
}

section {
    padding: 85px 9%;
}

.section-title {
    font-family: Orbitron, sans-serif;
    font-size: 30px;
    margin-bottom: 35px;
}

.section-title span {
    color: var(--cyan);
}

.about-grid {
    display: grid;
    grid-template-columns: 1.4fr 1fr;
    gap: 25px;
}

.panel {
    background: linear-gradient(145deg, #101c35, #080e20);
    border: 1px solid #203c61;
    padding: 30px;
    border-radius: 18px;
    transition: .3s;
}

.panel:hover {
    border-color: var(--cyan);
    box-shadow: 0 0 25px #00d9ff12;
}

.panel h3 {
    margin-bottom: 17px;
    color: var(--cyan);
    font-size: 21px;
}

.panel p {
    color: var(--muted);
    line-height: 1.9;
}

.quote {
    margin-top: 25px;
    padding: 15px;
    border-left: 3px solid var(--cyan);
    background: #0a2440;
    color: #b9edff;
    border-radius: 5px;
}

.roles {
    display: grid;
    gap: 16px;
}

.role {
    color: #dce8ff;
    display: flex;
    gap: 12px;
}

.role span {
    color: var(--cyan);
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(135px, 1fr));
    gap: 17px;
}

.skill {
    padding: 24px 12px;
    text-align: center;
    background: #101b32;
    border: 1px solid #213a5e;
    border-radius: 12px;
    transition: .3s;
}

.skill:hover {
    transform: translateY(-7px);
    border-color: var(--cyan);
    box-shadow: 0 0 20px #00d9ff20;
}

.skill .symbol {
    font-size: 30px;
    margin-bottom: 10px;
}

.skill h4 {
    font-size: 14px;
}

.skill p {
    font-size: 11px;
    color: var(--muted);
    margin-top: 6px;
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 20px;
}

.project {
    background: #0d1830;
    border: 1px solid #263e61;
    padding: 25px;
    border-radius: 15px;
    transition: .35s;
}

.project:hover {
    transform: translateY(-8px);
    border-color: var(--purple);
    box-shadow: 0 0 25px #9b5cff20;
}

.project-icon {
    font-size: 35px;
    margin-bottom: 20px;
}

.project h3 {
    color: var(--cyan);
    margin-bottom: 12px;
}

.project p {
    color: var(--muted);
    line-height: 1.7;
    font-size: 14px;
}

.project a {
    display: inline-block;
    margin-top: 20px;
    color: var(--cyan);
    font-size: 13px;
}

.learning {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 15px;
}

.learning div {
    padding: 20px;
    background: #101b32;
    border-radius: 10px;
    border: 1px solid #203c61;
}

.learning h4 {
    color: var(--cyan);
    margin-bottom: 8px;
}

.learning p {
    color: var(--muted);
    font-size: 13px;
}

.contact-box {
    text-align: center;
    padding: 50px 20px;
    background: linear-gradient(130deg, #101d38, #1a1040);
    border: 1px solid #4d3980;
    border-radius: 20px;
}

.contact-box p {
    color: var(--muted);
    margin: 15px auto 25px;
    line-height: 1.8;
}

footer {
    padding: 30px 8%;
    text-align: center;
    border-top: 1px solid #21344f;
    color: var(--muted);
    font-size: 13px;
}

footer strong {
    color: var(--cyan);
}

.reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity .8s, transform .8s;
}

.reveal.visible {
    opacity: 1;
    transform: translateY(0);
}

@keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-20px); }
}

@media(max-width: 800px) {
    nav {
        padding: 0 6%;
    }

    .menu {
        display: block;
    }

    .nav-links {
        display: none;
        position: absolute;
        top: 75px;
        left: 0;
        width: 100%;
        background: #080f20;
        padding: 25px;
        flex-direction: column;
        border-bottom: 1px solid #23446c;
    }

    .nav-links.open {
        display: flex;
    }

    .github-btn {
        display: none;
    }

    .hero {
        padding: 100px 7%;
        min-height: 570px;
    }

    .hero::before {
        opacity: .3;
        right: -30%;
    }

    .about-grid {
        grid-template-columns: 1fr;
    }

    section {
        padding: 65px 7%;
    }
}
</style>
</head>

<body>

<canvas id="particles"></canvas>

<nav>
    <a class="logo" href="#home">SOUL.</a>

    <button class="menu" id="menu" aria-label="Toggle navigation">☰</button>

    <div class="nav-links" id="navLinks">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
    </div>

    <a class="github-btn" href="https://github.com/YOUR_USERNAME" target="_blank" rel="noopener">
        GitHub ↗
    </a>
</nav>

<!-- HERO -->

<header class="hero" id="home">
    <div class="hero-content">
        <div class="hero-tag">WELCOME TO MY DIGITAL WORLD</div>

        <h1>
            Hello, I'm<br>
            <span class="gradient">Soumadip Biswas</span>
        </h1>

        <h3>Young Developer | Web Creator | Future Tech Innovator</h3>

        <p>
            Exploring technology, building creative ideas,
            learning programming and creating a better digital future.
        </p>

        <div class="hero-actions">
            <a href="#projects" class="primary-btn">Explore My Work →</a>
            <a href="#about" class="secondary-btn">Discover More</a>
        </div>
    </div>
</header>

<!-- ABOUT -->

<section id="about" class="reveal">
    <h2 class="section-title">About <span>Me</span></h2>

    <div class="about-grid">
        <div class="panel">
            <h3>Who Am I?</h3>
            <p>
                Hello! I'm Soumadip Biswas, a young developer
                passionate about programming, artificial intelligence,
                web development and technology innovation.
                I enjoy creating websites, exploring new technologies
                and transforming creative ideas into digital projects.
            </p>

            <div class="quote">
                "Don't just imagine the future. Learn, build and create it."
            </div>
        </div>

        <div class="panel">
            <h3>My Interests</h3>
            <div class="roles">
                <div class="role"><span>🚀</span> Technology Enthusiast</div>
                <div class="role"><span>💻</span> Web Developer</div>
                <div class="role"><span>🤖</span> AI Explorer</div>
                <div class="role"><span>🔐</span> Cybersecurity Learner</div>
                <div class="role"><span>🌌</span> SOUL Founder</div>
            </div>
        </div>
    </div>
</section>

<!-- SKILLS -->

<section id="skills" class="reveal">
    <h2 class="section-title">My <span>Skills</span></h2>

    <div class="skills-grid">
        <div class="skill"><div class="symbol">🌐</div><h4>HTML</h4><p>Web Structure</p></div>
        <div class="skill"><div class="symbol">🎨</div><h4>CSS</h4><p>Web Styling</p></div>
        <div class="skill"><div class="symbol">⚡</div><h4>JavaScript</h4><p>Interactivity</p></div>
        <div class="skill"><div class="symbol">©️</div><h4>C</h4><p>Programming</p></div>
        <div class="skill"><div class="symbol">🦀</div><h4>Rust</h4><p>Learning</p></div>
        <div class="skill"><div class="symbol">🐍</div><h4>Python</h4><p>Learning</p></div>
        <div class="skill"><div class="symbol">🔧</div><h4>Git</h4><p>Version Control</p></div>
        <div class="skill"><div class="symbol">🐙</div><h4>GitHub</h4><p>Repositories</p></div>
        <div class="skill"><div class="symbol">🔥</div><h4>Firebase</h4><p>Backend Learning</p></div>
    </div>
</section>

<!-- PROJECTS -->

<section id="projects" class="reveal">
    <h2 class="section-title">Featured <span>Projects</span></h2>

    <div class="projects-grid">

        <div class="project">
            <div class="project-icon">🌌</div>
            <h3>SOUL</h3>
            <p>
                Soumadip Orbit Universal Labs.
                My personal technology initiative focused on innovation
                and useful digital products.
            </p>
            <a href="#" >Explore Project →</a>
        </div>

        <div class="project">
            <div class="project-icon">🤖</div>
            <h3>SOUL AI</h3>
            <p>
                An AI assistant project exploring conversational
                interfaces and AI-powered experiences.
            </p>
            <a href="#">Explore Project →</a>
        </div>

        <div class="project">
            <div class="project-icon">🛡️</div>
            <h3>SOUL CYBERGUARD</h3>
            <p>
                A cybersecurity awareness project focused on
                online safety, scam awareness and education.
            </p>
            <a href="#">Explore Project →</a>
        </div>

        <div class="project">
            <div class="project-icon">🌍</div>
            <h3>ORVANTA</h3>
            <p>
                A community-oriented digital concept
                exploring online connections and experiences.
            </p>
            <a href="#">Explore Project →</a>
        </div>

        <div class="project">
            <div class="project-icon">💻</div>
            <h3>Web Experiments</h3>
            <p>
                Creative websites, animations, interactive
                interfaces and useful web-based tools.
            </p>
            <a href="#">Explore Project →</a>
        </div>

    </div>
</section>

<!-- LEARNING -->

<section class="reveal">
    <h2 class="section-title">My Learning <span>Journey</span></h2>

    <div class="learning">
        <div><h4>Web Development</h4><p>HTML, CSS and JavaScript</p></div>
        <div><h4>Programming</h4><p>C, Rust and Python</p></div>
        <div><h4>Artificial Intelligence</h4><p>Exploring AI technologies</p></div>
        <div><h4>Software Development</h4><p>Building digital projects</p></div>
        <div><h4>Cybersecurity</h4><p>Learning digital safety</p></div>
        <div><h4>Version Control</h4><p>Git and GitHub</p></div>
    </div>
</section>

<!-- CONTACT -->

<section id="contact" class="reveal">
    <div class="contact-box">
        <h2 class="section-title">Let's Connect</h2>

        <p>
            Interested in technology, programming or innovative ideas?
            Explore my projects and connect with me.
        </p>

        <a href="https://github.com/YOUR_USERNAME" class="primary-btn" target="_blank" rel="noopener">
            Visit My GitHub ↗
        </a>
    </div>
</section>

<footer>
    <p>Made with ♥ by <strong>Soumadip Biswas</strong></p>
    <br>
    <p>SOUL — Soumadip Orbit Universal Labs</p>
    <br>
    <p>Explore. Innovate. Build.</p>
    <br>
    <p>© <span id="year"></span> Soumadip Biswas. All Rights Reserved.</p>
</footer>

<script>
// Mobile navigation
const menu = document.getElementById("menu");
const navLinks = document.getElementById("navLinks");

menu.addEventListener("click", () => {
    navLinks.classList.toggle("open");
});

document.querySelectorAll(".nav-links a").forEach(link => {
    link.addEventListener("click", () => {
        navLinks.classList.remove("open");
    });
});

// Scroll reveal animations
const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add("visible");
            observer.unobserve(entry.target);
        }
    });
}, { threshold: 0.12 });

document.querySelectorAll(".reveal").forEach(element => {
    observer.observe(element);
});

// Dynamic year
document.getElementById("year").textContent =
    new Date().getFullYear();

// Animated background particles
const canvas = document.getElementById("particles");
const ctx = canvas.getContext("2d");

let particles = [];

function resizeCanvas() {
    const dpr = Math.min(window.devicePixelRatio || 1, 2);
    canvas.width = window.innerWidth * dpr;
    canvas.height = window.innerHeight * dpr;
    canvas.style.width = window.innerWidth + "px";
    canvas.style.height = window.innerHeight + "px";
    ctx.setTransform(dpr, 0, 0, dpr, 0, 0);

    particles = Array.from({ length: 55 }, () => ({
        x: Math.random() * window.innerWidth,
        y: Math.random() * window.innerHeight,
        size: Math.random() * 1.7 + .4,
        speed: Math.random() * .35 + .1
    }));
}

function animateParticles() {
    ctx.clearRect(0, 0, window.innerWidth, window.innerHeight);

    particles.forEach(p => {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
        ctx.fillStyle = "rgba(0,217,255,0.65)";
        ctx.fill();

        p.y -= p.speed;

        if (p.y < 0) {
            p.y = window.innerHeight;
            p.x = Math.random() * window.innerWidth;
        }
    });

    requestAnimationFrame(animateParticles);
}

resizeCanvas();
window.addEventListener("resize", resizeCanvas);
animateParticles();
</script>

</body>
</html>

