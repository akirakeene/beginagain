# akira keene teotrakool
---
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
    font-family: 'Georgia', 'Times New Roman', serif !important;
    background: #fdfdfd !important;
    color: #333 !important;
    font-size: 16px !important;
    line-height: 1.6 !important;
}

.container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 40px 60px;
}

/* header */
.header {
    text-align: center;
    margin-bottom: 60px;
    border-bottom: 1px solid #e0e0e0;
    padding-bottom: 40px;
}

.name {
    font-size: 2.2rem !important;
    font-weight: normal !important;
    color: #8B4513 !important;
    margin-bottom: 15px;
    letter-spacing: 0.5px;
}

.subtitle {
    font-size: 1.1rem;
    color: #666 !important;
    font-style: italic;
    margin-bottom: 20px;
}

/* navigation */
.nav {
    text-align: center;
    margin: 30px 0;
}

.nav a {
    color: #8B4513 !important;
    text-decoration: none !important;
    margin: 0 25px;
    font-size: 16px;
    border-bottom: 1px solid transparent;
    transition: border-bottom 0.3s ease;
}

.nav a:hover {
    border-bottom: 1px solid #8B4513;
}

/* main content */
.main-content {
    display: grid;
    grid-template-columns: 300px 1fr;
    gap: 60px;
    margin-top: 40px;
}

.sidebar {
    border-right: 1px solid #e0e0e0;
    padding-right: 40px;
}

.content {
    max-width: 700px;
}

/* profile section */
.profile-image {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background: linear-gradient(135deg, #8B4513, #A0522D);
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 30px auto;
    font-size: 3rem;
    color: white;
}

.contact-info {
    text-align: center;
    margin-bottom: 30px;
}

.contact-info p {
    margin: 8px 0;
    font-size: 14px;
    color: #666;
}

.contact-info a {
    color: #8B4513 !important;
    text-decoration: none !important;
}

.contact-info a:hover {
    text-decoration: underline !important;
}

/* sections */
.section {
    margin-bottom: 50px;
}

.section-title {
    font-size: 1.3rem !important;
    color: #8B4513 !important;
    margin-bottom: 25px !important;
    font-weight: normal;
    border-bottom: 1px solid #e0e0e0;
    padding-bottom: 8px;
}

/* bio text */
.bio-text {
    font-size: 16px;
    line-height: 1.7;
    color: #444;
    text-align: justify;
}

.bio-text p {
    margin-bottom: 20px;
}

/* research items */
.research-category {
    margin-bottom: 35px;
}

.category-title {
    font-size: 14px;
    color: #8B4513;
    text-transform: lowercase;
    letter-spacing: 0.5px;
    margin-bottom: 15px;
    font-weight: bold;
}

.research-item {
    margin-bottom: 20px;
    padding: 15px 0;
    border-bottom: 1px solid #f0f0f0;
}

.research-item:last-child {
    border-bottom: none;
}

.research-title {
    font-style: italic;
    color: #333;
    margin-bottom: 5px;
    line-height: 1.4;
    cursor: pointer;
    transition: color 0.3s ease;
}

.research-title:hover {
    color: #8B4513;
}

.research-details {
    font-size: 14px;
    color: #666;
    line-height: 1.5;
}

/* expandable content */
.expandable {
    cursor: pointer;
    position: relative;
}

.expandable:after {
    content: "▼";
    float: right;
    color: #8B4513;
    font-size: 12px;
    transition: transform 0.3s ease;
}

.expandable.expanded:after {
    transform: rotate(180deg);
}

.expandable-content {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
    margin-top: 10px;
}

.expandable.expanded .expandable-content {
    max-height: 1000px;
}

.abstract {
    font-size: 14px;
    line-height: 1.6;
    color: #555;
    text-align: justify;
    padding: 15px 0;
    border-left: 3px solid #f0f0f0;
    padding-left: 15px;
    margin-top: 10px;
}

.abstract p {
    margin-bottom: 15px;
}

/* experience */
.experience-item {
    margin-bottom: 30px;
    padding-bottom: 20px;
    border-bottom: 1px solid #f0f0f0;
}

.experience-item:last-child {
    border-bottom: none;
}

.experience-header {
    margin-bottom: 10px;
}

.experience-title {
    font-weight: bold;
    color: #333;
    font-size: 16px;
}

.experience-org {
    color: #8B4513;
    font-style: italic;
    margin: 5px 0;
}

.experience-date {
    font-size: 14px;
    color: #999;
    float: right;
}

.experience-description {
    font-size: 14px;
    color: #555;
    line-height: 1.5;
    clear: both;
}

.experience-description ul {
    list-style: none !important;
    margin-top: 10px;
}

.experience-description li {
    margin: 5px 0;
    position: relative;
    padding-left: 15px;
}

.experience-description li:before {
    content: "•";
    position: absolute;
    left: 0;
    color: #8B4513;
}

/* skills */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
}

