<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="format-detection" content="telephone=no" />
<meta name="theme-color" content="#e11d48" />
<title>Panel Bajar - User Panel</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
img,svg,video,canvas{max-width:100%;height:auto;display:block}
:root{
  --bg:#f4f6f9; --card:#ffffff; --card2:#f8fafc; --border:#e2e8f0;
  --primary:#e11d48; --primary-light:#fb7185; --accent:#7c3aed;
  --text:#0f172a; --muted:#64748b; --green:#10b981; --amber:#f59e0b;
  --red:#ef4444; --bkash:#e2136e; --blue:#3b82f6;
  --shadow-sm:0 1px 3px rgba(0,0,0,0.05), 0 1px 2px rgba(0,0,0,0.03);
  --shadow-md:0 4px 6px -1px rgba(0,0,0,0.05), 0 2px 4px -1px rgba(0,0,0,0.03);
  --shadow-lg:0 10px 15px -3px rgba(0,0,0,0.05), 0 4px 6px -2px rgba(0,0,0,0.025);
  --shadow-hover:0 12px 20px -5px rgba(225,29,72,0.15);
}
html{width:100%;max-width:100vw;overflow-x:hidden}
body{font-family:-apple-system,'Segoe UI','Hind Siliguri',system-ui,sans-serif;background:var(--bg);color:var(--text);min-height:100vh;line-height:1.5;-webkit-font-smoothing:antialiased;overflow-x:hidden;width:100%;max-width:100vw}
a{color:inherit;text-decoration:none}
button{cursor:pointer;border:none;font-family:inherit;color:inherit;background:none}
input,select,textarea{background:#fff;border:1px solid var(--border);color:var(--text);border-radius:10px;padding:12px 14px;width:100%;font-family:inherit;font-size:14px;transition:0.2s;max-width:100%}
input:focus,select:focus,textarea:focus{outline:none;border-color:var(--primary);box-shadow:0 0 0 3px rgba(225,29,72,.1)}
::-webkit-scrollbar{width:6px;height:6px}::-webkit-scrollbar-thumb{background:#cbd5e1;border-radius:3px}
.container{max-width:768px;width:100%;margin:0 auto;padding:0 14px}
header{position:sticky;top:0;z-index:40;background:rgba(255,255,255,.85);backdrop-filter:blur(12px);border-bottom:1px solid var(--border);box-shadow:0 1px 2px rgba(0,0,0,0.02)}
.header-in{max-width:768px;width:100%;margin:0 auto;padding:0 14px;height:60px;display:flex;align-items:center;justify-content:space-between;gap:8px}
.logo{display:flex;align-items:center;gap:10px;cursor:pointer;min-width:0}
.logo-badge{width:38px;height:38px;min-width:38px;min-height:38px;max-width:38px;max-height:38px;border-radius:11px;background:linear-gradient(135deg,var(--primary),var(--accent));display:flex;align-items:center;justify-content:center;font-weight:900;color:#fff;font-size:16px;box-shadow:0 4px 10px rgba(225,29,72,.3);overflow:hidden;flex-shrink:0;border:1px solid rgba(0,0,0,0.05)}
.logo-badge img{width:100%;height:100%;object-fit:cover;display:block}
.logo-name{font-weight:800;font-size:16px;color:var(--text);letter-spacing:-0.3px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.header-right{display:flex;align-items:center;gap:8px;flex-shrink:0}
.status-badge{display:flex;align-items:center;gap:5px;padding:6px 12px;border-radius:20px;font-size:11px;font-weight:700;border:1px solid transparent;transition:0.3s;white-space:nowrap}
.status-badge.online{background:rgba(16,185,129,.1);color:var(--green);border-color:rgba(16,185,129,.2)}
.status-badge.offline{background:rgba(239,68,68,.1);color:var(--red);border-color:rgba(239,68,68,.2)}
.status-dot{width:6px;height:6px;border-radius:50%}
.status-badge.online .status-dot{background:var(--green);animation:blink 1.5s infinite}
.status-badge.offline .status-dot{background:var(--red)}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.btn-login{padding:0 20px;height:36px;border-radius:20px;font-weight:700;font-size:13px;background:var(--text);color:#fff;box-shadow:0 4px 12px rgba(15,23,42,.2);transition:0.2s;white-space:nowrap}
.btn-login:hover{transform:translateY(-1px)}
.btn-avatar{width:36px;height:36px;min-width:36px;min-height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;color:#fff;font-size:13px;border:2px solid #fff;box-shadow:0 2px 8px rgba(0,0,0,.15)}
main{padding:16px 0 90px;min-height:calc(100vh - 60px);width:100%;overflow-x:hidden}
.card{background:var(--card);border:1px solid var(--border);border-radius:16px;box-shadow:var(--shadow-sm);max-width:100%}
.btn-primary{background:linear-gradient(135deg,var(--primary),#be123c);color:#fff;font-weight:700;transition:.2s;box-shadow:0 4px 12px rgba(225,29,72,.25);border-radius:10px}
.btn-primary:hover{transform:translateY(-1px);box-shadow:0 6px 16px rgba(225,29,72,.35)}
.btn-primary:disabled{opacity:.5;cursor:not-allowed;transform:none}
.btn-green{background:linear-gradient(135deg,var(--green),#059669);color:#fff;font-weight:700}
.btn-red{background:linear-gradient(135deg,var(--red),#dc2626);color:#fff;font-weight:700}
.btn-purple{background:linear-gradient(135deg,var(--accent),#6d28d9);color:#fff;font-weight:700}
.btn-blue{background:linear-gradient(135deg,var(--blue),#1d4ed8);color:#fff;font-weight:700}
.btn-bkash{background:linear-gradient(135deg,var(--bkash),#be185d);color:#fff;font-weight:700}

/* AD SLIDER */
.ad-slider{margin-bottom:16px;border-radius:16px;overflow:hidden;position:relative;background:var(--card2);box-shadow:var(--shadow-md);aspect-ratio:16/7;width:100%;max-width:100%;max-height:340px;border:1px solid var(--border);touch-action:pan-y;cursor:grab;-webkit-user-select:none;user-select:none}
.ad-slider.ad-dragging{cursor:grabbing}
.ad-track{display:flex;height:100%;will-change:transform;transition:transform .65s cubic-bezier(.45,0,.2,1)}
.ad-track.no-anim{transition:none}
.ad-slide{flex:0 0 100%;width:100%;height:100%;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center;pointer-events:none}
.ad-slide img{width:100%;height:100%;max-width:100%;max-height:100%;object-fit:cover;display:block;will-change:transform;animation:adZoom 10s ease-in-out infinite}
.ad-slide:nth-child(even) img{animation-name:adZoomAlt}
.ad-slide:not(.active) img{animation-play-state:paused}
@keyframes adZoom{0%{transform:scale(1) translate(0,0)}50%{transform:scale(1.15) translate(-2%,-1.2%)}100%{transform:scale(1) translate(0,0)}}
@keyframes adZoomAlt{0%{transform:scale(1.14) translate(1.8%,1%)}50%{transform:scale(1) translate(0,0)}100%{transform:scale(1.14) translate(1.8%,1%)}}
.ad-slide.ad-fallback-active::before{content:'🎮';position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-size:56px;background:linear-gradient(135deg,#f8fafc,#f1f5f9);z-index:1}
.ad-dots{position:absolute;bottom:10px;left:50%;transform:translateX(-50%);display:flex;gap:6px;z-index:5}
.ad-dot{width:8px;height:8px;border-radius:50%;background:rgba(255,255,255,.65);box-shadow:0 1px 3px rgba(0,0,0,.25);cursor:pointer;transition:all .3s;pointer-events:auto;position:relative;overflow:hidden}
.ad-dot.active{background:rgba(255,255,255,.45);width:22px;border-radius:4px}
.ad-dot.active::after{content:'';position:absolute;left:0;top:0;bottom:0;width:100%;border-radius:4px;background:var(--primary);transform-origin:left;animation:adDotFill var(--ad-delay,3s) linear forwards}
@keyframes adDotFill{from{transform:scaleX(0)}to{transform:scaleX(1)}}
.ad-dots.static .ad-dot.active::after{display:none}

.offer-bar{margin-bottom:14px;border-radius:12px;overflow:hidden;background:linear-gradient(90deg,#e11d48,#7c3aed,#e11d48);background-size:200% 100%;animation:offerGradient 4s linear infinite;box-shadow:0 4px 14px rgba(225,29,72,.25)}
@keyframes offerGradient{0%{background-position:0% 50%}100%{background-position:200% 50%}}
.offer-inner{display:flex;align-items:center;gap:10px;padding:10px 14px;color:#fff;font-size:13px;font-weight:600}
.offer-icon{font-size:18px;flex-shrink:0;animation:offerBounce 1s ease-in-out infinite}
@keyframes offerBounce{0%,100%{transform:translateY(0)}50%{transform:translateY(-3px)}}
.offer-marquee{overflow:hidden;flex:1;white-space:nowrap;min-width:0}
.offer-marquee span{display:inline-block;padding-left:100%;animation:offerScroll 18s linear infinite;letter-spacing:.3px}
@keyframes offerScroll{0%{transform:translateX(0)}100%{transform:translateX(-100%)}}

.notif{padding:10px 14px;font-size:12px;font-weight:500;background:linear-gradient(135deg,rgba(239,68,68,.95),rgba(220,38,38,.95));color:#fff;overflow:hidden;margin-bottom:14px;border-radius:12px;box-shadow:0 4px 12px rgba(239,68,68,.2)}
.notif-row{display:flex;align-items:center;gap:8px}.notif-text{overflow:hidden;flex:1;min-width:0}
.marquee{white-space:nowrap;animation:marquee 22s linear infinite}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}

.tabs{display:flex;gap:8px;position:sticky;top:60px;z-index:20;padding:12px 0;margin:0 -14px 16px;padding-left:14px;padding-right:14px;background:rgba(244,246,249,.95);backdrop-filter:blur(12px);overflow-x:auto;white-space:nowrap;-webkit-overflow-scrolling:touch;scrollbar-width:none}
.tabs::-webkit-scrollbar{display:none}
.tab{padding:8px 16px;border-radius:12px;font-size:13px;font-weight:700;background:#fff;border:1px solid var(--border);transition:.2s;color:var(--muted);flex-shrink:0;box-shadow:var(--shadow-sm)}
.tab.active{background:var(--text);color:#fff;box-shadow:0 4px 12px rgba(15,23,42,.2);border-color:transparent}

.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px;width:100%}
.prod-card{overflow:hidden;transition:.2s;border-radius:16px;border:1px solid var(--border);background:#fff;display:flex;flex-direction:column;min-width:0;max-width:100%}
.prod-card:hover{transform:translateY(-2px);border-color:rgba(225,29,72,.3);box-shadow:var(--shadow-hover)}
.prod-img{aspect-ratio:4/3;width:100%;max-width:100%;max-height:280px;display:flex;align-items:center;justify-content:center;font-size:48px;background:#f8fafc;position:relative;overflow:hidden;flex-shrink:0}
.prod-img img{width:100%;height:100%;max-width:100%;max-height:100%;object-fit:cover;object-position:center;display:block;will-change:transform;animation:prodZoom 8s ease-in-out infinite}
@keyframes prodZoom{0%{transform:scale(1) translate(0,0)}50%{transform:scale(1.1) translate(0,-1.5%)}100%{transform:scale(1) translate(0,0)}}
.badge-sale{position:absolute;top:10px;right:10px;font-size:10px;font-weight:800;padding:4px 10px;border-radius:999px;background:linear-gradient(135deg,var(--red),#b91c1c);color:#fff;letter-spacing:.5px;box-shadow:0 2px 6px rgba(239,68,68,.4)}
.badge-antiban{position:absolute;top:10px;left:10px;font-size:9px;font-weight:800;padding:4px 8px;border-radius:999px;background:linear-gradient(135deg,var(--green),#047857);color:#fff;box-shadow:0 2px 6px rgba(16,185,129,.4)}
.badge-maint{position:absolute;top:10px;left:10px;font-size:9px;font-weight:800;padding:4px 8px;border-radius:999px;background:linear-gradient(135deg,var(--amber),#b45309);color:#fff}
.prod-body{padding:14px;display:flex;flex-direction:column;flex:1;min-width:0;overflow:hidden}
.prod-name{font-weight:800;font-size:14px;margin-bottom:4px;letter-spacing:-0.2px;line-height:1.3;color:var(--text);display:-webkit-box;-webkit-line-clamp:1;-webkit-box-orient:vertical;overflow:hidden;word-wrap:break-word;overflow-wrap:break-word}
.prod-desc{font-size:11px;color:var(--muted);display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;min-height:32px;margin-bottom:10px;line-height:1.4;word-wrap:break-word;overflow-wrap:break-word}
.price-row{display:flex;align-items:center;gap:8px;margin-bottom:12px;flex-wrap:wrap}
.price{font-size:18px;font-weight:800;color:var(--text)}
.old-price{font-size:12px;color:var(--muted);text-decoration:line-through;font-weight:500}
.prod-btns{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:auto}
.btn-prod{padding:8px 4px;border-radius:10px;font-size:11px;font-weight:700;text-align:center;transition:0.2s;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.btn-prod:hover{transform:translateY(-1px)}

.live-feed{margin-bottom:16px;overflow:hidden}
.live-feed-head{display:flex;align-items:center;gap:8px;margin-bottom:10px;padding:0 4px}
.live-dot{width:10px;height:10px;border-radius:50%;background:var(--green);animation:blink 1.5s infinite;box-shadow:0 0 8px rgba(16,185,129,.6)}
.live-feed-title{font-size:14px;font-weight:800;color:var(--text);display:flex;align-items:center;gap:6px}
.live-list{display:flex;flex-direction:column;gap:8px}
.live-item{display:flex;align-items:center;gap:12px;padding:10px 12px;border-radius:14px;background:#fff;border:1px solid var(--border);box-shadow:var(--shadow-sm);animation:slideInRight .4s;font-size:13px;transition:0.2s;min-width:0}
.live-item:hover{border-color:rgba(225,29,72,.2);box-shadow:var(--shadow-md)}
@keyframes slideInRight{from{opacity:0;transform:translateX(20px)}to{opacity:1;transform:translateX(0)}}
.live-avatar{width:32px;height:32px;min-width:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:800;color:#fff;font-size:11px;flex-shrink:0;box-shadow:inset 0 -2px 4px rgba(0,0,0,0.1)}
.live-body{flex:1;min-width:0}
.live-text{font-size:12px;line-height:1.4;color:var(--muted);word-wrap:break-word;overflow-wrap:break-word}
.live-text strong{color:var(--text);font-weight:700}
.live-time{font-size:10px;color:#94a3b8;margin-top:2px;font-weight:500}

.social-bar{display:flex;gap:10px;margin:20px 0 10px;padding:0 2px}
.social-bar a{flex:1;padding:12px;border-radius:12px;font-size:13px;font-weight:700;color:#fff;display:flex;align-items:center;justify-content:center;gap:8px;box-shadow:var(--shadow-md);transition:.2s;min-width:0}
.social-bar a:hover{transform:translateY(-2px);box-shadow:var(--shadow-lg)}
.social-bar .tg{background:linear-gradient(135deg,#26a5e4,#1a8ec7)}
.social-bar .yt{background:linear-gradient(135deg,#ff0000,#cc0000)}

nav.botnav{position:fixed;bottom:0;left:0;right:0;z-index:30;background:rgba(255,255,255,.9);backdrop-filter:blur(16px);border-top:1px solid var(--border);box-shadow:0 -4px 12px rgba(0,0,0,0.03)}
.botnav-in{max-width:768px;width:100%;margin:0 auto;padding:0 8px;display:grid;grid-template-columns:repeat(4,1fr);height:64px}
.navbtn{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:4px;font-size:10px;color:var(--muted);transition:.2s;font-weight:600;border-radius:10px;margin:6px 0;min-width:0}
.navbtn.active{color:var(--primary)}
.navbtn.active svg{stroke:var(--primary)}
.navbtn svg{width:22px;height:22px;transition:0.2s}

.modal{position:fixed;inset:0;z-index:50;display:none;align-items:center;justify-content:center;background:rgba(15,23,42,.5);backdrop-filter:blur(4px);padding:16px}
.modal.show{display:flex;animation:fadeIn .2s}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
.modal-card{background:#fff;border:1px solid var(--border);border-radius:20px;padding:24px;width:100%;max-width:420px;max-height:90vh;overflow-y:auto;box-shadow:0 25px 50px -12px rgba(0,0,0,.25);position:relative;animation:scaleIn .2s}
@keyframes scaleIn{from{transform:scale(0.95);opacity:0}to{transform:scale(1);opacity:1}}
.modal-title{font-size:20px;font-weight:800;text-align:center;margin-bottom:20px;letter-spacing:-0.5px;color:var(--text)}
.modal-close{position:absolute;top:16px;right:16px;color:var(--muted);font-size:20px;background:var(--bg);width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;transition:0.2s}
.modal-close:hover{background:#e2e8f0;color:var(--text)}
.field{margin-bottom:16px}
.field label{font-size:12px;color:var(--muted);display:block;margin-bottom:6px;font-weight:600}
.btn-full{width:100%;padding:14px;border-radius:12px;font-weight:700;font-size:15px;transition:0.2s}
.auth-toggle{text-align:center;font-size:13px;color:var(--muted);margin-top:16px}
.auth-toggle button{color:var(--primary);font-weight:700;padding:4px}

.sidebar{position:fixed;inset:0;z-index:50;display:none}
.sidebar.show{display:block}
.sidebar-bg{position:absolute;inset:0;background:rgba(15,23,42,.5);backdrop-filter:blur(4px)}
.sidebar-panel{position:absolute;right:0;top:0;bottom:0;width:280px;max-width:85vw;overflow-y:auto;background:#fff;border-left:1px solid var(--border);box-shadow:-10px 0 30px rgba(0,0,0,.1);animation:slideLeft .3s}
@keyframes slideLeft{from{transform:translateX(100%)}to{transform:translateX(0)}}
.sidebar-head{padding:24px 20px;background:linear-gradient(135deg,rgba(225,29,72,.08),rgba(124,58,237,.08));position:relative;border-bottom:1px solid var(--border)}
.sidebar-close{position:absolute;top:16px;right:16px;color:var(--muted);font-size:20px;background:#fff;width:30px;height:30px;border-radius:50%;display:flex;align-items:center;justify-content:center;box-shadow:var(--shadow-sm)}
.avatar-lg{width:64px;height:64px;min-width:64px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:22px;font-weight:800;color:#fff;margin-bottom:12px;border:3px solid #fff;box-shadow:0 4px 10px rgba(0,0,0,.1)}
.sidebar-name{font-weight:800;font-size:18px;color:var(--text)}
.sidebar-email{font-size:13px;color:var(--muted);word-break:break-all;margin-top:2px}
.sidebar-nav{padding:12px}
.sidebar-nav button{width:100%;text-align:left;padding:12px 16px;border-radius:12px;font-size:14px;font-weight:600;display:flex;align-items:center;gap:12px;transition:.2s;color:var(--text)}
.sidebar-nav button:hover{background:var(--bg);color:var(--primary)}
.sidebar-foot{padding:16px;border-top:1px solid var(--border);background:var(--bg)}
.btn-logout{width:100%;padding:12px;border-radius:12px;font-size:14px;font-weight:700;background:#fff;color:var(--red);border:1px solid #fecaca;transition:0.2s}
.btn-logout:hover{background:#fef2f2}

.page-title{font-size:22px;font-weight:800;margin-bottom:20px;padding:0 4px;letter-spacing:-0.5px;color:var(--text)}
.empty{text-align:center;padding:50px 20px;color:var(--muted);display:flex;flex-direction:column;align-items:center;justify-content:center}
.empty-icon{font-size:56px;margin-bottom:16px;opacity:.8;filter:grayscale(1)}
.stat-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px;margin-bottom:20px}
.stat{padding:20px;border-radius:16px;background:#fff;border:1px solid var(--border);box-shadow:var(--shadow-sm);position:relative;overflow:hidden;min-width:0}
.stat::before{content:'';position:absolute;top:0;left:0;width:4px;height:100%;background:var(--primary)}
.stat-label{font-size:11px;text-transform:uppercase;color:var(--muted);font-weight:700;letter-spacing:.5px}
.stat-val{font-size:22px;font-weight:800;margin-top:6px;color:var(--text)}
.list-item{display:flex;align-items:center;gap:14px;padding:16px;margin-bottom:10px;border-radius:16px;background:#fff;border:1px solid var(--border);box-shadow:var(--shadow-sm);transition:0.2s;min-width:0;max-width:100%}
.list-item:hover{box-shadow:var(--shadow-md);border-color:rgba(225,29,72,.2)}
.list-icon{width:44px;height:44px;min-width:44px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:22px;background:var(--bg);flex-shrink:0}
.list-body{flex:1;min-width:0;overflow:hidden}
.list-title{font-weight:700;font-size:14px;color:var(--text);word-wrap:break-word;overflow-wrap:break-word}
.list-sub{font-size:11px;color:var(--muted);margin-top:4px;word-wrap:break-word;overflow-wrap:break-word}
.badge{font-size:11px;padding:3px 10px;border-radius:999px;font-weight:700}
.badge-green{background:rgba(16,185,129,.1);color:var(--green)}
.badge-amber{background:rgba(245,158,11,.1);color:var(--amber)}
.badge-red{background:rgba(239,68,68,.1);color:var(--red)}
.btn-copy{padding:8px 14px;border-radius:10px;font-size:12px;font-weight:700;background:var(--bkash);color:#fff;display:flex;align-items:center;gap:6px;box-shadow:0 4px 10px rgba(226,19,110,.2);transition:0.2s;flex-shrink:0;white-space:nowrap}
.btn-copy:hover{transform:translateY(-1px)}
.order-code-box{margin-top:10px;font-family:monospace;font-size:13px;padding:10px 14px;border-radius:10px;display:inline-block;background:rgba(16,185,129,.08);color:var(--green);border:1px solid rgba(16,185,129,.2);word-break:break-all;max-width:100%}
.bkash-box{padding:16px;border-radius:14px;font-size:13px;background:#fff;margin-top:16px;border:1.5px dashed var(--bkash);box-shadow:0 4px 12px rgba(226,19,110,.05)}
.bkash-num-row{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-top:8px;background:var(--bg);padding:8px 12px;border-radius:8px;flex-wrap:wrap}
.bkash-num{font-family:monospace;font-size:18px;font-weight:800;color:var(--bkash);letter-spacing:1px;word-break:break-all}
.toast{position:fixed;top:24px;left:50%;transform:translateX(-50%);background:var(--text);color:#fff;padding:12px 24px;border-radius:999px;z-index:100;animation:slideDown .3s;font-weight:600;font-size:13px;box-shadow:0 10px 25px rgba(0,0,0,.2);max-width:90vw;text-align:center}
@keyframes slideDown{from{opacity:0;transform:translate(-50%,-20px)}to{opacity:1;transform:translate(-50%,0)}}

.plan-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;margin:14px 0}
.plan{padding:14px;border-radius:12px;border:1.5px solid var(--border);background:#fff;cursor:pointer;transition:.2s;text-align:center;position:relative;min-width:0}
.plan:hover{border-color:var(--primary)}
.plan.active{border-color:var(--primary);background:rgba(225,29,72,.04);box-shadow:0 0 0 3px rgba(225,29,72,.1)}
.plan.disabled{opacity:.5;cursor:not-allowed;background:var(--bg)}
.plan-dur{font-size:14px;font-weight:800;color:var(--text)}
.plan-price{font-size:18px;font-weight:800;color:var(--primary);margin-top:4px}
.plan-stock{font-size:10px;color:var(--muted);margin-top:4px;font-weight:600}
.plan-stock.out{color:var(--red)}
.qty-row{display:flex;align-items:center;gap:12px;margin:14px 0}
.qty-btn{width:40px;height:40px;min-width:40px;border-radius:10px;background:var(--bg);font-size:20px;font-weight:700;display:flex;align-items:center;justify-content:center;border:1px solid var(--border);transition:0.2s}
.qty-btn:hover{background:#e2e8f0}
.qty-input{flex:1;text-align:center;font-weight:800;font-size:18px;background:var(--bg);border:1px solid var(--border);height:40px;min-width:0}
.setup-btn{padding:16px;border-radius:12px;font-weight:700;font-size:14px;margin-bottom:10px;display:flex;align-items:center;justify-content:center;gap:10px;text-align:center;box-shadow:0 4px 10px rgba(0,0,0,.1);transition:0.2s;word-break:break-word}
.setup-btn:hover{transform:translateY(-2px);box-shadow:0 6px 15px rgba(0,0,0,.15)}

.whatsapp-fab{position:fixed;width:56px;height:56px;min-width:56px;min-height:56px;max-width:56px;max-height:56px;border-radius:50%;background:linear-gradient(135deg,#25D366,#128C7E);color:#fff;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 20px rgba(37,211,102,.4);cursor:pointer;z-index:9999;touch-action:none;transition:box-shadow .1s, transform .1s;bottom:80px;right:16px;left:auto;top:auto;box-sizing:border-box;overflow:hidden;flex-shrink:0}
.whatsapp-fab:active{box-shadow:0 4px 10px rgba(37,211,102,.6);transform:scale(.95)}
.whatsapp-fab svg{width:32px;height:32px;min-width:32px;min-height:32px;max-width:32px;max-height:32px;pointer-events:none;flex-shrink:0;display:block}

@media(min-width:640px){
  .grid{grid-template-columns:repeat(3,minmax(0,1fr))}
  .plan-grid{grid-template-columns:repeat(3,minmax(0,1fr))}
  .container{padding:0 20px}
  .header-in{padding:0 20px}
  .prod-img{max-height:220px}
}
@media(max-width:360px){
  .logo-name{font-size:14px}
  .status-badge{padding:5px 8px;font-size:10px}
  .btn-login{padding:0 14px;font-size:12px}
  .prod-body{padding:10px}
  .price{font-size:16px}
  .btn-prod{font-size:10px}
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
<button class="navbtn" data-page="home" onclick="nav('home')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 12l9-9 9 9M5 10v10h14V10"/></svg>Home</button>
<button class="navbtn" data-page="orders" onclick="nav('orders')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M6 2l1 4h12l-2 8H8L6 2zM6 2H4M9 18a1 1 0 100 2 1 1 0 000-2zM17 18a1 1 0 100 2 1 1 0 000-2z"/></svg>My Order</button>
<button class="navbtn" data-page="codes" onclick="nav('codes')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 9l9-7 9 7v11a1 1 0 01-1 1h-5v-7H10v7H5a1 1 0 01-1-1V9z"/></svg>My Keys</button>
<button class="navbtn" data-page="account" onclick="nav('account')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4 4-7 8-7s8 3 8 7"/></svg>Account</button>
</div></nav>
<div class="modal" id="modal" onclick="if(event.target===this)closeModal()"><div class="modal-card" id="modalContent"></div></div>
<div class="modal" id="authModal" onclick="if(event.target===this)closeAuth()"><div class="modal-card" id="authContent" style="max-width:380px"></div></div>
<div class="sidebar" id="sidebar"><div class="sidebar-bg" onclick="closeSidebar()"></div><div class="sidebar-panel" id="sidebarPanel"></div></div>

<!-- WELCOME POPUP MODAL -->
<div class="modal" id="welcomeModal" style="z-index: 10000; background: rgba(15,23,42,.75);">
  <div class="modal-card" style="padding: 0; overflow: hidden; border-radius: 24px; max-width: 400px;">
    <div id="welcomeImageBox" style="width:100%; display:none; background:#f1f5f9;">
      <img id="welcomeImg" src="" style="width:100%; height:auto; display:block; object-fit:cover;">
    </div>
    <div style="padding: 24px 20px; text-align: center;">
      <p id="welcomeTextContent" style="font-size: 14px; font-weight: 500; color: var(--text); line-height: 1.6; margin-bottom: 20px;"></p>
      <a id="welcomeVideoBtn" href="#" target="_blank" class="btn-primary btn-full" style="display: inline-block; text-decoration: none; padding: 14px; margin-bottom: 10px;">
        ▶️ ভিডিও লিংক
      </a>
      <button onclick="closeWelcomeModal()" class="btn-full" style="background: var(--red); color: #fff; font-size: 15px; font-weight: 700; padding: 14px; box-shadow: 0 4px 12px rgba(239,68,68,.3);">
        ✕ CLOSE
      </button>
    </div>
  </div>
</div>

<a href="#" id="whatsappFab" class="whatsapp-fab" target="_blank" title="Chat on WhatsApp">
  <svg viewBox="0 0 24 24" fill="currentColor">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
  </svg>
</a>

<script>
var FIREBASE_CONFIG = {
  apiKey: "AIzaSyDt3gU-2iubzCZ94XFAGZswUnzxuDgUvFQ",
  authDomain: "free-fire-panel-611d6.firebaseapp.com",
  projectId: "free-fire-panel-611d6",
  storageBucket: "free-fire-panel-611d6.firebasestorage.app",
  messagingSenderId: "374641641780",
  appId: "1:374641641780:web:c87d374edf2371dae47d61",
  databaseURL: ""
};

// ==========================================
// 👇 এখানে আপনার টেলিগ্রাম বট টোকেন এবং চ্যাট আইডি বসান 👇
// ==========================================
var TELEGRAM_CONFIG = {
  botToken: "8886507238:AAEW429taQKomorvb1mD2PhnZD3exlOPmyc",  // উদাহরণ: "123456789:ABCdefGHIjklMNOpqrSTUvwxYZ"
  chatId: "7427334644"       // উদাহরণ: "-1001234567890" অথবা "123456789"
};
</script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>
<script>
/* ================= FIREBASE ================= */
let fbDb=null, fbConnected=false, fbSyncStarted=false;
function initFirebase(){
  try{
    if(typeof firebase==='undefined' || fbConnected) return fbConnected;
    if(!firebase.apps.length){
      firebase.initializeApp({
        apiKey:FIREBASE_CONFIG.apiKey, authDomain:FIREBASE_CONFIG.authDomain,
        projectId:FIREBASE_CONFIG.projectId, storageBucket:FIREBASE_CONFIG.storageBucket,
        messagingSenderId:FIREBASE_CONFIG.messagingSenderId, appId:FIREBASE_CONFIG.appId
      });
    }
    fbDb=firebase.firestore(); fbConnected=true; return true;
  }catch(e){ console.warn(e); return false; }
}
function fbDoc(col){ return fbDb.collection(col).doc('main'); }
function fbSave(col, arr){
  if(!fbConnected) return;
  try{ fbDoc(col).set({data:JSON.stringify(arr), updatedAt:new Date().toISOString()}).catch(e=>console.warn(e)); }catch(e){}
}
function fbLoad(col, cb){
  if(!fbConnected){ cb && cb(null); return; }
  try{
    fbDoc(col).get().then(doc=>{
      if(doc.exists){ try{ cb && cb(JSON.parse(doc.data().data||'[]')); }catch(e){ cb && cb(null); } }
      else cb && cb(null);
    }).catch(()=>cb && cb(null));
  }catch(e){ cb && cb(null); }
}
function fbListen(col, cb){
  if(!fbConnected) return;
  try{
    fbDoc(col).onSnapshot(doc=>{
      if(doc.exists){ try{ cb && cb(JSON.parse(doc.data().data||'[]')); }catch(e){} }
    });
  }catch(e){}
}

/* ================= STATE ================= */
const DEFAULT_SETTINGS = {
  site_name:'Panel Bajar', tagline:'Buy Premium Mods & Hacks',
  notification:'স্বাগতম Panel Bajar-এ!', notif_active:true,
  offer_text:'🔥 MEGA অফার! সব প্রোডাক্টে ৫০% ছাড়!', offer_active:true,
  telegram:'https://t.me/panelbajar', youtube:'https://youtube.com/@panelbajar',
  bkash_number:'01XXXXXXXXX', help_url:'https://t.me/panelbajar',
  ads:[], ad_delay:3000, is_online:true, logo_url:'#', logo_image:'',
  online_start:'00:00', online_end:'23:59', whatsapp_number:'8801700000000',
  welcome_active:false, welcome_image:'', welcome_text:'ভিডিওটি শুরু থেকে শেষ পর্যন্ত দেখুন, যাতে পেমেন্ট করতে বা প্যানেল কিনতে কোনো সমস্যা না হয়।', welcome_link:'',
  telegram_bot_token:'', telegram_chat_id:''
};

let state = {
  user: JSON.parse(localStorage.getItem('pb_user')||'null'),
  users: JSON.parse(localStorage.getItem('pb_users')||'[]'),
  products: JSON.parse(localStorage.getItem('pb_products')||'[]'),
  orders: JSON.parse(localStorage.getItem('pb_orders')||'[]'),
  settings: {...DEFAULT_SETTINGS, ...JSON.parse(localStorage.getItem('pb_settings')||'{}')},
  page:'home', productTab:'NON_ROOT', authMode:'login'
};

function saveLocal(){
  try{
    localStorage.setItem('pb_user', JSON.stringify(state.user));
    localStorage.setItem('pb_users', JSON.stringify(state.users));
    localStorage.setItem('pb_products', JSON.stringify(state.products));
    localStorage.setItem('pb_orders', JSON.stringify(state.orders));
    localStorage.setItem('pb_settings', JSON.stringify(state.settings));
  }catch(e){}
}
function pushCol(col){
  const map = {users:state.users, products:state.products, orders:state.orders, settings:[state.settings]};
  if(!map[col]) return;
  saveLocal();
  fbSave(col, map[col]);
}
function uid(){ return Date.now().toString(36)+Math.random().toString(36).slice(2,6); }
function $(id){ return document.getElementById(id); }
function esc(s){ return String(s==null?'':s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])); }
function fmt(n){ return '৳'+Number(n||0).toFixed(0); }
function tAgo(d){ try{ return new Date(d).toLocaleString('bn-BD'); }catch(e){ return ''; } }
function timeAgoShort(d){
  const diff=Date.now()-new Date(d).getTime();
  const m=Math.floor(diff/60000);
  if(m<1) return 'এইমাত্র';
  if(m<60) return m+' মিনিট আগে';
  const h=Math.floor(m/60); if(h<24) return h+' ঘন্টা আগে';
  return Math.floor(h/24)+' দিন আগে';
}
function toast(m){
  const t=document.createElement('div');
  t.className='toast'; t.textContent=m;
  document.body.appendChild(t);
  setTimeout(()=>t.remove(),3000);
}
function copyText(text){
  if(navigator.clipboard && navigator.clipboard.writeText){
    navigator.clipboard.writeText(text).then(()=>toast('কপি হয়েছে')).catch(()=>fallbackCopy(text));
  } else fallbackCopy(text);
}
function fallbackCopy(text){
  const ta=document.createElement('textarea');
  ta.value=text; ta.style.position='fixed'; ta.style.opacity='0';
  document.body.appendChild(ta); ta.select();
  try{ document.execCommand('copy'); toast('কপি হয়েছে'); }catch(e){ toast('কপি সমস্যা'); }
  document.body.removeChild(ta);
}

/* ================= TELEGRAM NOTIFICATION ================= */
function sendTelegramNotification(order, product) {
  // কোডের ভেতরের কনফিগ অথবা অ্যাডমিন প্যানেলের সেটিংস - যেটা আছে সেটা নিবে
  const token = (TELEGRAM_CONFIG.botToken && TELEGRAM_CONFIG.botToken !== 'YOUR_BOT_TOKEN_HERE') 
                ? TELEGRAM_CONFIG.botToken 
                : state.settings.telegram_bot_token;
                
  const chatId = (TELEGRAM_CONFIG.chatId && TELEGRAM_CONFIG.chatId !== 'YOUR_CHAT_ID_HERE') 
                ? TELEGRAM_CONFIG.chatId 
                : state.settings.telegram_chat_id;

  if (!token || !chatId) return;

  const msg = `
🔔 <b>New Order Received!</b>

📦 <b>Product:</b> ${product ? product.name : 'Unknown'}
⏱ <b>Plan:</b> ${order.planDur}
💰 <b>Amount:</b> ${order.price} BDT
🔢 <b>Qty:</b> ${order.qty}
🆔 <b>Txn ID:</b> <code>${order.txnId}</code>

👤 <b>User:</b> ${state.user.username}
📧 <b>Email:</b> ${state.user.email}

⏳ <i>Login to admin panel to approve.</i>
  `;

  fetch(`https://api.telegram.org/bot${token}/sendMessage`, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ chat_id: chatId, text: msg, parse_mode: 'HTML' })
  }).catch(e => console.warn('Telegram notification failed', e));
}

/* ================= ONLINE ================= */
function isStoreOnline(){
  const s=state.settings;
  if(s.is_online === false) return false;
  if(!s.online_start || !s.online_end) return true;
  const now = new Date();
  const cur = now.getHours()*60 + now.getMinutes();
  const [sh,sm] = s.online_start.split(':').map(Number);
  const [eh,em] = s.online_end.split(':').map(Number);
  const start = sh*60+sm, end = eh*60+em;
  if(start <= end) return cur >= start && cur <= end;
  return cur >= start || cur <= end;
}

/* ================= LOGO ================= */
function handleLogoClick(){
  const url = state.settings.logo_url;
  if(url && url !== '#' && url.trim() !== '') window.open(url, '_blank');
}

/* ================= AUTH ================= */
function openAuth(mode){ state.authMode=mode||'login'; renderAuth(); $('authModal').classList.add('show'); }
function closeAuth(){ $('authModal').classList.remove('show'); }
function toggleAuthMode(){ state.authMode = state.authMode==='login'?'register':'login'; renderAuth(); }
function renderAuth(){
  const isL = state.authMode==='login';
  $('authContent').innerHTML = `
    <button class="modal-close" onclick="closeAuth()">✕</button>
    <h2 class="modal-title">${isL?'লগইন করুন':'রেজিস্টার করুন'}</h2>
    <div class="field" style="display:${isL?'none':'block'}">
      <label>ইউজারনেম</label>
      <input id="authUsername" placeholder="আপনার নাম" />
    </div>
    <div class="field">
      <label>ইমেইল</label>
      <input id="authEmail" type="email" placeholder="email@example.com" />
    </div>
    <div class="field">
      <label>পাসওয়ার্ড</label>
      <input id="authPassword" type="password" placeholder="••••••••" onkeydown="if(event.key==='Enter')doAuth()" />
    </div>
    <button class="btn-primary btn-full" onclick="doAuth()">${isL?'লগইন':'রেজিস্টার'}</button>
    <p class="auth-toggle">${isL?'অ্যাকাউন্ট নেই?':'ইতিমধ্যে আছে?'}<button onclick="toggleAuthMode()">${isL?'রেজিস্টার':'লগইন'}</button></p>`;
}
function doAuth(){
  const e = ($('authEmail').value||'').trim().toLowerCase();
  const p = $('authPassword').value;
  if(!e||!p){ toast('সব ঘর পূরণ করুন'); return; }
  
  if(state.authMode==='register'){
    const u = ($('authUsername').value||'').trim();
    if(!u){ toast('ইউজারনেম দিন'); return; }
    if(state.users.find(x=>x.email===e)){ toast('এই ইমেইল ইতিমধ্যে ব্যবহৃত'); return; }
    const colors = ['#ec4899','#7c3aed','#06b6d4','#f97316','#10b981'];
    const nu = {
      id:uid(), email:e, username:u, password:p,
      role:'USER', totalOrders:0, totalSpent:0, banned:false,
      avatarColor: colors[Math.floor(Math.random()*colors.length)],
      createdAt: new Date().toISOString()
    };
    state.users.push(nu);
    state.user = nu;
    saveLocal();
    pushCol('users');
    closeAuth();
    toast('অ্যাকাউন্ট তৈরি হয়েছে!');
    render();
  } else {
    const u = state.users.find(x=>x.email===e);
    if(!u || u.password!==p){ toast('ইমেইল/পাসওয়ার্ড ভুল'); return; }
    if(u.banned){ toast('অ্যাকাউন্ট ব্যান করা'); return; }
    state.user = u;
    saveLocal();
    closeAuth();
    toast('স্বাগতম!');
    render();
  }
}
function logout(){ state.user=null; saveLocal(); toast('লগআউট হয়েছে'); nav('home'); }

/* ================= NAV ================= */
function nav(p){
  if(!state.user && ['orders','codes','account'].includes(p)){ openAuth('login'); return; }
  state.page = p; render();
}
function openSidebar(){ $('sidebar').classList.add('show'); }
function closeSidebar(){ $('sidebar').classList.remove('show'); }
function openModal(html){ $('modalContent').innerHTML=html; $('modal').classList.add('show'); }
function closeModal(){ $('modal').classList.remove('show'); }

/* ================= LIVE FEED ================= */
function generateLiveFeed(){
  const real = state.orders.slice().reverse().slice(0,6).map(o=>{
    const u = state.users.find(x=>x.id===o.userId);
    const p = state.products.find(x=>x.id===o.productId);
    return {user:u?.username||'User', color:u?.avatarColor||'#7c3aed', product:p?.name||'Product', icon:p?.icon||'🎮', time:o.createdAt, real:true};
  });
  const demoNames = [['Rahim','#ec4899'],['Karim','#7c3aed'],['Sadia','#06b6d4'],['Tanvir','#f97316'],['Nusrat','#10b981']];
  const demoProducts = state.products.filter(p=>p.status==='ACTIVE');
  if(demoProducts.length===0) return real;
  const demo = [];
  for(let i=0;i<3;i++){
    const n = demoNames[Math.floor(Math.random()*demoNames.length)];
    const p = demoProducts[Math.floor(Math.random()*demoProducts.length)];
    demo.push({user:n[0], color:n[1], product:p.name, icon:p.icon, time:new Date(Date.now()-Math.floor(Math.random()*3600000)).toISOString(), real:false});
  }
  return [...real, ...demo].sort((a,b)=>new Date(b.time)-new Date(a.time)).slice(0,6);
}
function renderLiveFeedItems(){
  const items = generateLiveFeed();
  if(items.length===0) return '<div style="text-align:center;padding:16px;color:var(--muted);font-size:12px">এখনো কোনো অর্ডার নেই</div>';
  return items.map(it=>`
    <div class="live-item">
      <div class="live-avatar" style="background:${esc(it.color)}">${esc(it.user.slice(0,2).toUpperCase())}</div>
      <div class="live-body">
        <div class="live-text"><strong>${esc(it.user)}</strong> কিনেছেন <span style="font-size:16px;margin:0 2px">${esc(it.icon)}</span> ${esc(it.product)}${it.real?' <span style="color:var(--green);font-size:10px">✓</span>':''}</div>
        <div class="live-time">⏰ ${timeAgoShort(it.time)}</div>
      </div>
    </div>`).join('');
}
setInterval(()=>{
  if(state.page==='home'){
    const f = $('liveFeed');
    if(f) f.innerHTML = renderLiveFeedItems();
  }
  updateStatusBadge();
  updateWhatsappLink();
},4000);

function updateStatusBadge(){
  const hr = $('headerRight');
  if(!hr) return;
  const online = isStoreOnline();
  const el = hr.querySelector('.status-badge');
  if(el){
    el.className = 'status-badge ' + (online?'online':'offline');
    el.innerHTML = '<span class="status-dot"></span> ' + (online?'online':'offline');
  }
}

/* ================= RENDER ================= */
function render(){
  $('siteName').textContent = state.settings.site_name || 'Panel Bajar';
  
  const logo = $('logoBadge');
  if(state.settings.logo_image && state.settings.logo_image.trim()){
    logo.innerHTML = `<img src="${esc(state.settings.logo_image)}" alt="Logo" onerror="this.style.display='none';this.parentElement.textContent='PB'">`;
  } else logo.textContent = 'PB';
  
  const hr = $('headerRight');
  const online = isStoreOnline();
  const statusHtml = online
    ? `<div class="status-badge online"><span class="status-dot"></span> online</div>`
    : `<div class="status-badge offline"><span class="status-dot"></span> offline</div>`;
  
  if(state.user){
    hr.innerHTML = `${statusHtml}<button class="btn-avatar" style="background:${esc(state.user.avatarColor||'#7c3aed')}" onclick="openSidebar()">${esc((state.user.username||'U').slice(0,2).toUpperCase())}</button>`;
  } else {
    hr.innerHTML = `${statusHtml}<button class="btn-login" onclick="openAuth('login')">লগইন</button>`;
  }
  
  if(state.user){
    $('sidebarPanel').innerHTML = `
      <div class="sidebar-head">
        <button class="sidebar-close" onclick="closeSidebar()">✕</button>
        <div class="avatar-lg" style="background:${esc(state.user.avatarColor||'#7c3aed')}">${esc((state.user.username||'U').slice(0,2).toUpperCase())}</div>
        <div class="sidebar-name">${esc(state.user.username||'')}</div>
        <div class="sidebar-email">${esc(state.user.email||'')}</div>
      </div>
      <nav class="sidebar-nav">
        <button onclick="nav('home');closeSidebar()">🏠 হোম</button>
        <button onclick="nav('account');closeSidebar()">👤 My Account</button>
        <button onclick="nav('orders');closeSidebar()">📦 My Order</button>
        <button onclick="nav('codes');closeSidebar()">🎫 My Keys</button>
      </nav>
      <div class="sidebar-foot"><button class="btn-logout" onclick="logout()">🚪 লগআউট</button></div>`;
  }
  
  document.querySelectorAll('.navbtn').forEach(b=>b.classList.toggle('active', b.dataset.page===state.page));
  
  const m = $('main');
  if(state.page==='home') m.innerHTML = renderHome();
  else if(state.page==='account') m.innerHTML = renderAccount();
  else if(state.page==='orders') m.innerHTML = renderOrders();
  else if(state.page==='codes') m.innerHTML = renderCodes();
  
  window.scrollTo(0,0);
  if(state.page==='home') startAdSlider();
  updateWhatsappLink();
}

/* ================= AD SLIDER ================= */
let adInterval=null, adIdx=0, adSlides=[], adTrack=null, adDrag=null;
function adApply(anim){
  if(!adTrack) return;
  if(anim===false) adTrack.classList.add('no-anim'); else adTrack.classList.remove('no-anim');
  adTrack.style.transform = 'translateX(-'+(adIdx*100)+'%)';
}
function adRestart(){
  if(adInterval){ clearInterval(adInterval); adInterval=null; }
  if(adSlides.length<=1) return;
  const delay = Math.max(1500, Number(state.settings.ad_delay)||3000);
  adInterval = setInterval(()=>goToAdSlide((adIdx+1)%adSlides.length), delay);
}
function startAdSlider(){
  if(adInterval){ clearInterval(adInterval); adInterval=null; }
  adTrack = document.querySelector('#adSlider .ad-track');
  adSlides = document.querySelectorAll('#adSlider .ad-slide');
  if(adSlides.length===0||!adTrack) return;
  if(adIdx>=adSlides.length) adIdx=0;
  adSlides.forEach((s,i)=>s.classList.toggle('active', i===adIdx));
  adApply(false);
  requestAnimationFrame(()=>adApply(true));
  document.querySelectorAll('.ad-dot').forEach((d,i)=>d.classList.toggle('active', i===adIdx));
  initAdSwipe();
  if(adSlides.length<=1){
    const dd = document.querySelector('#adSlider .ad-dots');
    if(dd) dd.classList.add('static');
    return;
  }
  const delay = Math.max(1500, Number(state.settings.ad_delay)||3000);
  const dotsEl = document.querySelector('#adSlider .ad-dots');
  if(dotsEl){ dotsEl.classList.remove('static'); dotsEl.style.setProperty('--ad-delay', delay+'ms'); }
  adRestart();
}
function goToAdSlide(i){
  if(!adSlides.length||!adTrack) return;
  i = ((i%adSlides.length)+adSlides.length)%adSlides.length;
  adIdx = i;
  adSlides.forEach((s,k)=>s.classList.toggle('active', k===i));
  adApply(true);
  document.querySelectorAll('.ad-dot').forEach((d,k)=>d.classList.toggle('active', k===i));
}
function initAdSwipe(){
  const slider = $('adSlider');
  if(!slider||slider.dataset.swipeBound) return;
  slider.dataset.swipeBound='1';
  const down = e=>{
    if(!adTrack) return;
    if(e.target&&e.target.closest&&e.target.closest('.ad-dot')) return;
    const p = e.touches?e.touches[0]:e;
    adDrag = {startX:p.clientX, startY:p.clientY, dx:0, axis:null, w:slider.offsetWidth||1};
    if(adSlides.length<=1) return;
    if(adInterval){ clearInterval(adInterval); adInterval=null; }
    adTrack.classList.add('no-anim');
    slider.classList.add('ad-dragging');
  };
  const move = e=>{
    if(!adDrag||adSlides.length<=1) return;
    const p = e.touches?e.touches[0]:e;
    const dx = p.clientX-adDrag.startX, dy = p.clientY-adDrag.startY;
    if(adDrag.axis===null && (Math.abs(dx)>8||Math.abs(dy)>8)) adDrag.axis = Math.abs(dx)>Math.abs(dy)?'x':'y';
    if(adDrag.axis!=='x') return;
    adDrag.dx = dx;
    if(e.cancelable) e.preventDefault();
    adTrack.style.transform = 'translateX(calc(-'+(adIdx*100)+'% + '+dx+'px))';
  };
  const up = ()=>{
    if(!adDrag) return;
    const d = adDrag; adDrag=null;
    slider.classList.remove('ad-dragging');
    adTrack.classList.remove('no-anim');
    if(d.axis===null){
      const slideEl = adSlides[adIdx];
      const link = slideEl?slideEl.getAttribute('data-link'):'';
      if(link){ try{ window.open(link,'_blank'); }catch(e){} }
    } else if(d.axis==='x' && Math.abs(d.dx)>(d.w*0.15)){
      goToAdSlide(adIdx + (d.dx<0?1:-1));
    } else adApply(true);
    adRestart();
  };
  slider.addEventListener('touchstart', down, {passive:true});
  slider.addEventListener('touchmove', move, {passive:false});
  slider.addEventListener('touchend', up);
  slider.addEventListener('touchcancel', up);
  slider.addEventListener('mousedown', down);
  if(!window.__adSwipeG){
    window.__adSwipeG = true;
    window.addEventListener('mousemove', move);
    window.addEventListener('mouseup', up);
  }
}

/* ================= HOME ================= */
function renderHome(){
  const prods = state.products.filter(p=>p.status==='ACTIVE' && p.category===state.productTab);
  
  const notif = state.settings.notif_active ? `
    <div class="notif"><div class="notif-row">
      <span>🔔</span>
      <div class="notif-text"><div class="marquee">${esc(state.settings.notification)} &nbsp;&nbsp;&nbsp; ${esc(state.settings.notification)}</div></div>
    </div></div>` : '';
  
  const offerBar = state.settings.offer_active && state.settings.offer_text ? `
    <div class="offer-bar"><div class="offer-inner">
      <span class="offer-icon">🎁</span>
      <div class="offer-marquee"><span>${esc(state.settings.offer_text)} &nbsp;&nbsp; 🎁 &nbsp;&nbsp; ${esc(state.settings.offer_text)} &nbsp;&nbsp; 🎁 &nbsp;&nbsp; </span></div>
      <span class="offer-icon">🔥</span>
    </div></div>` : '';
  
  const tabs = ['NON_ROOT','ROOT','IPHONE','PC'].map(t=>`
    <button class="tab ${state.productTab===t?'active':''}" onclick="state.productTab='${t}';render()">
      ${t==='NON_ROOT'?'🟢 NON ROOT':t==='ROOT'?'🔴 ROOT':t==='IPHONE'?'📱 IPHONE':'💻 PC'}
    </button>`).join('');
  
  let adHtml = '';
  let rawAds = state.settings.ads || [];
  if(typeof rawAds==='string'){ try{ rawAds=JSON.parse(rawAds); }catch(e){ rawAds=[]; } }
  if(!Array.isArray(rawAds)) rawAds = [];
  let ads = rawAds.map(ad=>{
    if(typeof ad==='string') return {url:ad.trim(), link:''};
    if(ad&&typeof ad==='object') return {url:(ad.url||ad.image||'').trim(), link:(ad.link||'')};
    return null;
  }).filter(ad=>ad && ad.url!=='');
  
  if(ads.length>0){
    adHtml = `<div class="ad-slider" id="adSlider"><div class="ad-track">`;
    ads.forEach((ad,i)=>{
      adHtml += `<div class="ad-slide ${i===0?'active':''}" data-index="${i}" data-link="${esc(ad.link||'')}">
        <img src="${esc(ad.url)}" alt="Ad ${i+1}" loading="${i===0?'eager':'lazy'}"
          onerror="this.onerror=null;this.style.display='none';this.parentElement.classList.add('ad-fallback-active')">
      </div>`;
    });
    adHtml += `</div><div class="ad-dots">`;
    ads.forEach((_,i)=>{ adHtml += `<div class="ad-dot ${i===0?'active':''}" data-dot="${i}" onclick="goToAdSlide(${i})"></div>`; });
    adHtml += `</div></div>`;
  } else {
    adHtml = `<div class="ad-slider" id="adSlider"><div class="ad-track">
      <div class="ad-slide active" style="background:linear-gradient(135deg,#f8fafc 0%,#f1f5f9 100%)">
        <div style="text-align:center;padding:20px">
          <div style="font-size:48px;margin-bottom:8px">🎮</div>
          <h1 style="font-size:24px;font-weight:900;color:var(--text)">${esc(state.settings.site_name)}</h1>
          <p style="font-size:13px;color:var(--muted);font-weight:500">${esc(state.settings.tagline)}</p>
        </div>
      </div>
    </div></div>`;
  }
  
  const socialBar = `<div class="social-bar">
    <a href="${esc(state.settings.telegram)}" target="_blank" class="tg">✈️ Telegram</a>
    <a href="${esc(state.settings.youtube)}" target="_blank" class="yt">▶️ YouTube</a>
  </div>`;
  
  return `${offerBar}${notif}${adHtml}
    <div class="live-feed">
      <div class="live-feed-head"><span class="live-dot"></span><div><div class="live-feed-title">🔴 LIVE Orders</div></div></div>
      <div class="live-list" id="liveFeed">${renderLiveFeedItems()}</div>
    </div>
    <div class="tabs">${tabs}</div>
    ${prods.length===0
      ? `<div class="card empty"><div class="empty-icon">🛍️</div><div style="font-weight:600">কোনো প্রোডাক্ট নেই</div><div style="font-size:13px;margin-top:4px">এই ক্যাটেগরিতে এখনো প্রোডাক্ট নেই।</div></div>`
      : `<div class="grid">${prods.map(p=>renderProductCard(p)).join('')}</div>`}
    ${socialBar}`;
}

function renderProductCard(p){
  const plans = p.plans||[];
  const validPrices = plans.filter(pl=>(pl.stock||0)>0).map(pl=>pl.price);
  const minPrice = validPrices.length ? Math.min(...validPrices) : (plans[0]?.price||0);
  return `<div class="card prod-card">
    <div class="prod-img">
      ${p.image
        ? `<img src="${esc(p.image)}" alt="${esc(p.name)}" onerror="this.style.display='none';this.parentElement.innerHTML='<span style=\\'font-size:48px\\'>${esc(p.icon||'🎮')}</span>'">`
        : `<span style="font-size:48px">${esc(p.icon||'🎮')}</span>`}
      ${p.antiban?'<div class="badge-antiban">100% ANTI BAN</div>':''}
      ${p.maintenance?'<div class="badge-maint">MAINTENANCE</div>':''}
      ${p.oldPrice?'<div class="badge-sale">🔥 SALE</div>':''}
    </div>
    <div class="prod-body">
      <div class="prod-name">${esc(p.name)}</div>
      <div class="prod-desc">${esc(p.description||'')}</div>
      <div class="price-row">
        <span class="price">${fmt(minPrice)}</span>
        ${p.oldPrice?`<span class="old-price">${fmt(p.oldPrice)}</span>`:''}
      </div>
      <div class="prod-btns">
        <button class="btn-prod btn-blue" onclick="openFileSetup('${p.id}')">📁 SETUP</button>
        <button class="btn-prod btn-primary" onclick="openBuyNow('${p.id}')" ${p.maintenance?'disabled':''}>
          ${p.maintenance?'OFF':'🛒 BUY NOW'}
        </button>
      </div>
    </div>
  </div>`;
}

function openFileSetup(pid){
  const p = state.products.find(x=>x.id===pid);
  if(!p) return;
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">📁 ${esc(p.name)}</h2>
    <p style="font-size:12px;color:var(--muted);text-align:center;margin-bottom:20px">নিচের যেকোনো বাটনে ক্লিক করুন</p>
    ${p.url_full_details?`<a href="${esc(p.url_full_details)}" target="_blank" class="setup-btn btn-green">📹 PANEL FULL DETAILS</a>`:''}
    ${p.url_setup_video?`<a href="${esc(p.url_setup_video)}" target="_blank" class="setup-btn btn-red">🎬 PANEL SETUP VIDEO</a>`:''}
    ${p.url_download?`<a href="${esc(p.url_download)}" target="_blank" class="setup-btn btn-purple">⬇️ PANEL DOWNLOAD</a>`:''}
    ${p.url_iphone_setup?`<a href="${esc(p.url_iphone_setup)}" target="_blank" class="setup-btn btn-blue">📱 IPHONE SETUP</a>`:''}
    ${!p.url_full_details && !p.url_setup_video && !p.url_download && !p.url_iphone_setup
      ? '<p style="text-align:center;color:var(--muted);font-size:13px;padding:20px">এখনো কোনো লিংক যোগ করা হয়নি</p>' : ''}
    <button class="btn-full" style="background:var(--bg);margin-top:12px;border:1px solid var(--border);color:var(--text)" onclick="closeModal()">বন্ধ করুন</button>`);
}

/* ================= BUY NOW ================= */
let selectedPlan=null, selectedQty=1, currentPlans=[];
function openBuyNow(pid){
  if(!isStoreOnline()){ toast('⚠️ এখন অফলাইন আছি, পরে চেষ্টা করুন।'); return; }
  const p = state.products.find(x=>x.id===pid);
  if(!p) return;
  if(!state.user){ openAuth('login'); return; }
  if(p.maintenance){ toast('এই প্রোডাক্ট মেইনটেন্যান্সে'); return; }
  
  selectedPlan = null; selectedQty = 1;
  currentPlans = (p.plans&&p.plans.length>0) ? p.plans : [{dur:'1 Day', price:p.price||0, stock:99}];
  
  const plansHtml = currentPlans.map((pl,i)=>`
    <div class="plan ${pl.stock===0?'disabled':''}" onclick="${pl.stock>0?`selectPlan(${i})`:''}">
      <div class="plan-dur">${esc(pl.dur)}</div>
      <div class="plan-price">${fmt(pl.price)}</div>
      <div class="plan-stock ${pl.stock===0?'out':''}">${pl.stock===0?'Out of Stock':'Stock: '+pl.stock}</div>
    </div>`).join('');
  
  openModal(`
    <button class="modal-close" onclick="closeModal()">✕</button>
    <h2 class="modal-title">🛒 ${esc(p.name)}</h2>
    <div style="background:var(--bg);padding:12px;border-radius:12px;margin-bottom:16px;font-size:13px;color:var(--muted);border:1px dashed var(--border)">
      <strong style="color:var(--text)">Select Plan:</strong> প্ল্যান বাছুন
    </div>
    <div class="plan-grid" id="planGrid">${plansHtml}</div>
    <div class="field">
      <label>Quantity</label>
      <div class="qty-row">
        <button class="qty-btn" onclick="changeQty(-1)">−</button>
        <input class="qty-input" id="qtyInput" value="1" readonly />
        <button class="qty-btn" onclick="changeQty(1)">+</button>
      </div>
    </div>
    <div class="bkash-box">
      <div style="font-weight:800;color:var(--bkash);display:flex;align-items:center;gap:8px;font-size:15px">
        <span>📲</span> bKash Payment
      </div>
      <div class="bkash-num-row">
        <div class="bkash-num" id="payBkashNum">${esc(state.settings.bkash_number||'01XXXXXXXXX')}</div>
        <button class="btn-copy" onclick="copyText('${esc(state.settings.bkash_number||'')}')">📋 কপি</button>
      </div>
      <div style="margin-top:12px;color:var(--muted);font-size:12px;line-height:1.6;background:#fff;padding:10px;border-radius:8px">
        ⚠️ উপরের নাম্বারে <strong id="payTotal" style="color:var(--bkash);font-size:15px">${fmt(0)}</strong> Send Money করুন, তারপর TxnID দিন।
      </div>
    </div>
    <div class="field" style="margin-top:16px">
      <label>bKash Transaction ID</label>
      <input id="payTxn" placeholder="8N7Y6T5R4E" style="font-family:monospace;font-size:15px;letter-spacing:1px" />
    </div>
    <button class="btn-bkash btn-full" onclick="submitOrder('${pid}')">✅ অর্ডার সাবমিট করুন</button>
    <p style="text-align:center;font-size:12px;color:var(--muted);margin-top:12px;font-weight:500">
      ⏳ অর্ডার PENDING হবে, অ্যাডমিন একসেপ্ট করলে API Key দিবে
    </p>`);
}
function selectPlan(i){
  selectedPlan = i;
  document.querySelectorAll('.plan').forEach((p,j)=>p.classList.toggle('active', j===i));
  updatePayTotal();
}
function changeQty(d){
  selectedQty = Math.max(1, selectedQty+d);
  const el = $('qtyInput'); if(el) el.value = selectedQty;
  updatePayTotal();
}
function updatePayTotal(){
  const total = (selectedPlan!==null && currentPlans[selectedPlan]) ? currentPlans[selectedPlan].price*selectedQty : 0;
  const el = $('payTotal'); if(el) el.textContent = fmt(total);
}
function submitOrder(pid){
  if(!isStoreOnline()){ toast('⚠️ এখন অফলাইন'); return; }
  const p = state.products.find(x=>x.id===pid);
  if(!p) return;
  if(selectedPlan===null){ toast('প্ল্যান সিলেক্ট করুন'); return; }
  const plan = currentPlans[selectedPlan];
  const txn = ($('payTxn').value||'').trim();
  if(!txn){ toast('Transaction ID দিন'); return; }
  if(plan.stock<=0){ toast('Stock শেষ'); return; }
  
  const order = {
    id:uid(), userId:state.user.id, productId:p.id,
    planDur:plan.dur, price:plan.price*selectedQty, qty:selectedQty,
    status:'PENDING', txnId:txn, codeContent:'',
    createdAt: new Date().toISOString()
  };
  state.orders.push(order);
  
  const realProd = state.products.find(x=>x.id===p.id);
  if(realProd && realProd.plans){
    const rp = realProd.plans.find(x=>x.dur===plan.dur);
    if(rp && rp.stock>0) rp.stock -= selectedQty;
  }
  
  saveLocal();
  pushCol('orders');
  pushCol('products');
  
  // Send Telegram Notification
  sendTelegramNotification(order, p);
  
  closeModal();
  toast('অর্ডার সফল! PENDING-এ আছে।');
  nav('orders');
}

/* ================= ACCOUNT / ORDERS / CODES ================= */
function renderAccount(){
  const u = state.user;
  if(!u) return '';
  const fresh = state.users.find(x=>x.id===u.id) || u;
  return `
    <h1 class="page-title">My Account</h1>
    <div class="card" style="margin-bottom:20px;padding:24px;background:linear-gradient(135deg,rgba(225,29,72,.05),rgba(124,58,237,.05));border:none">
      <div style="display:flex;align-items:center;gap:16px;flex-wrap:wrap">
        <div class="avatar-lg" style="background:${esc(fresh.avatarColor||'#7c3aed')};box-shadow:0 8px 20px ${esc(fresh.avatarColor||'#7c3aed')}40">${esc((fresh.username||'U').slice(0,2).toUpperCase())}</div>
        <div style="min-width:0;flex:1">
          <div style="font-size:13px;color:var(--muted);font-weight:500">স্বাগতম,</div>
          <div style="font-size:22px;font-weight:800;color:var(--text);letter-spacing:-0.5px;word-wrap:break-word">${esc(fresh.username||'')} 👋</div>
          <div style="font-size:12px;color:var(--muted);word-break:break-all;margin-top:2px">${esc(fresh.email||'')}</div>
        </div>
      </div>
    </div>
    <div class="stat-grid">
      <div class="stat" style="--primary:#3b82f6">
        <div class="stat-label">Total Orders</div>
        <div class="stat-val" style="color:#3b82f6">${fresh.totalOrders||0}</div>
      </div>
      <div class="stat" style="--primary:var(--green)">
        <div class="stat-label">Total Spent</div>
        <div class="stat-val" style="color:var(--green)">${fmt(fresh.totalSpent||0)}</div>
      </div>
    </div>`;
}

function renderOrders(){
  const orders = state.orders.filter(o=>o.userId===state.user.id).slice().reverse();
  return `<h1 class="page-title">My Order</h1>
    ${orders.length===0
      ? `<div class="card empty">
          <div class="empty-icon">📦</div>
          <div style="font-weight:700;font-size:16px;color:var(--text)">No order found!</div>
          <div style="font-size:13px;margin-top:6px">এখনো কোনো অর্ডার দেননি</div>
          <button class="btn-primary" style="margin-top:20px;padding:10px 24px;border-radius:12px" onclick="nav('home')">Order Now</button>
        </div>`
      : orders.map(o=>{
        const p = state.products.find(x=>x.id===o.productId);
        return `<div class="card list-item">
          <div class="list-icon">${esc(p?.icon||'📦')}</div>
          <div class="list-body">
            <div style="display:flex;justify-content:space-between;gap:8px;align-items:center;flex-wrap:wrap">
              <span class="list-title" style="font-size:15px">${esc(p?.name||'—')}</span>
              <span style="font-weight:800;color:var(--text);font-size:16px">${fmt(o.price)}</span>
            </div>
            <div class="list-sub" style="margin-top:6px;font-size:12px">
              <span style="background:var(--bg);padding:2px 6px;border-radius:4px">${o.planDur?'⏱ '+esc(o.planDur):''}</span>
              ${o.qty>1?' • '+o.qty+'x':''} • ${tAgo(o.createdAt)}<br>
              ${o.txnId?'🧾 Txn: '+esc(o.txnId):''}
            </div>
            <div style="margin-top:10px">
              <span class="badge ${o.status==='COMPLETED'?'badge-green':o.status==='PENDING'?'badge-amber':'badge-red'}">${esc(o.status)}</span>
            </div>
            ${o.status==='COMPLETED' && o.codeContent ? `<div class="order-code-box">🎫 API Key: ${esc(o.codeContent)}</div>` : ''}
            ${o.status==='PENDING' ? `<div style="margin-top:10px;font-size:12px;color:var(--amber);font-weight:600;background:rgba(245,158,11,.1);padding:8px;border-radius:8px;display:inline-block">⏳ অ্যাডমিনের অনুমোদনের অপেক্ষায়...</div>` : ''}
          </div>
        </div>`;
      }).join('')}`;
}

function renderCodes(){
  const orders = state.orders.filter(o=>o.userId===state.user.id && o.status==='COMPLETED' && o.codeContent);
  return `<h1 class="page-title">My API Keys</h1>
    ${orders.length===0
      ? `<div class="card empty">
          <div class="empty-icon">🎫</div>
          <div style="font-weight:700;font-size:16px;color:var(--text)">No API key found!</div>
          <div style="font-size:13px;margin-top:6px">এখনো কোনো API key পাননি</div>
          <button class="btn-primary" style="margin-top:20px;padding:10px 24px;border-radius:12px" onclick="nav('home')">Order Now</button>
        </div>`
      : orders.map(o=>{
        const p = state.products.find(x=>x.id===o.productId);
        return `<div class="card list-item">
          <div class="list-icon" style="background:rgba(16,185,129,.1);color:var(--green)">${esc(p?.icon||'🎫')}</div>
          <div class="list-body">
            <div class="list-title" style="font-size:15px">${esc(p?.name||'—')}</div>
            ${o.planDur?`<div class="list-sub" style="margin-top:4px">⏱ ${esc(o.planDur)}</div>`:''}
            <div class="order-code-box" style="margin-top:8px">🎫 ${esc(o.codeContent)}</div>
            <div class="list-sub" style="margin-top:8px;font-size:11px">${tAgo(o.createdAt)}</div>
          </div>
          <button class="btn-copy" onclick="copyText('${esc((o.codeContent||'').replace(/'/g,"\\'"))}')" style="flex-shrink:0">📋 কপি</button>
        </div>`;
      }).join('')}`;
}

/* ================= WHATSAPP ================= */
function updateWhatsappLink(){
  const fab = $('whatsappFab');
  if(!fab) return;
  let num = state.settings.whatsapp_number || '8801700000000';
  num = num.replace(/[^0-9]/g,'');
  fab.href = `https://wa.me/${num}`;
}
function initWhatsappDrag(){
  const fab = $('whatsappFab');
  if(!fab) return;
  updateWhatsappLink();
  let isDragging=false, hasDragged=false;
  let startX, startY, initialX, initialY, curX, curY;
  const saved = localStorage.getItem('wa_btn_pos');
  if(saved){ try{ const p=JSON.parse(saved); curX=p.x; curY=p.y; }catch(e){ curX=window.innerWidth-72; curY=window.innerHeight-150; } }
  else { curX=window.innerWidth-72; curY=window.innerHeight-150; }
  curX = Math.max(10, Math.min(curX, window.innerWidth-66));
  curY = Math.max(70, Math.min(curY, window.innerHeight-140));
  apply();
  function apply(){
    fab.style.bottom='auto'; fab.style.right='auto';
    fab.style.left = curX+'px'; fab.style.top = curY+'px';
  }
  window.addEventListener('resize', ()=>{
    curX = Math.max(10, Math.min(curX, window.innerWidth-66));
    curY = Math.max(70, Math.min(curY, window.innerHeight-140));
    apply();
  });
  fab.addEventListener('touchstart', start, {passive:false});
  fab.addEventListener('touchmove', move, {passive:false});
  fab.addEventListener('touchend', end);
  fab.addEventListener('mousedown', start);
  window.addEventListener('mousemove', move);
  window.addEventListener('mouseup', end);
  function start(e){
    if(e.type==='mousedown') e.preventDefault();
    isDragging=true; hasDragged=false;
    const c = e.touches?e.touches[0]:e;
    startX=c.clientX; startY=c.clientY;
    initialX=curX; initialY=curY;
    fab.style.transition='none';
  }
  function move(e){
    if(!isDragging) return;
    const c = e.touches?e.touches[0]:e;
    const dx = c.clientX-startX, dy = c.clientY-startY;
    if(Math.abs(dx)>5||Math.abs(dy)>5){ hasDragged=true; if(e.type==='touchmove') e.preventDefault(); }
    if(!hasDragged) return;
    curX = Math.max(10, Math.min(initialX+dx, window.innerWidth-66));
    curY = Math.max(70, Math.min(initialY+dy, window.innerHeight-140));
    apply();
  }
  function end(e){
    if(!isDragging) return;
    isDragging=false;
    fab.style.transition='box-shadow .1s, transform .1s';
    if(hasDragged) localStorage.setItem('wa_btn_pos', JSON.stringify({x:curX,y:curY}));
    else {
      const t = e.target.closest('a');
      if(t && t.href) window.open(t.href, '_blank');
    }
  }
  fab.addEventListener('contextmenu', e=>e.preventDefault());
}

/* ================= WELCOME POPUP ================= */
function checkWelcomePopup(){
  const hasSeen = sessionStorage.getItem('pb_welcome_seen');
  
  if(state.settings.welcome_active && !hasSeen) {
    const imgBox = $('welcomeImageBox');
    const imgTag = $('welcomeImg');
    const textEl = $('welcomeTextContent');
    const btnEl = $('welcomeVideoBtn');
    
    if(state.settings.welcome_image && state.settings.welcome_image.trim() !== ''){
      imgBox.style.display = 'block';
      imgTag.src = state.settings.welcome_image;
      imgTag.onerror = function(){ imgBox.style.display = 'none'; };
    } else {
      imgBox.style.display = 'none';
    }

    textEl.textContent = state.settings.welcome_text || '';

    if(state.settings.welcome_link && state.settings.welcome_link.trim() !== ''){
      btnEl.style.display = 'inline-block';
      btnEl.href = state.settings.welcome_link;
    } else {
      btnEl.style.display = 'none';
    }

    $('welcomeModal').classList.add('show');
  }
}
function closeWelcomeModal(){
  $('welcomeModal').classList.remove('show');
  sessionStorage.setItem('pb_welcome_seen', 'true');
}

/* ================= FIREBASE SYNC (KEY) ================= */
function startFbSync(){
  if(fbSyncStarted || !fbConnected) return;
  fbSyncStarted = true;
  
  fbListen('products', d=>{
    if(d && Array.isArray(d) && d.length>0){
      state.products = d;
      localStorage.setItem('pb_products', JSON.stringify(d));
      if(state.page==='home') render();
    }
  });
  fbListen('orders', d=>{
    if(d && Array.isArray(d) && d.length>0){
      state.orders = d;
      localStorage.setItem('pb_orders', JSON.stringify(d));
      if(['orders','codes','account'].includes(state.page)) render();
    }
  });
  fbListen('users', d=>{
    if(d && Array.isArray(d) && d.length>0){
      state.users = d;
      localStorage.setItem('pb_users', JSON.stringify(d));
      if(state.user){
        const fresh = d.find(x=>x.id===state.user.id);
        if(fresh){
          state.user = fresh;
          localStorage.setItem('pb_user', JSON.stringify(fresh));
          if(fresh.banned){ toast('⚠️ অ্যাকাউন্ট ব্যান'); logout(); return; }
        }
      }
      if(['account','orders'].includes(state.page)) render();
    }
  });
  fbListen('settings', d=>{
    if(d && Array.isArray(d) && d.length>0 && d[0]){
      state.settings = {...DEFAULT_SETTINGS, ...d[0]};
      localStorage.setItem('pb_settings', JSON.stringify(state.settings));
      render();
      updateWhatsappLink();
      checkWelcomePopup(); 
    }
  });
  
  fbLoad('products', d=>{
    if(d && Array.isArray(d) && d.length>0){
      state.products = d;
      localStorage.setItem('pb_products', JSON.stringify(d));
      if(state.page==='home') render();
    } else if(state.products.length>0){ fbSave('products', state.products); }
  });
  fbLoad('orders', d=>{
    if(d && Array.isArray(d) && d.length>0){
      state.orders = d;
      localStorage.setItem('pb_orders', JSON.stringify(d));
      if(['orders','codes','account'].includes(state.page)) render();
    } else if(state.orders.length>0){ fbSave('orders', state.orders); }
  });
  fbLoad('users', d=>{
    if(d && Array.isArray(d) && d.length>0){
      state.users = d;
      localStorage.setItem('pb_users', JSON.stringify(d));
      if(state.user){
        const fresh = d.find(x=>x.id===state.user.id);
        if(fresh){ state.user = fresh; localStorage.setItem('pb_user', JSON.stringify(fresh)); }
      }
      if(['account','orders'].includes(state.page)) render();
    } else if(state.users.length>0){ fbSave('users', state.users); }
  });
  fbLoad('settings', d=>{
    if(d && Array.isArray(d) && d.length>0 && d[0]){
      state.settings = {...DEFAULT_SETTINGS, ...d[0]};
      localStorage.setItem('pb_settings', JSON.stringify(state.settings));
      render();
      updateWhatsappLink();
      checkWelcomePopup();
    } else { fbSave('settings', [state.settings]); }
  });
}

/* ================= BOOT ================= */
document.addEventListener('DOMContentLoaded', function(){
  render();
  initWhatsappDrag();
  checkWelcomePopup();
  if(initFirebase()){
    startFbSync();
    fbListen('settings', () => {
      setTimeout(checkWelcomePopup, 500);
    });
  } else {
    console.warn('Firebase failed to init — running in localStorage mode');
  }
});
</script>
</body>
</html>
