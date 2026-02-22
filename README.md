
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="진고 JINGO - 24시간 무료상담 무료출장. 누수탐지, 배관공사, 방수공사 전문. 010-9279-5589">
<title>JINGO 진고 - 진짜고수 생활전문서비스</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700;900&family=Black+Han+Sans&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0b1120;
    --navy-light: #141d30;
    --navy-lighter: #1e2a42;
    --gold: #e8a020;
    --gold-light: #f5c052;
    --gold-dim: rgba(232,160,32,0.15);
    --white: #ffffff;
    --gray: #8a9bbf;
    --gray-light: #c5cedf;
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--navy);
    color: var(--white);
    font-family: 'Noto Sans KR', sans-serif;
    -webkit-font-smoothing: antialiased;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 16px 20px;
    background: rgba(11,17,32,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(232,160,32,0.12);
  }
  .nav-logo {
    font-family: 'Black Han Sans', sans-serif;
    font-size: 22px;
    color: var(--gold);
    letter-spacing: 2px;
  }
  .nav-logo span { color: var(--white); font-size: 12px; font-family: 'Noto Sans KR', sans-serif; font-weight: 300; letter-spacing: 4px; display: block; margin-top: -4px; }
  .nav-call {
    display: flex; align-items: center; gap: 8px;
    background: var(--gold); color: var(--navy);
    padding: 9px 16px; border-radius: 50px;
    font-weight: 700; font-size: 13px;
    text-decoration: none;
    transition: background 0.2s;
  }
  .nav-call:active { background: var(--gold-light); }

  /* ── HERO ── */
  .hero {
    min-height: 100svh;
    display: flex; flex-direction: column; justify-content: flex-end;
    padding: 0 20px 60px;
    position: relative;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 50% 0%, rgba(232,160,32,0.08) 0%, transparent 70%),
      radial-gradient(ellipse 100% 80% at 80% 100%, rgba(14,30,60,0.9) 0%, transparent 60%),
      linear-gradient(160deg, #0b1120 0%, #0e1e3c 50%, #0b1120 100%);
  }
  .hero-grid {
    position: absolute; inset: 0; opacity: 0.04;
    background-image: linear-gradient(var(--gold) 1px, transparent 1px), linear-gradient(90deg, var(--gold) 1px, transparent 1px);
    background-size: 40px 40px;
  }
  .hero-badge {
    position: relative;
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--gold-dim); border: 1px solid rgba(232,160,32,0.3);
    padding: 6px 14px; border-radius: 50px;
    font-size: 12px; font-weight: 500; color: var(--gold-light);
    margin-bottom: 20px;
    width: fit-content;
  }
  .badge-dot {
    width: 7px; height: 7px; border-radius: 50%;
    background: var(--gold);
    animation: pulse-dot 1.5s infinite;
  }
  @keyframes pulse-dot {
    0%,100% { opacity:1; transform:scale(1); }
    50% { opacity:0.4; transform:scale(1.5); }
  }
  .hero-title {
    position: relative;
    font-family: 'Black Han Sans', sans-serif;
    font-size: clamp(38px, 10vw, 56px);
    line-height: 1.15;
    margin-bottom: 16px;
  }
  .hero-title .gold { color: var(--gold); }
  .hero-sub {
    position: relative;
    font-size: 15px; color: var(--gray-light);
    line-height: 1.7; margin-bottom: 32px;
    font-weight: 300;
  }
  .hero-cta {
    position: relative;
    display: flex; flex-direction: column; gap: 12px;
  }
  .btn-primary {
    display: flex; align-items: center; justify-content: center; gap: 10px;
    background: var(--gold); color: var(--navy);
    padding: 18px; border-radius: 14px;
    font-weight: 700; font-size: 17px;
    text-decoration: none;
    transition: transform 0.15s, background 0.2s;
  }
  .btn-primary:active { transform: scale(0.97); background: var(--gold-light); }
  .btn-secondary {
    display: flex; align-items: center; justify-content: center; gap: 10px;
    background: transparent; color: var(--white);
    padding: 16px; border-radius: 14px;
    font-weight: 500; font-size: 15px;
    text-decoration: none; border: 1px solid rgba(255,255,255,0.15);
    transition: background 0.2s;
  }
  .btn-secondary:active { background: rgba(255,255,255,0.05); }
  .hero-stats {
    position: relative;
    display: grid; grid-template-columns: repeat(3,1fr);
    gap: 1px; background: rgba(255,255,255,0.06);
    border-radius: 16px; overflow: hidden;
    margin-top: 32px;
  }
  .stat-item {
    background: var(--navy-light);
    padding: 16px 12px; text-align: center;
  }
  .stat-num {
    font-family: 'Black Han Sans', sans-serif;
    font-size: 22px; color: var(--gold);
    display: block;
  }
  .stat-label { font-size: 11px; color: var(--gray); margin-top: 3px; }

  /* ── SCROLL INDICATOR ── */
  .scroll-ind {
    position: absolute; bottom: 24px; left: 50%;
    transform: translateX(-50%);
    display: flex; flex-direction: column; align-items: center; gap: 6px;
    color: var(--gray); font-size: 10px; letter-spacing: 3px;
    animation: bounce-ind 2s infinite;
  }
  .scroll-ind svg { opacity: 0.5; }
  @keyframes bounce-ind {
    0%,100% { transform: translateX(-50%) translateY(0); }
    50% { transform: translateX(-50%) translateY(6px); }
  }

  /* ── SECTION COMMON ── */
  section { padding: 72px 20px; }
  .section-tag {
    display: inline-block;
    font-size: 11px; letter-spacing: 4px; text-transform: uppercase;
    color: var(--gold); font-weight: 700;
    margin-bottom: 12px;
  }
  .section-title {
    font-family: 'Black Han Sans', sans-serif;
    font-size: clamp(26px, 7vw, 36px);
    line-height: 1.3; margin-bottom: 10px;
  }
  .section-desc { font-size: 14px; color: var(--gray); line-height: 1.8; margin-bottom: 40px; }

  /* ── WHY ── */
  .why { background: var(--navy-light); }
  .why-grid { display: flex; flex-direction: column; gap: 16px; }
  .why-card {
    background: var(--navy);
    border: 1px solid rgba(232,160,32,0.1);
    border-radius: 16px; padding: 22px;
    display: flex; align-items: flex-start; gap: 16px;
    transition: border-color 0.2s;
  }
  .why-card:active { border-color: rgba(232,160,32,0.4); }
  .why-icon {
    width: 44px; height: 44px; flex-shrink: 0;
    background: var(--gold-dim); border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 20px;
  }
  .why-card h3 { font-size: 15px; font-weight: 700; margin-bottom: 6px; }
  .why-card p { font-size: 13px; color: var(--gray); line-height: 1.7; }

  /* ── SERVICES ── */
  .services-grid {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 12px;
  }
  .service-item {
    background: var(--navy-lighter);
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 14px; padding: 18px 12px;
    text-align: center;
    transition: border-color 0.2s, background 0.2s;
  }
  .service-item:active { background: var(--navy-light); border-color: rgba(232,160,32,0.3); }
  .service-item .icon { font-size: 26px; margin-bottom: 8px; display: block; }
  .service-item span { font-size: 12px; color: var(--gray-light); font-weight: 500; line-height: 1.4; display: block; }

  /* ── BEFORE/AFTER ── */
  .ba-section { background: var(--navy-light); }
  .ba-cards { display: flex; flex-direction: column; gap: 24px; }
  .ba-card { border-radius: 20px; overflow: hidden; border: 1px solid rgba(255,255,255,0.06); }
  .ba-slider-wrap {
    position: relative; height: 220px; overflow: hidden;
    user-select: none; cursor: ew-resize;
  }
  .ba-after, .ba-before {
    position: absolute; inset: 0;
    background-size: cover; background-position: center;
  }
  .ba-before {
    background: linear-gradient(135deg, #1a2540 0%, #0d1625 100%);
    display: flex; align-items: center; justify-content: center;
    font-size: 13px; color: var(--gray);
  }
  .ba-after {
    background: linear-gradient(135deg, #1e3a2f 0%, #0d2018 100%);
    display: flex; align-items: center; justify-content: center;
    font-size: 13px; color: #5abf7a;
  }
  .ba-divider {
    position: absolute; top: 0; bottom: 0;
    width: 3px; background: var(--gold);
    transform: translateX(-50%);
    z-index: 2;
  }
  .ba-handle {
    position: absolute; top: 50%; left: 0;
    transform: translate(-50%, -50%);
    width: 36px; height: 36px;
    background: var(--gold); border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 4px 16px rgba(232,160,32,0.5);
    z-index: 3;
  }
  .ba-after-mask {
    position: absolute; top: 0; bottom: 0; right: 0;
    overflow: hidden;
  }
  .ba-after-inner {
    position: absolute; inset: 0;
  }
  .ba-label {
    position: absolute; top: 12px; padding: 4px 10px;
    font-size: 11px; font-weight: 700; border-radius: 50px;
    letter-spacing: 2px;
  }
  .ba-label.before { left: 12px; background: rgba(0,0,0,0.5); color: #aaa; }
  .ba-label.after { right: 12px; background: rgba(90,191,122,0.2); color: #5abf7a; }
  .ba-info { padding: 16px; background: var(--navy); }
  .ba-info h4 { font-size: 14px; font-weight: 700; margin-bottom: 4px; }
  .ba-info p { font-size: 12px; color: var(--gray); }
  .ba-solved {
    display: inline-block; margin-top: 8px;
    font-size: 11px; font-weight: 700; color: #5abf7a;
    background: rgba(90,191,122,0.1); padding: 3px 10px; border-radius: 50px;
  }

  /* ── EXPERTS ── */
  .experts-scroll {
    display: flex; gap: 14px;
    overflow-x: auto; padding-bottom: 8px;
    -ms-overflow-style: none; scrollbar-width: none;
  }
  .experts-scroll::-webkit-scrollbar { display: none; }
  .expert-card {
    flex-shrink: 0; width: 160px;
    background: var(--navy-lighter);
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 18px; padding: 20px 16px;
    text-align: center;
  }
  .expert-avatar {
    width: 64px; height: 64px; border-radius: 50%;
    background: var(--navy-light); margin: 0 auto 12px;
    border: 2px solid var(--gold);
    display: flex; align-items: center; justify-content: center;
    font-size: 26px;
  }
  .expert-card h4 { font-size: 14px; font-weight: 700; margin-bottom: 4px; }
  .expert-spec {
    font-size: 11px; color: var(--gold); margin-bottom: 4px;
    font-weight: 500;
  }
  .expert-career { font-size: 11px; color: var(--gray); margin-bottom: 8px; }
  .expert-rating {
    font-size: 13px; font-weight: 700; color: var(--gold-light);
    display: flex; align-items: center; justify-content: center; gap: 4px;
  }
  .expert-qual {
    font-size: 10px; color: var(--gray); margin-top: 4px; line-height: 1.4;
  }

  /* ── REVIEWS ── */
  .reviews { background: var(--navy-light); }
  .reviews-list { display: flex; flex-direction: column; gap: 14px; }
  .review-card {
    background: var(--navy);
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 16px; padding: 20px;
  }
  .review-top { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; }
  .review-avatar {
    width: 42px; height: 42px; border-radius: 50%;
    background: var(--gold-dim); border: 1px solid rgba(232,160,32,0.3);
    display: flex; align-items: center; justify-content: center;
    font-size: 16px; font-weight: 700; color: var(--gold);
    flex-shrink: 0;
  }
  .review-name { font-size: 14px; font-weight: 700; }
  .review-meta { font-size: 11px; color: var(--gray); margin-top: 2px; }
  .review-badge {
    margin-left: auto; font-size: 10px; font-weight: 700;
    background: rgba(90,191,122,0.12); color: #5abf7a;
    padding: 3px 10px; border-radius: 50px; white-space: nowrap;
  }
  .review-text { font-size: 14px; color: var(--gray-light); line-height: 1.75; }
  .review-stars { color: var(--gold); font-size: 12px; margin-top: 10px; }

  /* ── CTA ── */
  .cta-section {
    background: linear-gradient(160deg, #0e1e3c 0%, #0b1120 100%);
    border-top: 1px solid rgba(232,160,32,0.12);
    text-align: center; padding: 64px 20px;
    position: relative; overflow: hidden;
  }
  .cta-glow {
    position: absolute; top: -80px; left: 50%;
    transform: translateX(-50%);
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(232,160,32,0.12) 0%, transparent 70%);
  }
  .cta-section h2 {
    font-family: 'Black Han Sans', sans-serif;
    font-size: 28px; margin-bottom: 12px; position: relative;
  }
  .cta-section p { font-size: 14px; color: var(--gray); line-height: 1.8; margin-bottom: 32px; position: relative; }
  .cta-phone {
    display: block; position: relative;
    font-family: 'Black Han Sans', sans-serif;
    font-size: 32px; color: var(--gold);
    text-decoration: none; margin-bottom: 24px;
    letter-spacing: 2px;
  }
  .cta-buttons { display: flex; flex-direction: column; gap: 12px; position: relative; }
  .btn-kakao {
    display: flex; align-items: center; justify-content: center; gap: 10px;
    background: #FEE500; color: #3A1D1D;
    padding: 18px; border-radius: 14px;
    font-weight: 700; font-size: 16px;
    text-decoration: none;
  }
  .cta-free-badge {
    display: flex; gap: 10px; justify-content: center; margin-bottom: 28px;
    flex-wrap: wrap;
  }
  .free-tag {
    font-size: 12px; font-weight: 700;
    border: 1px solid rgba(232,160,32,0.3);
    color: var(--gold-light); padding: 5px 14px; border-radius: 50px;
    background: var(--gold-dim);
  }

  /* ── FOOTER ── */
  footer {
    background: #060c18;
    padding: 40px 20px 100px;
    border-top: 1px solid rgba(255,255,255,0.05);
  }
  .footer-logo {
    font-family: 'Black Han Sans', sans-serif;
    font-size: 20px; color: var(--gold);
    margin-bottom: 16px;
  }
  .footer-info { font-size: 12px; color: var(--gray); line-height: 2; }
  .footer-copy { font-size: 11px; color: rgba(255,255,255,0.2); margin-top: 20px; }

  /* ── FLOATING CTA ── */
  .floating-cta {
    position: fixed; bottom: 0; left: 0; right: 0;
    padding: 12px 16px 28px;
    background: linear-gradient(to top, rgba(11,17,32,1) 60%, transparent);
    z-index: 99;
  }
  .floating-inner {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 10px; max-width: 480px; margin: 0 auto;
  }
  .float-btn-call {
    display: flex; align-items: center; justify-content: center; gap: 8px;
    background: var(--gold); color: var(--navy);
    padding: 16px; border-radius: 14px;
    font-weight: 700; font-size: 15px;
    text-decoration: none;
  }
  .float-btn-kakao {
    display: flex; align-items: center; justify-content: center; gap: 8px;
    background: #FEE500; color: #3A1D1D;
    padding: 16px; border-radius: 14px;
    font-weight: 700; font-size: 15px;
    text-decoration: none;
  }

  /* ── ABOUT ── */
  .about-card {
    background: var(--navy-lighter);
    border: 1px solid rgba(232,160,32,0.15);
    border-radius: 20px; padding: 28px 22px;
    position: relative; overflow: hidden;
  }
  .about-quote {
    font-size: 12px; color: var(--gold);
    border-left: 3px solid var(--gold);
    padding-left: 14px; margin-bottom: 20px;
    line-height: 1.7; font-style: italic;
  }
  .about-text { font-size: 14px; color: var(--gray-light); line-height: 1.85; }
  .about-accent {
    position: absolute; top: -30px; right: -30px;
    width: 120px; height: 120px;
    background: radial-gradient(circle, rgba(232,160,32,0.08) 0%, transparent 70%);
  }

  /* ── FADE IN ANIMATION ── */
  .fade-up {
    opacity: 0; transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .fade-up.visible { opacity: 1; transform: translateY(0); }

  @media (min-width: 480px) {
    .services-grid { grid-template-columns: repeat(4,1fr); }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">JINGO<span>진 짜 고 수</span></div>
  <a href="tel:01092795589" class="nav-call">
    <svg width="14" height="14" fill="currentColor" viewBox="0 0 24 24"><path d="M6.6 10.8c1.4 2.8 3.8 5.1 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1-9.4 0-17-7.6-17-17 0-.6.4-1 1-1h3.5c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.3 0 .7-.2 1L6.6 10.8z"/></svg>
    무료상담
  </a>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-badge fade-up">
    <div class="badge-dot"></div>
    24시간 무료상담 · 무료출장
  </div>
  <h1 class="hero-title fade-up">
    실력으로 증명하고,<br>가격으로 <span class="gold">놀라게</span> 합니다.
  </h1>
  <p class="hero-sub fade-up">
    진짜고수는 해당 분야에서 검증된<br>최고의 닥터들이 직접 방문드립니다.<br>일반업체와 결과물의 차이를 경험하세요.
  </p>
  <div class="hero-cta fade-up">
    <a href="tel:01092795589" class="btn-primary">
      <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M6.6 10.8c1.4 2.8 3.8 5.1 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1-9.4 0-17-7.6-17-17 0-.6.4-1 1-1h3.5c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.3 0 .7-.2 1L6.6 10.8z"/></svg>
      지금 바로 상담하기
    </a>
    <a href="#services" class="btn-secondary">서비스 보기 →</a>
  </div>
  <div class="hero-stats fade-up">
    <div class="stat-item">
      <span class="stat-num">1위</span>
      <div class="stat-label">고객 만족도</div>
    </div>
    <div class="stat-item">
      <span class="stat-num">1년</span>
      <div class="stat-label">무상 A/S</div>
    </div>
    <div class="stat-item">
      <span class="stat-num">무료</span>
      <div class="stat-label">현장 출장</div>
    </div>
  </div>
  <div class="scroll-ind">
    SCROLL
    <svg width="16" height="16" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M19 9l-7 7-7-7"/></svg>
  </div>
</section>

<!-- WHY -->
<section class="why" id="why">
  <span class="section-tag fade-up">Why JINGO</span>
  <h2 class="section-title fade-up">진고를 선택해야<br>하는 이유</h2>
  <p class="section-desc fade-up">최선의 노력으로도 해결 안 됐다면,<br>이제 진짜 고수를 불러주세요.</p>
  <div class="why-grid">
    <div class="why-card fade-up">
      <div class="why-icon">🏆</div>
      <div>
        <h3>소비자 만족도 1위</h3>
        <p>높은 완성도로 검증된 결과. 일반 업체와 다른 차원의 퀄리티를 경험하세요.</p>
      </div>
    </div>
    <div class="why-card fade-up">
      <div class="why-icon">🚗</div>
      <div>
        <h3>100% 현장 방문 상담</h3>
        <p>전화가 아닌 직접 방문 후 정확한 진단 &amp; 시공 진행</p>
      </div>
    </div>
    <div class="why-card fade-up">
      <div class="why-icon">💰</div>
      <div>
        <h3>출장비 무료</h3>
        <p>현장 견적 후 협의. 숨겨진 비용 없이 투명하게</p>
      </div>
    </div>
    <div class="why-card fade-up">
      <div class="why-icon">✅</div>
      <div>
        <h3>합리적인 비용</h3>
        <p>높은 완성도 대비 합리적인 가격 보장</p>
      </div>
    </div>
    <div class="why-card fade-up">
      <div class="why-icon">🛡️</div>
      <div>
        <h3>A/S 1년 무상</h3>
        <p>시공 후 1년간 무상 A/S로 마음 편하게</p>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <span class="section-tag fade-up">Categories</span>
  <h2 class="section-title fade-up">서비스 카테고리</h2>
  <p class="section-desc fade-up">생활 속 모든 문제, 진고 전문가가 해결합니다.</p>
  <div class="services-grid">
    <div class="service-item fade-up"><span class="icon">🔍</span><span>누수탐지</span></div>
    <div class="service-item fade-up"><span class="icon">🔎</span><span>점검</span></div>
    <div class="service-item fade-up"><span class="icon">🚰</span><span>배관막힘</span></div>
    <div class="service-item fade-up"><span class="icon">🔧</span><span>각종부품교체</span></div>
    <div class="service-item fade-up"><span class="icon">🛠️</span><span>배관공사 &amp; 교체</span></div>
    <div class="service-item fade-up"><span class="icon">📷</span><span>내시경검수</span></div>
    <div class="service-item fade-up"><span class="icon">💨</span><span>악취제거</span></div>
    <div class="service-item fade-up"><span class="icon">🏗️</span><span>준설공사</span></div>
    <div class="service-item fade-up"><span class="icon">❄️</span><span>해빙</span></div>
    <div class="service-item fade-up"><span class="icon">🏠</span><span>방수공사</span></div>
  </div>
</section>

<!-- ABOUT -->
<section class="why">
  <span class="section-tag fade-up">About JINGO</span>
  <h2 class="section-title fade-up">편리미엄<br>생활전문서비스</h2>
  <div class="about-card fade-up">
    <div class="about-accent"></div>
    <div class="about-quote">"한 분야의 최고 경지에 도달한 사람,<br>그것이 진짜고수입니다."</div>
    <p class="about-text">
      진고는 <strong style="color:var(--gold)">진짜고수</strong>의 줄임말입니다.<br><br>
      지나치게 많은 광고나 저가 경쟁보다는 근본적인 원인 해결로 고객님의 소중한 시간과 노력을 아껴드립니다.<br><br>
      많은 시행착오를 거쳐 최고의 경지에 도달한 전문가들이 직접 방문합니다.
    </p>
  </div>
</section>

<!-- BEFORE/AFTER -->
<section class="ba-section">
  <span class="section-tag fade-up">Before &amp; After</span>
  <h2 class="section-title fade-up">시공 전·후<br>결과를 보여드립니다</h2>
  <p class="section-desc fade-up">진고의 완성도, 사진으로 직접 확인하세요.</p>
  <div class="ba-cards">
    <div class="ba-card fade-up">
      <div class="ba-slider-wrap" data-slider>
        <div class="ba-before">
          <div style="text-align:center">
            <div style="font-size:32px;margin-bottom:8px">🚿</div>
            <div>시공 전</div>
            <div style="font-size:11px;margin-top:4px;opacity:0.6">노후 배관 문제</div>
          </div>
        </div>
        <div class="ba-after-mask" style="left:50%">
          <div class="ba-after-inner">
            <div class="ba-after" style="left:calc(-100% + var(--mask-left, 50%));">
              <div style="text-align:center">
                <div style="font-size:32px;margin-bottom:8px">✨</div>
                <div>시공 완료</div>
                <div style="font-size:11px;margin-top:4px">완벽 해결</div>
              </div>
            </div>
          </div>
        </div>
        <div class="ba-divider" style="left:50%"></div>
        <div class="ba-handle" style="left:50%">
          <svg width="16" height="16" fill="none" stroke="#0b1120" stroke-width="2.5" viewBox="0 0 24 24"><path d="M9 18l-6-6 6-6M15 6l6 6-6 6"/></svg>
        </div>
        <div class="ba-label before">BEFORE</div>
        <div class="ba-label after">AFTER</div>
      </div>
      <div class="ba-info">
        <h4>욕실 배관 교체 시공</h4>
        <p>경기 용인 · 2024.11</p>
        <span class="ba-solved">✅ 완벽 해결</span>
      </div>
    </div>
    <div class="ba-card fade-up">
      <div class="ba-slider-wrap" data-slider>
        <div class="ba-before">
          <div style="text-align:center">
            <div style="font-size:32px;margin-bottom:8px">🚰</div>
            <div>시공 전</div>
            <div style="font-size:11px;margin-top:4px;opacity:0.6">하수구 심각한 막힘</div>
          </div>
        </div>
        <div class="ba-after-mask" style="left:50%">
          <div class="ba-after-inner">
            <div class="ba-after" style="left:calc(-100% + var(--mask-left, 50%));">
              <div style="text-align:center">
                <div style="font-size:32px;margin-bottom:8px">💧</div>
                <div>시공 완료</div>
                <div style="font-size:11px;margin-top:4px">완벽 해결</div>
              </div>
            </div>
          </div>
        </div>
        <div class="ba-divider" style="left:50%"></div>
        <div class="ba-handle" style="left:50%">
          <svg width="16" height="16" fill="none" stroke="#0b1120" stroke-width="2.5" viewBox="0 0 24 24"><path d="M9 18l-6-6 6-6M15 6l6 6-6 6"/></svg>
        </div>
        <div class="ba-label before">BEFORE</div>
        <div class="ba-label after">AFTER</div>
      </div>
      <div class="ba-info">
        <h4>주방 하수구 막힘 해결</h4>
        <p>경기 수원 · 2024.12</p>
        <span class="ba-solved">✅ 완벽 해결</span>
      </div>
    </div>
    <div class="ba-card fade-up">
      <div class="ba-slider-wrap" data-slider>
        <div class="ba-before">
          <div style="text-align:center">
            <div style="font-size:32px;margin-bottom:8px">🏚️</div>
            <div>시공 전</div>
            <div style="font-size:11px;margin-top:4px;opacity:0.6">옥상 방수 노후화</div>
          </div>
        </div>
        <div class="ba-after-mask" style="left:50%">
          <div class="ba-after-inner">
            <div class="ba-after" style="left:calc(-100% + var(--mask-left, 50%));">
              <div style="text-align:center">
                <div style="font-size:32px;margin-bottom:8px">🏠</div>
                <div>시공 완료</div>
                <div style="font-size:11px;margin-top:4px">완벽 해결</div>
              </div>
            </div>
          </div>
        </div>
        <div class="ba-divider" style="left:50%"></div>
        <div class="ba-handle" style="left:50%">
          <svg width="16" height="16" fill="none" stroke="#0b1120" stroke-width="2.5" viewBox="0 0 24 24"><path d="M9 18l-6-6 6-6M15 6l6 6-6 6"/></svg>
        </div>
        <div class="ba-label before">BEFORE</div>
        <div class="ba-label after">AFTER</div>
      </div>
      <div class="ba-info">
        <h4>옥상 방수 전면 시공</h4>
        <p>서울 강남 · 2025.01</p>
        <span class="ba-solved">✅ 완벽 해결</span>
      </div>
    </div>
  </div>
</section>

<!-- EXPERTS -->
<section id="experts">
  <span class="section-tag fade-up">Our Experts</span>
  <h2 class="section-title fade-up">검증된 전문가들이<br>직접 방문합니다</h2>
  <p class="section-desc fade-up">화려한 광고 대신, 실력으로 증명하는 진짜 고수들</p>
  <div class="experts-scroll">
    <div class="expert-card">
      <div class="expert-avatar">👨‍🔧</div>
      <h4>김○○ 마스터</h4>
      <div class="expert-spec">누수탐지 전문</div>
      <div class="expert-career">경력 18년</div>
      <div class="expert-rating">⭐ 4.9</div>
      <div class="expert-qual">누수탐지 기사 1급</div>
    </div>
    <div class="expert-card">
      <div class="expert-avatar">👷</div>
      <h4>박○○ 마스터</h4>
      <div class="expert-spec">배관공사 전문</div>
      <div class="expert-career">경력 22년</div>
      <div class="expert-rating">⭐ 5.0</div>
      <div class="expert-qual">배관기능장 자격</div>
    </div>
    <div class="expert-card">
      <div class="expert-avatar">🧑‍🏭</div>
      <h4>이○○ 마스터</h4>
      <div class="expert-spec">방수공사 전문</div>
      <div class="expert-career">경력 15년</div>
      <div class="expert-rating">⭐ 4.8</div>
      <div class="expert-qual">방수기능사 자격</div>
    </div>
    <div class="expert-card">
      <div class="expert-avatar">👨‍🔬</div>
      <h4>최○○ 마스터</h4>
      <div class="expert-spec">악취·준설 전문</div>
      <div class="expert-career">경력 12년</div>
      <div class="expert-rating">⭐ 4.9</div>
      <div class="expert-qual">환경처리 전문가</div>
    </div>
  </div>
</section>

<!-- REVIEWS -->
<section class="reviews">
  <span class="section-tag fade-up">Real Reviews</span>
  <h2 class="section-title fade-up">실제 고객 후기</h2>
  <p class="section-desc fade-up">과장 없는 진짜 리뷰, 직접 읽어보세요.</p>
  <div class="reviews-list">
    <div class="review-card fade-up">
      <div class="review-top">
        <div class="review-avatar">김</div>
        <div>
          <div class="review-name">김*진 고객님</div>
          <div class="review-meta">용인 · 2025년 1월</div>
        </div>
        <span class="review-badge">시공 후</span>
      </div>
      <p class="review-text">다른 업체 3곳에서 못 찾은 누수를 바로 찾아냈어요. 깔끔하게 해결해주셔서 너무 감사합니다.</p>
      <div class="review-stars">★★★★★</div>
    </div>
    <div class="review-card fade-up">
      <div class="review-top">
        <div class="review-avatar">박</div>
        <div>
          <div class="review-name">박*현 고객님</div>
          <div class="review-meta">수원 · 2024년 12월</div>
        </div>
        <span class="review-badge">시공 후</span>
      </div>
      <p class="review-text">출장비도 없고 현장 견적 후 바로 진행. 가격도 합리적이고 결과물이 정말 깔끔했습니다!</p>
      <div class="review-stars">★★★★★</div>
    </div>
    <div class="review-card fade-up">
      <div class="review-top">
        <div class="review-avatar">이</div>
        <div>
          <div class="review-name">이*영 고객님</div>
          <div class="review-meta">성남 · 2024년 11월</div>
        </div>
        <span class="review-badge">시공 후</span>
      </div>
      <p class="review-text">악취가 몇 달째 해결 안 됐는데 진고 마스터님이 근본 원인까지 완벽히 잡아주셨어요. A/S도 믿을 수 있어요.</p>
      <div class="review-stars">★★★★★</div>
    </div>
    <div class="review-card fade-up">
      <div class="review-top">
        <div class="review-avatar">최</div>
        <div>
          <div class="review-name">최*호 고객님</div>
          <div class="review-meta">강남 · 2024년 10월</div>
        </div>
        <span class="review-badge">시공 후</span>
      </div>
      <p class="review-text">방수 공사 1년 지났는데 완벽합니다. 1년 무상 A/S 덕분에 걱정 없이 지내고 있어요. 강력 추천!</p>
      <div class="review-stars">★★★★★</div>
    </div>
  </div>
</section>

<!-- CTA -->
<section class="cta-section">
  <div class="cta-glow"></div>
  <span class="section-tag">지금 바로 상담하세요</span>
  <h2>24시간 언제든지<br>무료 출장 · 무료 상담</h2>
  <p>출장비 없이 현장 견적 후 진행합니다</p>
  <div class="cta-free-badge">
    <span class="free-tag">무료 출장</span>
    <span class="free-tag">무료 상담</span>
    <span class="free-tag">1년 A/S</span>
  </div>
  <a href="tel:01092795589" class="cta-phone">010-9279-5589</a>
  <div class="cta-buttons">
    <a href="tel:01092795589" class="btn-primary">
      <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M6.6 10.8c1.4 2.8 3.8 5.1 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1-9.4 0-17-7.6-17-17 0-.6.4-1 1-1h3.5c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.3 0 .7-.2 1L6.6 10.8z"/></svg>
      전화 상담하기
    </a>
    <a href="https://open.kakao.com/me/jingo" class="btn-kakao">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="#3A1D1D"><path d="M12 3C6.477 3 2 6.477 2 10.8c0 2.7 1.6 5.1 4 6.6-.15.5-.95 3.2-1 3.4 0 0-.02.2.1.26.12.07.27 0 .27 0 .35-.05 4.1-2.7 4.7-3.1.6.08 1.27.14 1.93.14 5.523 0 10-3.477 10-7.8S17.523 3 12 3z"/></svg>
      카카오톡 상담
    </a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">JINGO 진고</div>
  <div class="footer-info">
    상호: JINGO 진고<br>
    주소: 경기도 용인시 기흥구 죽전로10 6층 601호<br>
    전화: <a href="tel:01092795589" style="color:var(--gold);text-decoration:none">010-9279-5589</a><br>
    팩스: 031-229-2110<br>
    메일: <a href="mailto:titanstool628@gmail.com" style="color:var(--gray);text-decoration:none">titanstool628@gmail.com</a>
  </div>
  <div class="footer-copy">© 2025 JINGO 진고. All rights reserved.</div>
</footer>

<!-- FLOATING CTA -->
<div class="floating-cta">
  <div class="floating-inner">
    <a href="tel:01092795589" class="float-btn-call">
      <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M6.6 10.8c1.4 2.8 3.8 5.1 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1-9.4 0-17-7.6-17-17 0-.6.4-1 1-1h3.5c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.3 0 .7-.2 1L6.6 10.8z"/></svg>
      전화 상담
    </a>
    <a href="https://open.kakao.com/me/jingo" class="float-btn-kakao">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="#3A1D1D"><path d="M12 3C6.477 3 2 6.477 2 10.8c0 2.7 1.6 5.1 4 6.6-.15.5-.95 3.2-1 3.4 0 0-.02.2.1.26.12.07.27 0 .27 0 .35-.05 4.1-2.7 4.7-3.1.6.08 1.27.14 1.93.14 5.523 0 10-3.477 10-7.8S17.523 3 12 3z"/></svg>
      카카오톡
    </a>
  </div>
</div>

<script>
// ── FADE IN ON SCROLL ──
const fadeEls = document.querySelectorAll('.fade-up');
const observer = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      setTimeout(() => e.target.classList.add('visible'), i * 60);
      observer.unobserve(e.target);
    }
  });
}, { threshold: 0.12 });
fadeEls.forEach(el => observer.observe(el));

// Trigger hero elements immediately
document.querySelectorAll('.hero .fade-up').forEach((el, i) => {
  setTimeout(() => el.classList.add('visible'), 200 + i * 120);
});

// ── BEFORE/AFTER SLIDERS ──
document.querySelectorAll('[data-slider]').forEach(slider => {
  const divider = slider.querySelector('.ba-divider');
  const handle = slider.querySelector('.ba-handle');
  const mask = slider.querySelector('.ba-after-mask');
  const afterInner = slider.querySelector('.ba-after-inner');
  let dragging = false;

  function setPos(pct) {
    pct = Math.max(5, Math.min(95, pct));
    divider.style.left = pct + '%';
    handle.style.left = pct + '%';
    mask.style.left = pct + '%';
    mask.style.width = (100 - pct) + '%';
    afterInner.style.transform = `translateX(${-(pct)}%)`;
  }

  function getPos(e) {
    const rect = slider.getBoundingClientRect();
    const x = (e.touches ? e.touches[0].clientX : e.clientX) - rect.left;
    return (x / rect.width) * 100;
  }

  slider.addEventListener('mousedown', e => { dragging = true; setPos(getPos(e)); });
  slider.addEventListener('touchstart', e => { dragging = true; setPos(getPos(e)); }, { passive: true });
  window.addEventListener('mousemove', e => { if (dragging) setPos(getPos(e)); });
  window.addEventListener('touchmove', e => { if (dragging) setPos(getPos(e)); }, { passive: true });
  window.addEventListener('mouseup', () => dragging = false);
  window.addEventListener('touchend', () => dragging = false);

  // Init
  setPos(50);

  // Auto demo animation
  let animated = false;
  const sliderObs = new IntersectionObserver(entries => {
    if (entries[0].isIntersecting && !animated) {
      animated = true;
      let p = 50, dir = -1, step = 0;
      const demo = setInterval(() => {
        p += dir * 1.2;
        if (p <= 20) dir = 1;
        if (p >= 80) { dir = -1; step++; }
        if (step >= 1 && p >= 50) { setPos(50); clearInterval(demo); return; }
        setPos(p);
      }, 16);
    }
  }, { threshold: 0.5 });
  sliderObs.observe(slider);
});
</script>
</body>
</html>
