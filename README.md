<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="title" content="Candidature Directeur Commercial Serax">
<meta name="apple-mobile-web-app-title" content="TR Candidature">
<meta property="og:title" content="Candidature Directeur Commercial Serax">
<title>Vision Stratégique France — Terence Richard</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=Jost:wght@200;300;400;500&display=swap" rel="stylesheet">

<style>
/* ═══════════════════════════════════════════════════════════
   VARIABLES & RESET
═══════════════════════════════════════════════════════════ */
:root {
  --cream:      #f5f0e8;
  --cream-dark: #ede6d6;
  --cream-mid:  #f9f5ef;
  --sand:       #c9b99a;
  --sand-light: #e2d8c8;
  --ink:        #1a1714;
  --ink-soft:   #3a3530;
  --ink-muted:  #7a7268;
  --white:      #fdfaf6;
  --nav-h:      56px;
  --announce-h: 36px;
  --ease-out:   cubic-bezier(0.22, 1, 0.36, 1);
  --ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
}

*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  background: var(--cream-mid);
  color: var(--ink);
  font-family: 'Jost', sans-serif;
  font-weight: 300;
  letter-spacing: 0.02em;
  overflow-x: hidden;
}

/* ═══════════════════════════════════════════════════════════
   ANNOUNCE BAR
═══════════════════════════════════════════════════════════ */
.announce {
  height: var(--announce-h);
  background: var(--ink);
  color: var(--cream);
  display: flex; align-items: center; justify-content: center;
  font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
  font-weight: 400; gap: 14px;
  transition: height 0.4s var(--ease-out), opacity 0.4s;
  overflow: hidden;
}
.announce em { color: var(--sand); font-style: normal; }
.announce.hidden { height: 0; opacity: 0; }

/* ═══════════════════════════════════════════════════════════
   STICKY HEADER
═══════════════════════════════════════════════════════════ */
.header-wrap {
  position: sticky;
  top: 0;
  z-index: 900;
}

/* ─── TOP BAR ─── */
.topbar {
  height: 34px;
  background: var(--cream-mid);
  border-bottom: 1px solid var(--sand-light);
  display: flex; align-items: center; justify-content: flex-end;
  padding: 0 52px; gap: 28px;
  transition: height 0.3s var(--ease-out), opacity 0.3s, border-color 0.3s;
}
.topbar.compact { height: 0; opacity: 0; pointer-events: none; overflow: hidden; }
.topbar-link {
  font-family: 'Jost', sans-serif;
  font-size: 10px; letter-spacing: 0.18em; text-transform: uppercase;
  color: var(--ink-muted); text-decoration: none; font-weight: 400;
  display: flex; align-items: center; gap: 6px;
  transition: color 0.2s;
}
.topbar-link:hover { color: var(--ink); }
.topbar-link svg { width: 12px; height: 12px; stroke-width: 1.4; }
.topbar-langs {
  display: flex; align-items: center; gap: 0;
  font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase;
}
.topbar-langs span {
  color: var(--ink-muted); padding: 2px 7px; cursor: pointer;
  transition: color 0.2s; font-weight: 400;
}
.topbar-langs span.active, .topbar-langs span:hover { color: var(--ink); }
.topbar-langs .dot { color: var(--sand-light); font-size: 8px; display: flex; align-items: center; }

/* ─── NAVBAR ─── */
.navbar {
  height: var(--nav-h);
  background: rgba(249, 245, 239, 0.95);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border-bottom: 1px solid var(--sand-light);
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  padding: 0 52px;
  transition: background 0.3s, box-shadow 0.3s;
  position: relative;
}
.navbar.elevated {
  box-shadow: 0 4px 40px rgba(26,23,20,0.08);
}

.nav-left  { display: flex; align-items: center; gap: 0; }
.nav-right { display: flex; align-items: center; justify-content: flex-end; gap: 0; }

.logo {
  font-family: 'Cormorant Garamond', serif;
  font-size: 22px; font-weight: 500; letter-spacing: 0.36em; text-transform: uppercase;
  color: var(--ink); text-decoration: none;
  text-align: center;
  transition: letter-spacing 0.3s;
}
.logo:hover { letter-spacing: 0.42em; }

/* ─── NAV ITEMS ─── */
.nav-item {
  position: relative;
  height: var(--nav-h);
  display: flex; align-items: center;
}

.nav-btn {
  height: 100%;
  display: flex; align-items: center;
  padding: 0 16px;
  font-family: 'Jost', sans-serif;
  font-size: 10.5px; letter-spacing: 0.16em; text-transform: uppercase;
  color: var(--ink-muted); font-weight: 400;
  background: none; border: none; cursor: pointer;
  transition: color 0.22s;
  position: relative;
  white-space: nowrap;
  gap: 6px;
}
.nav-btn::after {
  content: '';
  position: absolute; bottom: 0; left: 16px; right: 16px;
  height: 1.5px; background: var(--ink);
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.32s var(--ease-out);
}
.nav-btn .chevron {
  width: 8px; height: 8px;
  display: inline-block;
  transition: transform 0.28s var(--ease-out);
  opacity: 0.5;
}
.nav-btn .chevron svg { width: 8px; height: 8px; }

.nav-item.open .nav-btn,
.nav-btn:hover { color: var(--ink); }
.nav-item.open .nav-btn::after,
.nav-btn:hover::after { transform: scaleX(1); }
.nav-item.open .nav-btn .chevron { transform: rotate(180deg); opacity: 0.8; }

/* Icon btns */
.icon-btn {
  width: 40px; height: var(--nav-h);
  display: flex; align-items: center; justify-content: center;
  color: var(--ink-muted); text-decoration: none;
  transition: color 0.2s;
  cursor: pointer;
}
.icon-btn:hover { color: var(--ink); }
.icon-btn svg { width: 17px; height: 17px; stroke-width: 1.4; }

/* Hamburger */
.hamburger {
  display: none;
  flex-direction: column; align-items: center; justify-content: center;
  gap: 5px; width: 40px; height: var(--nav-h);
  background: none; border: none; cursor: pointer; padding: 0;
}
.hamburger span {
  display: block; width: 22px; height: 1.5px;
  background: var(--ink);
  transition: transform 0.32s var(--ease-out), opacity 0.22s, width 0.22s;
  transform-origin: center;
}
.hamburger.open span:nth-child(1) { transform: translateY(6.5px) rotate(45deg); }
.hamburger.open span:nth-child(2) { opacity: 0; width: 14px; }
.hamburger.open span:nth-child(3) { transform: translateY(-6.5px) rotate(-45deg); }

/* ═══════════════════════════════════════════════════════════
   MEGA MENU
═══════════════════════════════════════════════════════════ */
.mega-layer {
  position: absolute;
  top: 100%;
  left: 0; right: 0;
  z-index: 890;
  pointer-events: none;
}

.mega-panel {
  background: var(--white);
  border-top: 1px solid var(--sand-light);
  border-bottom: 1px solid var(--sand-light);
  box-shadow: 0 24px 64px rgba(26, 23, 20, 0.1);
  opacity: 0;
  transform: translateY(-6px);
  visibility: hidden;
  pointer-events: none;
  transition:
    opacity 0.28s var(--ease-out),
    transform 0.28s var(--ease-out),
    visibility 0s 0.28s;
}
.mega-panel.open {
  opacity: 1;
  transform: translateY(0);
  visibility: visible;
  pointer-events: all;
  transition:
    opacity 0.28s var(--ease-out),
    transform 0.28s var(--ease-out),
    visibility 0s 0s;
}

.mega-inner {
  max-width: 1200px;
  margin: 0 auto;
  padding: 44px 52px 48px;
  display: grid;
  gap: 0;
}

