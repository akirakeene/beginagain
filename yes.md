---
layout: default
title: akira keene teotrakool
---

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Courier New', monospace !important;
    background: #f5f5dc !important;
    color: #333 !important;
    font-size: 14px !important;
    line-height: 1.4 !important;
    overflow-x: hidden;
}

.cursor-trail {
    position: fixed;
    width: 20px;
    height: 20px;
    background: rgba(139, 90, 60, 0.3);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
    transition: all 0.1s ease;
}

.container {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
}

/* floating navigation */
.nav-floating {
    position: fixed;
    top: 20px;
    right: 20px;
    z-index: 1000;
    background: rgba(245, 245, 220, 0.9);
    border: 2px dashed #8b5a3c;
    padding: 15px;
    font-size: 12px;
    transform: rotate(2deg);
    transition: transform 0.3s ease;
}

.nav-floating:hover {
    transform: rotate(-1deg) scale(1.05);
}

.nav-floating a {
    display: block;
    color: #8b5a3c !important;
    text-decoration: none !important;
    margin: 5px 0;
    position: relative;
}

.nav-floating a:hover {
    color: #d2691e !important;
}

.nav-floating a:before {
    content: "→ ";
    opacity: 0;
    transition: opacity 0.3s ease;
}

.nav-floating a:hover:before {
    opacity: 1;
}

/* header */
.header {
    text-align: center;
    margin: 40px 0 60px 0;
    position: relative;
}

.name {
    font-size: 2.5rem !important;
    font-weight: bold !important;
    color: #8b5a3c !important;
    text-transform: lowercase;
    letter-spacing: -0.02em;
    position: relative;
    display: inline-block;
}

.name:after {
    content: "";
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 100%;
    height: 3px;
    background: repeating-linear-gradient(
        to right,
        #8b5a3c 0px,
        #8b5a3c 10px,
        transparent 10px,
        transparent 15px
    );
}

.subtitle {
    margin-top: 20px;
    font-style: italic;
    color: #666 !important;
    transform: rotate(-1deg);
    display: inline-block;
}

/* ascii art dividers */
.divider {
    text-align: center;
    margin: 40px 0;
    color: #8b5a3c;
    font-family: monospace;
    font-size: 12px;
    user-select: none;
}

/* content blocks */
.content-block {
    background: rgba(255, 255, 255, 0.7);
    border: 1px solid #ddd;
    margin: 30px 0;
    padding: 25px;
    position: relative;
    transform: rotate(0deg);
    transition: all 0.3s ease;
}

.content-block:nth-child(odd) {
    transform: rotate(0.5deg);
    border-style: dashed;
}

.content-block:nth-child(even) {
    transform: rotate(-0.3deg);
    border-style: dotted;
}

.content-block:hover {
    transform: rotate(0deg) scale(1.02);
    box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.1);
    z-index: 10;
}

.section-title {
    font-size: 1.2rem !important;
    color: #8b5a3c !important;
    margin-bottom: 15px !important;
    text-transform: lowercase;
    position: relative;
    display: inline-block;
}

.section-title:before {
    content: "◆ ";
    color: #d2691e;
}

/* research items */
.research-item {
    margin: 20px 0;
    padding: 15px;
    background: rgba(245, 245, 220, 0.5);
    border-left: 3px solid #8b5a3c;
    position: relative;
}

.research-status {
    font-size: 11px;
    color: #d2691e;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 8px;
    font-weight: bold;
}

.research-title {
    font-style: italic;
    color: #333;
    margin-bottom: 8px;
    line-height: 1.3;
}

.research-details {
    font-size: 12px;
    color: #666;
    line-height: 1.4;
}

/* experience */
.experience-item {
    margin: 25px 0;
    padding: 20px;
    background: rgba(255, 255, 255, 0.8);
    border: 2px solid #ddd;
    position: relative;
}

