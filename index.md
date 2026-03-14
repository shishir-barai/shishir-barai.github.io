---
layout: default
---

<style>
/* ── Google Fonts ── */
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=DM+Sans:wght@300;400;500;600&family=JetBrains+Mono:wght@400;600&display=swap');

/* ── CSS Variables ── */
:root {
  --navy:    #0d1f3c;
  --blue:    #1a4480;
  --accent:  #c8651b;
  --light:   #f4f7fb;
  --border:  #d0dae8;
  --text:    #1e2a3a;
  --muted:   #5a6a7e;
  --white:   #ffffff;
  --tag-bg:  #e8eef7;
}

/* ── Reset & Base ── */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--light);
  color: var(--text);
  line-height: 1.7;
  font-size: 15.5px;
}

/* ── Page wrapper ── */
.page-header { display: none !important; }

.main-content {
  max-width: 900px;
  margin: 0 auto;
  padding: 0 1.5rem 4rem;
}

/* ── HERO ── */
.hero {
  display: flex;
  align-items: center;
  gap: 2.5rem;
  padding: 3.5rem 0 2.5rem;
  border-bottom: 2px solid var(--border);
}

.hero-text { flex: 1; }

.hero-text h1 {
  font-family: 'DM Serif Display', serif;
  font-size: 2.6rem;
  color: var(--navy);
  line-height: 1.15;
  margin-bottom: 0.4rem;
}

.hero-text .tagline {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--accent);
  letter-spacing: 0.12em;
  text-transform: uppercase;
  margin-bottom: 1.1rem;
}

.hero-text p {
  color: var(--muted);
  font-weight: 300;
  font-size: 0.97rem;
  max-width: 520px;
  margin-bottom: 1.4rem;
  line-height: 1.75;
}

.hero-links {
  display: flex;
  gap: 0.75rem;
  flex-wrap: wrap;
}

.hero-links a {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.45rem 1rem;
  border-radius: 4px;
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 0.03em;
  text-decoration: none;
  transition: all 0.18s ease;
}

.btn-primary {
  background: var(--navy);
  color: var(--white) !important;
  border: 2px solid var(--navy);
}
.btn-primary:hover { background: var(--blue); border-color: var(--blue); }

.btn-outline {
  background: transparent;
  color: var(--navy) !important;
  border: 2px solid var(--navy);
}
.btn-outline:hover { background: var(--navy); color: var(--white) !important; }

.hero-photo {
  flex-shrink: 0;
  width: 175px;
  height: 175px;
  border-radius: 50%;
  overflow: hidden;
  border: 4px solid var(--white);
  box-shadow: 0 8px 30px rgba(13,31,60,0.18);
}

.hero-photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

/* ── SECTION TITLES ── */
.section {
  margin-top: 3rem;
}

.section-title {
  font-family: 'DM Serif Display', serif;
  font-size: 1.45rem;
  color: var(--navy);
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 1.4rem;
}

.section-title::after {
  content: '';
  flex: 1;
  height: 1px;
  background: var(--border);
}

/* ── SKILLS GRID ── */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 1rem;
}

.skill-card {
  background: var(--white);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1rem 1.2rem;
  border-top: 3px solid var(--accent);
}

.skill-card h4 {
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--accent);
  margin-bottom: 0.5rem;
}

.skill-card p {
  font-size: 0.84rem;
  color: var(--muted);
  line-height: 1.6;
}

/* ── EDUCATION ── */
.edu-item {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  gap: 1rem;
  padding: 0.9rem 0;
  border-bottom: 1px solid var(--border);
}

.edu-item:last-child { border-bottom: none; }

.edu-degree {
  font-weight: 600;
  color: var(--navy);
  font-size: 0.96rem;
}

.edu-school {
  font-size: 0.88rem;
  color: var(--muted);
}

.edu-year {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.8rem;
  color: var(--accent);
  white-space: nowrap;
  font-weight: 600;
}

/* ── EXPERIENCE ── */
.exp-item {
  background: var(--white);
  border: 1px solid var(--border);
  border-left: 4px solid var(--accent);
  border-radius: 6px;
  padding: 1.3rem 1.5rem;
  margin-bottom: 1.2rem;
}

.exp-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
  gap: 0.4rem;
  margin-bottom: 0.7rem;
}

.exp-role {
  font-weight: 700;
  font-size: 1.01rem;
  color: var(--navy);
}

.exp-company {
  font-size: 0.9rem;
  color: var(--blue);
  font-weight: 600;
}

.exp-meta {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.76rem;
  color: var(--muted);
  text-align: right;
  line-height: 1.6;
}

.exp-item ul {
  padding-left: 1.2rem;
  margin-top: 0.5rem;
}