.skill-category {
    padding: 20px 0;
}

.skill-category h4 {
    font-size: 14px;
    color: #8B4513;
    text-transform: lowercase;
    letter-spacing: 0.5px;
    margin-bottom: 10px;
    font-weight: bold;
    border-bottom: 1px solid #f0f0f0;
    padding-bottom: 5px;
}

.skill-list {
    font-size: 14px;
    color: #555;
    line-height: 1.6;
}

/* mobile */
@media (max-width: 768px) {
    .container {
        padding: 20px;
    }

    .main-content {
        grid-template-columns: 1fr;
        gap: 30px;
    }

    .sidebar {
        border-right: none;
        border-bottom: 1px solid #e0e0e0;
        padding-right: 0;
        padding-bottom: 30px;
    }

    .name {
        font-size: 1.8rem !important;
    }

    .nav a {
        margin: 0 15px;
        font-size: 14px;
    }

    .skills-grid {
        grid-template-columns: 1fr;
        gap: 20px;
    }

    .profile-image {
        width: 150px;
        height: 150px;
        font-size: 2rem;
    }
}

/* subtle hover effects */
.research-item:hover {
    background: rgba(139, 69, 19, 0.02);
    padding: 15px;
    margin: 0 -15px;
    border-radius: 4px;
}

.experience-item:hover {
    background: rgba(139, 69, 19, 0.02);
    padding: 20px 15px;
    margin: 0 -15px 30px -15px;
    border-radius: 4px;
}

/* Override GitHub Pages default styles */
.markdown-body {
    font-family: 'Georgia', 'Times New Roman', serif !important;
    background: #fdfdfd !important;
    color: #333 !important;
}

.markdown-body h1, .markdown-body h2, .markdown-body h3 {
    border-bottom: none !important;
}
</style>

<div class="container">

<!-- header -->
<div class="header">
<h1 class="name">akira keene teotrakool</h1>
<p class="subtitle">class researcher of transnational digital cultures</p>
<nav class="nav">
<a href="#about">about</a>
<a href="#research">research</a>
<a href="#experience">experience</a>
<a href="#contact">contact</a>
</nav>
</div>

<!-- main content -->
<div class="main-content">

<!-- sidebar -->
<div class="sidebar">
<div class="profile-image">
👥
</div>

<div class="contact-info">
<p><strong>email</strong></p>
<p><a href="mailto:teotrako@grinnell.edu">teotrako@grinnell.edu</a></p>
<br>
<p><strong>phone</strong></p>
<p>+1-641-643-0139</p>
<br>
<p><strong>address</strong></p>
<p>1115 8th ave #4900<br>grinnell, ia 50112</p>
<br>
<p><strong>pronouns</strong></p>
<p>they/them</p>
</div>

<div class="section">
<h3 class="section-title">interests & qualifications</h3>
<div class="skills-grid">
<div class="skill-category">
<h4>research interests</h4>
<div class="skill-list">political psychology, economic sociology, elites and international education, transnationalism, digital populism in southeast asia</div>
</div>

<div class="skill-category">
<h4>methodologies</h4>
<div class="skill-list">multi-sited/digital ethnography, narrative inquiry, causal inference</div>
</div>

<div class="skill-category">
<h4>software</h4>
<div class="skill-list">spss (beginner), r-studio (beginner), arcgis pro (intermediate)</div>
</div>

<div class="skill-category">
<h4>languages</h4>
<div class="skill-list">english (native), thai (native), italian (intermediate), german (beginner)</div>
</div>
</div>
</div>
</div>

<!-- main content area -->
<div class="content">

<!-- about section -->
<div id="about" class="section">
<h2 class="section-title">about</h2>
<div class="bio-text">
<p>I am a rising sophomore at <a href="https://www.grinnell.edu" style="color: #8B4513;">Grinnell College</a> studying Social Research and Analysis through an independent major. My research is informed by political psychology, economic sociology, and critical media studies to examine class identity and affect in urban youth cultures across Southeast Asia.</p>

