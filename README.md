# akira keene teotrakool
---

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Georgia', 'Times New Roman', serif !important;
    background: #f0f7ff !important;
    color: #333 !important;
    font-size: 14px !important;
    line-height: 1.5 !important;
    overflow-x: hidden;
}

.cursor-trail {
    position: fixed;
    width: 20px;
    height: 20px;
    background: rgba(70, 130, 180, 0.3);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
    transition: all 0.1s ease;
}

.container {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px 20px 20px 200px;
}

/* left navigation */
.nav-left {
    position: fixed;
    left: 0;
    top: 0;
    height: 100vh;
    width: 180px;
    background: rgba(240, 247, 255, 0.95);
    border-right: 2px dashed #4682b4;
    padding: 30px 20px;
    z-index: 1000;
    overflow-y: auto;
}

.nav-title {
    font-size: 14px;
    font-weight: bold;
    color: #4682b4;
    margin-bottom: 20px;
    text-transform: lowercase;
    letter-spacing: 0.5px;
}

.nav-left a {
    display: block;
    color: #4682b4 !important;
    text-decoration: none !important;
    margin: 12px 0;
    padding: 8px 12px;
    position: relative;
    border-radius: 4px;
    transition: all 0.3s ease;
    font-size: 13px;
}

.nav-left a:hover {
    background: rgba(70, 130, 180, 0.1);
    color: #1e90ff !important;
    transform: translateX(5px);
}

.nav-left a:before {
    content: "→ ";
    opacity: 0;
    transition: opacity 0.3s ease;
    color: #87ceeb;
}

.nav-left a:hover:before {
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
    font-weight: normal !important;
    color: #4682b4 !important;
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
        #4682b4 0px,
        #4682b4 10px,
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
    color: #4682b4;
    font-family: Georgia, serif;
    font-size: 12px;
    user-select: none;
}

/* content blocks */
.content-block {
    background: rgba(255, 255, 255, 0.8);
    border: 1px solid #b0d4f1;
    margin: 30px 0;
    padding: 25px;
    position: relative;
    transform: rotate(0deg);
    transition: all 0.3s ease;
    border-radius: 8px;
}

.content-block:nth-child(odd) {
    transform: rotate(0.3deg);
    border-style: dashed;
}

.content-block:nth-child(even) {
    transform: rotate(-0.2deg);
    border-style: dotted;
}

.content-block:hover {
    transform: rotate(0deg) scale(1.01);
    box-shadow: 0 8px 25px rgba(70, 130, 180, 0.15);
    z-index: 10;
}

.section-title {
    font-size: 1.3rem !important;
    color: #4682b4 !important;
    margin-bottom: 20px !important;
    text-transform: lowercase;
    position: relative;
    display: inline-block;
    font-weight: normal;
}

.section-title:before {
    content: "◆ ";
    color: #87ceeb;
}

/* research items */
.research-item {
    margin: 20px 0;
    padding: 18px;
    background: rgba(240, 247, 255, 0.6);
    border-left: 3px solid #4682b4;
    position: relative;
    border-radius: 4px;
}

.research-status {
    font-size: 11px;
    color: #1e90ff;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 10px;
    font-weight: bold;
}

.research-title {
    font-style: italic;
    color: #333;
    margin-bottom: 10px;
    line-height: 1.4;
    cursor: pointer;
    transition: color 0.3s ease;
}

.research-title:hover {
    color: #4682b4;
}

.research-details {
    font-size: 13px;
    color: #666;
    line-height: 1.5;
}

/* expandable working papers */
.working-paper {
    border: 1px solid #b0d4f1;
    border-radius: 8px;
    margin: 15px 0;
    overflow: hidden;
    transition: all 0.3s ease;
}

.working-paper-header {
    padding: 15px;
    background: rgba(70, 130, 180, 0.05);
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
    transition: background 0.3s ease;
}

.working-paper-header:hover {
    background: rgba(70, 130, 180, 0.1);
}

.working-paper-title {
    font-style: italic;
    color: #4682b4;
    font-size: 14px;
    font-weight: normal;
}

.expand-icon {
    color: #87ceeb;
    font-size: 18px;
    transition: transform 0.3s ease;
}

.working-paper.expanded .expand-icon {
    transform: rotate(180deg);
}

.working-paper-content {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
    padding: 0 15px;
}

.working-paper.expanded .working-paper-content {
    max-height: 1000px;
    padding: 0 15px 20px 15px;
}

.working-paper-abstract {
    font-size: 13px;
    line-height: 1.6;
    color: #555;
    text-align: justify;
}

.working-paper-abstract p {
    margin-bottom: 15px;
}

/* experience */
.experience-item {
    margin: 25px 0;
    padding: 22px;
    background: rgba(255, 255, 255, 0.9);
    border: 2px solid #b0d4f1;
    position: relative;
    border-radius: 8px;
}