.mega-col-title {
  font-size: 9.5px; letter-spacing: 0.24em; text-transform: uppercase;
  color: var(--sand); margin-bottom: 18px; padding-bottom: 12px;
  border-bottom: 1px solid var(--sand-light); font-weight: 400;
}
.mega-links { list-style: none; display: flex; flex-direction: column; gap: 10px; }
.mega-links a {
  font-size: 13px; letter-spacing: 0.04em; color: var(--ink-soft);
  text-decoration: none; font-weight: 300;
  display: flex; align-items: center; gap: 0;
  transition: color 0.2s, gap 0.22s var(--ease-out);
}
.mega-links a::before {
  content: '—';
  font-size: 9px; color: var(--sand); margin-right: 0;
  opacity: 0; width: 0; overflow: hidden;
  transition: opacity 0.2s, width 0.22s var(--ease-out), margin-right 0.22s;
}
.mega-links a:hover { color: var(--ink); }
.mega-links a:hover::before { opacity: 1; width: 14px; margin-right: 8px; }

.mega-see-all {
  display: inline-flex; align-items: center; gap: 8px;
  margin-top: 20px; font-size: 10px; letter-spacing: 0.2em;
  text-transform: uppercase; color: var(--ink-muted); text-decoration: none;
  font-weight: 400;
  transition: color 0.2s, gap 0.22s;
}
.mega-see-all::after { content: '→'; font-size: 11px; transition: transform 0.22s var(--ease-out); }
.mega-see-all:hover { color: var(--ink); }
.mega-see-all:hover::after { transform: translateX(4px); }

/* Backdrop */
.mega-backdrop {
  position: fixed; inset: 0;
  background: rgba(26, 23, 20, 0.15);
  backdrop-filter: blur(2px);
  -webkit-backdrop-filter: blur(2px);
  z-index: 880;
  opacity: 0; pointer-events: none;
  transition: opacity 0.28s var(--ease-out);
}
.mega-backdrop.open { opacity: 1; pointer-events: all; }

/* ═══════════════════════════════════════════════════════════
   MOBILE DRAWER
═══════════════════════════════════════════════════════════ */
.drawer-veil {
  position: fixed; inset: 0;
  background: rgba(26, 23, 20, 0.35);
  backdrop-filter: blur(3px);
  -webkit-backdrop-filter: blur(3px);
  z-index: 960;
  opacity: 0; pointer-events: none;
  transition: opacity 0.38s var(--ease-out);
}
.drawer-veil.open { opacity: 1; pointer-events: all; }

.drawer {
  position: fixed;
  top: 0; right: 0; bottom: 0;
  width: min(88vw, 360px);
  background: var(--white);
  z-index: 970;
  transform: translateX(102%);
  transition: transform 0.42s var(--ease-out);
  display: flex; flex-direction: column;
  box-shadow: -12px 0 60px rgba(26, 23, 20, 0.15);
  overflow: hidden;
}
.drawer.open { transform: translateX(0); }

.drawer-head {
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 24px;
  height: 56px;
  border-bottom: 1px solid var(--sand-light);
  flex-shrink: 0;
}
.drawer-logo {
  font-family: 'Cormorant Garamond', serif;
  font-size: 21px; font-weight: 500; letter-spacing: 0.32em; color: var(--ink);
}
.drawer-close-btn {
  width: 36px; height: 36px;
  display: flex; align-items: center; justify-content: center;
  background: none; border: none; cursor: pointer;
  color: var(--ink-muted); transition: color 0.2s, transform 0.22s;
}
.drawer-close-btn:hover { color: var(--ink); transform: rotate(90deg); }
.drawer-close-btn svg { width: 18px; height: 18px; stroke-width: 1.5; }

.drawer-body {
  flex: 1; overflow-y: auto;
  -webkit-overflow-scrolling: touch;
}
.drawer-body::-webkit-scrollbar { width: 3px; }
.drawer-body::-webkit-scrollbar-thumb { background: var(--sand-light); }

/* Drawer accordion */
.drawer-group { border-bottom: 1px solid var(--sand-light); }
.drawer-toggle {
  width: 100%; display: flex; align-items: center; justify-content: space-between;
  padding: 18px 24px;
  font-family: 'Jost', sans-serif;
  font-size: 10.5px; letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--ink-soft); font-weight: 400;
  background: none; border: none; cursor: pointer;
  transition: color 0.2s, background 0.2s;
}
.drawer-toggle:hover { color: var(--ink); background: var(--cream-mid); }
.drawer-toggle-icon {
  width: 16px; height: 16px; flex-shrink: 0;
  transition: transform 0.3s var(--ease-out);
}
.drawer-toggle-icon svg { width: 16px; height: 16px; stroke-width: 1.4; }
.drawer-toggle.expanded .drawer-toggle-icon { transform: rotate(180deg); }

.drawer-sub {
  max-height: 0; overflow: hidden;
  background: var(--cream-mid);
  transition: max-height 0.38s var(--ease-out);
}
.drawer-sub.open { max-height: 600px; }
.drawer-sub-cat {
  padding: 12px 24px 4px 36px;
  font-size: 9px; letter-spacing: 0.22em; text-transform: uppercase;
  color: var(--sand); font-weight: 400; margin-top: 4px;
}
.drawer-sub a {
  display: block; padding: 11px 24px 11px 36px;
  font-size: 13px; color: var(--ink-muted); text-decoration: none;
  font-weight: 300; letter-spacing: 0.03em;
  transition: color 0.2s, padding-left 0.22s var(--ease-out);
}
.drawer-sub a:hover { color: var(--ink); padding-left: 40px; }

.drawer-foot {
  padding: 20px 24px;
  border-top: 1px solid var(--sand-light);
  display: grid; grid-template-columns: 1fr 1fr; gap: 10px;
  flex-shrink: 0;
}
.drawer-foot-btn {
  text-align: center; padding: 12px;
  font-family: 'Jost', sans-serif;
  font-size: 10px; letter-spacing: 0.18em; text-transform: uppercase;
  text-decoration: none; font-weight: 400;
  border: 1px solid var(--sand-light); color: var(--ink-muted);
  transition: all 0.22s;
}
.drawer-foot-btn:hover { border-color: var(--ink); color: var(--ink); }
.drawer-foot-btn.primary {
  background: var(--ink); color: var(--cream); border-color: var(--ink);
}
.drawer-foot-btn.primary:hover { background: var(--ink-soft); }

/* ═══════════════════════════════════════════════════════════
   HERO
═══════════════════════════════════════════════════════════ */
.hero {
  min-height: 92vh;
  display: grid; grid-template-columns: 1fr 1fr;
}
.hero-visual {
  background: var(--cream-dark);
  position: relative; overflow: hidden;
}
.hero-pattern {
  position: absolute; inset: 0;
  background:
    repeating-linear-gradient(45deg, transparent, transparent 40px, rgba(201,185,154,.12) 40px, rgba(201,185,154,.12) 41px),
    repeating-linear-gradient(-45deg, transparent, transparent 40px, rgba(201,185,154,.08) 40px, rgba(201,185,154,.08) 41px);
}
.hero-mono {
  position: absolute; top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(160px, 22vw, 280px);
  font-weight: 300; color: rgba(201,185,154,.2);
  line-height: 1; user-select: none;
  animation: fadeIn 1.4s ease both;
}
.hero-side-text {
  position: absolute; bottom: 48px; left: 48px;
  writing-mode: vertical-lr; transform: rotate(180deg);
  font-size: 10px; letter-spacing: 0.26em; text-transform: uppercase;
  color: var(--ink-muted); font-weight: 400;
}
.hero-content {
  background: var(--white);
  display: flex; flex-direction: column; justify-content: center;
  padding: clamp(56px, 8vw, 96px) clamp(40px, 6vw, 72px);
  animation: slideUp 0.9s 0.2s both;
}
.hero-eyebrow {
  font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase;
  color: var(--sand); margin-bottom: 26px; font-weight: 400;
}
.hero-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(34px, 4.5vw, 60px);
  font-weight: 400; line-height: 1.08; color: var(--ink);
  margin-bottom: 14px;
}
.hero-title em { font-style: italic; font-weight: 300; color: var(--ink-soft); }
.hero-sub {
  font-family: 'Cormorant Garamond', serif;
  font-size: 18px; font-weight: 300; color: var(--ink-muted);
  letter-spacing: 0.08em; font-style: italic; margin-bottom: 32px;
}
.hero-rule { width: 48px; height: 1px; background: var(--sand); margin-bottom: 28px; }
.hero-intro {
  font-size: 14.5px; line-height: 1.88; color: var(--ink-soft);
  max-width: 420px; margin-bottom: 44px; font-weight: 300;
}
.hero-cta {
  display: inline-flex; align-items: center; gap: 14px;
  font-size: 10.5px; letter-spacing: 0.22em; text-transform: uppercase;
  color: var(--ink); text-decoration: none; font-weight: 400;
  width: fit-content;
  transition: gap 0.3s var(--ease-out);
}
.hero-cta-line {
  display: inline-block; width: 32px; height: 1px; background: var(--ink);
  transition: width 0.3s var(--ease-out);
}
.hero-cta:hover { gap: 20px; }
.hero-cta:hover .hero-cta-line { width: 52px; }