.experience-item:before {
    content: "";
    position: absolute;
    top: -2px;
    left: -2px;
    right: -2px;
    bottom: -2px;
    background: linear-gradient(45deg, #8b5a3c, #d2691e, #8b5a3c);
    z-index: -1;
    opacity: 0;
    transition: opacity 0.3s ease;
}

.experience-item:hover:before {
    opacity: 0.3;
}

.experience-header {
    margin-bottom: 10px;
}

.experience-title {
    font-weight: bold;
    color: #8b5a3c;
    text-transform: lowercase;
}

.experience-org {
    color: #666;
    font-style: italic;
    margin: 5px 0;
}

.experience-date {
    font-size: 11px;
    color: #999;
    float: right;
    transform: rotate(2deg);
}

.experience-details {
    font-size: 13px;
    color: #555;
    line-height: 1.4;
}

.experience-details ul {
    list-style: none !important;
    margin-top: 10px;
}

.experience-details li {
    margin: 5px 0;
    position: relative;
    padding-left: 20px;
}

.experience-details li:before {
    content: "•";
    position: absolute;
    left: 0;
    color: #8b5a3c;
    font-weight: bold;
}

/* bio section */
.bio-text {
    font-size: 14px;
    line-height: 1.6;
    color: #444;
    text-align: justify;
    columns: 2;
    column-gap: 30px;
    column-rule: 1px dashed #ccc;
}

.bio-text p {
    margin-bottom: 15px;
    break-inside: avoid;
}

/* skills grid */
.skills-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    margin-top: 20px;
}

.skill-box {
    background: rgba(255, 255, 255, 0.9);
    border: 1px solid #ddd;
    padding: 15px;
    text-align: center;
    transform: rotate(1deg);
    transition: all 0.3s ease;
}

.skill-box:nth-child(even) {
    transform: rotate(-1deg);
}

.skill-box:hover {
    transform: rotate(0deg) scale(1.05);
    border-color: #8b5a3c;
}

.skill-category {
    font-size: 12px;
    color: #8b5a3c;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 10px;
    font-weight: bold;
}

.skill-list {
    font-size: 13px;
    color: #555;
    line-height: 1.4;
}

/* contact section */
.contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 20px;
}

.contact-item {
    background: rgba(245, 245, 220, 0.7);
    border: 2px dashed #8b5a3c;
    padding: 15px;
    text-align: center;
    transform: rotate(-1deg);
    transition: all 0.3s ease;
}

.contact-item:nth-child(even) {
    transform: rotate(1deg);
}

.contact-item:hover {
    transform: rotate(0deg);
    background: rgba(255, 255, 255, 0.9);
}

.contact-label {
    font-size: 11px;
    color: #8b5a3c;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 8px;
    font-weight: bold;
}

.contact-value {
    color: #333;
    font-size: 13px;
}

.contact-value a {
    color: #8b5a3c !important;
    text-decoration: none !important;
}

.contact-value a:hover {
    color: #d2691e !important;
    text-decoration: underline !important;
}

/* footer */
.footer {
    text-align: center;
    margin: 60px 0 40px 0;
    font-size: 12px;
    color: #999;
    font-style: italic;
}

/* animations */
@keyframes float {
    0%, 100% { transform: translateY(0px) rotate(1deg); }
    50% { transform: translateY(-5px) rotate(-1deg); }
}

.floating {
    animation: float 6s ease-in-out infinite;
}

/* mobile */
@media (max-width: 768px) {
    .nav-floating {
        position: relative;
        top: auto;
        right: auto;
        margin: 20px auto;
        display: table;
        transform: rotate(0deg);
    }

    .bio-text {
        columns: 1;
    }

    .name {
        font-size: 2rem !important;
    }

    .skills-container {
        grid-template-columns: 1fr;
    }

    .contact-grid {
        grid-template-columns: 1fr;
    }
}

/* special effects */
.glitch {
    position: relative;
    color: #8b5a3c;
    font-size: 2rem;
    font-weight: bold;
    text-transform: lowercase;
    letter-spacing: -0.02em;
    animation: glitch 2s linear infinite;
}

@keyframes glitch {
    2%, 64% {
        transform: translate(2px, 0) skew(0deg);
    }
    4%, 60% {
        transform: translate(-2px, 0) skew(0deg);
    }
    62% {
        transform: translate(0, 0) skew(5deg);
    }
}

.glitch:before,
.glitch:after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

.glitch:before {
    animation: glitch 2s linear infinite;
    color: #d2691e;
    z-index: -1;
}

.glitch:after {
    animation: glitch 2s linear infinite;
    color: #8b5a3c;
    z-index: -2;
}

/* Override GitHub Pages default styles */
.markdown-body {
    font-family: 'Courier New', monospace !important;
    background: #f5f5dc !important;
    color: #333 !important;
}

.markdown-body h1, .markdown-body h2, .markdown-body h3 {
    border-bottom: none !important;
}
</style>

<div class="cursor-trail"></div>

