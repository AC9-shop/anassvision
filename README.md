<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>رؤيـة أنس | Anass Vision</title>
<meta name="description" content="رؤيـة أنس: قناة تأخذكم في رحلة عبر القصص والتاريخ والأفكار المتنوعة. حكايات من الماضي والحاضر، تحليلات، ومستجدات تثير الفضول.">
<meta property="og:type" content="website">
<meta property="og:title" content="رؤيـة أنس | Anass Vision">
<meta property="og:description" content="رحلة عبر القصص والتاريخ والأفكار المتنوعة.">
<meta property="og:image" content="">
<meta name="twitter:card" content="summary_large_image">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Aref+Ruqaa:wght@400;700&family=Cairo:wght@300;400;500;600;700;900&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #101d17;
    --bg-deep: #0a130e;
    --panel: #1a2b21;
    --panel-2: #1f3327;
    --moss: #3f5c46;
    --gold: #cda15a;
    --gold-light: #ecd39c;
    --teal: #3f8f88;
    --cream: #efe6cd;
    --cream-dim: #cfc6ab;
    --line: rgba(205,161,90,0.25);
    --overlay-bg: rgba(10,19,14,0.55);
  }
  html[data-theme="light"]{
    --bg: #f6f1e2;
    --bg-deep: #ece3cc;
    --panel: #ffffff;
    --panel-2: #f4ecd8;
    --moss: #7fa389;
    --gold: #a9793a;
    --gold-light: #7c5a26;
    --teal: #2f6e68;
    --cream: #20291f;
    --cream-dim: #55604f;
    --line: rgba(90,70,30,0.18);
    --overlay-bg: rgba(246,241,226,0.68);
  }

  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background: var(--bg);
    color: var(--cream);
    font-family: 'Cairo', sans-serif;
    overflow-x: hidden;
    position: relative;
    min-height:100vh;
    transition: background .35s ease, color .35s ease;
  }
  body::before{
    content:"";
    position:fixed; inset:0;
    background-image:
      radial-gradient(circle at 15% 20%, rgba(63,143,136,0.10), transparent 40%),
      radial-gradient(circle at 85% 70%, rgba(205,161,90,0.08), transparent 45%);
    pointer-events:none;
    z-index:0;
  }
  h1,h2,h3, .display{ font-family:'Aref Ruqaa', serif; font-weight:700; }
  .eyebrow{
    font-family:'Cairo',sans-serif; font-size:0.8rem; letter-spacing:0.15em;
    color: var(--gold); text-transform:uppercase; display:flex; align-items:center; gap:10px;
  }
  .eyebrow::after{ content:""; flex:1; height:1px; background: var(--line); }
  a{color:inherit; text-decoration:none;}
  .wrap{ max-width: 980px; margin: 0 auto; padding: 0 28px; position:relative; z-index:2; }

  /* ===== PATH LAYER (home only) ===== */
  #pathLayer{ position:absolute; top:0; left:0; width:100%; height:100%; z-index:1; pointer-events:none; }
  #pathLayer svg{ width:100%; height:100%; display:block; }
  #routeLine{ fill:none; stroke: var(--gold); stroke-width:2; stroke-dasharray: 7 10; opacity:0.55; }
  #routeLineGlow{ fill:none; stroke: var(--teal); stroke-width:6; opacity:0.08; filter: blur(2px); }

  /* ===== PAGE TRANSITION OVERLAY ===== */
  #pageTransition{
    position:fixed; inset:0; z-index:999;
    background: var(--bg);
    display:flex; align-items:center; justify-content:center;
    opacity:0; pointer-events:none;
    transition: opacity .22s ease;
  }
  #pageTransition.show{ opacity:1; pointer-events:all; }
  .loader-plane{
    font-size:1.8rem;
    color: var(--gold);
    animation: loaderMove 0.9s ease-in-out infinite alternate;
  }
  @keyframes loaderMove{
    from{ transform: translateX(-16px) rotate(0deg); }
    to{ transform: translateX(16px) rotate(0deg); }
  }

  /* ===== HEADER / NAV ===== */
  header{
    position:sticky; top:0; z-index:20;
    backdrop-filter: blur(10px);
    background: var(--overlay-bg);
    border-bottom: 1px solid var(--line);
    transition: background .35s ease;
  }
  .nav{ display:flex; align-items:center; justify-content:space-between; padding: 16px 28px; max-width:980px; margin:0 auto; gap:16px; }
  .brand{ display:flex; align-items:center; gap:12px; }
  .brand .mark{
    width:38px; height:38px; border-radius:50%;
    background: conic-gradient(from 45deg, var(--teal), var(--gold), var(--teal));
    display:flex; align-items:center; justify-content:center;
    font-family:'Aref Ruqaa',serif; font-weight:700; color: var(--bg-deep); font-size:1.1rem; flex-shrink:0;
  }
  .brand-name{ font-family:'Aref Ruqaa', serif; font-size:1.3rem; color: var(--gold-light); white-space:nowrap; }
  .nav-links{ display:flex; align-items:center; gap:22px; font-size:0.92rem; font-weight:600; flex:1; justify-content:center; }
  .nav-links a{ color: var(--cream-dim); padding-bottom:4px; border-bottom:2px solid transparent; transition: color .2s ease, border-color .2s ease; cursor:pointer; white-space:nowrap; }
  .nav-links a:hover, .nav-links a.active{ color: var(--gold-light); border-color: var(--gold); }
  .nav-right{ display:flex; align-items:center; gap:12px; }
  .theme-toggle{
    width:38px; height:38px; border-radius:50%;
    border:1px solid var(--line); background:transparent; color: var(--gold);
    display:flex; align-items:center; justify-content:center; cursor:pointer;
    font-size:1.05rem; transition: border-color .2s ease, transform .3s ease;
    flex-shrink:0;
  }
  .theme-toggle:hover{ border-color: var(--gold); transform: rotate(20deg); }
  .nav-cta{
    background: var(--gold); color: var(--bg-deep); padding: 9px 20px; border-radius: 999px;
    font-weight:700; font-size:0.9rem; transition: transform .2s ease, box-shadow .2s ease; white-space:nowrap;
  }
  .nav-cta:hover{ transform: translateY(-2px); box-shadow:0 8px 20px rgba(205,161,90,0.25); }

  /* ===== PAGES ===== */
  .page{ display:none; position:relative; }
  .page.active{ display:block; }

  /* ===== HERO with parallax bg (home) ===== */
  .hero-media{
    position:relative;
    height:220px;
    overflow:hidden;
    border-bottom: 1px solid var(--line);
  }
  .hero-media img{
    position:absolute; top:50%; left:0;
    width:100%; height:140%;
    object-fit:cover;
    transform: translateY(-50%);
    will-change: transform;
    filter: saturate(0.9) brightness(0.55);
  }
  .hero-media::after{
    content:"";
    position:absolute; inset:0;
    background: linear-gradient(180deg, rgba(10,19,14,0.2), var(--bg) 95%);
  }

  .page-hero{ padding: 70px 0 20px; text-align:center; position:relative; z-index:2; }
  .page-hero .eyebrow{ justify-content:center; }
  .page-hero .eyebrow::after{ display:none; }
  .page-hero .eyebrow::before{ content:""; flex:0 0 40px; height:1px; background: var(--line); }
  .page-hero h1{ font-size: clamp(2.2rem, 6vw, 3.2rem); color: var(--gold-light); margin-top:18px; }
  .page-hero p{ max-width:520px; margin: 20px auto 0; color: var(--cream-dim); line-height:1.9; font-size:1.05rem; }
  .route-divider{
    width:100%; height:2px; margin: 40px auto 0; max-width:980px;
    background-image: repeating-linear-gradient(to left, var(--gold) 0 10px, transparent 10px 20px);
    opacity:0.4;
  }

  .hero{ position:relative; padding: 50px 0 60px; text-align:center; }
  .hero .eyebrow{ justify-content:center; margin-bottom:22px; }
  .hero .eyebrow::after{ display:none; }
  .hero .eyebrow::before{ content:""; flex:0 0 40px; height:1px; background: var(--line); }
  .hero h1{ font-size: clamp(2.6rem, 7vw, 4.4rem); line-height:1.15; color: var(--gold-light); text-shadow: 0 0 40px rgba(205,161,90,0.2); }
  .hero h1 span{ color: var(--teal); }
  .hero p.tagline{ max-width:560px; margin: 26px auto 0; font-size:1.15rem; color: var(--cream-dim); line-height:1.9; }
  .hero-actions{ margin-top:38px; display:flex; gap:16px; justify-content:center; flex-wrap:wrap; }
  .btn-primary{
    background: var(--gold); color: var(--bg-deep); padding: 15px 34px; border-radius: 999px;
    font-weight:700; font-size:1rem; transition: transform .2s ease, box-shadow .2s ease; display:inline-block; cursor:pointer; border:none;
    font-family:'Cairo',sans-serif;
  }
  .btn-primary:hover{ transform: translateY(-3px); box-shadow: 0 10px 30px rgba(205,161,90,0.3); }
  .btn-ghost{
    border: 1px solid var(--line); color: var(--cream); padding: 15px 30px; border-radius: 999px;
    font-weight:600; transition: border-color .2s ease, background .2s ease; display:inline-block; cursor:pointer;
    background:transparent; font-family:'Cairo',sans-serif; font-size:1rem;
  }
  .btn-ghost:hover{ border-color: var(--gold); background: rgba(205,161,90,0.06); }
  .stats{ margin-top:56px; display:flex; justify-content:center; gap:0; flex-wrap:wrap; }
  .stat{ padding: 0 34px; border-left: 1px solid var(--line); }
  .stat:last-child{border-left:none;}
  .stat .num{ font-family:'Aref Ruqaa',serif; font-size:2rem; color:var(--teal); display:block; }
  .stat .lbl{ font-size:0.8rem; color: var(--cream-dim); }

  section{ position:relative; padding: 90px 0; }
  .section-head{ max-width:560px; margin-bottom:50px; }
  .section-head h2{ font-size: clamp(1.9rem, 4vw, 2.6rem); color: var(--gold-light); margin-top:14px; line-height:1.3; }

  .about-card{
    background: linear-gradient(160deg, var(--panel), var(--panel-2));
    border: 1px solid var(--line); border-radius: 20px; padding: 46px; position:relative; max-width:640px;
  }
  .about-card::before{
    content:"”"; position:absolute; top:8px; right:28px;
    font-family:'Aref Ruqaa',serif; font-size:5rem; color: var(--teal); opacity:0.35;
  }
  .about-card p{ font-size:1.08rem; line-height:2.1; color: var(--cream-dim); position:relative; z-index:2; }
  .about-card p + p{ margin-top:18px; }

  .waypoints{ display:flex; flex-direction:column; gap:26px; }
  .waypoint{
    display:flex; align-items:flex-start; gap:24px;
    background: rgba(26,43,33,0.5); border:1px solid var(--line); border-radius:18px; padding: 28px 30px;
    transition: border-color .25s ease, transform .25s ease, background .25s ease;
  }
  html[data-theme="light"] .waypoint{ background: rgba(255,255,255,0.5); }
  .waypoint:hover{ border-color: var(--gold); transform: translateY(-4px); }
  .waypoint .wp-icon{
    flex: 0 0 56px; width:56px; height:56px; border-radius:50%;
    background: rgba(205,161,90,0.1); border:1px solid var(--gold);
    display:flex; align-items:center; justify-content:center; font-size:1.5rem; color: var(--gold);
    transition: transform .3s ease;
  }
  .waypoint:hover .wp-icon{ transform: rotate(-8deg) scale(1.08); }
  .waypoint .wp-body h3{ font-size:1.3rem; color: var(--gold-light); margin-bottom:8px; }
  .waypoint .wp-body p{ color: var(--cream-dim); line-height:1.85; font-size:0.98rem; }

  .dest-grid{ display:grid; grid-template-columns: repeat(3, 1fr); gap:22px; }
  .dest-card{
    display:block; background: linear-gradient(160deg, var(--panel), var(--panel-2));
    border:1px solid var(--line); border-radius:20px; padding: 30px 26px;
    transition: border-color .25s ease, transform .25s ease; cursor:pointer;
  }
  .dest-card:hover{ border-color: var(--gold); transform: translateY(-5px); }
  .dest-card .dc-icon{ font-size:1.7rem; color: var(--gold); margin-bottom:14px; transition: transform .3s ease; }
  .dest-card:hover .dc-icon{ transform: scale(1.15); }
  .dest-card h3{ font-size:1.25rem; color: var(--gold-light); margin-bottom:8px; }
  .dest-card p{ color: var(--cream-dim); font-size:0.92rem; line-height:1.75; }
  .dest-card .dc-arrow{ margin-top:16px; color: var(--teal); font-weight:700; font-size:0.85rem; }

  /* ===== TESTIMONIALS ===== */
  .testi-row{ display:grid; grid-template-columns: repeat(3, 1fr); gap:20px; }
  .testi-card{
    background: rgba(26,43,33,0.4); border:1px solid var(--line); border-radius:16px; padding:26px;
  }
  html[data-theme="light"] .testi-card{ background: rgba(255,255,255,0.5); }
  .testi-card .stars{ color: var(--gold); font-size:0.95rem; margin-bottom:12px; letter-spacing:2px; }
  .testi-card p{ color: var(--cream-dim); font-size:0.95rem; line-height:1.8; margin-bottom:16px; }
  .testi-card .who{ display:flex; align-items:center; gap:10px; }
  .testi-card .who .avatar{
    width:34px; height:34px; border-radius:50%;
    background: conic-gradient(from 45deg, var(--teal), var(--gold));
    display:flex; align-items:center; justify-content:center;
    font-size:0.85rem; color: var(--bg-deep); font-weight:700; font-family:'Aref Ruqaa',serif;
  }
  .testi-card .who span{ font-size:0.88rem; color: var(--cream); font-weight:600; }

  /* ===== NEWSLETTER ===== */
  .newsletter{
    background: linear-gradient(160deg, var(--panel), var(--panel-2));
    border:1px solid var(--line); border-radius:22px; padding:44px;
    text-align:center;
  }
  .newsletter h2{ color: var(--gold-light); font-size:1.7rem; margin-bottom:12px; }
  .newsletter p{ color: var(--cream-dim); margin-bottom:26px; }
  .newsletter-form{ display:flex; gap:12px; max-width:440px; margin:0 auto; flex-wrap:wrap; justify-content:center; }
  .newsletter-form input{
    flex:1; min-width:220px;
    background: var(--bg-deep); border:1px solid var(--line); color: var(--cream);
    padding: 13px 18px; border-radius:999px; font-family:'Cairo',sans-serif; font-size:0.95rem;
  }
  .newsletter-form input:focus{ outline:none; border-color: var(--gold); }
  .newsletter-note{ margin-top:14px; font-size:0.85rem; color: var(--teal); min-height:20px; }

  /* ===== SEARCH / FILTER ===== */
  .filter-bar{
    display:flex; gap:12px; flex-wrap:wrap; align-items:center; margin-bottom:36px;
  }
  .filter-bar input[type="text"]{
    flex:1; min-width:200px;
    background: var(--panel); border:1px solid var(--line); color: var(--cream);
    padding: 12px 18px; border-radius:999px; font-family:'Cairo',sans-serif; font-size:0.95rem;
  }
  .filter-bar input[type="text"]:focus{ outline:none; border-color: var(--gold); }
  .chip-row{ display:flex; gap:8px; flex-wrap:wrap; }
  .chip{
    padding:9px 18px; border-radius:999px; border:1px solid var(--line);
    font-size:0.85rem; font-weight:600; color: var(--cream-dim); cursor:pointer;
    transition: all .2s ease; background:transparent; font-family:'Cairo',sans-serif;
  }
  .chip.active, .chip:hover{ border-color: var(--gold); color: var(--gold-light); }

  /* ===== FEATURED STRIP ===== */
  .featured-strip{
    display:grid; grid-template-columns: repeat(2, 1fr); gap:18px; margin-bottom:50px;
  }
  .featured-card{
    display:flex; gap:16px; align-items:center;
    background: var(--panel); border:1px solid var(--gold); border-radius:14px; padding:14px;
    transition: transform .25s ease;
  }
  .featured-card:hover{ transform: translateY(-3px); }
  .featured-card img{ width:90px; height:60px; object-fit:cover; border-radius:8px; flex-shrink:0; }
  .featured-card .fc-body h4{ font-size:0.95rem; color:var(--cream); margin-bottom:4px; }
  .featured-card .fc-body span{ font-size:0.78rem; color: var(--gold); }

  /* ===== EPISODE / VIDEO GRID ===== */
  .ep-grid{ display:grid; grid-template-columns: repeat(2, 1fr); gap:22px; }
  .ep-card{
    display:block; background: var(--panel); border:1px solid var(--line); border-radius:16px;
    overflow:hidden; transition: transform .25s ease, border-color .25s ease;
    position:relative;
  }
  .ep-card:hover{ transform: translateY(-5px); border-color: var(--gold); }
  .ep-thumb{
    height:150px;
    background: radial-gradient(circle at 30% 30%, rgba(63,143,136,0.5), transparent 60%), linear-gradient(135deg, var(--panel-2), var(--bg-deep));
    display:flex; align-items:center; justify-content:center; position:relative; overflow:hidden;
  }
  .ep-thumb img{ position:absolute; inset:0; width:100%; height:100%; object-fit:cover; opacity:0.85; }
  .ep-thumb .play{
    z-index:2; width:46px; height:46px; border-radius:50%;
    background: rgba(239,230,205,0.12); border:1px solid var(--gold);
    display:flex; align-items:center; justify-content:center; color: var(--gold-light); font-size:1.1rem;
  }
  .ep-tag{
    position:absolute; top:12px; right:12px; z-index:2; font-size:0.7rem;
    background: rgba(10,19,14,0.7); color: var(--gold); padding: 4px 10px; border-radius:999px; border:1px solid var(--line);
  }
  .ep-info{ padding:18px 20px 20px; }
  .ep-info h4{ font-family:'Cairo',sans-serif; font-weight:700; font-size:1.02rem; color:var(--cream); margin-bottom:6px; line-height:1.5; }
  .ep-meta{ display:flex; align-items:center; justify-content:space-between; }
  .ep-meta span{ font-size:0.8rem; color:var(--cream-dim); }
  .share-row{ display:flex; gap:8px; }
  .share-btn{
    width:30px; height:30px; border-radius:50%; border:1px solid var(--line);
    display:flex; align-items:center; justify-content:center; font-size:0.85rem;
    color: var(--cream-dim); transition: border-color .2s ease, color .2s ease, transform .2s ease;
  }
  .share-btn:hover{ border-color: var(--gold); color: var(--gold-light); transform: translateY(-2px); }

  .ep-card.video-card video{ width:100%; height:180px; object-fit:cover; display:block; background: var(--bg-deep); }
  .ep-cta{ text-align:center; margin-top:40px; }
  .empty-note{
    color: var(--cream-dim); border: 1px dashed var(--line); border-radius:16px; padding: 30px;
    text-align:center; font-size:0.95rem; line-height:1.8; grid-column: 1 / -1;
  }

  /* ===== ABOUT PAGE ===== */
  .about-hero{ display:flex; gap:40px; align-items:center; flex-wrap:wrap; padding: 60px 0; }
  .about-photo{
    width:180px; height:180px; border-radius:50%; flex-shrink:0;
    background: conic-gradient(from 45deg, var(--teal), var(--gold), var(--teal));
    padding:6px;
  }
  .about-photo .inner{
    width:100%; height:100%; border-radius:50%;
    background: var(--bg-deep);
    display:flex; align-items:center; justify-content:center;
    font-family:'Aref Ruqaa',serif; font-size:3rem; color: var(--gold);
    overflow:hidden;
  }
  .about-photo .inner img{ width:100%; height:100%; object-fit:cover; }
  .about-text{ flex:1; min-width:260px; }
  .about-text h2{ font-size:2rem; color: var(--gold-light); margin-bottom:16px; }
  .about-text p{ color: var(--cream-dim); line-height:2; margin-bottom:14px; font-size:1.02rem; }
  .about-timeline{ display:flex; flex-direction:column; gap:22px; margin-top:20px; }
  .about-timeline .t-item{ display:flex; gap:18px; }
  .about-timeline .t-dot{
    width:12px; height:12px; border-radius:50%; background: var(--gold); margin-top:6px; flex-shrink:0;
  }
  .about-timeline .t-body h4{ color: var(--gold-light); font-size:1.05rem; margin-bottom:4px; }
  .about-timeline .t-body p{ color: var(--cream-dim); font-size:0.92rem; line-height:1.7; }

  /* ===== FOOTER ===== */
  footer{ position:relative; padding: 70px 0 40px; text-align:center; border-top:1px solid var(--line); }
  footer .mark-big{
    width:64px; height:64px; margin: 0 auto 20px; border-radius:50%;
    background: conic-gradient(from 45deg, var(--teal), var(--gold), var(--teal));
    display:flex; align-items:center; justify-content:center;
    font-family:'Aref Ruqaa',serif; color: var(--bg-deep); font-size:1.6rem; font-weight:700;
  }
  footer h3{ font-size:1.7rem; color: var(--gold-light); margin-bottom:16px; }
  .social-row{ display:flex; justify-content:center; gap:16px; margin: 26px 0 40px; flex-wrap:wrap; }
  .social-row a{ padding:10px 22px; border:1px solid var(--line); border-radius:999px; font-size:0.9rem; transition: border-color .2s ease, color .2s ease; }
  .social-row a:hover{ border-color: var(--gold); color: var(--gold-light); }
  .fine{ color: var(--cream-dim); font-size:0.8rem; opacity:0.7; }

  @media (max-width: 720px){
    .ep-grid{ grid-template-columns: 1fr; }
    .dest-grid{ grid-template-columns: 1fr; }
    .testi-row{ grid-template-columns: 1fr; }
    .featured-strip{ grid-template-columns: 1fr; }
    .stat{ padding:0 18px; }
    .nav-links{ display:none; }
    .about-hero{ flex-direction:column; text-align:center; }
  }
  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ transition:none !important; animation:none !important; }
  }