/* ═══════════════════════════════════════════════════════════
   SHARED SECTION STYLES
═══════════════════════════════════════════════════════════ */
.section { padding: clamp(64px, 8vw, 96px) 0; }
.si { max-width: 1200px; margin: 0 auto; padding: 0 clamp(20px, 4vw, 52px); }
.sh { margin-bottom: clamp(40px, 6vw, 60px); }
.s-tag {
  display: block; font-size: 10px; letter-spacing: 0.3em; text-transform: uppercase;
  color: var(--sand); margin-bottom: 14px; font-weight: 400;
}
.s-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(26px, 3.2vw, 42px);
  font-weight: 400; line-height: 1.1; color: var(--ink);
}
.s-title em { font-style: italic; font-weight: 300; }

/* ═══════════════════════════════════════════════════════════
   PROFIL
═══════════════════════════════════════════════════════════ */
.s-profil { background: var(--white); }
.profil-grid {
  display: grid; grid-template-columns: 1fr 2px 1fr;
  gap: 64px; align-items: start;
}
.profil-divider { background: var(--sand-light); }
.profil-text { font-size: 15px; line-height: 1.9; color: var(--ink-soft); font-weight: 300; }
.profil-text p + p { margin-top: 16px; }
.tags { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 32px; }
.tag {
  font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase;
  border: 1px solid var(--sand); color: var(--ink-muted);
  padding: 7px 15px; font-weight: 400;
  transition: border-color 0.2s, color 0.2s, transform 0.2s;
  cursor: default;
}
.tag:hover { border-color: var(--ink); color: var(--ink); transform: translateY(-1px); }
.stats-grid {
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 1px; background: var(--sand-light); border: 1px solid var(--sand-light);
}
.stat-card {
  background: var(--white); padding: 32px 26px;
  transition: background 0.22s, transform 0.22s;
  cursor: default;
}
.stat-card:hover { background: var(--cream-mid); transform: scale(1.01); }
.stat-n {
  font-family: 'Cormorant Garamond', serif;
  font-size: 50px; font-weight: 300; color: var(--ink);
  line-height: 1; margin-bottom: 8px;
}
.stat-n sup { font-size: 22px; }
.stat-l {
  font-size: 10px; letter-spacing: 0.18em; text-transform: uppercase;
  color: var(--ink-muted); line-height: 1.5; font-weight: 400;
}

/* ═══════════════════════════════════════════════════════════
   MARCHÉ
═══════════════════════════════════════════════════════════ */
.s-marche { background: var(--cream-mid); }
.marche-grid {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 1px; background: var(--sand-light); border: 1px solid var(--sand-light);
}
.m-card {
  background: var(--white);
  padding: clamp(28px, 4vw, 44px) clamp(22px, 3vw, 36px);
  position: relative; overflow: hidden;
  transition: background 0.26s;
  cursor: default;
}
.m-card::after {
  content: ''; position: absolute; top: 0; left: 0; right: 0;
  height: 2px; background: var(--sand);
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.36s var(--ease-out);
}
.m-card:hover { background: var(--cream-mid); }
.m-card:hover::after { transform: scaleX(1); }
.m-icon { width: 38px; height: 38px; color: var(--sand); margin-bottom: 22px; }
.m-icon svg { width: 100%; height: 100%; stroke-width: 1; }
.m-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 22px; font-weight: 400; color: var(--ink); margin-bottom: 12px;
}
.m-text { font-size: 13px; line-height: 1.8; color: var(--ink-muted); font-weight: 300; }
.m-list { list-style: none; margin-top: 14px; display: flex; flex-direction: column; gap: 7px; }
.m-list li {
  font-size: 12.5px; color: var(--ink-soft);
  padding-left: 14px; position: relative; font-weight: 300;
}
.m-list li::before { content: '—'; position: absolute; left: 0; color: var(--sand); font-size: 10px; }

/* ═══════════════════════════════════════════════════════════
   STRATÉGIE
═══════════════════════════════════════════════════════════ */
.s-strat { background: var(--ink); }
.s-strat .s-title { color: var(--cream); }
.axes-grid {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 1px; background: rgba(201,185,154,.2); border: 1px solid rgba(201,185,154,.2);
}
.axe-card {
  background: var(--ink);
  padding: clamp(36px, 5vw, 56px) clamp(26px, 3.5vw, 44px);
  position: relative; overflow: hidden;
  transition: background 0.26s;
  cursor: default;
}
.axe-card:hover { background: #222018; }
.axe-bg-n {
  font-family: 'Cormorant Garamond', serif;
  font-size: 88px; font-weight: 300;
  color: rgba(201,185,154,.1);
  position: absolute; top: 16px; right: 20px;
  line-height: 1; transition: color 0.3s;
}
.axe-card:hover .axe-bg-n { color: rgba(201,185,154,.18); }
.axe-tag {
  font-size: 10px; letter-spacing: 0.24em; text-transform: uppercase;
  color: var(--sand); margin-bottom: 16px; display: block; font-weight: 400;
}
.axe-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 23px; font-weight: 400; color: var(--cream);
  margin-bottom: 14px; line-height: 1.2;
}
.axe-text { font-size: 13px; line-height: 1.8; color: rgba(245,240,232,.58); font-weight: 300; }
.axe-list { list-style: none; margin-top: 18px; display: flex; flex-direction: column; gap: 8px; }
.axe-list li {
  font-size: 12.5px; color: rgba(245,240,232,.56);
  padding-left: 16px; position: relative; font-weight: 300;
}
.axe-list li::before {
  content: ''; position: absolute; left: 0; top: 9px;
  width: 6px; height: 1px; background: var(--sand);
}

/* ═══════════════════════════════════════════════════════════
   PLAN 90 JOURS
═══════════════════════════════════════════════════════════ */
.s-plan { background: var(--cream-mid); }
.plan-grid {
  display: grid; grid-template-columns: repeat(3, 1fr);
  position: relative;
}
.plan-grid::before {
  content: ''; position: absolute;
  top: 32px; left: calc(100% / 6); right: calc(100% / 6);
  height: 1px; background: var(--sand-light);
}
.plan-phase { padding: 0 28px 40px; text-align: center; }
.plan-dot {
  width: 64px; height: 64px; border-radius: 50%;
  border: 1px solid var(--sand-light); background: var(--white);
  display: flex; align-items: center; justify-content: center;
  margin: 0 auto 24px; position: relative; z-index: 1;
  font-family: 'Cormorant Garamond', serif;
  font-size: 20px; font-weight: 400; color: var(--sand);
  transition: background 0.3s, border-color 0.3s, color 0.3s, transform 0.3s;
}
.plan-phase:hover .plan-dot {
  background: var(--ink); border-color: var(--ink);
  color: var(--cream); transform: scale(1.06);
}
.plan-period {
  font-size: 10px; letter-spacing: 0.24em; text-transform: uppercase;
  color: var(--sand); margin-bottom: 10px; font-weight: 400;
}
.plan-ph-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: 21px; font-weight: 400; color: var(--ink); margin-bottom: 16px;
}
.plan-items { list-style: none; text-align: left; display: flex; flex-direction: column; gap: 9px; }
.plan-items li {
  font-size: 13px; color: var(--ink-soft);
  padding-left: 18px; position: relative;
  font-weight: 300; line-height: 1.6;
}
.plan-items li::before { content: '—'; position: absolute; left: 0; color: var(--sand); font-size: 10px; top: 2px; }