<!-- floating navigation -->
<div class="nav-floating floating">
<div style="margin-bottom: 10px; font-weight: bold; color: #8b5a3c;">navigate:</div>
<a href="#about">about</a>
<a href="#research">research</a>
<a href="#experience">experience</a>
<a href="#skills">skills</a>
<a href="#contact">contact</a>
</div>

<div class="container">

<!-- header -->
<div class="header">
<div class="name glitch" data-text="akira keene teotrakool">akira keene teotrakool</div>
<div class="subtitle">class researcher of transnational digital cultures</div>
</div>

<div class="divider">
◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆
</div>

<!-- about section -->
<div id="about" class="content-block">
<div class="section-title">about</div>
<div class="bio-text">
<p>a rising sophomore at grinnell college studying social research and analysis through an independent major. their research is informed by political psychology, economic sociology, and critical media studies to examine class identity and affect in urban youth cultures across southeast asia.</p>

<p>their work focuses on two primary projects: "educational sequencing as class strategy," investigating how decisions to pursue higher education abroad affect human capital formation and class reproduction among thai international students; and "subcultural economies of addictive glamorization," exploring thai urban identity formation through aspirational femininity.</p>

<p>in a past life in thailand, akira worked as a creative event organizer, policy advocate for the thai student union, and philosophy-for/with-children facilitator via the philosophy and religion society of thailand.</p>

<p>they plan to pursue a phd in sociology, public policy, or political economy with further study in curatorial practice, to program national accessibility to cultural and creative spaces in southeast asia.</p>
</div>
</div>

<div class="divider">
◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇
</div>

<!-- research section -->
<div id="research" class="content-block">
<div class="section-title">research</div>

<div class="research-item">
<div class="research-status">forthcoming 2026</div>
<div class="research-title">"addictive glamorization: enterprising influencers and the reimagining of thai urban identity through aspirational femininity"</div>
<div class="research-details">in <em>influencer and gender politics in southeast asia</em>, edited by annisa beta, hao zheng, and crystal abidin.</div>
</div>

<div class="research-item">
<div class="research-status">forthcoming 2026</div>
<div class="research-title">"trans cinema from thailand"</div>
<div class="research-details">with shaka mcglotten. <em>routledge handbook of trans cinema</em>, edited by douglas a. vakoch, routledge.</div>
</div>

<div class="research-item">
<div class="research-status">under review</div>
<div class="research-title">"political psychology in thailand: future avenues for examining emotions in thai politics"</div>
<div class="research-details">revise and resubmit at <em>journal of social and political psychology</em>. supervised by dr. brandon ng and dr. courtney nava, grinnell college.</div>
</div>

<div class="research-item">
<div class="research-status">under review</div>
<div class="research-title">"transnational agitprop as feminist methodology: twitter 'protest-learning' and political issue formation in thailand's 2020-21 anti-government protests"</div>
<div class="research-details">under review at <em>asiascapes: digital asia, special issue on "networked agitprop"</em>.</div>
</div>

<div class="research-item">
<div class="research-status">working papers</div>
<div class="research-title">"educational sequencing as class strategy: thai undergraduate and graduate student cohesion in elite u.s. universities"</div>
<div class="research-details">with archawin kittirattanapaiboon.</div>
</div>

<div class="research-item">
<div class="research-status">in progress</div>
<div class="research-title">"not quite at home, not quite alone: comparing group cohesion and social identity between 'rare birds' and dominant international student groups at an elite liberal arts college"</div>
<div class="research-details">data collection in progress.</div>
</div>
</div>

<div class="divider">
◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆
</div>