</style>
</head>
<body>
<audio src="Anass Vision.mp3" autoplay loop ></audio>

<div id="pageTransition"><span class="loader-plane">✈</span></div>

<header>
  <div class="nav">
    <div class="brand">
      <div class="mark"><img src="3.png" alt="Photo" style="width:45px;height:45px;border-radius:50%;object-fit:cover;"></div>
      <span class="brand-name">رؤيـة أنس</span>
    </div>
    <nav class="nav-links">
      <a data-page="home" class="active">الرئيسية</a>
      <a data-page="episodes">الحلقات</a>
      <a data-page="videos">فيديوهات</a>
      <a data-page="about">من أنا</a>
    </nav>
    <div class="nav-right">
      <button class="theme-toggle" id="themeToggle" title="بدل المظهر">🌙</button>
      <a class="nav-cta" href="https://www.youtube.com/channel/UCzPGTjQSHJmgtR3Mdohu_Yw" target="_blank" rel="noopener">اشترك الآن</a>
    </div>
  </div>
</header>

<!-- ============ PAGE: HOME ============ -->
<div class="page active" id="page-home">
  <div class="hero-media" id="parallaxWrap">
    <img id="parallaxImg" src="data:image/jpeg;base64,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" alt="">
  </div>

  <div id="pathLayer">
    <svg preserveAspectRatio="none">
      <path id="routeLineGlow" d=""></path>
      <path id="routeLine" d=""></path>
      <g id="plane">
        <text x="0" y="0" font-size="22" text-anchor="middle" dominant-baseline="middle" fill="#cda15a" transform="rotate(90)">✈</text>
      </g>
    </svg>
  </div>

  <main class="wrap">
    <section class="hero" id="stop-0">
      <p class="eyebrow">رحلة عبر الزمن والأفكار</p>
      <h1>حكايات لا تُروى<br><span>مرتين</span></h1>
      <p class="tagline">
        قناة تأخذكم في رحلة عبر القصص والتاريخ والأفكار المتنوعة،
        نكتشف فيها المعرفة بطريقة ممتعة وغامضة في آن واحد.
      </p>
      <div class="hero-actions">
        <button class="btn-primary" data-page="episodes">شاهد آخر حلقة</button>
        <a class="btn-ghost" href="#waypoints">اكتشف المحطات</a>
      </div>
      <div class="stats">
        <div class="stat"><span class="num">92</span><span class="lbl">مشترك</span></div>
        <div class="stat"><span class="num">87</span><span class="lbl">حلقة</span></div>
        <div class="stat"><span class="num">18512</span><span class="lbl">المشاهدات</span></div>
      </div>
    </section>

    <section id="stop-1">
      <p class="eyebrow">عن الرحلة</p>
      <div class="about-card">
        <p>مرحبًا بكم في رؤيـة أنس، القناة التي تأخذكم في رحلة عبر القصص والتاريخ والأفكار المتنوعة.</p>
        <p>هنا ستجدون حكايات من الماضي والحاضر، تحليلات، ومستجدات تثير الفضول، كل ذلك في محاولة لاكتشاف المعرفة بطريقة ممتعة وغامضة في نفس الوقت.</p>
      </div>
    </section>

    <section id="waypoints">
      <div class="section-head">
        <p class="eyebrow">محطات الرحلة</p>
        <h2>أربع طرق لاكتشاف المحتوى</h2>
      </div>
      <div class="waypoints">
        <div class="waypoint" id="stop-2">
          <div class="wp-icon">📜</div>
          <div class="wp-body"><h3>التاريخ</h3><p>حكايات من الماضي، أحداث وشخصيات شكّلت مسار الزمن.</p></div>
        </div>
        <div class="waypoint" id="stop-3">
          <div class="wp-icon">🌙</div>
          <div class="wp-body"><h3>القصص</h3><p>روايات وحكايات تأخذكم في رحلة بعيدًا عن الواقع، ولو للحظة.</p></div>
        </div>
        <div class="waypoint" id="stop-4">
          <div class="wp-icon">🧭</div>
          <div class="wp-body"><h3>التحليلات</h3><p>نظرة أعمق على أفكار وقضايا تستحق التوقف عندها.</p></div>
        </div>
        <div class="waypoint" id="stop-5">
          <div class="wp-icon">✦</div>
          <div class="wp-body"><h3>المستجدات</h3><p>ما يثير الفضول اليوم، بأسلوب مبسّط وممتع.</p></div>
        </div>
      </div>
    </section>

    <section id="stop-6">
      <div class="section-head">
        <p class="eyebrow">كلام المتابعين</p>
        <h2>شنو كيقولو</h2>
      </div>
      <div class="testi-row" id="testiRow"></div>
    </section>

    <section id="stop-7">
      <div class="newsletter">
        <h2>خبرني بالحلقة الجاية</h2>
        <p>سجل بريدك الإلكتروني، وتوصل بإشعار كل ما نزلت حلقة جديدة.</p>
        <form class="newsletter-form" id="newsletterForm">
          <input type="email" id="newsletterEmail" placeholder="بريدك الإلكتروني" required>
          <button class="btn-primary" type="submit">سجل</button>
        </form>
        <div class="newsletter-note" id="newsletterNote"></div>
      </div>
    </section>

    <section id="stop-8">
      <div class="section-head">
        <p class="eyebrow">تابع الرحلة</p>
        <h2>وين بغيتي تكمل؟</h2>
      </div>
      <div class="dest-grid">
        <div class="dest-card" data-page="episodes">
          <div class="dc-icon">▶</div>
          <h3>الحلقات</h3>
          <p>آخر الحلقات المنشورة على قناة يوتيوب.</p>
          <div class="dc-arrow">شاهد الحلقات ←</div>
        </div>
        <div class="dest-card" data-page="videos">
          <div class="dc-icon">🎬</div>
          <h3>فيديوهات</h3>
          <p>مقاطع خاصة بالموقع، غير متوفرة على يوتيوب.</p>
          <div class="dc-arrow">شاهد الفيديوهات ←</div>
        </div>
        <div class="dest-card" data-page="about">
          <div class="dc-icon"><img src="3.png" alt="Photo" style="width:35px;height:35px;border-radius:50%;object-fit:cover;"></div>
          <h3>من أنا</h3>
          <p>تعرف على قصة القناة ومن ورائها.</p>
          <div class="dc-arrow">اقرأ القصة ←</div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap">
      <div class="mark-big"><img src="3.png" alt="Photo" style="width:68px;height:68px;border-radius:50%;object-fit:cover;"></div>
      <h3>انضم إلى الرحلة</h3>
      <p class="fine" style="max-width:420px;margin:0 auto;">اشترك الآن لتصلك كل حلقة جديدة أول بأول.</p>
      <div class="social-row">
        <a href="https://www.youtube.com/channel/UCzPGTjQSHJmgtR3Mdohu_Yw" target="_blank" rel="noopener">يوتيوب</a>
        <a href="https://www.instagram.com/anass_vision_/" target="_blank" rel="noopener">انستغرام</a>
        
      </div>
      <p class="fine">© رؤيـة أنس — anass vision</p>
    </div>
  </footer>
