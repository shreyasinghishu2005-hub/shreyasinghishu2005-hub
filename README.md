
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shreya Singh | Developer Profile</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap');

:root {
  --bg: #090812;
  --panel: #13101f;
  --purple: #a78bfa;
  --lavender: #d8ccff;
  --text: #f6f3ff;
  --muted: #aaa4bd;
  --line: rgba(210, 194, 255, .13);
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  background:
    radial-gradient(ellipse at 15% 0%, #291744 0%, transparent 38%),
    var(--bg);
  color: var(--text);
  font-family: 'DM Sans', sans-serif;
  line-height: 1.7;
  padding: 32px 18px;
}

a {
  color: inherit;
  text-decoration: none;
}

.page {
  max-width: 1050px;
  margin: auto;
}

/* Navigation */

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
  margin-bottom: 24px;
}

.logo {
  font-family: 'Space Grotesk', sans-serif;
  font-weight: 700;
  letter-spacing: -.5px;
}

.logo span {
  color: var(--purple);
}

.nav-label {
  font-size: 12px;
  color: var(--muted);
  letter-spacing: 2px;
}

/* Main glass panel */

.hero {
  position: relative;
  overflow: hidden;
  border: 1px solid var(--line);
  border-radius: 26px;
  background: linear-gradient(
    130deg,
    rgba(32, 25, 48, .94),
    rgba(16, 14, 27, .97) 65%,
    rgba(37, 22, 54, .8)
  );
  padding: clamp(28px, 6vw, 64px);
  box-shadow: 0 25px 70px rgba(0, 0, 0, .25);
}

.hero::after {
  content: "";
  position: absolute;
  top: -150px;
  right: -100px;
  width: 350px;
  height: 350px;
  border-radius: 50%;
  background: rgba(139, 92, 246, .09);
  filter: blur(50px);
  pointer-events: none;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.35fr .65fr;
  align-items: center;
  gap: 35px;
  position: relative;
  z-index: 1;
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 9px;
  color: #c9b8ff;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 22px;
}

.eyebrow::before {
  content: "";
  width: 22px;
  height: 1px;
  background: var(--purple);
}

h1 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: clamp(43px, 7vw, 76px);
  line-height: 1.04;
  letter-spacing: -3px;
  font-weight: 600;
}

h1 span {
  display: block;
  color: var(--purple);
}

.intro {
  color: var(--muted);
  font-size: 16px;
  margin-top: 22px;
  max-width: 470px;
}

.role {
  margin-top: 15px;
  font-size: 14px;
  color: #e4dcff;
}

.actions {
  display: flex;
  flex-wrap: wrap;
  gap: 11px;
  margin-top: 28px;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 9px;
  padding: 11px 17px;
  border: 1px solid var(--line);
  border-radius: 10px;
  font-size: 13px;
  font-weight: 600;
  transition: .2s ease;
}

.btn-primary {
  background: #c4b5fd;
  color: #171023;
  border-color: #c4b5fd;
}

.btn:hover {
  transform: translateY(-2px);
  border-color: var(--purple);
}

/* Static 3D glass artwork */

.art {
  min-height: 270px;
  display: flex;
  align-items: center;
  justify-content: center;
  perspective: 800px;
}

.glass-shape {
  width: 205px;
  height: 225px;
  position: relative;
  transform: rotate(-9deg) rotateY(-12deg);
  border: 1px solid rgba(230, 220, 255, .48);
  border-radius: 32px 55px 35px 55px;
  background:
    linear-gradient(140deg,
      rgba(255,255,255,.21),
      rgba(167,139,250,.08) 42%,
      rgba(86,45,137,.24));
  box-shadow:
    inset 1px 1px 1px rgba(255,255,255,.3),
    inset -12px -12px 28px rgba(94,54,150,.15),
    16px 22px 45px rgba(0,0,0,.25);
  backdrop-filter: blur(12px);
}