/* ═══════════════════════════════════════════════════════════
   VISION QUOTE
═══════════════════════════════════════════════════════════ */
.s-vision { background: var(--cream-dark); padding: clamp(72px, 10vw, 112px) 0; }
.vision-inner { max-width: 860px; margin: 0 auto; padding: 0 clamp(20px, 4vw, 52px); text-align: center; }
.vision-q {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(20px, 3.5vw, 40px);
  font-weight: 300; font-style: italic; line-height: 1.55;
  color: var(--ink); margin-bottom: 32px;
  position: relative; padding-top: 20px;
}
.vision-q::before {
  content: '\201C';
  font-size: 110px; color: rgba(201,185,154,.32);
  position: absolute; top: -16px; left: -8px;
  line-height: 1; font-family: 'Cormorant Garamond', serif;
}
.vision-rule { width: 40px; height: 1px; background: var(--sand); margin: 0 auto 18px; }
.vision-by { font-size: 11px; letter-spacing: 0.26em; text-transform: uppercase; color: var(--ink-muted); font-weight: 400; }

/* ═══════════════════════════════════════════════════════════
   LEADERSHIP
═══════════════════════════════════════════════════════════ */
.s-lead { background: var(--white); }
.lead-grid {
  display: grid; grid-template-columns: repeat(4, 1fr);
  gap: 1px; background: var(--sand-light); border: 1px solid var(--sand-light);
}
.lead-card {
  background: var(--white);
  padding: clamp(28px, 4vw, 40px) clamp(20px, 3vw, 30px);
  text-align: center;
  transition: background 0.22s, transform 0.22s;
  cursor: default;
}
.lead-card:hover { background: var(--cream-mid); transform: translateY(-2px); }
.lead-icon { width: 44px; height: 44px; margin: 0 auto 18px; color: var(--sand); }
.lead-icon svg { width: 100%; height: 100%; stroke-width: 1; }
.lead-name {
  font-family: 'Cormorant Garamond', serif;
  font-size: 19px; font-weight: 400; color: var(--ink); margin-bottom: 10px;
}
.lead-desc { font-size: 12.5px; line-height: 1.78; color: var(--ink-muted); font-weight: 300; }

/* ═══════════════════════════════════════════════════════════
   CONTACT
═══════════════════════════════════════════════════════════ */
.s-contact { background: var(--cream-dark); padding: clamp(64px, 9vw, 100px) 0; }
.contact-inner { max-width: 680px; margin: 0 auto; padding: 0 clamp(20px, 4vw, 52px); text-align: center; }
.contact-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(28px, 4vw, 40px); font-weight: 400; color: var(--ink); margin-bottom: 16px;
}
.contact-sub { font-size: 14.5px; color: var(--ink-muted); margin-bottom: 44px; line-height: 1.75; font-weight: 300; }
.contact-info { display: flex; justify-content: center; gap: 40px; flex-wrap: wrap; margin-bottom: 4px; }
.ci-label { font-size: 9.5px; letter-spacing: 0.24em; text-transform: uppercase; color: var(--sand); margin-bottom: 6px; font-weight: 400; }
.ci-val { font-size: 14px; color: var(--ink); font-weight: 300; }
.btn-cta {
  display: inline-block; margin-top: 36px;
  background: var(--ink); color: var(--cream);
  font-family: 'Jost', sans-serif;
  font-size: 10.5px; letter-spacing: 0.24em; text-transform: uppercase;
  padding: 16px 44px; text-decoration: none; font-weight: 400;
  transition: background 0.26s, letter-spacing 0.3s, transform 0.22s;
}
.btn-cta:hover { background: var(--ink-soft); letter-spacing: 0.3em; transform: translateY(-2px); }

/* ═══════════════════════════════════════════════════════════
   FOOTER
═══════════════════════════════════════════════════════════ */
footer {
  background: var(--ink);
  color: rgba(245,240,232,.55);
  padding: 60px clamp(20px, 4vw, 52px) 28px;
}
.footer-inner { max-width: 1200px; margin: 0 auto; }
.footer-grid {
  display: grid; grid-template-columns: 1.6fr 1fr 1fr 1fr;
  gap: 40px; padding-bottom: 40px;
  border-bottom: 1px solid rgba(201,185,154,.14); margin-bottom: 28px;
}
.footer-logo-text {
  font-family: 'Cormorant Garamond', serif;
  font-size: 21px; font-weight: 500; letter-spacing: 0.3em;
  color: var(--cream); display: block; margin-bottom: 14px;
}
.footer-tagline { font-size: 12px; line-height: 1.7; color: rgba(245,240,232,.4); font-weight: 300; max-width: 220px; }
.footer-col-head { font-size: 10px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--sand); margin-bottom: 16px; font-weight: 400; }
.footer-links { list-style: none; display: flex; flex-direction: column; gap: 10px; }
.footer-links a {
  font-size: 12.5px; color: rgba(245,240,232,.5);
  text-decoration: none; font-weight: 300;
  transition: color 0.2s, padding-left 0.22s;
  display: block;
}
.footer-links a:hover { color: var(--cream); padding-left: 4px; }
.footer-bottom {
  display: flex; justify-content: space-between; align-items: center;
  flex-wrap: wrap; gap: 8px;
}
.footer-copy { font-size: 10.5px; color: rgba(245,240,232,.28); letter-spacing: 0.1em; }
.footer-yr { font-family: 'Cormorant Garamond', serif; color: var(--sand); font-size: 13px; }

/* ═══════════════════════════════════════════════════════════
   SCROLL REVEAL
═══════════════════════════════════════════════════════════ */
.reveal {
  opacity: 0; transform: translateY(22px);
  transition: opacity 0.72s var(--ease-out), transform 0.72s var(--ease-out);
}
.reveal.visible { opacity: 1; transform: none; }

/* ═══════════════════════════════════════════════════════════
   ANIMATIONS
═══════════════════════════════════════════════════════════ */
@keyframes fadeIn  { from { opacity:0 } to { opacity:1 } }
@keyframes slideUp { from { opacity:0; transform:translateY(30px) } to { opacity:1; transform:none } }

/* ═══════════════════════════════════════════════════════════
   RESPONSIVE — TABLET ≤ 1024px
═══════════════════════════════════════════════════════════ */
@media (max-width: 1024px) {
  .topbar  { display: none; }
  .navbar  { padding: 0 24px; grid-template-columns: auto 1fr auto; }
  .nav-left, .nav-right { display: none; }
  .hamburger { display: flex; }
  .logo  { font-size: 20px; text-align: left; }

  .hero  { grid-template-columns: 1fr; min-height: auto; }
  .hero-visual { min-height: 280px; }
  .hero-mono { font-size: 180px; }
  .hero-side-text { display: none; }
  .hero-content { padding: 56px 40px; }

  .profil-grid { grid-template-columns: 1fr; gap: 40px; }
  .profil-divider { display: none; }

  .marche-grid { grid-template-columns: 1fr 1fr; }
  .marche-grid .m-card:last-child { grid-column: 1 / -1; }

  .axes-grid { grid-template-columns: 1fr; }
  .plan-grid { grid-template-columns: 1fr; }
  .plan-grid::before { display: none; }
  .plan-phase { padding: 0 0 32px; text-align: left; display: grid; grid-template-columns: 64px 1fr; gap: 0 20px; align-items: start; }
  .plan-dot { margin: 0; }
  .plan-period, .plan-ph-title, .plan-items { grid-column: 2; }

  .lead-grid { grid-template-columns: 1fr 1fr; }
  .footer-grid { grid-template-columns: 1fr 1fr; }
}

