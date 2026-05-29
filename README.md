
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Consolas',monospace;background:#080818}
.root{background:#080818;padding:1.5rem;display:flex;flex-direction:column;gap:1.25rem;min-height:100vh}

.panel{background:#0b0b1e;border:2px solid #ff6a00;border-radius:10px;padding:1.25rem 1.5rem;position:relative}
.panel::before,.panel::after{content:'';position:absolute;background:#ff6a00}
.panel::before{top:-2px;left:10px;width:30px;height:4px}
.panel::after{bottom:-2px;right:10px;width:30px;height:4px}
.panel-tl,.panel-tr,.panel-bl,.panel-br{position:absolute;width:14px;height:14px;border-color:#ff6a00}
.panel-tl{top:-2px;left:-2px;border-top:3px solid;border-left:3px solid;border-radius:4px 0 0 0}
.panel-tr{top:-2px;right:-2px;border-top:3px solid;border-right:3px solid;border-radius:0 4px 0 0}
.panel-bl{bottom:-2px;left:-2px;border-bottom:3px solid;border-left:3px solid;border-radius:0 0 0 4px}
.panel-br{bottom:-2px;right:-2px;border-bottom:3px solid;border-right:3px solid;border-radius:0 0 4px 0}

.panel-blue{border-color:#00b4ff}
.panel-blue::before,.panel-blue::after{background:#00b4ff}
.panel-blue .panel-tl,.panel-blue .panel-tr,.panel-blue .panel-bl,.panel-blue .panel-br{border-color:#00b4ff}

.hero-panel{background:#0b0b1e;border:2px solid #ff6a00;border-radius:10px;padding:1.5rem;position:relative;text-align:center}
.hero-panel::before{content:'';position:absolute;top:-2px;left:10px;width:30px;height:4px;background:#ff6a00}
.hero-panel::after{content:'';position:absolute;bottom:-2px;right:10px;width:30px;height:4px;background:#ff6a00}
.htl,.htr,.hbl,.hbr{position:absolute;width:14px;height:14px;border-color:#ff6a00}
.htl{top:-2px;left:-2px;border-top:3px solid;border-left:3px solid;border-radius:4px 0 0 0}
.htr{top:-2px;right:-2px;border-top:3px solid;border-right:3px solid;border-radius:0 4px 0 0}
.hbl{bottom:-2px;left:-2px;border-bottom:3px solid;border-left:3px solid;border-radius:0 0 0 4px}
.hbr{bottom:-2px;right:-2px;border-bottom:3px solid;border-right:3px solid;border-radius:0 0 4px 0}

.title-bar{background:#0f0f28;border:2px solid #ff6a00;border-radius:8px;padding:0.6rem 1.25rem;text-align:center;font-family:'Arial Black',sans-serif;font-size:22px;font-weight:900;color:#ffffff;letter-spacing:2px;margin-bottom:0.25rem}

.section-tag{font-size:11px;color:#ff6a00;letter-spacing:0.12em;text-transform:uppercase;margin-bottom:0.5rem;font-family:'Consolas',monospace}
.section-tag-blue{color:#00b4ff}

.avatar-row{display:flex;align-items:center;justify-content:center;gap:1rem;margin-bottom:0.75rem}
.avatar{width:60px;height:60px;border-radius:50%;background:#1a1a3e;border:2px solid #ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;font-weight:900;color:#ff6a00;font-family:'Arial Black',sans-serif}
.hero-name{font-size:20px;font-weight:900;color:#ffffff;font-family:'Arial Black',sans-serif}
.hero-sub{font-size:12px;color:#00b4ff;margin-top:2px}
.hero-loc{font-size:12px;color:#888;margin-top:4px}
.hero-bio{font-size:12px;color:#aaa;margin-top:0.75rem;line-height:1.7;font-family:sans-serif}

.pill-row{display:flex;flex-wrap:wrap;gap:6px;justify-content:center;margin-top:0.75rem}
.pill{font-size:11px;padding:3px 10px;border-radius:4px;border:1px solid #ff6a00;color:#ff6a00;background:#1a0a00}
.pill-b{border-color:#00b4ff;color:#00b4ff;background:#001a2e}

.code-block{font-family:'Consolas',monospace;font-size:12.5px;line-height:1.75;margin-top:0.25rem}
.kw{color:#569cd6}
.fn{color:#dcdcaa}
.str{color:#ce9178}
.cmt{color:#6a9955}
.cls{color:#4ec9b0}
.var{color:#9cdcfe}
.num{color:#b5cea8}
.pun{color:#d4d4d4}
.wh{color:#d4d4d4}
.inc{color:#4ec9b0}

.lang-badge{display:inline-block;padding:4px 14px;border-radius:5px;font-family:'Arial Black',sans-serif;font-size:16px;font-weight:900;font-style:italic;color:#fff;margin-bottom:0.75rem}
.badge-py{background:#c82000}
.badge-js{background:#c8a000}
.badge-ts{background:#006aad}
.badge-node{background:#2a7a00}
.badge-mongo{background:#00683a}
.badge-react{background:#0077a8}

.grid2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.grid3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:10px}
.mini-card{background:#0f0f28;border:1px solid #ff6a0066;border-radius:6px;padding:0.75rem;font-size:12px}
.mini-title{color:#ff6a00;font-weight:700;margin-bottom:2px;font-size:13px}
.mini-sub{color:#888;font-family:sans-serif;font-size:11.5px}
.active-dot{display:inline-block;width:7px;height:7px;border-radius:50%;background:#39d353;margin-right:5px;vertical-align:middle}

.repo-row{display:flex;align-items:flex-start;gap:10px;padding:0.6rem 0;border-bottom:1px solid #1e1e3a}
.repo-row:last-child{border-bottom:none}
.repo-icon-box{width:30px;height:30px;border-radius:5px;display:flex;align-items:center;justify-content:center;font-size:14px;flex-shrink:0}
.repo-name{color:#00b4ff;font-size:13px;font-weight:700}
.repo-desc{color:#888;font-size:11px;margin-top:1px;font-family:sans-serif}

.interest-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:8px}
.int-card{background:#0f0f28;border:1px solid #00b4ff44;border-radius:6px;padding:0.6rem;text-align:center}
.int-icon{font-size:18px;color:#00b4ff;display:block;margin-bottom:3px}
.int-label{font-size:10.5px;color:#aaa;font-family:sans-serif;line-height:1.4}

.quote-panel{background:#060616;border-left:3px solid #00b4ff;border-radius:0 6px 6px 0;padding:0.875rem 1.125rem}
.quote-text{font-size:13px;color:#aaa;font-style:italic;line-height:1.7;font-family:serif}

.mindset-bar{background:#060616;border:1px solid #ff6a0055;border-radius:6px;padding:0.75rem 1rem;font-size:13px;color:#ff6a00;text-align:center;letter-spacing:0.05em}

.connect-row{display:flex;gap:10px;flex-wrap:wrap}
.connect-btn{display:flex;align-items:center;gap:6px;padding:7px 16px;border-radius:6px;border:1px solid #ff6a00;font-size:12px;color:#ff6a00;background:#1a0a00;cursor:pointer;text-decoration:none;font-family:'Consolas',monospace}
.connect-btn-b{border-color:#00b4ff;color:#00b4ff;background:#001a2e}

.footer{text-align:center;font-size:11px;color:#555;margin-top:0.5rem;font-family:sans-serif;letter-spacing:0.05em}

.dot-grid{position:absolute;inset:0;border-radius:10px;overflow:hidden;pointer-events:none;opacity:0.07}
</style>

<h2 style="position:absolute;left:-9999px">Martin Code — Full-stack MERN developer profile</h2>

<div class="root">

  <div class="title-bar">⚡ MARTIN CODE ⚡</div>

  <div class="hero-panel">
    <div class="htl"></div><div class="htr"></div><div class="hbl"></div><div class="hbr"></div>
    <div class="section-tag">// profile.md</div>
    <div class="avatar-row">
      <div class="avatar">MC</div>
      <div style="text-align:left">
        <div class="hero-name">Martin</div>
        <div class="hero-sub">Full-Stack MERN Developer</div>
        <div class="hero-loc">&#x1F30D; Kigali, Rwanda</div>
      </div>
    </div>
    <div class="hero-bio">
      Building scalable web applications, intelligent systems &amp; modern software architectures.<br/>
      Long-term: Bridging <span style="color:#ff6a00;font-weight:700">AI + Software + Embedded Systems</span> to solve real-world problems.
    </div>
    <div class="pill-row">
      <span class="pill">React</span>
      <span class="pill">Node.js</span>
      <span class="pill-b pill">MongoDB</span>
      <span class="pill-b pill">Python</span>
      <span class="pill-b pill">AI &amp; Embedded</span>
    </div>
  </div>

  <div class="panel">
    <div class="panel-tl"></div><div class="panel-tr"></div><div class="panel-bl"></div><div class="panel-br"></div>
    <div class="section-tag">// currently_building.js</div>
    <div class="grid2">
      <div class="mini-card">
        <div class="mini-title"><span class="active-dot"></span>Rent Car Platform</div>
        <div class="mini-sub">Full MERN stack car rental app</div>
      </div>
      <div class="mini-card">
        <div class="mini-title"><span class="active-dot"></span>Validation Systems</div>
        <div class="mini-sub">Auth &amp; data validation platform</div>
      </div>
      <div class="mini-card">
        <div class="mini-title"><span class="active-dot"></span>Portfolio Website</div>
        <div class="mini-sub">Professional developer showcase</div>
      </div>
      <div class="mini-card">
        <div class="mini-title"><span class="active-dot"></span>AI &amp; Embedded</div>
        <div class="mini-sub">Smart systems &amp; automation</div>
      </div>
    </div>
  </div>

  <div class="panel panel-blue">
    <div class="panel-tl"></div><div class="panel-tr"></div><div class="panel-bl"></div><div class="panel-br"></div>
    <div class="section-tag section-tag-blue">// tech_stack.py</div>

    <div class="lang-badge badge-react" style="margin-right:6px">Frontend</div>
    <div class="code-block">
      <span class="kw">import</span> <span class="cls">{ React, JavaScript, TypeScript }</span> <span class="kw">from</span> <span class="str">'frontend'</span><br/>
      <span class="kw">import</span> <span class="cls">{ HTML, CSS, TailwindCSS }</span> <span class="kw">from</span> <span class="str">'styling'</span>
    </div>

    <div style="margin-top:1rem"><div class="lang-badge badge-node" style="margin-right:6px">Backend</div></div>
    <div class="code-block">
      <span class="kw">const</span> <span class="var">server</span> <span class="pun">=</span> <span class="fn">require</span><span class="pun">(</span><span class="str">'Node.js + Express'</span><span class="pun">)</span><br/>
      <span class="kw">import</span> <span class="cls">{ Django }</span> <span class="kw">from</span> <span class="str">'python'</span>
    </div>

    <div style="margin-top:1rem"><div class="lang-badge badge-mongo" style="margin-right:6px">Database</div></div>
    <div class="code-block">
      <span class="var">db</span><span class="pun">.</span><span class="fn">connect</span><span class="pun">(</span><span class="str">'MongoDB'</span><span class="pun">,</span> <span class="str">'MySQL'</span><span class="pun">,</span> <span class="str">'PostgreSQL'</span><span class="pun">)</span>
    </div>

    <div style="margin-top:1rem"><div class="lang-badge" style="background:#444;margin-right:6px">Tools</div></div>
    <div class="code-block">
      <span class="cmt">// Git, GitHub, VS Code, Linux, Figma</span>
    </div>
  </div>

  <div class="panel">
    <div class="panel-tl"></div><div class="panel-tr"></div><div class="panel-bl"></div><div class="panel-br"></div>
    <div class="section-tag">// engineering_interests[]</div>
    <div class="interest-grid">
      <div class="int-card"><i class="ti ti-stack-2 int-icon" aria-hidden="true"></i><div class="int-label">Full-stack dev</div></div>
      <div class="int-card"><i class="ti ti-cpu int-icon" aria-hidden="true"></i><div class="int-label">Embedded systems</div></div>
      <div class="int-card"><i class="ti ti-robot int-icon" aria-hidden="true"></i><div class="int-label">Artificial intelligence</div></div>
      <div class="int-card"><i class="ti ti-api int-icon" aria-hidden="true"></i><div class="int-label">API development</div></div>
      <div class="int-card"><i class="ti ti-topology-star int-icon" aria-hidden="true"></i><div class="int-label">System architecture</div></div>
      <div class="int-card"><i class="ti ti-device-desktop-analytics int-icon" aria-hidden="true"></i><div class="int-label">Modern UI/UX</div></div>
      <div class="int-card"><i class="ti ti-circuit-ground int-icon" aria-hidden="true"></i><div class="int-label">IoT &amp; automation</div></div>
      <div class="int-card"><i class="ti ti-tool int-icon" aria-hidden="true"></i><div class="int-label">MERN stack</div></div>
    </div>
  </div>

  <div class="panel panel-blue">
    <div class="panel-tl"></div><div class="panel-tr"></div><div class="panel-bl"></div><div class="panel-br"></div>
    <div class="section-tag section-tag-blue">// featured_repos.json</div>
    <div class="repo-row">
      <div class="repo-icon-box" style="background:#1a0a00;border:1px solid #ff6a00"><i class="ti ti-car" style="color:#ff6a00" aria-hidden="true"></i></div>
      <div>
        <div class="repo-name">Rent-Car-React-Nodejs</div>
        <div class="repo-desc">Modern MERN car rental platform</div>
      </div>
    </div>
    <div class="repo-row">
      <div class="repo-icon-box" style="background:#001a10;border:1px solid #00c97a"><i class="ti ti-shield-check" style="color:#00c97a" aria-hidden="true"></i></div>
      <div>
        <div class="repo-name">validationcheck</div>
        <div class="repo-desc">Advanced validation logic system</div>
      </div>
    </div>
    <div class="repo-row">
      <div class="repo-icon-box" style="background:#1a001a;border:1px solid #b060ff"><i class="ti ti-lock" style="color:#b060ff" aria-hidden="true"></i></div>
      <div>
        <div class="repo-name">Login-validation-in-JavaScript</div>
        <div class="repo-desc">Authentication &amp; form validation</div>
      </div>
    </div>
    <div class="repo-row">
      <div class="repo-icon-box" style="background:#001020;border:1px solid #00b4ff"><i class="ti ti-world" style="color:#00b4ff" aria-hidden="true"></i></div>
      <div>
        <div class="repo-name">Website</div>
        <div class="repo-desc">Personal website &amp; portfolio</div>
      </div>
    </div>
  </div>

  <div class="panel">
    <div class="panel-tl"></div><div class="panel-tr"></div><div class="panel-bl"></div><div class="panel-br"></div>
    <div class="section-tag">// philosophy.md</div>
    <div class="quote-panel">
      <div class="quote-text">"Speed is not created by flying first. It is created by removing delays."</div>
    </div>
  </div>

  <div class="panel panel-blue">
    <div class="panel-tl"></div><div class="panel-tr"></div><div class="panel-bl"></div><div class="panel-br"></div>
    <div class="section-tag section-tag-blue">// mindset.js</div>
    <div class="mindset-bar">learn() → build() → improve() → innovate() → repeat()</div>
  </div>

  <div class="panel">
    <div class="panel-tl"></div><div class="panel-tr"></div><div class="panel-bl"></div><div class="panel-br"></div>
    <div class="section-tag">// connect.sh</div>
    <div class="connect-row">
      <a class="connect-btn" href="https://github.com/martincode2"><i class="ti ti-brand-github" aria-hidden="true"></i>github/martincode2</a>
      <a class="connect-btn connect-btn-b" href="https://martincode2.com"><i class="ti ti-world" aria-hidden="true"></i>martincode2.com</a>
    </div>
  </div>

  <div class="footer">⚡ Building the future with software &amp; intelligence ⚡</div>

</div>
