<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>India's Business Frontier 2024–2030</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body { font-family: 'DM Sans', sans-serif; background: #f5f5f3; color: #1a1a18; line-height: 1.6; }

    /* HERO */
    .hero {
      background: linear-gradient(135deg, #0C447C 0%, #185FA5 60%, #1D9E75 100%);
      color: #fff;
      padding: 4rem 2rem 3rem;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      top: -60px; right: -80px;
      width: 320px; height: 320px;
      border-radius: 50%;
      background: rgba(255,255,255,0.05);
    }
    .hero::after {
      content: '';
      position: absolute;
      bottom: -80px; left: -60px;
      width: 260px; height: 260px;
      border-radius: 50%;
      background: rgba(255,255,255,0.04);
    }
    .flag-stripe { display: flex; height: 5px; margin-bottom: 2rem; max-width: 200px; margin-left: auto; margin-right: auto; border-radius: 3px; overflow: hidden; }
    .s1 { flex:1; background:#FF9933; }
    .s2 { flex:1; background:#fff; }
    .s3 { flex:1; background:#138808; }
    .hero h1 { font-family: 'Playfair Display', serif; font-size: clamp(2rem, 5vw, 3rem); line-height: 1.2; margin-bottom: .75rem; position: relative; z-index: 1; }
    .hero p { font-size: 1rem; opacity: .85; max-width: 560px; margin: 0 auto 2rem; position: relative; z-index: 1; }
    .hero-stats { display: flex; justify-content: center; gap: 3rem; flex-wrap: wrap; position: relative; z-index: 1; }
    .hs { text-align: center; }
    .hs-num { font-size: 2rem; font-weight: 700; font-family: 'Playfair Display', serif; }
    .hs-label { font-size: .72rem; opacity: .7; text-transform: uppercase; letter-spacing: .09em; margin-top: 3px; }

    /* NAV */
    nav {
      background: #fff;
      border-bottom: 1px solid #e8e6e0;
      padding: .8rem 2rem;
      display: flex;
      gap: 1rem;
      justify-content: center;
      flex-wrap: wrap;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 1px 8px rgba(0,0,0,0.06);
    }
    nav a {
      font-size: .85rem;
      font-weight: 500;
      color: #5f5e5a;
      text-decoration: none;
      cursor: pointer;
      padding: .3rem .75rem;
      border-radius: 6px;
      transition: background .15s, color .15s;
    }
    nav a:hover { background: #f1efe8; color: #1a1a18; }

    /* SECTIONS */
    section { padding: 3rem 2rem; max-width: 960px; margin: 0 auto; }
    section:nth-child(even) { background: #fff; max-width: 100%; }
    section:nth-child(even) > * { max-width: 960px; margin-left: auto; margin-right: auto; }
    h2 { font-family: 'Playfair Display', serif; font-size: 1.8rem; margin-bottom: .3rem; color: #1a1a18; }
    .subtitle { font-size: .88rem; color: #888780; margin-bottom: 1.75rem; }

    /* SECTOR CARDS */
    .sector-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 14px; margin-bottom: 1rem; }
    .sector-card {
      background: #fff;
      border: 0.5px solid #e0ded8;
      border-radius: 14px;
      padding: 1.1rem 1rem 1rem 1.25rem;
      position: relative;
      overflow: hidden;
      transition: transform .2s, box-shadow .2s;
    }
    .sector-card:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0,0,0,0.08); }
    .sector-card::before { content: ''; position: absolute; top: 0; left: 0; width: 4px; height: 100%; }
    .sc-blue::before  { background: #185FA5; }
    .sc-green::before { background: #3B6D11; }
    .sc-amber::before { background: #BA7517; }
    .sc-teal::before  { background: #0F6E56; }
    .sc-coral::before { background: #993C1D; }
    .sc-purple::before{ background: #534AB7; }
    .sector-card h3 { font-size: .9rem; font-weight: 500; color: #1a1a18; margin-bottom: .3rem; }
    .sector-card .cagr { font-size: 1.6rem; font-weight: 700; font-family: 'Playfair Display', serif; color: #185FA5; }
    .sector-card .cagr-label { font-size: .7rem; color: #888780; margin-bottom: .4rem; }
    .sector-card .desc { font-size: .78rem; color: #5f5e5a; line-height: 1.55; }

    /* BAR CHART */
    .bar-section { margin-bottom: 1.5rem; }
    .bar-row { display: flex; align-items: center; gap: 12px; margin-bottom: 11px; }
    .bar-label { font-size: .82rem; color: #5f5e5a; min-width: 150px; text-align: right; }
    .bar-track { flex: 1; background: #f1efe8; border-radius: 4px; height: 24px; overflow: hidden; }
    .bar-fill {
      height: 100%;
      border-radius: 4px;
      display: flex;
      align-items: center;
      padding-left: 10px;
      font-size: .75rem;
      font-weight: 500;
      color: #fff;
      animation: growBar 1.2s ease forwards;
      transform-origin: left;
    }
    @keyframes growBar { from { width: 0% !important; } }
    .b1{background:#185FA5} .b2{background:#3B6D11} .b3{background:#BA7517}
    .b4{background:#0F6E56} .b5{background:#534AB7} .b6{background:#993C1D} .b7{background:#888780}

    /* TAGS */
    .tag-row { margin-top: 1rem; }
    .tag {
      display: inline-block;
      background: #E6F1FB;
      color: #0C447C;
      font-size: .72rem;
      padding: 3px 10px;
      border-radius: 20px;
      margin: 3px;
      font-weight: 500;
    }
    .tag-note { font-size: .78rem; color: #888780; margin-left: 6px; }

    /* DRIVERS */
    .drivers-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; margin-bottom: 1rem; }
    @media(max-width:520px) { .drivers-grid { grid-template-columns: 1fr; } }
    .driver-card { background: #f5f5f3; border-radius: 10px; padding: 1rem 1.1rem; }
    .driver-icon { font-size: 1.4rem; margin-bottom: .45rem; display: block; }
    .driver-title { font-size: .9rem; font-weight: 500; color: #1a1a18; margin-bottom: .3rem; }
    .driver-text { font-size: .8rem; color: #5f5e5a; line-height: 1.55; }

    /* TIMELINE */
    .timeline { position: relative; padding-left: 2rem; margin-bottom: 1rem; }
    .timeline::before {
      content: '';
      position: absolute;
      left: 7px; top: 10px; bottom: 10px;
      width: 2px;
      background: #d3d1c7;
    }
    .tl-item { position: relative; margin-bottom: 1.5rem; }
    .tl-dot {
      width: 14px; height: 14px;
      border-radius: 50%;
      background: #185FA5;
      position: absolute;
      left: -1.85rem;
      top: 4px;
      border: 3px solid #f5f5f3;
      box-shadow: 0 0 0 2px #185FA5;
    }
    .tl-year { font-size: .75rem; font-weight: 500; color: #185FA5; text-transform: uppercase; letter-spacing: .08em; margin-bottom: .2rem; }
    .tl-text { font-size: .88rem; color: #1a1a18; line-height: 1.6; }

    /* OPPORTUNITY TABLE */
    .opp-table { width: 100%; border-collapse: collapse; margin-bottom: 1rem; }
    .opp-table th { font-size: .78rem; font-weight: 500; color: #888780; text-align: left; padding: .5rem .75rem; border-bottom: 1px solid #e8e6e0; text-transform: uppercase; letter-spacing: .06em; }
    .opp-table td { font-size: .85rem; padding: .65rem .75rem; border-bottom: .5px solid #f1efe8; color: #1a1a18; }
    .opp-table tr:hover td { background: #f9f8f5; }
    .badge { display: inline-block; font-size: .7rem; padding: 2px 8px; border-radius: 20px; font-weight: 500; }
    .badge-high { background: #EAF3DE; color: #3B6D11; }
    .badge-med  { background: #FAEEDA; color: #854F0B; }
    .badge-low  { background: #E6F1FB; color: #185FA5; }

    /* FOOTER */
    footer {
      background: #1a1a18;
      color: #888780;
      text-align: center;
      padding: 2.5rem 2rem;
      font-size: .82rem;
    }
    footer strong { color: #d3d1c7; }

    @media(max-width:600px) {
      .hero-stats { gap: 1.5rem; }
      .bar-label { min-width: 100px; font-size: .75rem; }
      nav a { font-size: .78rem; padding: .25rem .5rem; }
    }
  </style>
</head>
<body>

<div class="hero">
  <div class="flag-stripe"><div class="s1"></div><div class="s2"></div><div class="s3"></div></div>
  <h1>India's Business Frontier<br>2024 – 2030</h1>
  <p>The world's fastest-growing major economy — where capital flows, talent rises, and sectors transform at scale.</p>
  <div class="hero-stats">
    <div class="hs"><div class="hs-num">$7T</div><div class="hs-label">GDP target by 2030</div></div>
    <div class="hs"><div class="hs-num">6.8%</div><div class="hs-label">Projected GDP CAGR</div></div>
    <div class="hs"><div class="hs-num">#3</div><div class="hs-label">Economy globally by 2027</div></div>
    <div class="hs"><div class="hs-num">1.4B</div><div class="hs-label">Consumer base</div></div>
  </div>
</div>

<nav>
  <a href="#sectors">Sectors</a>
  <a href="#investment">FDI Inflows</a>
  <a href="#drivers">Growth Drivers</a>
  <a href="#opportunities">Opportunities</a>
  <a href="#roadmap">Roadmap</a>
</nav>

<section id="sectors">
  <h2>High-growth sectors</h2>
  <p class="subtitle">Projected CAGR 2024–2030 across key industries</p>
  <div class="sector-grid">
    <div class="sector-card sc-blue">
      <h3>Technology & AI</h3>
      <div class="cagr">18%</div>
      <div class="cagr-label">CAGR</div>
      <div class="desc">India's $245B IT sector expanding into GenAI, cloud, and SaaS globally.</div>
    </div>
    <div class="sector-card sc-green">
      <h3>Renewable Energy</h3>
      <div class="cagr">22%</div>
      <div class="cagr-label">CAGR</div>
      <div class="desc">500 GW clean energy target by 2030 driving massive infrastructure investment.</div>
    </div>
    <div class="sector-card sc-amber">
      <h3>Fintech</h3>
      <div class="cagr">20%</div>
      <div class="cagr-label">CAGR</div>
      <div class="desc">UPI dominance, credit penetration, and neo-banking reshaping India's finance stack.</div>
    </div>
    <div class="sector-card sc-teal">
      <h3>Healthcare</h3>
      <div class="cagr">15%</div>
      <div class="cagr-label">CAGR</div>
      <div class="desc">Medtech, generic pharma exports, and hospital chains scaling rapidly.</div>
    </div>
    <div class="sector-card sc-coral">
      <h3>Manufacturing</h3>
      <div class="cagr">12%</div>
      <div class="cagr-label">CAGR</div>
      <div class="desc">PLI schemes attracting Apple, Samsung & global supply chain diversification.</div>
    </div>
    <div class="sector-card sc-purple">
      <h3>EV & Mobility</h3>
      <div class="cagr">25%</div>
      <div class="cagr-label">CAGR</div>
      <div class="desc">World's fastest-growing EV 2-wheeler market with charging infra boom.</div>
    </div>
  </div>
</section>

<section id="investment" style="background:#fff;max-width:100%;padding:3rem 2rem">
  <div style="max-width:960px;margin:0 auto">
    <h2>FDI inflows by sector</h2>
    <p class="subtitle">Share of foreign direct investment flowing into India (2023–24)</p>
    <div class="bar-section">
      <div class="bar-row"><div class="bar-label">Services</div><div class="bar-track"><div class="bar-fill b1" style="width:28%">28%</div></div></div>
      <div class="bar-row"><div class="bar-label">Computer Software</div><div class="bar-track"><div class="bar-fill b2" style="width:22%">22%</div></div></div>
      <div class="bar-row"><div class="bar-label">Trading</div><div class="bar-track"><div class="bar-fill b3" style="width:14%">14%</div></div></div>
      <div class="bar-row"><div class="bar-label">Telecom</div><div class="bar-track"><div class="bar-fill b4" style="width:10%">10%</div></div></div>
      <div class="bar-row"><div class="bar-label">Automobile</div><div class="bar-track"><div class="bar-fill b5" style="width:9%">9%</div></div></div>
      <div class="bar-row"><div class="bar-label">Pharma</div><div class="bar-track"><div class="bar-fill b6" style="width:8%">8%</div></div></div>
      <div class="bar-row"><div class="bar-label">Others</div><div class="bar-track"><div class="bar-fill b7" style="width:9%">9%</div></div></div>
    </div>
    <div class="tag-row">
      <span class="tag">USA</span><span class="tag">Mauritius</span><span class="tag">Singapore</span><span class="tag">Netherlands</span><span class="tag">Japan</span><span class="tag">UAE</span>
      <span class="tag-note">Top FDI source nations</span>
    </div>
  </div>
</section>

<section id="drivers">
  <h2>Core growth drivers</h2>
  <p class="subtitle">Structural forces shaping India's business trajectory through 2030</p>
  <div class="drivers-grid">
    <div class="driver-card">
      <span class="driver-icon">🏗</span>
      <div class="driver-title">₹11.1L Cr infrastructure push</div>
      <div class="driver-text">Union Budget 2024–25 allocates record capex. Roads, railways, ports, and smart cities at the core of India's build-out.</div>
    </div>
    <div class="driver-card">
      <span class="driver-icon">📱</span>
      <div class="driver-title">Digital India at scale</div>
      <div class="driver-text">900M+ internet users, UPI processing 14B+ monthly transactions, ONDC democratizing commerce for small businesses.</div>
    </div>
    <div class="driver-card">
      <span class="driver-icon">🎓</span>
      <div class="driver-title">World's youngest workforce</div>
      <div class="driver-text">Median age 28. 65% under 35. Largest engineering graduate output globally — 1.5M engineers per year.</div>
    </div>
    <div class="driver-card">
      <span class="driver-icon">🏭</span>
      <div class="driver-title">China+1 beneficiary</div>
      <div class="driver-text">Global firms diversifying supply chains; India wins in electronics, chemicals, textiles, and defense manufacturing.</div>
    </div>
    <div class="driver-card">
      <span class="driver-icon">🏙</span>
      <div class="driver-title">Urbanization wave</div>
      <div class="driver-text">600M urban residents projected by 2036. Tier 2 & 3 cities emerging as new consumption and startup hubs.</div>
    </div>
    <div class="driver-card">
      <span class="driver-icon">📜</span>
      <div class="driver-title">Policy reforms</div>
      <div class="driver-text">GST maturity, IBC efficiency, ease of doing business improvements, and PLI schemes totaling ₹2L Cr across sectors.</div>
    </div>
  </div>
</section>

<section id="opportunities" style="background:#fff;max-width:100%;padding:3rem 2rem">
  <div style="max-width:960px;margin:0 auto">
    <h2>Investment opportunities snapshot</h2>
    <p class="subtitle">High-conviction business bets for 2024–2030</p>
    <table class="opp-table">
      <thead>
        <tr>
          <th>Opportunity</th>
          <th>Sector</th>
          <th>Market Size (2030E)</th>
          <th>Conviction</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>GenAI & SaaS for Bharat</td><td>Technology</td><td>$50B+</td><td><span class="badge badge-high">High</span></td></tr>
        <tr><td>Green hydrogen production</td><td>Energy</td><td>$8B</td><td><span class="badge badge-high">High</span></td></tr>
        <tr><td>Digital credit & insurance</td><td>Fintech</td><td>$30B</td><td><span class="badge badge-high">High</span></td></tr>
        <tr><td>EV battery supply chain</td><td>Mobility</td><td>$20B</td><td><span class="badge badge-high">High</span></td></tr>
        <tr><td>Semiconductor packaging</td><td>Manufacturing</td><td>$15B</td><td><span class="badge badge-med">Medium</span></td></tr>
        <tr><td>Health-tech & diagnostics</td><td>Healthcare</td><td>$22B</td><td><span class="badge badge-high">High</span></td></tr>
        <tr><td>Space tech (ISRO spinoffs)</td><td>Aerospace</td><td>$44B</td><td><span class="badge badge-med">Medium</span></td></tr>
        <tr><td>AgriTech & cold chain</td><td>Agriculture</td><td>$24B</td><td><span class="badge badge-low">Emerging</span></td></tr>
      </tbody>
    </table>
  </div>
</section>

<section id="roadmap">
  <h2>Business development roadmap</h2>
  <p class="subtitle">Key milestones and opportunities on the horizon</p>
  <div class="timeline">
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-year">2024 – 25</div>
      <div class="tl-text">PLI scheme maturation across 14 sectors; semiconductor fab groundbreakings; AI startup ecosystem boom in Bengaluru & Hyderabad. India crosses $4T GDP.</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-year">2025 – 26</div>
      <div class="tl-text">India overtakes Japan & Germany to become 3rd largest economy. Renewables cross 350 GW installed. EV penetration hits 15% for 2-wheelers.</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-year">2026 – 27</div>
      <div class="tl-text">ONDC scales to 100M merchants. 5G coverage reaches 90% of all districts. Green hydrogen projects become commercially viable. Defense exports hit $5B.</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-year">2027 – 28</div>
      <div class="tl-text">India's semiconductor fabs begin production. Global MNCs expand India GCCs to 2,000+. Tier 2 city startup density triples from 2023 levels.</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-year">2028 – 29</div>
      <div class="tl-text">Space economy hits $44B; ISRO commercialization drives spinoffs. India becomes net exporter of solar panels and lithium-ion cells.</div>
    </div>
    <div class="tl-item">
      <div class="tl-dot"></div>
      <div class="tl-year">2030</div>
      <div class="tl-text">$7T GDP milestone achieved. 500 GW renewable capacity online. 100+ unicorns active. India's startup ecosystem rivals Silicon Valley in breadth and depth.</div>
    </div>
  </div>
</section>

<footer>
  <strong>India Business Outlook 2024–2030</strong><br><br>
  Data sourced from DPIIT, RBI, NITI Aayog, World Bank, and IMF projections.<br>
  This site is for informational purposes. Projections are estimates based on publicly available economic data.
</footer>

</body>
</html>