/* ═══════════════════════════════════════════════════════════
   RESPONSIVE — MOBILE ≤ 640px
═══════════════════════════════════════════════════════════ */
@media (max-width: 640px) {
  .navbar { padding: 0 16px; }
  .logo { font-size: 19px; letter-spacing: 0.26em; }
  .hero-visual { min-height: 200px; }
  .hero-mono { font-size: 120px; }
  .hero-content { padding: 40px 24px 52px; }
  .marche-grid { grid-template-columns: 1fr; }
  .marche-grid .m-card:last-child { grid-column: auto; }
  .lead-grid { grid-template-columns: 1fr; }
  .lead-card { text-align: left; display: flex; gap: 18px; align-items: flex-start; padding: 28px 24px; }
  .lead-icon { flex-shrink: 0; margin: 0; }
  .footer-grid { grid-template-columns: 1fr; gap: 28px; }
  .footer-bottom { flex-direction: column; text-align: center; }
  .stats-grid { grid-template-columns: 1fr 1fr; }
  .plan-phase { grid-template-columns: 48px 1fr; }
  .plan-dot { width: 48px; height: 48px; font-size: 17px; }
}

@media (max-width: 380px) {
  .stats-grid { grid-template-columns: 1fr; }
}
</style>
</head>
<body>

<!-- ── ANNOUNCE ────────────────────────────────── -->
<div class="announce" id="announce">
  <span>Candidature</span>
  <span style="color:rgba(201,185,154,.4)">·</span>
  <span>Directeur Commercial France</span>
  <span style="color:rgba(201,185,154,.4)">·</span>
  <em>Terence Richard</em>
</div>

<!-- ── HEADER STICKY ──────────────────────────── -->
<div class="header-wrap">

  <!-- TOP BAR (desktop) -->
  <div class="topbar" id="topbar">
    <div class="topbar-langs">
      <span class="active">FR</span>
      <span class="dot">·</span>
      <span>EN</span>
    </div>
    <a href="#contact" class="topbar-link">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M2 7l10 7 10-7"/></svg>
      Contact
    </a>
    <a href="#" class="topbar-link">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
      LinkedIn
    </a>
  </div>

  <!-- NAVBAR -->
  <nav class="navbar" id="navbar">
    <div class="nav-left">
      <div class="nav-item" id="ni-vision">
        <button class="nav-btn" onclick="toggleMega('vision')">
          Vision stratégique
          <span class="chevron"><svg viewBox="0 0 8 8" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="1 2.5 4 5.5 7 2.5"/></svg></span>
        </button>
      </div>
      <div class="nav-item" id="ni-marche">
        <button class="nav-btn" onclick="toggleMega('marche')">
          Le Marché
          <span class="chevron"><svg viewBox="0 0 8 8" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="1 2.5 4 5.5 7 2.5"/></svg></span>
        </button>
      </div>
      <div class="nav-item" id="ni-plan">
        <button class="nav-btn" onclick="toggleMega('plan')">
          Plan d'action
          <span class="chevron"><svg viewBox="0 0 8 8" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="1 2.5 4 5.5 7 2.5"/></svg></span>
        </button>
      </div>
    </div>

    <!-- Hamburger mobile -->
    <button class="hamburger" id="hamburger" onclick="toggleDrawer()" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>

    <a href="#hero" class="logo">TR</a>

    <div class="nav-right">
      <div class="nav-item" id="ni-profil">
        <button class="nav-btn" onclick="toggleMega('profil')">
          Mon Profil
          <span class="chevron"><svg viewBox="0 0 8 8" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="1 2.5 4 5.5 7 2.5"/></svg></span>
        </button>
      </div>
      <div class="nav-item" id="ni-apropos">
        <button class="nav-btn" onclick="toggleMega('apropos')">
          À Propos
          <span class="chevron"><svg viewBox="0 0 8 8" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="1 2.5 4 5.5 7 2.5"/></svg></span>
        </button>
      </div>
      <a href="#contact" class="icon-btn" title="Contact">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M2 7l10 7 10-7"/></svg>
      </a>
    </div>

    <!-- MEGA LAYER -->
    <div class="mega-layer">

      <!-- Vision -->
      <div class="mega-panel" id="mega-vision">
        <div class="mega-inner" style="grid-template-columns:repeat(3,1fr);gap:0;">
          <div style="border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">Axes principaux</div>
            <ul class="mega-links">
              <li><a href="#strategie" onclick="closeAllMega()">Activation de l'écosystème</a></li>
              <li><a href="#strategie" onclick="closeAllMega()">Développement de partenariats</a></li>
              <li><a href="#strategie" onclick="closeAllMega()">Renforcement de la visibilité</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">Segments cibles</div>
            <ul class="mega-links">
              <li><a href="#marche" onclick="closeAllMega()">Hospitality &amp; Hôtellerie</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Architectes &amp; Designers</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Retail premium</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Corporate gifting</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;">
            <div class="mega-col-title">Vision à moyen terme</div>
            <ul class="mega-links">
              <li><a href="#vision" onclick="closeAllMega()">Référence hospitality France</a></li>
              <li><a href="#vision" onclick="closeAllMega()">Réseau de prescripteurs</a></li>
              <li><a href="#vision" onclick="closeAllMega()">Présence retail premium</a></li>
            </ul>
            <a href="#strategie" class="mega-see-all" onclick="closeAllMega()">Voir la stratégie complète</a>
          </div>
        </div>
      </div>

      <!-- Marché -->
      <div class="mega-panel" id="mega-marche">
        <div class="mega-inner" style="grid-template-columns:180px 1fr 1fr;gap:0 44px;align-items:stretch;">
          <div style="background:var(--cream-dark);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:10px;padding:32px 24px;margin:-44px -44px -48px 0;">
            <div style="font-family:'Cormorant Garamond',serif;font-size:60px;color:var(--sand);opacity:.45;line-height:1;">FR</div>
            <div style="font-size:10px;letter-spacing:.2em;text-transform:uppercase;color:var(--ink-muted);text-align:center;font-weight:400;">Marché Français</div>
          </div>
          <div>
            <div class="mega-col-title">Écosystèmes clés</div>
            <ul class="mega-links">
              <li><a href="#marche" onclick="closeAllMega()">Gastronomie &amp; Restauration</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Hôtellerie de luxe</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Architecture &amp; Design</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Lifestyle premium</a></li>
            </ul>
          </div>
          <div>
            <div class="mega-col-title">Réseaux prioritaires</div>
            <ul class="mega-links">
              <li><a href="#marche" onclick="closeAllMega()">Architectes d'intérieur</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Groupes hôteliers</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Concept stores design</a></li>
              <li><a href="#marche" onclick="closeAllMega()">Promoteurs immobiliers</a></li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Plan -->
      <div class="mega-panel" id="mega-plan">
        <div class="mega-inner" style="grid-template-columns:repeat(3,1fr);gap:0;">
          <div style="border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">0 – 30 jours</div>
            <ul class="mega-links">
              <li><a href="#plan" onclick="closeAllMega()">Phase d'écoute</a></li>
              <li><a href="#plan" onclick="closeAllMega()">Analyse de l'équipe</a></li>
              <li><a href="#plan" onclick="closeAllMega()">Comptes clés existants</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">30 – 60 jours</div>
            <ul class="mega-links">
              <li><a href="#plan" onclick="closeAllMega()">Identification des priorités</a></li>
              <li><a href="#plan" onclick="closeAllMega()">Comptes stratégiques</a></li>
              <li><a href="#plan" onclick="closeAllMega()">Activation quick wins</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;">
            <div class="mega-col-title">60 – 90 jours</div>
            <ul class="mega-links">
              <li><a href="#plan" onclick="closeAllMega()">Feuille de route</a></li>
              <li><a href="#plan" onclick="closeAllMega()">Lancement des initiatives</a></li>
              <li><a href="#plan" onclick="closeAllMega()">KPIs &amp; objectifs</a></li>
            </ul>
            <a href="#plan" class="mega-see-all" onclick="closeAllMega()">Voir le plan complet</a>
          </div>
        </div>
      </div>

      <!-- Profil -->
      <div class="mega-panel" id="mega-profil">
        <div class="mega-inner" style="grid-template-columns:180px 1fr 1fr;gap:0 44px;align-items:stretch;">
          <div style="background:var(--cream-dark);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:12px;padding:32px 24px;margin:-44px -44px -48px 0;">
            <div style="font-family:'Cormorant Garamond',serif;font-size:54px;color:var(--sand);font-weight:300;line-height:1;">20+</div>
            <div style="width:28px;height:1px;background:var(--sand);"></div>
            <div style="font-size:10px;letter-spacing:.18em;text-transform:uppercase;color:var(--ink-muted);text-align:center;line-height:1.6;font-weight:400;">Années<br>d'exp. B2B</div>
          </div>
          <div>
            <div class="mega-col-title">Expériences</div>
            <ul class="mega-links">
              <li><a href="#profil" onclick="closeAllMega()">Management commercial</a></li>
              <li><a href="#profil" onclick="closeAllMega()">Pilotage de P&amp;L</a></li>
              <li><a href="#profil" onclick="closeAllMega()">Comptes stratégiques</a></li>
              <li><a href="#profil" onclick="closeAllMega()">Distribution premium</a></li>
            </ul>
          </div>
          <div>
            <div class="mega-col-title">Atouts clés</div>
            <ul class="mega-links">
              <li><a href="#profil" onclick="closeAllMega()">Structuration de marchés</a></li>
              <li><a href="#profil" onclick="closeAllMega()">Activation d'écosystèmes</a></li>
              <li><a href="#profil" onclick="closeAllMega()">Réseau prescripteurs</a></li>
            </ul>
            <a href="#profil" class="mega-see-all" onclick="closeAllMega()">Voir le profil complet</a>
          </div>
        </div>
      </div>

      <!-- À propos -->
      <div class="mega-panel" id="mega-apropos">
        <div class="mega-inner" style="grid-template-columns:180px 1fr 1fr;gap:0 44px;align-items:stretch;">
          <div style="background:var(--ink);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:12px;padding:32px 20px;margin:-44px -44px -48px 0;">
            <div style="font-family:'Cormorant Garamond',serif;font-size:22px;color:var(--cream);font-weight:400;letter-spacing:.06em;text-align:center;line-height:1.3;">Terence<br>Richard</div>
            <div style="width:28px;height:1px;background:var(--sand);"></div>
            <div style="font-size:9.5px;letter-spacing:.18em;text-transform:uppercase;color:var(--sand);font-weight:400;text-align:center;">Dir. Commercial</div>
          </div>
          <div>
            <div class="mega-col-title">Candidature</div>
            <ul class="mega-links">
              <li><a href="#hero" onclick="closeAllMega()">Introduction</a></li>
              <li><a href="#profil" onclick="closeAllMega()">Mon profil</a></li>
              <li><a href="#strategie" onclick="closeAllMega()">Vision stratégique</a></li>
              <li><a href="#plan" onclick="closeAllMega()">Plan 90 jours</a></li>
            </ul>
          </div>
          <div>
            <div class="mega-col-title">Contact</div>
            <ul class="mega-links">
              <li><a href="#contact" onclick="closeAllMega()">Coordonnées</a></li>
              <li><a href="#" onclick="closeAllMega()">LinkedIn</a></li>
              <li><a href="#contact" onclick="closeAllMega()">Envoyer un message</a></li>
            </ul>
            <a href="#contact" class="mega-see-all" onclick="closeAllMega()">Prendre contact</a>
          </div>
        </div>
      </div>

    </div><!-- /mega-layer -->
  </nav>
