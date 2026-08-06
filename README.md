<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Subhadip Bera GitHub profile page with a 3D modern design, skills, and social links." />
  <title>Subhadip Bera | GitHub Profile</title>
  <style>
    :root {
      --panel: rgba(11, 19, 38, 0.72);
      --line: rgba(255, 255, 255, 0.09);
      --text: #f5f8ff;
      --muted: #a9b7d1;
      --cyan: #7df9ff;
      --mint: #8ff1c7;
      --shadow: 0 30px 90px rgba(0, 0, 0, 0.45);
      --radius-xl: 32px;
      --radius-lg: 24px;
      --radius-md: 18px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: "Bahnschrift", "Trebuchet MS", sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at 15% 15%, rgba(125, 249, 255, 0.18), transparent 22%),
        radial-gradient(circle at 85% 10%, rgba(143, 241, 199, 0.12), transparent 24%),
        radial-gradient(circle at 85% 85%, rgba(141, 184, 255, 0.14), transparent 25%),
        linear-gradient(145deg, #03050d 0%, #07102a 48%, #090f1f 100%);
      overflow-x: hidden;
      perspective: 1400px;
    }

    body::before,
    body::after {
      content: "";
      position: fixed;
      width: 28rem;
      height: 28rem;
      border-radius: 50%;
      filter: blur(90px);
      opacity: 0.22;
      pointer-events: none;
      z-index: 0;
    }

    body::before {
      top: -8rem;
      left: -8rem;
      background: #67f0e7;
    }

    body::after {
      right: -8rem;
      bottom: -8rem;
      background: #8db8ff;
    }

    .page {
      position: relative;
      z-index: 1;
      width: min(1220px, calc(100% - 1.5rem));
      margin: 0 auto;
      padding: 2rem 0 3rem;
      transform-style: preserve-3d;
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.15fr) minmax(330px, 0.85fr);
      gap: 1.25rem;
      align-items: stretch;
    }

    .panel {
      position: relative;
      background: linear-gradient(180deg, rgba(17, 29, 56, 0.9), rgba(8, 14, 29, 0.82));
      border: 1px solid var(--line);
      border-radius: var(--radius-xl);
      box-shadow: var(--shadow);
      backdrop-filter: blur(18px);
      transform-style: preserve-3d;
      overflow: hidden;
    }

    .panel::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, rgba(255,255,255,0.14), transparent 25%, transparent 70%, rgba(255,255,255,0.05));
      pointer-events: none;
    }

    .panel::after {
      content: "";
      position: absolute;
      inset: auto 0 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(125, 249, 255, 0.4), transparent);
      pointer-events: none;
    }

    .hero-card {
      padding: 1.6rem;
      min-height: 100%;
      transform: translateZ(30px);
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 0.55rem;
      padding: 0.55rem 0.9rem;
      border-radius: 999px;
      color: var(--muted);
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.08);
      margin-bottom: 1rem;
      font-size: 0.95rem;
      letter-spacing: 0.02em;
    }

    .badge-dot {
      width: 0.52rem;
      height: 0.52rem;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--cyan), var(--mint));
      box-shadow: 0 0 0 5px rgba(125, 249, 255, 0.14);
    }

    .profile-top {
      display: flex;
      gap: 1rem;
      align-items: center;
      margin-bottom: 1.2rem;
    }

    .avatar-wrap {
      position: relative;
      width: 5.8rem;
      height: 5.8rem;
      flex: 0 0 auto;
      transform-style: preserve-3d;
    }

    .avatar-glow {
      position: absolute;
      inset: -0.45rem;
      border-radius: 28px;
      background: radial-gradient(circle, rgba(125, 249, 255, 0.35), transparent 68%);
      filter: blur(10px);
      transform: translateZ(-10px);
    }

    .avatar {
      position: relative;
      width: 100%;
      height: 100%;
      border-radius: 24px;
      display: grid;
      place-items: center;
      font-size: 1.7rem;
      font-weight: 800;
      letter-spacing: 0.09em;
      color: #04121f;
      background: linear-gradient(145deg, #bffdf6 0%, #79b7ff 48%, #ffd88a 100%);
      box-shadow:
        0 12px 30px rgba(0, 0, 0, 0.32),
        inset 0 1px 0 rgba(255, 255, 255, 0.55);
      transform: translateZ(30px) rotateY(-6deg);
    }

    h1,
    h2,
    h3 {
      margin: 0;
      line-height: 1.08;
      letter-spacing: -0.04em;
    }

    h1 {
      font-size: clamp(2.35rem, 4.2vw, 4.6rem);
      text-wrap: balance;
    }

    .lead {
      margin: 0.75rem 0 0;
      color: var(--muted);
      font-size: 1.05rem;
      line-height: 1.8;
      max-width: 54rem;
    }

    .glass-row {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 0.85rem;
      margin: 1.4rem 0 1.2rem;
    }

    .glass-stat {
      padding: 1rem 1rem 0.95rem;
      border-radius: 18px;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.08);
      box-shadow: inset 0 1px 0 rgba(255,255,255,0.04);
      transform: translateZ(18px);
    }

    .glass-stat span {
      display: block;
    }

    .glass-stat .label {
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: 0.12em;
      font-size: 0.78rem;
      margin-bottom: 0.45rem;
    }

    .glass-stat .value {
      font-size: 1rem;
      font-weight: 700;
    }

    .cta-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem;
      margin-top: 0.4rem;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 3.05rem;
      padding: 0.8rem 1.2rem;
      border-radius: 999px;
      text-decoration: none;
      font-weight: 700;
      color: #03111d;
      background: linear-gradient(135deg, var(--mint) 0%, #d3ffef 100%);
      box-shadow: 0 16px 34px rgba(143, 241, 199, 0.2);
      transition: transform 160ms ease, box-shadow 160ms ease, opacity 160ms ease;
    }

    .button:hover {
      transform: translateY(-3px) scale(1.01);
    }

    .button.secondary {
      color: var(--text);
      background: rgba(255,255,255,0.06);
      border: 1px solid rgba(255,255,255,0.1);
      box-shadow: none;
    }

    .sidebar {
      padding: 1.3rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      transform: rotateY(-6deg) translateZ(28px);
      transform-origin: center;
    }

    .card-title {
      font-size: 1.2rem;
      margin-bottom: 0.2rem;
    }

    .card-subtitle {
      margin: 0;
      color: var(--muted);
      line-height: 1.7;
      font-size: 0.98rem;
    }

    .orb-panel {
      position: relative;
      min-height: 14rem;
      border-radius: 26px;
      background:
        radial-gradient(circle at 30% 30%, rgba(125, 249, 255, 0.28), transparent 25%),
        radial-gradient(circle at 70% 25%, rgba(143, 241, 199, 0.22), transparent 24%),
        linear-gradient(145deg, rgba(14, 24, 47, 0.95), rgba(6, 11, 24, 0.9));
      border: 1px solid rgba(255,255,255,0.08);
      box-shadow: inset 0 1px 0 rgba(255,255,255,0.05);
      overflow: hidden;
      transform-style: preserve-3d;
    }

    .orb {
      position: absolute;
      border-radius: 50%;
      filter: blur(0px);
      transform-style: preserve-3d;
    }

    .orb.one {
      width: 7rem;
      height: 7rem;
      top: 1rem;
      left: 1.2rem;
      background: radial-gradient(circle at 35% 35%, #dffdf9 0%, #87f8ff 32%, #357aff 78%, #0d1630 100%);
      box-shadow: 0 0 0 1px rgba(255,255,255,0.08), 0 18px 42px rgba(53, 122, 255, 0.35);
      transform: translateZ(28px) rotateX(18deg) rotateY(-18deg);
    }

    .orb.two {
      width: 4.2rem;
      height: 4.2rem;
      right: 1.3rem;
      top: 2.3rem;
      background: radial-gradient(circle at 35% 35%, #fff1b8 0%, #ffd88a 38%, #ff936d 76%, #3a1d16 100%);
      box-shadow: 0 14px 28px rgba(255, 147, 109, 0.22);
      transform: translateZ(20px) rotateZ(12deg);
    }

    .orb.three {
      width: 5.3rem;
      height: 5.3rem;
      right: 4.5rem;
      bottom: 1.2rem;
      background: linear-gradient(145deg, rgba(125,249,255,0.9), rgba(143,241,199,0.55));
      box-shadow: 0 0 0 1px rgba(255,255,255,0.08), 0 14px 30px rgba(125,249,255,0.18);
      opacity: 0.9;
      transform: translateZ(24px) rotateX(12deg);
    }

    .orb-line {
      position: absolute;
      inset: 0;
      background:
        linear-gradient(120deg, transparent 18%, rgba(255,255,255,0.07) 19%, transparent 20%),
        linear-gradient(60deg, transparent 54%, rgba(255,255,255,0.06) 55%, transparent 56%);
      opacity: 0.75;
    }

    .mini-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.8rem;
    }

    .mini {
      padding: 1rem;
      border-radius: var(--radius-md);
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.08);
      transform: translateZ(16px);
    }

    .mini .label {
      display: block;
      color: var(--muted);
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      margin-bottom: 0.45rem;
    }

    .mini .value {
      font-size: 1rem;
      font-weight: 700;
    }

    .section {
      margin-top: 1.25rem;
      padding: 1.4rem;
    }

    .section-head {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 1rem;
      margin-bottom: 1rem;
    }

    .section-head p {
      margin: 0.45rem 0 0;
      color: var(--muted);
      line-height: 1.7;
      max-width: 55rem;
    }

    .chips {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }

    .chip {
      padding: 0.72rem 1rem;
      border-radius: 999px;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.08);
      color: var(--text);
      font-size: 0.95rem;
      font-weight: 600;
    }

    .socials {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 0.85rem;
      margin-top: 1rem;
    }

    .social {
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 3.25rem;
      border-radius: 16px;
      text-decoration: none;
      color: var(--text);
      font-weight: 700;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.08);
      transition: transform 160ms ease, background 160ms ease, border-color 160ms ease;
    }

    .social:hover {
      transform: translateY(-3px);
      background: rgba(255,255,255,0.08);
      border-color: rgba(125, 249, 255, 0.25);
    }

    .footer {
      margin-top: 1.2rem;
      color: var(--muted);
      text-align: center;
      font-size: 0.95rem;
      padding-bottom: 0.5rem;
    }

    @media (max-width: 980px) {
      .hero {
        grid-template-columns: 1fr;
      }

      .sidebar {
        transform: none;
      }

      .socials,
      .glass-row,
      .mini-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 720px) {
      .page {
        width: min(100% - 1rem, 1220px);
        padding: 1rem 0 2rem;
      }

      .hero-card,
      .sidebar,
      .section {
        padding: 1.1rem;
      }

      .profile-top {
        align-items: flex-start;
      }

      .glass-row,
      .socials,
      .mini-grid {
        grid-template-columns: 1fr;
      }

      .section-head {
        flex-direction: column;
        align-items: start;
      }

      h1 {
        font-size: clamp(2.05rem, 10vw, 3rem);
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <section class="hero">
      <article class="panel hero-card">
        <div class="badge"><span class="badge-dot"></span> GitHub profile dashboard</div>

        <div class="profile-top">
          <div class="avatar-wrap">
            <div class="avatar-glow"></div>
            <div class="avatar">SB</div>
          </div>
          <div>
            <h1>Subhadip Bera</h1>
            <p class="lead">Aspiring AI and ML engineer from India. I build with JavaScript, Python, and modern web tools, and I like keeping things clean, practical, and visually strong.</p>
          </div>
        </div>

        <div class="glass-row">
          <div class="glass-stat">
            <span class="label">GitHub</span>
            <span class="value">subh-a-dip</span>
          </div>
          <div class="glass-stat">
            <span class="label">Focus</span>
            <span class="value">AI, ML, and Web</span>
          </div>
          <div class="glass-stat">
            <span class="label">Location</span>
            <span class="value">India</span>
          </div>
        </div>

        <p class="lead" style="margin-top:0; max-width:none;">This version is built to feel like a premium 3D GitHub profile card, with layered depth, glowing highlights, and clearer hierarchy across sections.</p>

        <div class="cta-row">
          <a class="button" href="mailto:subhadipb667@gmail.com">Contact me</a>
          <a class="button secondary" href="#skills">View skills</a>
        </div>
      </article>

      <aside class="panel sidebar">
        <div>
          <h2 class="card-title">3D profile card</h2>
          <p class="card-subtitle">A floating right panel with layered orbs, glass textures, and depth styling for a more premium GitHub look.</p>
        </div>

        <div class="orb-panel" aria-hidden="true">
          <div class="orb-line"></div>
          <div class="orb one"></div>
          <div class="orb two"></div>
          <div class="orb three"></div>
        </div>

        <div class="mini-grid">
          <div class="mini">
            <span class="label">Role</span>
            <span class="value">AI & ML Learner</span>
          </div>
          <div class="mini">
            <span class="label">Goal</span>
            <span class="value">Build useful products</span>
          </div>
          <div class="mini">
            <span class="label">Style</span>
            <span class="value">Modern and bold</span>
          </div>
          <div class="mini">
            <span class="label">Fun fact</span>
            <span class="value">Funny in shorts</span>
          </div>
        </div>
      </aside>
    </section>

    <section class="panel section" id="skills">
      <div class="section-head">
        <div>
          <h2>Languages and tools</h2>
          <p>My working stack across frontend, backend, and problem solving.</p>
        </div>
      </div>
      <div class="chips">
        <span class="chip">JavaScript</span>
        <span class="chip">TypeScript</span>
        <span class="chip">React</span>
        <span class="chip">HTML5</span>
        <span class="chip">CSS3</span>
        <span class="chip">Python</span>
        <span class="chip">C#</span>
        <span class="chip">Node.js</span>
        <span class="chip">Machine Learning</span>
        <span class="chip">Data Structures</span>
      </div>
    </section>

    <section class="panel section">
      <div class="section-head">
        <div>
          <h2>Connect with me</h2>
          <p>Every link below opens the right profile or contact destination directly.</p>
        </div>
      </div>
      <div class="socials">
        <a class="social" href="https://www.youtube.com/@subhadipbera260" target="_blank" rel="noreferrer">YouTube</a>
        <a class="social" href="https://www.instagram.com/im_subha_19?igsh=MW1pbnYyOGdudWE0NQ==" target="_blank" rel="noreferrer">Instagram</a>
        <a class="social" href="https://www.twitch.tv/settings/profile" target="_blank" rel="noreferrer">Twitch</a>
        <a class="social" href="https://discordapp.com/users/1153677407849545881" target="_blank" rel="noreferrer">Discord</a>
        <a class="social" href="mailto:subhadipb667@gmail.com">Gmail</a>
        <a class="social" href="https://www.linkedin.com/in/subhadip-bera-178395318?utm_source=share_via&utm_content=profile&utm_medium=member_android" target="_blank" rel="noreferrer">LinkedIn</a>
      </div>
    </section>

    <p class="footer">Built for Subhadip Bera. Clickable profile links open in a new tab and email opens a draft directly.</p>
  </main>
</body>
</html>
