
<html lang="bn">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0" />
<title>Panel Bajar - User Panel</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{--bg:#0a0614;--card:#14102a;--card2:#1e1740;--border:#2d2150;--primary:#ec4899;--accent:#7c3aed;--text:#f5f3ff;--muted:#a89cc9;--green:#10b981;--amber:#f59e0b;--red:#ef4444;--bkash:#e2136e;--blue:#3b82f6}
body{font-family:-apple-system,'Segoe UI','Hind Siliguri',system-ui,sans-serif;background:var(--bg);color:var(--text);min-height:100vh;line-height:1.5}
a{color:inherit;text-decoration:none}
button{cursor:pointer;border:none;font-family:inherit;color:inherit;background:none}
input,select,textarea{background:#0f0a1a;border:1px solid var(--border);color:var(--text);border-radius:10px;padding:11px 14px;width:100%;font-family:inherit;font-size:14px}
input:focus,select:focus,textarea:focus{outline:none;border-color:var(--primary)}
::-webkit-scrollbar{width:6px;height:6px}::-webkit-scrollbar-thumb{background:#3d2d6b;border-radius:3px}
.container{max-width:768px;margin:0 auto;padding:0 12px}
header{position:sticky;top:0;z-index:40;background:rgba(10,6,20,.92);backdrop-filter:blur(16px);border-bottom:1px solid rgba(45,33,80,.5)}
.header-in{max-width:768px;margin:0 auto;padding:0 12px;height:58px;display:flex;align-items:center;justify-content:space-between;gap:8px}
.logo{display:flex;align-items:center;gap:10px}
.logo-badge{width:34px;height:34px;border-radius:10px;background:linear-gradient(135deg,var(--primary),var(--accent));display:flex;align-items:center;justify-content:center;font-weight:900;color:#fff;font-size:15px;box-shadow:0 4px 12px rgba(236,72,153,.4)}
.logo-name{font-weight:800;font-size:15px}
.header-right{display:flex;align-items:center;gap:8px}
.btn-balance{display:flex;align-items:center;gap:5px;padding:0 14px;height:36px;border-radius:18px;font-weight:700;font-size:13px;background:rgba(236,72,153,.15);color:var(--primary);border:1px solid rgba(236,72,153,.3)}
.btn-login{padding:0 18px;height:36px;border-radius:18px;font-weight:700;font-size:13px;background:linear-gradient(135deg,var(--primary),#db2777);color:#fff;box-shadow:0 4px 12px rgba(236,72,153,.3)}
.btn-avatar{width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;color:#fff;font-size:12px;border:2px solid rgba(255,255,255,.1)}
main{padding:12px 0 80px;min-height:calc(100vh - 58px)}
.card{background:var(--card);border:1px solid var(--border);border-radius:14px}
.btn-primary{background:linear-gradient(135deg,var(--primary),#db2777);color:#fff;font-weight:700;transition:.2s;box-shadow:0 4px 12px rgba(236,72,153,.3)}
.btn-primary:hover{transform:translateY(-1px)}
.btn-primary:disabled{opacity:.5;cursor:not-allowed}
.btn-green{background:linear-gradient(135deg,var(--green),#059669);color:#fff;font-weight:700}
.btn-red{background:linear-gradient(135deg,var(--red),#dc2626);color:#fff;font-weight:700}
.btn-purple{background:linear-gradient(135deg,var(--accent),#6d28d9);color:#fff;font-weight:700}
.btn-blue{background:linear-gradient(135deg,var(--blue),#1d4ed8);color:#fff;font-weight:700}
.btn-bkash{background:linear-gradient(135deg,var(--bkash),#c10f5e);color:#fff;font-weight:700}
.hero{padding:20px;margin-bottom:14px;position:relative;overflow:hidden;background:linear-gradient(135deg,rgba(236,72,153,.15),rgba(124,58,237,.1));border:1px solid rgba(236,72,153,.2)}
.hero-row{display:flex;align-items:flex-start;justify-content:space-between;gap:16px;position:relative;z-index:2}
.hero h1{font-size:24px;font-weight:900;background:linear-gradient(135deg,#fff,#e9d5ff);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.hero p{font-size:12px;color:var(--muted);margin-top:4px}
.hero-btns{display:flex;gap:8px;margin-top:12px}
.hero-btns a{padding:7px 12px;border-radius:8px;font-size:11px;font-weight:700;color:#fff;display:flex;align-items:center;gap:4px}
.tg{background:linear-gradient(135deg,#26a5e4,#1a8ec7)}.yt{background:linear-gradient(135deg,#ff0000,#cc0000)}
.hero-emoji{font-size:56px;animation:glow 2s ease-in-out infinite;border-radius:50%}
@keyframes glow{0%,100%{box-shadow:0 0 0 0 rgba(236,72,153,.4)}50%{box-shadow:0 0 22px 5px rgba(236,72,153,.25)}}
.notif{padding:9px 12px;font-size:12px;font-weight:500;background:linear-gradient(135deg,rgba(239,68,68,.95),rgba(220,38,38,.95));color:#fff;overflow:hidden;margin-bottom:14px;border-radius:10px}
.notif-row{display:flex;align-items:center;gap:8px}.notif-text{overflow:hidden;flex:1}
.marquee{white-space:nowrap;animation:marquee 22s linear infinite}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
.tabs{display:flex;gap:6px;position:sticky;top:58px;z-index:20;padding:8px 0;margin:0 -12px 12px;padding-left:12px;padding-right:12px;background:rgba(10,6,20,.9);backdrop-filter:blur(12px);overflow-x:auto;white-space:nowrap}
.tab{padding:8px 14px;border-radius:10px;font-size:12px;font-weight:700;background:var(--card);border:1px solid var(--border);transition:.2s;color:var(--text);flex-shrink:0}
.tab.active{background:linear-gradient(135deg,var(--primary),#db2777);color:#fff;box-shadow:0 4px 12px rgba(236,72,153,.3);border-color:transparent}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
.prod-card{overflow:hidden;transition:.2s}
.prod-card:hover{transform:translateY(-2px);border-color:rgba(236,72,153,.4)}
.prod-img{aspect-ratio:4/3;display:flex;align-items:center;justify-content:center;font-size:48px;background:linear-gradient(135deg,var(--card2),rgba(124,58,237,.15));position:relative;overflow:hidden}
.prod-img img{width:100%;height:100%;object-fit:cover}
.badge-sale{position:absolute;top:8px;right:8px;font-size:9px;font-weight:800;padding:3px 8px;border-radius:999px;background:linear-gradient(135deg,var(--red),#dc2626);color:#fff;letter-spacing:.5px}
.badge-antiban{position:absolute;top:8px;left:8px;font-size:9px;font-weight:800;padding:3px 8px;border-radius:999px;background:linear-gradient(135deg,var(--green),#059669);color:#fff}
.badge-maint{position:absolute;top:8px;left:8px;font-size:9px;font-weight:800;padding:3px 8px;border-radius:999px;background:linear-gradient(135deg,var(--amber),#d97706);color:#fff}
.prod-body{padding:11px}
.prod-name{font-weight:800;font-size:13px;margin-bottom:3px;letter-spacing:-.2px;line-height:1.3}
.prod-desc{font-size:10px;color:var(--muted);display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;min-height:26px;margin-bottom:8px}
.price-row{display:flex;align-items:center;gap:6px;margin-bottom:8px}
.price{font-size:17px;font-weight:800;color:var(--primary)}
.old-price{font-size:11px;color:var(--muted);text-decoration:line-through}
.prod-btns{display:grid;grid-template-columns:1fr 1fr;gap:6px}
.btn-prod{padding:7px 4px;border-radius:8px;font-size:11px;font-weight:700;text-align:center}
nav.botnav{position:fixed;bottom:0;left:0;right:0;z-index:30;background:rgba(10,6,20,.92);backdrop-filter:blur(16px);border-top:1px solid rgba(45,33,80,.5)}
.botnav-in{max-width:768px;margin:0 auto;padding:0 4px;display:grid;grid-template-columns:repeat(5,1fr);height:56px}
.navbtn{display:flex;flex-direction:column;align-items:center;justify-content:center;gap:2px;font-size:10px;color:var(--muted);transition:.2s;font-weight:600}
.navbtn.active{color:var(--primary)}
.navbtn svg{width:19px;height:19px}
.modal{position:fixed;inset:0;z-index:50;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,.7);backdrop-filter:blur(6px);padding:16px}
.modal.show{display:flex}
.modal-card{background:var(--card);border:1px solid var(--border);border-radius:18px;padding:20px;width:100%;max-width:420px;max-height:90vh;overflow-y:auto;box-shadow:0 20px 60px rgba(0,0,0,.5)}
.modal-title{font-size:18px;font-weight:800;text-align:center;margin-bottom:14px;letter-spacing:-.3px}
.modal-close{position:absolute;top:14px;right:14px;color:var(--muted);font-size:22px;background:rgba(0,0,0,.3);width:30px;height:30px;border-radius:50%;display:flex;align-items:center;justify-content:center}
.field{margin-bottom:12px}
.field label{font-size:12px;color:var(--muted);display:block;margin-bottom:5px;font-weight:600}
.btn-full{width:100%;padding:11px;border-radius:11px;font-weight:700;font-size:14px}
.auth-toggle{text-align:center;font-size:13px;color:var(--muted);margin-top:12px}
.auth-toggle button{color:var(--primary);font-weight:700}
.sidebar{position:fixed;inset:0;z-index:50;display:none}
.sidebar.show{display:block}
.sidebar-bg{position:absolute;inset:0;background:rgba(0,0,0,.7);backdrop-filter:blur(4px)}
.sidebar-panel{position:absolute;right:0;top:0;bottom:0;width:280px;overflow-y:auto;background:var(--card);border-left:1px solid var(--border)}
.sidebar-head{padding:20px;background:linear-gradient(135deg,rgba(236,72,153,.2),rgba(124,58,237,.2));position:relative}
.sidebar-close{position:absolute;top:14px;right:14px;color:var(--muted);font-size:20px;background:rgba(0,0,0,.3);width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center}
.avatar-lg{width:60px;height:60px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:20px;font-weight:800;color:#fff;margin-bottom:8px;border:3px solid rgba(255,255,255,.15)}
.sidebar-name{font-weight:800;font-size:18px}
.sidebar-email{font-size:12px;color:var(--muted);word-break:break-all}
.sidebar-nav{padding:8px}
.sidebar-nav button{width:100%;text-align:left;padding:11px 13px;border-radius:10px;font-size:14px;font-weight:600;display:flex;align-items:center;gap:10px}
.sidebar-nav button:hover{background:rgba(255,255,255,.05)}
.sidebar-foot{padding:12px;border-top:1px solid var(--border)}
.btn-logout{width:100%;padding:11px;border-radius:10px;font-size:14px;font-weight:700;background:linear-gradient(135deg,var(--red),#dc2626);color:#fff}
.page-title{font-size:20px;font-weight:800;margin-bottom:16px;padding:0 4px;letter-spacing:-.3px}
.empty{text-align:center;padding:40px 20px;color:var(--muted)}
.empty-icon{font-size:48px;margin-bottom:12px;opacity:.5}
.stat-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:8px;margin-bottom:16px}
.stat{padding:14px}
.stat-label{font-size:9px;text-transform:uppercase;color:var(--muted);font-weight:700;letter-spacing:.5px}
.stat-val{font-size:18px;font-weight:800;margin-top:3px}
.list-item{display:flex;align-items:center;gap:12px;padding:12px;margin-bottom:8px}
.list-icon{width:40px;height:40px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:20px;background:var(--card2);flex-shrink:0}
.list-body{flex:1;min-width:0}
.list-title{font-weight:700;font-size:14px}
.list-sub{font-size:10px;color:var(--muted)}
.badge{font-size:10px;padding:2px 8px;border-radius:999px;font-weight:700}
.badge-green{background:rgba(16,185,129,.2);color:var(--green)}
.badge-amber{background:rgba(245,158,11,.2);color:var(--amber)}
.badge-red{background:rgba(239,68,68,.2);color:var(--red)}
.btn-copy{padding:7px 14px;border-radius:8px;font-size:12px;font-weight:700;background:var(--bkash);color:#fff;display:flex;align-items:center;gap:5px}
.bkash-box{padding:14px;border-radius:11px;font-size:13px;background:linear-gradient(135deg,rgba(226,19,110,.12),rgba(226,19,110,.05));margin-top:10px;border:1px solid rgba(226,19,110,.25)}
.bkash-num-row{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-top:6px}
.bkash-num{font-family:monospace;font-size:17px;font-weight:800;color:var(--bkash);letter-spacing:1px}
.toast{position:fixed;top:16px;left:50%;transform:translateX(-50%);background:var(--card);border:1px solid var(--border);padding:12px 20px;border-radius:11px;z-index:100;animation:slideDown .3s;font-weight:600;font-size:13px;box-shadow:0 8px 24px rgba(0,0,0,.4)}
@keyframes slideDown{from{opacity:0;transform:translate(-50%,-20px)}to{opacity:1;transform:translate(-50%,0)}}
.order-code-box{margin-top:8px;font-family:monospace;font-size:13px;padding:10px 12px;border-radius:8px;display:inline-block;background:rgba(16,185,129,.1);color:var(--green);border:1px solid rgba(16,185,129,.25);word-break:break-all}
.live-feed{margin-bottom:14px;overflow:hidden}
.live-feed-head{display:flex;align-items:center;gap:8px;margin-bottom:8px;padding:0 4px}
.live-dot{width:8px;height:8px;border-radius:50%;background:var(--green);animation:blink 1.5s infinite;box-shadow:0 0 8px rgba(16,185,129,.6)}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}
.live-feed-title{font-size:13px;font-weight:800}
.live-feed-sub{font-size:10px;color:var(--muted);font-weight:600}
.live-list{max-height:180px;overflow:hidden}
.live-item{display:flex;align-items:center;gap:10px;padding:9px 11px;border-radius:10px;background:var(--card);border:1px solid var(--border);margin-bottom:5px;animation:slideInRight .4s;font-size:12px}
@keyframes slideInRight{from{opacity:0;transform:translateX(20px)}to{opacity:1;transform:translateX(0)}}
.live-avatar{width:28px;height:28px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:800;color:#fff;font-size:10px;flex-shrink:0}
.live-body{flex:1;min-width:0}
.live-text{font-size:12px;line-height:1.4}
.live-text strong{color:var(--primary)}
.live-time{font-size:10px;color:var(--muted);margin-top:1px}
.live-icon{font-size:15px}
/* Recharge plans */
.plan-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin:12px 0}
.plan{padding:10px;border-radius:10px;border:1px solid var(--border);background:var(--card2);cursor:pointer;transition:.2s;text-align:center;position:relative}
.plan:hover{border-color:var(--primary)}
.plan.active{border-color:var(--primary);background:rgba(236,72,153,.1);box-shadow:0 0 0 2px rgba(236,72,153,.3)}
.plan.disabled{opacity:.4;cursor:not-allowed}
.plan-dur{font-size:13px;font-weight:800;color:var(--text)}
.plan-price{font-size:16px;font-weight:800;color:var(--primary);margin-top:3px}
.plan-stock{font-size:9px;color:var(--muted);margin-top:2px}
.plan-stock.out{color:var(--red)}
.qty-row{display:flex;align-items:center;gap:10px;margin:10px 0}
.qty-btn{width:34px;height:34px;border-radius:8px;background:var(--card2);font-size:18px;font-weight:700;display:flex;align-items:center;justify-content:center}
.qty-input{flex:1;text-align:center;font-weight:700;font-size:16px}
.setup-btn{padding:14px;border-radius:11px;font-weight:700;font-size:13px;margin-bottom:8px;display:flex;align-items:center;justify-content:center;gap:8px;text-align:center}
.fab-help{position:fixed;bottom:72px;right:14px;z-index:35;width:50px;height:50px;border-radius:50%;background:linear-gradient(135deg,var(--primary),#db2777);color:#fff;display:flex;align-items:center;justify-content:center;box-shadow:0 6px 18px rgba(236,72,153,.4);animation:glow 2s ease-in-out infinite}
/* Telegram Chat Widget */
.tg-chat-fab{position:fixed;bottom:72px;right:74px;z-index:35;width:50px;height:50px;border-radius:50%;background:linear-gradient(135deg,#26a5e4,#1a8ec7);color:#fff;display:flex;align-items:center;justify-content:center;box-shadow:0 6px 18px rgba(38,165,228,.4);cursor:pointer;transition:.2s}
.tg-chat-fab:hover{transform:scale(1.08)}
.tg-chat-fab svg{width:26px;height:26px}
.tg-chat-badge{position:absolute;top:-3px;right:-3px;width:18px;height:18px;border-radius:50%;background:var(--red);color:#fff;font-size:10px;font-weight:700;display:flex;align-items:center;justify-content:center;border:2px solid var(--bg)}
.tg-chat-panel{position:fixed;bottom:130px;right:14px;z-index:36;width:320px;max-width:calc(100vw - 28px);background:var(--card);border:1px solid var(--border);border-radius:16px;box-shadow:0 20px 50px rgba(0,0,0,.5);display:none;flex-direction:column;overflow:hidden;animation:slideUp .3s}
.tg-chat-panel.show{display:flex}
@keyframes slideUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.tg-chat-header{padding:14px 16px;background:linear-gradient(135deg,#26a5e4,#1a8ec7);color:#fff;display:flex;align-items:center;justify-content:space-between}
.tg-chat-header-info{display:flex;align-items:center;gap:10px}
.tg-chat-avatar{width:40px;height:40px;border-radius:50%;background:rgba(255,255,255,.2);display:flex;align-items:center;justify-content:center;font-size:22px}
.tg-chat-name{font-size:14px;font-weight:800}
.tg-chat-status{font-size:10px;opacity:.9;display:flex;align-items:center;gap:4px}
.tg-chat-status::before{content:'';width:7px;height:7px;border-radius:50%;background:#4ade80;display:inline-block}
.tg-chat-close{background:rgba(0,0,0,.2);border:none;color:#fff;width:28px;height:28px;border-radius:50%;cursor:pointer;font-size:16px;display:flex;align-items:center;justify-content:center}
.tg-chat-body{padding:14px;background:var(--card2);max-height:300px;overflow-y:auto;min-height:200px}
.tg-msg{margin-bottom:10px;max-width:80%;font-size:13px;line-height:1.4}
.tg-msg-in{background:var(--card);padding:9px 12px;border-radius:12px 12px 12px 4px;border:1px solid var(--border)}
.tg-msg-out{background:linear-gradient(135deg,var(--primary),#db2777);color:#fff;padding:9px 12px;border-radius:12px 12px 4px 12px;margin-left:auto;text-align:right}
.tg-msg-time{font-size:9px;opacity:.7;margin-top:3px}
.tg-chat-welcome{text-align:center;padding:20px 10px;color:var(--muted);font-size:12px}
.tg-chat-welcome-icon{font-size:40px;margin-bottom:8px}
.tg-chat-footer{padding:10px;border-top:1px solid var(--border);display:flex;gap:8px;background:var(--card)}
.tg-chat-input{flex:1;background:var(--card2);border:1px solid var(--border);color:var(--text);border-radius:10px;padding:9px 12px;font-size:13px;font-family:inherit}
.tg-chat-input:focus{outline:none;border-color:var(--primary)}
.tg-chat-send{background:linear-gradient(135deg,#26a5e4,#1a8ec7);color:#fff;border:none;width:38px;height:38px;border-radius:10px;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:16px}
.tg-chat-send:disabled{opacity:.5;cursor:not-allowed}
.tg-chat-login-hint{padding:16px;text-align:center;font-size:12px;color:var(--muted)}
.tg-chat-login-hint button{background:linear-gradient(135deg,var(--primary),#db2777);color:#fff;border:none;padding:8px 16px;border-radius:8px;font-weight:700;font-size:12px;margin-top:8px;cursor:pointer}
.tg-quick-reply{display:flex;gap:6px;flex-wrap:wrap;padding:0 10px 8px}
.tg-quick-reply button{font-size:11px;padding:5px 10px;border-radius:999px;background:rgba(38,165,228,.15);color:#26a5e4;border:1px solid rgba(38,165,228,.3);cursor:pointer;font-weight:600}
@media(min-width:640px){.grid{grid-template-columns:repeat(3,1fr)}.plan-grid{grid-template-columns:repeat(3,1fr)}}
</style>
</head>
<body>
<header><div class="header-in"><div class="logo"><div class="logo-badge">PB</div><span class="logo-name" id="siteName">Panel Bajar</span></div><div class="header-right" id="headerRight"></div></div></header>
<main><div class="container" id="main"></div></main>
<nav class="botnav"><div class="botnav-in">
<button class="navbtn" data-page="home" onclick="nav('home')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 12l9-9 9 9M5 10v10h14V10"/></svg>Home</button>
<button class="navbtn" data-page="orders" onclick="nav('orders')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M6 2l1 4h12l-2 8H8L6 2zM6 2H4M9 18a1 1 0 100 2 1 1 0 000-2zM17 18a1 1 0 100 2 1 1 0 000-2z"/></svg>My Order</button>
<button class="navbtn" data-page="codes" onclick="nav('codes')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M3 9l9-7 9 7v11a1 1 0 01-1 1h-5v-7H10v7H5a1 1 0 01-1-1V9z"/></svg>My Keys</button>
<button class="navbtn" data-page="account" onclick="nav('account')"><svg fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4 4-7 8-7s8 3 8 7"/></svg>Account</button>
</div></nav>
<div class="modal" id="modal" onclick="if(event.target===this)closeModal()"><div class="modal-card" id="modalContent" style="position:relative"></div></div>
<div class="modal" id="authModal" onclick="if(event.target===this)closeAuth()"><div class="modal-card" id="authContent" style="max-width:360px"></div></div>
<div class="sidebar" id="sidebar"><div class="sidebar-bg" onclick="closeSidebar()"></div><div class="sidebar-panel" id="sidebarPanel"></div></div>
<a href="#" id="fabHelp" class="fab-help" target="_blank" title="সাহায্য লাগবে?">💬</a>

<!-- Telegram Chat Widget -->
<div class="tg-chat-fab" onclick="toggleTgChat()" title="Telegram চ্যাট">
  <svg viewBox="0 0 24 24" fill="currentColor"><path d="M9.78 18.65l.28-4.23 7.68-6.92c.34-.31-.07-.46-.52-.19L7.74 13.3 3.64 12c-.88-.25-.89-.86.2-1.3l15.97-6.16c.73-.33 1.43.18 1.15 1.3l-2.72 12.81c-.19.91-.74 1.13-1.5.71L12.6 16.3l-1.99 1.93c-.23.23-.42.42-.83.42z"/></svg>
  <span class="tg-chat-badge" id="tgChatBadge" style="display:none">1</span>
</div>

<div class="tg-chat-panel" id="tgChatPanel">
  <div class="tg-chat-header">
    <div class="tg-chat-header-info">
      <div class="tg-chat-avatar">💬</div>
      <div>
        <div class="tg-chat-name" id="tgChatName">Admin Support</div>
        <div class="tg-chat-status">অনলাইন • সাধারণত ৫ মিনিটে রিপ্লাই</div>
      </div>
    </div>
    <button class="tg-chat-close" onclick="toggleTgChat()">✕</button>
  </div>
  <div class="tg-chat-body" id="tgChatBody"></div>
  <div class="tg-quick-reply" id="tgQuickReply">
    <button onclick="sendQuickReply('পেমেন্ট করেছি')">💰 পেমেন্ট করেছি</button>
    <button onclick="sendQuickReply('অর্ডার সম্পর্কে জানতে চাই')">📦 অর্ডার সম্পর্কে</button>
    <button onclick="sendQuickReply('সাহায্য লাগবে')">❓ সাহায্য লাগবে</button>
  </div>
  <div class="tg-chat-footer">
    <input type="text" class="tg-chat-input" id="tgChatInput" placeholder="মেসেজ লিখুন..." onkeydown="if(event.key==='Enter')sendTgMsg()" />
    <button class="tg-chat-send" onclick="sendTgMsg()">➤</button>
  </div>
</div>
<script>
/* ====================================================================
   🔥🔥🔥  FIREBASE CONFIG — এখানে আপনার Firebase কোডগুলো বসান  🔥🔥🔥
   --------------------------------------------------------------------
   কোথায় পাবেন? Firebase Console (console.firebase.google.com) →
   আপনার প্রজেক্ট → ⚙️ Project settings → General ট্যাব → নিচে স্ক্রল করুন →
   "Your apps" সেকশন → Web app (</> আইকন) → "SDK setup and configuration"
   → Config সিলেক্ট করলে নিচের মানগুলো দেখাবে।
   ওই মানগুলো কপি করে নিচের প্রতিটি উদ্ধৃতির ("") ভেতরে বসিয়ে দিন।

   ⚠️ প্যানেল পাবলিক করলে (সব ভিজিটরের জন্য) অবশ্যই এখানে বসান —
   সেটআপ ফর্ম দিয়ে সেভ করা কনফিগ শুধু নিজের ব্রাউজারেই থাকে।
   ==================================================================== */
var FIREBASE_CONFIG={
  apiKey: "AIzaSyC4rtb4f8GP4i2WCyB8T_rqnmkUPNhKs_Q",              /* যেমন: AIzaSyD1234abcd... */
  authDomain: "farmer-73a44.firebaseapp.com",          /* যেমন: panel-bajar.firebaseapp.com */
  projectId: "farmer-73a44",           /* যেমন: panel-bajar */
  storageBucket: "farmer-73a44.firebasestorage.app",       /* যেমন: panel-bajar.appspot.com */
  messagingSenderId: "919992492785",   /* যেমন: 123456789012 */
  appId: "1:919992492785:web:49a831f26c58afcd95ff50",               /* যেমন: 1:123456789012:web:abc123def456 */
  databaseURL: ""          /* (ঐচ্ছিক) যেমন: https://panel-bajar.firebaseio.com */
};
/* ============ FIREBASE SDK ============ */
let fbApp=null,fbDb=null,fbAuth=null,fbConnected=false,fbConfigSource='',fbLastError='',fbSyncStarted=false;
// কনফিগ কোথা থেকে নেবে: প্রথমে কোডের FIREBASE_CONFIG, না থাকলে সেটিংস (সেটআপ ফর্ম/অ্যাডমিন)
function getFbConfig(){
  var c={};
  try{c=window.FIREBASE_CONFIG||{}}catch(e){c={}}
  var s={};
  try{s=(typeof state!=='undefined'&&state&&state.settings)?state.settings:{}}catch(e){s={}}
  if(c.apiKey&&c.projectId&&c.appId&&String(c.apiKey).indexOf('YOUR_')!==0){
    return{apiKey:c.apiKey,authDomain:c.authDomain||'',projectId:c.projectId,databaseURL:c.databaseURL||'',storageBucket:c.storageBucket||'',messagingSenderId:c.messagingSenderId||'',appId:c.appId,from:'কোড (FIREBASE_CONFIG)'};
  }
  if(s.fb_api_key&&s.fb_project_id&&s.fb_app_id){
    return{apiKey:s.fb_api_key,authDomain:s.fb_auth_domain||'',projectId:s.fb_project_id,databaseURL:s.fb_database_url||'',storageBucket:s.fb_storage_bucket||'',messagingSenderId:s.fb_messaging_sender_id||'',appId:s.fb_app_id,from:'সেটিংস (ব্রাউজার)'};
  }
  return null;
}
function initFirebase(){
  try{
    if(typeof firebase==='undefined'){fbLastError='Firebase SDK লোড হয়নি — ইন্টারনেট সংযোগ চেক করুন';return false}
    if(fbConnected)return true;
    const cfg=getFbConfig();
    if(!cfg){return false}
    const config={apiKey:cfg.apiKey,authDomain:cfg.authDomain,projectId:cfg.projectId,storageBucket:cfg.storageBucket,messagingSenderId:cfg.messagingSenderId,appId:cfg.appId};
    if(cfg.databaseURL)config.databaseURL=cfg.databaseURL;
    if(!firebase.apps.length){fbApp=firebase.initializeApp(config)}else{fbApp=firebase.app()}
    fbDb=firebase.firestore();
    fbAuth=firebase.auth();
    fbConnected=true;
    fbConfigSource=cfg.from;
    fbLastError='';
    console.log('✅ Firebase সংযোগ সফল — সোর্স: '+cfg.from);
    return true;
  }catch(e){fbLastError=(e&&e.message)?e.message:String(e);console.warn('Firebase init error:',e);return false}
}
// Firebase-এ পুরো অ্যারে সেভ করুন (শুধু প্রথমবার আপলোড/reconcile-এ ব্যবহৃত)
function fbSync(collection,data){
  if(!fbConnected||!fbDb)return;
  try{fbDb.collection(collection).doc('main').set({data:JSON.stringify(data),updatedAt:new Date().toISOString()}).catch(e=>console.warn('FB sync err:',e))}catch(e){}
}
// নতুন অর্ডার/ইউজার Firebase-এ নিরাপদে যোগ করুন (transaction — অন্য ডিভাইসের ডেটা মুছে যাবে না)
function fbPushItem(col,item){
  if(!fbConnected||!fbDb)return;
  try{
    const ref=fbDb.collection(col).doc('main');
    fbDb.runTransaction(function(tx){
      return tx.get(ref).then(function(doc){
        let arr=[];
        if(doc.exists){try{arr=JSON.parse(doc.data().data||'[]')}catch(e){arr=[]}}
        if(!Array.isArray(arr))arr=[];
        arr.push(item);
        tx.set(ref,{data:JSON.stringify(arr),updatedAt:new Date().toISOString()});
      });
    }).then(function(){console.log('🔥 '+col+' → Firebase-এ পুশ হয়েছে')}).catch(function(e){console.warn('FB push err ('+col+'):',e)});
  }catch(e){console.warn('FB push err:',e)}
}
// Firebase-এ কালেকশন একদম খালি (doc নেই) হলে লোকাল ডেটা আপলোড — প্রথমবার সেটআপে কাজে লাগে
function fbReconcile(col,localArr){
  if(!fbConnected||!fbDb||!Array.isArray(localArr)||localArr.length===0)return;
  try{
    fbDb.collection(col).doc('main').get().then(function(doc){
      if(!doc.exists){console.log('🔥 '+col+' প্রথমবার Firebase-এ আপলোড হচ্ছে');fbSync(col,localArr)}
    }).catch(function(){});
  }catch(e){}
}
// অ্যাডমিন থেকে সেটিংস এলে fb_*/tg_* কীগুলো রক্ষা করুন — যেন সংযোগ কনফিগ মুছে না যায়
function applyFbSettings(s){
  if(!s||typeof s!=='object')return;
  const keep=['fb_api_key','fb_auth_domain','fb_project_id','fb_database_url','fb_storage_bucket','fb_messaging_sender_id','fb_app_id','tg_bot_token','tg_chat_id'];
  keep.forEach(function(k){if(s[k]===undefined&&state.settings[k]!==undefined)s[k]=state.settings[k]});
  state.settings=s;
  localStorage.setItem('pb_settings',JSON.stringify(s));
  render();
}
// Firestore সত্যিই পড়া যাচ্ছে কিনা টেস্ট (Rules সমস্যা ধরার জন্য)
function fbTestConnection(cb){
  if(!fbConnected||!fbDb){cb&&cb(false,'আগে Firebase সংযোগ করুন');return}
  try{
    fbDb.collection('settings').doc('main').get({source:'server'}).then(function(){cb&&cb(true)}).catch(function(e){cb&&cb(false,(e&&e.code)?e.code:((e&&e.message)||'অজানা সমস্যা'))});
  }catch(e){cb&&cb(false,String(e))}
}
// Firebase থেকে ডেটা লোড করুন
function fbLoad(collection,callback){
  if(!fbConnected||!fbDb){callback&&callback(null);return}
  try{fbDb.collection(collection).doc('main').get().then(doc=>{if(doc.exists){const data=JSON.parse(doc.data().data||'[]');callback&&callback(data)}else{callback&&callback(null)}}).catch(e=>{console.warn('FB load err:',e);callback&&callback(null)})}catch(e){callback&&callback(null)}
}
// Firebase real-time listener
function fbListen(collection,callback){
  if(!fbConnected||!fbDb){return}
  try{fbDb.collection(collection).doc('main').onSnapshot(doc=>{if(doc.exists){try{const data=JSON.parse(doc.data().data||'[]');callback&&callback(data)}catch(e){}}})}catch(e){}
}
</script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-auth-compat.js"></script>
<script>
let state={user:JSON.parse(localStorage.getItem('pb_user')||'null'),users:JSON.parse(localStorage.getItem('pb_users')||'[]'),products:JSON.parse(localStorage.getItem('pb_products')||'[]'),orders:JSON.parse(localStorage.getItem('pb_orders')||'[]'),settings:JSON.parse(localStorage.getItem('pb_settings')||JSON.stringify({site_name:'Panel Bajar',tagline:'Buy Premium Mods & Hacks',notification:'স্বাগতম Panel Bajar-এ! পেমেন্ট করার আগে এডমিনের সাথে কথা বলুন।',notif_active:true,telegram:'https://t.me/panelbajar',youtube:'https://youtube.com/@panelbajar',bkash_number:'01XXXXXXXXX',help_url:'https://t.me/panelbajar'})),page:'home',productTab:'NON_ROOT',authMode:'login'};
// লোকাল সেভ — Firebase-এ পুরো অ্যারে ওভাররাইট করা হয় না; নতুন অর্ডার/ইউজার যায় fbPushItem দিয়ে
function save(){['users','products','orders'].forEach(k=>localStorage.setItem('pb_'+k,JSON.stringify(state[k])));localStorage.setItem('pb_user',JSON.stringify(state.user));localStorage.setItem('pb_settings',JSON.stringify(state.settings))}
function uid(){return Date.now().toString(36)+Math.random().toString(36).slice(2,6)}
function $(id){return document.getElementById(id)}
function val(id){return $(id).value}
function fmt(n){return '৳'+Number(n).toFixed(0)}
function tAgo(d){return new Date(d).toLocaleString('bn-BD')}
function timeAgoShort(d){const diff=Date.now()-new Date(d).getTime();const m=Math.floor(diff/60000);if(m<1)return 'এইমাত্র';if(m<60)return m+' মিনিট আগে';const h=Math.floor(m/60);if(h<24)return h+' ঘন্টা আগে';return Math.floor(h/24)+' দিন আগে'}
function toast(m){const t=document.createElement('div');t.className='toast';t.textContent=m;document.body.appendChild(t);setTimeout(()=>t.remove(),3000)}
function copyText(text){try{if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(text).then(()=>toast('কপি হয়েছে')).catch(()=>fallbackCopy(text))}else{fallbackCopy(text)}}catch(e){fallbackCopy(text)}}
function fallbackCopy(text){const ta=document.createElement('textarea');ta.value=text;ta.style.position='fixed';ta.style.opacity='0';document.body.appendChild(ta);ta.select();try{document.execCommand('copy');toast('কপি হয়েছে')}catch(e){toast('কপি করতে সমস্যা')}document.body.removeChild(ta)}

/* ============ TELEGRAM CHAT WIDGET ============ */
let tgChatOpen=false,tgChatMessages=[];
function toggleTgChat(){
  const panel=$('tgChatPanel');
  tgChatOpen=!tgChatOpen;
  if(tgChatOpen){
    panel.classList.add('show');
    $('tgChatBadge').style.display='none';
    renderTgChat();
    setTimeout(()=>$('tgChatInput')?.focus(),100);
  }else{
    panel.classList.remove('show');
  }
}
function renderTgChat(){
  const body=$('tgChatBody');if(!body)return;
  if(!state.user){
    body.innerHTML=`<div class="tg-chat-welcome"><div class="tg-chat-welcome-icon">💬</div><p>চ্যাট করতে লগইন করুন</p></div><div class="tg-chat-login-hint"><p>অ্যাডমিনের সাথে সরাসরি চ্যাট করুন</p><button onclick="closeTgChat();openAuth('login')">লগইন করুন</button></div>`;
    $('tgQuickReply').style.display='none';
    document.querySelector('.tg-chat-footer').style.display='none';
    return;
  }
  $('tgQuickReply').style.display='flex';
  document.querySelector('.tg-chat-footer').style.display='flex';
  $('tgChatName').textContent=state.settings.site_name+' Support';
  if(tgChatMessages.length===0){
    body.innerHTML=`<div class="tg-chat-welcome"><div class="tg-chat-welcome-icon">👋</div><p>স্বাগতম <strong>${state.user.username}</strong>!</p><p style="margin-top:6px">কীভাবে সাহায্য করতে পারি?</p></div>`;
    return;
  }
  body.innerHTML=tgChatMessages.map(m=>`<div class="tg-msg" style="${m.out?'margin-left:auto':''}"><div class="${m.out?'tg-msg-out':'tg-msg-in'}">${m.text}</div><div class="tg-msg-time" style="${m.out?'text-align:right':''}">${m.time}</div></div>`).join('');
  body.scrollTop=body.scrollHeight;
}
function sendTgMsg(){
  if(!state.user){openAuth('login');return}
  const input=$('tgChatInput');const text=input.value.trim();
  if(!text)return;
  const now=new Date().toLocaleTimeString('bn-BD',{hour:'2-digit',minute:'2-digit'});
  tgChatMessages.push({text,time:now,out:true});
  input.value='';
  renderTgChat();
  // Telegram-এ মেসেজ পাঠান (যদি bot token থাকে)
  sendTelegramToAdmin(state.user.username+': '+text);
  // অটো রিপ্লাই
  setTimeout(()=>{
    tgChatMessages.push({text:'আপনার মেসেজ পেয়েছি! শীঘ্রই রিপ্লাই দিচ্ছি। জরুরি হলে সরাসরি Telegram-এ যোগাযোগ করুন: '+state.settings.telegram,time:new Date().toLocaleTimeString('bn-BD',{hour:'2-digit',minute:'2-digit'}),out:false});
    renderTgChat();
  },1500);
}
function sendQuickReply(text){
  $('tgChatInput').value=text;
  sendTgMsg();
}
function closeTgChat(){tgChatOpen=false;$('tgChatPanel').classList.remove('show')}
function sendTelegramToAdmin(msg){
  const s=state.settings;
  if(!s.tg_bot_token||!s.tg_chat_id)return;
  try{
    fetch('https://api.telegram.org/bot'+s.tg_bot_token+'/sendMessage',{
      method:'POST',headers:{'Content-Type':'application/json'},
      body:JSON.stringify({chat_id:s.tg_chat_id,text:'💬 <b>চ্যাট মেসেজ</b>\n\n👤 '+state.user.username+' ('+state.user.email+')\n💬 '+msg,parse_mode:'HTML'})
    }).catch(()=>{});
  }catch(e){}
}

/* AUTH */
function openAuth(mode){state.authMode=mode||'login';renderAuth();$('authModal').classList.add('show')}
function closeAuth(){$('authModal').classList.remove('show')}
function toggleAuthMode(){state.authMode=state.authMode==='login'?'register':'login';renderAuth()}
function renderAuth(){const isL=state.authMode==='login';$('authContent').innerHTML=`<h2 class="modal-title">${isL?'লগইন করুন':'রেজিস্টার করুন'}</h2><div class="field" style="display:${isL?'none':'block'}"><label>ইউজারনেম</label><input id="authUsername" placeholder="আপনার নাম" /></div><div class="field"><label>ইমেইল</label><input id="authEmail" type="email" placeholder="email@example.com" /></div><div class="field"><label>পাসওয়ার্ড</label><input id="authPassword" type="password" placeholder="••••••••" onkeydown="if(event.key==='Enter')doAuth()" /></div><button class="btn-primary btn-full" onclick="doAuth()">${isL?'লগইন':'রেজিস্টার'}</button><p class="auth-toggle">${isL?'অ্যাকাউন্ট নেই?':'ইতিমধ্যে অ্যাকাউন্ট আছে?'}<button onclick="toggleAuthMode()">${isL?'রেজিস্টার করুন':'লগইন করুন'}</button></p>`}
function doAuth(){const e=$('authEmail').value.trim().toLowerCase();const p=$('authPassword').value;if(!e||!p){toast('সব ঘর পূরণ করুন');return}if(state.authMode==='register'){const u=$('authUsername').value.trim();if(!u){toast('ইউজারনেম দিন');return}if(state.users.find(x=>x.email===e)){toast('এই ইমেইল ইতিমধ্যে ব্যবহৃত');return}const colors=['#ec4899','#7c3aed','#06b6d4','#f97316','#10b981'];const nu={id:uid(),email:e,username:u,password:p,role:'USER',totalOrders:0,totalSpent:0,banned:false,avatarColor:colors[Math.floor(Math.random()*colors.length)],createdAt:new Date().toISOString()};state.users.push(nu);state.user=nu;save();fbPushItem('users',nu);closeAuth();toast('অ্যাকাউন্ট তৈরি হয়েছে!');render()}else{const u=state.users.find(x=>x.email===e);if(!u||u.password!==p){toast('ইমেইল/পাসওয়ার্ড ভুল');return}if(u.banned){toast('অ্যাকাউন্ট ব্যান করা');return}state.user=u;save();closeAuth();toast('স্বাগতম!');render()}}
function logout(){state.user=null;save();toast('লগআউট হয়েছে');nav('home')}
function nav(p){if(!state.user&&['orders','codes','account'].includes(p)){openAuth('login');return}state.page=p;render()}
function openSidebar(){$('sidebar').classList.add('show')}
function closeSidebar(){$('sidebar').classList.remove('show')}
function openModal(html){$('modalContent').innerHTML=html;$('modal').classList.add('show')}
function closeModal(){$('modal').classList.remove('show')}
window.addEventListener('storage',function(e){if(e.key&&e.key.startsWith('pb_')){state.users=JSON.parse(localStorage.getItem('pb_users')||'[]');state.products=JSON.parse(localStorage.getItem('pb_products')||'[]');state.orders=JSON.parse(localStorage.getItem('pb_orders')||'[]');state.settings=JSON.parse(localStorage.getItem('pb_settings')||JSON.stringify(state.settings));if(state.user){const f=state.users.find(x=>x.id===state.user.id);if(f)state.user=f}render()}});

/* LIVE FEED */
function generateLiveFeed(){const real=state.orders.slice().reverse().slice(0,6).map(o=>{const u=state.users.find(x=>x.id===o.userId);const p=state.products.find(x=>x.id===o.productId);return{user:u?.username||'User',color:u?.avatarColor||'#7c3aed',product:p?.name||'Product',icon:p?.icon||'🎮',time:o.createdAt,real:true}});const demoNames=[['Rahim','#ec4899'],['Karim','#7c3aed'],['Sadia','#06b6d4'],['Tanvir','#f97316'],['Nusrat','#10b981'],['Imran','#ef4444'],['Farhan','#7c3aed'],['Mim','#ec4899']];const demoProducts=state.products.filter(p=>p.status==='ACTIVE');if(demoProducts.length===0)return real;const demo=[];for(let i=0;i<6;i++){const n=demoNames[Math.floor(Math.random()*demoNames.length)];const p=demoProducts[Math.floor(Math.random()*demoProducts.length)];demo.push({user:n[0],color:n[1],product:p.name,icon:p.icon,time:new Date(Date.now()-Math.floor(Math.random()*60*60*1000)).toISOString(),real:false})}return[...real,...demo].sort((a,b)=>new Date(b.time)-new Date(a.time)).slice(0,6)}
function renderLiveFeedItems(){const items=generateLiveFeed();if(items.length===0)return '<div style="text-align:center;padding:16px;color:var(--muted);font-size:12px">এখনো কোনো অর্ডার নেই</div>';return items.map(it=>`<div class="live-item"><div class="live-avatar" style="background:${it.color}">${it.user.slice(0,2).toUpperCase()}</div><div class="live-body"><div class="live-text"><strong>${it.user}</strong> কিনেছেন <span class="live-icon">${it.icon}</span> ${it.product}${it.real?' <span style="color:var(--green);font-size:10px">✓</span>':''}</div><div class="live-time">⏰ ${timeAgoShort(it.time)}</div></div></div>`).join('')}
setInterval(function(){state.orders=JSON.parse(localStorage.getItem('pb_orders')||'[]');state.users=JSON.parse(localStorage.getItem('pb_users')||'[]');if(state.page==='home'){const f=document.getElementById('liveFeed');if(f)f.innerHTML=renderLiveFeedItems()}},3500);

/* RENDER */
function render(){
  $('siteName').textContent=state.settings.site_name;
  $('fabHelp').href=state.settings.help_url||state.settings.telegram||'#';
  const hr=$('headerRight');
  if(state.user){
    hr.innerHTML=`<button class="btn-avatar" style="background:${state.user.avatarColor}" onclick="openSidebar()">${state.user.username.slice(0,2).toUpperCase()}</button>`;
  }else{
    hr.innerHTML=`<button class="btn-login" onclick="openAuth('login')">লগইন</button>`;
  }
  if(state.user){
    $('sidebarPanel').innerHTML=`<div class="sidebar-head"><button class="sidebar-close" onclick="closeSidebar()">✕</button><div class="avatar-lg" style="background:${state.user.avatarColor}">${state.user.username.slice(0,2).toUpperCase()}</div><div class="sidebar-name">${state.user.username}</div><div class="sidebar-email">${state.user.email}</div></div><nav class="sidebar-nav"><button onclick="nav('home');closeSidebar()">🏠 হোম</button><button onclick="nav('account');closeSidebar()">👤 My Account</button><button onclick="nav('orders');closeSidebar()">📦 My Order</button><button onclick="nav('codes');closeSidebar()">🎫 My Keys</button>${state.user.role==='ADMIN'?'<button onclick="closeSidebar();openFbSetup()">🔥 Firebase সেটআপ</button>':''}</nav><div class="sidebar-foot"><button class="btn-logout" onclick="logout()">🚪 লগআউট</button></div>`;
  }
  document.querySelectorAll('.navbtn').forEach(b=>b.classList.toggle('active',b.dataset.page===state.page));
  const m=$('main');
  if(state.page==='home')m.innerHTML=renderHome();
  else if(state.page==='account')m.innerHTML=renderAccount();
  else if(state.page==='orders')m.innerHTML=renderOrders();
  else if(state.page==='codes')m.innerHTML=renderCodes();
  window.scrollTo(0,0);
}

function renderHome(){
  const prods=state.products.filter(p=>p.status==='ACTIVE'&&p.category===state.productTab);
  const notif=state.settings.notif_active?`<div class="notif"><div class="notif-row"><span>🔔</span><div class="notif-text"><div class="marquee">${state.settings.notification} &nbsp;&nbsp;&nbsp; ${state.settings.notification}</div></div></div></div>`:'';
  const tabs=['NON_ROOT','ROOT','IPHONE','PC'].map(t=>`<button class="tab ${state.productTab===t?'active':''}" onclick="state.productTab='${t}';render()">${t==='NON_ROOT'?'🟢 NON ROOT':t==='ROOT'?'🔴 ROOT':t==='IPHONE'?'📱 IPHONE':'💻 PC'}</button>`).join('');
  return notif+`<div class="card hero"><div class="hero-row"><div style="flex:1"><h1>${state.settings.site_name}</h1><p>${state.settings.tagline}</p><div class="hero-btns"><a href="${state.settings.telegram}" target="_blank" class="tg">✈️ Telegram</a><a href="${state.settings.youtube}" target="_blank" class="yt">▶️ YouTube</a></div></div><div class="hero-emoji">🎮</div></div></div><div class="live-feed"><div class="live-feed-head"><span class="live-dot"></span><div><div class="live-feed-title">🔴 LIVE Orders</div><div class="live-feed-sub">ইউজাররা এখন কী কিনছে</div></div></div><div class="live-list" id="liveFeed">${renderLiveFeedItems()}</div></div><div class="tabs">${tabs}</div>${prods.length===0?`<div class="card empty"><div class="empty-icon">🛍️</div>এই ক্যাটেগরিতে কোনো প্রোডাক্ট নেই</div>`:`<div class="grid">${prods.map(p=>renderProductCard(p)).join('')}</div>`}`;
}

function renderProductCard(p){
  const imgHtml=p.image?`<img src="${p.image}" alt="${p.name}" onerror="this.style.display='none';this.parentElement.innerHTML='<span style=\\'font-size:48px\\'>${p.icon||'🎮'}</span>'+this.parentElement.innerHTML.indexOf('badge')" />`:`<span style="font-size:48px">${p.icon||'🎮'}</span>`;
  const minPrice=p.plans&&p.plans.length>0?Math.min(...p.plans.filter(pl=>pl.stock>0).map(pl=>pl.price),p.plans[0]?.price||p.price||0):p.price;
  return `<div class="card prod-card"><div class="prod-img">${p.image?`<img src="${p.image}" alt="${p.name}" onerror="this.style.display='none'" />`:''}${p.antiban?'<div class="badge-antiban">100% ANTI BAN</div>':''}${p.maintenance?'<div class="badge-maint">MAINTENANCE</div>':''}${p.oldPrice?'<div class="badge-sale">🔥 SALE</div>':''}</div><div class="prod-body"><div class="prod-name">${p.name}</div><div class="prod-desc">${p.description||''}</div><div class="price-row"><span class="price">${fmt(minPrice)}</span>${p.oldPrice?`<span class="old-price">${fmt(p.oldPrice)}</span>`:''}</div><div class="prod-btns"><button class="btn-prod btn-blue" onclick="openFileSetup('${p.id}')">📁 FILE & SETUP</button><button class="btn-prod btn-primary" onclick="openBuyNow('${p.id}')" ${p.maintenance?'disabled':''}>${p.maintenance?'MAINTENANCE':'🛒 BUY NOW'}</button></div></div></div>`;
}

/* FILE & SETUP MODAL */
function openFileSetup(pid){
  const p=state.products.find(x=>x.id===pid);if(!p)return;
  openModal(`<button class="modal-close" onclick="closeModal()">✕</button><h2 class="modal-title">📁 ${p.name}</h2><p style="font-size:12px;color:var(--muted);text-align:center;margin-bottom:14px">নিচের যেকোনো বাটনে ক্লিক করুন</p>${p.url_full_details?`<a href="${p.url_full_details}" target="_blank" class="setup-btn btn-green">📹 PANEL FULL DETAILS (ভিডিও)</a>`:''}${p.url_setup_video?`<a href="${p.url_setup_video}" target="_blank" class="setup-btn btn-red">🎬 PANEL SETUP VIDEO (ভিডিও)</a>`:''}${p.url_download?`<a href="${p.url_download}" target="_blank" class="setup-btn btn-purple">⬇️ PANEL DOWNLOAD LINK</a>`:''}${p.url_iphone_setup?`<a href="${p.url_iphone_setup}" target="_blank" class="setup-btn btn-blue">📱 AIMKILL IPHONE SETUP VIDEO</a>`:''}${!p.url_full_details&&!p.url_setup_video&&!p.url_download&&!p.url_iphone_setup?'<p style="text-align:center;color:var(--muted);font-size:12px;padding:16px">এখনো কোনো লিংক যোগ করা হয়নি</p>':''}<button class="btn-full" style="background:var(--card2);margin-top:8px" onclick="closeModal()">বন্ধ করুন</button>`);
}

/* BUY NOW MODAL (Recharge Plans) */
let selectedPlan=null,selectedQty=1;
function openBuyNow(pid){
  const p=state.products.find(x=>x.id===pid);if(!p)return;
  if(!state.user){openAuth('login');return}
  selectedPlan=null;selectedQty=1;
  const plans=p.plans&&p.plans.length>0?p.plans:[{dur:'1 Day',price:p.price,stock:99}];
  const plansHtml=plans.map((pl,i)=>`<div class="plan ${pl.stock===0?'disabled':''}" onclick="${pl.stock>0?`selectPlan(${i})`:''}"><div class="plan-dur">${pl.dur}</div><div class="plan-price">${fmt(pl.price)}</div><div class="plan-stock ${pl.stock===0?'out':''}">${pl.stock===0?'Out of Stock':'Stock: '+pl.stock}</div></div>`).join('');
  openModal(`<button class="modal-close" onclick="closeModal()">✕</button><h2 class="modal-title">🛒 ${p.name}</h2><div style="background:var(--card2);padding:10px;border-radius:10px;margin-bottom:10px;font-size:12px;color:var(--muted)"><strong style="color:var(--text)">Select Recharge:</strong> আপনার প্ল্যান বাছুন</div><div class="plan-grid" id="planGrid">${plansHtml}</div><div class="field"><label>Quantity</label><div class="qty-row"><button class="qty-btn" onclick="changeQty(-1)">−</button><input class="qty-input" id="qtyInput" value="1" readonly /><button class="qty-btn" onclick="changeQty(1)">+</button></div></div><div class="bkash-box"><div style="font-weight:800;color:var(--bkash);display:flex;align-items:center;gap:6px"><span>📲</span> bKash Payment</div><div class="bkash-num-row"><div class="bkash-num" id="payBkashNum">${state.settings.bkash_number||'01XXXXXXXXX'}</div><button class="btn-copy" onclick="copyText('${state.settings.bkash_number||''}')">📋 কপি</button></div><div style="margin-top:8px;color:var(--muted);font-size:11px;line-height:1.5">⚠️ উপরের নাম্বারে <strong id="payTotal" style="color:var(--bkash)">${fmt(0)}</strong> পাঠান, তারপর TxnID লিখে অর্ডার করুন</div></div><div class="field" style="margin-top:10px"><label>bKash Transaction ID</label><input id="payTxn" placeholder="8N7Y6T5R4E" style="font-family:monospace" /></div><button class="btn-bkash btn-full" onclick="submitOrder('${pid}')">✅ অর্ডার সাবমিট করুন</button><p style="text-align:center;font-size:11px;color:var(--muted);margin-top:8px">⏳ অর্ডার PENDING হবে, অ্যাডমিন একসেপ্ট করলে API Key দিবে</p>`);
  window._currentPlans=plans;
}
function selectPlan(i){selectedPlan=i;document.querySelectorAll('.plan').forEach((p,j)=>p.classList.toggle('active',j===i));updatePayTotal()}
function changeQty(d){selectedQty=Math.max(1,selectedQty+d);$('qtyInput').value=selectedQty;updatePayTotal()}
function updatePayTotal(){const total=selectedPlan!==null?window._currentPlans[selectedPlan].price*selectedQty:0;const el=$('payTotal');if(el)el.textContent=fmt(total)}

function submitOrder(pid){
  const p=state.products.find(x=>x.id===pid);if(!p)return;
  if(selectedPlan===null){toast('একটি প্ল্যান সিলেক্ট করুন');return}
  const plan=window._currentPlans[selectedPlan];
  const txn=$('payTxn').value.trim();
  if(!txn){toast('Transaction ID দিন');return}
  const order={id:uid(),userId:state.user.id,productId:p.id,planDur:plan.dur,price:plan.price*selectedQty,qty:selectedQty,status:'PENDING',txnId:txn,codeContent:'',createdAt:new Date().toISOString()};
  state.orders.push(order);
  if(plan.stock>0)plan.stock-=selectedQty;
  save();fbPushItem('orders',order);closeModal();toast('অর্ডার সফল! PENDING-এ আছে। অ্যাডমিন শীঘ্রই API Key দিয়ে ডেলিভারি দেবে।');nav('orders');
}

function renderAccount(){const u=state.user;return `<h1 class="page-title">My Account</h1><div class="card hero" style="margin-bottom:14px"><div style="display:flex;align-items:center;gap:14px"><div class="avatar-lg" style="background:${u.avatarColor}">${u.username.slice(0,2).toUpperCase()}</div><div><div style="font-size:11px;color:var(--muted)">Hi,</div><div style="font-size:18px;font-weight:800">${u.username} 👋</div><div style="font-size:11px;color:var(--muted);word-break:break-all">${u.email}</div></div></div></div><div class="stat-grid"><div class="card stat"><div class="stat-label">Total Orders</div><div class="stat-val" style="color:#26a5e4">${u.totalOrders||0}</div></div><div class="card stat"><div class="stat-label">Total Spent</div><div class="stat-val" style="color:var(--green)">${fmt(u.totalSpent||0)}</div></div></div>`}
function renderOrders(){const orders=state.orders.filter(o=>o.userId===state.user.id);return `<h1 class="page-title">My Order</h1>${orders.length===0?`<div class="card empty"><div class="empty-icon">📦</div><div style="font-weight:600">No order found!</div><div style="font-size:12px;margin-top:4px">এখনো কোনো অর্ডার দেননি</div><button class="btn-primary" style="margin-top:14px;padding:9px 22px;border-radius:10px" onclick="nav('home')">Order Now</button></div>`:orders.map(o=>{const p=state.products.find(x=>x.id===o.productId);return `<div class="card list-item"><div class="list-icon">${p?.icon||'📦'}</div><div class="list-body"><div style="display:flex;justify-content:space-between;gap:8px"><span class="list-title">${p?.name||'—'}</span><span style="font-weight:800;color:var(--primary)">${fmt(o.price)}</span></div><div class="list-sub" style="margin-top:2px">${o.planDur?'⏱ '+o.planDur+' • ':''}${o.qty>1?o.qty+'x • ':''}${tAgo(o.createdAt)}${o.txnId?' • Txn: '+o.txnId:''}</div><div style="margin-top:5px"><span class="badge ${o.status==='COMPLETED'?'badge-green':o.status==='PENDING'?'badge-amber':'badge-red'}">${o.status}</span></div>${o.status==='COMPLETED'&&o.codeContent?`<div class="order-code-box">🎫 API Key: ${o.codeContent}</div>`:''}${o.status==='PENDING'?`<div style="margin-top:6px;font-size:11px;color:var(--amber);font-weight:600">⏳ অ্যাডমিনের অনুমোদনের অপেক্ষায়...</div>`:''}</div></div>`}).join('')}`}
function renderCodes(){const orders=state.orders.filter(o=>o.userId===state.user.id&&o.status==='COMPLETED'&&o.codeContent);return `<h1 class="page-title">My API Keys</h1>${orders.length===0?`<div class="card empty"><div class="empty-icon">🎫</div><div style="font-weight:600">No API key found!</div><div style="font-size:12px;margin-top:4px">এখনো কোনো API key কেনেননি</div><button class="btn-primary" style="margin-top:14px;padding:9px 22px;border-radius:10px" onclick="nav('home')">Order Now</button></div>`:orders.map(o=>{const p=state.products.find(x=>x.id===o.productId);return `<div class="card list-item"><div class="list-icon">${p?.icon||'🎫'}</div><div class="list-body"><div class="list-title">${p?.name||'—'}</div>${o.planDur?`<div class="list-sub">⏱ ${o.planDur}</div>`:''}<div class="order-code-box">🎫 ${o.codeContent}</div><div class="list-sub" style="margin-top:4px">${tAgo(o.createdAt)}</div></div><button class="btn-copy" onclick="copyText('${(o.codeContent||'').replace(/'/g,"\\'")}')">📋 কপি</button></div>`}).join('')}`}

/* ============ FIREBASE সেটআপ মডাল (অ্যাডমিনের জন্য) ============ */
function openFbSetup(){
  const s=state.settings;
  let codeSet=false;
  try{codeSet=!!(window.FIREBASE_CONFIG&&window.FIREBASE_CONFIG.apiKey&&window.FIREBASE_CONFIG.apiKey!==''&&String(window.FIREBASE_CONFIG.apiKey).indexOf('YOUR_')!==0)}catch(e){}
  const status=fbConnected?'✅ সংযুক্ত — সোর্স: '+(fbConfigSource||'?'):(codeSet?'⚙️ কোডে কনফিগ সেট আছে, কিন্তু সংযোগ হয়নি':'❌ কনফিগার করা হয়নি — অফলাইন মোড');
  const f=function(id,label,ph){return '<div class="field"><label>'+label+'</label><input id="fbf_'+id+'" placeholder="'+ph+'" value="'+String(s[id]||'').replace(/"/g,'&quot;')+'" /></div>'};
  openModal(`<button class="modal-close" onclick="closeModal()">✕</button><h2 class="modal-title">🔥 Firebase সেটআপ</h2><div style="padding:10px;border-radius:10px;font-size:12px;font-weight:700;background:${fbConnected?'rgba(16,185,129,.12)':'rgba(239,68,68,.12)'};color:${fbConnected?'var(--green)':'var(--red)'};margin-bottom:12px">${status}</div><p style="font-size:11px;color:var(--muted);line-height:1.6;margin-bottom:10px">💡 সবচেয়ে ভালো উপায়: এই ফাইলের স্ক্রিপ্টের একদম শুরুতে <strong style="color:var(--primary)">FIREBASE_CONFIG</strong> ব্লকে আপনার Firebase কোডগুলো বসান — তাহলে সব ডিভাইস/ভিজিটরের জন্য সংযোগ হবে। নিচের ফর্ম শুধু এই ব্রাউজারে সেভ হয় (দ্রুত টেস্টের জন্য)।</p>${f('fb_api_key','API Key *','AIzaSy...')}${f('fb_project_id','Project ID *','panel-bajar')}${f('fb_app_id','App ID *','1:1234567890:web:abc123')}${f('fb_auth_domain','Auth Domain','panel-bajar.firebaseapp.com')}${f('fb_storage_bucket','Storage Bucket','panel-bajar.appspot.com')}${f('fb_messaging_sender_id','Messaging Sender ID','123456789012')}${f('fb_database_url','Database URL (ঐচ্ছিক)','https://...firebaseio.com')}<div style="margin:12px 0 4px;font-weight:800;font-size:13px">✈️ Telegram Bot (ঐচ্ছিক — চ্যাট নোটিফিকেশনের জন্য)</div>${f('tg_bot_token','Bot Token','123456:ABC-DEF...')}${f('tg_chat_id','Admin Chat ID','123456789')}<button class="btn-primary btn-full" onclick="saveFbSetup()">💾 সেভ ও সংযোগ করুন</button><button class="btn-full" style="background:var(--card2);margin-top:8px" onclick="fbTestConnection(function(ok,err){toast(ok?'✅ Firestore কাজ করছে!':'❌ Firestore এরর: '+(err||'')+' — Rules চেক করুন')})">🔌 সংযোগ টেস্ট করুন</button><p style="font-size:10px;color:var(--muted);margin-top:10px;line-height:1.6">📌 প্রথমবার ব্যবহারের আগে Firebase Console → Firestore Database → <strong>Create Database</strong> → <strong>Test mode</strong> সিলেক্ট করুন, নাহলে ডেটা পড়া/লেখা যাবে না।</p>`);
}
function saveFbSetup(){
  const s=state.settings;
  ['fb_api_key','fb_project_id','fb_app_id','fb_auth_domain','fb_storage_bucket','fb_messaging_sender_id','fb_database_url','tg_bot_token','tg_chat_id'].forEach(function(k){const el=$('fbf_'+k);if(el)s[k]=el.value.trim()});
  localStorage.setItem('pb_settings',JSON.stringify(s));
  fbConnected=false;fbDb=null;fbLastError='';fbSyncStarted=false;
  const reinit=function(){
    if(initFirebase()){
      startFbSync();
      fbTestConnection(function(ok,err){toast(ok?'✅ Firebase সংযোগ সম্পূর্ণ সফল!':'⚠ Firestore এরর: '+(err||'')+' — Rules/কনফিগ চেক করুন')});
    }else{
      toast('❌ সংযোগ ব্যর্থ — API Key / Project ID / App ID ঠিকভাবে দিন');
    }
    openFbSetup();
  };
  if(typeof firebase!=='undefined'&&firebase.apps&&firebase.apps.length){try{firebase.app().delete().then(reinit).catch(reinit)}catch(e){reinit()}}else{reinit()}
}

function seedDemo(){
  if(state.users.length===0){
    state.users.push({id:uid(),email:'admin@panelbajar.com',username:'admin',password:'admin123',role:'ADMIN',totalOrders:0,totalSpent:0,banned:false,avatarColor:'#7c3aed',createdAt:new Date().toISOString()});
    state.users.push({id:uid(),email:'saimon@example.com',username:'saimon',password:'user123',role:'USER',totalOrders:0,totalSpent:0,banned:false,avatarColor:'#ec4899',createdAt:new Date().toISOString()});
  }
  if(state.products.length>0)return;
  const samples=[
    {name:'AIM HACK - ANDROID - IOS',icon:'🎯',category:'NON_ROOT',antiban:true,maintenance:false,image:'',description:'100% Anti Ban • Auto Aim • Android & iOS Support',plans:[{dur:'1 Hour',price:15,stock:99},{dur:'3 Hours',price:40,stock:0},{dur:'6 Hours',price:80,stock:0},{dur:'12 Hours',price:120,stock:99},{dur:'1 Day',price:160,stock:99},{dur:'3 Days',price:300,stock:0},{dur:'7 Days',price:600,stock:0},{dur:'30 Days',price:1200,stock:0}]},
    {name:'BALA MODS - NON ROOT',icon:'🔥',category:'NON_ROOT',antiban:true,image:'',description:'Main ID Safe • Anti Ban • Aim • ESP • Non Root',plans:[{dur:'1 Day',price:25,stock:99},{dur:'7 Days',price:150,stock:99},{dur:'30 Days',price:500,stock:99}]},
    {name:'AIM HACK - ROOT',icon:'🎯',category:'ROOT',antiban:true,image:'',description:'Root Version • Premium Features • Anti Ban',plans:[{dur:'1 Day',price:30,stock:99},{dur:'7 Days',price:180,stock:99},{dur:'30 Days',price:600,stock:99}]},
    {name:'IPHONE MOD',icon:'📱',category:'IPHONE',antiban:true,image:'',description:'iOS Only • No Jailbreak • Anti Ban',plans:[{dur:'1 Day',price:50,stock:99},{dur:'7 Days',price:300,stock:99},{dur:'30 Days',price:1000,stock:99}]},
    {name:'PC ESP HACK',icon:'💻',category:'PC',antiban:true,image:'',description:'PC Version • ESP • Aim • Wallhack',plans:[{dur:'1 Day',price:40,stock:99},{dur:'7 Days',price:250,stock:99},{dur:'30 Days',price:800,stock:99}]}
  ];
  samples.forEach(s=>state.products.push({id:uid(),slug:s.name.toLowerCase().replace(/\s+/g,'-'),...s,status:'ACTIVE',url_full_details:'',url_setup_video:'',url_download:'',url_iphone_setup:''}));
  save();
}
seedDemo();render();
// Firebase init ও real-time sync — অ্যাডমিন প্যানেলের সাথে অটো সিঙ্ক
function startFbSync(){
  if(fbSyncStarted||!fbConnected)return;
  fbSyncStarted=true;
  console.log('🔥 Firebase সিঙ্ক চালু — অ্যাডমিন থেকে অর্ডার একসেপ্ট করলে অটো আপডেট হবে');
  // Real-time listeners — অ্যাডমিন প্যানেল থেকে ডেটা বদলালে ইউজার প্যানেলে অটো আপডেট
  fbListen('products',function(data){if(data&&data.length>0){state.products=data;localStorage.setItem('pb_products',JSON.stringify(data));if(state.page==='home')render()}});
  fbListen('orders',function(data){if(data&&data.length>0){state.orders=data;localStorage.setItem('pb_orders',JSON.stringify(data));if(['orders','codes','account'].includes(state.page))render()}});
  fbListen('users',function(data){if(data&&data.length>0){state.users=data;localStorage.setItem('pb_users',JSON.stringify(data));if(state.user){const f=data.find(x=>x.id===state.user.id);if(f){state.user=f;localStorage.setItem('pb_user',JSON.stringify(f))}render()}}});
  fbListen('settings',function(data){if(data&&data.length>0&&data[0])applyFbSettings(data[0])});
  // Firebase থেকে initial লোড (সংযোগ হওয়ার সাথে সাথেই চলবে)
  fbLoad('products',function(d){if(d&&d.length>0){state.products=d;localStorage.setItem('pb_products',JSON.stringify(d));if(state.page==='home')render()}});
  fbLoad('orders',function(d){if(d&&d.length>0){state.orders=d;localStorage.setItem('pb_orders',JSON.stringify(d));if(['orders','codes','account'].includes(state.page))render()}});
  fbLoad('users',function(d){if(d&&d.length>0){state.users=d;localStorage.setItem('pb_users',JSON.stringify(d));if(state.user){const f=d.find(x=>x.id===state.user.id);if(f){state.user=f;localStorage.setItem('pb_user',JSON.stringify(f))}render()}}});
  fbLoad('settings',function(d){if(d&&d.length>0&&d[0])applyFbSettings(d[0])});
  // Firebase খালি থাকলে লোকাল ইউজার/অর্ডার আপলোড (প্রথমবার)
  fbReconcile('users',state.users);
  fbReconcile('orders',state.orders);
}
setTimeout(function(){
  if(initFirebase()){
    startFbSync();
  }else{
    console.log('⚠ Firebase কনফিগার করা নেই — অফলাইন মোডে চলছে (localStorage only)');
    if(!localStorage.getItem('pb_fb_warned')){localStorage.setItem('pb_fb_warned','1');toast('⚠ Firebase সংযোগ নেই — কোডে FIREBASE_CONFIG বসান বা অ্যাডমিন লগইন করে সেটআপ করুন')}
  }
},1500);
</script>
</body>
</html>