</div>

<!-- ============ PAGE: EPISODES ============ -->
<div class="page" id="page-episodes">
  <main class="wrap">
    <div class="page-hero">
      <p class="eyebrow">من قناة يوتيوب</p>
      <h1>الحلقات</h1>
      <p>آخر الحلقات المنشورة على القناة، من تاريخ وقصص وتحليلات ومستجدات.</p>
    </div>
    <div class="route-divider"></div>

    <section>
      <div class="section-head" style="margin-bottom:26px;">
        <p class="eyebrow">الأكثر مشاهدة</p>
      </div>
      <div class="featured-strip" id="featuredStrip"></div>

      <div class="filter-bar">
        <input type="text" id="epSearch" placeholder="بحث فالحلقات...">
        <div class="chip-row" id="chipRow"></div>
      </div>

      <div class="ep-grid" id="epGrid"></div>
      <div class="ep-cta">
        <a class="btn-primary" href="https://www.youtube.com/channel/UCzPGTjQSHJmgtR3Mdohu_Yw/videos" target="_blank" rel="noopener">كل الحلقات على القناة</a>
      </div>
    </section>
  </main>
  <footer>
    <div class="wrap">
      <div class="mark-big"><img src="3.png" alt="Photo" style="width:68px;height:68px;border-radius:50%;object-fit:cover;"></div>
      <h3>انضم إلى الرحلة</h3>
      <p class="fine" style="max-width:420px;margin:0 auto;">اشترك الآن لتصلك كل حلقة جديدة أول بأول.</p>
      <div class="social-row">
        <a href="https://www.youtube.com/channel/UCzPGTjQSHJmgtR3Mdohu_Yw" target="_blank" rel="noopener">يوتيوب</a>
        <a href="https://www.instagram.com/anass_vision_/" target="_blank" rel="noopener">انستغرام</a>
        
      </div>
      <p class="fine">© رؤيـة أنس — anass vision</p>
    </div>
  </footer>
