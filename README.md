<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover" />
<meta name="theme-color" content="#7c3aed" />
<title>Panel Bajar - User Panel</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
img,svg{max-width:100%;height:auto;display:block}
:root{
  --bg:#f5f7fb; --card:#ffffff; --card2:#f8fafc; --border:#e8ecf3;
  --primary:#7c3aed; --primary-dark:#6d28d9; --primary-light:#a78bfa;
  --accent:#e11d48; --success:#10b981; --warning:#f59e0b; --danger:#ef4444;
  --info:#3b82f6; --bkash:#e2136e;
  --text:#0f172a; --text-mid:#475569; --muted:#94a3b8;
  --shadow-xs:0 1px 2px rgba(15,23,42,.04);
  --shadow-sm:0 2px 8px rgba(15,23,42,.06);
  --shadow-md:0 8px 24px rgba(15,23,42,.08);
  --shadow-lg:0 16px 48px rgba(15,23,42,.12);
  --gradient-primary:linear-gradient(135deg,#7c3aed 0%,#a855f7 100%);
  --gradient-success:linear-gradient(135deg,#10b981 0%,#059669 100%);
  --gradient-danger:linear-gradient(135deg,#ef4444 0%,#dc2626 100%);
  --gradient-bkash:linear-gradient(135deg,#e2136e 0%,#be185d 100%);
}
html,body{width:100%;max-width:100vw;overflow-x:hidden;-webkit-tap-highlight-color:transparent}
body{font-family:-apple-system,'Segoe UI','Hind Siliguri',system-ui,sans-serif;background:var(--bg);color:var(--text);min-height:100vh;line-height:1.55;-webkit-font-smoothing:antialiased}
a{color:inherit;text-decoration:none}
button{cursor:pointer;border:none;font-family:inherit;color:inherit;background:none}
input,select,textarea{background:#fff;border:1.5px solid var(--border);color:var(--text);border-radius:12px;padding:13px 16px;width:100%;font-family:inherit;font-size:14px;transition:all .2s;max-width:100%}
input:focus,select:focus,textarea:focus{outline:none;border-color:var(--primary);box-shadow:0 0 0 4px rgba(124,58,237,.1)}
::-webkit-scrollbar{width:6px;height:6px}::-webkit-scrollbar-thumb{background:#cbd5e1;border-radius:3px}

header{position:sticky;top:0;z-index:40;background:rgba(255,255,255,.92);backdrop-filter:blur(16px);border-bottom:1px solid var(--border);width:100%}
.header-in{max-width:1200px;margin:0 auto;padding:0 16px;height:64px;display:flex;align-items:center;justify-content:space-between;gap:12px}
.logo{display:flex;align-items:center;gap:10px;cursor:pointer;min-width:0}
.logo-badge{width:40px;height:40px;border-radius:12px;background:var(--gradient-primary);display:flex;align-items:center;justify-content:center;font-weight:900;color:#fff;font-size:16px;box-shadow:0 4px 12px rgba(124,58,237,.3);overflow:hidden;flex-shrink:0}
.logo-badge img{width:100%;height:100%;object-fit:cover}
.logo-name{font-weight:800;font-size:17px;letter-spacing:-.3px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.header-right{display:flex;align-items:center;gap:8px;flex-shrink:0}
.balance-chip{display:flex;align-items:center;gap:6px;padding:8px 14px;border-radius:24px;background:rgba(16,185,129,.1);color:var(--success);font-weight:800;font-size:13px;border:1px solid rgba(16,185,129,.2);white-space:nowrap;cursor:pointer}
.status-badge{display:flex;align-items:center;gap:5px;padding:6px 12px;border-radius:20px;font-size:11px;font-weight:700;border:1px solid transparent}
.status-badge.online{background:rgba(16,185,129,.1);color:var(--success);border-color:rgba(16,185,129,.2)}
.status-badge.offline{background:rgba(239,68,68,.1);color:var(--danger);border-color:rgba(239,68,68,.2)}
.status-dot{width:6px;height:6px;border-radius:50%;background:currentColor}
.status-badge.online .status-dot{animation:blink 1.5s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.btn-login{padding:0 20px;height:38px;border-radius:20px;font-weight:700;font-size:13px;background:var(--text);color:#fff;box-shadow:0 4px 12px rgba(15,23,42,.2);transition:.2s}
.btn-login:hover{transform:translateY(-1px)}
.btn-avatar{width:38px;height:38px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;color:#fff;font-size:13px;border:2px solid #fff;box-shadow:0 2px 8px rgba(0,0,0,.15)}

main{min-height:calc(100vh - 64px);padding-bottom:100px;width:100%}
.container{max-width:1200px;margin:0 auto;padding:20px 16px;width:100%}
.card{background:var(--card);border:1px solid var(--border);border-radius:18px;box-shadow:var(--shadow-sm);max-width:100%}

.btn-primary{background:var(--gradient-primary);color:#fff;font-weight:700;transition:.2s;box-shadow:0 4px 12px rgba(124,58,237,.25);border-radius:12px}
.btn-primary:hover{transform:translateY(-1px);box-shadow:0 8px 20px rgba(124,58,237,.35)}
.btn-primary:disabled{opacity:.5;cursor:not-allowed;transform:none}
.btn-success{background:var(--gradient-success);color:#fff;font-weight:700;box-shadow:0 4px 12px rgba(16,185,129,.25)}
.btn-danger{background:var(--gradient-danger);color:#fff;font-weight:700;box-shadow:0 4px 12px rgba(239,68,68,.25)}
.btn-bkash{background:var(--gradient-bkash);color:#fff;font-weight:700;box-shadow:0 4px 12px rgba(226,19,110,.25)}
.btn-ghost{background:var(--bg);color:var(--text);font-weight:700;border:1.5px solid var(--border)}
.btn-full{width:100%;padding:14px;border-radius:12px;font-weight:700;font-size:15px;transition:.2s}

.ad-slider{margin-bottom:20px;border-radius:18px;overflow:hidden;position:relative;background:var(--card2);box-shadow:var(--shadow-md);aspect-ratio:16/7;max-height:340px;border:1px solid var(--border);touch-action:pan-y;cursor:grab;user-select:none;width:100%}
.ad-slider.ad-dragging{cursor:grabbing}
.ad-track{display:flex;height:100%;transition:transform .6s cubic-bezier(.45,0,.2,1)}
.ad-track.no-anim{transition:none}
.ad-slide{flex:0 0 100%;height:100%;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center;pointer-events:none}
.ad-slide img{width:100%;height:100%;object-fit:cover}
.ad-dots{position:absolute;bottom:12px;left:50%;transform:translateX(-50%);display:flex;gap:6px;z-index:5}
.ad-dot{width:8px;height:8px;border-radius:50%;background:rgba(255,255,255,.6);cursor:pointer;transition:.3s;pointer-events:auto}
.ad-dot.active{background:#fff;width:24px;border-radius:4px}

.hero-card{margin-bottom:20px;padding:24px;border-radius:22px;background:var(--gradient-primary);color:#fff;box-shadow:0 16px 40px rgba(124,58,237,.3);position:relative;overflow:hidden}
.hero-card::before{content:'';position:absolute;top:-40%;right:-20%;width:280px;height:280px;background:rgba(255,255,255,.15);border-radius:50%}
.hero-card::after{content:'';position:absolute;bottom:-50%;left:-10%;width:220px;height:220px;background:rgba(255,255,255,.1);border-radius:50%}
.hero-content{position:relative;z-index:2}
.hero-label{font-size:13px;opacity:.85;font-weight:600;letter-spacing:.5px;text-transform:uppercase}
.hero-balance{font-size:36px;font-weight:900;margin:6px 0 4px;letter-spacing:-1px}
.hero-actions{display:flex;gap:10px;margin-top:20px;flex-wrap:wrap}
.hero-btn{padding:10px 20px;border-radius:12px;background:rgba(255,255,255,.2);color:#fff;font-weight:700;font-size:13px;backdrop-filter:blur(8px);border:1px solid rgba(255,255,255,.3);transition:.2s}
.hero-btn:hover{background:rgba(255,255,255,.3);transform:translateY(-1px)}
.hero-btn.solid{background:#fff;color:var(--primary)}

.tabs{display:flex;gap:8px;margin:20px 0 16px;overflow-x:auto;scrollbar-width:none;padding-bottom:4px;width:100%}
.tabs::-webkit-scrollbar{display:none}
.tab{padding:10px 18px;border-radius:12px;font-size:13px;font-weight:700;background:#fff;border:1.5px solid var(--border);transition:.2s;color:var(--text-mid);flex-shrink:0}
.tab.active{background:var(--text);color:#fff;border-color:transparent;box-shadow:0 4px 12px rgba(15,23,42,.15)}

/* Responsive Grid: Fixed for mobile */
.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px;width:100%;max-width:100%}
@media(min-width:640px){.grid{grid-template-columns:repeat(3,minmax(0,1fr));gap:16px}}
@media(min-width:1024px){.grid{grid-template-columns:repeat(4,minmax(0,1fr));gap:20px}}

.prod-card{overflow:hidden;transition:.25s;border-radius:18px;border:1px solid var(--border);background:#fff;display:flex;flex-direction:column;max-width:100%}
.prod-card:hover{transform:translateY(-4px);border-color:rgba(124,58,237,.3);box-shadow:0 16px 32px rgba(124,58,237,.12)}

/* Image fix: Aspect ratio & object-fit */
.prod-img{aspect-ratio:16/9;width:100%;display:flex;align-items:center;justify-content:center;font-size:48px;background:linear-gradient(135deg,#f8fafc,#f1f5f9);position:relative;overflow:hidden}
.prod-img img{width:100%;height:100%;object-fit:cover;object-position:center}
.badge-sale{position:absolute;top:10px;right:10px;font-size:10px;font-weight:800;padding:4px 10px;border-radius:999px;background:var(--gradient-danger);color:#fff}
.badge-antiban{position:absolute;top:10px;left:10px;font-size:9px;font-weight:800;padding:4px 8px;border-radius:999px;background:var(--gradient-success);color:#fff}

.prod-body{padding:12px;display:flex;flex-direction:column;flex:1;min-width:0}
.prod-name{font-weight:800;font-size:13px;margin-bottom:4px;line-height:1.3;display:-webkit-box;-webkit-line-clamp:1;-webkit-box-orient:vertical;overflow:hidden;word-break:break-word}
.prod-desc{font-size:11px;color:var(--text-mid);display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;min-height:30px;margin-bottom:8px;word-break:break-word}
.price-row{display:flex;align-items:center;gap:6px;margin-bottom:10px;flex-wrap:wrap}
.price{font-size:16px;font-weight:800}
.old-price{font-size:11px;color:var(--muted);text-decoration:line-through}

/* Button fix: Flexbox to prevent overflow */
.prod-btns{display:flex;gap:6px;margin-top:auto;width:100%}
.btn-prod{flex:1;padding:10px 4px;border-radius:10px;font-size:11px;font-weight:700;text-align:center;transition:.2s;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;display:flex;align-items:center;justify-content:center;gap:4px;min-width:0}
.btn-prod:hover{transform:translateY(-1px)}
.btn-prod svg{width:12px;height:12px;flex-shrink:0}

.list-item{display:flex;align-items:center;gap:14px;padding:16px;margin-bottom:10px;border-radius:16px;background:#fff;border:1px solid var(--border);box-shadow:var(--shadow-xs);transition:.2s}
.list-item:hover{box-shadow:var(--shadow-sm);border-color:rgba(124,58,237,.2)}
.list-icon{width:44px;height:44px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:22px;background:var(--bg);flex-shrink:0}
.list-body{flex:1;min-width:0;overflow:hidden}
.list-title{font-weight:700;font-size:14px;word-wrap:break-word}
.list-sub{font-size:11px;color:var(--text-mid);margin-top:4px;word-wrap:break-word}
.badge{font-size:11px;padding:3px 10px;border-radius:999px;font-weight:700;display:inline-block}
.badge-green{background:rgba(16,185,129,.12);color:var(--success)}
.badge-amber{background:rgba(245,158,11,.12);color:var(--warning)}
.badge-red{background:rgba(239,68,68,.12);color:var(--danger)}

.stat-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:14px;margin-bottom:20px}
@media(min-width:768px){.stat-grid{grid-template-columns:repeat(4,minmax(0,1fr))}}
.stat{padding:20px;border-radius:16px;background:#fff;border:1px solid var(--border);box-shadow:var(--shadow-xs);position:relative;overflow:hidden}
.stat::before{content:'';position:absolute;top:0;left:0;width:4px;height:100%;background:var(--primary)}
.stat.green::before{background:var(--success)}
.stat.amber::before{background:var(--warning)}
.stat.blue::before{background:var(--info)}
.stat-label{font-size:11px;text-transform:uppercase;color:var(--text-mid);font-weight:700;letter-spacing:.5px}
.stat-val{font-size:22px;font-weight:900;margin-top:6px}

.page-title{font-size:24px;font-weight:900;margin-bottom:20px;letter-spacing:-.5px}

.modal{position:fixed;inset:0;z-index:50;display:none;align-items:center;justify-content:center;background:rgba(15,23,42,.55);backdrop-filter:blur(6px);padding:16px}
.modal.show{display:flex;animation:fadeIn .2s}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
.modal-card{background:#fff;border-radius:22px;padding:24px;width:100%;max-width:440px;max-height:90vh;overflow-y:auto;box-shadow:0 25px 60px -12px rgba(0,0,0,.3);position:relative;animation:scaleIn .2s}
@keyframes scaleIn{from{transform:scale(.95);opacity:0}to{transform:scale(1);opacity:1}}
.modal-title{font-size:20px;font-weight:900;text-align:center;margin-bottom:20px;letter-spacing:-.3px}
.modal-close{position:absolute;top:16px;right:16px;color:var(--text-mid);font-size:18px;background:var(--bg);width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;transition:.2s}
.modal-close:hover{background:#e2e8f0}
.field{margin-bottom:16px}
.field label{font-size:12px;color:var(--text-mid);display:block;margin-bottom:6px;font-weight:700}
.auth-toggle{text-align:center;font-size:13px;color:var(--text-mid);margin-top:16px}
.auth-toggle button{color:var(--primary);font-weight:700;padding:4px}

.plan-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;margin:14px 0}
.plan{padding:14px;border-radius:14px;border:2px solid var(--border);background:#fff;cursor:pointer;transition:.2s;text-align:center}
.plan:hover{border-color:var(--primary-light)}
.plan.active{border-color:var(--primary);background:rgba(124,58,237,.05);box-shadow:0 0 0 4px rgba(124,58,237,.1)}
.plan.disabled{opacity:.45;cursor:not-allowed;background:var(--bg)}
.plan-dur{font-size:14px;font-weight:800}
.plan-price{font-size:18px;font-weight:900;color:var(--primary);margin-top:4px}
.plan-stock{font-size:10px;color:var(--text-mid);margin-top:4px;font-weight:600}

.bkash-box{padding:16px;border-radius:14px;background:#fff;border:2px dashed var(--bkash);margin-top:16px}
.bkash-num-row{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-top:8px;background:var(--bg);padding:10px 14px;border-radius:10px;flex-wrap:wrap}
.bkash-num{font-family:monospace;font-size:18px;font-weight:800;color:var(--bkash);letter-spacing:1px}
.btn-copy{padding:8px 14px;border-radius:10px;font-size:12px;font-weight:700;background:var(--bkash);color:#fff;box-shadow:0 4px 10px rgba(226,19,110,.25);transition:.2s;white-space:nowrap}

.toast{position:fixed;top:24px;left:50%;transform:translateX(-50%);background:var(--text);color:#fff;padding:12px 24px;border-radius:999px;z-index:100;animation:slideDown .3s;font-weight:600;font-size:13px;box-shadow:0 10px 25px rgba(0,0,0,.25);max-width:90vw;text-align:center}
@keyframes slideDown{from{opacity:0;transform:translate(-50%,-20px)}to{opacity:1;transform:translate(-50%,0)}}

.sidebar{position:fixed;inset:0;z-index:50;display:none}
.sidebar.show{display:block}
.sidebar-bg{position:absolute;inset:0;background:rgba(15,23,42,.55);backdrop-filter:blur(4px)}
.sidebar-panel{position:absolute;right:0;top:0;bottom:0;width:300px;max-width:88vw;overflow-y:auto;background:#fff;box-shadow:-10px 0 40px rgba(0,0,0,.15);animation:slideLeft .3s}
@keyframes slideLeft{from{transform:translateX(100%)}to{transform:translateX(0)}}
.sidebar-head{padding:24px 20px;background:linear-gradient(135deg,rgba(124,58,237,.08),rgba(225,29,72,.08));position:relative;border-bottom:1px solid var(--border)}
.sidebar-close{position:absolute;top:16px;right:16px;color:var(--text-mid);font-size:18px;background:#fff;width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;box-shadow:var(--shadow-sm)}
.avatar-lg{width:64px;height:64px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:22px;font-weight:900;color:#fff;margin-bottom:12px;border:3px solid #fff;box-shadow:0 4px 10px rgba(0,0,0,.1)}
.sidebar-name{font-weight:900;font-size:18px}
.sidebar-email{font-size:13px;color:var(--text-mid);word-break:break-all;margin-top:2px}
.sidebar-nav{padding:12px}
.sidebar-nav button{width:100%;text-align:left;padding:13px 16px;border-radius:12px;font-size:14px;font-weight:600;display:flex;align-items:center;gap:12px;transition:.2s;color:var(--text)}
.sidebar-nav button:hover{background:var(--bg);color:var(--primary)}
.sidebar-foot{padding:16px;border-top:1px solid var(--border);background:var(--bg)}
.btn-logout{width:100%;padding:13px;border-radius:12px;font-size:14px;font-weight:700;background:#fff;color:var(--danger);border:1px solid #fecaca;transition:.2s}
.btn-logout:hover{background:#fef2f2}

/* Bottom Nav Fix: To ensure it stays at bottom and doesn't overlap text */
nav.botnav{position:fixed;bottom:0;left:0;right:0;z-index:30;background:rgba(255,255,255,.95);backdrop-filter:blur(16px);border-top:1px solid var(--border);box-shadow:0 -4px 20px rgba(0,0,0,.05);width:100%}
.botnav-in{max-width:1200px;margin:0 auto;padding:0 8px;display:grid;grid-template-columns:repeat(4,1fr);height:66px;align-items:center}
.navbtn{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:4px;font-size:10px;color:var(--text-mid);transition:.2s;font-weight:600;border-radius:10px;margin:6px 0;height:54px;position:relative;width:100%}
.navbtn.active{color:var(--primary)}
.navbtn.active svg{stroke:var(--primary)}
.navbtn svg{width:22px;height:22px}

/* Premium Add Balance Button */
.navbtn-wallet{
  background:linear-gradient(135deg, #10b981 0%, #059669 50%, #047857 100%);
  color:#fff !important;
  box-shadow:0 6px 16px rgba(5,150,105,.4), inset 0 1px 0 rgba(255,255,255,.2);
  transform:translateY(-6px);
  border-radius:16px;
  margin:0 4px;
  height:60px;
  border:1.5px solid rgba(255,255,255,.3);
}
.navbtn-wallet.active{
  background:linear-gradient(135deg, #059669 0%, #047857 50%, #065f46 100%);
  color:#fff !important;
  box-shadow:0 8px 20px rgba(5,150,105,.6), inset 0 1px 0 rgba(255,255,255,.3);
}
.navbtn-wallet svg{stroke:#fff !important}
.navbtn-wallet::before{
  content:'';
  position:absolute;
  top:0;left:-100%;width:50%;height:100%;
  background:linear-gradient(90deg,transparent,rgba(255,255,255,.4),transparent);
  transform:skewX(-20deg);
  animation:sweep 3s infinite;
  border-radius:16px;
}
@keyframes sweep{
  0%, 40% { left: -100%; }
  60%, 100% { left: 200%; }
}

.empty{text-align:center;padding:60px 20px;color:var(--text-mid);display:flex;flex-direction:column;align-items:center}
.empty-icon{font-size:60px;margin-bottom:16px;opacity:.6}

.notif{padding:11px 16px;font-size:12px;font-weight:500;background:var(--gradient-danger);color:#fff;overflow:hidden;margin-bottom:14px;border-radius:12px;box-shadow:0 4px 12px rgba(239,68,68,.2);width:100%}
.marquee{white-space:nowrap;animation:marquee 22s linear infinite}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
.offer-bar{margin-bottom:14px;border-radius:12px;overflow:hidden;background:linear-gradient(90deg,#7c3aed,#e11d48,#7c3aed);background-size:200% 100%;animation:offerGradient 4s linear infinite;box-shadow:0 4px 14px rgba(124,58,237,.25);width:100%}
@keyframes offerGradient{0%{background-position:0% 50%}100%{background-position:200% 50%}}
.offer-inner{display:flex;align-items:center;gap:10px;padding:11px 16px;color:#fff;font-size:13px;font-weight:600}
.offer-marquee{overflow:hidden;flex:1;white-space:nowrap}
.offer-marquee span{display:inline-block;padding-left:100%;animation:offerScroll 18s linear infinite}
@keyframes offerScroll{0%{transform:translateX(0)}100%{transform:translateX(-100%)}}

.social-bar{display:flex;gap:10px;margin:24px 0 10px;width:100%}
.social-bar a{flex:1;padding:13px;border-radius:14px;font-size:13px;font-weight:700;color:#fff;display:flex;align-items:center;justify-content:center;gap:8px;box-shadow:var(--shadow-md);transition:.2s}
.social-bar a:hover{transform:translateY(-2px)}
.social-bar .tg{background:linear-gradient(135deg,#26a5e4,#1a8ec7)}
.social-bar .yt{background:linear-gradient(135deg,#ff0000,#cc0000)}

.key-box{margin-top:12px;padding:14px;border-radius:12px;background:rgba(16,185,129,.06);border:1.5px solid rgba(16,185,129,.3);width:100%}
.key-box-head{display:flex;align-items:center;gap:6px;font-size:11px;font-weight:900;color:var(--success);text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px}
.key-content{font-family:monospace;font-size:13px;white-space:pre-wrap;word-break:break-all;background:#fff;padding:12px;border-radius:10px;border:1px solid var(--border);line-height:1.7;max-height:200px;overflow-y:auto}
.key-copy-row{display:flex;gap:8px;margin-top:10px}
.key-copy-btn{flex:1;padding:10px;border-radius:10px;font-size:12px;font-weight:700;background:var(--gradient-success);color:#fff;transition:.2s}
.key-copy-btn:hover{transform:translateY(-1px)}

.welcome-modal{position:fixed;inset:0;z-index:60;display:none;align-items:center;justify-content:center;background:rgba(15,23,42,.75);backdrop-filter:blur(8px);padding:16px}
.welcome-modal.show{display:flex;animation:fadeIn .3s}
.welcome-card{background:#fff;border-radius:22px;padding:0;width:100%;max-width:440px;overflow:hidden;box-shadow:0 25px 60px -12px rgba(0,0,0,.4);position:relative;animation:scaleIn .3s}
.welcome-img{width:100%;aspect-ratio:16/9;object-fit:cover;display:block;background:var(--bg)}
.welcome-body{padding:20px}
.welcome-text{font-size:14px;color:var(--text-mid);line-height:1.6;text-align:center;margin-bottom:16px}
.welcome-btn{display:flex;align-items:center;justify-content:center;gap:8px;width:100%;padding:14px;border-radius:12px;background:var(--gradient-primary);color:#fff;font-weight:700;font-size:15px;text-decoration:none;margin-bottom:10px;box-shadow:0 4px 12px rgba(124,58,237,.3)}
.welcome-close{width:100%;padding:12px;border-radius:12px;background:var(--bg);color:var(--text-mid);font-weight:700;font-size:13px}

.whatsapp-fab{position:fixed;bottom:80px;right:16px;width:56px;height:56px;border-radius:50%;background:linear-gradient(135deg,#25D366,#128C7E);color:#fff;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 24px rgba(37,211,102,.45);z-index:9999;transition:transform .1s}
.whatsapp-fab svg{width:30px;height:30px}
.whatsapp-fab:active{transform:scale(.95)}

/* Mobile Specific Fixes */
@media(max-width:400px){
  .logo-name{font-size:14px}
  .balance-chip{padding:6px 10px;font-size:11px}
  .hero-balance{font-size:30px}
  .grid{gap:10px}
  .prod-img{aspect-ratio:4/3}
  .prod-body{padding:10px}
  .prod-name{font-size:12px}
  .prod-desc{font-size:10px;min-height:26px}
  .price{font-size:15px}
  .btn-prod{font-size:10px;padding:8px 2px}
  .btn-prod svg{width:10px;height:10px}
  .navbtn{font-size:9px}
  .navbtn-wallet{font-size:9px}
}
</style>
</head>
<body>

<header><div class="header-in">
  <div class="logo" onclick="handleLogoClick()">
    <div class="logo-badge" id="logoBadge">PB</div>
    <span class="logo-name" id="siteName">Panel Bajar</span>
  </div>
  <div class="header-right" id="headerRight"></div>
</div></header>

<main><div class="container" id="main"></div></main>

<nav class="botnav"><div class="botnav-in">
  <button class="navbtn" data-page="home" onclick="nav('home')">
    <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 12l9-9 9 9M5 10v10h14V10"/></svg>
    হোম
  </button>
  <button class="navbtn navbtn-wallet" data-page="wallet" onclick="nav('wallet')">
    <svg fill="none" stroke="currentColor" stroke-width="2.5" viewBox="0 0 24 24"><path d="M12 5v14M5 12h14"/></svg>
    এড ব্যালেন্স
  </button>
  <button class="navbtn" data-page="orders" onclick="nav('orders')">
    <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M6 2l1 4h12l-2 8H8L6 2zM6 2H4M9 18a1 1 0 100 2 1 1 0 000-2zM17 18a1 1 0 100 2 1 1 0 000-2z"/></svg>
    অর্ডার
  </button>
  <button class="navbtn" data-page="account" onclick="nav('account')">
    <svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4 4-7 8-7s8 3 8 7"/></svg>
    একাউন্ট
  </button>
</div></nav>

<div class="modal" id="modal" onclick="if(event.target===this)closeModal()"><div class="modal-card" id="modalContent"></div></div>
<div class="modal" id="authModal" onclick="if(event.target===this)closeAuth()"><div class="modal-card" id="authContent" style="max-width:400px"></div></div>
<div class="welcome-modal" id="welcomeModal" onclick="if(event.target===this)closeWelcome()"><div class="welcome-card" id="welcomeContent"></div></div>
<div class="sidebar" id="sidebar"><div class="sidebar-bg" onclick="closeSidebar()"></div><div class="sidebar-panel" id="sidebarPanel"></div></div>

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
  botToken: "8886507238:AAEW429taQKomorvb1mD2PhnZD3exlOPmyc",
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
    <button class="modal-close" style="position:absolute;top:12px;right:12px;z-index:10;background:rgba(255,255,255,.95);box-shadow:0 2px 8px rgba(0,0,0,.2);width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:16px" onclick="closeWelcome()">✕</button>
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
  if(!state.user && ['wallet','orders','account'].includes(p)){ openAuth('login'); return; }
  state.page=p; render();
}
function openSidebar(){ $('sidebar').classList.add('show'); }
function closeSidebar(){ $('sidebar').classList.remove('show'); }
function openModal(html){ $('modalContent').innerHTML=html; $('modal').classList.add('show'); }
function closeModal(){ $('modal').classList.remove('show'); }

setInterval(()=>{ updateStatusBadge(); updateWhatsappLink(); }, 4000);

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
    hr.innerHTML = `<div class="balance-chip" onclick="nav('wallet')">💰 ${fmt(bal)}</div>${statusHtml}<button class="btn-avatar" style="background:${esc(state.user.avatarColor||'#7c3aed')}" onclick="openSidebar()">${esc((state.user.username||'U').slice(0,2).toUpperCase())}</button>`;
  } else {
    hr.innerHTML = `${statusHtml}<button class="btn-login" onclick="openAuth('login')">লগইন</button>`;
  }
  
  if(state.user){
    const fresh = state.users.find(x=>x.id===state.user.id) || state.user;
    $('sidebarPanel').innerHTML = `
      <div class="sidebar-head">
        <button class="sidebar-close" onclick="closeSidebar()">✕</button>
        <div class="avatar-lg" style="background:${esc(state.user.avatarColor||'#7c3aed')}">${esc((state.user.username||'U').slice(0,2).toUpperCase())}</div>
        <div class="sidebar-name">${esc(state.user.username||'')}</div>
        <div class="sidebar-email">${esc(state.user.email||'')}</div>
        <div style="margin-top:12px;padding:10px 14px;border-radius:12px;background:#fff;font-weight:800;color:var(--success);font-size:16px">💰 ${fmt(fresh.balance||0)}</div>
      </div>
      <nav class="sidebar-nav">
        <button onclick="nav('home');closeSidebar()">🏠 হোম</button>
        <button onclick="nav('wallet');closeSidebar()">💰 ওয়ালেট</button>
        <button onclick="nav('orders');closeSidebar()">📦 My Orders</button>
        <button onclick="nav('account');closeSidebar()">👤 Account</button>
      </nav>
      <div class="sidebar-foot"><button class="btn-logout" onclick="logout()">🚪 লগআউট</button></div>`;
  }
  
  document.querySelectorAll('.navbtn').forEach(b=>b.classList.toggle('active', b.dataset.page===state.page));
  
  const m=$('main');
  if(state.page==='home') m.innerHTML=renderHome();
  else if(state.page==='wallet') m.innerHTML=renderWallet();
  else if(state.page==='account') m.innerHTML=renderAccount();
  else if(state.page==='orders') m.innerHTML=renderOrders();
  
  window.scrollTo(0,0);
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
  adApply(false); requestAnimationFrame(()=>adApply(true));
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
  if(!window.__adSwipeG){ window.__adSwipeG=true; window.addEventListener('mousemove',move); window.addEventListener('mouseup',up); }
}

function renderHome(){
  const prods=state.products.filter(p=>p.status==='ACTIVE'&&p.category===state.productTab);
  const notif = state.settings.notif_active ? `<div class="notif"><div style="display:flex;align-items:center;gap:8px"><span>🔔</span><div style="overflow:hidden;flex:1"><div class="marquee">${esc(state.settings.notification)} &nbsp;&nbsp;&nbsp; ${esc(state.settings.notification)}</div></div></div></div>` : '';
  const offerBar = state.settings.offer_active && state.settings.offer_text ? `<div class="offer-bar"><div class="offer-inner"><span style="font-size:18px">🎁</span><div class="offer-marquee"><span>${esc(state.settings.offer_text)} &nbsp;&nbsp; 🎁 &nbsp;&nbsp; ${esc(state.settings.offer_text)}</span></div><span style="font-size:18px">🔥</span></div></div>` : '';
  
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
    adHtml=`<div class="ad-slider" id="adSlider"><div class="ad-track"><div class="ad-slide active" style="background:linear-gradient(135deg,#7c3aed 0%,#a855f7 100%)"><div style="text-align:center;padding:20px;color:#fff"><div style="font-size:56px;margin-bottom:8px">🎮</div><h1 style="font-size:26px;font-weight:900">${esc(state.settings.site_name)}</h1><p style="font-size:14px;opacity:.9;margin-top:6px">${esc(state.settings.tagline)}</p></div></div></div></div>`;
  }
  
  const socialBar=`<div class="social-bar"><a href="${esc(state.settings.telegram)}" target="_blank" class="tg">✈️ Telegram</a><a href="${esc(state.settings.youtube)}" target="_blank" class="yt">▶️ YouTube</a></div>`;
  
  return `${offerBar}${notif}${adHtml}
    <div class="tabs">${tabs}</div>
    ${prods.length===0 ? `<div class="card empty"><div class="empty-icon">🛍️</div><div style="font-weight:700;font-size:16px">কোনো প্রোডাক্ট নেই</div><div style="font-size:13px;margin-top:6px">এই ক্যাটেগরিতে এখনো প্রোডাক্ট নেই</div></div>` : `<div class="grid">${prods.map(p=>renderProductCard(p)).join('')}</div>`}
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
        <button class="btn-prod btn-ghost" onclick="openFileSetup('${p.id}')">📁 SETUP</button>
        <button class="btn-prod btn-primary" onclick="openBuyNow('${p.id}')" ${p.maintenance?'disabled':''}>${p.maintenance?'OFF':'🛒 BUY'}</button>
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
    <p style="font-size:12px;color:var(--text-mid);text-align:center;margin-bottom:20px">নিচের বাটনে ক্লিক করুন</p>
    ${links.length===0?'<p style="text-align:center;color:var(--muted);padding:20px">এখনো কোনো লিংক নেই</p>':links.map(l=>`<a href="${esc(l.url)}" target="_blank" class="btn-full ${l.cls}" style="display:flex;align-items:center;justify-content:center;padding:15px;border-radius:12px;margin-bottom:10px;text-decoration:none;font-weight:700">${l.label}</a>`).join('')}
    <button class="btn-full btn-ghost" style="margin-top:8px" onclick="closeModal()">বন্ধ করুন</button>`);
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
    <div style="background:rgba(16,185,129,.08);padding:12px;border-radius:12px;margin-bottom:12px;border:1px solid rgba(16,185,129,.2)">
      <div style="font-size:12px;color:var(--text-mid);font-weight:600">💰 আপনার ব্যালেন্স</div>
      <div style="font-size:20px;font-weight:900;color:var(--success)">${fmt(balance)}</div>
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
    <div style="padding:14px;background:var(--bg);border-radius:12px;margin:16px 0;display:flex;justify-content:space-between;align-items:center">
      <span style="font-size:13px;font-weight:600;color:var(--text-mid)">মোট</span>
      <span id="payTotal" style="font-size:22px;font-weight:900;color:var(--primary)">${fmt(0)}</span>
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
    <div style="text-align:center;margin-bottom:20px">
      <div style="width:70px;height:70px;border-radius:50%;background:var(--gradient-success);color:#fff;display:inline-flex;align-items:center;justify-content:center;font-size:34px;box-shadow:0 8px 24px rgba(16,185,129,.4)">✅</div>
      <h2 style="font-size:20px;font-weight:900;margin-top:12px">অর্ডার সফল!</h2>
      <p style="font-size:13px;color:var(--text-mid);margin-top:4px">${esc(product.name)} — ${esc(order.planDur)}</p>
    </div>
    <div class="key-box">
      <div class="key-box-head">🎫 আপনার কী / কোড</div>
      <div class="key-content" id="successKeyBox">${esc(order.codeContent)}</div>
      <div class="key-copy-row">
        <button class="key-copy-btn" onclick="copyText(document.getElementById('successKeyBox').textContent)">📋 কপি করুন</button>
      </div>
    </div>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:14px">⚡ Telegram-এও পাঠানো হয়েছে</p>
    <button class="btn-primary btn-full" style="margin-top:14px" onclick="closeModal();nav('orders')">📦 অর্ডার দেখুন</button>
  `);
}

function renderWallet(){
  const u=state.users.find(x=>x.id===state.user.id)||state.user;
  const bal=Number(u.balance||0);
  const myDeposits=state.deposits.filter(d=>d.userId===state.user.id).slice().reverse();
  const myTx=state.transactions.filter(t=>t.userId===state.user.id).slice().reverse();
  const pendingCount=myDeposits.filter(d=>d.status==='PENDING').length;
  
  return `<h1 class="page-title">💰 আমার ওয়ালেট</h1>
    <div class="hero-card" style="margin-bottom:20px">
      <div class="hero-content">
        <div class="hero-label">বর্তমান ব্যালেন্স</div>
        <div class="hero-balance">${fmt(bal)}</div>
        <div style="font-size:13px;opacity:.85">${pendingCount>0?`⏳ ${pendingCount}টি অনুরোধ পেন্ডিং`: '✓ সব ক্লিয়ার'}</div>
        <div class="hero-actions">
          <button class="hero-btn solid" onclick="openDepositModal()">➕ টাকা যোগ করুন</button>
        </div>
      </div>
    </div>
    
    <h2 style="font-size:16px;font-weight:900;margin-bottom:12px">📋 ডিপোজিট রিকোয়েস্ট</h2>
    ${myDeposits.length===0 ? `<div class="card empty" style="padding:30px"><div class="empty-icon" style="font-size:44px">💳</div><div style="font-size:13px">কোনো ডিপোজিট রিকোয়েস্ট নেই</div></div>` :
      myDeposits.map(d=>`<div class="card list-item"><div class="list-icon">💳</div><div class="list-body"><div style="display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap"><span class="list-title">${fmt(d.amount)}</span><span class="badge ${d.status==='APPROVED'?'badge-green':d.status==='PENDING'?'badge-amber':'badge-red'}">${d.status}</span></div><div class="list-sub">🆔 ${esc(d.txnId)}<br>📅 ${tAgo(d.createdAt)}</div>${d.adminNote?`<div class="list-sub" style="margin-top:6px;color:var(--primary)">📝 ${esc(d.adminNote)}</div>`:''}</div></div>`).join('')}
    
    <h2 style="font-size:16px;font-weight:900;margin:24px 0 12px">📊 ট্রানজ্যাকশন হিস্ট্রি</h2>
    ${myTx.length===0 ? `<div class="card empty" style="padding:30px"><div class="empty-icon" style="font-size:44px">📊</div><div style="font-size:13px">কোনো ট্রানজ্যাকশন নেই</div></div>` :
      myTx.map(t=>`<div class="card list-item"><div class="list-icon" style="background:${t.amount>0?'rgba(16,185,129,.1)':'rgba(239,68,68,.1)'};color:${t.amount>0?'var(--success)':'var(--danger)'}">${t.amount>0?'➕':'➖'}</div><div class="list-body"><div style="display:flex;justify-content:space-between;gap:8px"><span class="list-title" style="font-size:13px">${esc(t.description||t.type)}</span><span style="font-weight:900;color:${t.amount>0?'var(--success)':'var(--danger)'}">${t.amount>0?'+':''}${fmt(t.amount)}</span></div><div class="list-sub">📅 ${tAgo(t.createdAt)} • ব্যালেন্স: ${fmt(t.balanceAfter)}</div></div></div>`).join('')}
  `;
}
function openDepositModal(){
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">💳 ব্যালেন্স যোগ করুন</h2>
    <div class="bkash-box">
      <div style="font-weight:800;color:var(--bkash);font-size:15px;display:flex;align-items:center;gap:8px">📲 bKash (Send Money)</div>
      <div class="bkash-num-row">
        <div class="bkash-num">${esc(state.settings.bkash_number||'01XXXXXXXXX')}</div>
        <button class="btn-copy" onclick="copyText('${esc(state.settings.bkash_number||'')}')">📋 কপি</button>
      </div>
      <div style="margin-top:12px;font-size:12px;color:var(--text-mid);line-height:1.6;background:#fff;padding:10px;border-radius:8px">⚠️ উপরে Send Money করুন, তারপর নিচে ফর্ম পূরণ করুন। অ্যাডমিন approve করলে ব্যালেন্স যোগ হবে।</div>
    </div>
    <div class="field" style="margin-top:16px"><label>পরিমাণ (৳)</label><input id="depAmount" type="number" min="10" placeholder="যেমন: 100" /></div>
    <div class="field"><label>bKash Transaction ID</label><input id="depTxn" placeholder="8N7Y6T5R4E" style="font-family:monospace;letter-spacing:1px" /></div>
    <div class="field"><label>নোট (ঐচ্ছিক)</label><input id="depNote" placeholder="কোনো মেসেজ..." /></div>
    <button class="btn-bkash btn-full" onclick="submitDeposit()">📤 রিকোয়েস্ট পাঠান</button>
    <p style="text-align:center;font-size:12px;color:var(--text-mid);margin-top:12px">⏳ Admin approve না করা পর্যন্ত PENDING থাকবে</p>
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
  state.deposits.push(dep); pushCol('deposits');
  closeModal(); toast('✓ রিকোয়েস্ট পাঠানো হয়েছে'); render();
}

function renderAccount(){
  const u=state.users.find(x=>x.id===state.user.id)||state.user;
  const orders=state.orders.filter(o=>o.userId===u.id);
  const tx=state.transactions.filter(t=>t.userId===u.id);
  const totalSpent=tx.filter(t=>t.amount<0).reduce((s,t)=>s+Math.abs(t.amount),0);
  return `<h1 class="page-title">👤 আমার একাউন্ট</h1>
    <div class="card" style="padding:24px;margin-bottom:20px;background:linear-gradient(135deg,rgba(124,58,237,.06),rgba(225,29,72,.06))">
      <div style="display:flex;align-items:center;gap:16px;flex-wrap:wrap">
        <div class="avatar-lg" style="background:${esc(u.avatarColor||'#7c3aed')};box-shadow:0 8px 20px ${esc(u.avatarColor||'#7c3aed')}40">${esc((u.username||'U').slice(0,2).toUpperCase())}</div>
        <div style="min-width:0;flex:1">
          <div style="font-size:13px;color:var(--text-mid)">স্বাগতম,</div>
          <div style="font-size:22px;font-weight:900;letter-spacing:-.5px;word-wrap:break-word">${esc(u.username||'')} 👋</div>
          <div style="font-size:12px;color:var(--text-mid);word-break:break-all;margin-top:2px">${esc(u.email||'')}</div>
        </div>
      </div>
    </div>
    <div class="stat-grid">
      <div class="stat green"><div class="stat-label">ব্যালেন্স</div><div class="stat-val">${fmt(u.balance||0)}</div></div>
      <div class="stat blue"><div class="stat-label">মোট অর্ডার</div><div class="stat-val">${orders.length}</div></div>
      <div class="stat amber"><div class="stat-label">স্পেন্ট</div><div class="stat-val">${fmt(totalSpent)}</div></div>
      <div class="stat"><div class="stat-label">জয়েন</div><div class="stat-val" style="font-size:14px">${new Date(u.createdAt).toLocaleDateString('bn-BD')}</div></div>
    </div>
    <button class="btn-danger btn-full" onclick="logout()" style="margin-top:20px">🚪 লগআউট</button>`;
}

function renderOrders(){
  const orders=state.orders.filter(o=>o.userId===state.user.id).slice().reverse();
  return `<h1 class="page-title">📦 আমার অর্ডার</h1>
    ${orders.length===0 ? `<div class="card empty"><div class="empty-icon">📦</div><div style="font-weight:700;font-size:16px">কোনো অর্ডার নেই</div><div style="font-size:13px;margin-top:6px">এখনো অর্ডার দেননি</div><button class="btn-primary" style="margin-top:20px;padding:10px 24px;border-radius:12px" onclick="nav('home')">শপিং করুন</button></div>` :
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
          </div>` : (o.status==='PENDING' ? `<div style="margin-top:10px;font-size:12px;color:var(--warning);font-weight:600;background:rgba(245,158,11,.1);padding:10px;border-radius:8px">⏳ অ্যাডমিন কী স্টক যোগ করলে স্বয়ংক্রিয়ভাবে দেওয়া হবে...</div>` : '');
        return `<div class="card list-item" style="flex-direction:column;align-items:stretch;padding:16px">
          <div style="display:flex;gap:14px;align-items:flex-start">
            <div class="list-icon">${esc(p?.icon||'📦')}</div>
            <div class="list-body">
              <div style="display:flex;justify-content:space-between;gap:8px;align-items:center;flex-wrap:wrap">
                <span class="list-title" style="font-size:15px">${esc(p?.name||o.productName||'—')}</span>
                <span style="font-weight:900;font-size:16px">${fmt(o.price)}</span>
              </div>
              <div class="list-sub" style="margin-top:6px">${o.planDur?'⏱ '+esc(o.planDur):''}${o.qty>1?' • '+o.qty+'x':''}<br>📅 ${tAgo(o.createdAt)}</div>
              <div style="margin-top:10px"><span class="badge ${statusBadge}">${statusText}</span></div>
            </div>
          </div>
          ${keyHtml}
        </div>`;
      }).join('')}`;
}

function updateWhatsappLink(){ const fab=$('whatsappFab'); if(!fab) return; let num=state.settings.whatsapp_number||'8801700000000'; num=num.replace(/[^0-9]/g,''); fab.href=`https://wa.me/${num}`; }

function startFbSync(){
  if(fbSyncStarted||!fbConnected) return;
  fbSyncStarted=true;
  fbListen('products', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.products=d; localStorage.setItem('pb_products',JSON.stringify(d)); if(state.page==='home') render(); } });
  fbListen('orders', d=>{ if(d&&Array.isArray(d)&&d.length>0){ state.orders=d; localStorage.setItem('pb_orders',JSON.stringify(d)); if(['orders','account'].includes(state.page)) render(); } });
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