.exp-item li {
  font-size: 0.9rem;
  color: var(--text);
  margin-bottom: 0.35rem;
  line-height: 1.6;
}

/* ── PROJECTS ── */
.project-card {
  background: var(--white);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 1.4rem 1.6rem;
  margin-bottom: 1.2rem;
  transition: box-shadow 0.18s;
}

.project-card:hover {
  box-shadow: 0 4px 20px rgba(13,31,60,0.09);
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 0.75rem;
}

.project-title {
  font-family: 'DM Serif Display', serif;
  font-size: 1.08rem;
  color: var(--navy);
}

.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
}

.tag {
  background: var(--tag-bg);
  color: var(--blue);
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.71rem;
  font-weight: 600;
  padding: 0.2rem 0.55rem;
  border-radius: 3px;
  letter-spacing: 0.04em;
}

.project-card ul {
  padding-left: 1.2rem;
}

.project-card li {
  font-size: 0.9rem;
  color: var(--text);
  margin-bottom: 0.35rem;
  line-height: 1.6;
}

/* ── PUBLICATIONS ── */
.pub-item {
  padding: 0.9rem 0 0.9rem 1rem;
  border-left: 3px solid var(--border);
  margin-bottom: 1rem;
  font-size: 0.9rem;
  line-height: 1.65;
  color: var(--text);
}

.pub-item:hover { border-left-color: var(--accent); }

.pub-item .pub-journal {
  font-style: italic;
  color: var(--muted);
  font-size: 0.85rem;
}

.pub-item a {
  color: var(--blue);
  text-decoration: none;
  font-weight: 600;
  font-size: 0.82rem;
}

.pub-item a:hover { text-decoration: underline; }

/* ── COLLABORATE ── */
.collab-box {
  background: var(--navy);
  color: var(--white);
  border-radius: 10px;
  padding: 2rem 2.2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
  flex-wrap: wrap;
}

.collab-box h3 {
  font-family: 'DM Serif Display', serif;
  font-size: 1.35rem;
  margin-bottom: 0.5rem;
}

.collab-box p {
  font-size: 0.9rem;
  color: #b0c0d8;
  max-width: 480px;
  line-height: 1.65;
}

.collab-box a.btn-collab {
  display: inline-block;
  padding: 0.65rem 1.5rem;
  background: var(--accent);
  color: var(--white) !important;
  border-radius: 5px;
  text-decoration: none;
  font-weight: 700;
  font-size: 0.88rem;
  white-space: nowrap;
  transition: background 0.18s;
}

