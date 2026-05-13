---
icon: fas fa-info-circle
order: 4
title:
---

<style>
  .about { margin-top: -1.5rem; }
  .about .hero {
    display: grid;
    grid-template-columns: 180px 1fr;
    gap: 1.75rem;
    align-items: center;
    padding: 2rem 0 1.5rem;
    border-bottom: 1px solid var(--main-border-color, rgba(128,128,128,0.2));
  }
  .about .hero img.avatar {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    object-fit: cover;
    box-shadow: 0 6px 22px rgba(0,0,0,0.18);
  }
  .about .hero h1 {
    margin: 0 0 .25rem;
    font-size: 2.1rem;
    font-weight: 700;
    line-height: 1.15;
  }
  .about .hero .role {
    color: var(--text-muted-color, #888);
    font-size: 1.05rem;
    margin-bottom: .35rem;
  }
  .about .hero .affil { font-size: .95rem; margin-bottom: 1rem; }
  .about .hero .cta { display: flex; flex-wrap: wrap; gap: .55rem; }
  .about .cta a {
    display: inline-flex; align-items: center; gap: .4rem;
    padding: .45rem .85rem;
    border-radius: 999px;
    border: 1px solid var(--btn-border-color, rgba(128,128,128,0.35));
    font-size: .9rem;
    text-decoration: none;
    transition: transform .12s ease, background-color .12s ease;
  }
  .about .cta a:hover { transform: translateY(-1px); background: rgba(128,128,128,0.08); }
  .about .cta a.primary {
    background: var(--link-color, #2a408e);
    border-color: transparent;
    color: #fff;
  }
  .about .cta a.primary:hover { opacity: .92; }

  .about section { padding: 1.5rem 0; }
  .about section + section { border-top: 1px solid var(--main-border-color, rgba(128,128,128,0.15)); }
  .about section h2 {
    font-size: 1.25rem;
    font-weight: 700;
    margin: 0 0 1rem;
    letter-spacing: .01em;
  }
  .about section h2 .accent { color: var(--link-color, #2a408e); }

  .about .grid-2 {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
  }
  .about .card {
    padding: 1rem 1.1rem;
    border: 1px solid var(--card-border-color, rgba(128,128,128,0.18));
    border-radius: 10px;
    background: var(--card-bg, transparent);
  }
  .about .card h3 {
    font-size: 1rem;
    font-weight: 600;
    margin: 0 0 .35rem;
  }
  .about .card p { margin: 0; font-size: .92rem; color: var(--text-muted-color, #888); }

  .about .tags { display: flex; flex-wrap: wrap; gap: .4rem; }
  .about .tags span {
    font-size: .8rem;
    padding: .25rem .6rem;
    border-radius: 6px;
    background: rgba(128,128,128,0.12);
  }

  .about .timeline { display: flex; flex-direction: column; gap: .9rem; }
  .about .timeline .item {
    display: grid;
    grid-template-columns: 130px 1fr;
    gap: 1rem;
    font-size: .94rem;
  }
  .about .timeline .when {
    color: var(--text-muted-color, #888);
    font-variant-numeric: tabular-nums;
    font-size: .88rem;
    padding-top: .15rem;
  }
  .about .timeline .what strong { display: block; }
  .about .timeline .what em { color: var(--text-muted-color, #888); font-style: normal; }

  .about .pub {
    padding: 1rem 1.1rem;
    border: 1px solid var(--card-border-color, rgba(128,128,128,0.18));
    border-left: 3px solid var(--link-color, #2a408e);
    border-radius: 8px;
    margin-bottom: .75rem;
  }
  .about .pub .pub-title { font-weight: 600; margin: 0 0 .25rem; }
  .about .pub .pub-authors { font-size: .9rem; color: var(--text-muted-color, #888); margin: 0 0 .15rem; }
  .about .pub .pub-venue { font-size: .88rem; font-style: italic; color: var(--text-muted-color, #888); margin: 0 0 .4rem; }
  .about .pub .pub-links { display: flex; flex-wrap: wrap; gap: .4rem; }
  .about .pub .pub-links a {
    font-size: .78rem;
    padding: .15rem .55rem;
    border-radius: 999px;
    background: rgba(128,128,128,0.12);
    text-decoration: none;
  }

  .about .lang-row {
    display: grid;
    grid-template-columns: 110px 1fr;
    gap: 1rem;
    padding: .35rem 0;
    border-bottom: 1px solid rgba(128,128,128,0.12);
    font-size: .94rem;
  }
  .about .lang-row:last-child { border-bottom: 0; }
  .about .lang-row .level { color: var(--text-muted-color, #888); }

  @media (max-width: 720px) {
    .about .hero { grid-template-columns: 1fr; text-align: center; }
    .about .hero img.avatar { margin: 0 auto; width: 140px; height: 140px; }
    .about .hero .cta { justify-content: center; }
    .about .grid-2 { grid-template-columns: 1fr; }
    .about .timeline .item { grid-template-columns: 1fr; }
    .about .lang-row { grid-template-columns: 1fr; }
  }
</style>

<div class="about">

  <header class="hero">
    <img class="avatar" src="{{ '/assets/img.jpeg' | relative_url }}" alt="Abdenour Soubih">
    <div>
      <h1>Abdenour Soubih</h1>
      <div class="role">PhD Student &middot; InfoLab @ SKKU &middot; AI Systems Engineering</div>
      <div class="affil">Researching trustworthy AI: federated learning security, adversarial ML, agentic systems, and LLMs.</div>
      <div class="cta">
        <a class="primary" href="mailto:abdenour@skku.edu"><i class="fas fa-envelope"></i> Email</a>
        <a href="https://scholar.google.com/citations?user=dxgFhR8AAAAJ" target="_blank" rel="noopener"><i class="fas fa-graduation-cap"></i> Google Scholar</a>
        <a href="https://orcid.org/0009-0002-4648-9289" target="_blank" rel="noopener"><i class="fab fa-orcid"></i> ORCID</a>
        <a href="https://github.com/soubihabdenour" target="_blank" rel="noopener"><i class="fab fa-github"></i> GitHub</a>
        <a href="https://www.linkedin.com/in/abdenour-soubih-5ba56a15a" target="_blank" rel="noopener"><i class="fab fa-linkedin"></i> LinkedIn</a>
        <a href="https://infolab-skku.github.io/members/abdenour-soubih.html" target="_blank" rel="noopener"><i class="fas fa-flask"></i> Lab Profile</a>
      </div>
    </div>
  </header>

  <section>
    <h2><span class="accent">/</span> About</h2>
    <p>
      I'm a PhD student at <a href="https://infolab-skku.github.io/" target="_blank" rel="noopener">InfoLab</a>,
      in the Department of AI Systems Engineering at Sungkyunkwan University (SKKU), South Korea.
      My research sits at the intersection of <strong>machine learning security</strong>,
      <strong>federated learning</strong>, and the emerging space of <strong>agentic AI systems</strong>
      built on top of large language models.
    </p>
    <p>
      I work on understanding how ML systems behave under realistic threat models — poisoning,
      inference, heterogeneity — and on designing mechanisms that keep them robust, private,
      and accountable when they're deployed beyond clean benchmark conditions. Alongside
      research, I'm a graduate teaching assistant for undergraduate C programming, and I
      maintain my course materials on this site.
    </p>
  </section>

  <section>
    <h2><span class="accent">/</span> Research areas</h2>
    <div class="grid-2">
      <div class="card">
        <h3>Security &amp; Adversarial ML</h3>
        <p>Threat models for ML pipelines and defenses that hold under realistic deployment.</p>
      </div>
      <div class="card">
        <h3>Federated Learning</h3>
        <p>Robustness under non-IID clients, poisoning attacks, and privacy leakage.</p>
      </div>
      <div class="card">
        <h3>Agentic AI Systems</h3>
        <p>Multi-agent coordination, tool use, and safety properties of LLM-driven agents.</p>
      </div>
      <div class="card">
        <h3>Large Language Models</h3>
        <p>Evaluation, alignment, and trust properties of LLM-based applications.</p>
      </div>
      <div class="card">
        <h3>Multi-agent Systems</h3>
        <p>Communication and emergent behavior across coordinating agents.</p>
      </div>
      <div class="card">
        <h3>Trustworthy AI</h3>
        <p>Privacy, robustness, and auditability as first-class system properties.</p>
      </div>
    </div>
  </section>

  <section>
    <h2><span class="accent">/</span> Publications</h2>

    <div class="pub">
      <p class="pub-title">Towards Robust Federated Learning: Investigating Poisoning Attacks Under Clients' Data Heterogeneity</p>
      <p class="pub-authors">Abdenour Soubih, Seyyid Ahmed Lahmer, Mohammed Abuhamad, Tamer Abuhmed</p>
      <p class="pub-venue">19th International Conference on Computing, Networking and Informatics (IMCOM), January 2025</p>
      <div class="pub-links">
        <a href="https://doi.org/10.1109/imcom64595.2025.10857574" target="_blank" rel="noopener">DOI</a>
        <a href="https://scholar.google.com/citations?user=dxgFhR8AAAAJ" target="_blank" rel="noopener">Scholar</a>
      </div>
    </div>
  </section>

  <section>
    <h2><span class="accent">/</span> Education</h2>
    <div class="timeline">
      <div class="item">
        <div class="when">2024 — present</div>
        <div class="what">
          <strong>Graduate Researcher, AI Systems Engineering</strong>
          <em>Sungkyunkwan University (SKKU), Suwon — InfoLab; ML security, federated learning, agentic systems</em>
        </div>
      </div>
      <div class="item">
        <div class="when">2018 — 2020</div>
        <div class="what">
          <strong>M.S., Computer Science</strong>
          <em>University of Oran 1 Ahmed Ben Bella — FIWARE-based IoT platform thesis</em>
        </div>
      </div>
      <div class="item">
        <div class="when">2015 — 2018</div>
        <div class="what">
          <strong>B.S., Computer Systems</strong>
          <em>UHBC University, Chlef — e-commerce &amp; online auction platform</em>
        </div>
      </div>
    </div>
  </section>

  <section>
    <h2><span class="accent">/</span> Experience</h2>
    <div class="grid-2">
      <div class="card">
        <h3>Graduate Teaching Assistant — SKKU</h3>
        <p>Labs and weekly exercises for undergraduate C programming. Course materials live on this site.</p>
      </div>
      <div class="card">
        <h3>WaterMed4.0 — PRIMA Project</h3>
        <p>Smart irrigation IoT systems with research teams in Spain and Turkey.</p>
      </div>
      <div class="card">
        <h3>Telecom Internship — Access Telecom</h3>
        <p>Cellular network performance and KPI analysis on real operator data.</p>
      </div>
      <div class="card">
        <h3>IoT &amp; Distributed Systems</h3>
        <p>FIWARE platform design, NGSI-LD context management, and real-time data pipelines.</p>
      </div>
    </div>
  </section>

  <section>
    <h2><span class="accent">/</span> Toolbox</h2>
    <div class="tags">
      <span>Python</span>
      <span>PyTorch</span>
      <span>Federated Learning</span>
      <span>Differential Privacy</span>
      <span>LLM tooling</span>
      <span>Multi-agent frameworks</span>
      <span>C</span>
      <span>Linux</span>
      <span>Docker</span>
      <span>FIWARE</span>
      <span>AWS IoT</span>
      <span>MQTT</span>
      <span>LoRaWAN</span>
      <span>NGSI-LD</span>
    </div>
  </section>

  <section>
    <h2><span class="accent">/</span> Languages</h2>
    <div class="lang-row"><strong>Arabic</strong><span class="level">Native</span></div>
    <div class="lang-row"><strong>French</strong><span class="level">Fluent</span></div>
    <div class="lang-row"><strong>English</strong><span class="level">Fluent</span></div>
  </section>

  <section>
    <h2><span class="accent">/</span> Get in touch</h2>
    <p>
      Open to research collaborations, PhD-track opportunities, and ML/AI engineering roles
      in trustworthy and privacy-aware AI. Reach me at
      <a href="mailto:abdenour@skku.edu">abdenour@skku.edu</a>.
    </p>
  </section>

</div>
