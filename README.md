<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>AGI Network</title>
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;900&display=swap" rel="stylesheet">

<!-- ====================================================
     ✅ كود Google AdSense الحقيقي
     📌 استبدل ca-pub-XXXXXXXXXXXXXXXX برقم ناشرك
     من: https://www.google.com/adsense
     ==================================================== -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
<style>
:root{
  --gold:#F5C518;--gold-dark:#C9A000;
  --bg:#08090F;--card:#0F1420;--card2:#141C2E;--input:#0A0D18;
  --border:rgba(245,197,24,0.18);--border2:rgba(255,255,255,0.07);
  --text:#E8ECF4;--muted:#6B7A9A;
  --green:#00D68F;--red:#FF4560;--blue:#4B8FFF;--purple:#9B6DFF;
  --bottom:60px;
}
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent;}
html,body{width:100%;min-height:100vh;overflow-x:hidden;}
body{font-family:'Cairo',sans-serif;background:var(--bg);color:var(--text);padding-bottom:var(--bottom);}

/* ── TOP HEADER ── */
.header{
  position:sticky;top:0;z-index:100;
  background:var(--card);border-bottom:1px solid var(--border2);
  padding:10px 14px;display:flex;align-items:center;justify-content:space-between;
}
.header-logo{display:flex;align-items:center;gap:8px;}
.header-logo-icon{font-size:22px;}
.header-logo-text{font-size:16px;font-weight:900;color:var(--gold);letter-spacing:2px;}
.header-right{display:flex;align-items:center;gap:8px;}
.hbtn{height:32px;padding:0 12px;border-radius:8px;font-family:'Cairo',sans-serif;font-size:12px;font-weight:700;cursor:pointer;border:none;}
.hbtn-gold{background:var(--gold);color:#000;}
.hbtn-out{background:transparent;border:1px solid var(--border2);color:var(--text);}
.notif{width:32px;height:32px;border-radius:8px;background:var(--card2);border:1px solid var(--border2);display:flex;align-items:center;justify-content:center;font-size:15px;position:relative;}
.ndot{position:absolute;top:5px;left:5px;width:6px;height:6px;border-radius:50%;background:var(--red);}

/* ── PAGE TITLE BAR ── */
.page-bar{background:var(--card2);border-bottom:1px solid var(--border2);padding:8px 14px;font-size:13px;font-weight:700;color:var(--muted);}

/* ── CONTENT ── */
.content{padding:12px;}
.page{display:none;}
.page.active{display:block;animation:fi .2s ease;}
@keyframes fi{from{opacity:0;transform:translateY(5px);}to{opacity:1;transform:translateY(0);}}

/* ── BOTTOM NAV ── */
.bottom-nav{
  position:fixed;bottom:0;left:0;right:0;z-index:200;
  background:var(--card);border-top:1px solid var(--border2);
  display:flex;height:var(--bottom);
  padding-bottom:env(safe-area-inset-bottom,0px);
}
.bn-item{
  flex:1;display:flex;flex-direction:column;align-items:center;
  justify-content:center;gap:2px;cursor:pointer;
  transition:color .2s;color:var(--muted);padding:4px 0;
  position:relative;
}
.bn-item.active{color:var(--gold);}
.bn-icon{font-size:18px;line-height:1;}
.bn-label{font-size:9px;font-weight:700;letter-spacing:.3px;}
.bn-badge{position:absolute;top:4px;right:calc(50% - 12px);background:var(--red);color:#fff;font-size:8px;font-weight:800;padding:1px 4px;border-radius:10px;}

/* ── MORE MENU ── */
.more-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.7);z-index:150;backdrop-filter:blur(4px);}
.more-overlay.open{display:block;}
.more-sheet{position:fixed;bottom:var(--bottom);left:0;right:0;background:var(--card);border-top:1px solid var(--border);border-radius:20px 20px 0 0;padding:16px;z-index:160;transform:translateY(100%);transition:transform .3s ease;}
.more-sheet.open{transform:translateY(0);}
.more-title{text-align:center;font-size:13px;font-weight:700;color:var(--muted);margin-bottom:14px;}
.more-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;}
.more-item{display:flex;flex-direction:column;align-items:center;gap:5px;cursor:pointer;padding:10px 4px;border-radius:12px;background:var(--card2);border:1px solid var(--border2);transition:border-color .2s;}
.more-item:hover{border-color:var(--gold);}
.more-item-icon{font-size:22px;}
.more-item-label{font-size:10px;font-weight:700;color:var(--muted);text-align:center;}

/* ── CARDS ── */
.card{background:var(--card);border:1px solid var(--border2);border-radius:14px;padding:14px;margin-bottom:12px;}
.card-head{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px;}
.card-title{font-size:14px;font-weight:700;}

/* ── STAT GRID ── */
.stat-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:12px;}
.stat-card{background:var(--card);border:1px solid var(--border2);border-radius:12px;padding:14px;}
.stat-icon{font-size:18px;margin-bottom:6px;}
.stat-val{font-size:20px;font-weight:800;margin-bottom:2px;}
.stat-label{font-size:11px;color:var(--muted);font-weight:600;}
.stat-change{font-size:11px;margin-top:6px;font-weight:600;}
.up{color:var(--green);}
.dn{color:var(--red);}