</div>

<!-- ============ PAGE: VIDEOS ============ -->
<div class="page" id="page-videos">
  <main class="wrap">
    <div class="page-hero">
      <p class="eyebrow">خاصة بالموقع</p>
      <h1>فيديوهات</h1>
      <p>مقاطع فيديو موجودة هنا فقط، ماشي على يوتيوب.</p>
    </div>
    <div class="route-divider"></div>
    <section>
      <div class="ep-grid" id="videoGrid"></div>
    </section>
  </main>
  <footer>
    <div class="wrap">
      <div class="mark-big"><img src="3.png" alt="Photo" style="width:68px;height:68px;border-radius:50%;object-fit:cover;"></div>
      <h3>انضم إلى الرحلة</h3>
      <p class="fine" style="max-width:420px;margin:0 auto;">اشترك الآن لتصلك كل حلقة جديدة أول بأول.</p>
      <div class="social-row">
        <a href="https://www.youtube.com/channel/UCzPGTjQSHJmgtR3Mdohu_Yw" target="_blank" rel="noopener">يوتيوب</a>
        <a href="https://www.instagram.com/anass_vision_/" target="_blank" rel="noopener">انستغرام</a>
        
      </div>
      <p class="fine">© رؤيـة أنس — anass vision</p>
    </div>
  </footer>