</div>

<!-- Backdrop desktop -->
<div class="mega-backdrop" id="backdrop" onclick="closeAllMega()"></div>

<!-- ── MOBILE DRAWER ─────────────────────────── -->
<div class="drawer-veil" id="drawerVeil" onclick="closeDrawer()"></div>
<div class="drawer" id="drawer">

  <div class="drawer-head">
    <span class="drawer-logo">TR</span>
    <button class="drawer-close-btn" onclick="closeDrawer()" aria-label="Fermer">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
        <line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/>
      </svg>
    </button>
  </div>

  <div class="drawer-body">
    <div class="drawer-group">
      <button class="drawer-toggle" onclick="toggleSub('dsub-vision', this)">
        Vision stratégique
        <span class="drawer-toggle-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><polyline points="6 9 12 15 18 9"/></svg></span>
      </button>
      <div class="drawer-sub" id="dsub-vision">
        <div class="drawer-sub-cat">Axes</div>
        <a href="#strategie" onclick="closeDrawer()">Activation de l'écosystème</a>
        <a href="#strategie" onclick="closeDrawer()">Développement de partenariats</a>
        <a href="#strategie" onclick="closeDrawer()">Renforcement de la visibilité</a>
        <div class="drawer-sub-cat">Objectifs</div>
        <a href="#vision" onclick="closeDrawer()">Référence hospitality France</a>
        <a href="#vision" onclick="closeDrawer()">Réseau de prescripteurs</a>
      </div>
    </div>
    <div class="drawer-group">
      <button class="drawer-toggle" onclick="toggleSub('dsub-marche', this)">
        Le Marché
        <span class="drawer-toggle-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><polyline points="6 9 12 15 18 9"/></svg></span>
      </button>
      <div class="drawer-sub" id="dsub-marche">
        <div class="drawer-sub-cat">Écosystèmes</div>
        <a href="#marche" onclick="closeDrawer()">Gastronomie &amp; Restauration</a>
        <a href="#marche" onclick="closeDrawer()">Hôtellerie de luxe</a>
        <a href="#marche" onclick="closeDrawer()">Architecture &amp; Design</a>
        <div class="drawer-sub-cat">Réseaux</div>
        <a href="#marche" onclick="closeDrawer()">Architectes d'intérieur</a>
        <a href="#marche" onclick="closeDrawer()">Groupes hôteliers</a>
        <a href="#marche" onclick="closeDrawer()">Concept stores design</a>
      </div>
    </div>
    <div class="drawer-group">
      <button class="drawer-toggle" onclick="toggleSub('dsub-plan', this)">
        Plan d'action
        <span class="drawer-toggle-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><polyline points="6 9 12 15 18 9"/></svg></span>
      </button>
      <div class="drawer-sub" id="dsub-plan">
        <a href="#plan" onclick="closeDrawer()">0–30 jours · Écoute &amp; Analyse</a>
        <a href="#plan" onclick="closeDrawer()">30–60 jours · Priorisation</a>
        <a href="#plan" onclick="closeDrawer()">60–90 jours · Lancement</a>
      </div>
    </div>
    <div class="drawer-group">
      <button class="drawer-toggle" onclick="toggleSub('dsub-profil', this)">
        Mon Profil
        <span class="drawer-toggle-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><polyline points="6 9 12 15 18 9"/></svg></span>
      </button>
      <div class="drawer-sub" id="dsub-profil">
        <a href="#profil" onclick="closeDrawer()">Expérience &amp; compétences</a>
        <a href="#leadership" onclick="closeDrawer()">Approche de leadership</a>
        <a href="#profil" onclick="closeDrawer()">Atouts différenciants</a>
      </div>
    </div>
    <div class="drawer-group">
      <button class="drawer-toggle" onclick="toggleSub('dsub-apropos', this)">
        À Propos
        <span class="drawer-toggle-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><polyline points="6 9 12 15 18 9"/></svg></span>
      </button>
      <div class="drawer-sub" id="dsub-apropos">
        <a href="#hero" onclick="closeDrawer()">Introduction</a>
        <a href="#strategie" onclick="closeDrawer()">Vision stratégique</a>
        <a href="#contact" onclick="closeDrawer()">Contact</a>
      </div>
    </div>
  </div>

  <div class="drawer-foot">
    <a href="#" class="drawer-foot-btn">LinkedIn</a>
    <a href="#contact" class="drawer-foot-btn primary" onclick="closeDrawer()">Contact</a>
  </div>

</div>

<!-- ══════════════════════════════════════════════
     HERO