/* ── WALLET HERO ── */
.wallet-hero{
  background:linear-gradient(135deg,#0F1E35,#0A1220);
  border:1px solid rgba(245,197,24,.3);border-radius:16px;padding:18px;margin-bottom:12px;
}
.wh-label{font-size:11px;color:var(--muted);font-weight:600;margin-bottom:2px;}
.wh-total{font-size:32px;font-weight:900;color:var(--gold);}
.wh-total span{font-size:14px;font-weight:500;color:var(--muted);}
.wh-min{font-size:11px;color:var(--green);margin-top:4px;font-weight:600;}
.wh-actions{display:flex;gap:8px;margin-top:14px;}
.wh-btn{flex:1;height:38px;border-radius:10px;display:flex;align-items:center;justify-content:center;gap:5px;font-family:'Cairo',sans-serif;font-size:12px;font-weight:700;cursor:pointer;border:none;}
.wh-btn.w{background:var(--gold);color:#000;}
.wh-btn.d{background:var(--card2);color:var(--text);border:1px solid var(--border2);}
.wh-btn.s{background:var(--card2);color:var(--text);border:1px solid var(--border2);}

/* ── COIN GRID ── */
.coin-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;}
.coin-card{background:var(--card2);border:1px solid var(--border2);border-radius:12px;padding:14px;text-align:center;}
.coin-sym{font-size:24px;margin-bottom:5px;}
.coin-name{font-size:13px;font-weight:700;}
.coin-bal{font-size:10px;color:var(--muted);margin-top:2px;}
.coin-usd{font-size:14px;font-weight:800;color:var(--gold);margin-top:3px;}

/* ── LIVE ROW ── */
.live-row{display:flex;align-items:center;gap:8px;padding:10px 12px;background:var(--card2);border-radius:10px;margin-bottom:6px;border:1px solid var(--border2);}
.pulse{width:7px;height:7px;border-radius:50%;background:var(--green);animation:pu 1.5s infinite;flex-shrink:0;}
@keyframes pu{0%,100%{opacity:1;transform:scale(1);}50%{opacity:.4;transform:scale(1.4);}}
.live-text{font-size:12px;flex:1;color:var(--muted);}
.live-earn{font-size:12px;font-weight:800;color:var(--gold);}

/* ── MACHINE CARD ── */
.mc{background:var(--card);border:1px solid var(--border2);border-radius:14px;padding:14px;margin-bottom:12px;}
.mc.owned{border-color:rgba(245,197,24,.3);}
.mc-badge{display:inline-flex;align-items:center;font-size:10px;font-weight:800;padding:3px 9px;border-radius:20px;margin-bottom:10px;}
.mc-badge.free{background:rgba(0,214,143,.12);color:var(--green);}
.mc-badge.pro{background:rgba(245,197,24,.12);color:var(--gold);}
.mc-badge.lk{background:rgba(255,255,255,.06);color:var(--muted);}
.mc-badge.vip{background:rgba(155,109,255,.12);color:var(--purple);}
.mc-name{font-size:15px;font-weight:800;margin-bottom:2px;}
.mc-hash{font-size:11px;color:var(--muted);margin-bottom:12px;}
.mc-row{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:12px;}
.mc-stat{background:var(--card2);border-radius:8px;padding:8px 10px;}
.mc-stat-l{font-size:10px;color:var(--muted);margin-bottom:1px;font-weight:600;}
.mc-stat-v{font-size:13px;font-weight:700;}
.mc-prog{height:4px;background:rgba(255,255,255,.06);border-radius:4px;margin-bottom:5px;overflow:hidden;}
.mc-bar{height:100%;border-radius:4px;background:linear-gradient(90deg,var(--gold-dark),var(--gold));transition:width .8s ease;}
.mc-spd{font-size:10px;color:var(--muted);margin-bottom:10px;}
.cs-lbl{font-size:10px;color:var(--muted);font-weight:600;margin-bottom:5px;}
.cs{display:flex;gap:5px;flex-wrap:wrap;margin-bottom:12px;}
.cb{padding:4px 8px;border-radius:6px;background:var(--input);border:1px solid var(--border2);color:var(--muted);font-size:11px;font-weight:600;cursor:pointer;font-family:'Cairo',sans-serif;}
.cb.active{background:rgba(245,197,24,.12);border-color:var(--gold);color:var(--gold);}
.mst{display:flex;align-items:center;gap:6px;padding:7px 10px;border-radius:8px;margin-top:8px;font-size:11px;font-weight:600;}
.mst.run{background:rgba(0,214,143,.08);color:var(--green);border:1px solid rgba(0,214,143,.15);}
.mst.stop{background:rgba(255,255,255,.03);color:var(--muted);border:1px solid var(--border2);}

/* ── AD CARD ── */
.ad-card{display:flex;align-items:center;gap:12px;padding:12px;background:var(--card2);border-radius:12px;margin-bottom:8px;border:1px solid var(--border2);}
.ad-thumb{width:46px;height:46px;border-radius:10px;background:var(--input);display:flex;align-items:center;justify-content:center;font-size:22px;flex-shrink:0;}
.ad-info{flex:1;}
.ad-title{font-size:13px;font-weight:700;margin-bottom:2px;}
.ad-desc{font-size:11px;color:var(--muted);}
.ad-rew{font-size:11px;color:var(--gold);font-weight:700;margin-top:3px;}

/* ── EARN TABS ── */
.earn-tabs{display:flex;background:var(--card2);border-radius:10px;padding:3px;gap:3px;margin-bottom:14px;}
.earn-tab{flex:1;padding:8px 4px;border-radius:8px;text-align:center;font-size:12px;font-weight:700;cursor:pointer;color:var(--muted);font-family:'Cairo',sans-serif;}
.earn-tab.active{background:var(--card);color:var(--gold);}

/* ── REF ── */
.ref-hero{background:linear-gradient(135deg,#0F2010,#0A1208);border:1px solid rgba(0,214,143,.2);border-radius:14px;padding:16px;margin-bottom:12px;}
.ref-code-row{display:flex;align-items:center;gap:8px;margin:10px 0;}
.ref-code{font-size:20px;font-weight:900;color:var(--gold);letter-spacing:3px;flex:1;}
.copy-btn{height:32px;padding:0 12px;border-radius:8px;background:var(--gold);color:#000;font-family:'Cairo',sans-serif;font-size:11px;font-weight:800;cursor:pointer;border:none;white-space:nowrap;}
.ref-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-bottom:12px;}
.ref-stat{background:var(--card2);border-radius:10px;padding:12px;text-align:center;}
.ref-val{font-size:18px;font-weight:800;color:var(--gold);}
.ref-lbl{font-size:10px;color:var(--muted);font-weight:600;margin-top:2px;}
.friend-row{display:flex;align-items:center;gap:10px;padding:11px 12px;background:var(--card2);border-radius:10px;margin-bottom:6px;}
.friend-av{width:32px;height:32px;border-radius:9px;background:var(--input);display:flex;align-items:center;justify-content:center;font-size:14px;flex-shrink:0;}
.friend-name{font-size:13px;font-weight:700;flex:1;}
.friend-earn{font-size:13px;font-weight:800;color:var(--gold);}

/* ── GAMES ── */
.games-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;}
.game-card{background:var(--card);border:1px solid var(--border2);border-radius:14px;overflow:hidden;cursor:pointer;}
.game-thumb{height:90px;display:flex;align-items:center;justify-content:center;font-size:44px;}
.game-body{padding:10px;}
.game-name{font-size:13px;font-weight:800;margin-bottom:2px;}
.game-rew{font-size:11px;color:var(--gold);font-weight:700;}

/* ── SWAP ── */
.swap-box{background:var(--card2);border:1px solid var(--border2);border-radius:12px;padding:14px;margin-bottom:8px;}
.swap-lbl{font-size:11px;color:var(--muted);font-weight:600;margin-bottom:6px;}
.swap-row{display:flex;align-items:center;gap:8px;}
.swap-input{flex:1;background:transparent;border:none;font-size:22px;font-weight:800;color:var(--text);font-family:'Cairo',sans-serif;outline:none;width:60px;}
.swap-sel{background:var(--input);border:1px solid var(--border2);border-radius:8px;padding:6px 10px;color:var(--text);font-family:'Cairo',sans-serif;font-size:12px;font-weight:700;outline:none;}
.swap-mid{text-align:center;padding:4px;font-size:20px;color:var(--gold);cursor:pointer;}
.swap-rate-txt{font-size:11px;color:var(--muted);text-align:center;margin-bottom:12px;}

/* ── ADMIN ── */
.admin-lock{display:flex;flex-direction:column;align-items:center;justify-content:center;min-height:60vh;gap:12px;}
.adm-input{width:260px;background:var(--card2);border:1px solid var(--border2);border-radius:10px;padding:11px 16px;color:var(--text);font-family:'Cairo',sans-serif;font-size:14px;outline:none;text-align:center;}
.adm-input:focus{border-color:var(--gold);}
.adm-wallet{background:linear-gradient(135deg,#1A0A00,#280E00);border:1px solid rgba(245,197,24,.35);border-radius:14px;padding:18px;margin-bottom:14px;}
.adm-bal{font-size:32px;font-weight:900;color:var(--gold);}
.adm-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:14px;}
.adm-stat{background:var(--card);border:1px solid var(--border2);border-radius:12px;padding:14px;text-align:center;}
.adm-stat-v{font-size:20px;font-weight:800;color:var(--gold);}
.adm-stat-l{font-size:11px;color:var(--muted);margin-top:2px;font-weight:600;}
.adm-actions{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-bottom:14px;}
.adm-act{background:var(--card);border:1px solid var(--border2);border-radius:12px;padding:12px 6px;text-align:center;cursor:pointer;}
.adm-act-icon{font-size:22px;margin-bottom:4px;}
.adm-act-lbl{font-size:10px;font-weight:700;color:var(--muted);}

/* ── TABLE ── */
.tbl{width:100%;border-collapse:collapse;font-size:12px;}
.tbl th{text-align:right;padding:8px 10px;color:var(--muted);font-weight:700;font-size:10px;border-bottom:1px solid var(--border2);}
.tbl td{padding:10px;border-bottom:1px solid rgba(255,255,255,.03);vertical-align:middle;}
.tbl tr:last-child td{border:none;}
.bdg{display:inline-flex;padding:2px 8px;border-radius:20px;font-size:10px;font-weight:700;}
.bg-g{background:rgba(0,214,143,.12);color:var(--green);}
.bg-b{background:rgba(75,143,255,.12);color:var(--blue);}
.bg-o{background:rgba(245,197,24,.12);color:var(--gold);}
.bg-r{background:rgba(255,69,96,.12);color:var(--red);}

/* ── MODAL ── */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.8);z-index:300;align-items:flex-end;justify-content:center;backdrop-filter:blur(4px);}
.modal-overlay.open{display:flex;}
.modal{background:var(--card);border:1px solid rgba(245,197,24,.2);border-radius:20px 20px 0 0;padding:20px;width:100%;max-height:90vh;overflow-y:auto;}
.modal-title{font-size:16px;font-weight:800;margin-bottom:16px;}
.inp-g{margin-bottom:12px;}
.inp-l{font-size:11px;color:var(--muted);font-weight:600;margin-bottom:5px;}
.inp{width:100%;background:var(--input);border:1px solid var(--border2);border-radius:9px;padding:10px 12px;color:var(--text);font-family:'Cairo',sans-serif;font-size:14px;outline:none;}
.inp:focus{border-color:var(--gold);}
select.inp{cursor:pointer;}
.modal-foot{display:flex;gap:8px;margin-top:14px;}

/* ── W-LINKS ── */
.w-link-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:12px;}
.w-link{display:flex;align-items:center;gap:8px;padding:12px;border-radius:10px;background:var(--card2);border:1px solid var(--border2);text-decoration:none;color:var(--text);}
.w-link-icon{font-size:22px;}
.w-link-name{font-size:13px;font-weight:700;}
.w-link-chain{font-size:10px;color:var(--muted);}