.collab-box a.btn-collab:hover { background: #a8531a; }

/* ── FOOTER ── */
.site-footer {
  text-align: center;
  padding: 2rem 0 1rem;
  margin-top: 3rem;
  border-top: 1px solid var(--border);
  font-size: 0.82rem;
  color: var(--muted);
}

/* ── RESPONSIVE ── */
@media (max-width: 640px) {
  .hero {
    flex-direction: column-reverse;
    align-items: center;
    text-align: center;
    padding-top: 2rem;
  }
  .hero-text p { max-width: 100%; }
  .hero-links { justify-content: center; }
  .edu-item { flex-direction: column; gap: 0.2rem; }
  .edu-year { text-align: left; }
  .exp-meta { text-align: left; }
  .collab-box { flex-direction: column; text-align: center; }
}
</style>

<!-- ════════════════════════════════
     HERO
════════════════════════════════ -->
<div class="hero">
  <div class="hero-text">
    <div class="tagline">Structural Analysis Engineer &nbsp;|&nbsp; FEA &nbsp;|&nbsp; Scripting &amp; Optimization &nbsp;|&nbsp; Multiphysics Simulation</div>
    <h1>Shishir Barai</h1>
    <p>
      Ph.D. in Engineering Science & Mechanics (Penn State). Specialized in finite element analysis, automated simulation workflows, and Python-based scripting for multiphysics modeling. Currently at X-energy; previously interned at ASML and Ansys.
    </p>
    <div class="hero-links">
      <a href="Resume_Barai_Shishir.pdf" class="btn-primary">⬇ Resume</a>
      <a href="https://www.linkedin.com/in/shishir-barai/" class="btn-outline" target="_blank">LinkedIn</a>
      <a href="https://scholar.google.com/citations?user=L8pNussAAAAJ" class="btn-outline" target="_blank">Scholar</a>
    </div>
  </div>
  <div class="hero-photo">
    <img src="MyPhoto2.JPG" alt="Shishir Barai" />
  </div>
</div>

<!-- ════════════════════════════════
     CORE SKILLS
════════════════════════════════ -->
<div class="section">
  <div class="section-title">Core Expertise</div>
  <div class="skills-grid">
    <div class="skill-card">
      <h4>FEA & Simulation</h4>
      <p>Abaqus CAE, ANSYS, COMSOL, LS-DYNA</p>
    </div>
    <div class="skill-card">
      <h4>Scripting & Automation</h4>
      <p>Python, PyAnsys, MAPDL, Matlab, C++</p>
    </div>
    <div class="skill-card">
      <h4>Optimization & DOE</h4>
      <p>Ansys optiSLang, Parametric Modeling, Design of Experiments (DOE)</p>
    </div>
    <div class="skill-card">
      <h4>ML for Simulation</h4>
      <p>CNNs, Autoencoders, TensorFlow, PyTorch, Scikit-learn, Numpy, Pandas</p>
    </div>
    <div class="skill-card">
      <h4>CAD & Modeling</h4>
      <p>SolidWorks, AutoCAD</p>
    </div>
    <div class="skill-card">
      <h4>Materials Modeling</h4>
      <p>Hyperelastic (Mooney-Rivlin, Ogden), RVE Analysis</p>
    </div>
  </div>
</div>

<!-- ════════════════════════════════
     EDUCATION
════════════════════════════════ -->
<div class="section">
  <div class="section-title">Education</div>

  <div class="edu-item">
    <div>
      <div class="edu-degree">Ph.D. — Engineering Science &amp; Mechanics</div>
      <div class="edu-school">Pennsylvania State University, PA</div>
    </div>
    <div class="edu-year">2026</div>
  </div>

  <div class="edu-item">
    <div>
      <div class="edu-degree">M.S. — Mechanical Engineering</div>
      <div class="edu-school">University of Texas Rio Grande Valley, TX</div>
    </div>
    <div class="edu-year">2021</div>
  </div>

  <div class="edu-item">
    <div>
      <div class="edu-degree">B.S. — Mechanical Engineering</div>
      <div class="edu-school">Bangladesh University of Engineering &amp; Technology (BUET)</div>
    </div>
    <div class="edu-year">2018</div>
  </div>
</div>

<!-- ════════════════════════════════
     INDUSTRY EXPERIENCE
════════════════════════════════ -->
<div class="section">
  <div class="section-title">Industry Experience</div>

  <div class="exp-item">
    <div class="exp-header">
      <div>
        <div class="exp-role">Structural Analysis Engineer</div>
        <div class="exp-company">X-energy LLC</div>
      </div>
      <div class="exp-meta">Mar 2026 – Present<br>Rockville, MD</div>
    </div>
    <ul>
      <li>Structural and thermal analysis of advanced nuclear reactor components using FEA in Ansys.</li>
      <li>Python scripting for simulation automation and post-processing workflows.</li>
    </ul>
  </div>

  <div class="exp-item">
    <div class="exp-header">
      <div>
        <div class="exp-role">Finite Element Analysis Intern</div>
        <div class="exp-company">ASML US, Inc.</div>
      </div>
      <div class="exp-meta">May 2025 – Aug 2025<br>San Diego, CA</div>
    </div>
    <ul>
      <li>Built a fully automated parametric CAD-to-simulation pipeline in Abaqus with 40 geometric design variables for EUV nozzle design.</li>
      <li>Scripted meshing, boundary conditions, solver settings, and post-processing using Abaqus Python API.</li>
      <li>Integrated Ansys optiSLang for DOE sampling, parameter sweeps, and performance-driven optimization.</li>
      <li>Conducted steady-state dynamic simulations to evaluate pressure response and maximize droplet formation.</li>
      <li>Delivered a modular, reusable automation framework; significantly reducing manual CAD-simulation iteration time.</li>
    </ul>
  </div>

  <div class="exp-item">
    <div class="exp-header">
      <div>
        <div class="exp-role">Mechanical Engineering Intern — Material Modeling Team</div>
        <div class="exp-company">Ansys Inc.</div>
      </div>
      <div class="exp-meta">Jun 2024 – Aug 2024<br>Canonsburg, PA</div>
    </div>
    <ul>
      <li>Developed a modular Python class to automate nonlinear FEA simulations and material calibration workflows using PyAnsys MAPDL.</li>
      <li>Applied Periodic Boundary Conditions on RVEs to extract homogenized hyperelastic material properties (Mooney-Rivlin, Ogden).</li>
      <li>Integrated Ansys Material Library (AML) for stress-strain data calibration and parameter verification.</li>
      <li>Built a flexible configuration system for load types, solver settings, and material definitions.</li>
    </ul>
  </div>
</div>

<!-- ════════════════════════════════
     RESEARCH & PROJECTS
════════════════════════════════ -->
<div class="section">
  <div class="section-title">Research &amp; Projects</div>

  <div class="project-card">
    <div class="project-header">
      <div class="project-title">FEA Framework for Composite Microstructure Modeling — Penn State</div>
      <div class="tags">
        <span class="tag">Python</span>
		<span class="tag">Object-Oriented Programming (OOP) </span>
		<span class="tag">MOOSE</span>
        <span class="tag">Gmsh</span>
        
      </div>
    </div>
    <ul>
      <li>Developed a Python class to generate two-phase microstructures with randomized particle distributions.</li>
      <li>Implemented linear elasticity FEA in MOOSE covering uniaxial tension, biaxial tension, and compression.</li>
      <li>Captured full displacement field data as training datasets for reduced order surrogate models.</li>
    </ul>
  </div>

  <div class="project-card">
    <div class="project-header">
      <div class="project-title">ML-Accelerated Microstructure Response Prediction — Penn State</div>
      <div class="tags">
        <span class="tag">TensorFlow</span>
        <span class="tag">CNN</span>
        <span class="tag">Autoencoder</span>
        <span class="tag">HPC/Slurm</span>
      </div>
    </div>
    <ul>
      <li>Trained CNN-based model to directly map microstructure inputs to FEA displacement fields.</li>
      <li>Built a convolutional autoencoder to compress high-dimensional FEA datasets by <strong>94%</strong>.</li>
      <li>Surrogate model trained on compressed latent space reduced overall training time by <strong>75%</strong>.</li>
      <li>Optimized training pipeline on a Linux-based Slurm HPC cluster.</li>
    </ul>
  </div>

  <div class="project-card">
    <div class="project-header">
      <div class="project-title">Transient FEA of Thin Plates — Penn State</div>
      <div class="tags">
        <span class="tag">COMSOL</span>
        <span class="tag">Weak Form PDE</span>
        <span class="tag">Verification</span>
      </div>
    </div>
    <ul>
      <li>Conducted transient structural analysis of rectangular plates under impulsive loading in COMSOL Multiphysics.</li>
      <li>Implemented weak form PDE formulations; analyzed stress distributions and dynamic response.</li>
      <li>Verified FEM accuracy using Method of Manufactured Solutions against analytical solutions.</li>
    </ul>
  </div>
</div>

<!-- ════════════════════════════════
     PUBLICATIONS
════════════════════════════════ -->
<div class="section">
  <div class="section-title">Selected Publications</div>

  <div class="pub-item">
    <strong>Shishir Barai</strong>, Feihong Liu, Manik Kumar, Christian Peco.
    "Neural network-driven framework for efficient microstructural modeling of particle-enriched composites."
    <span class="pub-journal">Materials Today Communications, 2025.</span>
    <a href="https://www.sciencedirect.com/science/article/abs/pii/S2352492824032604" target="_blank">[Link]</a>
  </div>

  <div class="pub-item">
    M. Kumar, N. Upadhyay, <strong>Shishir Barai</strong>, W.F. Reinhart, C. Peco.
    "A Bio-lattice Deep Learning Framework for Modeling Discrete Biological Materials."
    <span class="pub-journal">Journal of the Mechanical Behavior of Biomedical Materials, 2025.</span>
    <a href="https://www.sciencedirect.com/science/article/abs/pii/S1751616125000165" target="_blank">[Link]</a>
  </div>

  <div class="pub-item">
    Lorestani, Farnaz, et al.
    "A Highly Sensitive and Long-Term Stable Wearable Patch for Continuous Analysis of Biomarkers in Sweat."
    <span class="pub-journal">Advanced Functional Materials, 2023.</span>
    <a href="https://advanced.onlinelibrary.wiley.com/doi/full/10.1002/adfm.202306117" target="_blank">[Link]</a>
  </div>

  <div class="pub-item">
    J. Sgarrella, W. Laplante, <strong>Shishir Barai</strong>, M. Kumar, Christian Peco.
    "Data-driven material-based encoding for swarm decentralized controllers."
    <span class="pub-journal">Submitted — Journal of Swarm and Evolutionary Computation, 2025.</span>
  </div>
</div>

<!-- ════════════════════════════════
     COLLABORATE
════════════════════════════════ -->
<div class="section">
  <div class="collab-box">
    <div>
      <h3>Open to Collaborate</h3>
      <p>
        Interested in applied FEA, automated simulation workflows, or ML-accelerated physics problems?
        I am always open to collaborating on research or industry projects at the intersection of
        finite element methods, python scripting, and computational mechanics.
      </p>
    </div>
    <a href="mailto:shishirbarai9975@gmail.com" class="btn-collab">Get in Touch</a>
  </div>
</div>

<div class="site-footer">
  Shishir Barai &nbsp;·&nbsp; State College, PA &nbsp;·&nbsp;
  <a href="mailto:shishirbarai9975@gmail.com">shishirbarai9975@gmail.com</a> &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/in/shishir-barai/" target="_blank">LinkedIn</a>
</div>