<p>My work focuses on two primary projects: "Educational Sequencing as Class Strategy," investigating how decisions to pursue higher education abroad affect human capital formation and class reproduction among Thai international students; and "Subcultural Economies of Addictive Glamorization," exploring Thai urban identity formation through aspirational femininity.</p>

<p>In a past life in Thailand, I worked as a creative event organizer, policy advocate for the Thai Student Union, and Philosophy-for/with-Children facilitator via the Philosophy and Religion Society of Thailand.</p>

<p>I plan to pursue a PhD in Sociology, Public Policy, or Political Economy with further study in Curatorial Practice, to program national accessibility to cultural and creative spaces in Southeast Asia.</p>
</div>
</div>

<!-- research section -->
<div id="research" class="section">
<h2 class="section-title">research</h2>

<div class="research-category">
<div class="category-title">selected peer-reviewed publications</div>

<div class="research-item">
<div class="research-title">"Addictive Glamorization: Enterprising Influencers and the Reimagining of Thai Urban Identity through Aspirational Femininity"</div>
<div class="research-details">In <em>Influencer and Gender Politics in Southeast Asia</em>, edited by Annisa Beta, Hao Zheng, and Crystal Abidin. (forthcoming 2026)</div>
</div>

<div class="research-item">
<div class="research-title">"Trans Cinema from Thailand"</div>
<div class="research-details">with Shaka McGlotten. <em>Routledge Handbook of Trans Cinema</em>, edited by Douglas A. Vakoch, Routledge. (forthcoming 2026)</div>
</div>

<div class="research-item">
<div class="research-title">"Political Psychology in Thailand: Future Avenues for Examining Emotions in Thai Politics"</div>
<div class="research-details">Revise and Resubmit at <em>Journal of Social and Political Psychology</em>. Supervised by Dr. Brandon Ng and Dr. Courtney Nava, Grinnell College.</div>
</div>

<div class="research-item">
<div class="research-title">"Transnational Agitprop as Feminist Methodology: Twitter 'Protest-Learning' and Political Issue Formation in Thailand's 2020-21 Anti-Government Protests"</div>
<div class="research-details">Under review at <em>Asiascapes: Digital Asia, Special Issue on "Networked Agitprop"</em>.</div>
</div>
</div>

<div class="research-category">
<div class="category-title">working papers</div>

<div class="research-item">
<div class="research-title expandable" onclick="toggleContent(this)">"Educational Sequencing as Class Strategy: Thai Undergraduate and Graduate Student Cohesion in Elite U.S. Universities"</div>
<div class="research-details">with Archawin Kittirattanapaiboon</div>
<div class="expandable-content">
<div class="abstract">
<p>What happens when students from the same country arrive at elite U.S. universities through different educational routes—and why do these pathways matter more than shared cultural identity for determining social belonging? This paper examines internal group cohesion dynamics among Thai students at elite U.S. universities, exploring how educational pathways reproduce class stratification and privilege.</p>
<p>This paper hypothesizes that undergraduate Thai students in the U.S., often from families with long-standing elite status, benefit from early exposure to international schooling and develop distinct forms of cultural and social capital. In contrast, graduate students, who typically hold Thai bachelor's degrees, face greater difficulty aligning with the class practices of their undergraduate peers.</p>
<p>Building on existing arguments about international education as a site of class reproduction, we reveal how Thailand has witnessed a growing shift in elite educational strategies. Whereas a decade ago many families pursued graduate studies abroad after domestic bachelor's studies, fulfilling the "graduated from abroad" (jop nok) ideal, elite families now increasingly send children to international schools to pursue undergraduate degrees abroad. This paper challenges dominant narratives about international education as opportunity and highlights its role in reinforcing social inequalities.</p>
</div>
</div>
</div>