.glass-shape::before {
  content: "";
  position: absolute;
  inset: 15px;
  border: 1px solid rgba(221, 208, 255, .26);
  border-radius: 23px 40px 25px 40px;
  background: linear-gradient(145deg,
    rgba(196,181,253,.11),
    transparent 55%);
}

.glass-shape::after {
  content: "";
  position: absolute;
  width: 105px;
  height: 105px;
  border-radius: 50%;
  top: 45px;
  left: 48px;
  background: linear-gradient(145deg, #e9ddff, #9570e7 52%, #52318d);
  box-shadow:
    inset -10px -12px 20px rgba(33,15,62,.4),
    inset 5px 5px 12px rgba(255,255,255,.7),
    0 10px 30px rgba(137,94,246,.2);
  opacity: .9;
}

.glass-caption {
  position: absolute;
  z-index: 2;
  bottom: 32px;
  left: 0;
  right: 0;
  text-align: center;
  font-family: 'Space Grotesk', sans-serif;
  font-size: 16px;
  font-weight: 700;
  letter-spacing: 5px;
  color: #fff;
  text-shadow: 0 2px 15px #6d45a9;
}

.art-caption {
  text-align: center;
  color: #9188a8;
  font-size: 11px;
  letter-spacing: 2px;
  margin-top: 25px;
}

/* Content sections */

.section {
  margin-top: 26px;
  padding: 32px;
  border: 1px solid var(--line);
  border-radius: 20px;
  background: rgba(19, 16, 31, .72);
}

.section-heading {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 22px;
}

.section-heading .number {
  color: var(--purple);
  font-size: 11px;
  letter-spacing: 1px;
}

h2 {
  font-family: 'Space Grotesk', sans-serif;
  font-size: 21px;
  font-weight: 600;
  letter-spacing: -.4px;
}

.about-text {
  color: var(--muted);
  font-size: 14px;
  max-width: 800px;
}

.highlights {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
  margin-top: 24px;
}

.highlight {
  padding: 17px;
  border-radius: 13px;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.018);
}

.highlight strong {
  display: block;
  font-family: 'Space Grotesk', sans-serif;
  font-size: 27px;
  color: var(--lavender);
  line-height: 1.3;
}

.highlight span {
  color: var(--muted);
  font-size: 12px;
}

/* Skills */

.skill-group + .skill-group {
  margin-top: 23px;
}

.skill-title {
  color: #c9b8ff;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 1px;
  text-transform: uppercase;
  margin-bottom: 12px;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 9px;
}

.skills span {
  padding: 7px 12px;
  border: 1px solid var(--line);
  border-radius: 8px;
  color: #ded7ee;
  background: rgba(167,139,250,.045);
  font-size: 12px;
}

/* Footer */

.footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 14px;
  padding: 25px 4px 5px;
  color: #8e879f;
  font-size: 12px;
}

.footer a {
  color: #c4b5fd;
}

@media (max-width: 720px) {
  body {
    padding: 18px 12px;
  }

  .hero-grid {
    grid-template-columns: 1fr;
  }

  .hero {
    padding: 30px 24px;
  }

  .art {
    min-height: 235px;
  }

  .glass-shape {
    transform: scale(.85) rotate(-9deg) rotateY(-12deg);
  }

  .highlights {
    grid-template-columns: repeat(2, 1fr);
  }

  .section {
    padding: 24px 20px;
  }

  h1 {
    letter-spacing: -2px;
  }
}
</style>
</head>