</div>

<!-- ============ PAGE: ABOUT ============ -->
<div class="page" id="page-about">
  <main class="wrap">
    <div class="about-hero">
      <div class="about-photo"><div class="inner"><img src="3.png" alt="Photo" style="width:168px;height:168px;border-radius:50%;object-fit:cover;"></div></div>
      <div class="about-text">
        <p class="eyebrow">من ورا الكاميرا</p>
        <h2>من أنا</h2>
        <p>سميتي أنس، وهاد الفضاء هو المكان اللي كنجمع فيه الحكايات اللي عجبتني والأفكار اللي فكرتني، ونشاركها معاكم بطريقتي.</p>
        <p>بدأت هاد الرحلة باش نكتشف ونتعلم بصوت عالي، وحاليا كل حلقة هي محطة جديدة فهاد الطريق الطويل.</p>
      </div>
    </div>

    <section style="padding-top:20px;">
      <div class="section-head">
        <p class="eyebrow">محطات الرحلة</p>
        <h2>كيفاش بدات القصة</h2>
      </div>
      <div class="about-timeline">
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-body"><h4>البداية</h4><p>فكرة "رؤيـة أنس" بدات كمساحة صغيرة لمشاركة القصص والأفكار.</p></div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-body"><h4>أول 87 حلقة</h4><p>من التاريخ للقصص للتحليلات، كل حلقة زادت شوية من التجربة.</p></div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-body"><h4>اليوم</h4><p>القناة كتكبر بمتابعين كيشاركو نفس الفضول، والرحلة مازالت طويلة.</p></div>
        </div>
      </div>
    </section>
  </main>
  <footer>
    <div class="wrap">
      <div class="mark-big"><img src="3.png" alt="Photo" style="width:68px;height:68px;border-radius:50%;object-fit:cover;"></div>
      <h3>انضم إلى الرحلة</h3>
      <p class="fine" style="max-width:420px;margin:0 auto;">اشترك الآن لتصلك كل حلقة جديدة أول بأول.</p>
      <div class="social-row">

        <a href="https://www.youtube.com/channel/UCzPGTjQSHJmgtR3Mdohu_Yw" target="_blank" rel="noopener">يوتيوب</a>
        <a href="https://www.instagram.com/anass_vision_/" target="_blank" rel="noopener">انستغرام</a>
        
      </div>
      <p class="fine">© رؤيـة أنس — anass vision</p>
    </div>
  </footer>