.experience-item:before {
    content: "";
    position: absolute;
    top: -2px;
    left: -2px;
    right: -2px;
    bottom: -2px;
    background: linear-gradient(45deg, #4682b4, #87ceeb, #4682b4);
    z-index: -1;
    opacity: 0;
    transition: opacity 0.3s ease;
    border-radius: 8px;
}

.experience-item:hover:before {
    opacity: 0.3;
}

.experience-header {
    margin-bottom: 12px;
}

.experience-title {
    font-weight: bold;
    color: #4682b4;
    text-transform: lowercase;
    font-size: 15px;
}

.experience-org {
    color: #666;
    font-style: italic;
    margin: 5px 0;
    font-size: 14px;
}

.experience-date {
    font-size: 11px;
    color: #999;
    float: right;
    transform: rotate(1deg);
}

.experience-details {
    font-size: 13px;
    color: #555;
    line-height: 1.5;
}

.experience-details ul {
    list-style: none !important;
    margin-top: 10px;
}

.experience-details li {
    margin: 8px 0;
    position: relative;
    padding-left: 20px;
}

.experience-details li:before {
    content: "•";
    position: absolute;
    left: 0;
    color: #4682b4;
    font-weight: bold;
}

/* bio section */
.bio-text {
    font-size: 15px;
    line-height: 1.7;
    color: #444;
    text-align: justify;
    columns: 2;
    column-gap: 35px;
    column-rule: 1px dashed #b0d4f1;
}

.bio-text p {
    margin-bottom: 18px;
    break-inside: avoid;
}

/* skills grid */
.skills-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-top: 25px;
}

.skill-box {
    background: rgba(255, 255, 255, 0.9);
    border: 1px solid #b0d4f1;
    padding: 18px;
    text-align: center;
    transform: rotate(0.5deg);
    transition: all 0.3s ease;
    border-radius: 8px;
}

.skill-box:nth-child(even) {
    transform: rotate(-0.5deg);
}

.skill-box:hover {
    transform: rotate(0deg) scale(1.02);
    border-color: #4682b4;
    box-shadow: 0 5px 15px rgba(70, 130, 180, 0.1);
}

.skill-category {
    font-size: 12px;
    color: #4682b4;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 12px;
    font-weight: bold;
}

.skill-list {
    font-size: 13px;
    color: #555;
    line-height: 1.5;
}

/* contact section */
.contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 25px;
}

.contact-item {
    background: rgba(240, 247, 255, 0.8);
    border: 2px dashed #4682b4;
    padding: 18px;
    text-align: center;
    transform: rotate(-0.5deg);
    transition: all 0.3s ease;
    border-radius: 8px;
}

.contact-item:nth-child(even) {
    transform: rotate(0.5deg);
}

.contact-item:hover {
    transform: rotate(0deg);
    background: rgba(255, 255, 255, 0.95);
    box-shadow: 0 5px 15px rgba(70, 130, 180, 0.1);
}

.contact-label {
    font-size: 11px;
    color: #4682b4;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 10px;
    font-weight: bold;
}

.contact-value {
    color: #333;
    font-size: 13px;
    line-height: 1.4;
}

.contact-value a {
    color: #4682b4 !important;
    text-decoration: none !important;
}

.contact-value a:hover {
    color: #1e90ff !important;
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
    0%, 100% { transform: translateY(0px) rotate(0.5deg); }
    50% { transform: translateY(-3px) rotate(-0.5deg); }
}

.floating {
    animation: float 8s ease-in-out infinite;
}