══════════════════════════════════════════════ -->
<section class="hero" id="hero">
  <div class="hero-visual">
    <div class="hero-pattern"></div>
    <div class="hero-mono">TR</div>
    <div class="hero-side-text">Vision Stratégique · France · 2025</div>
  </div>
  <div class="hero-content">
    <span class="hero-eyebrow">Candidature — Directeur Commercial France</span>
    <h1 class="hero-title">Développement<br><em>de Serax</em><br>en France</h1>
    <p class="hero-sub">Terence Richard</p>
    <div class="hero-rule"></div>
    <p class="hero-intro">Serax occupe une position unique à l'intersection du design, de l'hospitality et du lifestyle premium. La France représente l'un des marchés les plus influents en Europe — un écosystème riche à structurer et à activer.</p>
    <a href="#profil" class="hero-cta">Découvrir la vision <span class="hero-cta-line"></span></a>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     PROFIL
══════════════════════════════════════════════ -->
<section class="section s-profil" id="profil">
  <div class="si">
    <div class="sh reveal">
      <span class="s-tag">Mon Profil</span>
      <h2 class="s-title">Dirigeant commercial<br><em>&amp; développeur de marchés</em></h2>
    </div>
    <div class="profil-grid reveal">
      <div>
        <div class="profil-text">
          <p>Dirigeant commercial avec plus de vingt ans d'expérience en développement et structuration de marchés B2B en France et à l'international.</p>
          <p>Plus récemment, création et structuration d'une plateforme de distribution dans l'univers du mobilier premium avec activation d'un réseau d'architectes et de prescripteurs.</p>
        </div>
        <div class="tags">
          <span class="tag">Management commercial</span>
          <span class="tag">Pilotage P&amp;L</span>
          <span class="tag">Comptes stratégiques</span>
          <span class="tag">Marchés premium</span>
          <span class="tag">Prescription</span>
          <span class="tag">Distribution sélective</span>
        </div>
      </div>
      <div class="profil-divider"></div>
      <div>
        <div class="stats-grid">
          <div class="stat-card"><div class="stat-n">20<sup>+</sup></div><div class="stat-l">Années d'expérience B2B</div></div>
          <div class="stat-card"><div class="stat-n">3</div><div class="stat-l">Axes stratégiques France</div></div>
          <div class="stat-card"><div class="stat-n">90</div><div class="stat-l">Jours pour un plan concret</div></div>
          <div class="stat-card"><div class="stat-n">5</div><div class="stat-l">Segments à activer</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     MARCHÉ
══════════════════════════════════════════════ -->
<section class="section s-marche" id="marche">
  <div class="si">
    <div class="sh reveal">
      <span class="s-tag">Le Marché Français</span>
      <h2 class="s-title">Un écosystème premium<br><em>à fort potentiel</em></h2>
    </div>
    <div class="marche-grid reveal">
      <div class="m-card">
        <div class="m-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg></div>
        <div class="m-title">Hospitality</div>
        <div class="m-text">Un secteur en plein essor, moteur de croissance pour Serax en France.</div>
        <ul class="m-list">
          <li>Hôtels &amp; palaces</li>
          <li>Restaurants &amp; chefs étoilés</li>
          <li>Groupes de restauration</li>
        </ul>
      </div>
      <div class="m-card">
        <div class="m-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><circle cx="12" cy="12" r="10"/><path d="M12 2a14.5 14.5 0 000 20 14.5 14.5 0 000-20"/><line x1="2" y1="12" x2="22" y2="12"/></svg></div>
        <div class="m-title">Prescription</div>
        <div class="m-text">Les architectes et designers sont des relais d'influence essentiels.</div>
        <ul class="m-list">
          <li>Architectes d'intérieur</li>
          <li>Studios de design</li>
          <li>Promoteurs immobiliers</li>
        </ul>
      </div>
      <div class="m-card">
        <div class="m-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M6 2L3 6v14a2 2 0 002 2h14a2 2 0 002-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 01-8 0"/></svg></div>
        <div class="m-title">Retail Premium</div>
        <div class="m-text">Une distribution sélective cohérente avec le positionnement Serax.</div>
        <ul class="m-list">
          <li>Concept stores design</li>
          <li>Showrooms sélectifs</li>
          <li>Corners dédiés premium</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     STRATÉGIE
══════════════════════════════════════════════ -->
<section class="section s-strat" id="strategie">
  <div class="si">
    <div class="sh reveal">
      <span class="s-tag">Stratégie de Développement</span>
      <h2 class="s-title">Trois axes<br><em>pour s'imposer</em></h2>
    </div>
    <div class="axes-grid reveal">
      <div class="axe-card">
        <span class="axe-bg-n">01</span>
        <span class="axe-tag">Axe 1</span>
        <div class="axe-title">Activation de l'écosystème</div>
        <div class="axe-text">Identifier et activer tous les acteurs clés du marché français autour de Serax.</div>
        <ul class="axe-list">
          <li>Architectes &amp; designers</li>
          <li>Hospitality &amp; restaurants</li>
          <li>Retail premium</li>
          <li>Projets immobiliers</li>
        </ul>
      </div>
      <div class="axe-card">
        <span class="axe-bg-n">02</span>
        <span class="axe-tag">Axe 2</span>
        <div class="axe-title">Développement de partenariats</div>
        <div class="axe-text">Construire des partenariats durables avec les acteurs premium du marché.</div>
        <ul class="axe-list">
          <li>Groupes hôteliers</li>
          <li>Restaurateurs &amp; chefs</li>
          <li>Concept stores</li>
          <li>Promoteurs immobiliers</li>
        </ul>
      </div>
      <div class="axe-card">
        <span class="axe-bg-n">03</span>
        <span class="axe-tag">Axe 3</span>
        <div class="axe-title">Renforcement de la visibilité</div>
        <div class="axe-text">Affirmer la présence de Serax dans l'univers créatif et professionnel français.</div>
        <ul class="axe-list">
          <li>Événements &amp; salons</li>
          <li>Collaborations chefs &amp; designers</li>
          <li>Réseaux professionnels</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     PLAN 90 JOURS
══════════════════════════════════════════════ -->
<section class="section s-plan" id="plan">
  <div class="si">
    <div class="sh reveal">
      <span class="s-tag">Plan d'Action</span>
      <h2 class="s-title">Les premiers<br><em>90 jours</em></h2>
    </div>
    <div class="plan-grid reveal">
      <div class="plan-phase">
        <div class="plan-dot">1</div>
        <div class="plan-period">0 — 30 jours</div>
        <div class="plan-ph-title">Écoute &amp; Analyse</div>
        <ul class="plan-items">
          <li>Phase d'écoute approfondie</li>
          <li>Analyse de l'équipe en place</li>
          <li>Audit des comptes clés</li>
          <li>Compréhension de la distribution et des partenaires existants</li>
        </ul>
      </div>
      <div class="plan-phase">
        <div class="plan-dot">2</div>
        <div class="plan-period">30 — 60 jours</div>
        <div class="plan-ph-title">Priorisation</div>
        <ul class="plan-items">
          <li>Identification des priorités stratégiques</li>
          <li>Sélection des comptes stratégiques</li>
          <li>Identification et activation des quick wins</li>
        </ul>
      </div>
      <div class="plan-phase">
        <div class="plan-dot">3</div>
        <div class="plan-period">60 — 90 jours</div>
        <div class="plan-ph-title">Lancement</div>
        <ul class="plan-items">
          <li>Construction d'une feuille de route structurée</li>
          <li>Lancement des initiatives prioritaires</li>
          <li>Mise en place des KPIs</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     VISION QUOTE
══════════════════════════════════════════════ -->
<section class="s-vision" id="vision">
  <div class="vision-inner">
    <blockquote class="vision-q reveal">
      Positionner Serax comme une référence incontournable dans l'univers hospitality et design en France.
    </blockquote>
    <div class="vision-rule"></div>
    <div class="vision-by">Terence Richard — Vision à moyen terme</div>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     LEADERSHIP