</div>

<script>
  /* ============================================================
     1) الحلقات ديال يوتيوب — زيد/بدل هنا فقط.
        id       : الجزء لي كاين فرابط يوتيوب من بعد "v="
        date     : تاريخ النشر (كيبان تحت العنوان)
        featured : true/false — إلا true كتبان فـ "الأكثر مشاهدة"
     ============================================================ */
  const episodes = [
    { id: "U7a6rKEExXI", title: "عنوان الحلقة الأولى", category: "تاريخ", date: "2026-06-01", featured: true },
    { id: "XXXXXXXXXXX", title: "عنوان الحلقة الثانية", category: "قصص", date: "2026-06-08", featured: true },
    { id: "XXXXXXXXXXX", title: "عنوان الحلقة الثالثة", category: "تحليل", date: "2026-06-15", featured: false },
    { id: "XXXXXXXXXXX", title: "عنوان الحلقة الرابعة", category: "مستجدات", date: "2026-06-22", featured: false },
  ];

  /* ============================================================
     2) فيديوهات خاصة بالموقع فقط (ماشي يوتيوب) — <video src="">
     ============================================================ */
  const siteVideos = [
    // { src: "videos/clip1.mp4", poster: "videos/clip1.jpg", title: "عنوان الفيديو", category: "حصري" },
    { src: "", poster: "2.jpg", title: "", category: "حصري" },
  ];

  /* ============================================================
     3) تعليقات/آراء المتابعين — زيد/بدل هنا.
     ============================================================ */
  const testimonials = [
    { name: "سارة", text: "حلقات ديال التاريخ عندها طريقة تحكي بيها كتخليك تحس بالقصة حقيقية.", initial: "س" },
    { name: "يوسف", text: "المحتوى بسيط ومفهوم، وفي نفس الوقت فيه عمق. كنتابع كل حلقة.", initial: "ي" },
    { name: "خديجة", text: "القناة لي كتخليني نكتشف أفكار جديدة كل جمعة. شكرا أنس!", initial: "خ" },
  ];

  /* ============================================================
     4) YouTube RSS — جلب الحلقات أوتوماتيك (اختياري)
        - كيخدم غير إذا كان عندك انترنت وقت فتح الصفحة
        - كيستعمل proxy مجاني (allorigins) باش يتخطى قيود CORS ديال يوتيوب
        - إلا فشل، كيبقى يخدم بالليستة اليدوية "episodes" لي فوق
        - بدل CHANNEL_ID بـ ID ديال القناة ديالك إلا تبدل
     ============================================================ */
  const AUTO_FETCH_FROM_YOUTUBE = true; // بدلها لـ true باش تجرب الجلب الأوتوماتيكي
  const CHANNEL_ID = "UCzPGTjQSHJmgtR3Mdohu_Yw";

  async function tryFetchYoutubeRSS(){
    if(!AUTO_FETCH_FROM_YOUTUBE) return null;
    try{
      const feedUrl = `https://www.youtube.com/feeds/videos.xml?channel_id=UCzPGTjQSHJmgtR3Mdohu_Yw`;
      const proxied = `https://api.allorigins.win/raw?url=${encodeURIComponent(feedUrl)}`;
      const res = await fetch(proxied);
      if(!res.ok) throw new Error('fetch failed');
      const text = await res.text();
      const xml = new window.DOMParser().parseFromString(text, "text/xml");
      const entries = Array.from(xml.querySelectorAll("entry")).slice(0, 8);
      if(!entries.length) throw new Error('no entries');
      return entries.map((e, i) => ({
        id: e.querySelector("videoId")?.textContent || "",
        title: e.querySelector("title")?.textContent || "حلقة جديدة",
        category: "جديد",
        date: (e.querySelector("published")?.textContent || "").slice(0,10),
        featured: i < 2
      }));
    }catch(err){
      console.warn("تعذر جلب الحلقات من يوتيوب، غادي نستعملو الليستة اليدوية.", err);
      return null;
    }
  }

  let activeEpisodes = episodes;
  let activeCategory = "الكل";
  let activeSearch = "";

  function formatDate(iso){
    if(!iso) return "";
    const d = new Date(iso);
    if(isNaN(d)) return iso;
    return d.toLocaleDateString('ar-MA', { year:'numeric', month:'long', day:'numeric' });
  }

  function shareUrls(v){
    const url = `https://www.youtube.com/watch?v=${v.id}`;
    const text = encodeURIComponent(v.title);
    return {
      whatsapp: `https://wa.me/?text=${text}%20${encodeURIComponent(url)}`,
      twitter: `https://twitter.com/intent/tweet?text=${text}&url=${encodeURIComponent(url)}`
    };
  }

  function renderChips(){
    const cats = ["الكل", ...new Set(activeEpisodes.map(e => e.category))];
    const row = document.getElementById('chipRow');
    row.innerHTML = cats.map(c => `<button class="chip ${c===activeCategory?'active':''}" data-cat="${c}">${c}</button>`).join('');
    row.querySelectorAll('.chip').forEach(btn => {
      btn.addEventListener('click', () => {
        activeCategory = btn.dataset.cat;
        renderChips();
        renderEpisodes();
      });
    });
  }

  function renderFeatured(){
    const strip = document.getElementById('featuredStrip');
    const featured = activeEpisodes.filter(e => e.featured);
    if(!featured.length){ strip.innerHTML = ''; strip.style.display='none'; return; }
    strip.style.display = 'grid';
    strip.innerHTML = featured.map(v => `
      <a class="featured-card" href="https://www.youtube.com/watch?v=${v.id}" target="_blank" rel="noopener">
        <img src="https://img.youtube.com/vi/${v.id}/hqdefault.jpg" alt="${v.title}">
        <div class="fc-body"><h4>${v.title}</h4><span>${v.category} · ${formatDate(v.date)}</span></div>
      </a>
    `).join('');
  }

  function renderEpisodes(){
    const grid = document.getElementById('epGrid');
    let list = activeEpisodes;
    if(activeCategory !== "الكل") list = list.filter(e => e.category === activeCategory);
    if(activeSearch.trim()) list = list.filter(e => e.title.includes(activeSearch.trim()));

    if(!list.length){
      grid.innerHTML = `<div class="empty-note">ماكاينش حلقات تطابق البحث/التصنيف.</div>`;
      return;
    }
    grid.innerHTML = list.map(v => {
      const s = shareUrls(v);
      return `
      <div class="ep-card">
        <a href="https://www.youtube.com/watch?v=${v.id}" target="_blank" rel="noopener">
          <div class="ep-thumb">
            <span class="ep-tag">${v.category}</span>
            <img src="https://img.youtube.com/vi/${v.id}/hqdefault.jpg" alt="${v.title}" loading="lazy">
            <div class="play">▶</div>
          </div>
          <div class="ep-info">
            <h4>${v.title}</h4>
          </div>
        </a>
        <div class="ep-info" style="padding-top:0;">
          <div class="ep-meta">
            <span>${formatDate(v.date)}</span>
            <div class="share-row">
              <a class="share-btn" href="${s.whatsapp}" target="_blank" rel="noopener" title="شارك فواتساب" onclick="event.stopPropagation()">📱</a>
              <a class="share-btn" href="${s.twitter}" target="_blank" rel="noopener" title="شارك فتويتر" onclick="event.stopPropagation()">🐦</a>
            </div>
          </div>
        </div>
      </div>`;
    }).join('');
  }

  function renderSiteVideos(){
    const grid = document.getElementById('videoGrid');
    if(!siteVideos.length){
      grid.innerHTML = `<div class="empty-note">مازال ماكاينة فيديوهات مزادة. زيدها فالليستة "siteVideos".</div>`;
      return;
    }
    grid.innerHTML = siteVideos.map(v => `
      <div class="ep-card video-card">
        <div class="ep-thumb" style="height:auto;">
          <span class="ep-tag">${v.category || ''}</span>
          <video src="${v.src}" ${v.poster ? `poster="${v.poster}"` : ''} controls preload="metadata"></video>
        </div>
        <div class="ep-info"><h4>${v.title}</h4></div>
      </div>
    `).join('');
  }

  function renderTestimonials(){
    const row = document.getElementById('testiRow');
    row.innerHTML = testimonials.map(t => `
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p>${t.text}</p>
        <div class="who"><div class="avatar">${t.initial}</div><span>${t.name}</span></div>
      </div>
    `).join('');
  }

  document.getElementById('epSearch').addEventListener('input', (e) => {
    activeSearch = e.target.value;
    renderEpisodes();
  });

  document.getElementById('newsletterForm').addEventListener('submit', (e) => {
    e.preventDefault();
    const email = document.getElementById('newsletterEmail').value;
    // ملاحظة: هادي واجهة فقط. باش الاشتراك يخدم بجد، خاصك تربطها بخدمة
    // بحال Mailchimp, EmailJS, ولا Google Form (بدل هاد الجزء بـ fetch/action ديال الخدمة).
    document.getElementById('newsletterNote').textContent = `تسجلتي بـ ${email} ✓ (رابط هاد الفورم بخدمة إيميل باش يخدم بجد)`;
    document.getElementById('newsletterForm').reset();
  });

  renderTestimonials();
  renderSiteVideos();

  (async function initEpisodes(){
    const fetched = await tryFetchYoutubeRSS();
    activeEpisodes = fetched && fetched.length ? fetched : episodes;
    renderChips();
    renderFeatured();
    renderEpisodes();
  })();

  /* ============================================================
     تبديل الصفحات (مع أنيميشن تحميل بسيط)
     ============================================================ */
  const navLinks = document.querySelectorAll('[data-page]');
  const pages = document.querySelectorAll('.page');
  const transitionEl = document.getElementById('pageTransition');

  function goToPage(name){
    transitionEl.classList.add('show');
    setTimeout(() => {
      pages.forEach(p => p.classList.toggle('active', p.id === 'page-' + name));
      document.querySelectorAll('.nav-links a').forEach(a => a.classList.toggle('active', a.dataset.page === name));
      window.scrollTo(0, 0);
      if(name === 'home'){ requestAnimationFrame(() => { buildPath(); updatePlane(); }); }
      requestAnimationFrame(() => transitionEl.classList.remove('show'));
    }, 220);
  }
  navLinks.forEach(el => {
    el.addEventListener('click', (e) => {
      e.preventDefault();
      goToPage(el.dataset.page);
    });
  });

  /* ============================================================
     Dark / Light toggle
     ============================================================ */
  const themeToggle = document.getElementById('themeToggle');
  function applyTheme(theme){
    document.documentElement.setAttribute('data-theme', theme);
    themeToggle.textContent = theme === 'light' ? '☀️' : '🌙';
    try{ localStorage.setItem('av-theme', theme); }catch(e){}
  }
  let savedTheme = 'dark';
  try{ savedTheme = localStorage.getItem('av-theme') || 'dark'; }catch(e){}
  applyTheme(savedTheme);
  themeToggle.addEventListener('click', () => {
    const current = document.documentElement.getAttribute('data-theme');
    applyTheme(current === 'light' ? 'dark' : 'light');
  });

  /* ============================================================
     المسار المنقط + الطيارة (الصفحة الرئيسية)
     ============================================================ */
  const svg = document.querySelector('#pathLayer svg');
  const line = document.getElementById('routeLine');
  const glow = document.getElementById('routeLineGlow');
  const plane = document.getElementById('plane');
  const stops = ['stop-0','stop-1','stop-2','stop-3','stop-4','stop-5','stop-6','stop-7','stop-8']
    .map(id => document.getElementById(id)).filter(Boolean);

  let pathEl = null;

  function buildPath(){
    const homePage = document.getElementById('page-home');
    const docHeight = homePage.scrollHeight;
    const width = window.innerWidth;
    svg.setAttribute('viewBox', `0 0 ${width} ${docHeight}`);

    const pathPoints = stops.map((el, i) => {
      const rect = el.getBoundingClientRect();
      const y = rect.top + window.scrollY + rect.height/2;
      const side = i % 2 === 0 ? width * 0.08 : width * 0.92;
      return { x: side, y };
    });
    if(pathPoints.length < 2) return;

    let d = `M ${pathPoints[0].x} ${pathPoints[0].y}`;
    for(let i = 1; i < pathPoints.length; i++){
      const prev = pathPoints[i-1];
      const curr = pathPoints[i];
      const midY = (prev.y + curr.y) / 2;
      d += ` C ${prev.x} ${midY}, ${curr.x} ${midY}, ${curr.x} ${curr.y}`;
    }
    line.setAttribute('d', d);
    glow.setAttribute('d', d);
    pathEl = document.createElementNS('http://www.w3.org/2000/svg','path');
    pathEl.setAttribute('d', d);
  }

  function updatePlane(){
    if(!pathEl || !document.getElementById('page-home').classList.contains('active')) return;
    const total = pathEl.getTotalLength();
    const scrollTop = window.scrollY;
    const docHeight = document.getElementById('page-home').scrollHeight - window.innerHeight;
    const frac = Math.min(Math.max(scrollTop / Math.max(docHeight,1), 0), 1);
    const point = pathEl.getPointAtLength(frac * total);
    const point2 = pathEl.getPointAtLength(Math.min(frac * total + 1, total));
    const angle = Math.atan2(point2.y - point.y, point2.x - point.x) * 180 / Math.PI;
    plane.setAttribute('transform', `translate(${point.x}, ${point.y}) rotate(${angle})`);
  }

  /* ===== Parallax on hero forest image ===== */
  const parallaxImg = document.getElementById('parallaxImg');
  function updateParallax(){
    if(!parallaxImg) return;
    const rect = parallaxImg.parentElement.getBoundingClientRect();
    const offset = rect.top * 0.25;
    parallaxImg.style.transform = `translateY(calc(-50% + ${offset}px))`;
  }

  window.addEventListener('load', () => { buildPath(); updatePlane(); updateParallax(); });
  window.addEventListener('resize', () => { buildPath(); updatePlane(); });
  window.addEventListener('scroll', () => { updatePlane(); updateParallax(); });
</script>

</body>
</html>