<!-- experience section -->
<div id="experience" class="content-block">
<div class="section-title">experience</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">organizer and executive committee member</div>
<div class="experience-date">mar 2023 — present</div>
<div class="experience-org">rosenfield program in public affairs, grinnell college</div>
</div>
<div class="experience-details">
<ul>
<li>coordinated symposia, guest speakers, program study trips, and sponsored campus events on public affairs, international relations, and human rights</li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">head of institutional outreach and programming</div>
<div class="experience-date">nov 2024 — present</div>
<div class="experience-org">association of thai students in the united states of america</div>
</div>
<div class="experience-details">
<ul>
<li>designed and implemented online programs easing thai students' cultural transition to u.s. academic life</li>
<li>launched research seminar series and mentorship programs connecting undergraduates with thai graduate students</li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">staff writer</div>
<div class="experience-date">jan 2023 — present</div>
<div class="experience-org">the scarlet and black, grinnell college</div>
</div>
<div class="experience-details">
<ul>
<li><a href="https://thesandb.com/51343/features/reflecting-on-southeast-asian-identity-after-faculty-trip-email/">reflecting on southeast asian identity after faculty trip email</a></li>
<li><a href="https://thesandb.com/51061/features/sustainability-initiatives-think-beyond-recycling-advocate-for-education-and-institutional-memory/">sustainability initiatives think beyond recycling</a></li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">co-founding member and fieldwork coordinator</div>
<div class="experience-date">may 2021 — jul 2023</div>
<div class="experience-org">thailand student union</div>
</div>
<div class="experience-details">
<ul>
<li>co-founded student organization centralizing youth organizations in thailand</li>
<li>supervised field safety and legal counsel for student demonstrators at ministry of education</li>
<li>organized 8-week policy study group on 2021-22 national education act</li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">philosophy for/with children facilitator</div>
<div class="experience-date">may 2022 — dec 2023</div>
<div class="experience-org">philosophy and religion society of thailand</div>
</div>
<div class="experience-details">
<ul>
<li>trained practitioner in philosophy for/with children techniques</li>
<li>facilitated workshops for youths aged 8-12 & 13-18 with supervision from mahidol u. faculty</li>
</ul>
</div>
</div>
</div>

<div class="divider">
◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇
</div>

<!-- skills section -->
<div id="skills" class="content-block">
<div class="section-title">interests & qualifications</div>

<div class="skills-container">
<div class="skill-box">
<div class="skill-category">research interests</div>
<div class="skill-list">political psychology<br>economic sociology<br>elites and international education<br>transnationalism<br>digital populism in southeast asia</div>
</div>

<div class="skill-box">
<div class="skill-category">methodologies</div>
<div class="skill-list">multi-sited/digital ethnography<br>narrative inquiry<br>causal inference</div>
</div>

<div class="skill-box">
<div class="skill-category">software</div>
<div class="skill-list">spss (beginner)<br>r-studio (beginner)<br>arcgis pro (intermediate)</div>
</div>

<div class="skill-box">
<div class="skill-category">languages</div>
<div class="skill-list">english (native)<br>thai (native)<br>italian (intermediate)<br>german (beginner)</div>
</div>
</div>
</div>

<div class="divider">
◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆ ◇ ◆
</div>

<!-- contact section -->
<div id="contact" class="content-block">
<div class="section-title">contact</div>

<div class="contact-grid">
<div class="contact-item">
<div class="contact-label">email</div>
<div class="contact-value"><a href="mailto:teotrako@grinnell.edu">teotrako@grinnell.edu</a></div>
</div>

<div class="contact-item">
<div class="contact-label">phone</div>
<div class="contact-value">+1-641-643-0139</div>
</div>

<div class="contact-item">
<div class="contact-label">address</div>
<div class="contact-value">1115 8th ave #4900<br>grinnell, ia 50112</div>
</div>

<div class="contact-item">
<div class="contact-label">pronouns</div>
<div class="contact-value">they/them</div>
</div>
</div>
</div>

<div class="footer">
references available upon request
<br>
◆ ◇ ◆
</div>

</div>

<script>
// cursor trail effect
let mouseX = 0;
let mouseY = 0;
const trail = document.querySelector('.cursor-trail');

document.addEventListener('mousemove', (e) => {
    mouseX = e.clientX;
    mouseY = e.clientY;
    
    trail.style.left = mouseX - 10 + 'px';
    trail.style.top = mouseY - 10 + 'px';
});

// smooth scrolling
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({
                behavior: 'smooth'
            });
        }
    });
});

// random rotation on page load
function randomizeRotations() {
    const blocks = document.querySelectorAll('.content-block');
    blocks.forEach((block, index) => {
        const randomRotation = (Math.random() - 0.5) * 2;
        block.style.transform = `rotate(${randomRotation}deg)`;
    });
}

// call on load
window.addEventListener('load', randomizeRotations);

// add some randomness to skill boxes
const skillBoxes = document.querySelectorAll('.skill-box');
skillBoxes.forEach(box => {
    const randomRotation = (Math.random() - 0.5) * 4;
    box.style.transform = `rotate(${randomRotation}deg)`;
});

// floating navigation subtle animation
const nav = document.querySelector('.nav-floating');
setInterval(() => {
    const randomRotation = (Math.random() - 0.5) * 6;
    nav.style.transform = `rotate(${randomRotation}deg)`;
}, 3000);
</script>