<body>
<div class="page">

  <header class="nav">
    <div class="logo">shreya<span>.</span></div>
    <div class="nav-label">DEVELOPMENT · COMMUNITY · IDEAS</div>
  </header>

  <main>

    <section class="hero">
      <div class="hero-grid">

        <div>
          <div class="eyebrow">Developer & Community Builder</div>

          <h1>Shreya<br><span>Singh.</span></h1>

          <p class="role">Community Manager · Hacker's Unity</p>

          <p class="intro">
            Exploring technology, bringing communities together,
            and turning ideas into meaningful projects through
            collaboration, creativity and continuous learning.
          </p>

          <div class="actions">
            <a class="btn btn-primary"
               href="https://github.com/shreyasinghishu2005-hub">
              Explore GitHub ↗
            </a>

            <a class="btn"
               href="https://www.linkedin.com/in/shreyasingh6294/">
              LinkedIn ↗
            </a>
          </div>
        </div>

        <div>
          <div class="art">
            <div class="glass-shape">
              <div class="glass-caption">CREATE</div>
            </div>
          </div>
          <div class="art-caption">IDEAS INTO IMPACT</div>
        </div>

      </div>
    </section>

    <section class="section">
      <div class="section-heading">
        <span class="number">01 /</span>
        <h2>A little about me</h2>
      </div>

      <p class="about-text">
        I'm a technology enthusiast interested in software development,
        artificial intelligence and cloud computing. As Community Manager
        at Hacker's Unity, I enjoy organizing tech experiences, connecting
        people and learning by building. I'm always open to collaboration,
        new ideas and opportunities to grow.
      </p>

      <div class="highlights">
        <div class="highlight">
          <strong>2×</strong>
          <span>National & Global Hackathons Organized</span>
        </div>

        <div class="highlight">
          <strong>6+</strong>
          <span>Podcasts Hosted</span>
        </div>

        <div class="highlight">
          <strong>5+</strong>
          <span>Events & Workshops Hosted</span>
        </div>

        <div class="highlight">
          <strong>50+</strong>
          <span>Hackathons Participated In</span>
        </div>

        <div class="highlight">
          <strong>Runner-up</strong>
          <span>Geo-Spatial Hackathon</span>
        </div>

        <div class="highlight">
          <strong>HU</strong>
          <span>Community Management</span>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-heading">
        <span class="number">02 /</span>
        <h2>Tech stack & tools</h2>
      </div>

      <div class="skill-group">
        <div class="skill-title">Programming & Core</div>
        <div class="skills">
          <span>Python</span>
          <span>C</span>
          <span>C++</span>
          <span>Data Structures & Algorithms</span>
          <span>Git</span>
          <span>GitHub</span>
        </div>
      </div>

      <div class="skill-group">
        <div class="skill-title">Web Development</div>
        <div class="skills">
          <span>HTML</span>
          <span>CSS</span>
          <span>JavaScript</span>
          <span>Angular</span>
          <span>Bootstrap</span>
          <span>Next.js</span>
          <span>.NET</span>
        </div>
      </div>

      <div class="skill-group">
        <div class="skill-title">Cloud & Deployment</div>
        <div class="skills">
          <span>AWS</span>
          <span>Google Cloud</span>
          <span>Vercel</span>
          <span>Render</span>
          <span>Alibaba Cloud</span>
        </div>
      </div>

      <div class="skill-group">
        <div class="skill-title">Tools & Creative Technology</div>
        <div class="skills">
          <span>Canva</span>
          <span>Figma</span>
          <span>Photoshop</span>
          <span>OpenCV</span>
          <span>SciPy</span>
          <span>Web3.js</span>
          <span>p5.js</span>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="section-heading">
        <span class="number">03 /</span>
        <h2>Find me online</h2>
      </div>

      <div class="actions">
        <a class="btn"
           href="https://github.com/shreyasinghishu2005-hub">
          GitHub ↗
        </a>

        <a class="btn"
           href="https://www.linkedin.com/in/shreyasingh6294/">
          LinkedIn ↗
        </a>

        <a class="btn"
           href="mailto:shreyasinghishu2005@gmail.com">
          Email ↗
        </a>
      </div>
    </section>

  </main>

  <footer class="footer">
    <span>Designed with intention, built with curiosity.</span>
    <a href="https://github.com/shreyasinghishu2005-hub">
      shreyasinghishu2005-hub ↗
    </a>
  </footer>

</div>
</body>
</html>
