
<html lang="bn">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
<meta name="theme-color" content="#7c3aed" />
<title>Panel Bajar - Premium Mods</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700;900&family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
img,svg{max-width:100%;height:auto;display:block}
:root{
  --bg:#0b1120; --card:#1e293b; --card2:#0f172a; --border:#334155;
  --primary:#7c3aed; --primary-dark:#6d28d9; --primary-light:#a78bfa;
  --accent:#e11d48; --success:#10b981; --warning:#f59e0b; --danger:#ef4444;
  --info:#3b82f6; --bkash:#e2136e;
  --text:#f8fafc; --text-mid:#94a3b8; --muted:#64748b;
  --shadow-xs:0 1px 2px rgba(0,0,0,.4);
  --shadow-sm:0 4px 12px rgba(0,0,0,.4);
  --shadow-md:0 10px 30px rgba(0,0,0,.6);
  --shadow-neon:0 0 20px rgba(124,58,237,.4);
  --gradient-primary:linear-gradient(135deg,#7c3aed 0%,#a855f7 100%);
  --gradient-success:linear-gradient(135deg,#10b981 0%,#059669 100%);
  --gradient-danger:linear-gradient(135deg,#ef4444 0%,#dc2626 100%);
  --gradient-bkash:linear-gradient(135deg,#e2136e 0%,#be185d 100%);
  --gradient-card:linear-gradient(180deg, #1e293b 0%, #0f172a 100%);
}
html,body{width:100%;max-width:100vw;overflow-x:hidden;-webkit-tap-highlight-color:transparent}
body{font-family:'Poppins',-apple-system,sans-serif;background:var(--bg);color:var(--text);min-height:100vh;line-height:1.55;-webkit-font-smoothing:antialiased}
a{color:inherit;text-decoration:none}
button{cursor:pointer;border:none;font-family:inherit;color:inherit;background:none;outline:none}
input,select,textarea{background:var(--card2);border:1.5px solid var(--border);color:var(--text);border-radius:12px;padding:13px 16px;width:100%;font-family:inherit;font-size:14px;transition:all .2s;max-width:100%}
input:focus,select:focus,textarea:focus{outline:none;border-color:var(--primary);box-shadow:0 0 15px rgba(124,58,237,.3)}
::-webkit-scrollbar{width:6px;height:6px}::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px}

/* ============ HEADER (NOT STICKY — normal flow) ============ */
header{background:rgba(11,17,32,.95);border-bottom:1px solid var(--border);width:100%}
.header-in{max-width:600px;margin:0 auto;padding:0 12px;height:60px;display:flex;align-items:center;justify-content:space-between;gap:6px}
.logo{display:flex;align-items:center;gap:8px;cursor:pointer;min-width:0}
.logo-badge{width:38px;height:38px;border-radius:11px;background:var(--gradient-primary);display:flex;align-items:center;justify-content:center;font-weight:900;color:#fff;font-size:15px;box-shadow:var(--shadow-neon);overflow:hidden;flex-shrink:0;font-family:'Orbitron',sans-serif}
.logo-badge img{width:100%;height:100%;object-fit:cover}
.logo-name{font-family:'Orbitron',sans-serif;font-weight:800;font-size:clamp(12px,3.5vw,15px);letter-spacing:.5px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;color:#fff;text-shadow:0 0 10px rgba(124,58,237,.5)}
.header-right{display:flex;align-items:center;gap:5px;flex-shrink:0}
.balance-chip{display:flex;align-items:center;gap:4px;padding:5px 9px;border-radius:24px;background:rgba(16,185,129,.1);color:var(--success);font-weight:800;font-size:clamp(10px,2.8vw,12px);border:1px solid rgba(16,185,129,.2);white-space:nowrap;cursor:pointer;font-family:'Orbitron',sans-serif}
.status-badge{display:flex;align-items:center;gap:3px;padding:5px 8px;border-radius:20px;font-size:clamp(9px,2.4vw,10px);font-weight:700;border:1px solid transparent}
.status-badge.online{background:rgba(16,185,129,.1);color:var(--success);border-color:rgba(16,185,129,.2)}
.status-badge.offline{background:rgba(239,68,68,.1);color:var(--danger);border-color:rgba(239,68,68,.2)}
.status-dot{width:5px;height:5px;border-radius:50%;background:currentColor}
.status-badge.online .status-dot{animation:blink 1.5s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.btn-login{padding:0 14px;height:32px;border-radius:20px;font-weight:700;font-size:11px;background:var(--primary);color:#fff;box-shadow:var(--shadow-neon);transition:.2s}
.btn-login:active{transform:scale(.96)}
.btn-avatar{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;color:#fff;font-size:11px;border:2px solid var(--primary);box-shadow:var(--shadow-neon)}

/* ============ MAIN & CONTAINER ============ */
main{width:100%;padding-bottom:calc(78px + env(safe-area-inset-bottom, 0px))}
.container{max-width:600px;margin:0 auto;padding:12px 10px 8px 10px;width:100%}

.card{background:var(--gradient-card);border:1px solid var(--border);border-radius:16px;box-shadow:var(--shadow-sm);max-width:100%}
.btn-primary{background:var(--gradient-primary);color:#fff;font-weight:700;transition:.2s;box-shadow:0 4px 12px rgba(124,58,237,.25);border-radius:12px}
.btn-primary:active{transform:scale(.98)}
.btn-primary:disabled{opacity:.5;cursor:not-allowed}
.btn-success{background:var(--gradient-success);color:#fff;font-weight:700}
.btn-danger{background:var(--gradient-danger);color:#fff;font-weight:700}
.btn-bkash{background:var(--gradient-bkash);color:#fff;font-weight:700}
.btn-ghost{background:var(--card2);color:var(--text);font-weight:700;border:1.5px solid var(--border)}
.btn-full{width:100%;padding:14px;border-radius:12px;font-weight:700;font-size:15px;transition:.2s}

/* ============ AD SLIDER ============ */
.ad-slider{margin-bottom:12px;border-radius:14px;overflow:hidden;position:relative;background:var(--card2);box-shadow:var(--shadow-md);aspect-ratio:16/8;max-height:260px;border:1px solid var(--border);touch-action:pan-y;cursor:grab;user-select:none;width:100%}
.ad-slider.ad-dragging{cursor:grabbing}
.ad-track{display:flex;height:100%;transition:transform .6s cubic-bezier(.45,0,.2,1)}
.ad-track.no-anim{transition:none}
.ad-slide{flex:0 0 100%;height:100%;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center;pointer-events:none}
.ad-slide img{width:100%;height:100%;object-fit:cover}
.ad-dots{position:absolute;bottom:10px;left:50%;transform:translateX(-50%);display:flex;gap:6px;z-index:5}
.ad-dot{width:7px;height:7px;border-radius:50%;background:rgba(255,255,255,.3);cursor:pointer;transition:.3s;pointer-events:auto}
.ad-dot.active{background:var(--primary);width:22px;border-radius:4px;box-shadow:0 0 10px var(--primary)}
@media (max-width:380px){.ad-slider{aspect-ratio:16/9;max-height:200px}}

/* ============ HERO CARD ============ */
.hero-card{margin-bottom:14px;padding:18px 16px;border-radius:18px;background:linear-gradient(135deg, rgba(124,58,237,.2), rgba(225,29,72,.2));border:1px solid rgba(124,58,237,.3);color:#fff;box-shadow:var(--shadow-md);position:relative;overflow:hidden}
.hero-card::before{content:'';position:absolute;top:-40%;right:-20%;width:240px;height:240px;background:radial-gradient(circle, rgba(124,58,237,.4) 0%, transparent 70%);border-radius:50%}
.hero-content{position:relative;z-index:2}
.hero-label{font-size:12px;opacity:.85;font-weight:600;letter-spacing:.5px;text-transform:uppercase}
.hero-balance{font-family:'Orbitron',sans-serif;font-size:clamp(26px,8vw,34px);font-weight:900;margin:4px 0 2px;letter-spacing:1px;text-shadow:0 0 20px rgba(255,255,255,.2)}
.hero-actions{display:flex;gap:8px;margin-top:14px;flex-wrap:wrap}
.hero-btn{padding:9px 16px;border-radius:10px;background:rgba(255,255,255,.1);color:#fff;font-weight:700;font-size:12px;backdrop-filter:blur(8px);border:1px solid rgba(255,255,255,.2);transition:.2s}
.hero-btn:active{transform:scale(.97)}
.hero-btn.solid{background:#fff;color:var(--primary)}

/* ============ TABS ============ */
.tabs{display:flex;gap:6px;margin:10px 0 10px;overflow-x:auto;scrollbar-width:none;padding-bottom:3px;width:100%}
.tabs::-webkit-scrollbar{display:none}
.tab{padding:8px 13px;border-radius:10px;font-size:clamp(11px,3vw,12.5px);font-weight:700;background:var(--card);border:1.5px solid var(--border);transition:.2s;color:var(--text-mid);flex-shrink:0;white-space:nowrap}
.tab.active{background:var(--primary);color:#fff;border-color:transparent;box-shadow:var(--shadow-neon)}

/* ============ PRODUCT GRID — BIGGER CARDS, 1:1 IMAGE ============ */
.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;width:100%;max-width:100%;margin:0 0 8px 0}

.prod-card{
  display:flex;flex-direction:column;
  width:100%;min-width:0;max-width:100%;height:100%;
  border-radius:14px;overflow:hidden;
  background:var(--card);border:1px solid var(--border);
  transition:transform .2s ease, border-color .2s ease, box-shadow .2s ease;
}
.prod-card:active{transform:scale(.985);border-color:var(--primary)}

/* 1:1 Square Image — বড় ও পরিষ্কার */
.prod-img{
  width:100%;aspect-ratio:1/1;overflow:hidden;
  background:#0a0f1a;position:relative;
  display:flex;align-items:center;justify-content:center;
  flex-shrink:0;
}
.prod-img img{width:100%;height:100%;object-fit:cover;object-position:center;display:block}
.prod-img > span{font-size:clamp(48px,15vw,72px);line-height:1}
.badge-sale,.badge-antiban{font-size:9px;padding:3px 8px;top:8px;border-radius:999px}
.badge-sale{right:8px;background:var(--gradient-danger);color:#fff;box-shadow:0 2px 5px rgba(0,0,0,.5);font-weight:800;position:absolute}
.badge-antiban{left:8px;background:var(--gradient-success);color:#fff;box-shadow:0 2px 5px rgba(0,0,0,.5);font-weight:800;position:absolute}

.prod-body{padding:10px 11px 11px 11px;display:flex;flex-direction:column;flex:1;min-height:0;min-width:0;gap:0}

.prod-name{
  font-size:clamp(12px,3.4vw,13.5px);font-weight:800;
  line-height:1.3;margin:0 0 4px 0;color:var(--text);
  display:-webkit-box;-webkit-line-clamp:2;line-clamp:2;
  -webkit-box-orient:vertical;overflow:hidden;
  word-break:break-word;overflow-wrap:anywhere;
  min-height:calc(2 * 1.3em);
}
.prod-desc{
  font-size:clamp(10px,2.8vw,11px);line-height:1.35;
  color:var(--text-mid);margin:0 0 6px 0;
  display:-webkit-box;-webkit-line-clamp:2;line-clamp:2;
  -webkit-box-orient:vertical;overflow:hidden;
  word-break:break-word;min-height:calc(2 * 1.35em);
}
.price-row{display:flex;align-items:center;gap:5px;margin:0 0 8px 0;flex-wrap:wrap;min-height:20px}
.price{font-size:clamp(14px,4vw,16px);font-weight:800;color:var(--success);font-family:'Orbitron',sans-serif;letter-spacing:.3px}
.old-price{font-size:clamp(9px,2.6vw,10.5px);color:var(--muted);text-decoration:line-through}

.prod-btns{display:flex;gap:5px;margin-top:auto;width:100%}
.btn-prod{
  flex:1 1 0;min-width:0;padding:8px 3px;
  border-radius:8px;font-size:clamp(9.5px,2.8vw,11px);
  font-weight:700;line-height:1.1;
  display:inline-flex;align-items:center;justify-content:center;gap:3px;
  white-space:nowrap;overflow:hidden;text-overflow:ellipsis;
  transition:transform .15s ease;
}
.btn-prod:active{transform:scale(.96)}
.btn-prod svg{width:10px;height:10px;flex-shrink:0}
.btn-setup{background:var(--card2);color:var(--text);border:1px solid var(--border)}
.btn-buy{background:var(--primary);color:#fff;box-shadow:0 2px 8px rgba(124,58,237,.35)}

/* ============ LIST ITEMS ============ */
.list-item{display:flex;align-items:center;gap:12px;padding:13px;margin-bottom:8px;border-radius:14px;background:var(--card);border:1px solid var(--border);box-shadow:var(--shadow-xs);transition:.2s}
.list-icon{width:40px;height:40px;border-radius:11px;display:flex;align-items:center;justify-content:center;font-size:20px;background:var(--card2);flex-shrink:0}
.list-body{flex:1;min-width:0;overflow:hidden}
.list-title{font-weight:700;font-size:clamp(12px,3.4vw,14px);word-break:break-word;overflow-wrap:anywhere}
.list-sub{font-size:clamp(10px,2.8vw,11px);color:var(--text-mid);margin-top:3px;word-break:break-word}
.badge{font-size:11px;padding:3px 10px;border-radius:999px;font-weight:700;display:inline-block}
.badge-green{background:rgba(16,185,129,.12);color:var(--success);border:1px solid rgba(16,185,129,.2)}
.badge-amber{background:rgba(245,158,11,.12);color:var(--warning);border:1px solid rgba(245,158,11,.2)}
.badge-red{background:rgba(239,68,68,.12);color:var(--danger);border:1px solid rgba(239,68,68,.2)}

.stat-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;margin-bottom:14px}
.stat{padding:14px 12px;border-radius:14px;background:var(--card);border:1px solid var(--border);box-shadow:var(--shadow-xs);position:relative;overflow:hidden}
.stat::before{content:'';position:absolute;top:0;left:0;width:4px;height:100%;background:var(--primary)}
.stat.green::before{background:var(--success)}
.stat.amber::before{background:var(--warning)}
.stat.blue::before{background:var(--info)}
.stat-label{font-size:clamp(10px,2.6vw,11px);text-transform:uppercase;color:var(--text-mid);font-weight:700;letter-spacing:.5px}
.stat-val{font-family:'Orbitron',sans-serif;font-size:clamp(17px,4.8vw,21px);font-weight:900;margin-top:4px}

.page-title{font-family:'Orbitron',sans-serif;font-size:clamp(18px,5vw,23px);font-weight:900;margin-bottom:14px;letter-spacing:-.5px;word-break:break-word;overflow-wrap:anywhere}

/* ============ MODAL ============ */
.modal{position:fixed;inset:0;z-index:50;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,.85);backdrop-filter:blur(6px);padding:max(16px, env(safe-area-inset-top,0px) + 8px) 16px max(16px, env(safe-area-inset-bottom,0px) + 8px)}
.modal.show{display:flex;animation:fadeIn .2s}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
.modal-card{background:var(--bg);border:1px solid var(--border);border-radius:20px;padding:22px;width:100%;max-width:440px;max-height:calc(100dvh - 32px);max-height:calc(100vh - 32px);overflow-y:auto;box-shadow:0 25px 60px -12px rgba(0,0,0,.8);position:relative;animation:scaleIn .2s}
@keyframes scaleIn{from{transform:scale(.95);opacity:0}to{transform:scale(1);opacity:1}}
.modal-title{font-size:clamp(17px,4.5vw,20px);font-weight:900;text-align:center;margin-bottom:18px;letter-spacing:-.3px}
.modal-close{position:absolute;top:14px;right:14px;color:var(--text-mid);font-size:18px;background:var(--card2);width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;transition:.2s}
.modal-close:active{background:var(--border)}
.field{margin-bottom:14px}
.field label{font-size:12px;color:var(--text-mid);display:block;margin-bottom:6px;font-weight:700}
.auth-toggle{text-align:center;font-size:13px;color:var(--text-mid);margin-top:14px}
.auth-toggle button{color:var(--primary);font-weight:700;padding:4px}

.plan-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:8px;margin:12px 0}
.plan{padding:12px;border-radius:12px;border:2px solid var(--border);background:var(--card2);cursor:pointer;transition:.2s;text-align:center}
.plan.active{border-color:var(--primary);background:rgba(124,58,237,.1);box-shadow:0 0 15px rgba(124,58,237,.2)}
.plan.disabled{opacity:.45;cursor:not-allowed;background:var(--bg)}
.plan-dur{font-size:clamp(12px,3.2vw,14px);font-weight:800}
.plan-price{font-family:'Orbitron',sans-serif;font-size:clamp(15px,4vw,18px);font-weight:900;color:var(--success);margin-top:3px}
.plan-stock{font-size:clamp(9px,2.5vw,10px);color:var(--text-mid);margin-top:3px;font-weight:600}

.bkash-box{padding:14px;border-radius:12px;background:rgba(226,19,110,.05);border:2px dashed var(--bkash);margin-top:14px}
.bkash-num-row{display:flex;align-items:center;justify-content:space-between;gap:8px;margin-top:8px;background:var(--card2);padding:10px 12px;border-radius:10px;flex-wrap:wrap}
.bkash-num{font-family:monospace;font-size:clamp(14px,4vw,18px);font-weight:800;color:var(--bkash);letter-spacing:1px;word-break:break-all}
.btn-copy{padding:7px 12px;border-radius:9px;font-size:11px;font-weight:700;background:var(--bkash);color:#fff;white-space:nowrap}

.toast{position:fixed;top:20px;left:50%;transform:translateX(-50%);background:var(--text);color:var(--bg);padding:11px 22px;border-radius:999px;z-index:100;animation:slideDown .3s;font-weight:600;font-size:13px;box-shadow:var(--shadow-md);max-width:90vw;text-align:center}
@keyframes slideDown{from{opacity:0;transform:translate(-50%,-20px)}to{opacity:1;transform:translate(-50%,0)}}

.empty{text-align:center;padding:40px 16px;color:var(--text-mid);display:flex;flex-direction:column;align-items:center}
.empty-icon{font-size:clamp(42px,11vw,56px);margin-bottom:12px;opacity:.6}

.notif{padding:9px 13px;font-size:clamp(11px,3vw,12px);font-weight:500;background:var(--gradient-danger);color:#fff;overflow:hidden;margin-bottom:10px;border-radius:10px;box-shadow:0 4px 12px rgba(239,68,68,.2);width:100%}
.marquee{white-space:nowrap;animation:marquee 22s linear infinite}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
.offer-bar{margin-bottom:10px;border-radius:10px;overflow:hidden;background:linear-gradient(90deg,#7c3aed,#e11d48,#7c3aed);background-size:200% 100%;animation:offerGradient 4s linear infinite;box-shadow:var(--shadow-neon);width:100%}
@keyframes offerGradient{0%{background-position:0% 50%}100%{background-position:200% 50%}}
.offer-inner{display:flex;align-items:center;gap:8px;padding:9px 13px;color:#fff;font-size:clamp(11px,3vw,12.5px);font-weight:600}
.offer-marquee{overflow:hidden;flex:1;white-space:nowrap}
.offer-marquee span{display:inline-block;padding-left:100%;animation:offerScroll 18s linear infinite}
@keyframes offerScroll{0%{transform:translateX(0)}100%{transform:translateX(-100%)}}

.live-feed{margin-bottom:12px}
.live-feed-head{display:flex;align-items:center;gap:8px;margin-bottom:8px}
.live-dot{width:9px;height:9px;border-radius:50%;background:var(--success);animation:blink 1.5s infinite;box-shadow:0 0 10px rgba(16,185,129,.6)}
.live-feed-title{font-size:13px;font-weight:800}
.live-item{display:flex;align-items:center;gap:10px;padding:9px 11px;border-radius:12px;background:var(--card);border:1px solid var(--border);box-shadow:var(--shadow-xs);font-size:13px;margin-bottom:6px}
.live-avatar{width:30px;height:30px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:800;color:#fff;font-size:10px;flex-shrink:0}
.live-body{flex:1;min-width:0}
.live-text{font-size:clamp(10.5px,2.9vw,12px);line-height:1.35;color:var(--text-mid);word-break:break-word;overflow-wrap:anywhere}
.live-text strong{color:var(--text);font-weight:700}
.live-time{font-size:9.5px;color:var(--muted);margin-top:1px}

.social-bar{display:flex;gap:8px;margin:10px 0 2px 0;width:100%}
.social-bar a{flex:1;padding:11px;border-radius:11px;font-size:clamp(11px,3vw,12.5px);font-weight:700;color:#fff;display:flex;align-items:center;justify-content:center;gap:6px;box-shadow:var(--shadow-md);transition:.2s}
.social-bar a:active{transform:scale(.97)}
.social-bar .tg{background:linear-gradient(135deg,#26a5e4,#1a8ec7)}
.social-bar .yt{background:linear-gradient(135deg,#ff0000,#cc0000)}
@media (max-width:340px){.social-bar{flex-direction:column;gap:6px}}

.key-box{margin-top:10px;padding:12px;border-radius:11px;background:rgba(16,185,129,.06);border:1.5px solid rgba(16,185,129,.3);width:100%}
.key-box-head{display:flex;align-items:center;gap:6px;font-size:11px;font-weight:900;color:var(--success);text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px}
.key-content{font-family:monospace;font-size:12px;white-space:pre-wrap;word-break:break-all;background:#000;padding:11px;border-radius:10px;border:1px solid var(--border);line-height:1.7;max-height:180px;overflow-y:auto;color:#fff}
.key-copy-row{display:flex;gap:8px;margin-top:9px}
.key-copy-btn{flex:1;padding:10px;border-radius:10px;font-size:12px;font-weight:700;background:var(--gradient-success);color:#fff;transition:.2s}

.welcome-modal{position:fixed;inset:0;z-index:60;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,.85);backdrop-filter:blur(8px);padding:max(16px,env(safe-area-inset-top,0px)+8px) 16px max(16px,env(safe-area-inset-bottom,0px)+8px)}
.welcome-modal.show{display:flex;animation:fadeIn .3s}
.welcome-card{background:var(--bg);border:1px solid var(--border);border-radius:20px;padding:0;width:100%;max-width:440px;max-height:calc(100dvh - 32px);overflow-y:auto;box-shadow:0 25px 60px -12px rgba(0,0,0,.8);position:relative;animation:scaleIn .3s}
.welcome-img{width:100%;aspect-ratio:16/9;object-fit:cover;display:block;background:var(--bg)}
.welcome-body{padding:18px}
.welcome-text{font-size:clamp(13px,3.6vw,15px);color:var(--text-mid);line-height:1.6;text-align:center;margin-bottom:14px}
.welcome-btn{display:flex;align-items:center;justify-content:center;gap:8px;width:100%;padding:13px;border-radius:11px;background:var(--gradient-primary);color:#fff;font-weight:700;font-size:clamp(13px,3.6vw,15px);text-decoration:none;margin-bottom:10px;box-shadow:var(--shadow-neon)}
.welcome-close{width:100%;padding:11px;border-radius:11px;background:var(--card2);color:var(--text-mid);font-weight:700;font-size:13px}

/* ============ WHATSAPP FAB ============ */
.whatsapp-fab{position:fixed;bottom:calc(86px + env(safe-area-inset-bottom,0px));right:12px;width:48px;height:48px;border-radius:50%;background:linear-gradient(135deg,#25D366,#128C7E);color:#fff;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 24px rgba(37,211,102,.45);z-index:49;transition:transform .1s}
.whatsapp-fab svg{width:24px;height:24px}
.whatsapp-fab:active{transform:scale(.95)}

/* ============ BOTTOM NAV (FIXED) ============ */
nav.botnav{
  position:fixed; bottom:calc(8px + env(safe-area-inset-bottom,0px)); left:50%; transform:translateX(-50%);
  width:calc(100% - 16px); max-width:440px;
  background:rgba(30,41,59,.92); backdrop-filter:blur(20px); -webkit-backdrop-filter:blur(20px);
  border:1px solid rgba(255,255,255,.1); border-radius:28px;
  box-shadow:0 10px 30px rgba(0,0,0,.6), inset 0 1px 0 rgba(255,255,255,.1);
  z-index:50;
}
.botnav-in{display:grid;grid-template-columns:repeat(5,1fr);height:60px;align-items:center;padding:0 4px;position:relative}
.navbtn{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:2px;font-size:clamp(9px,2.4vw,10px);color:var(--text-mid);transition:.3s;font-weight:600;height:100%;position:relative;background:none;border:none;cursor:pointer}
.navbtn.active{color:var(--primary)}
.navbtn.active svg{stroke:var(--primary);filter:drop-shadow(0 0 5px rgba(124,58,237,.5))}
.navbtn svg{width:19px;height:19px;transition:.3s}

.navbtn-wallet-wrap{position:relative;display:flex;flex-direction:column;align-items:center;justify-content:center;height:100%;width:100%;cursor:pointer}
.navbtn-wallet-circle{
  position:absolute;top:-19px;width:48px;height:48px;border-radius:50%;
  background:linear-gradient(135deg,#10b981,#059669);
  color:#fff;display:flex;align-items:center;justify-content:center;
  box-shadow:0 8px 20px rgba(16,185,129,.4), inset 0 2px 0 rgba(255,255,255,.3);
  border:2.5px solid var(--bg);
  transition:transform .2s;
}
.navbtn-wallet-circle:active{transform:scale(.95)}
.navbtn-wallet-circle svg{width:22px;height:22px;stroke-width:3}
.navbtn-wallet-label{margin-top:30px;font-size:clamp(8px,2.2vw,9px);color:var(--success);font-weight:700;letter-spacing:.4px}

/* ============ TABLET & DESKTOP ============ */
@media (min-width:480px){
  .container{max-width:560px;padding:16px 14px 8px}
  .header-in{max-width:560px}
  .grid{gap:12px}
}
@media (min-width:640px){
  .container{max-width:680px;padding:18px 16px 8px}
  .header-in{max-width:680px;padding:0 16px}
  .grid{gap:14px}
  .prod-name{-webkit-line-clamp:2;line-clamp:2;font-size:13.5px}
  .prod-desc{font-size:11.5px}
}
@media (min-width:768px){
  .container{max-width:760px}
  .header-in{max-width:760px}
  nav.botnav{max-width:480px}
}
@media (min-width:900px){
  .grid{grid-template-columns:repeat(3,minmax(0,1fr));gap:14px}
}

/* ============ SMALL SCREENS ============ */
@media (max-width:340px){
  .container{padding-left:8px;padding-right:8px}
  .grid{gap:7px}
  .prod-body{padding:9px 10px 10px}
  .prod-name{font-size:11.5px}
  .prod-desc{font-size:9.5px;-webkit-line-clamp:1;line-clamp:1;min-height:auto}
  .price{font-size:13px}
  .btn-prod{font-size:9px;padding:7px 2px}
  .prod-btns{gap:4px}
  .logo-name{display:none}
  .status-badge{display:none}
}
@media (max-width:320px){
  .grid{gap:6px}
  .prod-btns{flex-direction:column;gap:4px}
  .btn-prod{width:100%;font-size:9px}
}

/* iOS input zoom fix */
@media (max-width:480px){
  input,select,textarea{font-size:16px;padding:12px 14px}
}

/* Reduce motion */
@media (prefers-reduced-motion:reduce){
  .marquee,.offer-marquee span,.status-badge.online .status-dot,.live-dot{animation:none !important}
}

/* Landscape */
@media (max-height:500px) and (orientation:landscape){
  .ad-slider{max-height:160px;aspect-ratio:21/9}
  .hero-balance{font-size:22px}
}
</style>
</head>
<body>

<header><div class="header-in">
  <div class="logo" onclick="handleLogoClick()">
    <div class="logo-badge" id="logoBadge">PB</div>
    <span class="logo-name" id="siteName">PANEL BAJAR</span>
  </div>
  <div class="header-right" id="headerRight"></div>
</div></header>

<main><div class="container" id="main"></div></main>

<nav class="botnav">
  <div class="botnav-in">
    <button class="navbtn" data-page="home" onclick="nav('home')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 12l9-9 9 9M5 10v10h14V10"/></svg>
      হোম
    </button>
    <button class="navbtn" data-page="orders" onclick="nav('orders')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M6 2l1 4h12l-2 8H8L6 2zM6 2H4M9 18a1 1 0 100 2 1 1 0 000-2zM17 18a1 1 0 100 2 1 1 0 000-2z"/></svg>
      My Order
    </button>
    <div class="navbtn-wallet-wrap" onclick="nav('wallet')">
      <div class="navbtn-wallet-circle">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path d="M12 5v14M5 12h14"/></svg>
      </div>
      <span class="navbtn-wallet-label">ADD FUND</span>
    </div>
    <button class="navbtn" data-page="keys" onclick="nav('keys')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M15 7a2 2 0 012 2m4 0a6 6 0 01-7.743 5.743L11 17H9v2H7v2H4a1 1 0 01-1-1v-2.586a1 1 0 01.293-.707l5.964-5.964A6 6 0 1121 9z"/></svg>
      My Keys
    </button>
    <button class="navbtn" data-page="account" onclick="nav('account')">
      <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4 4-7 8-7s8 3 8 7"/></svg>
      Account
    </button>
  </div>
</nav>

<div class="modal" id="modal" onclick="if(event.target===this)closeModal()"><div class="modal-card" id="modalContent"></div></div>
<div class="modal" id="authModal" onclick="if(event.target===this)closeAuth()"><div class="modal-card" id="authContent" style="max-width:400px"></div></div>
<div class="welcome-modal" id="welcomeModal" onclick="if(event.target===this)closeWelcome()"><div class="welcome-card" id="welcomeContent"></div></div>

<a href="#" id="whatsappFab" class="whatsapp-fab" target="_blank">
  <svg viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/></svg>
</a>

<script>
var FIREBASE_CONFIG = {
  apiKey: "AIzaSyDt3gU-2iubzCZ94XFAGZswUnzxuDgUvFQ",
  authDomain: "free-fire-panel-611d6.firebaseapp.com",
  projectId: "free-fire-panel-611d6",
  storageBucket: "free-fire-panel-611d6.firebasestorage.app",
  messagingSenderId: "374641641780",
  appId: "1:374641641780:web:c87d374edf2371dae47d61"
};
var TELEGRAM_CONFIG = {
  botToken: "8842406650:AAESk-VLFq7qwOT2i14SuRAqWDIhNkQ7GNc",
  chatId: "7427334644"
};
</script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>
<script>
let fbDb=null, fbConnected=false, fbSyncStarted=false;
function initFirebase(){
  try{
    if(typeof firebase==='undefined'||fbConnected) return fbConnected;
    if(!firebase.apps.length) firebase.initializeApp(FIREBASE_CONFIG);
    fbDb=firebase.firestore(); fbConnected=true; return true;
  }catch(e){ console.warn(e); return false; }
}
function fbDoc(col){ return fbDb.collection(col).doc('main'); }
function fbSave(col, arr){ if(!fbConnected) return; try{ fbDoc(col).set({data:JSON.stringify(arr), updatedAt:new Date().toISOString()}).catch(e=>console.warn(e)); }catch(e){} }
function fbLoad(col, cb){ if(!fbConnected){ cb && cb(null); return; } try{ fbDoc(col).get().then(doc=>{ if(doc.exists){ try{ cb && cb(JSON.parse(doc.data().data||'[]')); }catch(e){ cb && cb(null); } } else cb && cb(null); }).catch(()=>cb && cb(null)); }catch(e){ cb && cb(null); } }
function fbListen(col, cb){ if(!fbConnected) return; try{ fbDoc(col).onSnapshot(doc=>{ if(doc.exists){ try{ cb && cb(JSON.parse(doc.data().data||'[]')); }catch(e){} } }); }catch(e){} }

const DEFAULT_SETTINGS = {
  site_name:'Panel Bajar', tagline:'Buy Premium Mods & Hacks',
  notification:'স্বাগতম Panel Bajar-এ!', notif_active:true,
  offer_text:'🔥 MEGA অফার! সব প্রোডাক্টে ৫০% ছাড়!', offer_active:true,
  telegram:'https://t.me/panelbajar', youtube:'https://youtube.com/@panelbajar',
  bkash_number:'01XXXXXXXXX', help_url:'https://t.me/panelbajar',
  ads:[], ad_delay:3000, is_online:true, logo_url:'#', logo_image:'',
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
  page:'home', productTab:'NON_ROOT', authMode:'login'
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
function fmt(n){ return '৳'+Number(n||0).toFixed(0); }
function tAgo(d){ try{ return new Date(d).toLocaleString('bn-BD'); }catch(e){ return ''; } }
function timeAgoShort(d){ const diff=Date.now()-new Date(d).getTime(); const m=Math.floor(diff/60000); if(m<1) return 'এইমাত্র'; if(m<60) return m+' মিনিট আগে'; const h=Math.floor(m/60); if(h<24) return h+' ঘন্টা আগে'; return Math.floor(h/24)+' দিন আগে'; }
function toast(m){ const t=document.createElement('div'); t.className='toast'; t.textContent=m; document.body.appendChild(t); setTimeout(()=>t.remove(),3000); }
function copyText(t){ if(navigator.clipboard){ navigator.clipboard.writeText(t).then(()=>toast('✓ কপি হয়েছে')).catch(()=>fallbackCopy(t)); } else fallbackCopy(t); }
function fallbackCopy(t){ const ta=document.createElement('textarea'); ta.value=t; ta.style.position='fixed'; ta.style.opacity='0'; document.body.appendChild(ta); ta.select(); try{ document.execCommand('copy'); toast('✓ কপি হয়েছে'); }catch(e){} document.body.removeChild(ta); }

function sendTelegramNotification(order, product, keyContent){
  const token = (TELEGRAM_CONFIG.botToken && TELEGRAM_CONFIG.botToken!=='YOUR_BOT_TOKEN_HERE') ? TELEGRAM_CONFIG.botToken : state.settings.telegram_bot_token;
  const chatId = (TELEGRAM_CONFIG.chatId && TELEGRAM_CONFIG.chatId!=='YOUR_CHAT_ID_HERE') ? TELEGRAM_CONFIG.chatId : state.settings.telegram_chat_id;
  if(!token||!chatId) return;
  const statusEmoji = order.status === 'COMPLETED' ? '✅' : '⏳';
  const keyInfo = keyContent ? `\n\n🔑 <b>Keys Delivered:</b>\n<pre>${esc(keyContent)}</pre>` : '\n\n⚠️ <b>কী স্টক শেষ!</b>';
  const msg = `${statusEmoji} <b>New Order — ${order.status}</b>\n\n📦 <b>Product:</b> ${product?product.name:'Unknown'}\n⏱ <b>Plan:</b> ${order.planDur}\n💰 <b>Amount:</b> ${order.price} BDT\n🔢 <b>Qty:</b> ${order.qty}\n🆔 <b>Txn:</b> <code>${order.txnId}</code>\n\n👤 <b>User:</b> ${order.username||state.user?.username}\n📧 <b>Email:</b> ${order.email||state.user?.email}${keyInfo}`;
  fetch(`https://api.telegram.org/bot${token}/sendMessage`,{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({chat_id:chatId,text:msg,parse_mode:'HTML'})}).catch(e=>console.warn(e));
}

function sendDepositTelegramNotification(dep){
  const token = (TELEGRAM_CONFIG.botToken && TELEGRAM_CONFIG.botToken!=='YOUR_BOT_TOKEN_HERE') ? TELEGRAM_CONFIG.botToken : state.settings.telegram_bot_token;
  const chatId = (TELEGRAM_CONFIG.chatId && TELEGRAM_CONFIG.chatId!=='YOUR_CHAT_ID_HERE') ? TELEGRAM_CONFIG.chatId : state.settings.telegram_chat_id;
  if(!token||!chatId) return;
  const msg = `💰 <b>New Add Balance Request!</b>\n\n👤 <b>User:</b> ${esc(dep.username)}\n📧 <b>Email:</b> ${esc(dep.email)}\n\n💵 <b>Amount:</b> ${fmt(dep.amount)}\n🆔 <b>TxnID:</b> <code>${esc(dep.txnId)}</code>\n${dep.note ? `\n📝 <b>Note:</b> ${esc(dep.note)}\n` : ''}\n⏳ <i>Please approve it from Admin Panel.</i>`;
  fetch(`https://api.telegram.org/bot${token}/sendMessage`,{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({chat_id:chatId,text:msg,parse_mode:'HTML'})}).catch(e=>console.warn(e));
}

function sendLowStockAlert(productName, planDur, remaining){
  const token = (TELEGRAM_CONFIG.botToken && TELEGRAM_CONFIG.botToken!=='YOUR_BOT_TOKEN_HERE') ? TELEGRAM_CONFIG.botToken : state.settings.telegram_bot_token;
  const chatId = (TELEGRAM_CONFIG.chatId && TELEGRAM_CONFIG.chatId!=='YOUR_CHAT_ID_HERE') ? TELEGRAM_CONFIG.chatId : state.settings.telegram_chat_id;
  if(!token||!chatId) return;
  const msg = `⚠️ <b>Low Stock Alert!</b>\n\n📦 <b>Product:</b> ${productName}\n⏱ <b>Plan:</b> ${planDur}\n🔑 <b>Remaining:</b> ${remaining}\n\n⚡ অ্যাডমিন প্যানেল থেকে কী রিফিল করুন।`;
  fetch(`https://api.telegram.org/bot${token}/sendMessage`,{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({chat_id:chatId,text:msg,parse_mode:'HTML'})}).catch(e=>console.warn(e));
}

function getBalance(userId){
  const u = state.users.find(x=>x.id===userId);
  return u ? Number(u.balance||0) : 0;
}
function addBalance(userId, amount, meta){
  const u = state.users.find(x=>x.id===userId);
  if(!u) return false;
  u.balance = Number(u.balance||0) + Number(amount||0);
  state.transactions.push({
    id: uid(), userId, type: meta.type||'credit', amount: Number(amount),
    balanceAfter: u.balance, description: meta.description||'',
    refId: meta.refId||'', createdAt: new Date().toISOString()
  });
  if(state.user && state.user.id===userId){
    state.user.balance = u.balance;
    localStorage.setItem('pb_user', JSON.stringify(state.user));
  }
  pushCol('users');
  pushCol('transactions');
  return true;
}

function getAvailableKeys(product, planDur){
  if(!product) return [];
  if(planDur && Array.isArray(product.plans)){
    const plan = product.plans.find(p=>p.dur===planDur);
    if(plan && Array.isArray(plan.keys)){
      return plan.keys.filter(k => {
        if(!k) return false;
        if(typeof k === 'string') return k.trim() !== '';
        if(typeof k === 'object') return k.status !== 'USED' && (k.code || k.value);
        return false;
      });
    }
    return [];
  }
  if(!Array.isArray(product.keys)) return [];
  return product.keys.filter(k => {
    if(!k) return false;
    if(typeof k === 'string') return k.trim() !== '';
    if(typeof k === 'object') return k.status !== 'USED' && (k.code || k.value);
    return false;
  });
}
function getKeyText(k){
  if(typeof k === 'string') return k.trim();
  if(k && typeof k === 'object') return String(k.code || k.value || '').trim();
  return '';
}
function reserveKeys(product, qty, planDur){
  const available = getAvailableKeys(product, planDur);
  if(available.length < qty) return null;
  const reserved = available.slice(0, qty);
  const texts = reserved.map(getKeyText).filter(Boolean);
  reserved.forEach(k=>{ if(typeof k==='object') k.status='USED'; });
  if(planDur && Array.isArray(product.plans)){
    const plan = product.plans.find(p=>p.dur===planDur);
    if(plan && Array.isArray(plan.keys)){
      plan.keys = plan.keys.filter(k=>{
        if(!k) return false;
        if(typeof k==='string') return !reserved.includes(k);
        if(typeof k==='object') return k.status !== 'USED';
        return true;
      });
    }
  } else if(Array.isArray(product.keys)){
    product.keys = product.keys.filter(k=>{
      if(!k) return false;
      if(typeof k==='string') return !reserved.includes(k);
      if(typeof k==='object') return k.status !== 'USED';
      return true;
    });
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

function showWelcomeIfNeeded(){
  const s = state.settings;
  if(!s.welcome_active) return;
  if(sessionStorage.getItem('pb_welcome_shown')==='1') return;
  if(!s.welcome_image && !s.welcome_text && !s.welcome_link) return;
  
  const html = `
    <button class="modal-close" style="position:absolute;top:12px;right:12px;z-index:10;background:rgba(30,41,59,.9);box-shadow:0 2px 8px rgba(0,0,0,.3);width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:15px;color:#fff" onclick="closeWelcome()">✕</button>
    ${s.welcome_image?`<img src="${esc(s.welcome_image)}" class="welcome-img" alt="Welcome" onerror="this.style.display='none'">`:''}
    <div class="welcome-body">
      ${s.welcome_text?`<div class="welcome-text">${esc(s.welcome_text)}</div>`:''}
      ${s.welcome_link?`<a href="${esc(s.welcome_link)}" target="_blank" class="welcome-btn">▶️ ভিডিও দেখুন</a>`:''}
      <button class="welcome-close" onclick="closeWelcome()">বন্ধ করুন</button>
    </div>`;
  $('welcomeContent').innerHTML = html;
  $('welcomeModal').classList.add('show');
  sessionStorage.setItem('pb_welcome_shown','1');
}
function closeWelcome(){ $('welcomeModal').classList.remove('show'); }

function openAuth(mode){ state.authMode=mode||'login'; renderAuth(); $('authModal').classList.add('show'); }
function closeAuth(){ $('authModal').classList.remove('show'); }
function toggleAuthMode(){ state.authMode = state.authMode==='login'?'register':'login'; renderAuth(); }
function renderAuth(){
  const isL=state.authMode==='login';
  $('authContent').innerHTML = `
    <button class="modal-close" onclick="closeAuth()">✕</button>
    <h2 class="modal-title">${isL?'🔐 লগইন':'✨ রেজিস্টার'}</h2>
    <div class="field" style="display:${isL?'none':'block'}"><label>ইউজারনেম</label><input id="authUsername" placeholder="আপনার নাম" /></div>
    <div class="field"><label>ইমেইল</label><input id="authEmail" type="email" placeholder="email@example.com" /></div>
    <div class="field"><label>পাসওয়ার্ড</label><input id="authPassword" type="password" placeholder="••••••••" onkeydown="if(event.key==='Enter')doAuth()" /></div>
    <button class="btn-primary btn-full" onclick="doAuth()">${isL?'লগইন':'রেজিস্টার'}</button>
    <p class="auth-toggle">${isL?'অ্যাকাউন্ট নেই?':'ইতিমধ্যে আছে?'}<button onclick="toggleAuthMode()">${isL?'রেজিস্টার':'লগইন'}</button></p>`;
}
function doAuth(){
  const e=($('authEmail').value||'').trim().toLowerCase(); const p=$('authPassword').value;
  if(!e||!p){ toast('সব ঘর পূরণ করুন'); return; }
  if(state.authMode==='register'){
    const u=($('authUsername').value||'').trim();
    if(!u){ toast('ইউজারনেম দিন'); return; }
    if(state.users.find(x=>x.email===e)){ toast('এই ইমেইল ইতিমধ্যে ব্যবহৃত'); return; }
    const colors=['#ec4899','#7c3aed','#06b6d4','#f97316','#10b981'];
    const nu={id:uid(),email:e,username:u,password:p,role:'USER',balance:0,totalOrders:0,totalSpent:0,banned:false,avatarColor:colors[Math.floor(Math.random()*colors.length)],createdAt:new Date().toISOString()};
    state.users.push(nu); state.user=nu; saveLocal(); pushCol('users'); closeAuth(); toast('✓ অ্যাকাউন্ট তৈরি হয়েছে!'); render();
  } else {
    const u=state.users.find(x=>x.email===e);
    if(!u||u.password!==p){ toast('ইমেইল/পাসওয়ার্ড ভুল'); return; }
    if(u.banned){ toast('অ্যাকাউন্ট ব্যান করা'); return; }
    state.user=u; saveLocal(); closeAuth(); toast('স্বাগতম!'); render();
  }
}
function logout(){ state.user=null; saveLocal(); toast('লগআউট হয়েছে'); nav('home'); }

function nav(p){
  if(!state.user && ['wallet','orders','account','keys'].includes(p)){ openAuth('login'); return; }
  state.page=p; render();
}
function openModal(html){ $('modalContent').innerHTML=html; $('modal').classList.add('show'); }
function closeModal(){ $('modal').classList.remove('show'); }

function generateLiveFeed(){
  const real = state.orders.slice().reverse().slice(0,6).map(o=>{ 
    const u=state.users.find(x=>x.id===o.userId); 
    const p=state.products.find(x=>x.id===o.productId); 
    return {user:u?.username||'User',color:u?.avatarColor||'#7c3aed',product:p?.name||'Product',icon:p?.icon||'🎮',time:o.createdAt,real:true}; 
  });
  const demoNames=[['Rahim','#ec4899'],['Karim','#7c3aed'],['Sadia','#06b6d4'],['Tanvir','#f97316'],['Nusrat','#10b981']];
  const demoProducts=state.products.filter(p=>p.status==='ACTIVE');
  if(demoProducts.length===0) return real;
  const demo=[];
  for(let i=0;i<3;i++){ 
    const n=demoNames[Math.floor(Math.random()*demoNames.length)]; 
    const p=demoProducts[Math.floor(Math.random()*demoProducts.length)]; 
    demo.push({user:n[0],color:n[1],product:p.name,icon:p.icon,time:new Date(Date.now()-Math.floor(Math.random()*3600000)).toISOString(),real:false}); 
  }
  return [...real,...demo].sort((a,b)=>new Date(b.time)-new Date(a.time)).slice(0,6);
}
function renderLiveFeedItems(){
  const items=generateLiveFeed();
  if(items.length===0) return '<div style="text-align:center;padding:14px;color:var(--muted);font-size:12px">এখনো কোনো অর্ডার নেই</div>';
  return items.map(it=>`<div class="live-item"><div class="live-avatar" style="background:${esc(it.color)}">${esc(it.user.slice(0,2).toUpperCase())}</div><div class="live-body"><div class="live-text"><strong>${esc(it.user)}</strong> কিনেছেন ${esc(it.icon)} ${esc(it.product)}${it.real?' <span style="color:var(--success);font-size:10px">✓</span>':''}</div><div class="live-time">⏰ ${timeAgoShort(it.time)}</div></div></div>`).join('');
}
setInterval(()=>{ if(state.page==='home'){ const f=$('liveFeed'); if(f) f.innerHTML=renderLiveFeedItems(); } updateStatusBadge(); updateWhatsappLink(); }, 4000);

function updateStatusBadge(){
  const hr=$('headerRight'); if(!hr) return;
  const online=isStoreOnline();
  const el=hr.querySelector('.status-badge');
  if(el){ el.className='status-badge '+(online?'online':'offline'); el.innerHTML='<span class="status-dot"></span> '+(online?'Online':'Offline'); }
}

function render(){
  $('siteName').textContent = state.settings.site_name||'Panel Bajar';
  const logo=$('logoBadge');
  if(state.settings.logo_image && state.settings.logo_image.trim()) logo.innerHTML=`<img src="${esc(state.settings.logo_image)}" onerror="this.style.display='none';this.parentElement.textContent='PB'">`;
  else logo.textContent='PB';
  
  const hr=$('headerRight');
  const online=isStoreOnline();
  const statusHtml = online ? `<div class="status-badge online"><span class="status-dot"></span> Online</div>` : `<div class="status-badge offline"><span class="status-dot"></span> Offline</div>`;
  
  if(state.user){
    const fresh = state.users.find(x=>x.id===state.user.id) || state.user;
    const bal = Number(fresh.balance||0);
    hr.innerHTML = `<div class="balance-chip" onclick="nav('wallet')">💰 ${fmt(bal)}</div>${statusHtml}<button class="btn-avatar" style="background:${esc(state.user.avatarColor||'#7c3aed')}" onclick="nav('account')">${esc((state.user.username||'U').slice(0,2).toUpperCase())}</button>`;
  } else {
    hr.innerHTML = `${statusHtml}<button class="btn-login" onclick="openAuth('login')">লগইন</button>`;
  }
  
  document.querySelectorAll('.navbtn').forEach(b=>b.classList.toggle('active', b.dataset.page===state.page));
  
  const m=$('main');
  if(state.page==='home') m.innerHTML=renderHome();
  else if(state.page==='wallet') m.innerHTML=renderWallet();
  else if(state.page==='account') m.innerHTML=renderAccount();
  else if(state.page==='orders') m.innerHTML=renderOrders();
  else if(state.page==='keys') m.innerHTML=renderKeys();
  
  window.scrollTo(0,0);
  void document.body.offsetHeight;
  if(state.page==='home') startAdSlider();
  updateWhatsappLink();
}

let adInterval=null, adIdx=0, adSlides=[], adTrack=null, adDrag=null;
function adApply(anim){ if(!adTrack) return; if(anim===false) adTrack.classList.add('no-anim'); else adTrack.classList.remove('no-anim'); adTrack.style.transform='translateX(-'+(adIdx*100)+'%)'; }
function adRestart(){ if(adInterval){clearInterval(adInterval); adInterval=null;} if(adSlides.length<=1) return; const delay=Math.max(1500,Number(state.settings.ad_delay)||3000); adInterval=setInterval(()=>goToAdSlide((adIdx+1)%adSlides.length),delay); }
function startAdSlider(){
  if(adInterval){clearInterval(adInterval); adInterval=null;}
  adTrack=document.querySelector('#adSlider .ad-track');
  adSlides=document.querySelectorAll('#adSlider .ad-slide');
  if(adSlides.length===0||!adTrack) return;
  if(adIdx>=adSlides.length) adIdx=0;
  adApply(false);
  requestAnimationFrame(()=>{ adApply(true); if(adDrag) adDrag.w = document.querySelector('#adSlider')?.offsetWidth || 1; });
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
  slider.addEventListener('mousedown',down);
  if(!window.__adSwipeG){ window.__adSwipeG=true; window.addEventListener('mousemove',move); window.addEventListener('mouseup',up); window.addEventListener('resize',()=>{ const s=document.getElementById('adSlider'); if(s && adDrag) adDrag.w=s.offsetWidth||1; }); }
}

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
    adHtml=`<div class="ad-slider" id="adSlider"><div class="ad-track"><div class="ad-slide active" style="background:linear-gradient(135deg,#7c3aed 0%,#a855f7 100%)"><div style="text-align:center;padding:16px;color:#fff"><div style="font-size:48px;margin-bottom:6px">🎮</div><h1 style="font-size:22px;font-weight:900;font-family:'Orbitron',sans-serif">${esc(state.settings.site_name)}</h1><p style="font-size:13px;opacity:.9;margin-top:4px">${esc(state.settings.tagline)}</p></div></div></div></div>`;
  }
  
  const socialBar=`<div class="social-bar"><a href="${esc(state.settings.telegram)}" target="_blank" class="tg">✈️ Telegram</a><a href="${esc(state.settings.youtube)}" target="_blank" class="yt">▶️ YouTube</a></div>`;
  
  return `${offerBar}${notif}${adHtml}
    <div class="live-feed">
      <div class="live-feed-head"><span class="live-dot"></span><div class="live-feed-title">🔴 লাইভ অর্ডার</div></div>
      <div id="liveFeed">${renderLiveFeedItems()}</div>
    </div>
    <div class="tabs">${tabs}</div>
    ${prods.length===0 ? `<div class="card empty"><div class="empty-icon">🛍️</div><div style="font-weight:700;font-size:15px">কোনো প্রোডাক্ট নেই</div><div style="font-size:12px;margin-top:6px">এই ক্যাটেগরিতে এখনো প্রোডাক্ট নেই</div></div>` : `<div class="grid">${prods.map(p=>renderProductCard(p)).join('')}</div>`}
    ${socialBar}`;
}

function renderProductCard(p){
  const plans=p.plans||[];
  const validPrices=plans.filter(pl=>(pl.stock||0)>0).map(pl=>pl.price);
  const minPrice=validPrices.length?Math.min(...validPrices):(plans[0]?.price||0);
  
  return `<div class="card prod-card">
    <div class="prod-img">
      ${p.image?`<img src="${esc(p.image)}" alt="${esc(p.name)}" onerror="this.style.display='none';this.parentElement.innerHTML='<span style=\\'font-size:48px\\'>${esc(p.icon||'🎮')}</span>'">`:`<span style="font-size:48px">${esc(p.icon||'🎮')}</span>`}
      ${p.antiban?'<div class="badge-antiban">ANTI BAN</div>':''}
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
  if(p.url_setup_video) links.push({label:'🎬 PANEL SETUP VIDEO',url:p.url_setup_video,cls:'btn-danger'});
  if(p.url_download) links.push({label:'⬇️ PANEL DOWNLOAD',url:p.url_download,cls:'btn-primary'});
  if(p.url_iphone_setup) links.push({label:'📱 IPHONE SETUP',url:p.url_iphone_setup,cls:'btn-primary'});
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">📁 ${esc(p.name)}</h2>
    <p style="font-size:12px;color:var(--text-mid);text-align:center;margin-bottom:18px">নিচের বাটনে ক্লিক করুন</p>
    ${links.length===0?'<p style="text-align:center;color:var(--muted);padding:20px">এখনো কোনো লিংক নেই</p>':links.map(l=>`<a href="${esc(l.url)}" target="_blank" class="btn-full ${l.cls}" style="display:flex;align-items:center;justify-content:center;padding:14px;border-radius:11px;margin-bottom:9px;text-decoration:none;font-weight:700">${l.label}</a>`).join('')}
    <button class="btn-full btn-ghost" style="margin-top:6px" onclick="closeModal()">বন্ধ করুন</button>`);
}

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
    const planKeys = getAvailableKeys(p, pl.dur).length;
    const stockOk = pl.stock > 0 && planKeys > 0;
    return `<div class="plan ${!stockOk?'disabled':''}" onclick="${stockOk?`selectPlan(${i})`:''}">
      <div class="plan-dur">${esc(pl.dur)}</div>
      <div class="plan-price">${fmt(pl.price)}</div>
      <div class="plan-stock">${!stockOk?`<span style="color:var(--danger)">❌ স্টক শেষ</span>`:`<span style="color:var(--success)">✓ Available</span>`}</div>
    </div>`;
  }).join('');
  
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">🛒 ${esc(p.name)}</h2>
    <div style="background:rgba(16,185,129,.08);padding:11px;border-radius:11px;margin-bottom:12px;border:1px solid rgba(16,185,129,.2)">
      <div style="font-size:12px;color:var(--text-mid);font-weight:600">💰 আপনার ব্যালেন্স</div>
      <div style="font-size:19px;font-weight:900;color:var(--success);font-family:'Orbitron',sans-serif">${fmt(balance)}</div>
    </div>
    <div class="field"><label>প্ল্যান বাছুন</label></div>
    <div class="plan-grid" id="planGrid">${plansHtml}</div>
    <div class="field">
      <label>পরিমাণ (Quantity)</label>
      <div style="display:flex;align-items:center;gap:10px">
        <button class="btn-ghost" style="width:44px;height:44px;border-radius:10px;font-size:20px;font-weight:700" onclick="changeQty(-1)">−</button>
        <input id="qtyInput" value="1" readonly style="text-align:center;font-weight:900;font-size:18px;height:44px" />
        <button class="btn-ghost" style="width:44px;height:44px;border-radius:10px;font-size:20px;font-weight:700" onclick="changeQty(1)">+</button>
      </div>
    </div>
    <div style="padding:13px;background:var(--card2);border-radius:11px;margin:14px 0;display:flex;justify-content:space-between;align-items:center">
      <span style="font-size:13px;font-weight:600;color:var(--text-mid)">মোট</span>
      <span id="payTotal" style="font-size:21px;font-weight:900;color:var(--primary);font-family:'Orbitron',sans-serif">${fmt(0)}</span>
    </div>
    <button class="btn-primary btn-full" id="buyBtn" onclick="submitOrder()">✅ ব্যালেন্স দিয়ে কিনুন</button>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:10px">ব্যালেন্স কম থাকলে <a href="#" onclick="event.preventDefault();closeModal();nav('wallet')" style="color:var(--primary);font-weight:700">যোগ করুন</a></p>
  `);
}
function selectPlan(i){ selectedPlan=i; document.querySelectorAll('.plan').forEach((p,j)=>p.classList.toggle('active',j===i)); updatePayTotal(); }
function changeQty(d){ selectedQty=Math.max(1,selectedQty+d); const el=$('qtyInput'); if(el) el.value=selectedQty; updatePayTotal(); }
function updatePayTotal(){ const total=(selectedPlan!==null&&currentPlans[selectedPlan])?currentPlans[selectedPlan].price*selectedQty:0; const el=$('payTotal'); if(el) el.textContent=fmt(total); }

function submitOrder(){
  if(!isStoreOnline()){ toast('⚠️ এখন অফলাইন'); return; }
  const p = currentProduct; if(!p) return;
  if(selectedPlan === null){ toast('প্ল্যান সিলেক্ট করুন'); return; }
  
  const plan = currentPlans[selectedPlan];
  const total = plan.price * selectedQty;
  const balance = getBalance(state.user.id);
  
  if(balance < total){ toast('❌ পর্যাপ্ত ব্যালেন্স নেই'); return; }
  if(plan.stock <= 0){ toast('Stock শেষ'); return; }
  
  const realProd = state.products.find(x => x.id === p.id);
  if(!realProd){ toast('প্রোডাক্ট পাওয়া যায়নি'); return; }
  
  const autoDeliveryEnabled = state.settings.auto_delivery !== false;
  const autoApproveEnabled = state.settings.auto_approve !== false;
  
  const availableKeys = getAvailableKeys(realProd, plan.dur);
  const canAutoDeliver = autoDeliveryEnabled && availableKeys.length >= selectedQty;
  
  addBalance(state.user.id, -total, {
    type: 'debit',
    description: `অর্ডার: ${realProd.name} (${plan.dur} × ${selectedQty})`,
    refId: ''
  });
  
  const order = {
    id: uid(),
    userId: state.user.id,
    username: state.user.username,
    email: state.user.email,
    productId: realProd.id,
    productName: realProd.name,
    planDur: plan.dur,
    price: total,
    unitPrice: plan.price,
    qty: selectedQty,
    status: 'PENDING',
    txnId: 'BAL-' + Date.now(),
    codeContent: '',
    keysAssigned: [],
    autoDelivered: false,
    createdAt: new Date().toISOString(),
    completedAt: null
  };
  
  if(canAutoDeliver){
    const reservedTexts = reserveKeys(realProd, selectedQty, plan.dur);
    if(reservedTexts && reservedTexts.length === selectedQty){
      order.codeContent = reservedTexts.join('\n');
      order.keysAssigned = reservedTexts;
      order.autoDelivered = true;
      order.status = autoApproveEnabled ? 'COMPLETED' : 'PROCESSING';
      if(order.status === 'COMPLETED') order.completedAt = new Date().toISOString();
    }
  }
  
  if(realProd.plans){
    const rp = realProd.plans.find(x => x.dur === plan.dur);
    if(rp && rp.stock > 0) rp.stock = Math.max(0, rp.stock - selectedQty);
  }
  
  state.orders.push(order);
  
  if(order.status === 'COMPLETED'){
    state.transactions.push({
      id: uid(),
      userId: state.user.id,
      type: 'purchase',
      amount: -total,
      balanceAfter: getBalance(state.user.id),
      description: `✅ ${realProd.name} (${plan.dur}) — অটো ডেলিভারড`,
      refId: order.id,
      createdAt: new Date().toISOString()
    });
  }
  
  saveLocal();
  pushCol('orders');
  pushCol('products');
  pushCol('transactions');
  pushCol('users');
  
  sendTelegramNotification(order, realProd, order.codeContent);
  
  const remaining = getAvailableKeys(realProd, plan.dur).length;
  const threshold = Number(state.settings.low_stock_threshold) || 5;
  if(remaining <= threshold){
    sendLowStockAlert(realProd.name, plan.dur, remaining);
  }
  
  closeModal();
  
  if(order.status === 'COMPLETED'){
    toast('✅ অর্ডার সফল! আপনার কী রেডি');
    setTimeout(()=>showKeySuccessModal(order, realProd), 400);
  } else if(order.status === 'PROCESSING'){
    toast('⏳ কী রিজার্ভ হয়েছে — অ্যাডমিন কনফার্ম করবে');
    nav('orders');
  } else {
    toast('⏳ অর্ডার PENDING — কী স্টক শেষ');
    nav('orders');
  }
}

function showKeySuccessModal(order, product){
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div style="text-align:center;margin-bottom:18px">
      <div style="width:64px;height:64px;border-radius:50%;background:var(--gradient-success);color:#fff;display:inline-flex;align-items:center;justify-content:center;font-size:30px;box-shadow:0 8px 24px rgba(16,185,129,.4)">✅</div>
      <h2 style="font-size:19px;font-weight:900;margin-top:10px">অর্ডার সফল!</h2>
      <p style="font-size:13px;color:var(--text-mid);margin-top:3px">${esc(product.name)} — ${esc(order.planDur)}</p>
    </div>
    <div class="key-box">
      <div class="key-box-head">🎫 আপনার কী / কোড</div>
      <div class="key-content" id="successKeyBox">${esc(order.codeContent)}</div>
      <div class="key-copy-row">
        <button class="key-copy-btn" onclick="copyText(document.getElementById('successKeyBox').textContent)">📋 কপি করুন</button>
      </div>
    </div>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:12px">⚡ Telegram-এও পাঠানো হয়েছে</p>
    <button class="btn-primary btn-full" style="margin-top:12px" onclick="closeModal();nav('orders')">📦 অর্ডার দেখুন</button>
  `);
}

function renderWallet(){
  const u=state.users.find(x=>x.id===state.user.id)||state.user;
  const bal=Number(u.balance||0);
  const myDeposits=state.deposits.filter(d=>d.userId===state.user.id).slice().reverse();
  const myTx=state.transactions.filter(t=>t.userId===state.user.id).slice().reverse();
  const pendingCount=myDeposits.filter(d=>d.status==='PENDING').length;
  
  return `<h1 class="page-title">💰 আমার ওয়ালেট</h1>
    <div class="hero-card" style="margin-bottom:14px">
      <div class="hero-content">
        <div class="hero-label">বর্তমান ব্যালেন্স</div>
        <div class="hero-balance">${fmt(bal)}</div>
        <div style="font-size:12px;opacity:.85">${pendingCount>0?`⏳ ${pendingCount}টি অনুরোধ পেন্ডিং`: '✓ সব ক্লিয়ার'}</div>
        <div class="hero-actions">
          <button class="hero-btn solid" onclick="openDepositModal()">➕ টাকা যোগ করুন</button>
        </div>
      </div>
    </div>
    
    <h2 style="font-size:15px;font-weight:900;margin-bottom:10px">📋 ডিপোজিট রিকোয়েস্ট</h2>
    ${myDeposits.length===0 ? `<div class="card empty" style="padding:26px"><div class="empty-icon" style="font-size:40px">💳</div><div style="font-size:13px">কোনো ডিপোজিট রিকোয়েস্ট নেই</div></div>` :
      myDeposits.map(d=>`<div class="card list-item"><div class="list-icon">💳</div><div class="list-body"><div style="display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap"><span class="list-title">${fmt(d.amount)}</span><span class="badge ${d.status==='APPROVED'?'badge-green':d.status==='PENDING'?'badge-amber':'badge-red'}">${d.status}</span></div><div class="list-sub">🆔 ${esc(d.txnId)}<br>📅 ${tAgo(d.createdAt)}</div>${d.adminNote?`<div class="list-sub" style="margin-top:5px;color:var(--primary)">📝 ${esc(d.adminNote)}</div>`:''}</div></div>`).join('')}
    
    <h2 style="font-size:15px;font-weight:900;margin:18px 0 10px">📊 ট্রানজ্যাকশন হিস্ট্রি</h2>
    ${myTx.length===0 ? `<div class="card empty" style="padding:26px"><div class="empty-icon" style="font-size:40px">📊</div><div style="font-size:13px">কোনো ট্রানজ্যাকশন নেই</div></div>` :
      myTx.map(t=>`<div class="card list-item"><div class="list-icon" style="background:${t.amount>0?'rgba(16,185,129,.1)':'rgba(239,68,68,.1)'};color:${t.amount>0?'var(--success)':'var(--danger)'}">${t.amount>0?'➕':'➖'}</div><div class="list-body"><div style="display:flex;justify-content:space-between;gap:8px"><span class="list-title" style="font-size:12.5px">${esc(t.description||t.type)}</span><span style="font-weight:900;color:${t.amount>0?'var(--success)':'var(--danger)'}">${t.amount>0?'+':''}${fmt(t.amount)}</span></div><div class="list-sub">📅 ${tAgo(t.createdAt)} • ব্যালেন্স: ${fmt(t.balanceAfter)}</div></div></div>`).join('')}
  `;
}
function openDepositModal(){
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">💳 ব্যালেন্স যোগ করুন</h2>
    <div class="bkash-box">
      <div style="font-weight:800;color:var(--bkash);font-size:14px;display:flex;align-items:center;gap:8px">📲 bKash (Send Money)</div>
      <div class="bkash-num-row">
        <div class="bkash-num">${esc(state.settings.bkash_number||'01XXXXXXXXX')}</div>
        <button class="btn-copy" onclick="copyText('${esc(state.settings.bkash_number||'')}')">📋 কপি</button>
      </div>
      <div style="margin-top:10px;font-size:12px;color:var(--text-mid);line-height:1.6;background:var(--card2);padding:9px;border-radius:8px">⚠️ উপরে Send Money করুন, তারপর নিচে ফর্ম পূরণ করুন। অ্যাডমিন approve করলে ব্যালেন্স যোগ হবে।</div>
    </div>
    <div class="field" style="margin-top:14px"><label>পরিমাণ (৳)</label><input id="depAmount" type="number" min="10" placeholder="যেমন: 100" /></div>
    <div class="field"><label>bKash Transaction ID</label><input id="depTxn" placeholder="8N7Y6T5R4E" style="font-family:monospace;letter-spacing:1px" /></div>
    <div class="field"><label>নোট (ঐচ্ছিক)</label><input id="depNote" placeholder="কোনো মেসেজ..." /></div>
    <button class="btn-bkash btn-full" onclick="submitDeposit()">📤 রিকোয়েস্ট পাঠান</button>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:10px">⏳ Admin approve না করা পর্যন্ত PENDING থাকবে</p>
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
  state.deposits.push(dep); 
  pushCol('deposits');
  
  sendDepositTelegramNotification(dep);
  
  closeModal(); toast('✓ রিকোয়েস্ট পাঠানো হয়েছে'); render();
}

function renderAccount(){
  const u=state.users.find(x=>x.id===state.user.id)||state.user;
  const orders=state.orders.filter(o=>o.userId===u.id);
  const tx=state.transactions.filter(t=>t.userId===u.id);
  const totalSpent=tx.filter(t=>t.amount<0).reduce((s,t)=>s+Math.abs(t.amount),0);
  return `<h1 class="page-title">👤 আমার একাউন্ট</h1>
    <div class="card" style="padding:18px;margin-bottom:14px;background:linear-gradient(135deg,rgba(124,58,237,.1),rgba(225,29,72,.1));border:1px solid rgba(124,58,237,.2)">
      <div style="display:flex;align-items:center;gap:14px;flex-wrap:wrap">
        <div class="avatar-lg" style="background:${esc(u.avatarColor||'#7c3aed')};box-shadow:0 8px 20px ${esc(u.avatarColor||'#7c3aed')}40;width:60px;height:60px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:20px;font-weight:900;color:#fff;border:3px solid #fff">${esc((u.username||'U').slice(0,2).toUpperCase())}</div>
        <div style="min-width:0;flex:1">
          <div style="font-size:12px;color:var(--text-mid)">স্বাগতম,</div>
          <div style="font-size:20px;font-weight:900;letter-spacing:-.5px;word-wrap:break-word">${esc(u.username||'')} 👋</div>
          <div style="font-size:11.5px;color:var(--text-mid);word-break:break-all;margin-top:2px">${esc(u.email||'')}</div>
        </div>
      </div>
    </div>
    <div class="stat-grid">
      <div class="stat green"><div class="stat-label">ব্যালেন্স</div><div class="stat-val">${fmt(u.balance||0)}</div></div>
      <div class="stat blue"><div class="stat-label">মোট অর্ডার</div><div class="stat-val">${orders.length}</div></div>
      <div class="stat amber"><div class="stat-label">স্পেন্ট</div><div class="stat-val">${fmt(totalSpent)}</div></div>
      <div class="stat"><div class="stat-label">জয়েন</div><div class="stat-val" style="font-size:13px">${new Date(u.createdAt).toLocaleDateString('bn-BD')}</div></div>
    </div>
    <button class="btn-danger btn-full" onclick="logout()" style="margin-top:14px">🚪 লগআউট</button>`;
}

function renderOrders(){
  const orders=state.orders.filter(o=>o.userId===state.user.id).slice().reverse();
  return `<h1 class="page-title">📦 আমার অর্ডার</h1>
    ${orders.length===0 ? `<div class="card empty"><div class="empty-icon">📦</div><div style="font-weight:700;font-size:15px">কোনো অর্ডার নেই</div><div style="font-size:12px;margin-top:6px">এখনো অর্ডার দেননি</div><button class="btn-primary" style="margin-top:16px;padding:9px 22px;border-radius:11px" onclick="nav('home')">শপিং করুন</button></div>` :
      orders.map(o=>{
        const p=state.products.find(x=>x.id===o.productId);
        const statusBadge = o.status==='COMPLETED' ? 'badge-green' : o.status==='PENDING' ? 'badge-amber' : o.status==='PROCESSING' ? 'badge-amber' : 'badge-red';
        const statusText = o.status==='COMPLETED' ? '✅ সম্পন্ন' : o.status==='PENDING' ? '⏳ অপেক্ষারত' : o.status==='PROCESSING' ? '⏳ প্রসেসিং' : o.status;
        const keyHtml = o.codeContent ? `
          <div class="key-box">
            <div class="key-box-head">${o.status==='COMPLETED'?'🎫 আপনার কী / কোড':'🔒 কী রিজার্ভ হয়েছে'}</div>
            <div class="key-content" id="key_${o.id}">${esc(o.codeContent)}</div>
            <div class="key-copy-row">
              <button class="key-copy-btn" onclick="copyText(document.getElementById('key_${o.id}').textContent)">📋 কপি করুন</button>
            </div>
          </div>` : (o.status==='PENDING' ? `<div style="margin-top:9px;font-size:12px;color:var(--warning);font-weight:600;background:rgba(245,158,11,.1);padding:9px;border-radius:8px">⏳ অ্যাডমিন কী স্টক যোগ করলে স্বয়ংক্রিয়ভাবে দেওয়া হবে...</div>` : '');
        return `<div class="card list-item" style="flex-direction:column;align-items:stretch;padding:14px">
          <div style="display:flex;gap:12px;align-items:flex-start">
            <div class="list-icon">${esc(p?.icon||'📦')}</div>
            <div class="list-body">
              <div style="display:flex;justify-content:space-between;gap:8px;align-items:center;flex-wrap:wrap">
                <span class="list-title" style="font-size:14px">${esc(p?.name||o.productName||'—')}</span>
                <span style="font-weight:900;font-size:15px">${fmt(o.price)}</span>
              </div>
              <div class="list-sub" style="margin-top:5px">${o.planDur?'⏱ '+esc(o.planDur):''}${o.qty>1?' • '+o.qty+'x':''}<br>📅 ${tAgo(o.createdAt)}</div>
              <div style="margin-top:9px"><span class="badge ${statusBadge}">${statusText}</span></div>
            </div>
          </div>
          ${keyHtml}
        </div>`;
      }).join('')}`;
}

function renderKeys(){
  const orders=state.orders.filter(o=>o.userId===state.user.id && o.codeContent).slice().reverse();
  return `<h1 class="page-title">🔑 My Keys</h1>
    ${orders.length===0 ? `<div class="card empty"><div class="empty-icon">🔑</div><div style="font-weight:700;font-size:15px">কোনো কী নেই</div></div>` :
      orders.map(o=>{
        const p=state.products.find(x=>x.id===o.productId);
        return `<div class="card list-item" style="flex-direction:column;align-items:stretch;padding:14px">
          <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:9px">
            <span style="font-weight:800;font-size:13px">${esc(p?.name||o.productName||'—')} <span style="font-size:10px;color:var(--text-mid);font-weight:400">(${o.planDur})</span></span>
            <span style="font-size:11.5px;color:var(--success);font-weight:700">${fmt(o.price)}</span>
          </div>
          <div class="key-box" style="margin-top:0">
            <div class="key-content" id="key_${o.id}">${esc(o.codeContent)}</div>
            <div class="key-copy-row">
              <button class="key-copy-btn" onclick="copyText(document.getElementById('key_${o.id}').textContent)">📋 কপি করুন</button>
            </div>
          </div>
        </div>`;
      }).join('')}`;
}

function updateWhatsappLink(){ const fab=$('whatsappFab'); if(!fab) return; let num=state.settings.whatsapp_number||'8801700000000'; num=num.replace(/[^0-9]/g,''); fab.href=`https://wa.me/${num}`; }

function startFbSync(){
  if(fbSyncStarted||!fbConnected) return;
  fbSyncStarted=true;
  fbListen('products', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.products=d; localStorage.setItem('pb_products',JSON.stringify(d)); if(state.page==='home') render(); } });
  fbListen('orders', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.orders=d; localStorage.setItem('pb_orders',JSON.stringify(d)); if(['orders','account','keys'].includes(state.page)) render(); } });
  fbListen('users', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.users=d; localStorage.setItem('pb_users',JSON.stringify(d)); if(state.user){ const fresh=d.find(x=>x.id===state.user.id); if(fresh){ state.user=fresh; localStorage.setItem('pb_user',JSON.stringify(fresh)); if(fresh.banned){ toast('⚠️ অ্যাকাউন্ট ব্যান'); logout(); return; } } } render(); } });
  fbListen('deposits', d=>{ if(d&&Array.isArray(d)){ state.deposits=d; localStorage.setItem('pb_deposits',JSON.stringify(d)); if(state.page==='wallet') render(); } });
  fbListen('transactions', d=>{ if(d&&Array.isArray(d)){ state.transactions=d; localStorage.setItem('pb_transactions',JSON.stringify(d)); if(['wallet','account'].includes(state.page)) render(); } });
  fbListen('settings', d=>{ 
    if(d&&Array.isArray(d)&&d.length>0&&d[0]){ 
      state.settings={...DEFAULT_SETTINGS,...d[0]}; 
      localStorage.setItem('pb_settings',JSON.stringify(state.settings)); 
      render(); 
      if(state.settings.welcome_active && sessionStorage.getItem('pb_welcome_shown')!=='1'){
        showWelcomeIfNeeded();
      }
    } 
  });
  
  fbLoad('products', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.products=d; localStorage.setItem('pb_products',JSON.stringify(d)); if(state.page==='home') render(); } else if(state.products.length>0) fbSave('products',state.products); });
  fbLoad('orders', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.orders=d; localStorage.setItem('pb_orders',JSON.stringify(d)); } else if(state.orders.length>0) fbSave('orders',state.orders); });
  fbLoad('users', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.users=d; localStorage.setItem('pb_users',JSON.stringify(d)); } else if(state.users.length>0) fbSave('users',state.users); });
  fbLoad('deposits', d=>{ if(d&&Array.isArray(d)){ state.deposits=d; localStorage.setItem('pb_deposits',JSON.stringify(d)); } else if(state.deposits.length>0) fbSave('deposits',state.deposits); });
  fbLoad('transactions', d=>{ if(d&&Array.isArray(d)){ state.transactions=d; localStorage.setItem('pb_transactions',JSON.stringify(d)); } else if(state.transactions.length>0) fbSave('transactions',state.transactions); });
  fbLoad('settings', d=>{ if(d&&Array.isArray(d)&&d.length>0&&d[0]){ state.settings={...DEFAULT_SETTINGS,...d[0]}; localStorage.setItem('pb_settings',JSON.stringify(state.settings)); render(); } else fbSave('settings',[state.settings]); });
}

document.addEventListener('DOMContentLoaded', ()=>{
  render();
  updateWhatsappLink();
  if(initFirebase()) startFbSync();
  else console.warn('Firebase failed — localStorage mode');
  setTimeout(()=>showWelcomeIfNeeded(), 800);
});
</script>
</body>
</html>