/* mobile */
@media (max-width: 768px) {
    .nav-left {
        position: relative;
        width: 100%;
        height: auto;
        border-right: none;
        border-bottom: 2px dashed #4682b4;
        margin-bottom: 20px;
    }

    .container {
        padding: 20px;
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
    color: #4682b4;
    font-size: 2.5rem;
    font-weight: normal;
    text-transform: lowercase;
    letter-spacing: -0.02em;
    animation: glitch 3s linear infinite;
}

@keyframes glitch {
    2%, 64% {
        transform: translate(1px, 0) skew(0deg);
    }
    4%, 60% {
        transform: translate(-1px, 0) skew(0deg);
    }
    62% {
        transform: translate(0, 0) skew(2deg);
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
    animation: glitch 3s linear infinite;
    color: #87ceeb;
    z-index: -1;
}

.glitch:after {
    animation: glitch 3s linear infinite;
    color: #4682b4;
    z-index: -2;
}

/* Override GitHub Pages default styles */
.markdown-body {
    font-family: 'Georgia', 'Times New Roman', serif !important;
    background: #f0f7ff !important;
    color: #333 !important;
}

.markdown-body h1, .markdown-body h2, .markdown-body h3 {
    border-bottom: none !important;
}
</style>

<div class="cursor-trail"></div>

<!-- left navigation -->
<div class="nav-left">
<div class="nav-title">navigate</div>
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

<div class="working-paper" onclick="togglePaper(this)">
<div class="working-paper-header">
<div class="working-paper-title">"educational sequencing as class strategy: thai undergraduate and graduate student cohesion in elite u.s. universities"</div>
<div class="expand-icon">▼</div>
</div>
<div class="working-paper-content">
<div class="working-paper-abstract">
<p><em>with archawin kittirattanapaiboon</em></p>
<p>What happens when students from the same country arrive at elite U.S. universities through different educational routes—and why do these pathways matter more than shared cultural identity for determining social belonging? This paper examines internal group cohesion dynamics among Thai students at elite U.S. universities, exploring how educational pathways reproduce class stratification and privilege.</p>
<p>This paper hypothesizes that undergraduate Thai students in the U.S., often from families with long-standing elite status, benefit from early exposure to international schooling and develop distinct forms of cultural and social capital. In contrast, graduate students, who typically hold Thai bachelor's degrees, face greater difficulty aligning with the class practices of their undergraduate peers.</p>
<p>Building on existing arguments about international education as a site of class reproduction, we reveal how Thailand has witnessed a growing shift in elite educational strategies. Whereas a decade ago many families pursued graduate studies abroad after domestic bachelor's studies, fulfilling the "graduated from abroad" (jop nok) ideal, elite families now increasingly send children to international schools to pursue undergraduate degrees abroad. Consequently, graduate students with Thai bachelor's degrees find themselves less able to share the same class practices as their undergraduate counterparts. This paper challenges dominant narratives about international education as opportunity and highlights its role in reinforcing social inequalities.</p>
</div>
</div>
</div>

<div class="working-paper" onclick="togglePaper(this)">
<div class="working-paper-header">
<div class="working-paper-title">"addictive glamorization: enterprising influencers and the reimagining of thai urban identity through aspirational femininity"</div>
<div class="expand-icon">▼</div>
</div>
<div class="working-paper-content">
<div class="working-paper-abstract">
<p>In contemporary Bangkok, a distinct entrepreneurial niche has emerged among female influencers educated at elite international schools in the Silom–Asoke corridor. These "dek inter" (internationally educated) influencers deploy enterprise self-branding, visual digital media, and business ventures to reinforce high-class entrepreneurial feminine values. Their content simultaneously produces and transmits affects of aspirational femininity to young audiences who often possess substantial economic privilege, though less entrenched than that of the content creators themselves.</p>
<p>This aspirational femininity manifests in distinctive consumption patterns: Triam Udom Suksa students receive boutique-packaged Thai tea cakes via Grab delivery at school gates; Chulalongkorn interns unwind over Spanish tapas at The Commons; Longchamp bags rest casually on metal sheet tables at street-side Isaan restaurants.</p>
<p>Thai youth describe this phenomenon as "tid glam" (addictive glamorization), a relationship wherein individuals from lower socioeconomic backgrounds become symbolically invested in content marketed aspirationally by those from higher strata. What distinguishes this dynamic from conventional celebrity influence or aspirational marketing is its specifically gendered dimension within the Thai context. The content creators project an entrepreneurial femininity that fuses business acumen with traditionally "glam" feminine aesthetic and relational qualities. Their audience—predominantly middle-class high school students—consumes this content not merely as entertainment but as instructional material for potential social mobility and cultural critique.</p>
</div>
</div>
</div>

<div class="working-paper" onclick="togglePaper(this)">
<div class="working-paper-header">
<div class="working-paper-title">"political psychology in thailand: future avenues for examining emotions in thai politics"</div>
<div class="expand-icon">▼</div>
</div>
<div class="working-paper-content">
<div class="working-paper-abstract">
<p><em>Revise and Resubmit, Journal of Social and Political Psychology</em></p>
<p>This paper presents a critical review of political psychology in Thailand, addressing a significant gap in a discipline dominated by Western, Educated, Industrialized, Rich, and Democratic (WEIRD) populations. Thailand's complex political landscape offers fertile ground for expanding political psychology's theoretical horizons through its institutional volatility, color-coded movements, religious influences, and emerging digital activism.</p>
<p>This analysis examines how existing theoretical frameworks require fundamental reconsideration when applied to Thai contexts. Drawing on established literature and recent research, this paper identifies six interconnected dimensions warranting further investigation: (1) the emotional underpinnings of Thailand's factional politics; (2) the impact of Buddhist cultural contexts on political trust and legitimacy perceptions; (3) the evolving dynamics of youth political socialization through digital platforms; (4) the psychological mechanisms that sustain institutional relationships despite governance challenges; (5) the relationship between religious identity and political attitudes; and (6) evidence-based approaches to mitigating polarization.</p>
<p>By critically examining the methodological and conceptual limitations of existing research and proposing the Thai Political Affect-Identity-Institution Framework (TPAIM), this study contributes to the development of culturally informed political psychology theories while offering insights into Thailand's ongoing political challenges.</p>
</div>
</div>
</div>

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

// expandable working papers
function togglePaper(element) {
    element.classList.toggle('expanded');
}

// random rotation on page load
function randomizeRotations() {
    const blocks = document.querySelectorAll('.content-block');
    blocks.forEach((block, index) => {
        const randomRotation = (Math.random() - 0.5) * 1;
        block.style.transform = `rotate(${randomRotation}deg)`;
    });
}

// call on load
window.addEventListener('load', randomizeRotations);

// add some randomness to skill boxes
const skillBoxes = document.querySelectorAll('.skill-box');
skillBoxes.forEach(box => {
    const randomRotation = (Math.random() - 0.5) * 2;
    box.style.transform = `rotate(${randomRotation}deg)`;
});
</script>
