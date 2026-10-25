
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Developer Profile</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: radial-gradient(circle at top, #211044, #080b18 65%);
  font-family: "Segoe UI", sans-serif;
  color: #f8fafc;
  padding: 30px;
}

.profile {
  width: min(100%, 1000px);
  padding: 45px;
  position: relative;
  overflow: hidden;
  border: 1px solid rgba(167, 139, 250, .3);
  border-radius: 28px;
  background: linear-gradient(135deg, #11152c, #17112f 60%, #0c2636);
  box-shadow: 0 25px 80px #0009, 0 0 35px #7c3aed20;
}

.profile::before {
  content: "";
  position: absolute;
  width: 300px;
  height: 300px;
  right: -100px;
  top: -120px;
  background: #7c3aed;
  filter: blur(110px);
  opacity: .4;
}

.content {
  position: relative;
  z-index: 1;
  display: grid;
  grid-template-columns: 1.3fr .7fr;
  align-items: center;
  gap: 35px;
}

.tag {
  display: inline-block;
  padding: 9px 15px;
  border: 1px solid #8b5cf6;
  border-radius: 30px;
  color: #c4b5fd;
  background: #8b5cf61a;
  font-size: 12px;
  letter-spacing: 2px;
  margin-bottom: 22px;
}

h1 {
  font-size: clamp(38px, 6vw, 68px);
  line-height: 1.05;
  letter-spacing: -2px;
  margin-bottom: 16px;
}

h1 span {
  background: linear-gradient(90deg, #c4b5fd, #67e8f9);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.subtitle {
  color: #a5b4fc;
  font-size: 18px;
  margin-bottom: 20px;
}

.description {
  max-width: 520px;
  color: #cbd5e1;
  line-height: 1.8;
  font-size: 15px;
}

.skills {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 25px;
}

.skills span {
  padding: 9px 13px;
  border-radius: 10px;
  background: #ffffff0a;
  border: 1px solid #ffffff18;
  color: #e0e7ff;
  font-size: 13px;
}

.art {
  display: flex;
  align-items: center;
  justify-content: center;
  perspective: 800px;
  min-height: 280px;
}

.cube {
  width: 160px;
  height: 160px;
  position: relative;
  transform-style: preserve-3d;
  animation: rotate 12s infinite linear;
}

.face {
  position: absolute;
  width: 160px;
  height: 160px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 42px;
  font-weight: 800;
  color: #e0f2fe;
  border: 2px solid #67e8f9;
  background: linear-gradient(135deg, #7c3aed88, #0891b288);
  box-shadow: inset 0 0 30px #67e8f933, 0 0 25px #8b5cf644;
  backdrop-filter: blur(8px);
}

.front  { transform: translateZ(80px); }
.back   { transform: rotateY(180deg) translateZ(80px); }
.right  { transform: rotateY(90deg) translateZ(80px); }
.left   { transform: rotateY(-90deg) translateZ(80px); }
.top    { transform: rotateX(90deg) translateZ(80px); }
.bottom { transform: rotateX(-90deg) translateZ(80px); }

@keyframes rotate {
  from { transform: rotateX(-20deg) rotateY(0deg); }
  to   { transform: rotateX(340deg) rotateY(360deg); }
}

.footer {
  position: relative;
  z-index: 1;
  border-top: 1px solid #ffffff1c;
  margin-top: 35px;
  padding-top: 22px;
  display: flex;
  justify-content: space-between;
  gap: 15px;
  flex-wrap: wrap;
  color: #94a3b8;
  font-size: 13px;
}

.footer strong {
  color: #67e8f9;
}

@media (max-width: 700px) {
  .profile { padding: 28px 22px; }
  .content { grid-template-columns: 1fr; }
  .art { min-height: 240px; }
  .cube {
    transform: scale(.8);
  }
  .footer { flex-direction: column; }
}
</style>
</head>

<body>
<main class="profile">

  <div class="content">
    <section>
      <div class="tag">✦ DEVELOPER • COMMUNITY BUILDER</div>

      <h1>Building<br><span>Beyond Limits.</span></h1>

      <p class="subtitle">
        Community Manager @ Hacker's Unity
      </p>

      <p class="description">
        Exploring technology, building meaningful projects,
        bringing people together through hackathons, and
        turning creative ideas into real-world solutions.
      </p>

      <div class="skills">
        <span>Python</span>
        <span>C / C++</span>
        <span>AI & Cloud</span>
        <span>Git & GitHub</span>
        <span>Hackathons</span>
      </div>
    </section>

    <div class="art">
      <div class="cube">
        <div class="face front">DEV</div>
        <div class="face back">AI</div>
        <div class="face right">&lt;/&gt;</div>
        <div class="face left">{ }</div>
        <div class="face top">✦</div>
        <div class="face bottom">01</div>
      </div>
    </div>
  </div>

  <div class="footer">
    <span><strong>50+</strong> Hackathons</span>
    <span><strong>6+</strong> Podcasts Hosted</span>
    <span><strong>2×</strong> Hackathon Organizer</span>
    <span>Made with curiosity ✦</span>
  </div>

</main>
</body>
</html>
