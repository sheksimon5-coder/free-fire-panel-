
<html lang="bn">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover, shrink-to-fit=no, maximum-scale=1.0, user-scalable=no" />
<meta name="theme-color" content="#0b0f1a" />
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<meta name="format-detection" content="telephone=no" />
<title>Panel Bajar — Premium Mods Store</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Poppins:wght@400;500;600;700;800&family=Hind+Siliguri:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
/* ============================================================
   PANEL BAJAR — PREMIUM MODS STORE
   Mobile-first, full-width, professional design
   ============================================================ */

*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
img,svg{max-width:100%;height:auto;display:block}

:root{
  --bg:#080b14;
  --bg-soft:#0f1421;
  --card:#161c2e;
  --card-2:#0c111d;
  --card-3:#1a2138;
  --border:#252d44;
  --border-soft:#1c2438;
  --primary:#7c3aed;
  --primary-dark:#5b21b6;
  --primary-light:#a78bfa;
  --primary-glow:rgba(124,58,237,.45);
  --accent:#ec4899;
  --success:#10b981;
  --success-dark:#059669;
  --warning:#f59e0b;
  --danger:#ef4444;
  --info:#3b82f6;
  --bkash:#e2136e;
  --nagad:#ec1c24;
  --text:#f1f5f9;
  --text-mid:#94a3b8;
  --muted:#64748b;
  --white:#fff;
  --shadow-xs:0 1px 2px rgba(0,0,0,.5);
  --shadow-sm:0 4px 14px rgba(0,0,0,.45);
  --shadow-md:0 10px 32px rgba(0,0,0,.6);
  --shadow-lg:0 20px 50px rgba(0,0,0,.7);
  --shadow-neon:0 0 24px rgba(124,58,237,.4);
  --shadow-neon-s:0 0 24px rgba(16,185,129,.4);
  --grad-primary:linear-gradient(135deg,#7c3aed 0%,#a855f7 50%,#ec4899 100%);
  --grad-success:linear-gradient(135deg,#10b981 0%,#059669 100%);
  --grad-danger:linear-gradient(135deg,#ef4444 0%,#dc2626 100%);
  --grad-bkash:linear-gradient(135deg,#e2136e 0%,#be185d 100%);
  --grad-card:linear-gradient(180deg,#161c2e 0%,#0c111d 100%);
  --grad-hero:linear-gradient(135deg,rgba(124,58,237,.25) 0%,rgba(236,72,153,.18) 50%,rgba(16,185,129,.12) 100%);
  --safe-top:env(safe-area-inset-top,0px);
  --safe-bottom:env(safe-area-inset-bottom,0px);
  --radius-sm:10px;
  --radius-md:14px;
  --radius-lg:18px;
  --radius-xl:22px;
  --radius-full:999px;
}

/* === CRITICAL: Force FULL-WIDTH mobile layout (no side gaps) === */
html{
  width:100%;
  max-width:100%;
  -webkit-text-size-adjust:100%;
  text-size-adjust:100%;
  scroll-behavior:smooth;
  background:var(--bg);
}
body{
  width:100%;
  max-width:100%;
  margin:0;
  padding:0;
  font-family:'Hind Siliguri','Poppins',-apple-system,BlinkMacSystemFont,sans-serif;
  background:var(--bg);
  color:var(--text);
  min-height:100vh;
  min-height:100dvh;
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  overflow-x:hidden;
  overflow-y:auto;
  position:relative;
  padding-bottom:calc(96px + var(--safe-bottom));
}

/* Every container fills FULL width on mobile */
main, header, .container, .header-in, .botnav, .modal, .welcome-modal, .whatsapp-fab, .ad-slider, .grid, .tabs, .social-bar{
  width:100%;
  max-width:100%;
}

a{color:inherit;text-decoration:none}
button{cursor:pointer;border:none;font-family:inherit;color:inherit;background:none;outline:none;-webkit-tap-highlight-color:transparent}
button:focus-visible{outline:2px solid var(--primary-light);outline-offset:2px}
input,select,textarea{
  background:var(--card-2);
  border:1.5px solid var(--border);
  color:var(--text);
  border-radius:var(--radius-md);
  padding:14px 16px;
  width:100%;
  font-family:inherit;
  font-size:16px; /* prevents iOS auto-zoom */
  transition:all .2s;
  max-width:100%;
  -webkit-appearance:none;
  appearance:none;
}
input:focus,select:focus,textarea:focus{outline:none;border-color:var(--primary);box-shadow:0 0 0 3px var(--primary-glow)}
textarea{resize:vertical;min-height:80px}
select{background-image:url("data:image/svg+xml;charset=utf-8,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath fill='%2394a3b8' d='M6 8L0 0h12z'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 16px center;padding-right:40px}
::-webkit-scrollbar{width:5px;height:5px}
::-webkit-scrollbar-track{background:transparent}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px}

/* ============ HEADER ============ */
header{
  position:sticky;
  top:0;
  z-index:40;
  background:rgba(8,11,20,.85);
  backdrop-filter:blur(20px) saturate(180%);
  -webkit-backdrop-filter:blur(20px) saturate(180%);
  border-bottom:1px solid var(--border-soft);
  padding-top:var(--safe-top);
}
.header-in{
  width:100%;
  max-width:100%;
  margin:0;
  padding:10px 14px;
  height:60px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:10px;
}
.logo{display:flex;align-items:center;gap:10px;cursor:pointer;min-width:0;flex-shrink:1}
.logo-badge{
  width:42px;height:42px;
  border-radius:12px;
  background:var(--grad-primary);
  display:flex;align-items:center;justify-content:center;
  font-weight:900;color:#fff;font-size:15px;
  box-shadow:0 4px 14px var(--primary-glow);
  overflow:hidden;flex-shrink:0;
  font-family:'Orbitron',sans-serif;
  letter-spacing:.5px;
  position:relative;
}
.logo-badge::after{content:'';position:absolute;inset:0;background:linear-gradient(135deg,rgba(255,255,255,.2),transparent 50%);pointer-events:none}
.logo-badge img{width:100%;height:100%;object-fit:cover}
.logo-name{
  font-family:'Orbitron',sans-serif;
  font-weight:800;
  font-size:clamp(13px,3.5vw,16px);
  letter-spacing:.5px;
  white-space:nowrap;
  overflow:hidden;
  text-overflow:ellipsis;
  color:#fff;
  text-shadow:0 0 12px var(--primary-glow);
  min-width:0;
}
.header-right{display:flex;align-items:center;gap:6px;flex-shrink:0}

/* === PREMIUM BALANCE CHIP WITH WALLET SVG === */
.balance-chip{
  display:inline-flex;
  align-items:center;
  gap:6px;
  padding:8px 14px;
  border-radius:var(--radius-full);
  background:linear-gradient(135deg,rgba(16,185,129,.18),rgba(5,150,105,.12));
  color:var(--success);
  font-weight:800;
  font-size:clamp(11px,3vw,13px);
  border:1px solid rgba(16,185,129,.35);
  white-space:nowrap;
  cursor:pointer;
  font-family:'Orbitron',sans-serif;
  transition:.2s;
  min-height:38px;
  box-shadow:0 2px 10px rgba(16,185,129,.15);
}
.balance-chip:active{transform:scale(.96)}
.balance-chip .wallet-ic{
  width:16px;height:16px;
  stroke:var(--success);
  filter:drop-shadow(0 0 4px rgba(16,185,129,.5));
  flex-shrink:0;
}

.status-badge{display:flex;align-items:center;gap:4px;padding:6px 10px;border-radius:var(--radius-full);font-size:10px;font-weight:700;border:1px solid transparent;white-space:nowrap}
.status-badge.online{background:rgba(16,185,129,.12);color:var(--success);border-color:rgba(16,185,129,.25)}
.status-badge.offline{background:rgba(239,68,68,.12);color:var(--danger);border-color:rgba(239,68,68,.25)}
.status-dot{width:6px;height:6px;border-radius:50%;background:currentColor}
.status-badge.online .status-dot{animation:blink 1.5s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.btn-login{
  padding:0 18px;height:38px;border-radius:var(--radius-full);
  font-weight:700;font-size:13px;
  background:var(--grad-primary);
  color:#fff;
  box-shadow:0 4px 14px var(--primary-glow);
  transition:.2s;min-height:38px;
  display:inline-flex;align-items:center;gap:6px;
}
.btn-login:active{transform:scale(.96)}
.btn-avatar{
  width:38px;height:38px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-weight:700;color:#fff;font-size:13px;
  border:2px solid var(--primary);
  box-shadow:0 4px 14px var(--primary-glow);
  flex-shrink:0;
}

/* ============ MAIN ============ */
main{
  min-height:calc(100vh - 60px);
  min-height:calc(100dvh - 60px);
  width:100%;
  padding-bottom:calc(96px + var(--safe-bottom));
}
/* Container: FULL WIDTH on mobile, centered with max-width only on large screens */
.container{
  width:100%;
  max-width:100%;
  margin:0;
  padding:12px 12px;
}
@media (min-width:768px){
  .container{max-width:720px;margin:0 auto;padding:20px}
  .header-in{max-width:720px;margin:0 auto}
}

.card{
  background:var(--grad-card);
  border:1px solid var(--border-soft);
  border-radius:var(--radius-lg);
  box-shadow:var(--shadow-sm);
  max-width:100%;
}

/* ============ BUTTONS ============ */
.btn{display:inline-flex;align-items:center;justify-content:center;gap:6px;border-radius:var(--radius-md);font-weight:700;transition:.2s;min-height:44px;padding:12px 18px;font-size:14px;border:none;cursor:pointer;font-family:inherit;text-align:center}
.btn:active{transform:scale(.97)}
.btn-primary{background:var(--grad-primary);color:#fff;box-shadow:0 4px 14px var(--primary-glow)}
.btn-success{background:var(--grad-success);color:#fff;box-shadow:0 4px 14px rgba(16,185,129,.3)}
.btn-danger{background:var(--grad-danger);color:#fff;box-shadow:0 4px 14px rgba(239,68,68,.3)}
.btn-warning{background:linear-gradient(135deg,#f59e0b,#d97706);color:#fff}
.btn-bkash{background:var(--grad-bkash);color:#fff;box-shadow:0 4px 14px rgba(226,19,110,.3)}
.btn-ghost{background:var(--card-2);color:var(--text);border:1.5px solid var(--border)}
.btn-soft{background:var(--card-3);color:var(--text)}
.btn-full{width:100%}
.btn-sm{min-height:36px;padding:8px 14px;font-size:12px}
.btn-lg{min-height:52px;padding:16px 24px;font-size:16px}
.btn:disabled{opacity:.5;cursor:not-allowed;transform:none}

/* ============ AD SLIDER ============ */
.ad-slider{
  width:100%;
  max-width:100%;
  margin:0 0 14px;
  border-radius:var(--radius-lg);
  overflow:hidden;
  position:relative;
  background:var(--card-2);
  box-shadow:var(--shadow-md);
  aspect-ratio:16/7;
  max-height:260px;
  border:1px solid var(--border-soft);
  touch-action:pan-y;
  cursor:grab;
  user-select:none;
}
.ad-slider.ad-dragging{cursor:grabbing}
.ad-track{display:flex;height:100%;transition:transform .5s cubic-bezier(.45,0,.2,1);will-change:transform}
.ad-track.no-anim{transition:none}
.ad-slide{flex:0 0 100%;height:100%;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center;pointer-events:none}
.ad-slide img{width:100%;height:100%;object-fit:cover;object-position:center}
.ad-dots{position:absolute;bottom:10px;left:50%;transform:translateX(-50%);display:flex;gap:5px;z-index:5}
.ad-dot{width:7px;height:7px;border-radius:50%;background:rgba(255,255,255,.35);cursor:pointer;transition:.3s;pointer-events:auto}
.ad-dot.active{background:var(--primary);width:22px;border-radius:4px;box-shadow:0 0 8px var(--primary)}

/* ============ HERO CARD ============ */
.hero-card{
  margin:0 0 14px;
  padding:22px 18px;
  border-radius:var(--radius-xl);
  background:var(--grad-hero);
  border:1px solid rgba(124,58,237,.3);
  color:#fff;
  box-shadow:var(--shadow-md);
  position:relative;
  overflow:hidden;
  width:100%;
}
.hero-card::before{
  content:'';position:absolute;top:-40%;right:-20%;
  width:260px;height:260px;
  background:radial-gradient(circle,rgba(124,58,237,.35) 0%,transparent 70%);
  border-radius:50%;
}
.hero-card::after{
  content:'';position:absolute;bottom:-30%;left:-15%;
  width:200px;height:200px;
  background:radial-gradient(circle,rgba(16,185,129,.2) 0%,transparent 70%);
  border-radius:50%;
}
.hero-content{position:relative;z-index:2}
.hero-label{
  font-size:12px;opacity:.9;font-weight:600;letter-spacing:.5px;
  text-transform:uppercase;display:flex;align-items:center;gap:8px;
}
.hero-label .wallet-ic-lg{width:18px;height:18px;stroke:#fff;opacity:.9;flex-shrink:0}
.hero-balance{
  font-family:'Orbitron',sans-serif;
  font-size:clamp(28px,8vw,38px);
  font-weight:900;
  margin:8px 0 4px;
  letter-spacing:1px;
  text-shadow:0 0 20px rgba(255,255,255,.2);
  word-break:break-all;
}
.hero-actions{display:flex;gap:8px;margin-top:18px;flex-wrap:wrap}
.hero-btn{
  padding:11px 20px;
  border-radius:var(--radius-md);
  background:rgba(255,255,255,.12);
  color:#fff;font-weight:700;font-size:13px;
  backdrop-filter:blur(8px);
  border:1px solid rgba(255,255,255,.2);
  transition:.2s;min-height:44px;
  display:inline-flex;align-items:center;gap:6px;cursor:pointer;
}
.hero-btn:active{transform:scale(.97)}
.hero-btn.solid{background:#fff;color:var(--primary)}

/* ============ TABS ============ */
.tabs{
  display:flex;gap:6px;margin:0 0 12px;
  overflow-x:auto;scrollbar-width:none;padding-bottom:2px;
  width:100%;
  -webkit-overflow-scrolling:touch;
}
.tabs::-webkit-scrollbar{display:none}
.tab{
  padding:9px 16px;
  border-radius:var(--radius-md);
  font-size:13px;font-weight:700;
  background:var(--card);border:1.5px solid var(--border-soft);
  transition:.2s;color:var(--text-mid);flex-shrink:0;
  min-height:40px;display:inline-flex;align-items:center;gap:4px;
  cursor:pointer;white-space:nowrap;
}
.tab.active{background:var(--grad-primary);color:#fff;border-color:transparent;box-shadow:0 4px 12px var(--primary-glow)}

/* ============ PRODUCT GRID (SINGLE COLUMN ON MOBILE) ============ */
.grid{
  display:grid;
  grid-template-columns:1fr;   /* single column = full width, no gaps */
  gap:12px;
  width:100%;
  max-width:100%;
}
@media (min-width:600px){
  .grid{grid-template-columns:repeat(2,1fr);gap:14px}
}
@media (min-width:1024px){
  .grid{grid-template-columns:repeat(3,1fr)}
}

.prod-card{
  overflow:hidden;
  transition:.25s;
  border-radius:var(--radius-lg);
  border:1px solid var(--border-soft);
  background:var(--card);
  display:flex;
  flex-direction:column;
  max-width:100%;
  min-width:0;
  position:relative;
}
.prod-card:active{transform:scale(.99)}
.prod-card:hover{border-color:var(--primary);box-shadow:0 12px 28px rgba(124,58,237,.18)}

/* === PRODUCT IMAGE — full image visible, NEVER cropped === */
.prod-img{
  width:100%;
  aspect-ratio:16/9;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:56px;
  background:
    linear-gradient(135deg,#0a0f1c 0%,#1a2138 100%);
  position:relative;
  overflow:hidden;
  padding:12px;
}
.prod-img::before{
  content:'';
  position:absolute;inset:0;
  background:
    radial-gradient(circle at 30% 30%,rgba(124,58,237,.15),transparent 60%),
    radial-gradient(circle at 70% 70%,rgba(236,72,153,.1),transparent 60%);
  pointer-events:none;
}
.prod-img img{
  width:100%;
  height:100%;
  object-fit:contain;            /* FULL image, never crops */
  object-position:center;
  border-radius:6px;
  transition:transform .3s;
  position:relative;
  z-index:1;
  background:transparent;
}
.prod-card:hover .prod-img img{transform:scale(1.05)}
.prod-img-fallback{
  font-size:56px;
  z-index:1;
  position:relative;
  filter:drop-shadow(0 4px 12px rgba(124,58,237,.4));
}
.badge-sale{
  position:absolute;top:10px;right:10px;
  font-size:10px;font-weight:800;
  padding:4px 10px;border-radius:var(--radius-full);
  background:var(--grad-danger);color:#fff;
  box-shadow:0 2px 8px rgba(239,68,68,.4);z-index:2;
}
.badge-antiban{
  position:absolute;top:10px;left:10px;
  font-size:9px;font-weight:800;
  padding:4px 9px;border-radius:var(--radius-full);
  background:var(--grad-success);color:#fff;
  box-shadow:0 2px 8px rgba(16,185,129,.4);z-index:2;
  display:flex;align-items:center;gap:3px;
}

.prod-body{padding:14px;display:flex;flex-direction:column;flex:1;min-width:0}
.prod-name{
  font-weight:800;
  font-size:clamp(14px,4vw,16px);
  margin-bottom:4px;line-height:1.3;
  display:-webkit-box;-webkit-line-clamp:2;line-clamp:2;-webkit-box-orient:vertical;
  overflow:hidden;word-break:break-word;overflow-wrap:anywhere;
}
.prod-desc{
  font-size:clamp(11px,3vw,12px);
  color:var(--text-mid);
  display:-webkit-box;-webkit-line-clamp:2;line-clamp:2;-webkit-box-orient:vertical;
  overflow:hidden;min-height:32px;margin-bottom:10px;
  word-break:break-word;overflow-wrap:anywhere;
}
.price-row{display:flex;align-items:center;gap:8px;margin-bottom:12px;flex-wrap:wrap}
.price{font-family:'Orbitron',sans-serif;font-size:clamp(16px,4.5vw,19px);font-weight:800;color:var(--success)}
.old-price{font-size:12px;color:var(--muted);text-decoration:line-through}
.prod-btns{display:flex;gap:8px;margin-top:auto;width:100%}
.btn-prod{
  flex:1;padding:12px 6px;border-radius:var(--radius-md);
  font-size:clamp(11px,3vw,12px);font-weight:700;text-align:center;
  transition:.2s;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;
  display:flex;align-items:center;justify-content:center;gap:4px;
  min-width:0;min-height:46px;cursor:pointer;border:none;font-family:inherit;
}
.btn-prod:active{transform:scale(.97)}
.btn-prod svg{width:14px;height:14px;flex-shrink:0}
.btn-setup{background:var(--card-3);color:var(--text);border:1px solid var(--border)}
.btn-buy{background:var(--grad-primary);color:#fff;box-shadow:0 4px 12px var(--primary-glow)}

/* ============ LIST ITEMS ============ */
.list-item{
  display:flex;align-items:center;gap:12px;
  padding:14px;margin:0 0 8px;
  border-radius:var(--radius-md);
  background:var(--card);border:1px solid var(--border-soft);
  box-shadow:var(--shadow-xs);transition:.2s;
  width:100%;
}
.list-item:hover{box-shadow:var(--shadow-sm);border-color:rgba(124,58,237,.3)}
.list-icon{
  width:42px;height:42px;border-radius:var(--radius-md);
  display:flex;align-items:center;justify-content:center;
  font-size:20px;background:var(--card-2);flex-shrink:0;
}
.list-body{flex:1;min-width:0;overflow:hidden}
.list-title{font-weight:700;font-size:14px;word-wrap:break-word;overflow-wrap:anywhere}
.list-sub{font-size:11px;color:var(--text-mid);margin-top:3px;word-wrap:break-word;overflow-wrap:anywhere}

/* ============ BADGES ============ */
.badge{font-size:11px;padding:3px 10px;border-radius:var(--radius-full);font-weight:700;display:inline-block;white-space:nowrap}
.badge-green{background:rgba(16,185,129,.12);color:var(--success);border:1px solid rgba(16,185,129,.25)}
.badge-amber{background:rgba(245,158,11,.12);color:var(--warning);border:1px solid rgba(245,158,11,.25)}
.badge-red{background:rgba(239,68,68,.12);color:var(--danger);border:1px solid rgba(239,68,68,.25)}
.badge-blue{background:rgba(59,130,246,.12);color:var(--info);border:1px solid rgba(59,130,246,.25)}
.badge-purple{background:rgba(124,58,237,.12);color:var(--primary-light);border:1px solid rgba(124,58,237,.25)}

/* ============ STATS ============ */
.stat-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;margin:0 0 14px;width:100%}
.stat{
  padding:16px 14px;border-radius:var(--radius-md);
  background:var(--card);border:1px solid var(--border-soft);
  box-shadow:var(--shadow-xs);position:relative;overflow:hidden;
}
.stat::before{content:'';position:absolute;top:0;left:0;width:4px;height:100%;background:var(--primary)}
.stat.green::before{background:var(--success)}
.stat.amber::before{background:var(--warning)}
.stat.blue::before{background:var(--info)}
.stat.pink::before{background:var(--accent)}
.stat-label{font-size:11px;text-transform:uppercase;color:var(--text-mid);font-weight:700;letter-spacing:.5px}
.stat-val{font-family:'Orbitron',sans-serif;font-size:clamp(18px,5vw,22px);font-weight:900;margin-top:5px;word-break:break-all}

/* ============ PAGE TITLE ============ */
.page-title{
  font-family:'Orbitron',sans-serif;
  font-size:clamp(20px,5.5vw,26px);
  font-weight:900;margin:0 0 14px;
  letter-spacing:-.5px;
  display:flex;align-items:center;gap:10px;
  word-break:break-word;overflow-wrap:anywhere;
}
.page-title .wallet-ic-lg{
  width:24px;height:24px;stroke:var(--primary);
  filter:drop-shadow(0 0 8px var(--primary-glow));flex-shrink:0;
}
.section-title{font-size:15px;font-weight:800;margin:18px 0 10px;display:flex;align-items:center;gap:8px}

/* ============ MODALS ============ */
.modal{
  position:fixed;inset:0;z-index:50;display:none;
  align-items:flex-end;justify-content:center;
  background:rgba(0,0,0,.8);backdrop-filter:blur(8px);
  padding:0;padding-top:max(0,var(--safe-top));
}
.modal.show{display:flex;animation:fadeIn .25s}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
.modal-card{
  background:var(--bg-soft);
  border:1px solid var(--border);
  border-radius:22px 22px 0 0;
  padding:20px 18px calc(20px + var(--safe-bottom));
  width:100%;max-width:520px;
  max-height:92vh;max-height:92dvh;
  overflow-y:auto;
  box-shadow:0 -20px 50px rgba(0,0,0,.6);
  position:relative;animation:slideUp .3s;
  -webkit-overflow-scrolling:touch;
}
@keyframes slideUp{from{transform:translateY(100%)}to{transform:translateY(0)}}
@media (min-width:600px){
  .modal{align-items:center;padding:16px}
  .modal-card{border-radius:22px;max-width:480px;animation:scaleIn .25s}
}
@keyframes scaleIn{from{transform:scale(.95);opacity:0}to{transform:scale(1);opacity:1}}
.modal-title{font-size:20px;font-weight:900;text-align:center;margin-bottom:16px;letter-spacing:-.3px;display:flex;align-items:center;justify-content:center;gap:8px}
.modal-close{
  position:absolute;top:14px;right:14px;color:var(--text-mid);
  font-size:18px;background:var(--card-2);
  width:34px;height:34px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  transition:.2s;flex-shrink:0;z-index:2;
}
.modal-close:active{transform:scale(.9);background:var(--border)}
.field{margin-bottom:14px}
.field label{font-size:12px;color:var(--text-mid);display:block;margin-bottom:6px;font-weight:700}
.field-hint{font-size:11px;color:var(--muted);margin-top:4px}

/* ============ PLAN GRID ============ */
.plan-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;margin:10px 0 14px;width:100%}
.plan{
  padding:14px 10px;border-radius:var(--radius-md);
  border:2px solid var(--border);background:var(--card-2);
  cursor:pointer;transition:.2s;text-align:center;min-height:72px;
}
.plan:active{transform:scale(.97)}
.plan.active{border-color:var(--primary);background:rgba(124,58,237,.1);box-shadow:0 0 15px var(--primary-glow)}
.plan.disabled{opacity:.45;cursor:not-allowed}
.plan-dur{font-size:clamp(12px,3.2vw,14px);font-weight:800}
.plan-price{font-family:'Orbitron',sans-serif;font-size:clamp(15px,4vw,18px);font-weight:900;color:var(--success);margin-top:4px}
.plan-stock{font-size:10px;color:var(--text-mid);margin-top:4px;font-weight:600}

/* ============ BILLS / KEYS ============ */
.bkash-box{padding:14px;border-radius:var(--radius-md);background:rgba(226,19,110,.06);border:2px dashed var(--bkash);margin-top:14px}
.bkash-num-row{display:flex;align-items:center;justify-content:space-between;gap:8px;margin-top:8px;background:var(--card-2);padding:10px 14px;border-radius:var(--radius-md);flex-wrap:wrap}
.bkash-num{font-family:monospace;font-size:clamp(15px,4.2vw,18px);font-weight:800;color:var(--bkash);letter-spacing:1px;word-break:break-all}
.btn-copy{padding:8px 12px;border-radius:var(--radius-md);font-size:12px;font-weight:700;background:var(--bkash);color:#fff;box-shadow:0 4px 10px rgba(226,19,110,.25);transition:.2s;white-space:nowrap;min-height:36px;cursor:pointer;border:none}
.btn-copy:active{transform:scale(.96)}

.key-box{margin-top:12px;padding:14px;border-radius:var(--radius-md);background:rgba(16,185,129,.06);border:1.5px solid rgba(16,185,129,.3);width:100%}
.key-box-head{display:flex;align-items:center;gap:6px;font-size:11px;font-weight:900;color:var(--success);text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px}
.key-content{font-family:monospace;font-size:13px;white-space:pre-wrap;word-break:break-all;background:#000;padding:12px;border-radius:var(--radius-md);border:1px solid var(--border);line-height:1.7;max-height:200px;overflow-y:auto;color:#0f0}
.key-copy-row{display:flex;gap:8px;margin-top:10px}
.key-copy-btn{flex:1;padding:11px;border-radius:var(--radius-md);font-size:12px;font-weight:700;background:var(--grad-success);color:#fff;transition:.2s;min-height:44px;cursor:pointer;border:none;display:inline-flex;align-items:center;justify-content:center;gap:6px}
.key-copy-btn:active{transform:scale(.97)}

/* ============ TOAST ============ */
.toast{
  position:fixed;top:max(70px,calc(var(--safe-top) + 10px));left:50%;
  transform:translateX(-50%);
  background:var(--text);color:var(--bg);
  padding:12px 22px;border-radius:var(--radius-full);
  z-index:100;animation:slideDown .3s;font-weight:600;font-size:13px;
  box-shadow:var(--shadow-md);max-width:90vw;text-align:center;
}
@keyframes slideDown{from{opacity:0;transform:translate(-50%,-20px)}to{opacity:1;transform:translate(-50%,0)}}

/* ============ EMPTY STATE ============ */
.empty{text-align:center;padding:48px 20px;color:var(--text-mid);display:flex;flex-direction:column;align-items:center}
.empty-icon{font-size:56px;margin-bottom:14px;opacity:.6}

/* ============ NOTIFICATIONS / OFFERS ============ */
.notif{padding:10px 14px;font-size:12px;font-weight:500;background:var(--grad-danger);color:#fff;overflow:hidden;margin:0 0 10px;border-radius:var(--radius-md);box-shadow:0 4px 12px rgba(239,68,68,.2);width:100%}
.marquee{white-space:nowrap;animation:marquee 22s linear infinite}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
.offer-bar{margin:0 0 10px;border-radius:var(--radius-md);overflow:hidden;background:linear-gradient(90deg,#7c3aed,#ec4899,#7c3aed);background-size:200% 100%;animation:offerGradient 4s linear infinite;box-shadow:var(--shadow-neon);width:100%}
@keyframes offerGradient{0%{background-position:0% 50%}100%{background-position:200% 50%}}
.offer-inner{display:flex;align-items:center;gap:8px;padding:10px 14px;color:#fff;font-size:13px;font-weight:600}
.offer-marquee{overflow:hidden;flex:1;white-space:nowrap}
.offer-marquee span{display:inline-block;padding-left:100%;animation:offerScroll 18s linear infinite}
@keyframes offerScroll{0%{transform:translateX(0)}100%{transform:translateX(-100%)}}

/* ============ LIVE FEED ============ */
.live-feed{margin:0 0 14px}
.live-feed-head{display:flex;align-items:center;gap:8px;margin-bottom:8px}
.live-dot{width:10px;height:10px;border-radius:50%;background:var(--success);animation:blink 1.5s infinite;box-shadow:0 0 10px rgba(16,185,129,.6)}
.live-feed-title{font-size:14px;font-weight:800}
.live-item{display:flex;align-items:center;gap:10px;padding:10px 12px;border-radius:var(--radius-md);background:var(--card);border:1px solid var(--border-soft);box-shadow:var(--shadow-xs);font-size:13px;margin:0 0 6px}
.live-avatar{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:800;color:#fff;font-size:11px;flex-shrink:0}
.live-body{flex:1;min-width:0}
.live-text{font-size:clamp(11px,3vw,12px);line-height:1.4;color:var(--text-mid);word-break:break-word;overflow-wrap:anywhere}
.live-text strong{color:var(--text);font-weight:700}
.live-time{font-size:10px;color:var(--muted);margin-top:2px}

/* ============ SOCIAL BAR ============ */
.social-bar{display:flex;gap:8px;margin:18px 0 8px;width:100%}
.social-bar a{flex:1;padding:13px;border-radius:var(--radius-md);font-size:13px;font-weight:700;color:#fff;display:flex;align-items:center;justify-content:center;gap:8px;box-shadow:var(--shadow-sm);transition:.2s;min-height:48px}
.social-bar a:active{transform:scale(.97)}
.social-bar .tg{background:linear-gradient(135deg,#26a5e4,#1a8ec7)}
.social-bar .yt{background:linear-gradient(135deg,#ff0000,#cc0000)}

/* ============ WELCOME MODAL ============ */
.welcome-modal{position:fixed;inset:0;z-index:60;display:none;align-items:flex-end;justify-content:center;background:rgba(0,0,0,.85);backdrop-filter:blur(8px);padding:0}
.welcome-modal.show{display:flex;animation:fadeIn .3s}
.welcome-card{background:var(--bg-soft);border:1px solid var(--border);border-radius:22px 22px 0 0;padding:0;width:100%;max-width:480px;overflow:hidden;box-shadow:0 -20px 50px rgba(0,0,0,.7);position:relative;animation:slideUp .35s;max-height:92dvh;overflow-y:auto}
@media (min-width:600px){
  .welcome-modal{align-items:center;padding:16px}
  .welcome-card{border-radius:22px;max-width:440px;animation:scaleIn .3s}
}
.welcome-img{width:100%;aspect-ratio:16/9;object-fit:cover;display:block;background:var(--bg)}
.welcome-body{padding:18px}
.welcome-text{font-size:14px;color:var(--text-mid);line-height:1.6;text-align:center;margin-bottom:14px}
.welcome-btn{display:flex;align-items:center;justify-content:center;gap:8px;width:100%;padding:14px;border-radius:var(--radius-md);background:var(--grad-primary);color:#fff;font-weight:700;font-size:15px;text-decoration:none;margin-bottom:8px;box-shadow:var(--shadow-neon);min-height:48px}
.welcome-close{width:100%;padding:12px;border-radius:var(--radius-md);background:var(--card-2);color:var(--text-mid);font-weight:700;font-size:13px;min-height:44px;border:none;cursor:pointer}

/* ============ WHATSAPP FAB ============ */
.whatsapp-fab{
  position:fixed;
  bottom:calc(88px + var(--safe-bottom));
  right:12px;
  width:52px;height:52px;
  border-radius:50%;
  background:linear-gradient(135deg,#25D366,#128C7E);
  color:#fff;
  display:flex;align-items:center;justify-content:center;
  box-shadow:0 6px 20px rgba(37,211,102,.45);
  z-index:45;transition:transform .15s;
}
.whatsapp-fab svg{width:28px;height:28px}
.whatsapp-fab:active{transform:scale(.92)}

/* ============ BOTTOM NAVIGATION ============ */
nav.botnav{
  position:fixed;
  bottom:calc(10px + var(--safe-bottom));
  left:8px;right:8px;
  width:calc(100% - 16px);
  background:rgba(22,28,46,.92);
  backdrop-filter:blur(24px) saturate(180%);
  -webkit-backdrop-filter:blur(24px) saturate(180%);
  border:1px solid rgba(255,255,255,.08);
  border-radius:30px;
  box-shadow:0 10px 30px rgba(0,0,0,.5),inset 0 1px 0 rgba(255,255,255,.08);
  z-index:45;
}
@media (min-width:768px){
  nav.botnav{left:50%;right:auto;transform:translateX(-50%);width:480px}
}
.botnav-in{display:grid;grid-template-columns:repeat(5,1fr);height:62px;align-items:center;padding:0 6px;position:relative}
.navbtn{
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  gap:3px;font-size:clamp(9px,2.6vw,10px);color:var(--text-mid);
  transition:.25s;font-weight:600;height:100%;position:relative;
  background:none;border:none;cursor:pointer;min-height:44px;
}
.navbtn.active{color:var(--primary)}
.navbtn.active svg{stroke:var(--primary);filter:drop-shadow(0 0 5px var(--primary-glow))}
.navbtn svg{width:21px;height:21px;transition:.25s}
.navbtn:active{transform:scale(.92)}

.navbtn-wallet-wrap{position:relative;display:flex;flex-direction:column;align-items:center;justify-content:center;height:100%;width:100%;cursor:pointer}
.navbtn-wallet-circle{
  position:absolute;top:-22px;
  width:52px;height:52px;border-radius:50%;
  background:var(--grad-success);color:#fff;
  display:flex;align-items:center;justify-content:center;
  box-shadow:0 6px 18px rgba(16,185,129,.5),inset 0 2px 0 rgba(255,255,255,.3);
  border:3px solid var(--bg);
  transition:transform .2s;
}
.navbtn-wallet-circle:active{transform:scale(.92)}
.navbtn-wallet-circle svg{width:24px;height:24px;stroke-width:2.2}
.navbtn-wallet-label{margin-top:32px;font-size:9px;color:var(--success);font-weight:700;letter-spacing:.3px}

/* ============ ADMIN PANEL ============ */
.admin-tab-bar{
  display:flex;gap:6px;margin:0 0 12px;overflow-x:auto;
  scrollbar-width:none;padding-bottom:2px;
}
.admin-tab-bar::-webkit-scrollbar{display:none}
.admin-tab{
  padding:8px 14px;border-radius:var(--radius-md);
  font-size:12px;font-weight:700;background:var(--card);
  border:1.5px solid var(--border-soft);color:var(--text-mid);
  flex-shrink:0;white-space:nowrap;cursor:pointer;min-height:38px;
  display:inline-flex;align-items:center;gap:4px;
}
.admin-tab.active{background:var(--grad-primary);color:#fff;border-color:transparent;box-shadow:0 4px 12px var(--primary-glow)}

.admin-card{
  background:var(--card);border:1px solid var(--border-soft);
  border-radius:var(--radius-md);padding:14px;margin:0 0 10px;width:100%;
}
.admin-card-title{font-size:13px;font-weight:800;margin-bottom:10px;color:var(--primary-light);display:flex;align-items:center;gap:6px}

.product-mgmt-item{
  display:flex;gap:10px;padding:12px;border-radius:var(--radius-md);
  background:var(--card-2);border:1px solid var(--border-soft);
  margin-bottom:8px;align-items:flex-start;
}
.product-mgmt-thumb{
  width:60px;height:60px;border-radius:var(--radius-md);
  background:var(--card-3);display:flex;align-items:center;justify-content:center;
  font-size:28px;flex-shrink:0;overflow:hidden;
}
.product-mgmt-thumb img{width:100%;height:100%;object-fit:contain}

.switch{position:relative;display:inline-block;width:46px;height:26px;flex-shrink:0}
.switch input{opacity:0;width:0;height:0}
.slider{position:absolute;cursor:pointer;inset:0;background:var(--card-3);border-radius:26px;transition:.3s}
.slider::before{content:'';position:absolute;height:20px;width:20px;left:3px;bottom:3px;background:#fff;border-radius:50%;transition:.3s}
input:checked + .slider{background:var(--success)}
input:checked + .slider::before{transform:translateX(20px)}

/* ============ RESPONSIVE ============ */
@media (max-width:380px){
  .header-in{padding:8px 10px;gap:6px}
  .balance-chip{padding:6px 10px;font-size:11px}
  .logo-name{font-size:13px}
  .stat-grid{gap:8px}
  .stat{padding:14px 12px}
}
@media (max-width:340px){
  .social-bar{flex-direction:column}
  .logo-name{display:none}
}
@media (max-width:320px){
  .container{padding:10px 8px}
  .header-in{padding:8px}
  .balance-chip{padding:5px 8px}
  .navbtn{font-size:9px}
  .navbtn svg{width:19px;height:19px}
}
@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{animation-duration:.01ms!important;animation-iteration-count:1!important;transition-duration:.01ms!important}
}
</style>
</head>
<body>

<header>
  <div class="header-in">
    <div class="logo" onclick="handleLogoClick()">
      <div class="logo-badge" id="logoBadge">PB</div>
      <span class="logo-name" id="siteName">PANEL BAJAR</span>
    </div>
    <div class="header-right" id="headerRight"></div>
  </div>
</header>

<main><div class="container" id="main"></div></main>

<nav class="botnav">
  <div class="botnav-in">
    <button class="navbtn" data-page="home" onclick="nav('home')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M3 12l9-9 9 9M5 10v10h14V10"/></svg>
      <span>হোম</span>
    </button>
    <button class="navbtn" data-page="orders" onclick="nav('orders')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01"/></svg>
      <span>অর্ডার</span>
    </button>
    <div class="navbtn-wallet-wrap" onclick="nav('wallet')">
      <div class="navbtn-wallet-circle">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round"><path d="M21 12V7H5a2 2 0 0 1 0-4h14v4"/><path d="M3 5v14a2 2 0 0 0 2 2h16v-5"/><path d="M18 12a2 2 0 0 0 0 4h4v-4Z"/></svg>
      </div>
      <span class="navbtn-wallet-label">ADD FUND</span>
    </div>
    <button class="navbtn" data-page="keys" onclick="nav('keys')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" d="M15 7a2 2 0 012 2m4 0a6 6 0 01-7.743 5.743L11 17H9v2H7v2H4a1 1 0 01-1-1v-2.586a1 1 0 01.293-.707l5.964-5.964A6 6 0 1121 9z"/></svg>
      <span>কীস</span>
    </button>
    <button class="navbtn" data-page="account" onclick="nav('account')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path stroke-linecap="round" stroke-linejoin="round" d="M4 21c0-4 4-7 8-7s8 3 8 7"/></svg>
      <span>একাউন্ট</span>
    </button>
  </div>
</nav>

<div class="modal" id="modal" onclick="if(event.target===this)closeModal()"><div class="modal-card" id="modalContent"></div></div>
<div class="modal" id="authModal" onclick="if(event.target===this)closeAuth()"><div class="modal-card" id="authContent"></div></div>
<div class="welcome-modal" id="welcomeModal" onclick="if(event.target===this)closeWelcome()"><div class="welcome-card" id="welcomeContent"></div></div>

<a href="#" id="whatsappFab" class="whatsapp-fab" target="_blank" aria-label="WhatsApp">
  <svg viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51l-.57-.01c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.885 3.488"/></svg>
</a>

<script>
/* ============================================================
   FIREBASE CONFIG  (already configured for your project)
   ============================================================ */
var FIREBASE_CONFIG = {
  apiKey: "AIzaSyDt3gU-2iubzCZ94XFAGZswUnzxuDgUvFQ",
  authDomain: "free-fire-panel-611d6.firebaseapp.com",
  projectId: "free-fire-panel-611d6",
  storageBucket: "free-fire-panel-611d6.firebasestorage.app",
  messagingSenderId: "374641641780",
  appId: "1:374641641780:web:c87d374edf2371dae47d61"
};

/* TELEGRAM BOT CONFIG (your bot token + chat id) */
var TELEGRAM_CONFIG = {
  botToken: "8842406650:AAESk-VLFq7qwOT2i14SuRAqWDIhNkQ7GNc",
  chatId: "7427334644"
};
</script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>
<script>
/* ============================================================
   PANEL BAJAR — Complete App Logic
   Features: User Panel + Admin Panel + Firebase + Telegram
   ============================================================ */

let fbDb=null, fbConnected=false, fbSyncStarted=false;
function initFirebase(){
  try{
    if(typeof firebase==='undefined'||fbConnected) return fbConnected;
    if(!firebase.apps.length) firebase.initializeApp(FIREBASE_CONFIG);
    fbDb=firebase.firestore(); fbConnected=true; return true;
  }catch(e){ console.warn('Firebase init failed:',e); return false; }
}
function fbDoc(col){ return fbDb.collection(col).doc('main'); }
function fbSave(col, arr){ if(!fbConnected) return; try{ fbDoc(col).set({data:JSON.stringify(arr), updatedAt:new Date().toISOString()}).catch(e=>console.warn(e)); }catch(e){} }
function fbLoad(col, cb){ if(!fbConnected){ cb&&cb(null); return; } try{ fbDoc(col).get().then(doc=>{ if(doc.exists){ try{ cb&&cb(JSON.parse(doc.data().data||'[]')); }catch(e){ cb&&cb(null); } } else cb&&cb(null); }).catch(()=>cb&&cb(null)); }catch(e){ cb&&cb(null); } }
function fbListen(col, cb){ if(!fbConnected) return; try{ fbDoc(col).onSnapshot(doc=>{ if(doc.exists){ try{ cb&&cb(JSON.parse(doc.data().data||'[]')); }catch(e){} } }); }catch(e){} }

const DEFAULT_SETTINGS = {
  site_name:'PANEL BAJAR', tagline:'Buy Premium Mods & Hacks',
  notification:'স্বাগতম! Panel Bajar-এ প্রিমিয়াম mods কিনুন।', notif_active:true,
  offer_text:'🔥 MEGA OFFER! সব প্রোডাক্টে ৫০% ছাড়!', offer_active:true,
  telegram:'https://t.me/panelbajar', youtube:'https://youtube.com/@panelbajar',
  bkash_number:'01XXXXXXXXX', help_url:'https://t.me/panelbajar',
  ads:[], ad_delay:3500, is_online:true, logo_url:'#', logo_image:'',
  online_start:'00:00', online_end:'23:59', whatsapp_number:'8801700000000',
  welcome_active:false, welcome_image:'', welcome_text:'', welcome_link:'',
  telegram_bot_token:'', telegram_chat_id:'',
  auto_delivery:true, auto_approve:true, low_stock_threshold:5
};

let state = {
  user: JSON.parse(localStorage.getItem('pb_user')||'null'),
  users: JSON.parse(localStorage.getItem('pb_users')||'[]'),
  products: JSON.parse(localStorage.getItem('pb_products')||'[]'),
  orders: JSON.parse(localStorage.getItem('pb_orders')||'[]'),
  deposits: JSON.parse(localStorage.getItem('pb_deposits')||'[]'),
  transactions: JSON.parse(localStorage.getItem('pb_transactions')||'[]'),
  settings: {...DEFAULT_SETTINGS, ...JSON.parse(localStorage.getItem('pb_settings')||'{}')},
  page:'home', productTab:'NON_ROOT', authMode:'login',
  adminTab:'dashboard', adminProductEdit:null
};

function saveLocal(){
  try{
    localStorage.setItem('pb_user', JSON.stringify(state.user));
    localStorage.setItem('pb_users', JSON.stringify(state.users));
    localStorage.setItem('pb_products', JSON.stringify(state.products));
    localStorage.setItem('pb_orders', JSON.stringify(state.orders));
    localStorage.setItem('pb_deposits', JSON.stringify(state.deposits));
    localStorage.setItem('pb_transactions', JSON.stringify(state.transactions));
    localStorage.setItem('pb_settings', JSON.stringify(state.settings));
  }catch(e){}
}
function pushCol(col){
  const map={users:state.users,products:state.products,orders:state.orders,deposits:state.deposits,transactions:state.transactions,settings:[state.settings]};
  if(!map[col]) return;
  saveLocal(); fbSave(col, map[col]);
}
function uid(){ return Date.now().toString(36)+Math.random().toString(36).slice(2,6); }
function $(id){ return document.getElementById(id); }
function esc(s){ return String(s==null?'':s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])); }
function fmt(n){ return '৳'+Number(n||0).toLocaleString('en-IN'); }
function tAgo(d){ try{ return new Date(d).toLocaleString('bn-BD'); }catch(e){ return ''; } }
function timeAgoShort(d){
  const diff=Date.now()-new Date(d).getTime();
  const m=Math.floor(diff/60000);
  if(m<1) return 'এইমাত্র';
  if(m<60) return m+' মিনিট আগে';
  const h=Math.floor(m/60);
  if(h<24) return h+' ঘন্টা আগে';
  return Math.floor(h/24)+' দিন আগে';
}
function toast(m){ const t=document.createElement('div'); t.className='toast'; t.textContent=m; document.body.appendChild(t); setTimeout(()=>t.remove(),2800); }
function copyText(t){ if(navigator.clipboard){ navigator.clipboard.writeText(t).then(()=>toast('✓ কপি হয়েছে')).catch(()=>fallbackCopy(t)); } else fallbackCopy(t); }
function fallbackCopy(t){ const ta=document.createElement('textarea'); ta.value=t; ta.style.position='fixed'; ta.style.opacity='0'; document.body.appendChild(ta); ta.select(); try{ document.execCommand('copy'); toast('✓ কপি হয়েছে'); }catch(e){} document.body.removeChild(ta); }

/* Wallet SVG icons (replace emoji everywhere) */
const WALLET_SVG_SM = '<svg class="wallet-ic" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 12V7H5a2 2 0 0 1 0-4h14v4"/><path d="M3 5v14a2 2 0 0 0 2 2h16v-5"/><path d="M18 12a2 2 0 0 0 0 4h4v-4Z"/></svg>';
const WALLET_SVG_LG = '<svg class="wallet-ic-lg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 12V7H5a2 2 0 0 1 0-4h14v4"/><path d="M3 5v14a2 2 0 0 0 2 2h16v-5"/><path d="M18 12a2 2 0 0 0 0 4h4v-4Z"/></svg>';

/* === Telegram notifications === */
function tgToken(){ return (TELEGRAM_CONFIG.botToken && TELEGRAM_CONFIG.botToken!=='YOUR_BOT_TOKEN_HERE') ? TELEGRAM_CONFIG.botToken : state.settings.telegram_bot_token; }
function tgChat(){ return (TELEGRAM_CONFIG.chatId && TELEGRAM_CONFIG.chatId!=='YOUR_CHAT_ID_HERE') ? TELEGRAM_CONFIG.chatId : state.settings.telegram_chat_id; }
function sendTg(msg){
  const token=tgToken(), chat=tgChat();
  if(!token||!chat) return;
  fetch(`https://api.telegram.org/bot${token}/sendMessage`,{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({chat_id:chat,text:msg,parse_mode:'HTML'})}).catch(e=>console.warn(e));
}
function notifyOrder(order, product, keyContent){
  const e = order.status==='COMPLETED'?'✅':'⏳';
  const k = keyContent?`\n\n🔑 <b>Keys:</b>\n<pre>${esc(keyContent)}</pre>`:'\n\n⚠️ <b>Key stock empty!</b>';
  sendTg(`${e} <b>New Order — ${order.status}</b>\n\n📦 <b>Product:</b> ${product?product.name:'Unknown'}\n⏱ <b>Plan:</b> ${order.planDur}\n💰 <b>Amount:</b> ${fmt(order.price)}\n🔢 <b>Qty:</b> ${order.qty}\n🆔 <b>Txn:</b> <code>${order.txnId}</code>\n\n👤 <b>User:</b> ${order.username||state.user?.username}\n📧 <b>Email:</b> ${order.email||state.user?.email}${k}`);
}
function notifyDeposit(dep){
  sendTg(`💰 <b>New Add Balance Request</b>\n\n👤 <b>User:</b> ${esc(dep.username)}\n📧 <b>Email:</b> ${esc(dep.email)}\n💵 <b>Amount:</b> ${fmt(dep.amount)}\n🆔 <b>TxnID:</b> <code>${esc(dep.txnId)}</code>\n${dep.note?`\n📝 <b>Note:</b> ${esc(dep.note)}`:''}\n\n⏳ Approve from Admin Panel.`);
}
function notifyLowStock(name, dur, rem){
  sendTg(`⚠️ <b>Low Stock Alert</b>\n\n📦 <b>Product:</b> ${name}\n⏱ <b>Plan:</b> ${dur}\n🔑 <b>Remaining:</b> ${rem}\n\n⚡ Refill keys from admin panel.`);
}

/* === Balance / Transaction === */
function getBalance(userId){ const u=state.users.find(x=>x.id===userId); return u?Number(u.balance||0):0; }
function addBalance(userId, amount, meta){
  const u=state.users.find(x=>x.id===userId);
  if(!u) return false;
  u.balance = Number(u.balance||0) + Number(amount||0);
  state.transactions.push({id:uid(),userId,type:meta.type||(amount>0?'credit':'debit'),amount:Number(amount),balanceAfter:u.balance,description:meta.description||'',refId:meta.refId||'',createdAt:new Date().toISOString()});
  if(state.user && state.user.id===userId){ state.user=u; localStorage.setItem('pb_user',JSON.stringify(state.user)); }
  pushCol('users'); pushCol('transactions');
  return true;
}

/* === Keys management === */
function getAvailableKeys(product, planDur){
  if(!product) return [];
  if(planDur && Array.isArray(product.plans)){
    const plan=product.plans.find(p=>p.dur===planDur);
    if(plan && Array.isArray(plan.keys)) return plan.keys.filter(k=>{ if(!k) return false; if(typeof k==='string') return k.trim()!==''; if(typeof k==='object') return k.status!=='USED'&&(k.code||k.value); return false; });
    return [];
  }
  if(!Array.isArray(product.keys)) return [];
  return product.keys.filter(k=>{ if(!k) return false; if(typeof k==='string') return k.trim()!==''; if(typeof k==='object') return k.status!=='USED'&&(k.code||k.value); return false; });
}
function getKeyText(k){ if(typeof k==='string') return k.trim(); if(k&&typeof k==='object') return String(k.code||k.value||'').trim(); return ''; }
function reserveKeys(product, qty, planDur){
  const available=getAvailableKeys(product,planDur);
  if(available.length<qty) return null;
  const reserved=available.slice(0,qty);
  const texts=reserved.map(getKeyText).filter(Boolean);
  reserved.forEach(k=>{ if(typeof k==='object') k.status='USED'; });
  if(planDur && Array.isArray(product.plans)){
    const plan=product.plans.find(p=>p.dur===planDur);
    if(plan && Array.isArray(plan.keys)){ plan.keys=plan.keys.filter(k=>{ if(!k) return false; if(typeof k==='string') return !reserved.includes(k); if(typeof k==='object') return k.status!=='USED'; return true; }); }
  } else if(Array.isArray(product.keys)){
    product.keys=product.keys.filter(k=>{ if(!k) return false; if(typeof k==='string') return !reserved.includes(k); if(typeof k==='object') return k.status!=='USED'; return true; });
  }
  return texts;
}

function isStoreOnline(){
  const s=state.settings;
  if(s.is_online===false) return false;
  if(!s.online_start||!s.online_end) return true;
  const now=new Date(); const cur=now.getHours()*60+now.getMinutes();
  const [sh,sm]=s.online_start.split(':').map(Number); const [eh,em]=s.online_end.split(':').map(Number);
  const start=sh*60+sm, end=eh*60+em;
  if(start<=end) return cur>=start && cur<=end;
  return cur>=start || cur<=end;
}
function handleLogoClick(){ const url=state.settings.logo_url; if(url && url!=='#' && url.trim()!=='') window.open(url,'_blank'); }
function isAdmin(){ return state.user && state.user.role==='ADMIN'; }

/* === Welcome Modal === */
function showWelcomeIfNeeded(){
  const s=state.settings;
  if(!s.welcome_active) return;
  if(sessionStorage.getItem('pb_welcome_shown')==='1') return;
  if(!s.welcome_image && !s.welcome_text && !s.welcome_link) return;
  const html=`
    <button class="modal-close" style="position:absolute;top:12px;right:12px;z-index:10;background:rgba(22,28,46,.92);width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:16px;color:#fff" onclick="closeWelcome()">✕</button>
    ${s.welcome_image?`<img src="${esc(s.welcome_image)}" class="welcome-img" alt="Welcome" onerror="this.style.display='none'">`:''}
    <div class="welcome-body">
      ${s.welcome_text?`<div class="welcome-text">${esc(s.welcome_text)}</div>`:''}
      ${s.welcome_link?`<a href="${esc(s.welcome_link)}" target="_blank" class="welcome-btn">▶️ ভিডিও দেখুন</a>`:''}
      <button class="welcome-close" onclick="closeWelcome()">বন্ধ করুন</button>
    </div>`;
  $('welcomeContent').innerHTML=html;
  $('welcomeModal').classList.add('show');
  sessionStorage.setItem('pb_welcome_shown','1');
}
function closeWelcome(){ $('welcomeModal').classList.remove('show'); }

/* === AUTH === */
function openAuth(mode){ state.authMode=mode||'login'; renderAuth(); $('authModal').classList.add('show'); }
function closeAuth(){ $('authModal').classList.remove('show'); }
function toggleAuthMode(){ state.authMode = state.authMode==='login'?'register':'login'; renderAuth(); }
function renderAuth(){
  const isL=state.authMode==='login';
  $('authContent').innerHTML=`
    <button class="modal-close" onclick="closeAuth()">✕</button>
    <h2 class="modal-title">${isL?'🔐 লগইন':'✨ রেজিস্টার'}</h2>
    <div class="field" style="display:${isL?'none':'block'}"><label>ইউজারনেম</label><input id="authUsername" placeholder="আপনার নাম" /></div>
    <div class="field"><label>ইমেইল</label><input id="authEmail" type="email" placeholder="email@example.com" /></div>
    <div class="field"><label>পাসওয়ার্ড</label><input id="authPassword" type="password" placeholder="••••••••" onkeydown="if(event.key==='Enter')doAuth()" /></div>
    <button class="btn btn-primary btn-full" onclick="doAuth()">${isL?'লগইন করুন':'রেজিস্টার করুন'}</button>
    <p class="auth-toggle" style="text-align:center;font-size:13px;color:var(--text-mid);margin-top:14px">${isL?'অ্যাকাউন্ট নেই?':'ইতিমধ্যে আছে?'} <button onclick="toggleAuthMode()" style="color:var(--primary);font-weight:700;background:none;border:none;cursor:pointer;padding:4px">${isL?'রেজিস্টার':'লগইন'}</button></p>`;
}
function doAuth(){
  const e=($('authEmail').value||'').trim().toLowerCase(); const p=$('authPassword').value;
  if(!e||!p){ toast('সব ঘর পূরণ করুন'); return; }
  if(state.authMode==='register'){
    const u=($('authUsername').value||'').trim();
    if(!u){ toast('ইউজারনেম দিন'); return; }
    if(state.users.find(x=>x.email===e)){ toast('এই ইমেইল ইতিমধ্যে ব্যবহৃত'); return; }
    const colors=['#ec4899','#7c3aed','#06b6d4','#f97316','#10b981','#e11d48','#3b82f6'];
    /* First user becomes ADMIN automatically */
    const isFirst = state.users.length===0;
    const nu={id:uid(),email:e,username:u,password:p,role:isFirst?'ADMIN':'USER',balance:0,totalOrders:0,totalSpent:0,banned:false,avatarColor:colors[Math.floor(Math.random()*colors.length)],createdAt:new Date().toISOString()};
    state.users.push(nu); state.user=nu; saveLocal(); pushCol('users'); closeAuth();
    toast(isFirst?'✓ অ্যাডমিন অ্যাকাউন্ট তৈরি!':'✓ অ্যাকাউন্ট তৈরি হয়েছে!'); render();
  } else {
    const u=state.users.find(x=>x.email===e);
    if(!u||u.password!==p){ toast('ইমেইল/পাসওয়ার্ড ভুল'); return; }
    if(u.banned){ toast('অ্যাকাউন্ট ব্যান করা'); return; }
    state.user=u; saveLocal(); closeAuth(); toast('স্বাগতম!'); render();
  }
}
function logout(){ state.user=null; state.page='home'; state.adminTab='dashboard'; saveLocal(); toast('লগআউট হয়েছে'); render(); }

function nav(p){
  if(!state.user && ['wallet','orders','account','keys','admin'].includes(p)){ openAuth('login'); return; }
  if(p==='admin' && !isAdmin()){ toast('অ্যাডমিন অ্যাক্সেস নেই'); return; }
  state.page=p; render();
}
function openModal(html){ $('modalContent').innerHTML=html; $('modal').classList.add('show'); }
function closeModal(){ $('modal').classList.remove('show'); }

/* === Live Feed === */
function generateLiveFeed(){
  const real=state.orders.slice().reverse().slice(0,6).map(o=>{
    const u=state.users.find(x=>x.id===o.userId); const p=state.products.find(x=>x.id===o.productId);
    return {user:u?.username||'User',color:u?.avatarColor||'#7c3aed',product:p?.name||'Product',icon:p?.icon||'🎮',time:o.createdAt,real:true};
  });
  const demoNames=[['Rahim','#ec4899'],['Karim','#7c3aed'],['Sadia','#06b6d4'],['Tanvir','#f97316'],['Nusrat','#10b981'],['Saimon','#e11d48'],['Alamin','#3b82f6']];
  const demoProducts=state.products.filter(p=>p.status==='ACTIVE');
  if(demoProducts.length===0) return real;
  const demo=[];
  for(let i=0;i<4;i++){
    const n=demoNames[Math.floor(Math.random()*demoNames.length)];
    const p=demoProducts[Math.floor(Math.random()*demoProducts.length)];
    demo.push({user:n[0],color:n[1],product:p.name,icon:p.icon,time:new Date(Date.now()-Math.floor(Math.random()*3600000)).toISOString(),real:false});
  }
  return [...real,...demo].sort((a,b)=>new Date(b.time)-new Date(a.time)).slice(0,7);
}
function renderLiveFeedItems(){
  const items=generateLiveFeed();
  if(items.length===0) return '<div style="text-align:center;padding:16px;color:var(--muted);font-size:12px">এখনো কোনো অর্ডার নেই</div>';
  return items.map(it=>`<div class="live-item"><div class="live-avatar" style="background:${esc(it.color)}">${esc(it.user.slice(0,2).toUpperCase())}</div><div class="live-body"><div class="live-text"><strong>${esc(it.user)}</strong> কিনেছেন ${esc(it.icon)} ${esc(it.product)}${it.real?' <span style="color:var(--success);font-size:10px">✓</span>':''}</div><div class="live-time">⏰ ${timeAgoShort(it.time)}</div></div></div>`).join('');
}
setInterval(()=>{ if(state.page==='home'){ const f=$('liveFeed'); if(f) f.innerHTML=renderLiveFeedItems(); } updateStatusBadge(); }, 4000);

function updateStatusBadge(){
  const hr=$('headerRight'); if(!hr) return;
  const online=isStoreOnline();
  const el=hr.querySelector('.status-badge');
  if(el){ el.className='status-badge '+(online?'online':'offline'); el.innerHTML='<span class="status-dot"></span> '+(online?'Online':'Offline'); }
}

/* === MAIN RENDER === */
function render(){
  $('siteName').textContent=state.settings.site_name||'Panel Bajar';
  const logo=$('logoBadge');
  if(state.settings.logo_image && state.settings.logo_image.trim()) logo.innerHTML=`<img src="${esc(state.settings.logo_image)}" onerror="this.style.display='none';this.parentElement.textContent='PB'">`;
  else logo.textContent=(state.settings.site_name||'PB').slice(0,2).toUpperCase();

  const hr=$('headerRight');
  const online=isStoreOnline();
  const statusHtml = online
    ? `<div class="status-badge online"><span class="status-dot"></span> Online</div>`
    : `<div class="status-badge offline"><span class="status-dot"></span> Offline</div>`;

  if(state.user){
    const fresh=state.users.find(x=>x.id===state.user.id)||state.user;
    const bal=Number(fresh.balance||0);
    hr.innerHTML = `<div class="balance-chip" onclick="nav('wallet')">${WALLET_SVG_SM}<span>${fmt(bal)}</span></div>${statusHtml}<button class="btn-avatar" style="background:${esc(state.user.avatarColor||'#7c3aed')}" onclick="nav('account')">${esc((state.user.username||'U').slice(0,2).toUpperCase())}</button>`;
  } else {
    hr.innerHTML = `${statusHtml}<button class="btn-login" onclick="openAuth('login')">লগইন</button>`;
  }

  document.querySelectorAll('.navbtn').forEach(b=>b.classList.toggle('active',b.dataset.page===state.page));

  const m=$('main');
  switch(state.page){
    case 'home': m.innerHTML=renderHome(); break;
    case 'wallet': m.innerHTML=renderWallet(); break;
    case 'account': m.innerHTML=renderAccount(); break;
    case 'orders': m.innerHTML=renderOrders(); break;
    case 'keys': m.innerHTML=renderKeys(); break;
    case 'admin': m.innerHTML=renderAdmin(); break;
    default: m.innerHTML=renderHome();
  }

  window.scrollTo(0,0);
  void document.body.offsetHeight;
  if(state.page==='home') startAdSlider();
  updateWhatsappLink();
}

/* === AD SLIDER === */
let adInterval=null, adIdx=0, adSlides=[], adTrack=null, adDrag=null;
function adApply(anim){ if(!adTrack) return; if(anim===false) adTrack.classList.add('no-anim'); else adTrack.classList.remove('no-anim'); adTrack.style.transform='translateX(-'+(adIdx*100)+'%)'; }
function adRestart(){ if(adInterval){clearInterval(adInterval); adInterval=null;} if(adSlides.length<=1) return; const delay=Math.max(1500,Number(state.settings.ad_delay)||3500); adInterval=setInterval(()=>goToAdSlide((adIdx+1)%adSlides.length),delay); }
function startAdSlider(){
  if(adInterval){clearInterval(adInterval); adInterval=null;}
  adTrack=document.querySelector('#adSlider .ad-track');
  adSlides=document.querySelectorAll('#adSlider .ad-slide');
  if(adSlides.length===0||!adTrack) return;
  if(adIdx>=adSlides.length) adIdx=0;
  adApply(false);
  requestAnimationFrame(()=>{ adApply(true); });
  document.querySelectorAll('.ad-dot').forEach((d,i)=>d.classList.toggle('active',i===adIdx));
  initAdSwipe(); adRestart();
}
function goToAdSlide(i){
  if(!adSlides.length||!adTrack) return;
  i=((i%adSlides.length)+adSlides.length)%adSlides.length; adIdx=i;
  adApply(true); document.querySelectorAll('.ad-dot').forEach((d,k)=>d.classList.toggle('active',k===i));
}
function initAdSwipe(){
  const slider=$('adSlider'); if(!slider||slider.dataset.swipeBound) return;
  slider.dataset.swipeBound='1';
  const down=e=>{ if(!adTrack) return; if(e.target&&e.target.closest&&e.target.closest('.ad-dot')) return; const p=e.touches?e.touches[0]:e; adDrag={startX:p.clientX,startY:p.clientY,dx:0,axis:null,w:slider.offsetWidth||1}; if(adSlides.length<=1) return; if(adInterval){clearInterval(adInterval); adInterval=null;} adTrack.classList.add('no-anim'); slider.classList.add('ad-dragging'); };
  const move=e=>{ if(!adDrag||adSlides.length<=1) return; const p=e.touches?e.touches[0]:e; const dx=p.clientX-adDrag.startX,dy=p.clientY-adDrag.startY; if(adDrag.axis===null&&(Math.abs(dx)>8||Math.abs(dy)>8)) adDrag.axis=Math.abs(dx)>Math.abs(dy)?'x':'y'; if(adDrag.axis!=='x') return; adDrag.dx=dx; if(e.cancelable) e.preventDefault(); adTrack.style.transform='translateX(calc(-'+(adIdx*100)+'% + '+dx+'px))'; };
  const up=()=>{ if(!adDrag) return; const d=adDrag; adDrag=null; slider.classList.remove('ad-dragging'); adTrack.classList.remove('no-anim'); if(d.axis==='x'&&Math.abs(d.dx)>(d.w*0.15)){ goToAdSlide(adIdx+(d.dx<0?1:-1)); } else adApply(true); adRestart(); };
  slider.addEventListener('touchstart',down,{passive:true}); slider.addEventListener('touchmove',move,{passive:false}); slider.addEventListener('touchend',up); slider.addEventListener('touchcancel',up);
}

/* === HOME PAGE === */
function renderHome(){
  const prods=state.products.filter(p=>p.status==='ACTIVE'&&p.category===state.productTab);
  const notif = state.settings.notif_active ? `<div class="notif"><div style="display:flex;align-items:center;gap:8px"><span>🔔</span><div style="overflow:hidden;flex:1"><div class="marquee">${esc(state.settings.notification)} &nbsp;&nbsp;&nbsp; ${esc(state.settings.notification)}</div></div></div></div>` : '';
  const offerBar = state.settings.offer_active && state.settings.offer_text ? `<div class="offer-bar"><div class="offer-inner"><span style="font-size:16px">🎁</span><div class="offer-marquee"><span>${esc(state.settings.offer_text)} &nbsp;&nbsp; 🎁 &nbsp;&nbsp; ${esc(state.settings.offer_text)}</span></div><span style="font-size:16px">🔥</span></div></div>` : '';

  const tabs=['NON_ROOT','ROOT','IPHONE','PC'].map(t=>`<button class="tab ${state.productTab===t?'active':''}" onclick="state.productTab='${t}';render()">${t==='NON_ROOT'?'🟢 NON ROOT':t==='ROOT'?'🔴 ROOT':t==='IPHONE'?'📱 IPHONE':'💻 PC'}</button>`).join('');

  let adHtml='';
  let rawAds=state.settings.ads||[];
  if(typeof rawAds==='string'){ try{ rawAds=JSON.parse(rawAds); }catch(e){ rawAds=[]; } }
  if(!Array.isArray(rawAds)) rawAds=[];
  let ads=rawAds.map(ad=>{ if(typeof ad==='string') return {url:ad.trim(),link:''}; if(ad&&typeof ad==='object') return {url:(ad.url||ad.image||'').trim(),link:(ad.link||'')}; return null; }).filter(ad=>ad&&ad.url!=='');

  if(ads.length>0){
    adHtml=`<div class="ad-slider" id="adSlider"><div class="ad-track">`;
    ads.forEach((ad,i)=>{ adHtml+=`<div class="ad-slide ${i===0?'active':''}"><img src="${esc(ad.url)}" alt="Ad ${i+1}" loading="${i===0?'eager':'lazy'}" onerror="this.onerror=null;this.style.display='none'"></div>`; });
    adHtml+=`</div><div class="ad-dots">`;
    ads.forEach((_,i)=>{ adHtml+=`<div class="ad-dot ${i===0?'active':''}" onclick="goToAdSlide(${i})"></div>`; });
    adHtml+=`</div></div>`;
  } else {
    adHtml=`<div class="ad-slider" id="adSlider"><div class="ad-track"><div class="ad-slide active" style="background:var(--grad-primary)"><div style="text-align:center;padding:20px;color:#fff;position:relative;z-index:2"><div style="font-size:52px;margin-bottom:8px">🎮</div><h1 style="font-size:clamp(20px,6vw,26px);font-weight:900;font-family:'Orbitron',sans-serif">${esc(state.settings.site_name)}</h1><p style="font-size:13px;opacity:.9;margin-top:6px">${esc(state.settings.tagline)}</p></div></div></div></div>`;
  }

  const socialBar=`<div class="social-bar"><a href="${esc(state.settings.telegram)}" target="_blank" class="tg">✈️ Telegram</a><a href="${esc(state.settings.youtube)}" target="_blank" class="yt">▶️ YouTube</a></div>`;

  return `${offerBar}${notif}${adHtml}
    <div class="live-feed">
      <div class="live-feed-head"><span class="live-dot"></span><div class="live-feed-title">🔴 লাইভ অর্ডার</div></div>
      <div id="liveFeed">${renderLiveFeedItems()}</div>
    </div>
    <div class="tabs">${tabs}</div>
    ${prods.length===0
      ? `<div class="card empty"><div class="empty-icon">🛍️</div><div style="font-weight:700;font-size:16px">কোনো প্রোডাক্ট নেই</div><div style="font-size:13px;margin-top:6px">এই ক্যাটেগরিতে এখনো প্রোডাক্ট নেই</div></div>`
      : `<div class="grid">${prods.map(p=>renderProductCard(p)).join('')}</div>`}
    ${socialBar}`;
}

function renderProductCard(p){
  const plans=p.plans||[];
  const validPrices=plans.filter(pl=>(pl.stock||0)>0).map(pl=>pl.price);
  const minPrice=validPrices.length?Math.min(...validPrices):(plans[0]?.price||0);
  const imgHtml = p.image
    ? `<img src="${esc(p.image)}" alt="${esc(p.name)}" onerror="this.style.display='none';this.parentElement.innerHTML='<div class=\\'prod-img-fallback\\'>${esc(p.icon||'🎮')}</div>'">`
    : `<div class="prod-img-fallback">${esc(p.icon||'🎮')}</div>`;
  return `<div class="card prod-card">
    <div class="prod-img">
      ${imgHtml}
      ${p.antiban?'<div class="badge-antiban">🛡️ ANTI BAN</div>':''}
      ${p.oldPrice?'<div class="badge-sale">SALE</div>':''}
    </div>
    <div class="prod-body">
      <div class="prod-name">${esc(p.name)}</div>
      <div class="prod-desc">${esc(p.description||'')}</div>
      <div class="price-row"><span class="price">${fmt(minPrice)}</span>${p.oldPrice?`<span class="old-price">${fmt(p.oldPrice)}</span>`:''}</div>
      <div class="prod-btns">
        <button class="btn-prod btn-setup" onclick="openFileSetup('${p.id}')">📁 SETUP</button>
        <button class="btn-prod btn-buy" onclick="openBuyNow('${p.id}')" ${p.maintenance?'disabled':''}>${p.maintenance?'OFF':'🛒 BUY'}</button>
      </div>
    </div>
  </div>`;
}

function openFileSetup(pid){
  const p=state.products.find(x=>x.id===pid); if(!p) return;
  const links=[];
  if(p.url_full_details) links.push({label:'📹 PANEL FULL DETAILS',url:p.url_full_details,cls:'btn-success'});
  if(p.url_setup_video) links.push({label:'🎬 SETUP VIDEO',url:p.url_setup_video,cls:'btn-danger'});
  if(p.url_download) links.push({label:'⬇️ DOWNLOAD',url:p.url_download,cls:'btn-primary'});
  if(p.url_iphone_setup) links.push({label:'📱 IPHONE SETUP',url:p.url_iphone_setup,cls:'btn-primary'});
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">📁 ${esc(p.name)}</h2>
    <p style="font-size:12px;color:var(--text-mid);text-align:center;margin-bottom:16px">নিচের বাটনে ক্লিক করুন</p>
    ${links.length===0?'<p style="text-align:center;color:var(--muted);padding:20px">এখনো কোনো লিংক নেই</p>':links.map(l=>`<a href="${esc(l.url)}" target="_blank" class="btn ${l.cls} btn-full" style="margin-bottom:8px">${l.label}</a>`).join('')}
    <button class="btn btn-ghost btn-full" style="margin-top:8px" onclick="closeModal()">বন্ধ করুন</button>`);
}

/* === BUY NOW === */
let selectedPlan=null, selectedQty=1, currentPlans=[], currentProduct=null;
function openBuyNow(pid){
  if(!isStoreOnline()){ toast('⚠️ এখন অফলাইন'); return; }
  const p=state.products.find(x=>x.id===pid); if(!p) return;
  if(!state.user){ openAuth('login'); return; }
  if(p.maintenance){ toast('প্রোডাক্ট মেইনটেন্যান্সে'); return; }
  selectedPlan=null; selectedQty=1; currentProduct=p;
  currentPlans=(p.plans&&p.plans.length>0)?p.plans:[{dur:'1 Day',price:p.price||0,stock:99}];
  const balance=getBalance(state.user.id);
  const plansHtml=currentPlans.map((pl,i)=>{
    const planKeys=getAvailableKeys(p, pl.dur).length;
    const stockOk=pl.stock>0 && planKeys>0;
    return `<div class="plan ${!stockOk?'disabled':''}" onclick="${stockOk?`selectPlan(${i})`:''}">
      <div class="plan-dur">${esc(pl.dur)}</div>
      <div class="plan-price">${fmt(pl.price)}</div>
      <div class="plan-stock">${!stockOk?`<span style="color:var(--danger)">❌ স্টক শেষ</span>`:`<span style="color:var(--success)">✓ Available</span>`}</div>
    </div>`;
  }).join('');
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">🛒 ${esc(p.name)}</h2>
    <div style="background:rgba(16,185,129,.08);padding:12px 14px;border-radius:var(--radius-md);margin-bottom:12px;border:1px solid rgba(16,185,129,.2);display:flex;align-items:center;gap:10px">
      ${WALLET_SVG_SM.replace('class="wallet-ic"','class="wallet-ic" style="width:20px;height:20px;stroke:var(--success)"')}
      <div style="flex:1"><div style="font-size:11px;color:var(--text-mid);font-weight:600">আপনার ব্যালেন্স</div><div style="font-size:18px;font-weight:900;color:var(--success);font-family:'Orbitron',sans-serif">${fmt(balance)}</div></div>
    </div>
    <div class="field"><label>প্ল্যান বাছুন</label></div>
    <div class="plan-grid">${plansHtml}</div>
    <div class="field"><label>পরিমাণ</label>
      <div style="display:flex;align-items:center;gap:8px">
        <button class="btn btn-ghost btn-sm" style="width:44px;height:44px;font-size:20px;padding:0" onclick="changeQty(-1)">−</button>
        <input id="qtyInput" value="1" readonly style="text-align:center;font-weight:900;font-size:18px;height:44px" />
        <button class="btn btn-ghost btn-sm" style="width:44px;height:44px;font-size:20px;padding:0" onclick="changeQty(1)">+</button>
      </div>
    </div>
    <div style="padding:12px 14px;background:var(--card-2);border-radius:var(--radius-md);margin:12px 0;display:flex;justify-content:space-between;align-items:center">
      <span style="font-size:13px;font-weight:600;color:var(--text-mid)">মোট</span>
      <span id="payTotal" style="font-size:20px;font-weight:900;color:var(--primary);font-family:'Orbitron',sans-serif">${fmt(0)}</span>
    </div>
    <button class="btn btn-primary btn-full btn-lg" onclick="submitOrder()">✅ ব্যালেন্স দিয়ে কিনুন</button>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:10px">ব্যালেন্স কম? <a href="#" onclick="event.preventDefault();closeModal();nav('wallet')" style="color:var(--primary);font-weight:700">যোগ করুন</a></p>
  `);
}
function selectPlan(i){ selectedPlan=i; document.querySelectorAll('.plan').forEach((p,j)=>p.classList.toggle('active',j===i)); updatePayTotal(); }
function changeQty(d){ selectedQty=Math.max(1,selectedQty+d); const el=$('qtyInput'); if(el) el.value=selectedQty; updatePayTotal(); }
function updatePayTotal(){ const total=(selectedPlan!==null&&currentPlans[selectedPlan])?currentPlans[selectedPlan].price*selectedQty:0; const el=$('payTotal'); if(el) el.textContent=fmt(total); }

function submitOrder(){
  if(!isStoreOnline()){ toast('⚠️ এখন অফলাইন'); return; }
  const p=currentProduct; if(!p) return;
  if(selectedPlan===null){ toast('প্ল্যান সিলেক্ট করুন'); return; }
  const plan=currentPlans[selectedPlan];
  const total=plan.price*selectedQty;
  const balance=getBalance(state.user.id);
  if(balance<total){ toast('❌ পর্যাপ্ত ব্যালেন্স নেই'); return; }
  if(plan.stock<=0){ toast('Stock শেষ'); return; }
  const realProd=state.products.find(x=>x.id===p.id);
  if(!realProd){ toast('প্রোডাক্ট পাওয়া যায়নি'); return; }
  const autoDelivery=state.settings.auto_delivery!==false;
  const autoApprove=state.settings.auto_approve!==false;
  const available=getAvailableKeys(realProd, plan.dur);
  const canAutoDeliver=autoDelivery && available.length>=selectedQty;
  addBalance(state.user.id, -total, {type:'debit', description:`অর্ডার: ${realProd.name} (${plan.dur} × ${selectedQty})`});
  const order={
    id:uid(), userId:state.user.id, username:state.user.username, email:state.user.email,
    productId:realProd.id, productName:realProd.name, planDur:plan.dur,
    price:total, unitPrice:plan.price, qty:selectedQty, status:'PENDING',
    txnId:'BAL-'+Date.now(), codeContent:'', keysAssigned:[], autoDelivered:false,
    createdAt:new Date().toISOString(), completedAt:null
  };
  if(canAutoDeliver){
    const reservedTexts=reserveKeys(realProd, selectedQty, plan.dur);
    if(reservedTexts && reservedTexts.length===selectedQty){
      order.codeContent=reservedTexts.join('\n');
      order.keysAssigned=reservedTexts;
      order.autoDelivered=true;
      order.status=autoApprove?'COMPLETED':'PROCESSING';
      if(order.status==='COMPLETED') order.completedAt=new Date().toISOString();
    }
  }
  if(realProd.plans){ const rp=realProd.plans.find(x=>x.dur===plan.dur); if(rp&&rp.stock>0) rp.stock=Math.max(0,rp.stock-selectedQty); }
  state.orders.push(order);
  if(order.status==='COMPLETED'){ state.transactions.push({id:uid(),userId:state.user.id,type:'purchase',amount:-total,balanceAfter:getBalance(state.user.id),description:`✅ ${realProd.name} (${plan.dur}) — অটো ডেলিভারড`,refId:order.id,createdAt:new Date().toISOString()}); }
  saveLocal(); pushCol('orders'); pushCol('products'); pushCol('transactions'); pushCol('users');
  notifyOrder(order, realProd, order.codeContent);
  const remaining=getAvailableKeys(realProd, plan.dur).length;
  const threshold=Number(state.settings.low_stock_threshold)||5;
  if(remaining<=threshold) notifyLowStock(realProd.name, plan.dur, remaining);
  closeModal();
  if(order.status==='COMPLETED'){ toast('✅ অর্ডার সফল! কী রেডি'); setTimeout(()=>showKeySuccessModal(order, realProd),300); }
  else if(order.status==='PROCESSING'){ toast('⏳ কী রিজার্ভ হয়েছে'); nav('orders'); }
  else { toast('⏳ অর্ডার PENDING'); nav('orders'); }
}

function showKeySuccessModal(order, product){
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div style="text-align:center;margin-bottom:16px">
      <div style="width:64px;height:64px;border-radius:50%;background:var(--grad-success);color:#fff;display:inline-flex;align-items:center;justify-content:center;font-size:30px;box-shadow:0 8px 24px rgba(16,185,129,.4)">✅</div>
      <h2 style="font-size:20px;font-weight:900;margin-top:10px">অর্ডার সফল!</h2>
      <p style="font-size:13px;color:var(--text-mid);margin-top:4px">${esc(product.name)} — ${esc(order.planDur)}</p>
    </div>
    <div class="key-box">
      <div class="key-box-head">🎫 আপনার কী / কোড</div>
      <div class="key-content" id="successKeyBox">${esc(order.codeContent)}</div>
      <div class="key-copy-row"><button class="key-copy-btn" onclick="copyText(document.getElementById('successKeyBox').textContent)">📋 কপি করুন</button></div>
    </div>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:12px">⚡ Telegram-এও পাঠানো হয়েছে</p>
    <button class="btn btn-primary btn-full" style="margin-top:12px" onclick="closeModal();nav('orders')">📦 অর্ডার দেখুন</button>
  `);
}

/* === WALLET PAGE === */
function renderWallet(){
  const u=state.users.find(x=>x.id===state.user.id)||state.user;
  const bal=Number(u.balance||0);
  const myDeposits=state.deposits.filter(d=>d.userId===state.user.id).slice().reverse();
  const myTx=state.transactions.filter(t=>t.userId===state.user.id).slice().reverse();
  const pendingCount=myDeposits.filter(d=>d.status==='PENDING').length;
  return `<h1 class="page-title">${WALLET_SVG_LG} আমার ওয়ালেট</h1>
    <div class="hero-card">
      <div class="hero-content">
        <div class="hero-label">${WALLET_SVG_LG} বর্তমান ব্যালেন্স</div>
        <div class="hero-balance">${fmt(bal)}</div>
        <div style="font-size:13px;opacity:.85">${pendingCount>0?`⏳ ${pendingCount}টি অনুরোধ পেন্ডিং`:'✓ সব ক্লিয়ার'}</div>
        <div class="hero-actions"><button class="hero-btn solid" onclick="openDepositModal()">➕ টাকা যোগ করুন</button></div>
      </div>
    </div>
    <h2 class="section-title">📋 ডিপোজিট রিকোয়েস্ট</h2>
    ${myDeposits.length===0 ? `<div class="card empty" style="padding:24px"><div class="empty-icon" style="font-size:40px">💳</div><div style="font-size:13px">কোনো ডিপোজিট রিকোয়েস্ট নেই</div></div>` :
      myDeposits.map(d=>`<div class="card list-item"><div class="list-icon">💳</div><div class="list-body"><div style="display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap"><span class="list-title">${fmt(d.amount)}</span><span class="badge ${d.status==='APPROVED'?'badge-green':d.status==='PENDING'?'badge-amber':'badge-red'}">${d.status}</span></div><div class="list-sub">🆔 ${esc(d.txnId)}<br>📅 ${tAgo(d.createdAt)}</div>${d.adminNote?`<div class="list-sub" style="margin-top:6px;color:var(--primary)">📝 ${esc(d.adminNote)}</div>`:''}</div></div>`).join('')}
    <h2 class="section-title">📊 ট্রানজ্যাকশন হিস্ট্রি</h2>
    ${myTx.length===0 ? `<div class="card empty" style="padding:24px"><div class="empty-icon" style="font-size:40px">📊</div><div style="font-size:13px">কোনো ট্রানজ্যাকশন নেই</div></div>` :
      myTx.map(t=>`<div class="card list-item"><div class="list-icon" style="background:${t.amount>0?'rgba(16,185,129,.1)':'rgba(239,68,68,.1)'};color:${t.amount>0?'var(--success)':'var(--danger)'}">${t.amount>0?'➕':'➖'}</div><div class="list-body"><div style="display:flex;justify-content:space-between;gap:8px"><span class="list-title" style="font-size:13px">${esc(t.description||t.type)}</span><span style="font-weight:900;color:${t.amount>0?'var(--success)':'var(--danger)'}">${t.amount>0?'+':''}${fmt(t.amount)}</span></div><div class="list-sub">📅 ${tAgo(t.createdAt)} • ব্যালেন্স: ${fmt(t.balanceAfter)}</div></div></div>`).join('')}
  `;
}
function openDepositModal(){
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">💳 ব্যালেন্স যোগ করুন</h2>
    <div class="bkash-box">
      <div style="font-weight:800;color:var(--bkash);font-size:15px;display:flex;align-items:center;gap:8px">📲 bKash (Send Money)</div>
      <div class="bkash-num-row"><div class="bkash-num">${esc(state.settings.bkash_number||'01XXXXXXXXX')}</div><button class="btn-copy" onclick="copyText('${esc(state.settings.bkash_number||'')}')">📋 কপি</button></div>
      <div style="margin-top:10px;font-size:12px;color:var(--text-mid);line-height:1.6;background:var(--card-2);padding:10px;border-radius:var(--radius-md)">⚠️ উপরে Send Money করুন, তারপর নিচে ফর্ম পূরণ করুন। অ্যাডমিন approve করলে ব্যালেন্স যোগ হবে।</div>
    </div>
    <div class="field" style="margin-top:14px"><label>পরিমাণ (৳)</label><input id="depAmount" type="number" min="10" placeholder="যেমন: 100" /></div>
    <div class="field"><label>bKash Transaction ID</label><input id="depTxn" placeholder="8N7Y6T5R4E" style="font-family:monospace;letter-spacing:1px" /></div>
    <div class="field"><label>নোট (ঐচ্ছিক)</label><input id="depNote" placeholder="কোনো মেসেজ..." /></div>
    <button class="btn btn-bkash btn-full btn-lg" onclick="submitDeposit()">📤 রিকোয়েস্ট পাঠান</button>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:10px">⏳ Admin approve না করা পর্যন্ত PENDING</p>
  `);
}
function submitDeposit(){
  const amount=Number($('depAmount').value||0);
  const txn=($('depTxn').value||'').trim();
  const note=($('depNote').value||'').trim();
  if(amount<10){ toast('সর্বনিম্ন ৳১০'); return; }
  if(!txn){ toast('Transaction ID দিন'); return; }
  if(state.deposits.find(d=>d.txnId===txn)){ toast('এই TxnID আগে ব্যবহার হয়েছে'); return; }
  const dep={id:uid(),userId:state.user.id,username:state.user.username,email:state.user.email,amount,txnId:txn,note,status:'PENDING',adminNote:'',createdAt:new Date().toISOString(),processedAt:null};
  state.deposits.push(dep); pushCol('deposits'); notifyDeposit(dep);
  closeModal(); toast('✓ রিকোয়েস্ট পাঠানো হয়েছে'); render();
}

/* === ACCOUNT PAGE === */
function renderAccount(){
  const u=state.users.find(x=>x.id===state.user.id)||state.user;
  const orders=state.orders.filter(o=>o.userId===u.id);
  const tx=state.transactions.filter(t=>t.userId===u.id);
  const totalSpent=tx.filter(t=>t.amount<0).reduce((s,t)=>s+Math.abs(t.amount),0);
  const adminBtn = isAdmin() ? `<button class="btn btn-warning btn-full" style="margin-bottom:10px" onclick="nav('admin')">⚙️ অ্যাডমিন প্যানেল</button>` : '';
  return `<h1 class="page-title">👤 আমার একাউন্ট</h1>
    <div class="card" style="padding:20px;margin-bottom:14px;background:var(--grad-hero);border:1px solid rgba(124,58,237,.3)">
      <div style="display:flex;align-items:center;gap:14px;flex-wrap:wrap">
        <div style="background:${esc(u.avatarColor||'#7c3aed')};box-shadow:0 8px 20px ${esc(u.avatarColor||'#7c3aed')}40;width:60px;height:60px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:22px;font-weight:900;color:#fff;border:3px solid #fff;flex-shrink:0">${esc((u.username||'U').slice(0,2).toUpperCase())}</div>
        <div style="min-width:0;flex:1">
          <div style="font-size:12px;color:var(--text-mid)">স্বাগতম,</div>
          <div style="font-size:clamp(18px,5vw,22px);font-weight:900;word-wrap:break-word">${esc(u.username||'')} 👋</div>
          <div style="font-size:12px;color:var(--text-mid);word-break:break-all;margin-top:2px">${esc(u.email||'')}</div>
          ${u.role==='ADMIN'?'<span class="badge badge-purple" style="margin-top:6px">⚙️ ADMIN</span>':''}
        </div>
      </div>
    </div>
    <div class="stat-grid">
      <div class="stat green"><div class="stat-label">ব্যালেন্স</div><div class="stat-val">${fmt(u.balance||0)}</div></div>
      <div class="stat blue"><div class="stat-label">মোট অর্ডার</div><div class="stat-val">${orders.length}</div></div>
      <div class="stat amber"><div class="stat-label">স্পেন্ট</div><div class="stat-val">${fmt(totalSpent)}</div></div>
      <div class="stat pink"><div class="stat-label">জয়েন</div><div class="stat-val" style="font-size:13px">${new Date(u.createdAt).toLocaleDateString('bn-BD')}</div></div>
    </div>
    ${adminBtn}
    <button class="btn btn-danger btn-full" onclick="logout()">🚪 লগআউট</button>`;
}

/* === ORDERS PAGE === */
function renderOrders(){
  const orders=state.orders.filter(o=>o.userId===state.user.id).slice().reverse();
  return `<h1 class="page-title">📦 আমার অর্ডার</h1>
    ${orders.length===0 ? `<div class="card empty"><div class="empty-icon">📦</div><div style="font-weight:700;font-size:16px">কোনো অর্ডার নেই</div><div style="font-size:13px;margin-top:6px">এখনো অর্ডার দেননি</div><button class="btn btn-primary" style="margin-top:16px" onclick="nav('home')">শপিং করুন</button></div>` :
      orders.map(o=>{
        const p=state.products.find(x=>x.id===o.productId);
        const statusBadge=o.status==='COMPLETED'?'badge-green':o.status==='PENDING'?'badge-amber':o.status==='PROCESSING'?'badge-amber':'badge-red';
        const statusText=o.status==='COMPLETED'?'✅ সম্পন্ন':o.status==='PENDING'?'⏳ অপেক্ষারত':o.status==='PROCESSING'?'⏳ প্রসেসিং':o.status;
        const keyHtml=o.codeContent?`<div class="key-box"><div class="key-box-head">${o.status==='COMPLETED'?'🎫 আপনার কী':'🔒 কী রিজার্ভ'}</div><div class="key-content" id="key_${o.id}">${esc(o.codeContent)}</div><div class="key-copy-row"><button class="key-copy-btn" onclick="copyText(document.getElementById('key_${o.id}').textContent)">📋 কপি করুন</button></div></div>`:(o.status==='PENDING'?`<div style="margin-top:8px;font-size:12px;color:var(--warning);font-weight:600;background:rgba(245,158,11,.1);padding:10px;border-radius:var(--radius-md)">⏳ অ্যাডমিন কী স্টক যোগ করলে স্বয়ংক্রিয়ভাবে দেওয়া হবে...</div>`:'');
        return `<div class="card list-item" style="flex-direction:column;align-items:stretch;padding:14px">
          <div style="display:flex;gap:12px;align-items:flex-start">
            <div class="list-icon">${esc(p?.icon||'📦')}</div>
            <div class="list-body">
              <div style="display:flex;justify-content:space-between;gap:8px;align-items:center;flex-wrap:wrap"><span class="list-title" style="font-size:15px">${esc(p?.name||o.productName||'—')}</span><span style="font-weight:900;font-size:16px">${fmt(o.price)}</span></div>
              <div class="list-sub" style="margin-top:4px">${o.planDur?'⏱ '+esc(o.planDur):''}${o.qty>1?' • '+o.qty+'x':''}<br>📅 ${tAgo(o.createdAt)}</div>
              <div style="margin-top:8px"><span class="badge ${statusBadge}">${statusText}</span></div>
            </div>
          </div>${keyHtml}
        </div>`;
      }).join('')}`;
}

/* === KEYS PAGE === */
function renderKeys(){
  const orders=state.orders.filter(o=>o.userId===state.user.id && o.codeContent).slice().reverse();
  return `<h1 class="page-title">🔑 My Keys</h1>
    ${orders.length===0 ? `<div class="card empty"><div class="empty-icon">🔑</div><div style="font-weight:700;font-size:16px">কোনো কী নেই</div></div>` :
      orders.map(o=>{
        const p=state.products.find(x=>x.id===o.productId);
        return `<div class="card list-item" style="flex-direction:column;align-items:stretch;padding:14px">
          <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px">
            <span style="font-weight:800;font-size:14px">${esc(p?.name||o.productName||'—')} <span style="font-size:10px;color:var(--text-mid);font-weight:400">(${o.planDur})</span></span>
            <span style="font-size:12px;color:var(--success);font-weight:700">${fmt(o.price)}</span>
          </div>
          <div class="key-box" style="margin-top:0"><div class="key-content" id="key_${o.id}">${esc(o.codeContent)}</div><div class="key-copy-row"><button class="key-copy-btn" onclick="copyText(document.getElementById('key_${o.id}').textContent)">📋 কপি করুন</button></div></div>
        </div>`;
      }).join('')}`;
}

/* ============================================================
   ADMIN PANEL — Complete Management System
   ============================================================ */
function renderAdmin(){
  if(!isAdmin()){ toast('অ্যাডমিন অ্যাক্সেস নেই'); nav('account'); return ''; }
  const tabs=[
    {id:'dashboard',label:'📊 ড্যাশবোর্ড'},
    {id:'products',label:'📦 প্রোডাক্ট'},
    {id:'orders',label:'📦 অর্ডার'},
    {id:'deposits',label:'💰 ডিপোজিট'},
    {id:'users',label:'👥 ইউজার'},
    {id:'settings',label:'⚙️ সেটিংস'}
  ];
  const tabsHtml=tabs.map(t=>`<button class="admin-tab ${state.adminTab===t.id?'active':''}" onclick="state.adminTab='${t.id}';render()">${t.label}</button>`).join('');
  let content='';
  switch(state.adminTab){
    case 'dashboard': content=adminDashboard(); break;
    case 'products': content=adminProducts(); break;
    case 'orders': content=adminOrders(); break;
    case 'deposits': content=adminDeposits(); break;
    case 'users': content=adminUsers(); break;
    case 'settings': content=adminSettings(); break;
  }
  return `<h1 class="page-title">⚙️ অ্যাডমিন প্যানেল</h1>
    <div class="admin-tab-bar">${tabsHtml}</div>
    ${content}`;
}

function adminDashboard(){
  const totalUsers=state.users.length;
  const totalOrders=state.orders.length;
  const totalRevenue=state.orders.reduce((s,o)=>s+Number(o.price||0),0);
  const pendingDeposits=state.deposits.filter(d=>d.status==='PENDING').length;
  const pendingOrders=state.orders.filter(o=>o.status==='PENDING').length;
  const totalProducts=state.products.length;
  const activeProducts=state.products.filter(p=>p.status==='ACTIVE').length;
  const lowStock=state.products.filter(p=>{
    if(!p.plans) return false;
    return p.plans.some(pl=>pl.stock<=Number(state.settings.low_stock_threshold||5));
  }).length;
  return `<div class="stat-grid">
    <div class="stat green"><div class="stat-label">Revenue</div><div class="stat-val">${fmt(totalRevenue)}</div></div>
    <div class="stat blue"><div class="stat-label">Users</div><div class="stat-val">${totalUsers}</div></div>
    <div class="stat amber"><div class="stat-label">Orders</div><div class="stat-val">${totalOrders}</div></div>
    <div class="stat pink"><div class="stat-label">Products</div><div class="stat-val">${totalProducts}</div></div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">📋 Pending Actions</div>
    <div style="display:flex;flex-direction:column;gap:8px">
      <button class="btn btn-ghost btn-full" style="justify-content:space-between" onclick="state.adminTab='deposits';render()"><span>💰 Pending Deposits</span><span class="badge badge-amber">${pendingDeposits}</span></button>
      <button class="btn btn-ghost btn-full" style="justify-content:space-between" onclick="state.adminTab='orders';render()"><span>📦 Pending Orders</span><span class="badge badge-amber">${pendingOrders}</span></button>
      <button class="btn btn-ghost btn-full" style="justify-content:space-between" onclick="state.adminTab='products';render()"><span>⚠️ Low Stock</span><span class="badge badge-red">${lowStock}</span></button>
    </div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">📊 Quick Stats</div>
    <div style="font-size:13px;line-height:2;color:var(--text-mid)">
      <div style="display:flex;justify-content:space-between"><span>Active Products:</span><span style="color:var(--success);font-weight:700">${activeProducts}</span></div>
      <div style="display:flex;justify-content:space-between"><span>Total Orders:</span><span style="color:var(--text);font-weight:700">${totalOrders}</span></div>
      <div style="display:flex;justify-content:space-between"><span>Store Status:</span><span style="color:${isStoreOnline()?'var(--success)':'var(--danger)'};font-weight:700">${isStoreOnline()?'Online':'Offline'}</span></div>
    </div>
  </div>`;
}

function adminProducts(){
  let html=`<button class="btn btn-primary btn-full" style="margin-bottom:12px" onclick="openProductEditor()">➕ নতুন প্রোডাক্ট যোগ করুন</button>`;
  if(state.products.length===0){
    html+=`<div class="card empty"><div class="empty-icon">📦</div><div style="font-weight:700;font-size:16px">কোনো প্রোডাক্ট নেই</div><div style="font-size:13px;margin-top:6px">নতুন প্রোডাক্ট যোগ করুন</div></div>`;
  } else {
    state.products.forEach(p=>{
      const totalKeys=(p.plans||[]).reduce((s,pl)=>s+(pl.keys||[]).length,0);
      html+=`<div class="product-mgmt-item">
        <div class="product-mgmt-thumb">${p.image?`<img src="${esc(p.image)}" onerror="this.style.display='none';this.parentElement.textContent='${esc(p.icon||'🎮')}'">`:esc(p.icon||'🎮')}</div>
        <div style="flex:1;min-width:0">
          <div style="font-weight:800;font-size:14px;word-break:break-word">${esc(p.name)}</div>
          <div style="font-size:11px;color:var(--text-mid);margin-top:2px">${esc(p.category||'NON_ROOT')} • ${p.status==='ACTIVE'?'<span style="color:var(--success)">Active</span>':'<span style="color:var(--danger)">Inactive</span>'}</div>
          <div style="font-size:11px;color:var(--text-mid);margin-top:2px">🔑 ${totalKeys} keys • ${(p.plans||[]).length} plans</div>
          <div style="display:flex;gap:6px;margin-top:8px;flex-wrap:wrap">
            <button class="btn btn-soft btn-sm" onclick="openProductEditor('${p.id}')">✏️ Edit</button>
            <button class="btn btn-danger btn-sm" onclick="deleteProduct('${p.id}')">🗑️ Delete</button>
          </div>
        </div>
      </div>`;
    });
  }
  return html;
}

function openProductEditor(pid){
  const p = pid ? state.products.find(x=>x.id===pid) : null;
  state.adminProductEdit = pid || null;
  const data = p || {name:'',description:'',image:'',icon:'🎮',category:'NON_ROOT',status:'ACTIVE',antiban:false,maintenance:false,oldPrice:0,plans:[{dur:'7 Days',price:99,stock:10,keys:[]}]};
  const plansHtml=(data.plans||[]).map((pl,i)=>`
    <div class="admin-card" style="background:var(--card-2)" data-plan-idx="${i}">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:8px">
        <span style="font-size:12px;font-weight:700;color:var(--primary-light)">Plan ${i+1}</span>
        ${(data.plans||[]).length>1?`<button class="btn btn-danger btn-sm" onclick="removePlan(${i})">✕</button>`:''}
      </div>
      <div class="field"><label>Duration</label><input data-plan="${i}" data-key="dur" value="${esc(pl.dur||'')}" placeholder="7 Days / 30 Days" /></div>
      <div class="field"><label>Price (৳)</label><input data-plan="${i}" data-key="price" type="number" value="${esc(pl.price||0)}" /></div>
      <div class="field"><label>Stock</label><input data-plan="${i}" data-key="stock" type="number" value="${esc(pl.stock||0)}" /></div>
      <div class="field"><label>Keys (one per line)</label><textarea data-plan="${i}" data-key="keys" placeholder="KEY-001&#10;KEY-002&#10;KEY-003" style="min-height:100px;font-family:monospace;font-size:12px">${esc((pl.keys||[]).map(k=>getKeyText(k)).join('\n'))}</textarea></div>
    </div>`).join('');
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">${pid?'✏️ প্রোডাক্ট এডিট':'➕ নতুন প্রোডাক্ট'}</h2>
    <div class="field"><label>প্রোডাক্ট নাম</label><input id="pName" value="${esc(data.name||'')}" placeholder="FF Auto Headshot Panel" /></div>
    <div class="field"><label>বিবরণ</label><textarea id="pDesc" placeholder="প্রোডাক্টের বিবরণ" style="min-height:60px">${esc(data.description||'')}</textarea></div>
    <div class="field"><label>ইমেজ URL</label><input id="pImage" value="${esc(data.image||'')}" placeholder="https://..." /></div>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px">
      <div class="field"><label>আইকন (emoji)</label><input id="pIcon" value="${esc(data.icon||'🎮')}" /></div>
      <div class="field"><label>ক্যাটেগরি</label>
        <select id="pCategory">
          <option value="NON_ROOT" ${data.category==='NON_ROOT'?'selected':''}>NON ROOT</option>
          <option value="ROOT" ${data.category==='ROOT'?'selected':''}>ROOT</option>
          <option value="IPHONE" ${data.category==='IPHONE'?'selected':''}>IPHONE</option>
          <option value="PC" ${data.category==='PC'?'selected':''}>PC</option>
        </select>
      </div>
    </div>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px">
      <div class="field"><label>পুরনো দাম (৳)</label><input id="pOldPrice" type="number" value="${esc(data.oldPrice||0)}" /></div>
      <div class="field"><label>সেটআপ লিংক (ঐচ্ছিক)</label><input id="pSetupUrl" value="${esc(data.url_setup_video||'')}" placeholder="YouTube link" /></div>
    </div>
    <div style="display:flex;gap:14px;margin-bottom:14px;flex-wrap:wrap">
      <label style="display:flex;align-items:center;gap:8px;font-size:13px;cursor:pointer"><input type="checkbox" id="pAntiban" ${data.antiban?'checked':''} style="width:18px;height:18px" /> Anti Ban</label>
      <label style="display:flex;align-items:center;gap:8px;font-size:13px;cursor:pointer"><input type="checkbox" id="pMaintenance" ${data.maintenance?'checked':''} style="width:18px;height:18px" /> Maintenance</label>
      <label style="display:flex;align-items:center;gap:8px;font-size:13px;cursor:pointer"><input type="checkbox" id="pActive" ${data.status==='ACTIVE'?'checked':''} style="width:18px;height:18px" /> Active</label>
    </div>
    <div class="section-title">📋 Plans & Keys</div>
    <div id="plansContainer">${plansHtml}</div>
    <button class="btn btn-ghost btn-full btn-sm" style="margin-bottom:14px" onclick="addPlan()">➕ আরেকটি Plan যোগ করুন</button>
    <button class="btn btn-primary btn-full btn-lg" onclick="saveProduct()">💾 সেভ করুন</button>
  `);
}

let editPlans = null;
function addPlan(){
  // Read current plans from DOM
  readPlansFromDOM();
  editPlans.push({dur:'',price:0,stock:0,keys:[]});
  const p = state.adminProductEdit ? state.products.find(x=>x.id===state.adminProductEdit) : null;
  if(p){ p.plans = editPlans.slice(); }
  openProductEditor(state.adminProductEdit || null);
  // Restore editPlans data
  if(p){ p.plans = editPlans.slice(); }
}
function removePlan(idx){
  readPlansFromDOM();
  if(editPlans.length<=1){ toast('অন্তত একটি plan দরকার'); return; }
  editPlans.splice(idx,1);
  const p = state.adminProductEdit ? state.products.find(x=>x.id===state.adminProductEdit) : null;
  if(p){ p.plans = editPlans.slice(); }
  openProductEditor(state.adminProductEdit || null);
  if(p){ p.plans = editPlans.slice(); }
}
function readPlansFromDOM(){
  editPlans = [];
  const cards = document.querySelectorAll('[data-plan-idx]');
  cards.forEach((card)=>{
    const idx = parseInt(card.dataset.planIdx);
    const dur = card.querySelector(`[data-plan="${idx}"][data-key="dur"]`).value;
    const price = Number(card.querySelector(`[data-plan="${idx}"][data-key="price"]`).value||0);
    const stock = Number(card.querySelector(`[data-plan="${idx}"][data-key="stock"]`).value||0);
    const keysText = card.querySelector(`[data-plan="${idx}"][data-key="keys"]`).value;
    const keys = keysText.split('\n').map(k=>k.trim()).filter(Boolean);
    editPlans[idx] = {dur,price,stock,keys};
  });
}

function saveProduct(){
  const name=$('pName').value.trim();
  if(!name){ toast('নাম দিন'); return; }
  readPlansFromDOM();
  if(editPlans.length===0){ toast('অন্তত একটি plan দরকার'); return; }
  const pid = state.adminProductEdit;
  const existing = pid ? state.products.find(x=>x.id===pid) : null;
  const product = {
    id: pid || uid(),
    name,
    description: $('pDesc').value.trim(),
    image: $('pImage').value.trim(),
    icon: $('pIcon').value.trim()||'🎮',
    category: $('pCategory').value,
    oldPrice: Number($('pOldPrice').value||0),
    url_setup_video: $('pSetupUrl').value.trim(),
    antiban: $('pAntiban').checked,
    maintenance: $('pMaintenance').checked,
    status: $('pActive').checked ? 'ACTIVE' : 'INACTIVE',
    plans: editPlans,
    createdAt: existing?.createdAt || new Date().toISOString()
  };
  if(existing){
    Object.assign(existing, product);
  } else {
    state.products.push(product);
  }
  pushCol('products');
  closeModal();
  toast(pid?'✓ প্রোডাক্ট আপডেট হয়েছে':'✓ প্রোডাক্ট যোগ হয়েছে');
  render();
}
function deleteProduct(pid){
  if(!confirm('প্রোডাক্ট ডিলিট করতে চান?')) return;
  state.products = state.products.filter(p=>p.id!==pid);
  pushCol('products');
  toast('✓ ডিলিট হয়েছে');
  render();
}

function adminOrders(){
  const orders=state.orders.slice().reverse();
  if(orders.length===0) return `<div class="card empty"><div class="empty-icon">📦</div><div style="font-weight:700;font-size:16px">কোনো অর্ডার নেই</div></div>`;
  return orders.map(o=>{
    const u=state.users.find(x=>x.id===o.userId);
    const p=state.products.find(x=>x.id===o.productId);
    const statusBadge=o.status==='COMPLETED'?'badge-green':o.status==='PENDING'?'badge-amber':o.status==='PROCESSING'?'badge-amber':'badge-red';
    let actions='';
    if(o.status==='PENDING'){
      actions=`<button class="btn btn-success btn-sm" onclick="adminCompleteOrder('${o.id}')">✅ Complete</button>`;
    }
    if(o.status!=='REFUNDED' && o.status!=='COMPLETED'){
      actions+=`<button class="btn btn-danger btn-sm" onclick="adminRefundOrder('${o.id}')">↩️ Refund</button>`;
    }
    return `<div class="admin-card">
      <div style="display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap;margin-bottom:8px">
        <span style="font-weight:800;font-size:14px">${esc(p?.name||o.productName||'—')}</span>
        <span class="badge ${statusBadge}">${o.status}</span>
      </div>
      <div style="font-size:12px;color:var(--text-mid);line-height:1.7">
        👤 ${esc(o.username||u?.username||'')} • 📧 ${esc(o.email||'')}<br>
        ⏱ ${esc(o.planDur)} • 🔢 ${o.qty}x • 💰 ${fmt(o.price)}<br>
        🆔 <code>${esc(o.txnId)}</code><br>
        📅 ${tAgo(o.createdAt)}
      </div>
      ${o.codeContent?`<div style="margin-top:8px;font-size:11px;color:var(--success)">🔑 ${o.keysAssigned.length} keys assigned</div>`:''}
      ${actions?`<div style="display:flex;gap:6px;margin-top:10px">${actions}</div>`:''}
    </div>`;
  }).join('');
}
function adminCompleteOrder(oid){
  const o=state.orders.find(x=>x.id===oid); if(!o) return;
  o.status='COMPLETED'; o.completedAt=new Date().toISOString();
  pushCol('orders');
  toast('✓ অর্ডার সম্পন্ন');
  render();
}
function adminRefundOrder(oid){
  const o=state.orders.find(x=>x.id===oid); if(!o) return;
  if(!confirm('টাকা ফেরত দিতে চান?')) return;
  addBalance(o.userId, o.price, {type:'refund', description:`Refund: ${o.productName}`});
  o.status='REFUNDED';
  pushCol('orders');
  toast('✓ টাকা ফেরত দেওয়া হয়েছে');
  render();
}

function adminDeposits(){
  const deps=state.deposits.slice().reverse();
  if(deps.length===0) return `<div class="card empty"><div class="empty-icon">💰</div><div style="font-weight:700;font-size:16px">কোনো ডিপোজিট নেই</div></div>`;
  return deps.map(d=>{
    const u=state.users.find(x=>x.id===d.userId);
    const statusBadge=d.status==='APPROVED'?'badge-green':d.status==='PENDING'?'badge-amber':'badge-red';
    let actions='';
    if(d.status==='PENDING'){
      actions=`<div style="display:flex;gap:6px;margin-top:10px">
        <button class="btn btn-success btn-sm" onclick="adminApproveDeposit('${d.id}')">✅ Approve</button>
        <button class="btn btn-danger btn-sm" onclick="adminRejectDeposit('${d.id}')">❌ Reject</button>
      </div>`;
    }
    return `<div class="admin-card">
      <div style="display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap;margin-bottom:8px">
        <span style="font-weight:800;font-size:14px;color:var(--success)">${fmt(d.amount)}</span>
        <span class="badge ${statusBadge}">${d.status}</span>
      </div>
      <div style="font-size:12px;color:var(--text-mid);line-height:1.7">
        👤 ${esc(d.username||u?.username||'')} • 📧 ${esc(d.email||'')}<br>
        🆔 <code>${esc(d.txnId)}</code><br>
        ${d.note?`📝 ${esc(d.note)}<br>`:''}
        📅 ${tAgo(d.createdAt)}
      </div>
      ${d.adminNote?`<div style="margin-top:8px;font-size:12px;color:var(--primary)">📝 ${esc(d.adminNote)}</div>`:''}
      ${actions}
    </div>`;
  }).join('');
}
function adminApproveDeposit(did){
  const d=state.deposits.find(x=>x.id===did); if(!d) return;
  if(!confirm(`${fmt(d.amount)} approve করতে চান?`)) return;
  addBalance(d.userId, d.amount, {type:'credit', description:`Deposit approved: ${d.txnId}`, refId:d.id});
  d.status='APPROVED'; d.processedAt=new Date().toISOString();
  pushCol('deposits');
  sendTg(`✅ <b>Deposit Approved</b>\n\n👤 ${esc(d.username)}\n💵 ${fmt(d.amount)}\n🆔 <code>${esc(d.txnId)}</code>`);
  toast('✓ ডিপোজিট approve হয়েছে');
  render();
}
function adminRejectDeposit(did){
  const d=state.deposits.find(x=>x.id===did); if(!d) return;
  const note=prompt('Reject করার কারণ:', 'Invalid transaction');
  d.status='REJECTED'; d.adminNote=note||''; d.processedAt=new Date().toISOString();
  pushCol('deposits');
  toast('✓ ডিপোজিট reject হয়েছে');
  render();
}

function adminUsers(){
  if(state.users.length===0) return `<div class="card empty"><div class="empty-icon">👥</div><div style="font-weight:700;font-size:16px">কোনো ইউজার নেই</div></div>`;
  return state.users.slice().reverse().map(u=>{
    const orders=state.orders.filter(o=>o.userId===u.id).length;
    return `<div class="admin-card">
      <div style="display:flex;align-items:center;gap:10px;margin-bottom:8px">
        <div style="width:40px;height:40px;border-radius:50%;background:${esc(u.avatarColor||'#7c3aed')};display:flex;align-items:center;justify-content:center;color:#fff;font-weight:700;font-size:13px;flex-shrink:0">${esc((u.username||'U').slice(0,2).toUpperCase())}</div>
        <div style="flex:1;min-width:0">
          <div style="font-weight:800;font-size:14px">${esc(u.username||'')} ${u.role==='ADMIN'?'<span class="badge badge-purple" style="font-size:9px">ADMIN</span>':''}</div>
          <div style="font-size:11px;color:var(--text-mid);word-break:break-all">${esc(u.email||'')}</div>
        </div>
      </div>
      <div style="font-size:12px;color:var(--text-mid);line-height:1.6;margin-bottom:8px">
        💰 Balance: <b style="color:var(--success)">${fmt(u.balance||0)}</b> • 📦 Orders: ${orders}<br>
        ${u.banned?'<span style="color:var(--danger)">🚫 Banned</span>':'<span style="color:var(--success)">✓ Active</span>'}
      </div>
      <div style="display:flex;gap:6px;flex-wrap:wrap">
        <button class="btn btn-soft btn-sm" onclick="adminAddBalance('${u.id}')">💰 Balance</button>
        ${u.role!=='ADMIN'?`<button class="btn btn-warning btn-sm" onclick="adminToggleBan('${u.id}')">${u.banned?'✓ Unban':'🚫 Ban'}</button>`:''}
        ${u.role!=='ADMIN'?`<button class="btn btn-ghost btn-sm" onclick="adminPromote('${u.id}')">⬆️ Admin</button>`:`<button class="btn btn-ghost btn-sm" onclick="adminDemote('${u.id}')">⬇️ User</button>`}
      </div>
    </div>`;
  }).join('');
}
function adminAddBalance(uid_){
  const u=state.users.find(x=>x.id===uid_); if(!u) return;
  const amt=prompt(`Balance adjust for ${u.username} (current: ${fmt(u.balance)})\nUse + or - sign (e.g. +100 or -50):`, '+100');
  if(amt===null) return;
  const n=Number(amt);
  if(isNaN(n)){ toast('সঠিক সংখ্যা দিন'); return; }
  addBalance(u.id, n, {type:'admin', description:`Admin adjust: ${amt}`});
  toast('✓ ব্যালেন্স আপডেট হয়েছে');
  render();
}
function adminToggleBan(uid_){
  const u=state.users.find(x=>x.id===uid_); if(!u) return;
  u.banned=!u.banned;
  pushCol('users');
  toast(u.banned?'🚫 Banned':'✓ Unbanned');
  render();
}
function adminPromote(uid_){
  const u=state.users.find(x=>x.id===uid_); if(!u) return;
  if(!confirm(`${u.username} কে Admin বানাতে চান?`)) return;
  u.role='ADMIN';
  pushCol('users');
  toast('✓ Admin বানানো হয়েছে');
  render();
}
function adminDemote(uid_){
  const u=state.users.find(x=>x.id===uid_); if(!u) return;
  if(uid_===state.user.id){ toast('নিজেকে demote করতে পারবেন না'); return; }
  u.role='USER';
  pushCol('users');
  toast('✓ User বানানো হয়েছে');
  render();
}

function adminSettings(){
  const s=state.settings;
  return `<div class="admin-card">
    <div class="admin-card-title">🏪 Store Info</div>
    <div class="field"><label>Site Name</label><input id="sSiteName" value="${esc(s.site_name||'')}" /></div>
    <div class="field"><label>Tagline</label><input id="sTagline" value="${esc(s.tagline||'')}" /></div>
    <div class="field"><label>Logo Image URL</label><input id="sLogoImage" value="${esc(s.logo_image||'')}" placeholder="https://..." /></div>
    <div class="field"><label>Logo Click URL</label><input id="sLogoUrl" value="${esc(s.logo_url||'')}" /></div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">📢 Notification & Offer</div>
    <label style="display:flex;align-items:center;gap:8px;font-size:13px;margin-bottom:10px;cursor:pointer"><input type="checkbox" id="sNotifActive" ${s.notif_active?'checked':''} style="width:18px;height:18px" /> Notification Active</label>
    <div class="field"><label>Notification Text</label><input id="sNotification" value="${esc(s.notification||'')}" /></div>
    <label style="display:flex;align-items:center;gap:8px;font-size:13px;margin-bottom:10px;cursor:pointer"><input type="checkbox" id="sOfferActive" ${s.offer_active?'checked':''} style="width:18px;height:18px" /> Offer Active</label>
    <div class="field"><label>Offer Text</label><input id="sOfferText" value="${esc(s.offer_text||'')}" /></div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">💰 Payment</div>
    <div class="field"><label>bKash Number</label><input id="sBkash" value="${esc(s.bkash_number||'')}" /></div>
    <div class="field"><label>WhatsApp Number</label><input id="sWhatsapp" value="${esc(s.whatsapp_number||'')}" /></div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">🌐 Social</div>
    <div class="field"><label>Telegram Link</label><input id="sTelegram" value="${esc(s.telegram||'')}" /></div>
    <div class="field"><label>YouTube Link</label><input id="sYoutube" value="${esc(s.youtube||'')}" /></div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">⚙️ Store Settings</div>
    <label style="display:flex;align-items:center;gap:8px;font-size:13px;margin-bottom:10px;cursor:pointer"><input type="checkbox" id="sOnline" ${s.is_online?'checked':''} style="width:18px;height:18px" /> Store Online</label>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px">
      <div class="field"><label>Online Start</label><input id="sOnlineStart" type="time" value="${esc(s.online_start||'00:00')}" /></div>
      <div class="field"><label>Online End</label><input id="sOnlineEnd" type="time" value="${esc(s.online_end||'23:59')}" /></div>
    </div>
    <label style="display:flex;align-items:center;gap:8px;font-size:13px;margin-bottom:10px;cursor:pointer"><input type="checkbox" id="sAutoDelivery" ${s.auto_delivery?'checked':''} style="width:18px;height:18px" /> Auto Key Delivery</label>
    <label style="display:flex;align-items:center;gap:8px;font-size:13px;margin-bottom:10px;cursor:pointer"><input type="checkbox" id="sAutoApprove" ${s.auto_approve?'checked':''} style="width:18px;height:18px" /> Auto Approve Orders</label>
    <div class="field"><label>Low Stock Threshold</label><input id="sLowStock" type="number" value="${esc(s.low_stock_threshold||5)}" /></div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">🎨 Welcome Modal</div>
    <label style="display:flex;align-items:center;gap:8px;font-size:13px;margin-bottom:10px;cursor:pointer"><input type="checkbox" id="sWelcomeActive" ${s.welcome_active?'checked':''} style="width:18px;height:18px" /> Welcome Modal Active</label>
    <div class="field"><label>Welcome Image URL</label><input id="sWelcomeImage" value="${esc(s.welcome_image||'')}" /></div>
    <div class="field"><label>Welcome Text</label><textarea id="sWelcomeText" style="min-height:60px">${esc(s.welcome_text||'')}</textarea></div>
    <div class="field"><label>Welcome Link</label><input id="sWelcomeLink" value="${esc(s.welcome_link||'')}" /></div>
  </div>
  <div class="admin-card">
    <div class="admin-card-title">🖼️ Ad Slider</div>
    <div class="field"><label>Ad Image URLs (one per line)</label><textarea id="sAds" style="min-height:80px;font-family:monospace;font-size:12px" placeholder="https://example.com/ad1.jpg&#10;https://example.com/ad2.jpg">${esc((s.ads||[]).map(a=>typeof a==='string'?a:(a.url||a.image||'')).join('\n'))}</textarea></div>
    <div class="field"><label>Ad Delay (ms)</label><input id="sAdDelay" type="number" value="${esc(s.ad_delay||3500)}" /></div>
  </div>
  <button class="btn btn-primary btn-full btn-lg" onclick="saveSettings()">💾 সেটিংস সেভ করুন</button>`;
}

function saveSettings(){
  const adsText=($('sAds').value||'').trim();
  const ads=adsText?adsText.split('\n').map(u=>u.trim()).filter(Boolean):[];
  state.settings = {
    ...state.settings,
    site_name: $('sSiteName').value.trim()||'Panel Bajar',
    tagline: $('sTagline').value.trim(),
    logo_image: $('sLogoImage').value.trim(),
    logo_url: $('sLogoUrl').value.trim(),
    notif_active: $('sNotifActive').checked,
    notification: $('sNotification').value.trim(),
    offer_active: $('sOfferActive').checked,
    offer_text: $('sOfferText').value.trim(),
    bkash_number: $('sBkash').value.trim(),
    whatsapp_number: $('sWhatsapp').value.trim(),
    telegram: $('sTelegram').value.trim(),
    youtube: $('sYoutube').value.trim(),
    is_online: $('sOnline').checked,
    online_start: $('sOnlineStart').value,
    online_end: $('sOnlineEnd').value,
    auto_delivery: $('sAutoDelivery').checked,
    auto_approve: $('sAutoApprove').checked,
    low_stock_threshold: Number($('sLowStock').value||5),
    welcome_active: $('sWelcomeActive').checked,
    welcome_image: $('sWelcomeImage').value.trim(),
    welcome_text: $('sWelcomeText').value.trim(),
    welcome_link: $('sWelcomeLink').value.trim(),
    ads,
    ad_delay: Number($('sAdDelay').value||3500)
  };
  pushCol('settings');
  closeModal();
  toast('✓ সেটিংস সেভ হয়েছে');
  sessionStorage.removeItem('pb_welcome_shown');
  render();
}

function updateWhatsappLink(){
  const fab=$('whatsappFab'); if(!fab) return;
  let num=state.settings.whatsapp_number||'8801700000000';
  num=num.replace(/[^0-9]/g,'');
  fab.href=`https://wa.me/${num}`;
}

/* === FIREBASE SYNC === */
function startFbSync(){
  if(fbSyncStarted||!fbConnected) return;
  fbSyncStarted=true;
  fbListen('products', d=>{ if(d&&Array.isArray(d)){ state.products=d; localStorage.setItem('pb_products',JSON.stringify(d)); if(state.page==='home') render(); } });
  fbListen('orders', d=>{ if(d&&Array.isArray(d)){ state.orders=d; localStorage.setItem('pb_orders',JSON.stringify(d)); if(['orders','account','admin'].includes(state.page)) render(); } });
  fbListen('users', d=>{ if(d&&Array.isArray(d)){ state.users=d; localStorage.setItem('pb_users',JSON.stringify(d)); if(state.user){ const fresh=d.find(x=>x.id===state.user.id); if(fresh){ state.user=fresh; localStorage.setItem('pb_user',JSON.stringify(fresh)); if(fresh.banned){ toast('⚠️ অ্যাকাউন্ট ব্যান'); logout(); return; } } } render(); } });
  fbListen('deposits', d=>{ if(d&&Array.isArray(d)){ state.deposits=d; localStorage.setItem('pb_deposits',JSON.stringify(d)); if(['wallet','admin'].includes(state.page)) render(); } });
  fbListen('transactions', d=>{ if(d&&Array.isArray(d)){ state.transactions=d; localStorage.setItem('pb_transactions',JSON.stringify(d)); if(['wallet','account'].includes(state.page)) render(); } });
  fbListen('settings', d=>{
    if(d&&Array.isArray(d)&&d.length>0){
      state.settings={...DEFAULT_SETTINGS,...d[0]};
      localStorage.setItem('pb_settings',JSON.stringify(state.settings));
      render();
      if(state.settings.welcome_active && sessionStorage.getItem('pb_welcome_shown')!=='1') showWelcomeIfNeeded();
    }
  });
  fbLoad('products', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.products=d; localStorage.setItem('pb_products',JSON.stringify(d)); } else if(state.products.length>0) fbSave('products',state.products); });
  fbLoad('orders', d=>{ if(d&&Array.isArray(d)){ state.orders=d; localStorage.setItem('pb_orders',JSON.stringify(d)); } else if(state.orders.length>0) fbSave('orders',state.orders); });
  fbLoad('users', d=>{ if(d&&Array.isArray(d)){ state.users=d; localStorage.setItem('pb_users',JSON.stringify(d)); } else if(state.users.length>0) fbSave('users',state.users); });
  fbLoad('deposits', d=>{ if(d&&Array.isArray(d)){ state.deposits=d; localStorage.setItem('pb_deposits',JSON.stringify(d)); } else if(state.deposits.length>0) fbSave('deposits',state.deposits); });
  fbLoad('transactions', d=>{ if(d&&Array.isArray(d)){ state.transactions=d; localStorage.setItem('pb_transactions',JSON.stringify(d)); } else if(state.transactions.length>0) fbSave('transactions',state.transactions); });
  fbLoad('settings', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.settings={...DEFAULT_SETTINGS,...d[0]}; localStorage.setItem('pb_settings',JSON.stringify(state.settings)); render(); } else fbSave('settings',[state.settings]); });
}

document.addEventListener('DOMContentLoaded', ()=>{
  render();
  updateWhatsappLink();
  if(initFirebase()) startFbSync();
  else console.warn('Firebase offline — localStorage mode');
  setTimeout(()=>showWelcomeIfNeeded(), 1000);
});
</script>
</body>
</html>