══════════════════════════════════════════════ -->
<section class="section s-lead" id="leadership">
  <div class="si">
    <div class="sh reveal" style="text-align:center;">
      <span class="s-tag" style="text-align:center;display:block;">Approche de Leadership</span>
      <h2 class="s-title" style="text-align:center;">Un management<br><em>orienté terrain</em></h2>
    </div>
    <div class="lead-grid reveal">
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg></div>
        <div>
          <div class="lead-name">Clarté des objectifs</div>
          <div class="lead-desc">Définir des priorités claires, mesurables et alignées avec la stratégie globale Serax.</div>
        </div>
      </div>
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg></div>
        <div>
          <div class="lead-name">Responsabilisation</div>
          <div class="lead-desc">Accompagner l'équipe dans une culture de l'autonomie et de la performance.</div>
        </div>
      </div>
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg></div>
        <div>
          <div class="lead-name">Proximité terrain</div>
          <div class="lead-desc">Un management ancré dans la réalité du marché, au contact direct des clients.</div>
        </div>
      </div>
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/></svg></div>
        <div>
          <div class="lead-name">Communication directe</div>
          <div class="lead-desc">Favoriser la collaboration ouverte et la transparence à tous les niveaux.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     CONTACT
══════════════════════════════════════════════ -->
<section class="s-contact" id="contact">
  <div class="contact-inner reveal">
    <h2 class="contact-title">Prenons contact</h2>
    <p class="contact-sub">Je suis disponible pour échanger sur cette opportunité et approfondir ensemble la vision stratégique pour Serax en France.</p>
    <div class="contact-info">
      <div>
        <div class="ci-label">Nom</div>
        <div class="ci-val">Terence Richard</div>
      </div>
      <div>
        <div class="ci-label">Poste visé</div>
        <div class="ci-val">Directeur Commercial France</div>
      </div>
      <div>
        <div class="ci-label">Disponibilité</div>
        <div class="ci-val">Sur demande</div>
      </div>
    </div>
    <a href="mailto:terence.richard75@gmail.com" class="btn-cta">Envoyer un message</a>
  </div>
</section>

<!-- ══════════════════════════════════════════════
     FOOTER
══════════════════════════════════════════════ -->
<footer>
  <div class="footer-inner">
    <div class="footer-grid">
      <div>
        <span class="footer-logo-text">TR</span>
        <p class="footer-tagline">Vision stratégique pour le développement de Serax en France — Terence Richard, Directeur Commercial.</p>
      </div>
      <div>
        <div class="footer-col-head">Vision</div>
        <ul class="footer-links">
          <li><a href="#strategie">Stratégie</a></li>
          <li><a href="#marche">Marché français</a></li>
          <li><a href="#plan">Plan 90 jours</a></li>
          <li><a href="#vision">Objectifs</a></li>
        </ul>
      </div>
      <div>
        <div class="footer-col-head">Profil</div>
        <ul class="footer-links">
          <li><a href="#profil">Expérience</a></li>
          <li><a href="#leadership">Leadership</a></li>
          <li><a href="#profil">Compétences</a></li>
        </ul>
      </div>
      <div>
        <div class="footer-col-head">Contact</div>
        <ul class="footer-links">
          <li><a href="#contact">Message direct</a></li>
          <li><a href="#">LinkedIn</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <span class="footer-copy">© Terence Richard — Candidature Serax France</span>
      <span class="footer-yr">2025</span>
    </div>
  </div>
</footer>

<!-- ══════════════════════════════════════════════
     JAVASCRIPT
══════════════════════════════════════════════ -->
<script>
/* ─── CONFIG ─── */
const MEGAS = {
  vision:  { ni: 'ni-vision',  panel: 'mega-vision'  },
  marche:  { ni: 'ni-marche',  panel: 'mega-marche'  },
  plan:    { ni: 'ni-plan',    panel: 'mega-plan'    },
  profil:  { ni: 'ni-profil',  panel: 'mega-profil'  },
  apropos: { ni: 'ni-apropos', panel: 'mega-apropos' },
};
let currentMega = null;
let megaCloseTimer = null;

/* ─── MEGA MENUS ─── */
function openMega(key) {
  if (megaCloseTimer) { clearTimeout(megaCloseTimer); megaCloseTimer = null; }
  if (currentMega === key) return;
  closeMegaOnly(currentMega, false);
  currentMega = key;
  document.getElementById(MEGAS[key].ni).classList.add('open');
  document.getElementById(MEGAS[key].panel).classList.add('open');
  document.getElementById('backdrop').classList.add('open');
}

function closeMegaOnly(key, resetCurrent = true) {
  if (!key) return;
  document.getElementById(MEGAS[key].ni).classList.remove('open');
  document.getElementById(MEGAS[key].panel).classList.remove('open');
  if (resetCurrent) {
    document.getElementById('backdrop').classList.remove('open');
    currentMega = null;
  }
}

function toggleMega(key) {
  if (currentMega === key) { closeAllMega(); }
  else { openMega(key); }
}

function closeAllMega() {
  Object.keys(MEGAS).forEach(k => {
    document.getElementById(MEGAS[k].ni).classList.remove('open');
    document.getElementById(MEGAS[k].panel).classList.remove('open');
  });
  document.getElementById('backdrop').classList.remove('open');
  currentMega = null;
}

/* Hover intent on nav items */
document.querySelectorAll('.nav-item').forEach(item => {
  const key = Object.keys(MEGAS).find(k => item.id === MEGAS[k].ni);
  if (!key) return;
  item.addEventListener('mouseenter', () => openMega(key));
  item.addEventListener('mouseleave', () => {
    megaCloseTimer = setTimeout(() => {
      if (currentMega === key) closeAllMega();
    }, 120);
  });
});

/* Keep open when hovering the panel */
Object.keys(MEGAS).forEach(key => {
  const panel = document.getElementById(MEGAS[key].panel);
  panel.addEventListener('mouseenter', () => {
    if (megaCloseTimer) { clearTimeout(megaCloseTimer); megaCloseTimer = null; }
  });
  panel.addEventListener('mouseleave', () => {
    megaCloseTimer = setTimeout(() => closeAllMega(), 120);
  });
});

/* ─── DRAWER MOBILE ─── */
let drawerIsOpen = false;
let openSubId = null;

function toggleDrawer() {
  drawerIsOpen ? closeDrawer() : openDrawer();
}
function openDrawer() {
  drawerIsOpen = true;
  document.getElementById('drawer').classList.add('open');
  document.getElementById('drawerVeil').classList.add('open');
  document.getElementById('hamburger').classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeDrawer() {
  drawerIsOpen = false;
  document.getElementById('drawer').classList.remove('open');
  document.getElementById('drawerVeil').classList.remove('open');
  document.getElementById('hamburger').classList.remove('open');
  document.body.style.overflow = '';
}

function toggleSub(id, btn) {
  const sub = document.getElementById(id);
  const isOpen = sub.classList.contains('open');

  // Close previously open
  if (openSubId && openSubId !== id) {
    const prev = document.getElementById(openSubId);
    if (prev) {
      prev.classList.remove('open');
      const prevBtn = prev.previousElementSibling;
      if (prevBtn) prevBtn.classList.remove('expanded');
    }
  }

  if (isOpen) {
    sub.classList.remove('open');
    btn.classList.remove('expanded');
    openSubId = null;
  } else {
    sub.classList.add('open');
    btn.classList.add('expanded');
    openSubId = id;
  }
}

/* ─── SCROLL BEHAVIOUR ─── */
const navbar   = document.getElementById('navbar');
const topbar   = document.getElementById('topbar');
const announce = document.getElementById('announce');
let lastScroll = 0;

window.addEventListener('scroll', () => {
  const y = window.scrollY;

  // Navbar elevation
  navbar.classList.toggle('elevated', y > 10);

  // Hide announce + topbar on scroll down
  if (y > 80) {
    announce.classList.add('hidden');
    topbar.classList.add('compact');
  } else {
    announce.classList.remove('hidden');
    topbar.classList.remove('compact');
  }

  // Close mega on scroll
  if (Math.abs(y - lastScroll) > 40) closeAllMega();
  lastScroll = y;
}, { passive: true });

/* ─── KEYBOARD ─── */
document.addEventListener('keydown', e => {
  if (e.key === 'Escape') { closeAllMega(); closeDrawer(); }
});

/* ─── SCROLL REVEAL ─── */
const revealObs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.classList.add('visible');
      revealObs.unobserve(e.target);
    }
  });
}, { threshold: 0.08 });
document.querySelectorAll('.reveal').forEach(el => revealObs.observe(el));
</script>
</body>
</html>