/* ── VIDEO ── */
.video-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.95);z-index:400;flex-direction:column;align-items:center;justify-content:center;gap:14px;}
.video-overlay.open{display:flex;}
.video-screen{width:90vw;height:50vw;max-height:200px;background:var(--card);border-radius:14px;display:flex;align-items:center;justify-content:center;font-size:44px;border:2px solid var(--gold);}
.video-timer{font-size:40px;font-weight:900;color:var(--gold);}
.skip-btn{height:40px;padding:0 24px;border-radius:10px;background:var(--gold);color:#000;font-family:'Cairo',sans-serif;font-size:14px;font-weight:800;cursor:pointer;border:none;opacity:.35;pointer-events:none;}
.skip-btn.ready{opacity:1;pointer-events:all;}

/* ── TOAST ── */
.toast{position:fixed;bottom:72px;left:50%;transform:translateX(-50%);background:var(--card);border:1px solid var(--gold);border-radius:10px;padding:10px 18px;font-size:13px;font-weight:700;color:var(--gold);z-index:500;opacity:0;transition:opacity .3s;pointer-events:none;white-space:nowrap;box-shadow:0 4px 20px rgba(0,0,0,.5);}
.toast.show{opacity:1;}

/* ── UTILS ── */
.btn{height:38px;padding:0 14px;border-radius:9px;font-family:'Cairo',sans-serif;font-size:13px;font-weight:700;cursor:pointer;border:none;display:inline-flex;align-items:center;gap:5px;}
.btn-gold{background:var(--gold);color:#000;}
.btn-out{background:transparent;border:1px solid var(--border2);color:var(--text);}
.btn-sm{height:30px;padding:0 10px;font-size:11px;}
.btn-full{width:100%;justify-content:center;}
::-webkit-scrollbar{width:3px;}
::-webkit-scrollbar-thumb{background:var(--border2);border-radius:3px;}
</style>
</head>
<body>

<!-- HEADER -->
<div class="header">
  <div class="header-logo">
    <div class="header-logo-icon">⛏️</div>
    <div class="header-logo-text">AGI NETWORK</div>
  </div>
  <div class="header-right">
    <button class="hbtn hbtn-gold" onclick="openM('depositModal')">+ إيداع</button>
    <button class="hbtn hbtn-out" onclick="openM('withdrawModal')">سحب</button>
    <div class="notif">🔔<div class="ndot"></div></div>
  </div>
</div>

<!-- PAGE TITLE BAR -->
<div class="page-bar" id="pageBar">AGI Network / لوحة التحكم</div>

<!-- CONTENT -->
<div class="content">

<!-- ████ DASHBOARD ████ -->
<div class="page active" id="page-dashboard">
  <div class="wallet-hero">
    <div class="wh-label">إجمالي رصيدك</div>
    <div class="wh-total" id="d-balance">$847.32 <span>USD</span></div>
    <div class="wh-min">✓ أدنى سحب: $0.001</div>
    <div class="wh-actions">
      <button class="wh-btn w" onclick="openM('withdrawModal')">📤 سحب</button>
      <button class="wh-btn d" onclick="openM('depositModal')">📥 إيداع</button>
      <button class="wh-btn s" onclick="go('swap')">🔄 تبديل</button>
    </div>
  </div>

  <div class="stat-grid">
    <div class="stat-card">
      <div class="stat-icon">⛏️</div>
      <div class="stat-val" id="d-mining">$0.000000</div>
      <div class="stat-label">أرباح التعدين الحي</div>
      <div class="stat-change up">↑ يعمل الآن</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">⚡</div>
      <div class="stat-val" id="d-active">0</div>
      <div class="stat-label">الماكينات النشطة</div>
      <div class="stat-change up">اضغط تشغيل ⛏️</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">👥</div>
      <div class="stat-val">23</div>
      <div class="stat-label">الأصدقاء المدعوون</div>
      <div class="stat-change up">↑ +3 هذا الأسبوع</div>
    </div>
    <div class="stat-card">
      <div class="stat-icon">💰</div>
      <div class="stat-val">$47.80</div>
      <div class="stat-label">أرباح الإحالة</div>
      <div class="stat-change up">↑ +$2.10</div>
    </div>
  </div>

  <div class="card">
    <div class="card-head"><div class="card-title">🔥 التعدين الحي</div><span class="bdg bg-g">● نشط</span></div>
    <div class="live-row"><div class="pulse"></div><div class="live-text">Starter — <span id="dc0">BTC</span></div><div class="live-earn" id="le0">$0.000000</div></div>
    <div class="live-row"><div class="pulse"></div><div class="live-text">Pro — <span id="dc1">ETH</span></div><div class="live-earn" id="le1">$0.000000</div></div>
    <div class="live-row"><div class="pulse"></div><div class="live-text">Turbo — <span id="dc2">USDT</span></div><div class="live-earn" id="le2">$0.000000</div></div>
  </div>

  <div class="card">
    <div class="card-head"><div class="card-title">⚡ اكسب الآن</div><button class="btn btn-gold btn-sm" onclick="go('earn')">المزيد</button></div>
    <div class="ad-card"><div class="ad-thumb">📺</div><div class="ad-info"><div class="ad-title">شاهد إعلان 30 ثانية</div><div class="ad-rew">+$0.05</div></div><button class="btn btn-gold btn-sm" onclick="watchVideo()">شاهد</button></div>
    <div class="ad-card"><div class="ad-thumb">🖱️</div><div class="ad-info"><div class="ad-title">زيارة موقع معلن</div><div class="ad-rew">+$0.02</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">زيارة</button></div>
  </div>

  <div class="card">
    <div class="card-head"><div class="card-title">📋 آخر المعاملات</div></div>
    <div style="overflow-x:auto"><table class="tbl">
      <thead><tr><th>النوع</th><th>المبلغ</th><th>الحالة</th></tr></thead>
      <tbody>
        <tr><td>⛏️ تعدين</td><td style="color:var(--green);font-weight:700">+$3.24</td><td><span class="bdg bg-g">مكتمل</span></td></tr>
        <tr><td>👥 إحالة</td><td style="color:var(--green);font-weight:700">+$1.50</td><td><span class="bdg bg-g">مكتمل</span></td></tr>
        <tr><td>🎮 لعبة</td><td style="color:var(--green);font-weight:700">+$0.35</td><td><span class="bdg bg-g">مكتمل</span></td></tr>
        <tr><td>💸 سحب</td><td style="color:var(--red);font-weight:700">-$100</td><td><span class="bdg bg-b">معلق</span></td></tr>
      </tbody>
    </table></div>
  </div>
</div>

<!-- ████ MINING ████ -->
<div class="page" id="page-mining">
  <div class="mc owned">
    <div class="mc-badge free">✓ مجانية — ممتلكة</div>
    <div class="mc-name">⚙️ Starter Miner</div>
    <div class="mc-hash">1 TH/s • مجانية تماماً</div>
    <div class="mc-row">
      <div class="mc-stat"><div class="mc-stat-l">الربح/يوم</div><div class="mc-stat-v" style="color:var(--green)">$0.50</div></div>
      <div class="mc-stat"><div class="mc-stat-l">السرعة</div><div class="mc-stat-v" id="spd-s">0%</div></div>
    </div>
    <div class="mc-prog"><div class="mc-bar" id="bar-s" style="width:0%"></div></div>
    <div class="mc-spd" id="stxt-s">⏸ متوقفة</div>
    <div class="cs-lbl">اختر عملة التعدين:</div>
    <div class="cs">
      <button class="cb active" onclick="setCoin('s',this,'BTC')">₿ BTC</button>
      <button class="cb" onclick="setCoin('s',this,'ETH')">Ξ ETH</button>
      <button class="cb" onclick="setCoin('s',this,'SOL')">◎ SOL</button>
      <button class="cb" onclick="setCoin('s',this,'USDT')">₮ USDT</button>
    </div>
    <button class="btn btn-gold btn-full" id="btn-s" onclick="toggleM('s')">▶ تشغيل التعدين</button>
    <div class="mst stop" id="mst-s">⏸ متوقف</div>
  </div>

  <div class="mc owned">
    <div class="mc-badge pro">★ Pro — ممتلكة</div>
    <div class="mc-name">🔧 Pro Miner</div>
    <div class="mc-hash">5 TH/s • $4.99</div>
    <div class="mc-row">
      <div class="mc-stat"><div class="mc-stat-l">الربح/يوم</div><div class="mc-stat-v" style="color:var(--green)">$2.50</div></div>
      <div class="mc-stat"><div class="mc-stat-l">السرعة</div><div class="mc-stat-v" id="spd-p">0%</div></div>
    </div>
    <div class="mc-prog"><div class="mc-bar" id="bar-p" style="width:0%"></div></div>
    <div class="mc-spd" id="stxt-p">⏸ متوقفة</div>
    <div class="cs-lbl">اختر عملة التعدين:</div>
    <div class="cs">
      <button class="cb" onclick="setCoin('p',this,'BTC')">₿ BTC</button>
      <button class="cb active" onclick="setCoin('p',this,'ETH')">Ξ ETH</button>
      <button class="cb" onclick="setCoin('p',this,'SOL')">◎ SOL</button>
      <button class="cb" onclick="setCoin('p',this,'USDT')">₮ USDT</button>
      <button class="cb" onclick="setCoin('p',this,'LTC')">◐ LTC</button>
    </div>
    <button class="btn btn-gold btn-full" id="btn-p" onclick="toggleM('p')">▶ تشغيل التعدين</button>
    <div class="mst stop" id="mst-p">⏸ متوقف</div>
  </div>

  <div class="mc owned">
    <div class="mc-badge pro">🚀 Turbo — ممتلكة</div>
    <div class="mc-name">⚡ Turbo Miner</div>
    <div class="mc-hash">20 TH/s • $19.99</div>
    <div class="mc-row">
      <div class="mc-stat"><div class="mc-stat-l">الربح/يوم</div><div class="mc-stat-v" style="color:var(--green)">$10.00</div></div>
      <div class="mc-stat"><div class="mc-stat-l">السرعة</div><div class="mc-stat-v" id="spd-t">0%</div></div>
    </div>
    <div class="mc-prog"><div class="mc-bar" id="bar-t" style="width:0%"></div></div>
    <div class="mc-spd" id="stxt-t">⏸ متوقفة</div>
    <div class="cs-lbl">اختر عملة التعدين:</div>
    <div class="cs">
      <button class="cb" onclick="setCoin('t',this,'BTC')">₿ BTC</button>
      <button class="cb" onclick="setCoin('t',this,'ETH')">Ξ ETH</button>
      <button class="cb" onclick="setCoin('t',this,'SOL')">◎ SOL</button>
      <button class="cb active" onclick="setCoin('t',this,'USDT')">₮ USDT</button>
    </div>
    <button class="btn btn-gold btn-full" id="btn-t" onclick="toggleM('t')">▶ تشغيل التعدين</button>
    <div class="mst stop" id="mst-t">⏸ متوقف</div>
  </div>

  <div class="mc" style="border-color:rgba(245,197,24,.15)">
    <div class="mc-badge lk">🔒 للشراء</div><div class="mc-name">💎 Ultra Miner</div><div class="mc-hash">100 TH/s</div>
    <div class="mc-row"><div class="mc-stat"><div class="mc-stat-l">الربح/يوم</div><div class="mc-stat-v" style="color:var(--gold)">$50</div></div><div class="mc-stat"><div class="mc-stat-l">الربح/شهر</div><div class="mc-stat-v">$1,500</div></div></div>
    <button class="btn btn-gold btn-full" onclick="toast('💳 جاري فتح بوابة الدفع...')">شراء — $49.99</button>
  </div>

  <div class="mc" style="border-color:rgba(155,109,255,.2)">
    <div class="mc-badge vip">👑 الأقوى</div><div class="mc-name">🔥 God Miner</div><div class="mc-hash">2000 TH/s</div>
    <div class="mc-row"><div class="mc-stat"><div class="mc-stat-l">الربح/يوم</div><div class="mc-stat-v" style="color:var(--purple)">$1,000</div></div><div class="mc-stat"><div class="mc-stat-l">الربح/شهر</div><div class="mc-stat-v">$30,000</div></div></div>
    <button class="btn btn-full" style="background:var(--purple);color:#fff;font-family:Cairo,sans-serif;font-size:13px;font-weight:700;cursor:pointer;border:none;border-radius:9px;height:38px" onclick="toast('💳 جاري فتح بوابة الدفع...')">شراء — $999.99</button>
  </div>
</div>

<!-- ████ WALLET ████ -->
<div class="page" id="page-wallet">
  <div class="wallet-hero">
    <div class="wh-label">إجمالي رصيدك</div>
    <div class="wh-total">$847.32 <span>USD</span></div>
    <div class="wh-min">✓ أدنى سحب: $0.001 فقط</div>
    <div class="wh-actions">
      <button class="wh-btn w" onclick="openM('withdrawModal')">📤 سحب</button>
      <button class="wh-btn d" onclick="openM('depositModal')">📥 إيداع</button>
      <button class="wh-btn s" onclick="go('swap')">🔄 تبديل</button>
    </div>
  </div>
  <div class="card">
    <div class="card-head"><div class="card-title">💱 عملاتك</div></div>
    <div class="coin-grid">
      <div class="coin-card"><div class="coin-sym">₿</div><div class="coin-name">Bitcoin</div><div class="coin-bal">0.00821 BTC</div><div class="coin-usd">$489.20</div></div>
      <div class="coin-card"><div class="coin-sym">Ξ</div><div class="coin-name">Ethereum</div><div class="coin-bal">0.0943 ETH</div><div class="coin-usd">$218.40</div></div>
      <div class="coin-card"><div class="coin-sym">₮</div><div class="coin-name">USDT</div><div class="coin-bal">120.50 USDT</div><div class="coin-usd">$120.50</div></div>
      <div class="coin-card"><div class="coin-sym">◎</div><div class="coin-name">Solana</div><div class="coin-bal">0.21 SOL</div><div class="coin-usd">$19.22</div></div>
    </div>
  </div>
  <div class="card">
    <div class="card-head"><div class="card-title">🔗 ربط محفظة</div><button class="btn btn-gold btn-sm" onclick="openM('linkWalletModal')">+ ربط</button></div>
    <div class="w-link-grid">
      <a class="w-link" href="https://metamask.io" target="_blank"><div class="w-link-icon">🦊</div><div><div class="w-link-name">MetaMask</div><div class="w-link-chain">ETH</div></div></a>
      <a class="w-link" href="https://trustwallet.com" target="_blank"><div class="w-link-icon">🔶</div><div><div class="w-link-name">Trust Wallet</div><div class="w-link-chain">Multi</div></div></a>
      <a class="w-link" href="https://www.binance.com/en/wallet-direct" target="_blank"><div class="w-link-icon">🟠</div><div><div class="w-link-name">Binance</div><div class="w-link-chain">BSC</div></div></a>
      <a class="w-link" href="https://phantom.app" target="_blank"><div class="w-link-icon">👻</div><div><div class="w-link-name">Phantom</div><div class="w-link-chain">SOL</div></div></a>
      <a class="w-link" href="https://www.coinbase.com/wallet" target="_blank"><div class="w-link-icon">🔵</div><div><div class="w-link-name">Coinbase</div><div class="w-link-chain">ETH</div></div></a>
      <a class="w-link" href="https://ton.org/wallets" target="_blank"><div class="w-link-icon">💎</div><div><div class="w-link-name">TON Wallet</div><div class="w-link-chain">TON</div></div></a>
    </div>
  </div>
</div>

<!-- ████ EARN ████ -->
<div class="page" id="page-earn">
  <div class="earn-tabs">
    <div class="earn-tab active" onclick="earnTab(this,'ads')">📺 إعلانات</div>
    <div class="earn-tab" onclick="earnTab(this,'video')">🎬 فيديو</div>
    <div class="earn-tab" onclick="earnTab(this,'click')">🖱️ نقر</div>
  </div>
  <div id="earn-ads">
    <div class="card">

      <!-- ═══════════════════════════════════════════
           ✅ إعلان Google AdSense — مستطيل أعلى
           📌 استبدل data-ad-client و data-ad-slot
           من لوحة AdSense الخاصة بك
           ═══════════════════════════════════════════ -->
      <div style="margin-bottom:12px;text-align:center;background:var(--card2);border-radius:10px;padding:8px;border:1px dashed var(--border2);">
        <div style="font-size:10px;color:var(--muted);margin-bottom:6px">— إعلان —</div>
        <ins class="adsbygoogle"
             style="display:block;min-height:60px"
             data-ad-client="ca-pub-XXXXXXXXXXXXXXXX"
             data-ad-slot="1234567890"
             data-ad-format="auto"
             data-full-width-responsive="true"></ins>
        <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
        <!-- إعلان احتياطي يظهر حتى تفعيل AdSense -->
        <div class="adsense-placeholder" style="background:linear-gradient(135deg,#1a1f35,#0f1420);border-radius:8px;padding:14px;text-align:center">
          <div style="font-size:20px;margin-bottom:4px">📢</div>
          <div style="font-size:12px;font-weight:700;color:var(--gold)">مساحة إعلانية</div>
          <div style="font-size:10px;color:var(--muted)">سيظهر إعلان حقيقي بعد تفعيل AdSense</div>
        </div>
      </div>

      <div style="font-size:11px;color:var(--muted);margin-bottom:12px;padding:8px 10px;background:var(--card2);border-radius:8px">📢 للإعلان: <a href="mailto:ads@agi-network.io" style="color:var(--gold)">ads@agi-network.io</a></div>
      <div class="ad-card"><div class="ad-thumb">🛒</div><div class="ad-info"><div class="ad-title">Crypto Store</div><div class="ad-desc">اشترِ وبِع بأفضل الأسعار</div><div class="ad-rew">+$0.03/زيارة</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">زيارة</button></div>
      <div class="ad-card"><div class="ad-thumb">💡</div><div class="ad-info"><div class="ad-title">دورة Blockchain</div><div class="ad-desc">تعلم البلوكشين</div><div class="ad-rew">+$0.05/تسجيل</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">سجل</button></div>
      <div class="ad-card"><div class="ad-thumb">📱</div><div class="ad-info"><div class="ad-title">تطبيق DeFi</div><div class="ad-desc">حمّل واحصل على مكافأة</div><div class="ad-rew">+$0.10/تنزيل</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">حمّل</button></div>
      <div class="ad-card"><div class="ad-thumb">🏦</div><div class="ad-info"><div class="ad-title">حساب تداول</div><div class="ad-desc">افتح حساباً مجاناً</div><div class="ad-rew">+$0.25/حساب</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">ابدأ</button></div>
    </div>
  </div>
  <div id="earn-video" style="display:none">
    <div class="card">
      <div class="ad-card"><div class="ad-thumb">🎬</div><div class="ad-info"><div class="ad-title">فيديو إعلاني 30 ثانية</div><div class="ad-rew">+$0.05</div></div><button class="btn btn-gold btn-sm" onclick="watchVideo()">▶ شاهد</button></div>
      <div class="ad-card"><div class="ad-thumb">📊</div><div class="ad-info"><div class="ad-title">مراجعة تداول 60 ثانية</div><div class="ad-rew">+$0.08</div></div><button class="btn btn-gold btn-sm" onclick="watchVideo()">▶ شاهد</button></div>
      <div class="ad-card"><div class="ad-thumb">🌐</div><div class="ad-info"><div class="ad-title">إعلان Web3 — 120 ثانية</div><div class="ad-rew">+$0.15</div></div><button class="btn btn-gold btn-sm" onclick="watchVideo()">▶ شاهد</button></div>
    </div>
  </div>
  <div id="earn-click" style="display:none">
    <div class="card">
      <div class="ad-card"><div class="ad-thumb">🖱️</div><div class="ad-info"><div class="ad-title">CryptoNews — 10 ثوانٍ</div><div class="ad-rew">+$0.02</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">انقر</button></div>
      <div class="ad-card"><div class="ad-thumb">📰</div><div class="ad-info"><div class="ad-title">BlockDaily — 10 ثوانٍ</div><div class="ad-rew">+$0.02</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">انقر</button></div>
      <div class="ad-card"><div class="ad-thumb">🔐</div><div class="ad-info"><div class="ad-title">NFT Marketplace — 10 ثوانٍ</div><div class="ad-rew">+$0.03</div></div><button class="btn btn-gold btn-sm" onclick="visitSite()">انقر</button></div>
    </div>
  </div>
</div>

<!-- ████ REFERRAL ████ -->
<div class="page" id="page-referral">
  <div class="ref-hero">
    <div style="font-size:14px;font-weight:800">🎁 رابط الإحالة الخاص بك</div>
    <div style="font-size:12px;color:var(--muted);margin-top:4px">احصل على <strong style="color:var(--gold)">10%</strong> من أرباح كل صديق للأبد!</div>
    <div class="ref-code-row"><div class="ref-code">AGI-A7X92K</div><button class="copy-btn" onclick="copyRef()">📋 نسخ</button></div>
    <div style="background:rgba(0,0,0,.3);border-radius:7px;padding:8px 10px;font-size:11px;color:var(--muted)">https://agi-network.io/ref/AGI-A7X92K</div>
  </div>
  <div class="ref-stats">
    <div class="ref-stat"><div class="ref-val">23</div><div class="ref-lbl">مدعوون</div></div>
    <div class="ref-stat"><div class="ref-val">$47.80</div><div class="ref-lbl">أرباح</div></div>
    <div class="ref-stat"><div class="ref-val">$2.10</div><div class="ref-lbl">هذا الأسبوع</div></div>
  </div>
  <div class="card">
    <div class="card-head"><div class="card-title">👥 الأصدقاء</div></div>
    <div class="friend-row"><div class="friend-av">👤</div><div class="friend-name">أحمد محمد</div><div style="font-size:10px;color:var(--muted)">5 أيام</div><div class="friend-earn">+$12.30</div></div>
    <div class="friend-row"><div class="friend-av">👤</div><div class="friend-name">فاطمة علي</div><div style="font-size:10px;color:var(--muted)">12 يوم</div><div class="friend-earn">+$8.50</div></div>
    <div class="friend-row"><div class="friend-av">👤</div><div class="friend-name">خالد عمر</div><div style="font-size:10px;color:var(--muted)">20 يوم</div><div class="friend-earn">+$21.00</div></div>
  </div>
</div>

<!-- ████ SWAP ████ -->
<div class="page" id="page-swap">
  <div class="card" style="max-width:100%">
    <div class="card-head"><div class="card-title">🔄 تبديل العملات</div><span style="font-size:11px;color:var(--muted)">رسوم 0.5%</span></div>
    <div class="swap-box">
      <div class="swap-lbl">من</div>
      <div class="swap-row">
        <input class="swap-input" type="number" value="1" id="swapFrom" oninput="calcSwap()">
        <select class="swap-sel" id="coinFrom" onchange="calcSwap()">
          <option value="usdt">₮ USDT</option><option value="btc">₿ BTC</option><option value="eth">Ξ ETH</option><option value="sol">◎ SOL</option>
        </select>
      </div>
    </div>
    <div class="swap-mid" onclick="swapCoins()">⇅</div>
    <div class="swap-box">
      <div class="swap-lbl">إلى</div>
      <div class="swap-row">
        <input class="swap-input" type="number" id="swapTo" readonly style="color:var(--gold)">
        <select class="swap-sel" id="coinTo" onchange="calcSwap()">
          <option value="btc">₿ BTC</option><option value="eth">Ξ ETH</option><option value="usdt">₮ USDT</option><option value="sol">◎ SOL</option>
        </select>
      </div>
    </div>
    <div class="swap-rate-txt" id="swapRate">1 USDT = 0.0000168 BTC</div>
    <button class="btn btn-gold btn-full" onclick="doSwap()">🔄 تبديل الآن</button>
  </div>
</div>

<!-- ████ MORE (Games / Admin) ████ -->
<div class="page" id="page-games">
  <div style="margin-bottom:12px;text-align:center;background:var(--card2);border-radius:10px;padding:8px;border:1px dashed var(--border2);">
    <div style="font-size:10px;color:var(--muted);margin-bottom:5px">— إعلان Google AdSense —</div>
    <ins class="adsbygoogle" style="display:block;min-height:50px" data-ad-client="ca-pub-XXXXXXXXXXXXXXXX" data-ad-slot="9876543210" data-ad-format="auto" data-full-width-responsive="true"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
    <div style="background:linear-gradient(135deg,#1a1f35,#0f1420);border-radius:8px;padding:10px;font-size:10px;color:var(--muted)">مساحة إعلانية — تُفعَّل بعد ربط AdSense</div>
  </div>
  <div style="font-size:12px;font-weight:700;color:var(--muted);margin-bottom:10px">🎮 ألعاب كريبتو حقيقية — أرباح فعلية</div>
  <a href="https://rollercoin.com" target="_blank" style="text-decoration:none">
    <div class="card" style="display:flex;align-items:center;gap:12px;border-color:rgba(245,197,24,.25);margin-bottom:10px">
      <div style="width:48px;height:48px;border-radius:12px;background:linear-gradient(135deg,#1a0a2e,#2d1060);display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0">🎮</div>
      <div style="flex:1"><div style="font-size:13px;font-weight:800;color:var(--gold)">RollerCoin</div><div style="font-size:11px;color:var(--muted);margin-top:2px">العب ألعاباً واكسب BTC و ETH و DOGE</div><div style="font-size:11px;color:var(--green);margin-top:3px;font-weight:700">✅ مجاني — أرباح حقيقية</div></div>
      <div style="font-size:16px;color:var(--muted)">←</div>
    </div>
  </a>
  <a href="https://cointiply.com" target="_blank" style="text-decoration:none">
    <div class="card" style="display:flex;align-items:center;gap:12px;border-color:rgba(245,197,24,.25);margin-bottom:10px">
      <div style="width:48px;height:48px;border-radius:12px;background:linear-gradient(135deg,#0a1a0a,#103d10);display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0">🪙</div>
      <div style="flex:1"><div style="font-size:13px;font-weight:800;color:var(--gold)">Cointiply</div><div style="font-size:11px;color:var(--muted);margin-top:2px">ألعاب + استطلاعات + مشاهدة إعلانات</div><div style="font-size:11px;color:var(--green);margin-top:3px;font-weight:700">✅ يدفع Bitcoin حقيقي</div></div>
      <div style="font-size:16px;color:var(--muted)">←</div>
    </div>
  </a>
  <a href="https://freebitco.in" target="_blank" style="text-decoration:none">
    <div class="card" style="display:flex;align-items:center;gap:12px;border-color:rgba(245,197,24,.25);margin-bottom:10px">
      <div style="width:48px;height:48px;border-radius:12px;background:linear-gradient(135deg,#1a0f00,#3d2800);display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0">₿</div>
      <div style="flex:1"><div style="font-size:13px;font-weight:800;color:var(--gold)">FreeBitcoin</div><div style="font-size:11px;color:var(--muted);margin-top:2px">عجلة BTC مجانية كل ساعة + Hi-Lo</div><div style="font-size:11px;color:var(--green);margin-top:3px;font-weight:700">✅ يعمل منذ 2013</div></div>
      <div style="font-size:16px;color:var(--muted)">←</div>
    </div>
  </a>
  <a href="https://womplay.io" target="_blank" style="text-decoration:none">
    <div class="card" style="display:flex;align-items:center;gap:12px;border-color:rgba(0,214,143,.2);margin-bottom:10px">
      <div style="width:48px;height:48px;border-radius:12px;background:linear-gradient(135deg,#001a14,#003d2a);display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0">🏆</div>
      <div style="flex:1"><div style="font-size:13px;font-weight:800;color:var(--green)">Womplay</div><div style="font-size:11px;color:var(--muted);margin-top:2px">العب أي لعبة واكسب EOS و BTC</div><div style="font-size:11px;color:var(--green);margin-top:3px;font-weight:700">✅ مجاني 100%</div></div>
      <div style="font-size:16px;color:var(--muted)">←</div>
    </div>
  </a>
  <a href="https://splinterlands.com" target="_blank" style="text-decoration:none">
    <div class="card" style="display:flex;align-items:center;gap:12px;border-color:rgba(75,143,255,.2);margin-bottom:10px">
      <div style="width:48px;height:48px;border-radius:12px;background:linear-gradient(135deg,#0a0f1a,#102040);display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0">⚔️</div>
      <div style="flex:1"><div style="font-size:13px;font-weight:800;color:var(--blue)">Splinterlands</div><div style="font-size:11px;color:var(--muted);margin-top:2px">بطاقات NFT — اكسب DEC و SPS</div><div style="font-size:11px;color:var(--blue);margin-top:3px;font-weight:700">✅ P2E الأكثر شعبية</div></div>
      <div style="font-size:16px;color:var(--muted)">←</div>
    </div>
  </a>
  <a href="https://stake.com" target="_blank" style="text-decoration:none">
    <div class="card" style="display:flex;align-items:center;gap:12px;border-color:rgba(155,109,255,.2);margin-bottom:10px">
      <div style="width:48px;height:48px;border-radius:12px;background:linear-gradient(135deg,#0f001a,#200040);display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0">🎰</div>
      <div style="flex:1"><div style="font-size:13px;font-weight:800;color:var(--purple)">Stake.com</div><div style="font-size:11px;color:var(--muted);margin-top:2px">Crash, Dice, Plinko بالعملات الرقمية</div><div style="font-size:11px;color:var(--purple);margin-top:3px;font-weight:700">🔞 للبالغين +18 فقط</div></div>
      <div style="font-size:16px;color:var(--muted)">←</div>
    </div>
  </a>
</div>

<!-- ████ ADMIN ████ -->
<div class="page" id="page-admin">
  <div id="adminLogin">
    <div class="admin-lock">
      <div style="font-size:56px">🔐</div>
      <div style="font-size:20px;font-weight:800;color:var(--gold)">لوحة الإدارة</div>
      <div style="font-size:12px;color:var(--muted)">للمالك فقط</div>
      <input class="adm-input" id="adminUser" type="text" placeholder="اسم المستخدم">
      <input class="adm-input" id="adminPass" type="password" placeholder="كلمة المرور" onkeydown="if(event.key==='Enter')doLogin()">
      <button class="btn btn-gold" style="padding:0 36px;height:42px;font-size:15px" onclick="doLogin()">دخول →</button>
      <div id="loginErr" style="color:var(--red);font-size:12px;display:none">❌ بيانات خاطئة</div>
    </div>
  </div>
  <div id="adminPanel" style="display:none">
    <div class="adm-wallet">
      <div style="font-size:11px;color:var(--muted);font-weight:600;margin-bottom:2px">👑 محفظة المالك — eidmo11</div>
      <div class="adm-bal">$12,847.50</div>
      <div style="font-size:11px;color:var(--muted);margin-top:4px">أرباح الإعلانات + مبيعات الماكينات</div>
      <div style="display:flex;gap:8px;margin-top:12px">
        <button class="btn btn-gold" style="flex:1;font-size:12px" onclick="openM('ownerWithdraw')">📤 سحب المالك</button>
        <button class="btn btn-out" style="flex:1;font-size:12px" onclick="openM('addFunds')">+ تمويل</button>
        <button class="btn btn-out" style="font-size:12px;color:var(--red);border-color:var(--red)" onclick="doLogout()">خروج</button>
      </div>
    </div>
    <div class="adm-grid">
      <div class="adm-stat"><div class="adm-stat-v">1,247</div><div class="adm-stat-l">المستخدمون</div></div>
      <div class="adm-stat"><div class="adm-stat-v">843</div><div class="adm-stat-l">المعدنون</div></div>
      <div class="adm-stat"><div class="adm-stat-v">$71,330</div><div class="adm-stat-l">الإيرادات</div></div>
      <div class="adm-stat"><div class="adm-stat-v">$5,940</div><div class="adm-stat-l">صافي الربح</div></div>
    </div>
    <div class="adm-actions">
      <div class="adm-act" onclick="toast('👥 إدارة المستخدمين')"><div class="adm-act-icon">👥</div><div class="adm-act-lbl">المستخدمون</div></div>
      <div class="adm-act" onclick="toast('📢 إدارة الإعلانات')"><div class="adm-act-icon">📢</div><div class="adm-act-lbl">الإعلانات</div></div>
      <div class="adm-act" onclick="toast('⛏️ إدارة الماكينات')"><div class="adm-act-icon">⛏️</div><div class="adm-act-lbl">الماكينات</div></div>
      <div class="adm-act" onclick="toast('💳 إدارة المدفوعات')"><div class="adm-act-icon">💳</div><div class="adm-act-lbl">المدفوعات</div></div>
      <div class="adm-act" onclick="toast('🎮 إدارة الألعاب')"><div class="adm-act-icon">🎮</div><div class="adm-act-lbl">الألعاب</div></div>
      <div class="adm-act" onclick="toast('📊 التقارير')"><div class="adm-act-icon">📊</div><div class="adm-act-lbl">التقارير</div></div>
      <div class="adm-act" onclick="toast('⚙️ الإعدادات')"><div class="adm-act-icon">⚙️</div><div class="adm-act-lbl">الإعدادات</div></div>
      <div class="adm-act" onclick="toast('💰 الإيرادات')"><div class="adm-act-icon">💰</div><div class="adm-act-lbl">الإيرادات</div></div>
    </div>
    <div class="card">
      <div class="card-head"><div class="card-title">📋 طلبات السحب</div></div>
      <div style="overflow-x:auto"><table class="tbl">
        <thead><tr><th>المستخدم</th><th>المبلغ</th><th>الحالة</th><th>إجراء</th></tr></thead>
        <tbody>
          <tr><td>أحمد م.</td><td>$0.001</td><td><span class="bdg bg-b">معلق</span></td><td><button class="btn btn-gold btn-sm" onclick="toast('✅ تمت الموافقة')">موافقة</button></td></tr>
          <tr><td>فاطمة ع.</td><td>$0.05</td><td><span class="bdg bg-b">معلق</span></td><td><button class="btn btn-gold btn-sm" onclick="toast('✅ تمت الموافقة')">موافقة</button></td></tr>
          <tr><td>خالد ع.</td><td>$120.00</td><td><span class="bdg bg-b">معلق</span></td><td><button class="btn btn-gold btn-sm" onclick="toast('✅ تمت الموافقة')">موافقة</button></td></tr>
        </tbody>
      </table></div>
    </div>
  </div>
</div>

</div><!-- /content -->

<!-- BOTTOM NAV -->
<nav class="bottom-nav">
  <div class="bn-item active" onclick="go('dashboard')"><div class="bn-icon">⚡</div><div class="bn-label">الرئيسية</div></div>
  <div class="bn-item" onclick="go('mining')"><div class="bn-icon">⛏️</div><div class="bn-label">التعدين</div></div>
  <div class="bn-item" onclick="go('wallet')"><div class="bn-icon">💼</div><div class="bn-label">المحفظة</div></div>
  <div class="bn-item" onclick="go('earn')"><div class="bn-icon">💰</div><div class="bn-label">اكسب</div><div class="bn-badge">NEW</div></div>
  <div class="bn-item" onclick="toggleMore()"><div class="bn-icon">☰</div><div class="bn-label">المزيد</div></div>
</nav>

<!-- MORE OVERLAY -->
<div class="more-overlay" id="moreOverlay" onclick="closeMore()"></div>
<div class="more-sheet" id="moreSheet">
  <div class="more-title">القائمة الكاملة</div>
  <div class="more-grid">
    <div class="more-item" onclick="go('referral');closeMore()"><div class="more-item-icon">👥</div><div class="more-item-label">الإحالة</div></div>
    <div class="more-item" onclick="go('games');closeMore()"><div class="more-item-icon">🎮</div><div class="more-item-label">الألعاب</div></div>
    <div class="more-item" onclick="go('swap');closeMore()"><div class="more-item-icon">🔄</div><div class="more-item-label">التبديل</div></div>
    <div class="more-item" onclick="go('admin');closeMore()"><div class="more-item-icon">👑</div><div class="more-item-label">الإدارة</div></div>
  </div>
</div>

<!-- MODALS -->
<div class="modal-overlay" id="depositModal" onclick="if(event.target===this)closeM('depositModal')">
  <div class="modal">
    <div class="modal-title">📥 إيداع رصيد</div>
    <div class="inp-g"><div class="inp-l">العملة</div><select class="inp"><option>₿ Bitcoin (BTC)</option><option>Ξ Ethereum (ETH)</option><option>₮ USDT (TRC-20)</option><option>◎ Solana (SOL)</option></select></div>
    <div class="inp-g"><div class="inp-l">المبلغ (أدنى $0.50)</div><input class="inp" type="number" placeholder="0.50"></div>
    <div style="background:var(--input);border:1px dashed rgba(245,197,24,.3);border-radius:9px;padding:12px;margin-bottom:12px;text-align:center">
      <div style="font-size:10px;color:var(--muted);margin-bottom:5px">عنوان الإيداع</div>
      <div style="font-family:monospace;font-size:11px;color:var(--gold);word-break:break-all">0x742d35Cc6634C0532925a3b844Bc454e4438f44e</div>
    </div>
    <div class="modal-foot"><button class="btn btn-gold" style="flex:1" onclick="closeM('depositModal');toast('✅ تم إرسال طلب الإيداع')">تأكيد</button><button class="btn btn-out" style="flex:1" onclick="closeM('depositModal')">إلغاء</button></div>
  </div>
</div>

<div class="modal-overlay" id="withdrawModal" onclick="if(event.target===this)closeM('withdrawModal')">
  <div class="modal">
    <div class="modal-title">📤 سحب رصيد</div>
    <div style="background:rgba(0,214,143,.07);border:1px solid rgba(0,214,143,.2);border-radius:8px;padding:9px 12px;margin-bottom:12px;font-size:12px;color:var(--green);font-weight:700">✓ الحد الأدنى: $0.001 فقط</div>
    <div class="inp-g"><div class="inp-l">عنوان محفظتك</div><input class="inp" type="text" placeholder="0x... أو TRX..."></div>
    <div class="inp-g"><div class="inp-l">العملة</div><select class="inp"><option>₮ USDT</option><option>₿ Bitcoin</option><option>Ξ Ethereum</option><option>◎ Solana</option></select></div>
    <div class="inp-g"><div class="inp-l">المبلغ</div><input class="inp" type="number" placeholder="0.001"></div>
    <div class="modal-foot"><button class="btn btn-gold" style="flex:1" onclick="closeM('withdrawModal');toast('✅ طلب السحب قيد المعالجة')">تأكيد</button><button class="btn btn-out" style="flex:1" onclick="closeM('withdrawModal')">إلغاء</button></div>
  </div>
</div>

<div class="modal-overlay" id="linkWalletModal" onclick="if(event.target===this)closeM('linkWalletModal')">
  <div class="modal">
    <div class="modal-title">🔗 ربط محفظة خارجية</div>
    <div class="w-link-grid">
      <a class="w-link" href="https://metamask.io" target="_blank"><div class="w-link-icon">🦊</div><div><div class="w-link-name">MetaMask</div><div class="w-link-chain">ETH</div></div></a>
      <a class="w-link" href="https://trustwallet.com" target="_blank"><div class="w-link-icon">🔶</div><div><div class="w-link-name">Trust Wallet</div><div class="w-link-chain">Multi</div></div></a>
      <a class="w-link" href="https://www.binance.com/en/wallet-direct" target="_blank"><div class="w-link-icon">🟠</div><div><div class="w-link-name">Binance</div><div class="w-link-chain">BSC</div></div></a>
      <a class="w-link" href="https://phantom.app" target="_blank"><div class="w-link-icon">👻</div><div><div class="w-link-name">Phantom</div><div class="w-link-chain">SOL</div></div></a>
      <a class="w-link" href="https://www.coinbase.com/wallet" target="_blank"><div class="w-link-icon">🔵</div><div><div class="w-link-name">Coinbase</div><div class="w-link-chain">ETH</div></div></a>
      <a class="w-link" href="https://ton.org/wallets" target="_blank"><div class="w-link-icon">💎</div><div><div class="w-link-name">TON</div><div class="w-link-chain">TON</div></div></a>
    </div>
    <div style="font-size:11px;color:var(--muted);text-align:center">اضغط للانتقال المباشر للمحفظة</div>
  </div>
</div>

<div class="modal-overlay" id="ownerWithdraw" onclick="if(event.target===this)closeM('ownerWithdraw')">
  <div class="modal">
    <div class="modal-title">👑 سحب المالك</div>
    <div style="background:rgba(245,197,24,.07);border:1px solid rgba(245,197,24,.2);border-radius:8px;padding:9px 12px;margin-bottom:12px;font-size:12px;color:var(--gold);font-weight:700">رصيد المالك: $12,847.50</div>
    <div class="inp-g"><div class="inp-l">عنوان محفظتك</div><input class="inp" type="text" placeholder="أدخل عنوان محفظتك"></div>
    <div class="inp-g"><div class="inp-l">العملة</div><select class="inp"><option>₮ USDT</option><option>₿ Bitcoin</option><option>Ξ Ethereum</option></select></div>
    <div class="inp-g"><div class="inp-l">المبلغ</div><input class="inp" type="number" placeholder="0.00"></div>
    <div class="modal-foot"><button class="btn btn-gold" style="flex:1" onclick="closeM('ownerWithdraw');toast('✅ تم سحب أرباح المالك!')">تأكيد</button><button class="btn btn-out" style="flex:1" onclick="closeM('ownerWithdraw')">إلغاء</button></div>
  </div>
</div>

<div class="modal-overlay" id="addFunds" onclick="if(event.target===this)closeM('addFunds')">
  <div class="modal">
    <div class="modal-title">💰 تمويل الموقع</div>
    <div class="inp-g"><div class="inp-l">مبلغ التمويل</div><input class="inp" type="number" placeholder="0.00"></div>
    <div class="inp-g"><div class="inp-l">الغرض</div><select class="inp"><option>صندوق السحوبات</option><option>تمويل الإعلانات</option><option>مكافآت المعدنين</option></select></div>
    <div class="modal-foot"><button class="btn btn-gold" style="flex:1" onclick="closeM('addFunds');toast('✅ تم إضافة التمويل')">تأكيد</button><button class="btn btn-out" style="flex:1" onclick="closeM('addFunds')">إلغاء</button></div>
  </div>
</div>

<!-- VIDEO -->
<div class="video-overlay" id="videoOverlay">
  <div class="video-screen">📺</div>
  <div class="video-timer" id="vidTimer">30</div>
  <div style="font-size:13px;color:var(--muted)">شاهد للحصول على مكافأتك</div>
  <button class="skip-btn" id="skipBtn" onclick="closeVideo()">✓ احصل على $0.05</button>
</div>

<div class="toast" id="toastEl"></div>

<script>
// STATE
const M={s:{on:false,coin:'BTC',rate:0.0000058,earn:0,tgt:78},p:{on:false,coin:'ETH',rate:0.000029,earn:0,tgt:95},t:{on:false,coin:'USDT',rate:0.000116,earn:0,tgt:100}};
let totalBal=847.32;

// NAV
const titles={dashboard:'لوحة التحكم',mining:'ماكينات التعدين',wallet:'المحفظة',earn:'اكسب المزيد',referral:'دعوة الأصدقاء',swap:'تبديل العملات',games:'الألعاب',admin:'لوحة الإدارة'};
function go(id){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById('page-'+id).classList.add('active');
  document.getElementById('pageBar').textContent='AGI Network / '+(titles[id]||'');
  document.querySelectorAll('.bn-item').forEach(n=>n.classList.remove('active'));
  const map={dashboard:0,mining:1,wallet:2,earn:3};
  if(map[id]!==undefined)document.querySelectorAll('.bn-item')[map[id]].classList.add('active');
}

// MORE SHEET
function toggleMore(){
  document.getElementById('moreOverlay').classList.toggle('open');
  document.getElementById('moreSheet').classList.toggle('open');
}
function closeMore(){
  document.getElementById('moreOverlay').classList.remove('open');
  document.getElementById('moreSheet').classList.remove('open');
}

// MACHINE TOGGLE
function toggleM(id){
  const m=M[id];m.on=!m.on;
  const btn=document.getElementById('btn-'+id),st=document.getElementById('mst-'+id),bar=document.getElementById('bar-'+id),spd=document.getElementById('spd-'+id),stxt=document.getElementById('stxt-'+id);
  if(m.on){
    btn.textContent='⏹ إيقاف';btn.style.background='var(--red)';btn.style.color='#fff';
    st.className='mst run';st.innerHTML='<div class="pulse"></div> يعدن — '+m.coin;
    let s=0;const iv=setInterval(()=>{s=Math.min(s+4,m.tgt);bar.style.width=s+'%';spd.textContent=s+'%';stxt.textContent='⚡ '+s+'%';if(s>=m.tgt)clearInterval(iv);},40);
    toast('✅ بدأ التعدين — '+m.coin);
  } else {
    btn.textContent='▶ تشغيل التعدين';btn.style.background='';btn.style.color='';
    st.className='mst stop';st.innerHTML='⏸ متوقف';
    let s=m.tgt;const iv=setInterval(()=>{s=Math.max(s-5,0);bar.style.width=s+'%';spd.textContent=s+'%';stxt.textContent='⏸ متوقفة';if(s<=0)clearInterval(iv);},40);
    toast('⏹ تم الإيقاف');
  }
  const n=Object.values(M).filter(x=>x.on).length;const el=document.getElementById('d-active');if(el)el.textContent=n;
}

// COIN
function setCoin(id,btn,coin){
  btn.closest('.cs').querySelectorAll('.cb').forEach(b=>b.classList.remove('active'));btn.classList.add('active');
  M[id].coin=coin;
  const r={BTC:0.0000058,ETH:0.000029,SOL:0.00055,USDT:0.00058,LTC:0.000145};M[id].rate=r[coin]||0.0000058;
  if(M[id].on){document.getElementById('mst-'+id).innerHTML='<div class="pulse"></div> يعدن — '+coin;}
  const i={s:0,p:1,t:2}[id];const el=document.getElementById('dc'+i);if(el)el.textContent=coin;
  toast('✅ '+coin+' للتعدين');
}

// LIVE
setInterval(()=>{
  ['s','p','t'].forEach((id,i)=>{if(M[id].on){M[id].earn+=M[id].rate;totalBal+=M[id].rate;}const el=document.getElementById('le'+i);if(el)el.textContent='$'+M[id].earn.toFixed(6);});
  const db=document.getElementById('d-balance');if(db)db.innerHTML='$'+totalBal.toFixed(2)+' <span>USD</span>';
  const dm=document.getElementById('d-mining');const tot=M.s.earn+M.p.earn+M.t.earn;if(dm)dm.textContent='$'+tot.toFixed(6);
},1000);

// ADMIN
function doLogin(){
  const u=document.getElementById('adminUser').value.trim(),p=document.getElementById('adminPass').value;
  if(u==='eidmo11'&&btoa(p)===btoa('Mno112233')){
    document.getElementById('adminLogin').style.display='none';document.getElementById('adminPanel').style.display='block';
    document.getElementById('loginErr').style.display='none';toast('👑 مرحباً بالمدير!');
  } else {document.getElementById('loginErr').style.display='block';}
}
function doLogout(){document.getElementById('adminLogin').style.display='block';document.getElementById('adminPanel').style.display='none';document.getElementById('adminUser').value='';document.getElementById('adminPass').value='';go('dashboard');toast('تم الخروج');}

// EARN TABS
function earnTab(tab,type){
  document.querySelectorAll('.earn-tab').forEach(t=>t.classList.remove('active'));tab.classList.add('active');
  ['ads','video','click'].forEach(t=>{const e=document.getElementById('earn-'+t);if(e)e.style.display=t===type?'block':'none';});
}

// MODAL
function openM(id){document.getElementById(id).classList.add('open');}
function closeM(id){document.getElementById(id).classList.remove('open');}

// VIDEO
let vt;
function watchVideo(){
  document.getElementById('videoOverlay').classList.add('open');let t=30;
  document.getElementById('vidTimer').textContent=t;const sk=document.getElementById('skipBtn');
  sk.classList.remove('ready');sk.style.pointerEvents='none';
  vt=setInterval(()=>{t--;document.getElementById('vidTimer').textContent=t;if(t<=0){clearInterval(vt);document.getElementById('vidTimer').textContent='✓';sk.classList.add('ready');sk.style.pointerEvents='all';}},1000);
}
function closeVideo(){clearInterval(vt);document.getElementById('videoOverlay').classList.remove('open');toast('🎉 تم إضافة $0.05!');}

// MISC
function visitSite(){toast('🔗 جاري فتح الموقع...');setTimeout(()=>toast('💰 تم إضافة المكافأة!'),2500);}
function copyRef(){navigator.clipboard&&navigator.clipboard.writeText('https://agi-network.io/ref/AGI-A7X92K');toast('📋 تم نسخ رابط الإحالة!');}
let toastTm;
function toast(msg){const e=document.getElementById('toastEl');e.textContent=msg;e.classList.add('show');clearTimeout(toastTm);toastTm=setTimeout(()=>e.classList.remove('show'),3000);}

// SWAP
const sr={btc:59500,eth:2310,usdt:1,sol:91.2};
function calcSwap(){const f=document.getElementById('coinFrom').value,t=document.getElementById('coinTo').value,a=parseFloat(document.getElementById('swapFrom').value)||0;document.getElementById('swapTo').value=((a*sr[f])/sr[t]*0.995).toFixed(6);document.getElementById('swapRate').textContent='1 '+f.toUpperCase()+' = '+(sr[f]/sr[t]).toFixed(6)+' '+t.toUpperCase();}
function swapCoins(){const cf=document.getElementById('coinFrom'),ct=document.getElementById('coinTo');const tmp=cf.value;cf.value=ct.value;ct.value=tmp;calcSwap();}
function doSwap(){toast('✅ تم التبديل بنجاح!');}
calcSwap();
</script>
</body>
</html>