<div class="research-item">
<div class="research-title expandable" onclick="toggleContent(this)">"Subcultural Economies of Addictive Glamorization in Bangkok's Middle-Class Youths"</div>
<div class="research-details">with Napat Arjananont and Jack Thornton</div>
<div class="expandable-content">
<div class="abstract">
<p>In contemporary Bangkok, a distinct entrepreneurial niche has emerged among female influencers educated at elite international schools in the Silom–Asoke corridor. These "dek inter" (internationally educated) influencers deploy enterprise self-branding, visual digital media, and business ventures to reinforce high-class entrepreneurial feminine values.</p>
<p>This aspirational femininity manifests in distinctive consumption patterns: Triam Udom Suksa students receive boutique-packaged Thai tea cakes via Grab delivery at school gates; Chulalongkorn interns unwind over Spanish tapas at The Commons; Longchamp bags rest casually on metal sheet tables at street-side Isaan restaurants.</p>
<p>Thai youth describe this phenomenon as "tid glam" (addictive glamorization), a relationship wherein individuals from lower socioeconomic backgrounds become symbolically invested in content marketed aspirationally by those from higher strata. The content creators project an entrepreneurial femininity that fuses business acumen with traditionally "glam" feminine aesthetic and relational qualities.</p>
</div>
</div>
</div>

<div class="research-item">
<div class="research-title">"Not Quite at Home, Not Quite Alone: Comparing Group Cohesion and Social Identity Between 'Rare Birds' and Dominant International Student Groups at an Elite Liberal Arts College"</div>
<div class="research-details">Data collection in progress.</div>
</div>
</div>
</div>

<!-- experience section -->
<div id="experience" class="section">
<h2 class="section-title">experience</h2>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">Organizer and Executive Committee Member</div>
<div class="experience-date">Mar 2023 — Present</div>
<div class="experience-org">Rosenfield Program in Public Affairs, Grinnell College</div>
</div>
<div class="experience-description">
<ul>
<li>Coordinated symposia, guest speakers, program study trips, and sponsored campus events on public affairs, international relations, and human rights in collaboration with team of five peers and five faculty advisors.</li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">Head of Institutional Outreach and Programming</div>
<div class="experience-date">Nov 2024 — Present</div>
<div class="experience-org">Association of Thai Students in the United States of America</div>
</div>
<div class="experience-description">
<ul>
<li>Designed and implemented online programs easing Thai students' cultural transition to U.S. academic life and strengthening community engagement.</li>
<li>Launched a research seminar series and mentorship programs connecting undergraduates with Thai graduate students across disciplines.</li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">Staff Writer</div>
<div class="experience-date">Jan 2023 — Present</div>
<div class="experience-org">The Scarlet and Black, Grinnell College</div>
</div>
<div class="experience-description">
<ul>
<li><a href="https://thesandb.com/51343/features/reflecting-on-southeast-asian-identity-after-faculty-trip-email/" style="color: #8B4513;">Reflecting on Southeast Asian identity after faculty trip email</a></li>
<li><a href="https://thesandb.com/51061/features/sustainability-initiatives-think-beyond-recycling-advocate-for-education-and-institutional-memory/" style="color: #8B4513;">Sustainability initiatives think beyond recycling, advocate for education and institutional memory</a></li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">Co-founding Member and Fieldwork Coordinator</div>
<div class="experience-date">May 2021 — Jul 2023</div>
<div class="experience-org">Thailand Student Union</div>
</div>
<div class="experience-description">
<ul>
<li>Co-founded student organization aimed at centralizing a network of arising youth organizations in Thailand to shed light on less-represented issues in Thai educational politics.</li>
<li>Supervised field safety and legal counsel for active student demonstrators at Ministry of Education.</li>
<li>Organized 8-week policy study group on 2021-22 National Education Act with direction from legal-educational professionals.</li>
</ul>
</div>
</div>

<div class="experience-item">
<div class="experience-header">
<div class="experience-title">Philosophy for/with Children Facilitator</div>
<div class="experience-date">May 2022 — Dec 2023</div>
<div class="experience-org">Philosophy and Religion Society of Thailand</div>
</div>
<div class="experience-description">
<ul>
<li>Trained Practitioner in Philosophy for/with Children (P4wC) techniques through Philosophy with Children and Youth Network for Asia and the Pacific (PCYNAP) workshops.</li>
<li>Facilitated 2 workshops for youths aged 8-12 & 13-18 with supervision from Mahidol University faculty.</li>
</ul>
</div>
</div>
</div>

</div>
</div>

<div style="text-align: center; margin-top: 50px; padding-top: 30px; border-top: 1px solid #e0e0e0; font-size: 14px; color: #999; font-style: italic;">
References available upon request.
</div>

</div>

<script>
function toggleContent(element) {
    element.classList.toggle('expanded');
}

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
</script>
