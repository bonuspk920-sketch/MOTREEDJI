<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>DJI Drone Simulator 3D - มนตรี</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<link href="https://fonts.googleapis.com/css2?family=Prompt:wght@400;600;800&display=swap" rel="stylesheet">
<style>
:root{
  --glass:rgba(12,18,32,.78); --glass2:rgba(20,28,46,.92); --line:rgba(255,255,255,.16);
  --cyan:#22d3ee; --orange:#f97316; --lime:#a3e635; --pink:#f472b6; --gold:#facc15;
  --text:#f1f5f9; --muted:#94a3b8;
}
*{box-sizing:border-box;margin:0;padding:0;user-select:none;-webkit-user-select:none;-webkit-tap-highlight-color:transparent;font-family:'Prompt',system-ui,sans-serif}
html,body{width:100%;height:100%;overflow:hidden;background:#05070d;color:var(--text)}
#cv{position:fixed;inset:0}
#cv canvas{display:block;width:100%;height:100%;touch-action:none}
.hidden{display:none!important}
button{border:0;color:inherit;cursor:pointer;font:inherit;touch-action:manipulation}
button:active{transform:scale(.95)}
.pill{background:var(--glass);border:1px solid var(--line);border-radius:999px;padding:6px 12px;font-size:13px;font-weight:600;backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px);white-space:nowrap}
.ic{width:40px;height:40px;border-radius:12px;background:var(--glass);border:1px solid var(--line);font-size:18px;display:flex;align-items:center;justify-content:center;position:relative;backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px)}
.ic.lg{width:46px;height:46px;font-size:20px}
.ic.on{background:rgba(34,211,238,.35);border-color:var(--cyan)}
.badge{position:absolute;top:-6px;right:-6px;background:var(--cyan);color:#021018;font-size:11px;font-weight:800;border-radius:999px;padding:0 6px}

/* ---------- HUD ---------- */
#hud,#hud2{position:fixed;inset:0;pointer-events:none;z-index:10}
#hud button,#hud2 button,#hud .pads{pointer-events:auto}
.topbar{position:absolute;top:0;left:0;right:0;display:flex;justify-content:space-between;align-items:flex-start;gap:8px;padding:10px 12px 26px;background:linear-gradient(rgba(0,0,0,.55),transparent)}
.tb-left,.tb-right{display:flex;gap:6px;align-items:center;flex-wrap:wrap}
.tb-right{justify-content:flex-end}
.tb-center{position:absolute;left:50%;top:10px;transform:translateX(-50%);display:flex;flex-direction:column;align-items:center;gap:4px}
.mode{color:var(--gold);font-weight:800;min-width:40px;height:32px}
.mission{color:#a5f3fc;max-width:46vw;overflow:hidden;text-overflow:ellipsis}
.timer{font-size:18px;font-weight:800;font-variant-numeric:tabular-nums;color:#fff}
.ptag{font-weight:800}
.rec{color:#fb7185;animation:blink 1s infinite}
@keyframes blink{50%{opacity:.4}}
.guide{position:absolute;top:92px;left:50%;transform:translateX(-50%);background:rgba(250,204,21,.92);color:#1c1402;font-weight:800;font-size:14px;padding:5px 14px;border-radius:999px;box-shadow:0 4px 14px rgba(0,0,0,.35)}
.rail{position:absolute;top:50%;transform:translateY(-50%);display:flex;flex-direction:column;gap:8px;align-items:center}
.rail.right{right:12px}.rail.left{left:12px}
.gim{font-size:11px;font-weight:700;color:var(--muted);background:var(--glass);padding:2px 6px;border-radius:6px}
.shutter{width:62px;height:62px;border-radius:50%;background:#fff;border:5px solid rgba(255,255,255,.35);background-clip:padding-box;box-shadow:0 0 0 2px rgba(0,0,0,.25)}
.shutter:active{background:#e2e8f0}
#b-video.rec-on{background:rgba(244,63,94,.5);border-color:#fb7185}
.tele{position:absolute;bottom:10px;left:50%;transform:translateX(-50%);display:flex;gap:4px;background:var(--glass);border:1px solid var(--line);border-radius:16px;padding:6px 10px;backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px)}
.tele div{display:flex;align-items:baseline;gap:4px;padding:0 8px;border-right:1px solid var(--line)}
.tele div:last-child{border-right:0}
.tele span{font-size:11px;font-weight:800;color:var(--muted)}
.tele b{font-size:18px;font-variant-numeric:tabular-nums;min-width:44px;text-align:right}
.tele i{font-style:normal;font-size:10px;color:var(--muted)}
#t-h{color:var(--gold)}#t-hs{color:#4ade80}#t-vs{color:#38bdf8}
.pads{position:absolute;left:0;right:0;bottom:62px;display:flex;justify-content:space-between;padding:0 12px}
.pad{display:grid;grid-template-columns:repeat(3,58px);grid-template-rows:repeat(3,52px);gap:5px}
.pad button{background:rgba(15,23,42,.72);border:1px solid rgba(34,211,238,.4);border-radius:14px;font-size:20px;font-weight:800;display:flex;flex-direction:column;align-items:center;justify-content:center;line-height:1;touch-action:none}
.pad button small{font-size:9px;font-weight:600;color:#a5f3fc;margin-top:2px}
.pad button.held{background:rgba(34,211,238,.55)}
.pad .u{grid-column:2;grid-row:1}.pad .l{grid-column:1;grid-row:2}.pad .r{grid-column:3;grid-row:2}.pad .d{grid-column:2;grid-row:3}

/* split screen */
.divider{position:absolute;top:0;bottom:0;left:50%;width:4px;margin-left:-2px;background:#05070d}
.sp{position:absolute;top:10px;background:var(--glass);border:2px solid var(--line);border-radius:16px;padding:8px 14px;min-width:170px}
.sp1{left:10px}.sp2{right:10px}
.sp h3{font-size:16px;font-weight:800}
.sp .row{font-size:13px;color:#cbd5e1}
.sp .big{font-size:20px;font-weight:800;color:#fff;text-shadow:0 1px 4px rgba(0,0,0,.6)}
.sp-timer{position:absolute;top:10px;left:50%;transform:translateX(-50%);font-size:20px;font-weight:800;font-variant-numeric:tabular-nums}
.sp-pause{position:absolute;top:56px;left:50%;transform:translateX(-50%)}
.sp-help{position:absolute;bottom:10px;left:0;right:0;display:flex;justify-content:space-around;font-size:12px;color:#e2e8f0}
.sp-help div{background:var(--glass);padding:6px 12px;border-radius:12px}
kbd{display:inline-block;background:#334155;border-radius:5px;padding:0 6px;margin:0 1px;font-family:inherit;font-weight:800;font-size:12px;border-bottom:2px solid #0f172a}

/* ---------- screens ---------- */
.screen{position:fixed;inset:0;z-index:30;display:flex;align-items:center;justify-content:center;padding:16px}
#scr-menu,#scr-count{background:radial-gradient(ellipse at center,rgba(5,7,13,.35),rgba(5,7,13,.85))}
.menu-card{width:min(560px,100%);max-height:100%;overflow:auto;background:var(--glass2);border:1px solid var(--line);border-radius:28px;padding:26px 22px;text-align:center;box-shadow:0 24px 60px rgba(0,0,0,.5)}
.logo{font-size:44px;width:76px;height:76px;margin:0 auto 8px;border-radius:22px;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#06b6d4,#2563eb);box-shadow:0 10px 30px rgba(34,211,238,.35)}
h1{font-size:clamp(22px,5vw,30px);font-weight:800;letter-spacing:-.5px}
.sub{color:var(--muted);font-size:14px;margin:4px 0 18px}
.menu-btns{display:flex;flex-direction:column;gap:10px}
.big{width:100%;padding:14px 16px;border-radius:18px;font-size:18px;font-weight:800;display:flex;flex-direction:column;align-items:center;gap:2px;color:#04121a}
.big small{font-size:12px;font-weight:600;opacity:.8}
.cyan{background:linear-gradient(135deg,#22d3ee,#3b82f6)}
.orange{background:linear-gradient(135deg,#fb923c,#f43f5e)}
.lime{background:linear-gradient(135deg,#bef264,#22c55e)}
.ghost{background:rgba(255,255,255,.08);border:1px solid var(--line);color:var(--text)}
.howto{margin-top:16px;text-align:left;background:rgba(255,255,255,.05);border-radius:16px;padding:10px 14px;font-size:13px}
.howto summary{font-weight:800;cursor:pointer}
.howto table{width:100%;margin-top:8px;border-collapse:collapse}
.howto td{padding:4px 2px;color:#cbd5e1;vertical-align:top}
.howto td:first-child{white-space:nowrap;padding-right:8px}
.count-btns{display:flex;gap:10px;margin:14px 0}
.count-btns button{flex:1;padding:18px 0;font-size:28px}

.screen.bottom{align-items:flex-end;padding:0;background:linear-gradient(transparent 35%,rgba(5,7,13,.92) 75%)}
.sel{width:100%;max-width:1000px;margin:0 auto;padding:14px 16px 18px}
.sel-head{display:flex;align-items:center;gap:10px;margin-bottom:10px}
.sel-head h2{font-size:clamp(18px,4.5vw,26px);font-weight:800;text-shadow:0 2px 10px rgba(0,0,0,.6)}
.back{width:42px;height:42px;border-radius:12px;background:var(--glass);border:1px solid var(--line);font-size:20px;flex:none}
.cards{display:flex;gap:10px;overflow-x:auto;padding:4px 2px 10px;scroll-snap-type:x mandatory}
.card{flex:1 0 220px;scroll-snap-align:start;background:var(--glass2);border:2px solid var(--line);border-radius:20px;padding:12px 14px;text-align:left;cursor:pointer;transition:border-color .15s,transform .15s}
.card.sel-on{border-color:var(--cyan);box-shadow:0 0 0 3px rgba(34,211,238,.25);transform:translateY(-3px)}
.card .t{font-size:18px;font-weight:800}
.card .tag{display:inline-block;font-size:12px;font-weight:800;padding:1px 9px;border-radius:999px;margin:3px 0 6px;color:#04121a}
.card .d{font-size:12.5px;color:#cbd5e1;min-height:34px}
.stat{display:flex;align-items:center;gap:8px;font-size:12px;margin-top:5px}
.stat span{width:70px;color:var(--muted)}
.stat .bar{flex:1;display:flex;gap:3px}
.stat .bar i{flex:1;height:8px;border-radius:3px;background:rgba(255,255,255,.12)}
.stat .bar i.f{background:var(--cyan)}
.card .emoji{font-size:34px;float:right;line-height:1}
.card .best{font-size:12px;color:var(--gold);margin-top:6px;font-weight:600}
.go{margin-top:6px}

.countdown{position:fixed;inset:0;z-index:25;display:flex;align-items:center;justify-content:center;font-size:min(34vw,200px);font-weight:800;color:#fff;text-shadow:0 8px 40px rgba(0,0,0,.6);pointer-events:none}
.countdown.pop{animation:pop .9s ease-out}
@keyframes pop{0%{transform:scale(1.6);opacity:0}25%{transform:scale(1);opacity:1}100%{transform:scale(.8);opacity:.2}}
.toast{position:fixed;top:132px;left:50%;transform:translate(-50%,-10px);z-index:40;background:rgba(15,23,42,.94);border:1px solid var(--cyan);border-radius:16px;padding:10px 18px;font-weight:600;font-size:15px;opacity:0;transition:all .25s;pointer-events:none;text-align:center;max-width:90vw}
.toast.show{opacity:1;transform:translate(-50%,0)}

.modal{position:fixed;inset:0;z-index:50;background:rgba(3,6,14,.72);backdrop-filter:blur(6px);-webkit-backdrop-filter:blur(6px);display:flex;align-items:center;justify-content:center;padding:16px}
.modal-card{width:min(440px,100%);max-height:100%;overflow:auto;background:var(--glass2);border:1px solid var(--line);border-radius:26px;padding:22px;text-align:center}
.modal-card.wide{width:min(820px,100%);height:min(80vh,700px);display:flex;flex-direction:column;text-align:left}
.m-icon{font-size:52px;line-height:1.1}
.modal-card h2{font-size:24px;font-weight:800;margin:6px 0}
#modal-body{color:#cbd5e1;font-size:15px;margin-bottom:14px}
.stars{font-size:38px;letter-spacing:4px;margin:6px 0}
.stars .off{filter:grayscale(1);opacity:.3}
.rank{display:flex;flex-direction:column;gap:6px;margin:8px 0;text-align:left}
.rank div{display:flex;justify-content:space-between;background:rgba(255,255,255,.06);border-radius:12px;padding:8px 12px;font-weight:600}
.m-btns{display:flex;flex-direction:column;gap:8px}
.m-btns .big{font-size:16px;padding:12px}
.gal-head{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px}
.gal-grid{flex:1;overflow:auto;display:grid;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));gap:10px;align-content:start}
.gal-grid .it{background:rgba(255,255,255,.05);border-radius:14px;padding:6px;font-size:12px}
.gal-grid img,.gal-grid video{width:100%;height:110px;object-fit:cover;border-radius:10px;background:#000;display:block}
.gal-grid a{display:block;text-align:center;margin-top:5px;padding:4px;border-radius:8px;background:#0891b2;color:#fff;text-decoration:none;font-weight:600}
.photo-pop{position:fixed;right:70px;bottom:70px;z-index:35;width:min(300px,60vw);background:var(--glass2);border:1px solid var(--cyan);border-radius:16px;padding:8px}
.photo-pop img{width:100%;border-radius:10px;display:block}
.photo-pop .row{display:flex;justify-content:space-between;align-items:center;margin-top:6px;font-size:12px}
.photo-pop a{color:#fff;background:#0891b2;padding:3px 10px;border-radius:8px;text-decoration:none;font-weight:600}
#flash{position:fixed;inset:0;background:#fff;opacity:0;pointer-events:none;z-index:60;transition:opacity .25s}

@media (max-width:640px){
  .tb-right .batt,.tb-right #b-rain{display:none}
  .mission{max-width:40vw;font-size:12px}
  .tele b{font-size:15px;min-width:36px}
  .tele div{padding:0 5px}
  .guide{top:100px;font-size:12px}
  .rail{gap:6px}
  .card{flex-basis:78vw}
}
@media (max-width:520px) and (min-height:501px){
  .tb-center{top:58px}
  .mission{max-width:52vw}
  .guide{top:104px}
  .toast{top:146px}
  .pads{padding:0 8px}
  .pad{grid-template-columns:repeat(3,52px);grid-template-rows:repeat(3,48px);gap:4px}
  .rail{top:46%}
}
@media (max-height:500px){
  .rail{top:58px;transform:none;flex-direction:row}
  #b-gup,#b-gdn,.gim{display:none}
  .rail .ic.lg{width:40px;height:40px;font-size:18px}
  .shutter{width:44px;height:44px;border-width:4px}
  .pads{bottom:6px;padding:0 8px}
  .pad{grid-template-columns:repeat(3,48px);grid-template-rows:repeat(3,40px);gap:4px}
  .pad button{font-size:17px}
  .tele{bottom:6px;padding:4px 6px}.tele div{padding:0 5px}.tele b{font-size:14px;min-width:34px}
  .topbar{padding:8px 10px 20px}
  .tb-center{top:8px}
  .guide{top:62px;font-size:12px}
  .toast{top:108px;font-size:13px}
  .photo-pop{bottom:10px;right:50%;transform:translateX(50%);width:220px}
  .screen.bottom .d{min-height:0}
  .card{padding:8px 12px}
  .stat{margin-top:2px}
}
</style>
</head>
<body>
<div id="cv"></div>
<div id="flash"></div>

<!-- ===== HUD (เล่นคนเดียว / ผลัดกันเล่น) ===== -->
<div id="hud" class="hidden">
  <div class="topbar">
    <div class="tb-left">
      <button id="b-pause" class="ic" title="หยุดเกม (Esc)">☰</button>
      <button id="b-mode" class="pill mode" title="โหมดบิน (M)">N</button>
      <div id="mission" class="pill mission">🎯 บินลอดห่วง</div>
    </div>
    <div class="tb-center">
      <div id="timer" class="pill timer">00:00.0</div>
      <div id="ptag" class="pill ptag hidden"></div>
    </div>
    <div class="tb-right">
      <div id="rec" class="pill rec hidden">● REC <span id="rec-t">00:00</span></div>
      <div class="pill batt">🔋 <span id="batt">100%</span></div>
      <button id="b-tod" class="ic" title="เปลี่ยนเวลา กลางวัน/เย็น/กลางคืน">☀️</button>
      <button id="b-rain" class="ic" title="ฝนตก">🌧️</button>
      <button id="b-gal" class="ic" title="คลังภาพ">🖼️<span id="gal-n" class="badge">0</span></button>
    </div>
  </div>
  <div id="guide" class="guide">ห่วงถัดไป</div>
  <div class="rail right">
    <button id="b-view" class="ic lg" title="เปลี่ยนมุมกล้อง (X)">🎥</button>
    <button id="b-zoom" class="ic lg" title="ซูม (Z)" style="font-size:15px;font-weight:800">1x</button>
    <button id="b-gup" class="ic" title="เงยกล้อง (T)">▲</button>
    <div id="gimbal" class="gim">0°</div>
    <button id="b-gdn" class="ic" title="ก้มกล้อง (G)">▼</button>
    <button id="b-video" class="ic lg" title="อัดวิดีโอ (V)">⏺️</button>
    <button id="b-shot" class="shutter" title="ถ่ายรูป (C)"></button>
  </div>
  <div class="rail left">
    <button id="b-rth" class="ic lg" title="บินกลับฐาน (H)">🏠</button>
    <button id="b-light" class="ic lg" title="ไฟหน้า (F)">💡</button>
    <button id="b-touch" class="ic lg" title="ปุ่มบังคับบนจอ">🎮</button>
  </div>
  <div id="pads" class="pads hidden">
    <div class="pad">
      <button class="u" data-k="up">⬆<small>บินขึ้น</small></button>
      <button class="l" data-k="tl">⟲<small>หมุนซ้าย</small></button>
      <button class="r" data-k="tr">⟳<small>หมุนขวา</small></button>
      <button class="d" data-k="down">⬇<small>บินลง</small></button>
    </div>
    <div class="pad">
      <button class="u" data-k="fwd">▲<small>เดินหน้า</small></button>
      <button class="l" data-k="left">◀<small>ซ้าย</small></button>
      <button class="r" data-k="right">▶<small>ขวา</small></button>
      <button class="d" data-k="back">▼<small>ถอยหลัง</small></button>
    </div>
  </div>
  <div class="tele">
    <div><span>D</span><b id="t-d">0.0</b><i>m</i></div>
    <div><span>H</span><b id="t-h">0.0</b><i>m</i></div>
    <div><span>HS</span><b id="t-hs">0.0</b><i>km/h</i></div>
    <div><span>VS</span><b id="t-vs">0.0</b><i>m/s</i></div>
  </div>
</div>

<!-- ===== HUD แข่ง 2 คนจอแยก ===== -->
<div id="hud2" class="hidden">
  <div class="divider"></div>
  <div id="sp1" class="sp sp1"></div>
  <div id="sp2" class="sp sp2"></div>
  <div id="sp-timer" class="pill sp-timer">00:00.0</div>
  <button id="b-pause2" class="ic sp-pause" title="หยุดเกม (Esc)">☰</button>
  <div class="sp-help">
    <div>คนที่ 1: <kbd>W</kbd><kbd>S</kbd> หน้า/หลัง <kbd>A</kbd><kbd>D</kbd> เลี้ยว <kbd>E</kbd> ขึ้น <kbd>Q</kbd> ลง</div>
    <div>คนที่ 2: <kbd>↑</kbd><kbd>↓</kbd> หน้า/หลัง <kbd>←</kbd><kbd>→</kbd> เลี้ยว <kbd>O</kbd> ขึ้น <kbd>U</kbd> ลง</div>
  </div>
</div>

<!-- ===== เมนูหลัก ===== -->
<div id="scr-menu" class="screen hidden">
  <div class="menu-card">
    <div class="logo">🚁</div>
    <h1>DJI Drone Simulator 3D</h1>
    <p class="sub">เกมบินโดรนของมนตรี • 4 ด่าน • 3 โดรน • แข่งกับเพื่อนได้!</p>
    <div class="menu-btns">
      <button id="m-solo" class="big cyan">🚁 เล่นคนเดียว<small>บินลอดห่วง แล้วถ่ายรูปสถานที่สำคัญ</small></button>
      <button id="m-split" class="big orange">⚔️ แข่ง 2 คน จอแยก<small>เล่นพร้อมกันบนคีย์บอร์ดเครื่องเดียว</small></button>
      <button id="m-turns" class="big lime">🏆 ผลัดกันแข่ง 2-4 คน<small>ใครบินลอดห่วงครบเร็วที่สุดชนะ</small></button>
    </div>
    <details class="howto">
      <summary>🎮 วิธีบังคับโดรน</summary>
      <table>
        <tr><td><kbd>W</kbd><kbd>A</kbd><kbd>S</kbd><kbd>D</kbd> / ลูกศร</td><td>เดินหน้า / ซ้าย / ถอยหลัง / ขวา</td></tr>
        <tr><td><kbd>Space</kbd> / <kbd>Shift</kbd></td><td>บินขึ้น / บินลง</td></tr>
        <tr><td><kbd>Q</kbd> / <kbd>E</kbd></td><td>หมุนตัวซ้าย / หมุนตัวขวา</td></tr>
        <tr><td><kbd>C</kbd> <kbd>V</kbd></td><td>ถ่ายรูป / อัดวิดีโอ</td></tr>
        <tr><td><kbd>X</kbd> <kbd>Z</kbd></td><td>เปลี่ยนมุมกล้อง / ซูม</td></tr>
        <tr><td><kbd>T</kbd> <kbd>G</kbd></td><td>เงยกล้อง / ก้มกล้อง</td></tr>
        <tr><td><kbd>M</kbd> <kbd>F</kbd> <kbd>H</kbd></td><td>โหมดบิน / ไฟหน้า / บินกลับฐาน</td></tr>
        <tr><td>ลากเมาส์บนจอ</td><td>หมุนมองรอบๆ</td></tr>
      </table>
    </details>
  </div>
</div>

<div id="scr-count" class="screen hidden">
  <div class="menu-card">
    <div class="logo">🏆</div>
    <h1>ผลัดกันแข่ง</h1>
    <p class="sub">มีผู้เล่นกี่คน? แต่ละคนผลัดกันบิน ใครเร็วสุดชนะ</p>
    <div class="count-btns">
      <button class="big lime" data-count="2">2</button>
      <button class="big lime" data-count="3">3</button>
      <button class="big lime" data-count="4">4</button>
    </div>
    <button class="big ghost" data-back="menu">← กลับ</button>
  </div>
</div>

<div id="scr-drone" class="screen bottom hidden">
  <div class="sel">
    <div class="sel-head"><button class="back" id="drone-back">←</button><h2 id="drone-title">เลือกโดรน</h2></div>
    <div id="drone-cards" class="cards"></div>
    <button id="b-drone-ok" class="big cyan go">เลือกลำนี้ ➜</button>
  </div>
</div>

<div id="scr-level" class="screen bottom hidden">
  <div class="sel">
    <div class="sel-head"><button class="back" id="level-back">←</button><h2>เลือกด่าน</h2></div>
    <div id="level-cards" class="cards"></div>
    <button id="b-level-ok" class="big cyan go">เริ่มบิน ➜</button>
  </div>
</div>

<div id="countdown" class="countdown hidden"></div>
<div id="toast" class="toast"></div>

<div id="modal" class="modal hidden">
  <div class="modal-card">
    <div id="modal-icon" class="m-icon"></div>
    <h2 id="modal-title"></h2>
    <div id="modal-body"></div>
    <div id="modal-btns" class="m-btns"></div>
  </div>
</div>

<div id="gal" class="modal hidden">
  <div class="modal-card wide">
    <div class="gal-head"><h2>🖼️ คลังภาพและวิดีโอ</h2><button id="gal-x" class="ic">✕</button></div>
    <div id="gal-grid" class="gal-grid"></div>
  </div>
</div>

<div id="photo-pop" class="photo-pop hidden">
  <img id="photo-img" alt="รูปที่ถ่าย">
  <div class="row"><span id="photo-cap"></span><a id="photo-dl" download="drone_photo.jpg">⬇ ดาวน์โหลด</a></div>
</div>
<script>
'use strict';
/* =====================================================================
   DJI Drone Simulator 3D — เกมของมนตรี
   ส่วนที่ 1: ค่าตั้งต้น เสียง และโมเดลโดรน
   ===================================================================== */
const V3 = THREE.Vector3;
const $ = id => document.getElementById(id);
const clamp = THREE.MathUtils.clamp;
const lerp = THREE.MathUtils.lerp;
const smooth = (a, b, x) => { const t = clamp((x - a) / (b - a), 0, 1); return t * t * (3 - 2 * t); };
function makeRng(seed) { let s = seed >>> 0; return () => { s = (s * 1664525 + 1013904223) >>> 0; return s / 4294967296; }; }
function store(k, v) { try { localStorage.setItem('motree_' + k, JSON.stringify(v)); } catch (e) {} }
function load(k, def) { try { const v = localStorage.getItem('motree_' + k); return v == null ? def : JSON.parse(v); } catch (e) { return def; } }
function fmtTime(s) { const m = Math.floor(s / 60), r = s - m * 60; return String(m).padStart(2, '0') + ':' + r.toFixed(1).padStart(4, '0'); }

/* ---------- โดรน 3 ลำ ---------- */
const DRONES = {
  mini: {
    name: 'DJI Mini', tag: 'บังคับง่าย', tagColor: '#a3e635', emoji: '🟢',
    desc: 'ลำเล็ก เบา หยุดนิ่งได้ทันที เหมาะกับมือใหม่',
    speed: 13, accel: 6.5, climb: 5.5, turn: 2.0, tilt: 0.22, scale: 0.78,
    stats: [2, 5, 3], photoW: 1600, maxZoom: 2, photoBonus: 1.25,
    look: { body: 0xf1f3f5, top: 0xd5d9de, arm: 0xe5e7eb, cam: 0x2a2e35 }
  },
  fpv: {
    name: 'DJI FPV', tag: 'บินเร็วสุด', tagColor: '#fb923c', emoji: '🔥',
    desc: 'เร็วแรงแบบโดรนแข่ง แต่เลี้ยวยากและไถลไกล',
    speed: 34, accel: 2.3, climb: 12, turn: 2.7, tilt: 0.5, scale: 1.0,
    stats: [5, 2, 2], photoW: 1280, maxZoom: 1, photoBonus: 1.0,
    look: { body: 0x2b2f36, top: 0x3a3f47, arm: 0x24272d, cam: 0x111317, accent: 0xff6a13 }
  },
  mavic: {
    name: 'DJI Mavic 3 Pro', tag: 'กล้องชัดสุด', tagColor: '#22d3ee', emoji: '📸',
    desc: 'กล้อง 3 ตัว ภาพคมชัดสุด ซูมได้ 4 เท่า',
    speed: 20, accel: 3.8, climb: 7, turn: 1.9, tilt: 0.28, scale: 1.0,
    stats: [3, 3, 5], photoW: 2560, maxZoom: 4, photoBonus: 1.6,
    look: { body: 0x9aa0a8, top: 0x4a4f57, arm: 0x7d838b, cam: 0x1d2127 }
  }
};
const DRONE_ORDER = ['mini', 'fpv', 'mavic'];
const FLIGHT_MODES = {
  cine: { mul: 0.55, label: 'C', name: 'โหมดภาพยนตร์ (ช้า นุ่มนวล)' },
  normal: { mul: 1.0, label: 'N', name: 'โหมดปกติ' },
  sport: { mul: 1.35, label: 'S', name: 'โหมดสปอร์ต (เร็วขึ้น)' }
};
const PLAYER_COLORS = [0x22d3ee, 0xf97316, 0xa3e635, 0xf472b6];
const PLAYER_CSS = ['#22d3ee', '#f97316', '#a3e635', '#f472b6'];
const RING_R = 4.6;

/* ---------- สถานะเกม ---------- */
const game = {
  state: 'menu',          // menu | count | drone | level | countdown | play | paused | result
  mode: 'solo',           // solo | split | turns
  levelId: 'city',
  players: [],
  active: 0,              // ผู้เล่นที่กำลังบิน (โหมดผลัดกัน)
  turnCount: 2, turnResults: [],
  elapsed: 0, countdown: 0,
  tod: 'day', rain: false, headlight: false,
  flightMode: 'normal', camView: 0, zoom: 1, gimbal: -5,
  photos: [], battery: 100,
  pickType: 'mavic', pickFor: 0,
  touchOn: false
};

/* ---------- เสียง ---------- */
const sfx = {
  ctx: null, gain: null, osc: [],
  init() {
    if (this.ctx) { if (this.ctx.state === 'suspended') this.ctx.resume(); return; }
    try {
      const AC = window.AudioContext || window.webkitAudioContext; if (!AC) return;
      this.ctx = new AC();
      const f = this.ctx.createBiquadFilter(); f.type = 'lowpass'; f.frequency.value = 700;
      this.gain = this.ctx.createGain(); this.gain.gain.value = 0;
      ['sawtooth', 'square'].forEach((t, i) => { const o = this.ctx.createOscillator(); o.type = t; o.frequency.value = 110 + i * 1.7; o.connect(f); o.start(); this.osc.push(o); });
      f.connect(this.gain); this.gain.connect(this.ctx.destination);
    } catch (e) {}
  },
  hum(level, pitch) {
    if (!this.ctx) return; const t = this.ctx.currentTime;
    this.gain.gain.setTargetAtTime(level * 0.03, t, 0.12);
    this.osc.forEach((o, i) => o.frequency.setTargetAtTime(pitch * (1 + i * 0.012), t, 0.12));
  },
  beep(freq, dur = 0.15, type = 'sine', vol = 0.15, slide = 0, delay = 0) {
    if (!this.ctx) return;
    try {
      const t = this.ctx.currentTime + delay, o = this.ctx.createOscillator(), g = this.ctx.createGain();
      o.type = type; o.frequency.setValueAtTime(freq, t);
      if (slide) o.frequency.exponentialRampToValueAtTime(freq * slide, t + dur);
      g.gain.setValueAtTime(vol, t); g.gain.exponentialRampToValueAtTime(0.001, t + dur);
      o.connect(g); g.connect(this.ctx.destination); o.start(t); o.stop(t + dur + 0.05);
    } catch (e) {}
  },
  ring() { this.beep(880, 0.2, 'sine', 0.16, 2); this.beep(1320, 0.18, 'triangle', 0.08, 0, 0.08); },
  bump() { this.beep(160, 0.18, 'square', 0.1, 0.5); },
  shutter() { this.beep(2600, 0.04, 'square', 0.07); this.beep(1700, 0.05, 'square', 0.05, 0, 0.06); },
  count(go) { this.beep(go ? 1320 : 660, go ? 0.45 : 0.2, 'triangle', 0.2); },
  win() { [523, 659, 784, 1047].forEach((f, i) => this.beep(f, 0.3, 'triangle', 0.15, 0, i * 0.12)); },
  click() { this.beep(1100, 0.05, 'sine', 0.06); },
  fail() { this.beep(330, 0.25, 'sawtooth', 0.08, 0.7); }
};

/* ---------- ตัวช่วยสร้างของ 3 มิติ ---------- */
const _matCache = {};
function mat(color, o = {}) {
  const key = color + JSON.stringify(o);
  if (!_matCache[key]) _matCache[key] = new THREE.MeshStandardMaterial(Object.assign({ color, roughness: 0.6, metalness: 0.05 }, o));
  return _matCache[key];
}
function mesh(geo, material, x = 0, y = 0, z = 0, parent) {
  const m = new THREE.Mesh(geo, material); m.position.set(x, y, z);
  if (parent) parent.add(m); return m;
}
// แท่งเชื่อมระหว่างจุด 2 จุด (ใช้ทำแขนโดรน)
function beam(p0, p1, w, h, material, parent) {
  const len = p0.distanceTo(p1);
  const m = new THREE.Mesh(new THREE.BoxGeometry(w, h, len), material);
  m.position.copy(p0).add(p1).multiplyScalar(0.5); m.lookAt(p1); parent.add(m); return m;
}
// ตัวถังทรงโดรน DJI มองจากด้านบน (หัวแคบ ท้ายมน) แล้วรีดให้หนา
function droneShellGeo(len, wid, hgt) {
  const L = len / 2, W = wid / 2, s = new THREE.Shape();
  s.moveTo(-W * 0.5, L);
  s.lineTo(W * 0.5, L);
  s.quadraticCurveTo(W * 0.95, L * 0.8, W, L * 0.3);
  s.lineTo(W * 0.96, -L * 0.5);
  s.quadraticCurveTo(W * 0.9, -L, W * 0.4, -L);
  s.lineTo(-W * 0.4, -L);
  s.quadraticCurveTo(-W * 0.9, -L, -W * 0.96, -L * 0.5);
  s.lineTo(-W, L * 0.3);
  s.quadraticCurveTo(-W * 0.95, L * 0.8, -W * 0.5, L);
  const g = new THREE.ExtrudeGeometry(s, { depth: hgt, bevelEnabled: true, bevelThickness: hgt * 0.3, bevelSize: Math.min(W, L) * 0.2, bevelSegments: 4, curveSegments: 10 });
  g.rotateX(-Math.PI / 2);          // หัวโดรนหันไปทาง -Z
  g.translate(0, -hgt / 2, 0);
  return g;
}
function lensGeo(r, len) { const g = new THREE.CylinderGeometry(r, r, len, 20); g.rotateX(Math.PI / 2); return g; }

// ใบพัด 2 แฉก + แผ่นเบลอตอนหมุนเร็ว
function makeProp(parent, x, y, z, dir, bladeLen, discMat, bladeMat, tipMat) {
  const grp = new THREE.Group(); grp.position.set(x, y, z); parent.add(grp);
  const blades = new THREE.Group(); grp.add(blades);
  for (let i = 0; i < 2; i++) {
    const b = mesh(new THREE.BoxGeometry(bladeLen, 0.012, 0.075), bladeMat, bladeLen / 2 * (i ? -1 : 1), 0, 0, blades);
    b.rotation.x = (i ? -1 : 1) * 0.18 * dir;
    if (tipMat) mesh(new THREE.BoxGeometry(0.07, 0.014, 0.078), tipMat, bladeLen * 0.93 * (i ? -1 : 1), 0, 0, blades);
  }
  mesh(new THREE.CylinderGeometry(0.035, 0.035, 0.05, 10), bladeMat, 0, 0.01, 0, grp);
  const disc = new THREE.Mesh(new THREE.CircleGeometry(bladeLen, 28), discMat);
  disc.rotation.x = -Math.PI / 2; grp.add(disc);
  grp.rotation.y = Math.random() * 6;
  return { grp, blades, disc, dir };
}

/* ---------- โมเดลโดรนทรง DJI Mavic / Mini (แขนพับ) ---------- */
function buildFoldDrone(body, spec, type, props, leds) {
  const c = spec.look, isPro = type === 'mavic';
  const bodyMat = new THREE.MeshStandardMaterial({ color: c.body, roughness: 0.42, metalness: isPro ? 0.35 : 0.1 });
  const topMat = new THREE.MeshStandardMaterial({ color: c.top, roughness: 0.35, metalness: 0.3 });
  const armMat = new THREE.MeshStandardMaterial({ color: c.arm, roughness: 0.45, metalness: 0.25 });
  const darkMat = mat(0x16181c, { roughness: 0.3, metalness: 0.6 });
  const glass = mat(0x0a1628, { roughness: 0.05, metalness: 0.95 });
  // ตัวถังหลัก + ฝาแบตเตอรี่ด้านบน
  mesh(droneShellGeo(1.5, 0.62, 0.24), bodyMat, 0, 0, 0, body);
  mesh(droneShellGeo(0.95, 0.5, 0.04), topMat, 0, 0.19, 0.16, body);
  mesh(new THREE.BoxGeometry(0.34, 0.03, 0.05), darkMat, 0, 0.23, 0.55, body);        // ปุ่มปลดแบต
  // เซนเซอร์หลบสิ่งกีดขวาง (ตาคู่หน้า-หลัง)
  [-0.13, 0.13].forEach(x => {
    mesh(new THREE.SphereGeometry(0.045, 12, 10), glass, x, 0.03, -0.8, body);
    mesh(new THREE.SphereGeometry(0.04, 12, 10), glass, x, 0.03, 0.8, body);
  });
  // กิมบอล + กล้อง
  mesh(new THREE.BoxGeometry(0.2, 0.08, 0.16), darkMat, 0, -0.17, -0.64, body);
  const camMat = new THREE.MeshStandardMaterial({ color: c.cam, roughness: 0.35, metalness: 0.5 });
  if (isPro) {
    mesh(new THREE.BoxGeometry(0.36, 0.24, 0.26), camMat, 0, -0.29, -0.74, body);
    mesh(lensGeo(0.085, 0.05), mat(0x9ca3af, { metalness: 0.9, roughness: 0.2 }), -0.07, -0.29, -0.88, body);
    mesh(lensGeo(0.07, 0.06), glass, -0.07, -0.29, -0.9, body);
    mesh(lensGeo(0.045, 0.05), glass, 0.1, -0.24, -0.88, body);
    mesh(lensGeo(0.035, 0.05), glass, 0.1, -0.34, -0.88, body);
    mesh(new THREE.BoxGeometry(0.05, 0.02, 0.01), mat(0xf59e0b, { emissive: 0xf59e0b, emissiveIntensity: 0.4 }), 0.12, -0.18, -0.875, body);
  } else {
    mesh(new THREE.SphereGeometry(0.12, 18, 14), camMat, 0, -0.27, -0.72, body);
    mesh(lensGeo(0.055, 0.06), glass, 0, -0.27, -0.83, body);
  }
  // แขนพับ 4 ข้าง: หน้า (สูง กางไปข้างหน้า) / หลัง (ต่ำ กางไปข้างหลัง)
  const arms = [
    { a: new V3(0.26, 0.07, -0.42), b: new V3(0.8, 0.1, -0.74), front: true },
    { a: new V3(-0.26, 0.07, -0.42), b: new V3(-0.8, 0.1, -0.74), front: true },
    { a: new V3(0.27, -0.04, 0.5), b: new V3(0.84, 0.02, 0.72), front: false },
    { a: new V3(-0.27, -0.04, 0.5), b: new V3(-0.84, 0.02, 0.72), front: false }
  ];
  const discMat = new THREE.MeshBasicMaterial({ color: 0x9aa3ad, transparent: true, opacity: 0, depthWrite: false, side: THREE.DoubleSide });
  const bladeMat = mat(0x1b1d21, { roughness: 0.5 });
  const tipMat = isPro ? mat(0xd4d8dd) : null;
  arms.forEach((arm, i) => {
    beam(arm.a, arm.b, 0.09, 0.06, armMat, body);
    mesh(new THREE.CylinderGeometry(0.1, 0.09, 0.13, 18), darkMat, arm.b.x, arm.b.y + 0.02, arm.b.z, body);
    mesh(new THREE.CylinderGeometry(0.1, 0.1, 0.02, 18), armMat, arm.b.x, arm.b.y + 0.09, arm.b.z, body);
    // ขาตั้งเล็กๆ ใต้มอเตอร์หน้า
    if (arm.front) mesh(new THREE.CylinderGeometry(0.02, 0.025, 0.2, 8), darkMat, arm.b.x, arm.b.y - 0.13, arm.b.z, body);
    // ไฟ LED ใต้แขน: หน้าสีแดง หลังสีเขียว
    const led = mesh(new THREE.SphereGeometry(0.035, 8, 8), new THREE.MeshBasicMaterial({ color: arm.front ? 0xff2a2a : 0x22ff66 }), arm.b.x * 0.92, arm.b.y - 0.06, arm.b.z * 0.95, body);
    leds.push({ m: led, blink: !arm.front });
    props.push(makeProp(body, arm.b.x, arm.b.y + 0.14, arm.b.z, i % 3 === 0 ? 1 : -1, 0.46, discMat, bladeMat, tipMat));
  });
  // ขาหลัง
  [-0.18, 0.18].forEach(x => mesh(new THREE.BoxGeometry(0.05, 0.12, 0.08), darkMat, x, -0.17, 0.5, body));
}

/* ---------- โมเดลโดรนแข่ง DJI FPV ---------- */
function buildFpvDrone(body, spec, props, leds) {
  const c = spec.look;
  const bodyMat = new THREE.MeshStandardMaterial({ color: c.body, roughness: 0.4, metalness: 0.3 });
  const accent = new THREE.MeshStandardMaterial({ color: c.accent, roughness: 0.4, emissive: c.accent, emissiveIntensity: 0.15 });
  const darkMat = mat(0x111317, { roughness: 0.3, metalness: 0.6 });
  const glass = mat(0x0a1628, { roughness: 0.05, metalness: 0.95 });
  mesh(droneShellGeo(1.35, 0.5, 0.28), bodyMat, 0, 0, 0, body);
  mesh(new THREE.BoxGeometry(0.1, 0.03, 0.9), accent, 0, 0.21, 0.05, body);                     // แถบส้มบนหลัง
  const canopy = mesh(new THREE.SphereGeometry(0.22, 18, 12, 0, Math.PI * 2, 0, Math.PI / 2), glass, 0, 0.12, -0.42, body);
  canopy.scale.set(1, 0.7, 1.3);
  mesh(new THREE.BoxGeometry(0.2, 0.16, 0.12), darkMat, 0, -0.02, -0.72, body);                 // กล้องหน้า
  mesh(lensGeo(0.055, 0.06), glass, 0, -0.02, -0.8, body);
  [-0.1, 0.1].forEach(x => { const a = mesh(new THREE.CylinderGeometry(0.012, 0.012, 0.4, 6), darkMat, x, 0.3, 0.55, body); a.rotation.x = -0.5; });
  const discMat = new THREE.MeshBasicMaterial({ color: 0xff8a3d, transparent: true, opacity: 0, depthWrite: false, side: THREE.DoubleSide });
  const bladeMat = mat(0x202226);
  [[1, -1], [-1, -1], [1, 1], [-1, 1]].forEach(([sx, sz], i) => {
    const tip = new V3(0.78 * sx, 0.02, 0.7 * sz);
    beam(new V3(0.15 * sx, 0, 0.2 * sz), tip, 0.12, 0.07, bodyMat, body);
    beam(new V3(0.2 * sx, 0.04, 0.24 * sz), tip.clone().setY(0.06), 0.04, 0.02, accent, body);
    mesh(new THREE.CylinderGeometry(0.11, 0.1, 0.14, 18), darkMat, tip.x, 0.06, tip.z, body);
    mesh(new THREE.CylinderGeometry(0.02, 0.02, 0.18, 6), darkMat, tip.x, -0.1, tip.z, body);
    const led = mesh(new THREE.SphereGeometry(0.04, 8, 8), new THREE.MeshBasicMaterial({ color: sz < 0 ? 0xffffff : 0xff6a13 }), tip.x, -0.02, tip.z + 0.11 * sz, body);
    leds.push({ m: led, blink: sz > 0 });
    props.push(makeProp(body, tip.x, 0.17, tip.z, i % 3 === 0 ? 1 : -1, 0.42, discMat, bladeMat, accent));
  });
}

function buildDroneMesh(type, accentColor) {
  const spec = DRONES[type];
  const root = new THREE.Group(); root.rotation.order = 'YXZ';
  const body = new THREE.Group(); root.add(body);
  const props = [], leds = [];
  if (type === 'fpv') buildFpvDrone(body, spec, props, leds); else buildFoldDrone(body, spec, type, props, leds);
  if (accentColor != null) {   // แถบสีประจำผู้เล่น (โหมดแข่ง)
    mesh(new THREE.TorusGeometry(0.2, 0.035, 8, 24), new THREE.MeshBasicMaterial({ color: accentColor }), 0, 0.26, 0.15, body).rotation.x = Math.PI / 2;
  }
  body.scale.setScalar(spec.scale);
  root.traverse(o => { if (o.isMesh && !o.material.transparent) o.castShadow = true; });
  // ไฟหน้า (เปิดตอนกลางคืน)
  const spot = new THREE.SpotLight(0xffffff, 0, 90, Math.PI / 5, 0.5, 1.2);
  spot.position.set(0, -0.2, -0.8); spot.target.position.set(0, -6, -20);
  root.add(spot); root.add(spot.target);
  return { root, props, leds, spot };
}

/* ---------- ฟิสิกส์โดรน ---------- */
class Drone {
  constructor(type, accentColor) {
    this.type = type; this.spec = DRONES[type];
    const m = buildDroneMesh(type, accentColor);
    this.mesh = m.root; this.props = m.props; this.leds = m.leds; this.spot = m.spot;
    this.pos = new V3(); this.vel = new V3();
    this.yaw = 0; this.pitch = 0; this.roll = 0; this.spin = 0;
    this.flying = false; this.lastBump = 0; this.seed = Math.random() * 10;
    scene.add(this.mesh);
  }
  dispose() { scene.remove(this.mesh); this.mesh.traverse(o => { if (o.geometry) o.geometry.dispose(); }); }
  fwd() { return new V3(-Math.sin(this.yaw), 0, -Math.cos(this.yaw)); }     // หน้าโดรน
  right() { return new V3(Math.cos(this.yaw), 0, -Math.sin(this.yaw)); }    // ขวามือโดรน
  place(x, y, z, yaw) { this.pos.set(x, y, z); this.vel.set(0, 0, 0); this.yaw = yaw; this.pitch = this.roll = 0; this.flying = false; }

  // inp = { fwd: เดินหน้า(+)/ถอย(-), side: ขวา(+)/ซ้าย(-), up: ขึ้น(+)/ลง(-), turn: หมุนขวา(+)/ซ้าย(-) }
  update(dt, inp, t, armed) {
    const s = this.spec, mul = FLIGHT_MODES[game.flightMode].mul, vmax = s.speed * mul;
    let f = inp ? inp.fwd : 0, sd = inp ? inp.side : 0, up = inp ? inp.up : 0, tr = inp ? inp.turn : 0;
    const mag = Math.hypot(f, sd); if (mag > 1) { f /= mag; sd /= mag; }
    this.yaw -= tr * s.turn * dt;
    const F = this.fwd(), R = this.right();
    const k = 1 - Math.exp(-s.accel * dt);
    this.vel.x += ((F.x * f + R.x * sd) * vmax - this.vel.x) * k;
    this.vel.z += ((F.z * f + R.z * sd) * vmax - this.vel.z) * k;
    this.vel.y += (up * s.climb * Math.max(0.8, mul) - this.vel.y) * (1 - Math.exp(-5 * dt));
    this.pos.addScaledVector(this.vel, dt);

    const gy = LV.ground(this.pos.x, this.pos.z) + 0.3 * s.scale;
    if (this.pos.y < gy) { this.pos.y = gy; if (this.vel.y < 0) this.vel.y = 0; this.vel.x *= 0.9; this.vel.z *= 0.9; }
    if (this.pos.y > 320) { this.pos.y = 320; if (this.vel.y > 0) this.vel.y = 0; }
    const hd = Math.hypot(this.pos.x, this.pos.z), B = LV.bounds;
    if (hd > B) { this.pos.x *= B / hd; this.pos.z *= B / hd; this.vel.x *= -0.4; this.vel.z *= -0.4; if (this === activeDrone()) toast('🚧 ไกลเกินไปแล้ว บินกลับเข้ามานะ'); }
    this.collide();
    this.flying = this.pos.y > gy + 0.08 || up > 0;

    const lf = (this.vel.x * F.x + this.vel.z * F.z) / vmax, ls = (this.vel.x * R.x + this.vel.z * R.z) / vmax;
    const k2 = 1 - Math.exp(-8 * dt);
    this.pitch += (-clamp(lf, -1.2, 1.2) * s.tilt - this.pitch) * k2;   // เดินหน้า = ก้มหัว
    this.roll += (-clamp(ls, -1.2, 1.2) * s.tilt - this.roll) * k2;     // ไปขวา = เอียงขวา
    const target = this.flying ? 42 + Math.hypot(this.vel.x, this.vel.z) * 1.4 + Math.abs(this.vel.y) * 2 : (armed ? 20 : 0);
    this.spin += (target - this.spin) * (1 - Math.exp(-3 * dt));
    this.sync(t, dt);
  }
  sync(t, dt) {
    const bob = this.flying ? Math.sin(t * 2.3 + this.seed) * 0.035 : 0;
    this.mesh.position.set(this.pos.x, this.pos.y + bob, this.pos.z);
    this.mesh.rotation.set(this.pitch, this.yaw, this.roll);
    const blur = clamp((this.spin - 14) / 28, 0, 1);
    for (const p of this.props) {
      p.grp.rotation.y += this.spin * dt * p.dir;
      p.disc.material.opacity = 0.3 * blur;
      p.blades.visible = blur < 0.85;
    }
    for (const l of this.leds) if (l.blink) l.m.visible = Math.sin(t * 7 + this.seed) > -0.2;
    this.spot.intensity = game.headlight ? 3.2 : 0;
  }
  // ชนตึก / ภูเขา / เกาะ แล้วเด้งออก (ไม่พัง เล่นต่อได้เลย)
  collide() {
    const r = 0.6 * this.spec.scale, p = this.pos, v = this.vel; let hit = false;
    for (const c of LV.colliders) {
      if (c.t === 'box') {
        if (p.x < c.x0 - r || p.x > c.x1 + r || p.z < c.z0 - r || p.z > c.z1 + r || p.y < c.y0 - r || p.y > c.y1 + r) continue;
        const dx0 = p.x - (c.x0 - r), dx1 = c.x1 + r - p.x, dz0 = p.z - (c.z0 - r), dz1 = c.z1 + r - p.z, dy = c.y1 + r - p.y;
        const m = Math.min(dx0, dx1, dz0, dz1, dy);
        if (m === dy) { p.y = c.y1 + r; if (v.y < 0) v.y = 0; continue; }    // ลงจอดบนหลังคาได้
        hit = true;
        if (m === dx0) { p.x = c.x0 - r; v.x = -Math.abs(v.x) * 0.35; }
        else if (m === dx1) { p.x = c.x1 + r; v.x = Math.abs(v.x) * 0.35; }
        else if (m === dz0) { p.z = c.z0 - r; v.z = -Math.abs(v.z) * 0.35; }
        else { p.z = c.z1 + r; v.z = Math.abs(v.z) * 0.35; }
      } else {
        if (p.y < c.y0 - r || p.y > c.y1 + r) continue;
        const u = clamp((p.y - c.y0) / (c.y1 - c.y0), 0, 1);
        const rad = c.t === 'cone' ? c.r * (1 - u) : (c.r2 != null ? lerp(c.r, c.r2, u) : c.r);
        const dx = p.x - c.x, dz = p.z - c.z, d = Math.hypot(dx, dz), min = rad + r;
        if (d >= min) continue;
        if (c.t !== 'cone' && p.y > c.y1 - 0.6) { p.y = c.y1 + r; if (v.y < 0) v.y = 0; continue; }
        hit = true;
        const nx = d > 1e-4 ? dx / d : 1, nz = d > 1e-4 ? dz / d : 0;
        p.x = c.x + nx * min; p.z = c.z + nz * min;
        const vn = v.x * nx + v.z * nz; if (vn < 0) { v.x -= 1.35 * vn * nx; v.z -= 1.35 * vn * nz; }
        if (c.t === 'cone') v.y = Math.max(v.y, 2.5);
      }
    }
    if (hit) { const now = performance.now(); if (now - this.lastBump > 400) { this.lastBump = now; sfx.bump(); } }
    return hit;
  }
}

/* =====================================================================
   ส่วนที่ 2: ท้องฟ้า แสง เมฆ ฝน กลางวัน/กลางคืน + ตัวช่วยสร้างฉาก
   ===================================================================== */
let scene, renderer, clock, menuCam;
let skyMat, skyMesh, sunLight, hemiLight, starPts, cloudMesh, rainPts;
let cloudData = [];
const sunDir = new V3(0.4, 0.8, 0.3).normalize();
const focus = new V3();
let LV = { ground: () => 0, colliders: [], bounds: 400, updaters: [], nightMats: [], nightObjs: [], blinkers: [], rings: [], fx: [] };

function initEngine() {
  scene = new THREE.Scene();
  scene.fog = new THREE.FogExp2(0xc7dcef, 0.002);
  renderer = new THREE.WebGLRenderer({ antialias: true });
  renderer.setPixelRatio(Math.min(window.devicePixelRatio || 1, 1.75));
  renderer.setSize(window.innerWidth, window.innerHeight);
  renderer.shadowMap.enabled = true;
  renderer.shadowMap.type = THREE.PCFSoftShadowMap;
  $('cv').appendChild(renderer.domElement);
  clock = new THREE.Clock();
  menuCam = new THREE.PerspectiveCamera(55, window.innerWidth / window.innerHeight, 0.1, 3200);

  // ท้องฟ้าไล่สี + ดวงอาทิตย์/ดวงจันทร์
  skyMat = new THREE.ShaderMaterial({
    uniforms: { top: { value: new THREE.Color() }, bottom: { value: new THREE.Color() }, sunDir: { value: sunDir.clone() }, sunCol: { value: new THREE.Color(0xfff0c0) } },
    vertexShader: 'varying vec3 vDir; void main(){ vDir = position; gl_Position = projectionMatrix * modelViewMatrix * vec4(position,1.0); }',
    fragmentShader: 'uniform vec3 top; uniform vec3 bottom; uniform vec3 sunDir; uniform vec3 sunCol; varying vec3 vDir;' +
      'void main(){ vec3 d = normalize(vDir); vec3 c = mix(bottom, top, pow(smoothstep(-0.08, 0.65, d.y), 0.75));' +
      'float s = max(dot(d, normalize(sunDir)), 0.0); c += sunCol * (step(0.9993, s) * 1.3 + pow(s, 14.0) * 0.28);' +
      'gl_FragColor = vec4(c, 1.0); }',
    side: THREE.BackSide, depthWrite: false, fog: false
  });
  skyMesh = new THREE.Mesh(new THREE.SphereGeometry(1500, 32, 16), skyMat);
  skyMesh.frustumCulled = false; skyMesh.renderOrder = -10;
  skyMesh.onBeforeRender = (r, s, cam) => { skyMesh.position.copy(cam.position); skyMesh.updateMatrixWorld(true); };
  scene.add(skyMesh);

  // ดาวตอนกลางคืน
  const sp = [], rng = makeRng(99);
  for (let i = 0; i < 1400; i++) {
    const a = rng() * Math.PI * 2, y = 0.05 + rng() * 0.95, r = Math.sqrt(1 - y * y);
    sp.push(Math.cos(a) * r * 1400, y * 1400, Math.sin(a) * r * 1400);
  }
  const sg = new THREE.BufferGeometry(); sg.setAttribute('position', new THREE.Float32BufferAttribute(sp, 3));
  starPts = new THREE.Points(sg, new THREE.PointsMaterial({ color: 0xffffff, size: 2, sizeAttenuation: false, fog: false, transparent: true, opacity: 0.9, depthWrite: false }));
  starPts.frustumCulled = false; starPts.renderOrder = -9; starPts.visible = false;
  skyMesh.add(starPts);

  hemiLight = new THREE.HemisphereLight(0xdfeeff, 0x5b5a45, 0.7); scene.add(hemiLight);
  sunLight = new THREE.DirectionalLight(0xfff3dd, 1.25);
  sunLight.castShadow = true;
  const mobile = window.matchMedia('(pointer: coarse)').matches;
  sunLight.shadow.mapSize.set(mobile ? 1024 : 2048, mobile ? 1024 : 2048);
  const sc = sunLight.shadow.camera; sc.left = -80; sc.right = 80; sc.top = 80; sc.bottom = -80; sc.near = 1; sc.far = 900;
  sunLight.shadow.bias = -0.0006;
  scene.add(sunLight); scene.add(sunLight.target);

  // เมฆ
  cloudMesh = new THREE.InstancedMesh(new THREE.IcosahedronGeometry(1, 1),
    new THREE.MeshStandardMaterial({ color: 0xffffff, flatShading: true, roughness: 1, emissive: 0x8899aa, emissiveIntensity: 0.3 }), 260);
  cloudMesh.frustumCulled = false; scene.add(cloudMesh);

  // ฝน
  const rp = new Float32Array(2600 * 3);
  for (let i = 0; i < rp.length; i += 3) { rp[i] = (Math.random() - 0.5) * 140; rp[i + 1] = Math.random() * 70; rp[i + 2] = (Math.random() - 0.5) * 140; }
  const rg = new THREE.BufferGeometry(); rg.setAttribute('position', new THREE.BufferAttribute(rp, 3));
  rainPts = new THREE.Points(rg, new THREE.PointsMaterial({ color: 0xa5d8ff, size: 0.25, transparent: true, opacity: 0.7 }));
  rainPts.visible = false; rainPts.frustumCulled = false; scene.add(rainPts);

  window.addEventListener('resize', onResize);
}

function onResize() {
  renderer.setSize(window.innerWidth, window.innerHeight);
  menuCam.aspect = window.innerWidth / window.innerHeight; menuCam.updateProjectionMatrix();
}

function setClouds(count, y0, y1) {
  const rng = makeRng(count * 7 + 3), dummy = new THREE.Object3D();
  cloudData = []; let n = 0;
  for (let c = 0; c < count && n < 250; c++) {
    const cx = (rng() - 0.5) * 1900, cz = (rng() - 0.5) * 1900, cy = y0 + rng() * (y1 - y0), big = 10 + rng() * 14;
    const puffs = 4 + Math.floor(rng() * 4);
    for (let p = 0; p < puffs && n < 250; p++, n++) {
      cloudData.push({ x: cx + (rng() - 0.5) * big * 2.4, y: cy + (rng() - 0.3) * big * 0.5, z: cz + (rng() - 0.5) * big, s: big * (0.55 + rng() * 0.6) });
    }
  }
  cloudMesh.count = n;
  cloudData.forEach((d, i) => { dummy.position.set(d.x, d.y, d.z); dummy.scale.set(d.s * 1.3, d.s * 0.65, d.s); dummy.updateMatrix(); cloudMesh.setMatrixAt(i, dummy.matrix); });
  cloudMesh.instanceMatrix.needsUpdate = true;
}
const _cd = new THREE.Object3D();
function updateEnv(dt, t) {
  // เมฆลอยช้าๆ
  for (let i = 0; i < cloudData.length; i++) {
    const d = cloudData[i]; d.x += dt * 3; if (d.x > 950) d.x -= 1900;
    _cd.position.set(d.x, d.y, d.z); _cd.scale.set(d.s * 1.3, d.s * 0.65, d.s); _cd.updateMatrix(); cloudMesh.setMatrixAt(i, _cd.matrix);
  }
  cloudMesh.instanceMatrix.needsUpdate = true;
  // แสงแดด + เงาตามโดรน
  sunLight.position.copy(focus).addScaledVector(sunDir, 400);
  sunLight.target.position.copy(focus);
  // ฝน
  if (game.rain) {
    rainPts.position.set(focus.x, Math.max(0, focus.y - 30), focus.z);
    const a = rainPts.geometry.attributes.position;
    for (let i = 0; i < a.count; i++) { let y = a.getY(i) - 48 * dt; if (y < 0) y += 70; a.setY(i, y); }
    a.needsUpdate = true;
  }
  for (const b of LV.blinkers) b.visible = Math.sin(t * 3 + b.userData.ph) > 0.4;
  for (const fn of LV.updaters) fn(dt, t);
}

const TOD_SET = {
  sunset: { top: 0x23315f, bottom: 0xff9a5c, fog: 0xe5a07a, sun: 0xffb27a, sunI: 1.0, hs: 0xffc2a0, hg: 0x4a3a4a, hI: 0.55, elev: 0.09, az: -0.9, cloud: 0xffc9ad, win: 0.45, dens: 1.0, moon: 0xffd08a },
  night: { top: 0x020414, bottom: 0x0f1c3c, fog: 0x0b1430, sun: 0x9fb4ff, sunI: 0.3, hs: 0x4a5a8a, hg: 0x0a0c14, hI: 0.4, elev: 0.6, az: 0.7, cloud: 0x2c3552, win: 1.0, dens: 1.15, moon: 0xdfe6ff }
};
function applyTod() {
  const d = LV.def.sky;
  const T = game.tod === 'day'
    ? { top: d.top, bottom: d.bottom, fog: d.fog, sun: 0xfff3dd, sunI: 1.0, hs: d.hs || 0xdfeeff, hg: d.hg || 0x5b5a45, hI: 0.58, elev: 0.9, az: 0.55, cloud: 0xffffff, win: 0.0, dens: 1.0, moon: 0xfff0c0 }
    : TOD_SET[game.tod];
  skyMat.uniforms.top.value.setHex(T.top); skyMat.uniforms.bottom.value.setHex(T.bottom);
  skyMat.uniforms.sunCol.value.setHex(T.moon);
  scene.fog.color.setHex(T.fog); scene.fog.density = d.fogD * T.dens;
  sunLight.color.setHex(T.sun); sunLight.intensity = T.sunI;
  hemiLight.color.setHex(T.hs); hemiLight.groundColor.setHex(T.hg); hemiLight.intensity = T.hI;
  sunDir.set(Math.cos(T.elev) * Math.sin(T.az), Math.sin(T.elev), Math.cos(T.elev) * Math.cos(T.az)).normalize();
  skyMat.uniforms.sunDir.value.copy(sunDir);
  starPts.visible = game.tod === 'night';
  cloudMesh.material.color.setHex(T.cloud);
  cloudMesh.material.emissiveIntensity = game.tod === 'night' ? 0.05 : 0.3;
  LV.nightMats.forEach(m => { m.emissiveIntensity = T.win * (m.userData.nightI || 1); });
  LV.nightObjs.forEach(o => { o.visible = game.tod !== 'day'; });
  const icon = { day: '☀️', sunset: '🌅', night: '🌙' }[game.tod];
  const b = $('b-tod'); if (b) b.textContent = icon;
}

/* ---------- ตัวช่วยสร้างฉาก ---------- */
function textSprite(text, color = '#ffffff', bg = 'rgba(0,0,0,0.55)', scale = 3) {
  const c = document.createElement('canvas'); c.width = c.height = 128;
  const x = c.getContext('2d');
  x.fillStyle = bg; x.beginPath(); x.arc(64, 64, 58, 0, Math.PI * 2); x.fill();
  x.fillStyle = color; x.font = 'bold 64px Prompt, sans-serif'; x.textAlign = 'center'; x.textBaseline = 'middle';
  x.fillText(text, 64, 70);
  const sp = new THREE.Sprite(new THREE.SpriteMaterial({ map: new THREE.CanvasTexture(c), transparent: true, depthWrite: false }));
  sp.scale.set(scale, scale, 1); return sp;
}

function makePad(g, x, y, z) {
  mesh(new THREE.CylinderGeometry(3.4, 3.6, 0.2, 40), mat(0x2d333b, { roughness: 0.8 }), x, y + 0.1, z, g).receiveShadow = true;
  const ring = mesh(new THREE.RingGeometry(2.6, 3.0, 40), new THREE.MeshBasicMaterial({ color: 0xfacc15, side: THREE.DoubleSide }), x, y + 0.22, z, g);
  ring.rotation.x = -Math.PI / 2;
  const w = new THREE.MeshBasicMaterial({ color: 0xffffff });
  const h = new THREE.Group(); h.position.set(x, y + 0.22, z); g.add(h);
  mesh(new THREE.BoxGeometry(0.35, 0.02, 2.2), w, -0.7, 0, 0, h);
  mesh(new THREE.BoxGeometry(0.35, 0.02, 2.2), w, 0.7, 0, 0, h);
  mesh(new THREE.BoxGeometry(1.4, 0.02, 0.35), w, 0, 0, 0, h);
}

// ต้นไม้แบบ Instanced (วาดทีละเยอะๆ ได้ไม่หน่วง)  type: 'round' | 'pine'
function instTrees(g, list, type) {
  if (!list.length) return;
  const n = list.length, dummy = new THREE.Object3D(), col = new THREE.Color();
  const trunkGeo = new THREE.CylinderGeometry(0.25, 0.4, 1, 6); trunkGeo.translate(0, 0.5, 0);
  const crownGeo = type === 'pine' ? new THREE.ConeGeometry(1, 1, 7) : new THREE.IcosahedronGeometry(1, 0);
  if (type === 'pine') crownGeo.translate(0, 0.5, 0);
  const trunks = new THREE.InstancedMesh(trunkGeo, mat(0x6b4a2f, { roughness: 1 }), n);
  const crowns = new THREE.InstancedMesh(crownGeo, new THREE.MeshStandardMaterial({ color: 0xffffff, roughness: 0.9, flatShading: true }), n);
  list.forEach((t, i) => {
    const s = t.s;
    dummy.rotation.set(0, t.r || 0, 0);
    dummy.position.set(t.x, t.y, t.z); dummy.scale.set(s, (type === 'pine' ? 2.5 : 3) * s, s); dummy.updateMatrix(); trunks.setMatrixAt(i, dummy.matrix);
    if (type === 'pine') { dummy.position.set(t.x, t.y + 1.8 * s, t.z); dummy.scale.set(2.6 * s, 8 * s, 2.6 * s); }
    else { dummy.position.set(t.x, t.y + 3.6 * s, t.z); dummy.scale.set(2.4 * s, 2.1 * s, 2.4 * s); }
    dummy.updateMatrix(); crowns.setMatrixAt(i, dummy.matrix);
    col.setHex(t.c || 0x3f8f3a); crowns.setColorAt(i, col);
  });
  trunks.castShadow = crowns.castShadow = true; crowns.receiveShadow = true;
  g.add(trunks); g.add(crowns);
}

// ต้นมะพร้าว
function palm(g, x, y, z, h, rng) {
  const grp = new THREE.Group(); grp.position.set(x, y, z); grp.rotation.y = rng() * 6; g.add(grp);
  const lean = 0.15 + rng() * 0.2, trunkMat = mat(0x8b6b45, { roughness: 1 }), segs = 4;
  let px = 0, py = 0;
  for (let i = 0; i < segs; i++) {
    const sh = h / segs, a = lean * (i + 1) / segs;
    const m = mesh(new THREE.CylinderGeometry(0.22, 0.3, sh, 7), trunkMat, px + Math.sin(a) * sh / 2, py + Math.cos(a) * sh / 2, 0, grp);
    m.rotation.z = -a; m.castShadow = true;
    px += Math.sin(a) * sh; py += Math.cos(a) * sh;
  }
  const leafMat = mat(0x2f8a3a, { roughness: 0.9, side: THREE.DoubleSide });
  for (let i = 0; i < 7; i++) {
    const piv = new THREE.Group(); piv.position.set(px, py, 0); piv.rotation.y = i / 7 * Math.PI * 2; grp.add(piv);
    const leaf = mesh(new THREE.BoxGeometry(0.7, 0.06, 3.4), leafMat, 0, -0.5, 1.6, piv);
    leaf.rotation.x = 0.55; leaf.castShadow = true;
  }
  for (let i = 0; i < 3; i++) mesh(new THREE.SphereGeometry(0.2, 6, 6), mat(0x5a3b1c), px + Math.cos(i * 2) * 0.25, py - 0.25, Math.sin(i * 2) * 0.25, grp);
  return grp;
}

/* ---------- ห่วง ---------- */
function buildRings(L) {
  const pts = L.def.rings.map(r => new V3(r.x, L.ground(r.x, r.z) + r.h, r.z));
  const tor = new THREE.TorusGeometry(RING_R, 0.42, 12, 48);
  const disc = new THREE.CircleGeometry(RING_R - 0.3, 40);
  pts.forEach((p, i) => {
    const last = i === pts.length - 1, col = last ? 0xffc400 : 0xff2d95;
    const grp = new THREE.Group(); grp.position.copy(p);
    const prev = i === 0 ? L.spawn.clone().setY(p.y) : pts[i - 1];
    const next = last ? p.clone().add(p.clone().sub(prev)) : pts[i + 1];
    const dir = next.clone().sub(prev); dir.y *= 0.3;
    grp.lookAt(p.clone().add(dir));
    const m = new THREE.MeshStandardMaterial({ color: col, emissive: col, emissiveIntensity: 0.5, roughness: 0.35, transparent: true, opacity: 1 });
    const torus = new THREE.Mesh(tor, m); grp.add(torus);
    const dsk = new THREE.Mesh(disc, new THREE.MeshBasicMaterial({ color: col, transparent: true, opacity: 0.16, side: THREE.DoubleSide, depthWrite: false }));
    grp.add(dsk);
    const label = textSprite(last ? '★' : String(i + 1), last ? '#ffd400' : '#ffffff');
    label.position.set(0, RING_R + 1.9, 0); grp.add(label);
    L.group.add(grp);
    L.rings.push({ grp, torus, mat: m, disc: dsk, label, pos: p, color: col });
  });
}
function popRing(R) {   // เอฟเฟกต์ห่วงแตกเป็นวงขยาย
  const m = new THREE.Mesh(R.torus.geometry, new THREE.MeshBasicMaterial({ color: 0x7dffb2, transparent: true, opacity: 0.9, depthWrite: false }));
  m.position.copy(R.pos); m.quaternion.copy(R.grp.quaternion); LV.group.add(m);
  LV.fx.push({ m, t: 0 });
}
function updateFx(dt) {
  for (let i = LV.fx.length - 1; i >= 0; i--) {
    const f = LV.fx[i]; f.t += dt;
    f.m.scale.setScalar(1 + f.t * 2.4); f.m.material.opacity = Math.max(0, 0.9 - f.t * 1.8);
    if (f.t > 0.5) { LV.group.remove(f.m); f.m.material.dispose(); LV.fx.splice(i, 1); }
  }
}

function loadLevel(id) {
  const def = LEVELS.find(l => l.id === id) || LEVELS[0];
  if (LV.group) { scene.remove(LV.group); LV.group.traverse(o => { if (o.geometry) o.geometry.dispose(); }); }
  const g = new THREE.Group(); scene.add(g);
  LV = { def, id: def.id, group: g, colliders: [], updaters: [], nightMats: [], nightObjs: [], blinkers: [], rings: [], fx: [], ground: def.ground, bounds: def.bounds };
  def.build(g, LV, makeRng(def.seed));
  LV.spawn = new V3(def.spawn.x, def.ground(def.spawn.x, def.spawn.z), def.spawn.z);
  makePad(g, LV.spawn.x, LV.spawn.y, LV.spawn.z);
  buildRings(LV);
  const lm = def.landmark;
  LV.landmark = { name: lm.name, pos: new V3(lm.x, def.ground(lm.x, lm.z) + lm.dy, lm.z), radius: lm.radius };
  setClouds(def.clouds, def.cloudY[0], def.cloudY[1]);
  applyTod();
  game.levelId = def.id;
}

/* =====================================================================
   ส่วนที่ 3: ด่านเมืองตึกสูง + ด่านทะเลอันดามัน
   ===================================================================== */
let _cityTex = null;
function cityTextures() {
  if (_cityTex) return _cityTex;
  const aniso = Math.min(8, renderer.capabilities.getMaxAnisotropy());
  const mk = (c, rep) => { const t = new THREE.CanvasTexture(c); t.wrapS = t.wrapT = THREE.RepeatWrapping; t.anisotropy = aniso; if (rep) t.repeat.set(rep, rep); return t; };
  // ถนน 1 บล็อก = 60 เมตร (ถนนกว้าง 14 ม. + ทางเท้า)
  const c = document.createElement('canvas'); c.width = c.height = 256; const x = c.getContext('2d');
  x.fillStyle = '#7b8088'; x.fillRect(0, 0, 256, 256);
  x.fillStyle = '#c3c7cc'; [[0, 0, 256, 43], [0, 213, 256, 43], [0, 0, 43, 256], [213, 0, 43, 256]].forEach(r => x.fillRect(...r));
  x.fillStyle = '#35383e'; [[0, 0, 256, 30], [0, 226, 256, 30], [0, 0, 30, 256], [226, 0, 30, 256]].forEach(r => x.fillRect(...r));
  x.fillStyle = '#f5d142';
  for (let p = 50; p < 206; p += 22) { x.fillRect(p, 0, 12, 2); x.fillRect(p, 254, 12, 2); x.fillRect(0, p, 2, 12); x.fillRect(254, p, 2, 12); }
  x.fillStyle = '#e8e8e8';
  for (let k = 0; k < 5; k++) {
    [32, 214].forEach(a => { x.fillRect(a, 2 + k * 6, 10, 3.5); x.fillRect(a, 228 + k * 5.3, 10, 3); x.fillRect(2 + k * 6, a, 3.5, 10); x.fillRect(228 + k * 5.3, a, 3, 10); });
  }
  // ผนังตึก: map = หน้าต่าง, emissive = ไฟในห้องตอนกลางคืน (8x8 ช่อง = กว้าง 32 ม. สูง 28 ม.)
  const facade = kind => {
    const m = document.createElement('canvas'); m.width = m.height = 256; const a = m.getContext('2d');
    const e = document.createElement('canvas'); e.width = e.height = 256; const b = e.getContext('2d');
    a.fillStyle = '#ffffff'; a.fillRect(0, 0, 256, 256); b.fillStyle = '#000'; b.fillRect(0, 0, 256, 256);
    for (let i = 0; i < 8; i++) for (let j = 0; j < 8; j++) {
      const X = i * 32, Y = j * 32;
      if (kind === 0) { a.fillStyle = Math.random() < 0.15 ? '#5f7088' : '#3b4a60'; a.fillRect(X + 6, Y + 7, 20, 19); a.fillStyle = 'rgba(255,255,255,.28)'; a.fillRect(X + 6, Y + 7, 20, 4); }
      else { a.fillStyle = '#35506d'; a.fillRect(X, Y + 8, 32, 18); a.fillStyle = '#5b7ea3'; a.fillRect(X + 15, Y + 8, 2, 18); }
      if (Math.random() < 0.45) { b.fillStyle = ['#ffe08a', '#fff1c2', '#ffcf73', '#cfe8ff'][Math.floor(Math.random() * 4)]; if (kind === 0) b.fillRect(X + 6, Y + 7, 20, 19); else b.fillRect(X, Y + 8, 32, 18); }
    }
    return { map: mk(m), em: mk(e) };
  };
  _cityTex = { road: mk(c, 27), f0: facade(0), f1: facade(1) };
  return _cityTex;
}

// กล่องตึกพร้อมหน้าต่าง + ใส่ตัวชน
function tower(g, L, material, x, y0, z, w, h, d) {
  const geo = new THREE.BoxGeometry(w, h, d), uv = geo.attributes.uv;
  const dims = [[d, h], [d, h], [0, 0], [0, 0], [w, h], [w, h]];
  for (let f = 0; f < 6; f++) for (let i = 0; i < 4; i++) { const k = f * 4 + i; uv.setXY(k, uv.getX(k) * dims[f][0] / 32, uv.getY(k) * dims[f][1] / 28); }
  const m = mesh(geo, material, x, y0 + h / 2, z, g); m.castShadow = m.receiveShadow = true;
  L.colliders.push({ t: 'box', x0: x - w / 2, x1: x + w / 2, z0: z - d / 2, z1: z + d / 2, y0, y1: y0 + h });
  return m;
}
function blinker(g, L, x, y, z) {
  const b = mesh(new THREE.SphereGeometry(0.6, 8, 8), new THREE.MeshBasicMaterial({ color: 0xff1a1a }), x, y, z, g);
  b.userData.ph = Math.random() * 6; L.blinkers.push(b); return b;
}

function buildCity(g, L, rng) {
  const tex = cityTextures();
  const ground = mesh(new THREE.PlaneGeometry(1620, 1620), new THREE.MeshStandardMaterial({ map: tex.road, roughness: 0.95 }), 0, 0, 0, g);
  ground.rotation.x = -Math.PI / 2; ground.receiveShadow = true;
  const far = mesh(new THREE.PlaneGeometry(5000, 5000), mat(0x56694a, { roughness: 1 }), 0, -0.1, 0, g); far.rotation.x = -Math.PI / 2;

  const mkMat = (kind, hex) => { const m = new THREE.MeshStandardMaterial({ color: hex, map: tex['f' + kind].map, emissiveMap: tex['f' + kind].em, emissive: 0xffffff, emissiveIntensity: 0, roughness: kind ? 0.35 : 0.7, metalness: kind ? 0.4 : 0.05 }); L.nightMats.push(m); return m; };
  const mats = [[0xe8e4dc, 0xc9d3dd, 0xd9c7a8, 0xb8c4b0, 0xf2f2f2, 0xe0b8a0].map(h => mkMat(0, h)), [0x9fc3df, 0x7fa6c8, 0xa7d0dc, 0xb9c6d6].map(h => mkMat(1, h))];
  const roofMat = mat(0x5b6068, { roughness: 0.9 }), acMat = mat(0x9aa1a9, { roughness: 0.6 });
  const PARKS = new Set(['-2,1', '3,2', '-4,-3', '1,4', '-1,-4', '-5,2', '5,-1', '-3,5', '2,-6']);
  const trees = [];

  const building = (x, z, w, d, h) => {
    const kind = h > 55 && rng() < 0.6 ? 1 : 0;
    const list = mats[kind];
    tower(g, L, list[Math.floor(rng() * list.length)], x, 0, z, w, h, d);
    let top = h;
    if (h > 80 && rng() < 0.6) { const w2 = w * 0.68, d2 = d * 0.68, h2 = h * 0.22; tower(g, L, list[Math.floor(rng() * list.length)], x, h, z, w2, h2, d2); top += h2; w = w2; d = d2; }
    mesh(new THREE.BoxGeometry(w - 1, 0.6, d - 1), roofMat, x, top + 0.3, z, g).receiveShadow = true;
    const r = rng();
    if (top > 45 && r < 0.45) { mesh(new THREE.CylinderGeometry(0.2, 0.3, 12, 6), acMat, x, top + 6, z, g); blinker(g, L, x, top + 12.3, z); }
    else if (top > 60 && r < 0.7) {
      mesh(new THREE.CylinderGeometry(6, 6, 0.4, 24), mat(0x2d333b), x, top + 0.8, z, g);
      const hm = new THREE.MeshBasicMaterial({ color: 0xffffff });
      mesh(new THREE.BoxGeometry(0.8, 0.1, 5), hm, x - 1.5, top + 1.05, z, g); mesh(new THREE.BoxGeometry(0.8, 0.1, 5), hm, x + 1.5, top + 1.05, z, g); mesh(new THREE.BoxGeometry(3, 0.1, 0.8), hm, x, top + 1.05, z, g);
    } else { for (let k = 0; k < 3; k++) mesh(new THREE.BoxGeometry(2.5, 1.6, 2.5), acMat, x + (rng() - 0.5) * (w - 5), top + 1.1, z + (rng() - 0.5) * (d - 5), g).castShadow = true; }
  };

  for (let i = -6; i <= 6; i++) for (let j = -6; j <= 6; j++) {
    const cx = i * 60, cz = j * 60, dist = Math.hypot(cx, cz);
    if (dist > 400) continue;
    if (i === 0 && j === 0) {   // ลานกลางเมือง (จุดขึ้นบิน)
      mesh(new THREE.BoxGeometry(40, 0.1, 40), mat(0xa9a397, { roughness: 0.95 }), 0, 0.05, 0, g).receiveShadow = true;
      mesh(new THREE.CylinderGeometry(5, 5.4, 0.8, 32), mat(0xbfc5cc), 0, 0.4, -12, g);
      mesh(new THREE.CylinderGeometry(4.4, 4.4, 0.1, 32), mat(0x3aa0d8, { roughness: 0.1, metalness: 0.3 }), 0, 0.8, -12, g);
      mesh(new THREE.CylinderGeometry(0.6, 0.9, 3, 12), mat(0xbfc5cc), 0, 1.5, -12, g);
      L.colliders.push({ t: 'cyl', x: 0, z: -12, r: 5.4, y0: 0, y1: 3 });
      [[-16, -16], [16, -16], [-16, 16], [16, 16]].forEach(([a, b]) => trees.push({ x: a, y: 0, z: b, s: 1.1, c: 0x3f8f3a }));
      continue;
    }
    if (i === 4 && j === -4) continue;   // ที่ของตึกระฟ้า
    if (PARKS.has(i + ',' + j)) {
      mesh(new THREE.BoxGeometry(40, 0.1, 40), mat(0x5c9a45, { roughness: 1 }), cx, 0.05, cz, g).receiveShadow = true;
      if (rng() < 0.5) mesh(new THREE.CylinderGeometry(7, 7, 0.12, 24), mat(0x3b8fd0, { roughness: 0.15, metalness: 0.2 }), cx + 5, 0.08, cz + 4, g);
      for (let k = 0; k < 16; k++) trees.push({ x: cx + (rng() - 0.5) * 36, y: 0, z: cz + (rng() - 0.5) * 36, s: 0.8 + rng() * 0.6, c: [0x3f8f3a, 0x4c9e3f, 0x2f7a33][k % 3] });
      continue;
    }
    const down = Math.max(0, 1 - dist / 330);
    if (rng() < 0.38) {
      const w = 22 + rng() * 12, d = 22 + rng() * 12;
      building(cx, cz, w, d, 25 + rng() * 40 + down * down * 150 * rng());
    } else {
      for (const sx of [-1, 1]) for (const sz of [-1, 1]) {
        if (rng() < 0.12) { trees.push({ x: cx + sx * 10, y: 0, z: cz + sz * 10, s: 1, c: 0x3f8f3a }); continue; }
        building(cx + sx * 10, cz + sz * 10, 11 + rng() * 6, 11 + rng() * 6, 10 + rng() * 30 + down * 75 * rng());
      }
    }
  }

  // ตึกระฟ้าใจกลางเมือง (สถานที่ถ่ายรูป)
  const tx = 240, tz = -240;
  tower(g, L, mats[0][4], tx, 0, tz, 36, 14, 36);
  tower(g, L, mats[1][1], tx, 14, tz, 24, 150, 24);
  tower(g, L, mats[1][0], tx, 164, tz, 18, 36, 18);
  mesh(new THREE.BoxGeometry(19, 1.2, 19), mat(0xd4af37, { metalness: 0.8, roughness: 0.3 }), tx, 200.6, tz, g);
  mesh(new THREE.CylinderGeometry(0.4, 1.6, 38, 8), mat(0xdfe3e8, { metalness: 0.8, roughness: 0.25 }), tx, 220, tz, g);
  L.colliders.push({ t: 'cyl', x: tx, z: tz, r: 1.6, y0: 200, y1: 239 });
  blinker(g, L, tx, 239.5, tz);
  [[-8, -8], [8, -8], [-8, 8], [8, 8]].forEach(([a, b]) => blinker(g, L, tx + a, 201.8, tz + b));

  instTrees(g, trees, 'round');

  // รถวิ่งบนถนน (ชิดซ้ายแบบเมืองไทย)
  const N = 70, lanes = []; for (let k = -6; k <= 7; k++) lanes.push(k * 60 - 30);
  const carBody = new THREE.BoxGeometry(2, 1.2, 4.2); carBody.translate(0, 0.8, 0);
  const carTop = new THREE.BoxGeometry(1.8, 0.8, 2.2); carTop.translate(0, 1.8, 0.2);
  const bodies = new THREE.InstancedMesh(carBody, new THREE.MeshStandardMaterial({ color: 0xffffff, roughness: 0.35, metalness: 0.4 }), N);
  const tops = new THREE.InstancedMesh(carTop, mat(0x1e2733, { roughness: 0.2, metalness: 0.6 }), N);
  const cars = [], cc = new THREE.Color(), dm = new THREE.Object3D();
  const carCols = [0xef4444, 0xf8fafc, 0x3b82f6, 0xfacc15, 0x111827, 0x22c55e, 0xf97316, 0x9ca3af, 0xec4899];
  for (let i = 0; i < N; i++) {
    cars.push({ ax: rng() < 0.5 ? 'x' : 'z', lane: lanes[Math.floor(rng() * lanes.length)], p: (rng() - 0.5) * 800, v: (rng() < 0.5 ? -1 : 1) * (8 + rng() * 7) });
    cc.setHex(carCols[i % carCols.length]); bodies.setColorAt(i, cc);
  }
  bodies.castShadow = tops.castShadow = true; g.add(bodies); g.add(tops);
  L.updaters.push(dt => {
    for (let i = 0; i < N; i++) {
      const c = cars[i]; c.p += c.v * dt; if (c.p > 400) c.p -= 800; if (c.p < -400) c.p += 800;
      const s = c.v > 0 ? 1 : -1;
      if (c.ax === 'z') { dm.position.set(c.lane + s * 3.5, 0, c.p); dm.rotation.set(0, s > 0 ? 0 : Math.PI, 0); }
      else { dm.position.set(c.p, 0, c.lane - s * 3.5); dm.rotation.set(0, s > 0 ? Math.PI / 2 : -Math.PI / 2, 0); }
      dm.updateMatrix(); bodies.setMatrixAt(i, dm.matrix); tops.setMatrixAt(i, dm.matrix);
    }
    bodies.instanceMatrix.needsUpdate = tops.instanceMatrix.needsUpdate = true;
  });
}

/* ---------- ทะเลอันดามัน ---------- */
const SEA_KARSTS = [
  [-90, -60, 14, 45], [60, -130, 12, 55], [50, -274, 10, 48], [50, -226, 9, 40], [-120, -200, 18, 60],
  [-80, -285, 14, 50], [0, -335, 20, 70], [140, -300, 16, 45], [215, -170, 14, 55], [205, -60, 16, 40],
  [-160, -10, 16, 35], [-200, -120, 12, 50], [235, -270, 10, 35], [-45, -255, 11, 42], [95, -340, 12, 50],
  [-260, -240, 22, 65], [300, -120, 20, 60], [-300, 40, 18, 45], [120, 160, 16, 40]
];
function seaGround(x, z) {
  const d = Math.hypot(x, z - 60);
  if (d < 50) { const dh = Math.hypot(x, z - 75); return dh < 22 ? 1 + 12 * Math.sqrt(1 - (dh / 22) ** 2) : 1.0; }
  if (Math.hypot(x - 200, z - 60) < 14) return 1.0;
  return 0.4;
}
function karstGeo(r, h) {
  const geo = new THREE.CylinderGeometry(r * 0.72, r, h, 12, 6), p = geo.attributes.position;
  for (let i = 0; i < p.count; i++) {
    const x = p.getX(i), y = p.getY(i), z = p.getZ(i);
    if (Math.hypot(x, z) < 0.01) continue;
    const n = 1 + 0.12 * Math.sin(x * 0.9 + y * 0.4) * Math.cos(z * 0.8 - y * 0.3) + 0.06 * Math.sin(y * 1.3 + x);
    p.setX(i, x * n); p.setZ(i, z * n);
  }
  geo.translate(0, h / 2, 0); geo.computeVertexNormals();
  return geo;
}
function longtail(g, rng) {
  const grp = new THREE.Group(); g.add(grp);
  const s = new THREE.Shape();
  s.moveTo(-4, 1.0); s.lineTo(-3.4, 0); s.lineTo(3, 0); s.quadraticCurveTo(4.6, 0.3, 5.4, 2.3); s.lineTo(4.7, 1.1); s.lineTo(-4, 1.1);
  const hull = new THREE.ExtrudeGeometry(s, { depth: 1.5, bevelEnabled: false }); hull.translate(0, -0.3, -0.75);
  mesh(hull, mat([0x8b5a2b, 0x2f6fb0, 0x9b2c2c][Math.floor(rng() * 3)], { roughness: 0.8 }), 0, 0, 0, grp).castShadow = true;
  mesh(new THREE.BoxGeometry(7, 0.1, 1.3), mat(0x5a3b1c), -0.3, 0.6, 0, grp);
  [0xff4fa3, 0xffd400, 0x22c55e].forEach((c, i) => mesh(new THREE.BoxGeometry(0.25, 0.5, 0.25), mat(c, { emissive: c, emissiveIntensity: 0.2 }), 5.2 - i * 0.2, 1.9 - i * 0.25, 0, grp));
  const canopy = mat(0xf1f5f9, { side: THREE.DoubleSide });
  mesh(new THREE.BoxGeometry(3.4, 0.08, 1.7), canopy, -0.5, 2.5, 0, grp);
  [[-2, -0.7], [-2, 0.7], [1, -0.7], [1, 0.7]].forEach(([a, b]) => mesh(new THREE.CylinderGeometry(0.04, 0.04, 1.9, 5), mat(0x5a3b1c), a, 1.55, b, grp));
  mesh(new THREE.BoxGeometry(0.9, 0.7, 0.7), mat(0x374151, { metalness: 0.6 }), -4.2, 1.3, 0, grp);
  const pole = mesh(new THREE.CylinderGeometry(0.06, 0.06, 4.5, 6), mat(0x6b7280, { metalness: 0.6 }), -6.2, 0.4, 0, grp);
  pole.rotation.z = Math.PI / 2 - 0.35;
  return grp;
}
function buildSea(g, L, rng) {
  // น้ำทะเลมีคลื่น (สีฟ้าใสใกล้เกาะ สีน้ำเงินเข้มไกลเกาะ)
  const islands = [[0, 60, 50], [200, 60, 14], [-150, -120, 6]].concat(SEA_KARSTS.map(k => [k[0], k[1], k[2]]));
  const wg = new THREE.PlaneGeometry(2600, 2600, 110, 110); wg.rotateX(-Math.PI / 2);
  const wp = wg.attributes.position, cols = [], shallow = new THREE.Color(0x2fd3c8), deep = new THREE.Color(0x0b5fa5), tmp = new THREE.Color();
  for (let i = 0; i < wp.count; i++) {
    const x = wp.getX(i), z = wp.getZ(i);
    let m = 1e9; for (const s of islands) m = Math.min(m, Math.hypot(x - s[0], z - s[1]) - s[2]);
    tmp.copy(deep).lerp(shallow, 1 - smooth(0, 70, m)); cols.push(tmp.r, tmp.g, tmp.b);
  }
  wg.setAttribute('color', new THREE.Float32BufferAttribute(cols, 3));
  const water = mesh(wg, new THREE.MeshStandardMaterial({ vertexColors: true, flatShading: true, roughness: 0.25, metalness: 0.15 }), 0, 0, 0, g);
  water.receiveShadow = true;
  L.updaters.push((dt, t) => {
    for (let i = 0; i < wp.count; i++) { const x = wp.getX(i), z = wp.getZ(i); wp.setY(i, Math.sin(x * 0.045 + t * 1.1) * 0.35 + Math.cos(z * 0.05 + t * 0.9) * 0.3); }
    wp.needsUpdate = true;
  });

  // เกาะหลัก (จุดขึ้นบิน) มีหาดทราย เนินเขา ต้นมะพร้าว ร่ม และสะพานท่าเรือ
  const sand = mat(0xecd9a6, { roughness: 1 });
  mesh(new THREE.CylinderGeometry(50, 58, 3, 56), sand, 0, -0.5, 60, g).receiveShadow = true;
  const hill = mesh(new THREE.SphereGeometry(22, 28, 16), mat(0x4c9a3f, { roughness: 1, flatShading: true }), 0, 1, 75, g);
  hill.scale.set(1, 12 / 22, 1); hill.receiveShadow = true;
  const trees = [];
  for (let k = 0; k < 12; k++) { const a = rng() * 6.28, r = rng() * 15; trees.push({ x: Math.cos(a) * r, y: seaGround(Math.cos(a) * r, 75 + Math.sin(a) * r) - 0.5, z: 75 + Math.sin(a) * r, s: 0.9 + rng() * 0.5, c: 0x2f7a33 }); }
  instTrees(g, trees, 'round');
  for (let k = 0; k < 18; k++) {
    const a = k / 18 * Math.PI * 2 + rng() * 0.2, r = 38 + rng() * 8, x = Math.sin(a) * r, z = 60 + Math.cos(a) * r;
    if (Math.hypot(x, z - 25) < 12 || (Math.abs(x + 25) < 4 && z < 30)) continue;
    palm(g, x, 1, z, 7 + rng() * 3, rng);
  }
  [[10, 28, 0xef4444], [14, 36, 0x3b82f6], [-12, 30, 0xfacc15]].forEach(([x, z, c]) => {
    mesh(new THREE.CylinderGeometry(0.06, 0.06, 2.6, 6), mat(0xffffff), x, 2.3, z, g);
    mesh(new THREE.ConeGeometry(1.8, 0.8, 10), mat(c, { roughness: 0.8 }), x, 3.6, z, g).castShadow = true;
  });
  const wood = mat(0x8a6a48, { roughness: 1 });
  mesh(new THREE.BoxGeometry(3, 0.3, 34), wood, -25, 1.3, 2, g).castShadow = true;
  for (let k = 0; k < 6; k++) { mesh(new THREE.CylinderGeometry(0.2, 0.2, 3, 6), wood, -26.3, 0, -12 + k * 6, g); mesh(new THREE.CylinderGeometry(0.2, 0.2, 3, 6), wood, -23.7, 0, -12 + k * 6, g); }

  // เกาะหินปูนแบบพังงา
  const rock = mat(0x8a8d84, { roughness: 1, flatShading: true }), green = mat(0x3f7d3a, { roughness: 1, flatShading: true });
  SEA_KARSTS.forEach(([x, z, r, h]) => {
    mesh(karstGeo(r, h), rock, x, -2, z, g).castShadow = true;
    const cap = mesh(new THREE.SphereGeometry(r * 0.78, 10, 6, 0, Math.PI * 2, 0, Math.PI / 2), green, x, h - 2.6, z, g);
    cap.scale.y = 0.5;
    L.colliders.push({ t: 'cyl', x, z, r: r * 1.1, y0: -5, y1: h - 2 + r * 0.35 });
  });
  // เกาะตะปู (สถานที่ถ่ายรูป) — ฐานเล็ก ยอดใหญ่
  const tapu = new THREE.CylinderGeometry(8, 3.2, 30, 12, 6); tapu.translate(0, 15, 0);
  const tp = tapu.attributes.position;
  for (let i = 0; i < tp.count; i++) { const x = tp.getX(i), y = tp.getY(i), z = tp.getZ(i); const n = 1 + 0.1 * Math.sin(y * 0.8 + x) * Math.cos(z * 0.9); tp.setX(i, x * n); tp.setZ(i, z * n); }
  tapu.computeVertexNormals();
  mesh(tapu, mat(0x9c9486, { roughness: 1, flatShading: true }), -150, -2, -120, g).castShadow = true;
  const tcap = mesh(new THREE.SphereGeometry(7.5, 10, 6, 0, Math.PI * 2, 0, Math.PI / 2), green, -150, 27.5, -120, g); tcap.scale.y = 0.45;
  for (let k = 0; k < 4; k++) mesh(new THREE.DodecahedronGeometry(2 + rng() * 1.5), rock, -150 + Math.cos(k * 1.6) * 5, -0.5, -120 + Math.sin(k * 1.6) * 5, g);
  L.colliders.push({ t: 'cyl', x: -150, z: -120, r: 3.6, r2: 8.8, y0: -3, y1: 29.5 });

  // ประภาคาร (ไฟหมุนตอนกลางคืน)
  mesh(new THREE.CylinderGeometry(14, 17, 3, 32), sand, 200, -0.5, 60, g);
  const white = mat(0xf8fafc), red = mat(0xdc2626);
  for (let k = 0; k < 4; k++) mesh(new THREE.CylinderGeometry(2.2 - k * 0.15 - 0.15, 2.2 - k * 0.15, 4, 16), k % 2 ? red : white, 200, 3 + k * 4, 60, g).castShadow = true;
  mesh(new THREE.CylinderGeometry(2.6, 2.6, 0.4, 16), mat(0x1f2937), 200, 17.2, 60, g);
  const lampMat = new THREE.MeshStandardMaterial({ color: 0xfff3c4, emissive: 0xffe08a, emissiveIntensity: 0, roughness: 0.2 });
  lampMat.userData.nightI = 1.5; L.nightMats.push(lampMat);
  mesh(new THREE.CylinderGeometry(1.4, 1.4, 2, 12), lampMat, 200, 18.4, 60, g);
  mesh(new THREE.ConeGeometry(1.9, 1.8, 12), red, 200, 20.3, 60, g);
  const beamG = new THREE.ConeGeometry(6, 70, 16, 1, true); beamG.translate(0, -35, 0); beamG.rotateZ(Math.PI / 2);
  const beam = mesh(beamG, new THREE.MeshBasicMaterial({ color: 0xfff2b0, transparent: true, opacity: 0.16, depthWrite: false, side: THREE.DoubleSide, blending: THREE.AdditiveBlending }), 200, 18.4, 60, g);
  L.nightObjs.push(beam);
  L.updaters.push(dt => { beam.rotation.y += dt * 1.2; });
  L.colliders.push({ t: 'cyl', x: 200, z: 60, r: 2.6, y0: 0, y1: 21.2 });
  for (let k = 0; k < 4; k++) palm(g, 200 + Math.cos(k * 1.7) * 9, 1, 60 + Math.sin(k * 1.7) * 9, 6 + rng() * 2, rng);

  // เรือหางยาววิ่งวน
  [[60, -60, 30], [-80, -150, 26], [150, -20, 34], [-30, -200, 22], [110, -260, 20], [-120, 60, 28]].forEach(([cx, cz, R], i) => {
    const b = longtail(g, rng), w = (i % 2 ? 1 : -1) * (0.12 + rng() * 0.08); let a = rng() * 6.28;
    L.updaters.push((dt, t) => {
      a += w * dt; b.position.set(cx + Math.cos(a) * R, Math.sin(t * 1.5 + i) * 0.15 - 0.1, cz + Math.sin(a) * R);
      const vx = -Math.sin(a) * w, vz = Math.cos(a) * w; b.rotation.set(Math.sin(t * 1.3 + i) * 0.04, Math.atan2(-vz, vx), 0);
    });
  });
}

/* =====================================================================
   ส่วนที่ 4: ด่านภูเขา + ด่านทะเลทราย + รายชื่อด่านทั้งหมด
   ===================================================================== */
function mtnH(x, z) {
  let h = 22 * Math.sin(x * 0.011 + 0.5) * Math.cos(z * 0.009) + 14 * Math.sin(x * 0.023 + 1.3) * Math.sin(z * 0.021 + 0.7) + 6 * Math.sin(x * 0.057 + 2.1) * Math.cos(z * 0.049 + 0.3);
  const d = Math.hypot(x, z);
  h += Math.max(0, d - 360) * 0.5 * (0.75 + 0.25 * Math.sin(Math.atan2(z, x) * 5));
  h += 95 * Math.exp(-((x + 160) ** 2 + (z + 280) ** 2) / 4050);     // ยอดดอยที่มีเจดีย์
  return h * smooth(22, 95, Math.hypot(x, z - 10));                   // ทุ่งหญ้าเรียบตรงจุดขึ้นบิน
}
function mtnGround(x, z) { return Math.max(mtnH(x, z), -4); }

// สร้างพื้นดินจากฟังก์ชันความสูง + ระบายสีตามความสูง
function terrainMesh(g, size, seg, hf, colorFn) {
  const geo = new THREE.PlaneGeometry(size, size, seg, seg); geo.rotateX(-Math.PI / 2);
  const p = geo.attributes.position, cols = [], c = new THREE.Color();
  for (let i = 0; i < p.count; i++) {
    const x = p.getX(i), z = p.getZ(i), y = hf(x, z);
    p.setY(i, y);
    const slope = Math.hypot(hf(x + 2, z) - y, hf(x, z + 2) - y) / 2;
    colorFn(c, y, slope, x, z); cols.push(c.r, c.g, c.b);
  }
  geo.setAttribute('color', new THREE.Float32BufferAttribute(cols, 3));
  geo.computeVertexNormals();
  const m = mesh(geo, new THREE.MeshStandardMaterial({ vertexColors: true, roughness: 0.95 }), 0, 0, 0, g);
  m.receiveShadow = true; return m;
}

function hut(g, L, x, z, rot, y) {
  const grp = new THREE.Group(); grp.position.set(x, y, z); grp.rotation.y = rot; g.add(grp);
  const wood = mat(0x8a5a32, { roughness: 1 }), roof = mat(0x7a3b1e, { roughness: 0.9, flatShading: true });
  mesh(new THREE.BoxGeometry(6, 3, 5), wood, 0, 2.5, 0, grp).castShadow = true;
  for (const a of [-2.6, 2.6]) for (const b of [-2.1, 2.1]) mesh(new THREE.CylinderGeometry(0.15, 0.15, 1, 6), wood, a, 0.5, b, grp);
  const r = mesh(new THREE.CylinderGeometry(0.01, 4.4, 3, 4, 1), roof, 0, 5.5, 0, grp); r.rotation.y = Math.PI / 4; r.scale.set(1.15, 1, 0.95); r.castShadow = true;
  L.colliders.push({ t: 'box', x0: x - 3.5, x1: x + 3.5, z0: z - 3.5, z1: z + 3.5, y0: y, y1: y + 6 });
}

function buildMountain(g, L, rng) {
  const grassA = new THREE.Color(0x5f9e3f), grassB = new THREE.Color(0x3f7a30), rockC = new THREE.Color(0x857b70), snow = new THREE.Color(0xf4f7fa), mud = new THREE.Color(0x9b8a62);
  terrainMesh(g, 1500, 150, mtnH, (c, y, s, x, z) => {
    c.copy(grassA).lerp(grassB, 0.5 + 0.5 * Math.sin(x * 0.05) * Math.cos(z * 0.04));
    if (y < -2.5) c.lerp(mud, 0.7);
    c.lerp(rockC, smooth(40, 95, y + s * 40));
    c.lerp(snow, smooth(115, 150, y - s * 20));
  });
  const lake = mesh(new THREE.PlaneGeometry(1600, 1600), new THREE.MeshStandardMaterial({ color: 0x3b82c4, roughness: 0.15, metalness: 0.2 }), 0, -4, 0, g);
  lake.rotation.x = -Math.PI / 2;

  // ป่าสน
  const trees = [];
  for (let k = 0; k < 1400 && trees.length < 750; k++) {
    const x = (rng() - 0.5) * 1100, z = (rng() - 0.5) * 1100, y = mtnH(x, z);
    const s = Math.hypot(mtnH(x + 2, z) - y, mtnH(x, z + 2) - y) / 2;
    if (y < -2 || y > 85 || s > 0.8 || Math.hypot(x, z - 10) < 32 || Math.hypot(x + 160, z + 280) < 40) continue;
    trees.push({ x, y: y - 0.3, z, s: 0.8 + rng() * 0.7, c: [0x2f6b35, 0x3d7a3a, 0x285c30, 0x47843f][k % 4] });
  }
  instTrees(g, trees, 'pine');
  hut(g, L, -26, 22, 0.4, mtnH(-26, 22));
  hut(g, L, 30, 34, -0.6, mtnH(30, 34));

  // เจดีย์ทองบนยอดดอย (สถานที่ถ่ายรูป)
  const x = -160, z = -280, y = mtnH(x, z);
  const white = mat(0xf5f1e6, { roughness: 0.8 }), gold = mat(0xe0b640, { metalness: 0.85, roughness: 0.28 });
  mesh(new THREE.BoxGeometry(24, 9, 24), white, x, y - 3.5, z, g).receiveShadow = true;
  mesh(new THREE.BoxGeometry(16, 2, 16), white, x, y + 2, z, g).castShadow = true;
  mesh(new THREE.BoxGeometry(12, 2, 12), white, x, y + 4, z, g).castShadow = true;
  mesh(new THREE.BoxGeometry(9, 1.6, 9), gold, x, y + 5.8, z, g);
  mesh(new THREE.SphereGeometry(5.2, 28, 18, 0, Math.PI * 2, 0, Math.PI * 0.6), gold, x, y + 6.6, z, g).castShadow = true;
  mesh(new THREE.CylinderGeometry(2.4, 2.4, 1.6, 16), gold, x, y + 12.2, z, g);
  for (let k = 0; k < 6; k++) mesh(new THREE.CylinderGeometry(2.1 - k * 0.3, 2.2 - k * 0.3, 0.8, 16), gold, x, y + 13.5 + k * 0.9, z, g);
  mesh(new THREE.ConeGeometry(0.9, 9, 12), gold, x, y + 22.5, z, g).castShadow = true;
  mesh(new THREE.SphereGeometry(0.45, 10, 8), gold, x, y + 27.2, z, g);
  for (const a of [-6.5, 6.5]) for (const b of [-6.5, 6.5]) mesh(new THREE.ConeGeometry(0.8, 4, 8), gold, x + a, y + 5, z + b, g);
  L.colliders.push({ t: 'cone', x, z, r: 12, y0: y - 1, y1: y + 30 });
}

/* ---------- ทะเลทราย ---------- */
const PYRAMIDS = [[100, -300, 120, 90], [-40, -360, 90, 70], [-150, -330, 60, 45]];
function desertH(x, z) {
  let h = 5 * Math.sin(x * 0.018 + z * 0.012) + 3.5 * Math.sin(z * 0.033 + 1.1) * Math.cos(x * 0.021) + 2 * Math.sin(x * 0.07 + z * 0.05);
  h += Math.max(0, Math.hypot(x, z) - 340) * 0.22 * (0.6 + 0.4 * Math.sin(Math.atan2(z, x) * 3 + 1));
  const dx = Math.max(-210 - x, 0, x - 200), dz = Math.max(-440 - z, 0, z + 200);
  const f = Math.min(smooth(15, 70, Math.hypot(x, z - 10)), smooth(0, 60, Math.hypot(dx, dz)), smooth(24, 50, Math.hypot(x - 120, z + 100)));
  return h * f;
}
function camel(g) {
  const grp = new THREE.Group(), c = mat(0xc19a6b, { roughness: 1 }); g.add(grp);
  mesh(new THREE.BoxGeometry(1.2, 1.2, 3), c, 0, 2.4, 0, grp).castShadow = true;
  mesh(new THREE.SphereGeometry(0.75, 10, 8), c, 0, 3.1, 0.2, grp);
  const neck = mesh(new THREE.BoxGeometry(0.5, 1.8, 0.5), c, 0, 3.2, -1.7, grp); neck.rotation.x = 0.5;
  mesh(new THREE.BoxGeometry(0.55, 0.55, 1.1), c, 0, 4, -2.3, grp);
  const legs = [];
  for (const a of [-0.4, 0.4]) for (const b of [-1.1, 1.1]) { const l = mesh(new THREE.BoxGeometry(0.28, 1.9, 0.28), c, a, 0.95, b, grp); legs.push(l); }
  grp.userData.legs = legs; return grp;
}
function buildDesert(g, L, rng) {
  const sA = new THREE.Color(0xd9b170), sB = new THREE.Color(0xc08c4a), sC = new THREE.Color(0xe6c486);
  terrainMesh(g, 1600, 140, desertH, (c, y, s, x, z) => {
    c.copy(sA).lerp(sB, 0.5 + 0.5 * Math.sin(x * 0.03 + z * 0.02)).lerp(sC, smooth(2, 10, y) * 0.6);
  });
  // พีระมิด 3 องค์
  const cv = document.createElement('canvas'); cv.width = cv.height = 64; const x2 = cv.getContext('2d');
  x2.fillStyle = '#dcbb7c'; x2.fillRect(0, 0, 64, 64); x2.fillStyle = '#b8965a';
  for (let r = 0; r < 8; r++) { x2.fillRect(0, r * 8, 64, 1.5); for (let k = 0; k < 4; k++) x2.fillRect(k * 16 + (r % 2) * 8, r * 8, 1.2, 8); }
  const stone = new THREE.CanvasTexture(cv); stone.wrapS = stone.wrapT = THREE.RepeatWrapping; stone.repeat.set(8, 16);
  const pyrMat = new THREE.MeshStandardMaterial({ map: stone, roughness: 0.95, flatShading: true });
  PYRAMIDS.forEach(([x, z, base, h], i) => {
    const R = base / Math.SQRT2, geo = new THREE.ConeGeometry(R, h, 4, 1); geo.rotateY(Math.PI / 4);
    const p = mesh(geo, pyrMat, x, h / 2 - 1, z, g); p.castShadow = p.receiveShadow = true;
    if (i === 0) mesh(new THREE.ConeGeometry(4.1, 4.4, 4).rotateY(Math.PI / 4), mat(0xf2c94c, { metalness: 0.9, roughness: 0.25 }), x, h - 3.2, z, g);
    L.colliders.push({ t: 'cone', x, z, r: R, y0: -1, y1: h - 1 });
  });
  // เสาโอเบลิสก์
  const ob = mat(0xcfae72, { roughness: 0.9 });
  mesh(new THREE.BoxGeometry(3, 26, 3), ob, -35, 13, -70, g).castShadow = true;
  mesh(new THREE.ConeGeometry(2.15, 3, 4).rotateY(Math.PI / 4), mat(0xf2c94c, { metalness: 0.8, roughness: 0.3 }), -35, 27.5, -70, g);
  L.colliders.push({ t: 'box', x0: -36.5, x1: -33.5, z0: -71.5, z1: -68.5, y0: 0, y1: 29 });
  // โอเอซิส + ต้นมะพร้าว + อูฐเดินวน
  const oy = desertH(120, -100);
  mesh(new THREE.CircleGeometry(26, 32), mat(0x7fae4a, { roughness: 1 }), 120, oy + 0.08, -100, g).rotation.x = -Math.PI / 2;
  mesh(new THREE.CircleGeometry(16, 32), mat(0x2f9fd6, { roughness: 0.1, metalness: 0.3 }), 120, oy + 0.15, -100, g).rotation.x = -Math.PI / 2;
  for (let k = 0; k < 8; k++) palm(g, 120 + Math.cos(k * 0.8) * (18 + rng() * 5), oy, -100 + Math.sin(k * 0.8) * (18 + rng() * 5), 6 + rng() * 3, rng);
  for (let k = 0; k < 3; k++) {
    const cm = camel(g); let a = k * 2.1;
    L.updaters.push((dt, t) => {
      a += dt * 0.05; const px = 120 + Math.cos(a) * 36, pz = -100 + Math.sin(a) * 36;
      cm.position.set(px, desertH(px, pz), pz); cm.rotation.y = -a + Math.PI;
      cm.userData.legs.forEach((l, i) => { l.rotation.x = Math.sin(t * 3 + i * 1.6 + k) * 0.35; });
    });
  }
  // กระบองเพชร + ก้อนหิน
  const cact = mat(0x3f7d3a, { roughness: 0.9 }), trunk = new THREE.CylinderGeometry(0.45, 0.5, 5, 8), arm = new THREE.CylinderGeometry(0.32, 0.32, 2.2, 8), tip = new THREE.SphereGeometry(0.45, 8, 6);
  const nearPyr = (x, z) => x > -230 && x < 220 && z > -460 && z < -180;
  for (let k = 0, n = 0; k < 400 && n < 70; k++) {
    const x = (rng() - 0.5) * 900, z = (rng() - 0.5) * 900;
    if (nearPyr(x, z) || Math.hypot(x, z - 10) < 28 || Math.hypot(x - 120, z + 100) < 45) continue;
    n++; const y = desertH(x, z), grp = new THREE.Group(); grp.position.set(x, y, z); grp.rotation.y = rng() * 6; grp.scale.setScalar(0.8 + rng() * 0.6); g.add(grp);
    mesh(trunk, cact, 0, 2.5, 0, grp).castShadow = true; mesh(tip, cact, 0, 5, 0, grp);
    const side = rng() < 0.5 ? 1 : -1;
    const a1 = mesh(arm, cact, side * 0.9, 2.2, 0, grp); a1.rotation.z = Math.PI / 2;
    mesh(arm, cact, side * 1.9, 3.2, 0, grp); mesh(tip, cact, side * 1.9, 4.3, 0, grp).scale.setScalar(0.7);
  }
  const rocks = new THREE.InstancedMesh(new THREE.DodecahedronGeometry(1, 0), new THREE.MeshStandardMaterial({ color: 0xffffff, flatShading: true, roughness: 1 }), 110);
  const dm = new THREE.Object3D(), rc = new THREE.Color();
  for (let i = 0; i < 110; i++) {
    let x, z; do { x = (rng() - 0.5) * 1000; z = (rng() - 0.5) * 1000; } while (nearPyr(x, z) || Math.hypot(x, z - 10) < 25);
    const s = 0.8 + rng() * 3; dm.position.set(x, desertH(x, z) + s * 0.3, z); dm.rotation.set(rng() * 3, rng() * 3, rng() * 3); dm.scale.set(s * 1.4, s, s * 1.2); dm.updateMatrix();
    rocks.setMatrixAt(i, dm.matrix); rc.setHex([0xb0703f, 0x9a5f36, 0xc98a52][i % 3]); rocks.setColorAt(i, rc);
  }
  rocks.castShadow = true; g.add(rocks);
}

/* ---------- รายชื่อด่าน (แก้ตำแหน่งห่วงได้ที่นี่) ---------- */
const LEVELS = [
  {
    id: 'city', name: 'เมืองตึกสูง', emoji: '🏙️', desc: 'บินลอดห่วงไปตามถนน ผ่านตึกระฟ้ากลางเมือง', seed: 11, par: 55, bounds: 430,
    sky: { top: 0x2f78d8, bottom: 0xd4e8fa, fog: 0xc9dcee, fogD: 0.0021, hs: 0xdfeeff, hg: 0x6b6b5a }, clouds: 34, cloudY: [170, 240],
    ground: () => 0, spawn: { x: 0, z: 10, yaw: 0 }, build: buildCity,
    rings: [{ x: 30, z: -30, h: 10 }, { x: 30, z: -110, h: 15 }, { x: 30, z: -210, h: 22 }, { x: 110, z: -210, h: 30 }, { x: 210, z: -210, h: 42 }, { x: 210, z: -120, h: 60 }, { x: 210, z: -30, h: 38 }, { x: 90, z: -30, h: 20 }],
    landmark: { name: 'ตึกระฟ้าใจกลางเมือง', x: 240, z: -240, dy: 110, radius: 180 }
  },
  {
    id: 'sea', name: 'ทะเลอันดามัน', emoji: '🏝️', desc: 'บินเลียบเกาะหินปูน ผ่านเรือหางยาว แล้วถ่ายรูปเกาะตะปู', seed: 22, par: 60, bounds: 470,
    sky: { top: 0x1f7ae0, bottom: 0xcdefff, fog: 0xbfe3f5, fogD: 0.0014, hs: 0xe0f4ff, hg: 0x4a7a8a }, clouds: 40, cloudY: [120, 200],
    ground: seaGround, spawn: { x: 0, z: 25, yaw: 0 }, build: buildSea,
    rings: [{ x: 0, z: -30, h: 8 }, { x: -40, z: -110, h: 12 }, { x: -20, z: -190, h: 18 }, { x: 50, z: -250, h: 14 }, { x: 125, z: -195, h: 22 }, { x: 145, z: -110, h: 12 }, { x: 95, z: -45, h: 26 }, { x: 35, z: -5, h: 14 }],
    landmark: { name: 'เกาะตะปู', x: -150, z: -120, dy: 16, radius: 120 }
  },
  {
    id: 'mountain', name: 'ภูเขาสูง', emoji: '⛰️', desc: 'บินไต่หุบเขาผ่านป่าสน ไปหาเจดีย์ทองบนยอดดอย', seed: 33, par: 70, bounds: 560,
    sky: { top: 0x3a86d6, bottom: 0xe6f0f5, fog: 0xd5e2ea, fogD: 0.0017, hs: 0xe6f2ff, hg: 0x3f5a36 }, clouds: 46, cloudY: [110, 190],
    ground: mtnGround, spawn: { x: 0, z: 10, yaw: 0 }, build: buildMountain,
    rings: [{ x: 0, z: -40, h: 10 }, { x: -45, z: -105, h: 14 }, { x: -15, z: -175, h: 16 }, { x: 45, z: -235, h: 18 }, { x: 25, z: -315, h: 22 }, { x: -50, z: -370, h: 22 }, { x: -120, z: -385, h: 24 }, { x: -235, z: -330, h: 26 }],
    landmark: { name: 'เจดีย์ทองบนยอดดอย', x: -160, z: -280, dy: 14, radius: 130 }
  },
  {
    id: 'desert', name: 'ทะเลทราย', emoji: '🏜️', desc: 'บินอ้อมพีระมิด แล้วบินข้ามยอดพีระมิดใหญ่', seed: 44, par: 65, bounds: 500,
    sky: { top: 0x3d8fd6, bottom: 0xf3d9a8, fog: 0xe9cf9c, fogD: 0.0014, hs: 0xfff1d6, hg: 0x9c7a4a }, clouds: 10, cloudY: [180, 240],
    ground: desertH, spawn: { x: 0, z: 10, yaw: 0 }, build: buildDesert,
    rings: [{ x: 0, z: -40, h: 10 }, { x: 40, z: -110, h: 14 }, { x: 0, z: -180, h: 20 }, { x: -120, z: -230, h: 24 }, { x: -215, z: -360, h: 24 }, { x: -100, z: -385, h: 34 }, { x: 0, z: -440, h: 50 }, { x: 100, z: -300, h: 98 }],
    landmark: { name: 'พีระมิดใหญ่', x: 100, z: -300, dy: 40, radius: 170 }
  }
];

/* =====================================================================
   ส่วนที่ 5: ผู้เล่น การบังคับ กล้อง ภารกิจ ถ่ายรูป อัดวิดีโอ
   ===================================================================== */
const held = new Set();
const touch = { fwd: 0, back: 0, left: 0, right: 0, up: 0, down: 0, tl: 0, tr: 0, gup: 0, gdn: 0 };
const showroom = { drone: null, type: null };
game.flyers = [];
game.camDist = 1;
let dragging = false, dragX = 0, dragY = 0;

function makePlayer(i, type) {
  return {
    idx: i, name: 'ผู้เล่น ' + (i + 1), color: PLAYER_COLORS[i], css: PLAYER_CSS[i], type,
    drone: null, arrow: null, cam: new THREE.PerspectiveCamera(62, 1, 0.1, 3200),
    input: { fwd: 0, side: 0, up: 0, turn: 0 }, next: 0, stage: 'rings', finished: false, time: 0,
    lookYaw: 0, lookPitch: 0, snap: true, rth: false, rthAlt: 0
  };
}
function makeArrow(color) {
  const g = new THREE.Group(), m = new THREE.MeshStandardMaterial({ color, emissive: color, emissiveIntensity: 0.35, roughness: 0.4, metalness: 0.1 });
  const cone = new THREE.Mesh(new THREE.ConeGeometry(0.3, 0.75, 16), m); cone.rotation.x = Math.PI / 2; cone.position.z = 0.4;
  const shaft = new THREE.Mesh(new THREE.CylinderGeometry(0.08, 0.08, 0.7, 10), m); shaft.rotation.x = Math.PI / 2; shaft.position.z = -0.3;
  g.add(cone); g.add(shaft); scene.add(g); return g;
}
const inRun = () => game.flyers.length > 0 && ['countdown', 'play', 'paused', 'result'].includes(game.state);
const mainP = () => game.flyers[0];
function activeDrone() { return inRun() ? mainP().drone : showroom.drone; }

function showShowroom(type) {
  if (showroom.drone && showroom.type === type) { showroom.drone.mesh.visible = true; return; }
  if (showroom.drone) showroom.drone.dispose();
  showroom.drone = new Drone(type); showroom.type = type; showroom.drone.yaw = 0.6;
}
function hideShowroom() { if (showroom.drone) showroom.drone.mesh.visible = false; }
function clearFlyers() {
  stopVideo();
  game.flyers.forEach(P => { if (P.drone) { P.drone.dispose(); P.drone = null; } if (P.arrow) { scene.remove(P.arrow); P.arrow = null; } });
  game.flyers = [];
}

// เริ่มบิน (ใช้ได้ทุกโหมด)
function startRun(flyers) {
  if (flyers) { clearFlyers(); game.flyers = flyers; } else { const f = game.flyers.slice(); clearFlyers(); game.flyers = f; }
  hideShowroom(); hideModal(); showScreen(null);
  const n = game.flyers.length, yaw = LV.def.spawn.yaw;
  game.flyers.forEach((P, i) => {
    P.drone = new Drone(P.type, game.mode === 'split' ? P.color : null);
    P.arrow = makeArrow(P.color);
    const off = n > 1 ? (i === 0 ? -3.2 : 3.2) : 0, x = LV.spawn.x + Math.cos(yaw) * off, z = LV.spawn.z - Math.sin(yaw) * off;
    P.drone.place(x, LV.ground(x, z) + 0.3 * P.drone.spec.scale, z, yaw);
    Object.assign(P, { next: 0, stage: 'rings', finished: false, time: 0, lookYaw: 0, lookPitch: 0, snap: true, rth: false });
  });
  Object.assign(game, { elapsed: 0, battery: 100, zoom: 1, gimbal: -5, countdown: 3.2, _lastCount: 99, state: 'countdown' });
  if (game.camView === 1 && game.mode === 'split') game.camView = 0;
  const solo = game.mode !== 'split';
  $('hud').classList.toggle('hidden', !solo); $('hud2').classList.toggle('hidden', solo);
  $('pads').classList.toggle('hidden', !(solo && game.touchOn));
  $('b-touch').classList.toggle('on', game.touchOn);
  $('ptag').classList.toggle('hidden', game.mode !== 'turns');
  if (game.mode === 'turns') { const P = mainP(); $('ptag').textContent = '🎮 ตาของ ' + P.name; $('ptag').style.color = P.css; }
  $('b-mode').textContent = FLIGHT_MODES[game.flightMode].label;
  $('b-zoom').textContent = '1x';
  $('b-rth').classList.remove('on');
  sfx.init();
}

/* ---------- อ่านปุ่มกด ---------- */
function readInput(P, idx) {
  const k = c => (held.has(c) ? 1 : 0), I = P.input;
  if (game.mode === 'split') {
    if (idx === 0) { I.fwd = k('KeyW') - k('KeyS'); I.turn = k('KeyD') - k('KeyA'); I.up = k('KeyE') - k('KeyQ'); }
    else { I.fwd = Math.max(k('ArrowUp'), k('KeyI')) - Math.max(k('ArrowDown'), k('KeyK')); I.turn = Math.max(k('ArrowRight'), k('KeyL')) - Math.max(k('ArrowLeft'), k('KeyJ')); I.up = k('KeyO') - k('KeyU'); }
    I.side = 0; return;
  }
  I.fwd = Math.max(k('KeyW'), k('ArrowUp'), touch.fwd) - Math.max(k('KeyS'), k('ArrowDown'), touch.back);
  I.side = Math.max(k('KeyD'), k('ArrowRight'), touch.right) - Math.max(k('KeyA'), k('ArrowLeft'), touch.left);
  I.up = Math.max(k('Space'), touch.up) - Math.max(k('ShiftLeft'), k('ShiftRight'), touch.down);
  I.turn = Math.max(k('KeyE'), touch.tr) - Math.max(k('KeyQ'), k('KeyO'), touch.tl);
  if (P.rth) {
    if (I.fwd || I.side || I.up || I.turn) { P.rth = false; $('b-rth').classList.remove('on'); toast('ยกเลิกบินกลับฐาน'); }
    else autopilot(P);
  }
}

/* ---------- บินกลับฐานอัตโนมัติ (RTH) ---------- */
function obstacleTop(x, z) {
  let top = LV.ground(x, z);
  for (const c of LV.colliders) {
    if (c.t === 'box') { if (x > c.x0 - 3 && x < c.x1 + 3 && z > c.z0 - 3 && z < c.z1 + 3) top = Math.max(top, c.y1); }
    else if (Math.hypot(x - c.x, z - c.z) < Math.max(c.r, c.r2 || 0) + 3) top = Math.max(top, c.y1);
  }
  return top;
}
function toggleRth() {
  const P = mainP(); if (!P || game.state !== 'play' || game.mode === 'split') return;
  P.rth = !P.rth; $('b-rth').classList.toggle('on', P.rth);
  if (P.rth) {
    let top = 0; const a = P.drone.pos, b = LV.spawn;
    for (let i = 0; i <= 30; i++) { const t = i / 30; top = Math.max(top, obstacleTop(lerp(a.x, b.x, t), lerp(a.z, b.z, t))); }
    P.rthAlt = Math.max(a.y, top + 12); toast('🏠 กำลังบินกลับฐาน... (กดปุ่มบังคับเพื่อยกเลิก)', 2500);
  }
  sfx.click();
}
function autopilot(P) {
  const d = P.drone, I = P.input, dx = LV.spawn.x - d.pos.x, dz = LV.spawn.z - d.pos.z, dist = Math.hypot(dx, dz);
  I.side = 0;
  if (dist > 3) {
    if (d.pos.y < P.rthAlt - 1.5) { I.up = 1; I.fwd = 0; I.turn = 0; return; }
    I.up = clamp((P.rthAlt - d.pos.y) * 0.3, -1, 1);
    let diff = Math.atan2(-dx, -dz) - d.yaw; diff = Math.atan2(Math.sin(diff), Math.cos(diff));
    I.turn = clamp(-diff * 2, -1, 1);
    I.fwd = Math.abs(diff) < 0.5 ? clamp(dist / 45, 0.12, 1) : 0;
  } else {
    I.fwd = I.turn = 0; I.up = -1;
    if (!d.flying || d.pos.y <= LV.ground(d.pos.x, d.pos.z) + 0.3 * d.spec.scale + 0.02) { P.rth = false; $('b-rth').classList.remove('on'); toast('🏠 ลงจอดที่ฐานเรียบร้อย'); }
  }
}

/* ---------- กล้อง ---------- */
const _v1 = new V3(), _v2 = new V3();
function insideBox(p) {
  for (const c of LV.colliders) if (c.t === 'box' && p.x > c.x0 && p.x < c.x1 && p.z > c.z0 && p.z < c.z1 && p.y < c.y1 + 0.5) return true;
  return false;
}
function updateCam(P, dt) {
  const d = P.drone, s = d.spec, cam = P.cam, F = d.fwd();
  const view = game.mode === 'split' ? 0 : game.camView;
  if (!dragging || game.mode === 'split') { const k = Math.exp(-1.6 * dt); P.lookYaw *= k; P.lookPitch *= k; }
  if (view === 1) {   // มุมกล้องโดรน (FPV)
    cam.position.copy(d.pos).addScaledVector(F, 1.0 * s.scale); cam.position.y -= 0.28 * s.scale;
    const fpv = d.type === 'fpv';
    cam.rotation.set(THREE.MathUtils.degToRad(game.gimbal) + (fpv ? d.pitch * 0.7 : 0) + P.lookPitch, d.yaw + P.lookYaw, fpv ? d.roll * 0.6 : 0, 'YXZ');
    cam.fov = 70 / game.zoom;
  } else {            // มุมหลังโดรน / มุมสูง
    const far = view === 2;
    const dist = (far ? 16 : 6.2) * Math.max(0.85, s.scale) * game.camDist + (far ? 0 : Math.min(3, Math.hypot(d.vel.x, d.vel.z) * 0.07));
    const yaw = d.yaw + P.lookYaw, pit = P.lookPitch;
    _v1.set(d.pos.x + Math.sin(yaw) * dist * Math.cos(pit), d.pos.y + (far ? 7 : 2.3) + dist * Math.sin(pit), d.pos.z + Math.cos(yaw) * dist * Math.cos(pit));
    for (let i = 0; i < 5 && insideBox(_v1); i++) _v1.lerp(d.pos, 0.3);
    const gmin = LV.ground(_v1.x, _v1.z) + 0.8; if (_v1.y < gmin) _v1.y = gmin;
    if (P.snap) { cam.position.copy(_v1); P.snap = false; } else cam.position.lerp(_v1, 1 - Math.exp(-7 * dt));
    _v2.copy(d.pos).addScaledVector(F, 3).y += 0.6;
    cam.lookAt(_v2);
    cam.fov = 62;
  }
}

/* ---------- ห่วงและภารกิจ ---------- */
function guideTarget(P) {
  if (P.finished) return null;
  if (P.stage === 'rings') return LV.rings[P.next] ? LV.rings[P.next].pos : null;
  if (P.stage === 'photo') return LV.landmark.pos;
  return null;
}
function updateArrow(P, t) {
  P.drone.mesh.visible = game.mode === 'split' || game.camView !== 1;
  const tg = guideTarget(P), a = P.arrow;
  if (!tg || (game.mode !== 'split' && game.camView === 1)) { a.visible = false; return; }
  a.visible = true;
  a.position.copy(P.drone.pos); a.position.y += 1.3 * P.drone.spec.scale + 0.35 + Math.sin(t * 4) * 0.08;
  a.lookAt(tg);
}
function updateRings(t) {
  const fl = game.flyers.filter(p => p.drone);
  if (!fl.length || !inRun()) { LV.rings.forEach(R => { R.grp.visible = true; R.mat.opacity = 0.85; R.disc.visible = false; R.label.visible = true; }); return; }
  const minNext = Math.min(...fl.map(p => (p.stage === 'rings' ? p.next : LV.rings.length)));
  LV.rings.forEach((R, i) => {
    R.grp.visible = i >= minNext; if (i < minNext) return;
    const isNext = fl.some(p => p.stage === 'rings' && p.next === i);
    R.torus.rotation.z += 0.012;
    R.torus.scale.setScalar(isNext ? 1 + Math.sin(t * 5) * 0.06 : 1);
    R.mat.opacity = isNext ? 1 : 0.4;
    R.mat.emissiveIntensity = isNext ? 0.9 + Math.sin(t * 5) * 0.3 : 0.2;
    R.disc.visible = isNext; R.label.visible = isNext || i < minNext + 3;
  });
}
function checkMission(P) {
  if (P.finished || P.stage !== 'rings') return;
  const R = LV.rings[P.next];
  if (!R || P.drone.pos.distanceTo(R.pos) > RING_R + 0.4) return;
  popRing(R); sfx.ring(); P.next++;
  const N = LV.rings.length;
  if (P.next < N) { if (game.mode !== 'split') toast('ผ่านห่วง ' + P.next + '/' + N + ' ✔', 900); return; }
  if (game.mode === 'solo') { P.stage = 'photo'; toast('📸 ห่วงครบแล้ว! ต่อไปถ่ายรูป "' + LV.landmark.name + '" ตามลูกศรสีเหลืองเลย', 4500); P.arrow.children.forEach(c => c.material.color.setHex(0xfacc15)); }
  else finishPlayer(P);
}

/* ---------- ถ่ายรูป ---------- */
function snapPhoto() {
  const P = mainP(); if (!P || game.state !== 'play' || game.mode === 'split') return;
  sfx.shutter();
  const fl = $('flash'); fl.style.transition = 'none'; fl.style.opacity = '0.85';
  requestAnimationFrame(() => { fl.style.transition = 'opacity .35s'; fl.style.opacity = '0'; });
  const spec = P.drone.spec, pr = renderer.getPixelRatio(), W = window.innerWidth, H = window.innerHeight;
  const ratio = Math.max(pr, Math.min(spec.photoW / W, 3, Math.sqrt(9e6 / (W * H))));
  const av = P.arrow.visible; P.arrow.visible = false;
  renderer.setPixelRatio(ratio); renderer.setViewport(0, 0, W, H);
  P.cam.aspect = W / H; P.cam.updateProjectionMatrix();
  renderer.shadowMap.needsUpdate = true; renderer.render(scene, P.cam);
  const url = renderer.domElement.toDataURL('image/jpeg', 0.9);
  renderer.setPixelRatio(pr); P.arrow.visible = av;
  const time = new Date().toLocaleTimeString('th-TH'), px = Math.round(W * ratio) + '×' + Math.round(H * ratio);
  game.photos.push({ type: 'img', url, time, info: LV.def.name + ' • ' + px });
  updateGalBadge();
  $('photo-img').src = url; $('photo-dl').href = url; $('photo-dl').download = 'drone_' + Date.now() + '.jpg';
  $('photo-cap').textContent = '📸 ' + px;
  $('photo-pop').classList.remove('hidden');
  clearTimeout(snapPhoto._t); snapPhoto._t = setTimeout(() => $('photo-pop').classList.add('hidden'), 3500);
  if (P.stage === 'photo') checkLandmarkPhoto(P);
}
function checkLandmarkPhoto(P) {
  const lm = LV.landmark, dist = P.drone.pos.distanceTo(lm.pos), maxD = lm.radius * P.drone.spec.photoBonus;
  const ndc = lm.pos.clone().project(P.cam);
  const inView = ndc.z < 1 && Math.abs(ndc.x) < 0.8 && Math.abs(ndc.y) < 0.85;
  if (inView && dist <= maxD) { P.stage = 'done'; completeSolo(P); }
  else if (!inView) toast('🎯 ยังไม่เห็น ' + lm.name + ' ในรูปเลย หันไปทางลูกศรสีเหลืองก่อนนะ', 3000);
  else toast('🔭 ไกลไปนิด! บินเข้าไปใกล้อีก ' + Math.ceil(dist - maxD) + ' เมตร' + (P.drone.type !== 'mavic' ? ' (Mavic 3 Pro ถ่ายได้ไกลกว่า)' : ''), 3200);
}

/* ---------- อัดวิดีโอ ---------- */
let rec = null, recChunks = [], recStart = 0;
function toggleVideo() { if (rec) stopVideo(); else startVideo(); }
function startVideo() {
  const cv = renderer.domElement;
  if (!window.MediaRecorder || !cv.captureStream) { toast('เครื่องนี้อัดวิดีโอไม่ได้ 😢'); return; }
  try {
    const mime = ['video/webm;codecs=vp9', 'video/webm;codecs=vp8', 'video/webm', 'video/mp4'].find(m => MediaRecorder.isTypeSupported(m)) || '';
    const r = new MediaRecorder(cv.captureStream(30), mime ? { mimeType: mime, videoBitsPerSecond: 4e6 } : {});
    recChunks = [];
    r.ondataavailable = e => { if (e.data && e.data.size) recChunks.push(e.data); };
    r.onstop = () => {
      const type = r.mimeType || 'video/webm', url = URL.createObjectURL(new Blob(recChunks, { type }));
      game.photos.push({ type: 'vid', url, time: new Date().toLocaleTimeString('th-TH'), info: LV.def.name, ext: type.includes('mp4') ? 'mp4' : 'webm' });
      updateGalBadge(); toast('🎬 บันทึกวิดีโอแล้ว ดูได้ที่ปุ่มคลังภาพ 🖼️');
    };
    r.start(1000); rec = r; recStart = performance.now();
    $('rec').classList.remove('hidden'); $('b-video').classList.add('rec-on'); toast('⏺️ เริ่มอัดวิดีโอ');
  } catch (e) { rec = null; toast('อัดวิดีโอไม่ได้ 😢'); }
}
function stopVideo() {
  if (!rec) return; const r = rec; rec = null;
  try { r.stop(); } catch (e) {}
  $('rec').classList.add('hidden'); $('b-video').classList.remove('rec-on');
}
function updateGalBadge() { $('gal-n').textContent = game.photos.length; }
function openGallery() {
  const grid = $('gal-grid'); grid.innerHTML = '';
  if (!game.photos.length) grid.innerHTML = '<div style="grid-column:1/-1;text-align:center;color:#94a3b8;padding:40px">ยังไม่มีรูปหรือวิดีโอ<br>กดปุ่มวงกลมสีขาวเพื่อถ่ายรูปนะ 📸</div>';
  game.photos.slice().reverse().forEach((it, i) => {
    const d = document.createElement('div'); d.className = 'it';
    const media = it.type === 'img' ? `<img src="${it.url}" alt="">` : `<video src="${it.url}" controls playsinline></video>`;
    d.innerHTML = `${media}<div style="margin-top:4px">${it.type === 'img' ? '📸' : '🎬'} ${it.time}<br><span style="color:#94a3b8">${it.info || ''}</span></div><a href="${it.url}" download="drone_${i}.${it.type === 'img' ? 'jpg' : it.ext}">⬇ ดาวน์โหลด</a>`;
    grid.appendChild(d);
  });
  $('gal').classList.remove('hidden');
}

/* ---------- จบด่าน ---------- */
function starsHtml(n) { return '<div class="stars">' + [1, 2, 3].map(i => `<span class="${i <= n ? '' : 'off'}">⭐</span>`).join('') + '</div>'; }
function completeSolo(P) {
  P.finished = true; P.time = game.elapsed; game.state = 'result'; sfx.win();
  const par = LV.def.par, t = P.time, stars = t <= par ? 3 : t <= par * 1.5 ? 2 : 1;
  const best = load('best', {}), prev = best[LV.id], isNew = !prev || t < prev.time;
  best[LV.id] = { time: isNew ? t : prev.time, stars: Math.max(stars, prev ? prev.stars : 0) }; store('best', best);
  setTimeout(() => showModal({
    icon: '🏆', title: 'ผ่านด่าน ' + LV.def.name + '!',
    body: starsHtml(stars) + `<div>เวลา <b>${fmtTime(t)}</b>${isNew ? ' 🎉 สถิติใหม่!' : ''}</div><div style="font-size:13px;margin-top:6px;color:#94a3b8">ทำเวลาไม่เกิน ${fmtTime(par)} จะได้ 3 ดาว</div>`,
    btns: [['ด่านต่อไป ➜', 'cyan', nextLevel], ['เล่นด่านนี้อีกครั้ง', 'ghost', () => startRun()], ['เปลี่ยนโดรน', 'ghost', changeDrone], ['เมนูหลัก', 'ghost', toMenu]]
  }), 800);
}
function finishPlayer(P) {
  P.finished = true; P.time = game.elapsed; sfx.win();
  if (game.mode === 'split') {
    game.state = 'result';
    const o = game.flyers.find(q => q !== P);
    setTimeout(() => showModal({
      icon: '🏆', title: P.name + ' ชนะ!',
      body: `<div class="rank"><div style="border-left:6px solid ${P.css}"><span>🥇 ${P.name} • ${DRONES[P.type].name}</span><b>${fmtTime(P.time)}</b></div><div style="border-left:6px solid ${o.css}"><span>🥈 ${o.name} • ${DRONES[o.type].name}</span><b>ห่วง ${o.next}/${LV.rings.length}</b></div></div>`,
      btns: [['แข่งอีกครั้ง', 'orange', () => startRun()], ['เปลี่ยนโดรน', 'ghost', startSplitSelect], ['เปลี่ยนด่าน', 'ghost', () => openLevelSelect(() => startRun(), toMenu)], ['เมนูหลัก', 'ghost', toMenu]]
    }), 900);
  } else {
    game.state = 'result'; game.turnResults[game.active] = P.time;
    const last = game.active >= game.turnCount - 1;
    setTimeout(() => showModal({ icon: '⏱️', title: P.name + ' บินครบแล้ว!', body: `เวลา <b style="font-size:22px">${fmtTime(P.time)}</b>`, btns: [[last ? 'ดูผลการแข่ง 🏆' : 'คนต่อไป ➜', 'lime', nextTurn]] }), 700);
  }
}

/* =====================================================================
   ส่วนที่ 6: หน้าจอเมนู ปุ่มต่างๆ HUD และลูปหลักของเกม
   ===================================================================== */
function showScreen(id) {
  document.querySelectorAll('.screen').forEach(s => s.classList.toggle('hidden', s.id !== id));
  if (id) { $('hud').classList.add('hidden'); $('hud2').classList.add('hidden'); }
}
function toast(msg, ms = 2000) {
  const t = $('toast'); t.textContent = msg; t.classList.add('show');
  clearTimeout(toast._t); toast._t = setTimeout(() => t.classList.remove('show'), ms);
}
function showModal({ icon = '', title = '', body = '', btns = [] }) {
  $('modal-icon').textContent = icon; $('modal-title').textContent = title; $('modal-body').innerHTML = body;
  const box = $('modal-btns'); box.innerHTML = '';
  btns.forEach(([label, cls, fn]) => { const b = document.createElement('button'); b.className = 'big ' + cls; b.textContent = label; b.onclick = () => { sfx.click(); fn(); }; box.appendChild(b); });
  $('modal').classList.remove('hidden');
}
function hideModal() { $('modal').classList.add('hidden'); }
function showCount(txt) {
  const el = $('countdown'); el.textContent = txt; el.classList.remove('hidden', 'pop'); void el.offsetWidth; el.classList.add('pop');
  clearTimeout(showCount._t); showCount._t = setTimeout(() => el.classList.add('hidden'), 900);
}

/* ---------- เมนู / เลือกโดรน / เลือกด่าน ---------- */
function toMenu() {
  hideModal(); clearFlyers(); game.state = 'menu';
  $('hud').classList.add('hidden'); $('hud2').classList.add('hidden'); $('photo-pop').classList.add('hidden');
  showScreen('scr-menu'); showShowroom(game.pickType);
}
let droneOk = null, droneBack = null, levelOk = null, levelBack = null;
function openDroneSelect(idx, title, onOk, onBack) {
  hideModal(); clearFlyers(); game.state = 'drone'; game.pickFor = idx;
  $('drone-title').textContent = title; $('drone-back').style.visibility = onBack ? 'visible' : 'hidden';
  droneOk = onOk; droneBack = onBack;
  const P = game.players[idx]; game.pickType = (P && P.type) || load('lastDrone', 'mavic');
  const box = $('drone-cards'); box.innerHTML = '';
  DRONE_ORDER.forEach(type => {
    const s = DRONES[type], c = document.createElement('div');
    c.className = 'card' + (type === game.pickType ? ' sel-on' : ''); c.dataset.type = type;
    const bars = v => '<div class="bar">' + [1, 2, 3, 4, 5].map(i => `<i class="${i <= v ? 'f' : ''}"></i>`).join('') + '</div>';
    c.innerHTML = `<div class="emoji">${s.emoji}</div><div class="t">${s.name}</div><span class="tag" style="background:${s.tagColor}">${s.tag}</span>
      <div class="d">${s.desc}</div>
      <div class="stat"><span>ความเร็ว</span>${bars(s.stats[0])}</div>
      <div class="stat"><span>บังคับง่าย</span>${bars(s.stats[1])}</div>
      <div class="stat"><span>กล้อง</span>${bars(s.stats[2])}</div>`;
    c.onclick = () => { sfx.click(); game.pickType = type; box.querySelectorAll('.card').forEach(x => x.classList.toggle('sel-on', x === c)); showShowroom(type); };
    box.appendChild(c);
  });
  showScreen('scr-drone'); showShowroom(game.pickType);
}
function openLevelSelect(onOk, onBack) {
  hideModal(); clearFlyers(); game.state = 'level';
  levelOk = onOk; levelBack = onBack;
  const best = load('best', {}), box = $('level-cards'); box.innerHTML = '';
  LEVELS.forEach(L => {
    const c = document.createElement('div'); c.className = 'card' + (L.id === game.levelId ? ' sel-on' : '');
    const b = best[L.id];
    c.innerHTML = `<div class="emoji">${L.emoji}</div><div class="t">${L.name}</div><div class="d">${L.desc}</div>
      <div class="best">${b ? '⭐'.repeat(b.stars) + ' สถิติ ' + fmtTime(b.time) : 'ยังไม่เคยเล่น'}</div>`;
    c.onclick = () => { sfx.click(); box.querySelectorAll('.card').forEach(x => x.classList.toggle('sel-on', x === c)); if (L.id !== LV.id) loadLevel(L.id); };
    box.appendChild(c);
  });
  showScreen('scr-level'); showShowroom(game.pickType);
}

/* ---------- ลำดับการเล่นแต่ละโหมด ---------- */
function startSolo() {
  game.mode = 'solo'; game.players = [makePlayer(0, load('lastDrone', 'mavic'))];
  const pickDrone = () => openDroneSelect(0, 'เลือกโดรนที่อยากบิน', pickLevel, toMenu);
  const pickLevel = () => openLevelSelect(() => startRun([game.players[0]]), pickDrone);
  pickDrone();
}
function startSplitSelect() {
  game.mode = 'split';
  if (game.players.length !== 2 || game.players[0].idx !== 0) game.players = [makePlayer(0, 'mavic'), makePlayer(1, 'fpv')];
  game.players[0].name = 'คนที่ 1'; game.players[1].name = 'คนที่ 2';
  const p1 = () => openDroneSelect(0, 'คนที่ 1 (ใช้ปุ่ม W A S D) เลือกโดรน', p2, toMenu);
  const p2 = () => openDroneSelect(1, 'คนที่ 2 (ใช้ปุ่มลูกศร) เลือกโดรน', lvl, p1);
  const lvl = () => openLevelSelect(() => startRun(game.players.slice()), p2);
  p1();
  if (window.matchMedia('(pointer: coarse)').matches) toast('⌨️ โหมดนี้ต้องใช้คีย์บอร์ด ถ้าเล่นบนมือถือให้เลือก "ผลัดกันแข่ง" นะ', 4500);
}
function startTurns(count) {
  game.mode = 'turns'; game.turnCount = count; game.turnResults = [];
  game.players = []; for (let i = 0; i < count; i++) game.players.push(makePlayer(i, 'mavic'));
  openLevelSelect(() => { game.active = 0; game.turnResults = []; turnPick(); }, () => { showScreen('scr-count'); game.state = 'count'; });
}
function turnPick() {
  const P = game.players[game.active];
  openDroneSelect(game.active, '🎮 ตาของ ' + P.name + ' — เลือกโดรน', () => startRun([P]),
    game.active === 0 ? () => startTurns(game.turnCount) : null);
}
function nextTurn() {
  game.active++;
  if (game.active < game.turnCount) { turnPick(); return; }
  const list = game.players.map((P, i) => ({ P, t: game.turnResults[i] })).sort((a, b) => (a.t == null) - (b.t == null) || a.t - b.t);
  const medal = ['🥇', '🥈', '🥉', '4️⃣'];
  clearFlyers(); game.state = 'result'; sfx.win();
  showModal({
    icon: '🏆', title: list[0].t == null ? 'ไม่มีใครถึงเส้นชัยเลย 😅' : list[0].P.name + ' ชนะ!',
    body: '<div class="rank">' + list.map((r, i) => `<div style="border-left:6px solid ${r.P.css}"><span>${medal[i]} ${r.P.name} • ${DRONES[r.P.type].name}</span><b>${r.t == null ? 'ไม่ถึงเส้นชัย' : fmtTime(r.t)}</b></div>`).join('') + '</div>',
    btns: [['แข่งอีกรอบ', 'lime', () => { game.active = 0; game.turnResults = []; turnPick(); }], ['เปลี่ยนด่าน', 'ghost', () => startTurns(game.turnCount)], ['เมนูหลัก', 'ghost', toMenu]]
  });
}
function nextLevel() {
  const i = LEVELS.findIndex(l => l.id === LV.id), L = LEVELS[(i + 1) % LEVELS.length];
  loadLevel(L.id); startRun();
}
function changeDrone() { openDroneSelect(0, 'เลือกโดรนที่อยากบิน', () => startRun([game.players[0]]), null); }

let pausedFrom = null;
function togglePause() {
  if (game.state === 'paused') { resume(); return; }
  if (game.state !== 'play' && game.state !== 'countdown') return;
  pausedFrom = game.state; game.state = 'paused'; held.clear();
  const btns = [['เล่นต่อ ▶', 'cyan', resume], ['เริ่มใหม่', 'ghost', () => startRun()]];
  if (game.mode === 'solo') btns.push(['เปลี่ยนโดรน', 'ghost', changeDrone], ['เปลี่ยนด่าน', 'ghost', () => openLevelSelect(() => startRun([game.players[0]]), null)]);
  if (game.mode === 'split') btns.push(['เปลี่ยนโดรน', 'ghost', startSplitSelect]);
  if (game.mode === 'turns') btns.push(['ยอมแพ้ ข้ามตานี้', 'ghost', () => { game.turnResults[game.active] = null; nextTurn(); }]);
  btns.push(['เมนูหลัก', 'ghost', toMenu]);
  showModal({ icon: '⏸️', title: 'หยุดเกมชั่วคราว', body: '', btns });
}
function resume() { hideModal(); if (game.state === 'paused') game.state = pausedFrom || 'play'; }

/* ---------- ปุ่มในเกม ---------- */
function cycleView() {
  game.camView = (game.camView + 1) % 3;
  if (game.camView !== 1) { game.zoom = 1; $('b-zoom').textContent = '1x'; }
  toast(['🎥 มุมหลังโดรน', '📷 มุมกล้องโดรน', '🦅 มุมสูง'][game.camView], 1200); sfx.click();
}
function cycleZoom() {
  const P = mainP(); if (!P) return; const max = P.drone.spec.maxZoom;
  if (max <= 1) { toast('โดรนลำนี้ซูมไม่ได้ ลอง Mavic 3 Pro สิ 📸'); return; }
  game.zoom = game.zoom >= max ? 1 : game.zoom * 2;
  if (game.zoom > 1 && game.camView !== 1) game.camView = 1;
  $('b-zoom').textContent = game.zoom + 'x'; toast('🔍 ซูม ' + game.zoom + ' เท่า', 900); sfx.click();
}
function cycleMode() {
  const k = ['cine', 'normal', 'sport'], m = k[(k.indexOf(game.flightMode) + 1) % 3];
  game.flightMode = m; $('b-mode').textContent = FLIGHT_MODES[m].label; toast(FLIGHT_MODES[m].name, 1300); sfx.click();
}
function cycleTod() {
  const k = ['day', 'sunset', 'night']; game.tod = k[(k.indexOf(game.tod) + 1) % 3];
  game.headlight = game.tod === 'night'; $('b-light').classList.toggle('on', game.headlight);
  applyTod(); sfx.click();
}
function toggleLight() { game.headlight = !game.headlight; $('b-light').classList.toggle('on', game.headlight); sfx.click(); }
function toggleRain() { game.rain = !game.rain; rainPts.visible = game.rain; $('b-rain').classList.toggle('on', game.rain); sfx.click(); }

function setupInput() {
  window.addEventListener('keydown', e => {
    if (['Space', 'ArrowUp', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'Tab'].includes(e.code)) e.preventDefault();
    held.add(e.code);
    if (e.repeat) return;
    sfx.init();
    if (!inRun()) return;
    if (e.code === 'Escape' || e.code === 'KeyP') { togglePause(); return; }
    if (game.mode === 'split' || game.state !== 'play') return;
    const act = { KeyC: snapPhoto, KeyV: toggleVideo, KeyX: cycleView, KeyZ: cycleZoom, KeyF: toggleLight, KeyH: toggleRth, KeyM: cycleMode }[e.code];
    if (act) act();
  });
  window.addEventListener('keyup', e => held.delete(e.code));
  window.addEventListener('blur', () => held.clear());
  document.addEventListener('click', e => { const b = e.target.closest('button'); if (b) b.blur(); });

  // ปุ่มบังคับบนจอ (มือถือ/แท็บเล็ต) กดค้างได้ กดหลายปุ่มพร้อมกันได้
  const bindHold = (el, key) => {
    const on = e => { e.preventDefault(); sfx.init(); touch[key] = 1; el.classList.add('held'); };
    const off = () => { touch[key] = 0; el.classList.remove('held'); };
    el.addEventListener('pointerdown', on); ['pointerup', 'pointerleave', 'pointercancel'].forEach(ev => el.addEventListener(ev, off));
    el.addEventListener('contextmenu', e => e.preventDefault());
  };
  document.querySelectorAll('[data-k]').forEach(b => bindHold(b, b.dataset.k));
  bindHold($('b-gup'), 'gup'); bindHold($('b-gdn'), 'gdn');

  // ลากบนจอเพื่อหมุนมองรอบๆ / ลูกล้อเมาส์ ซูมระยะกล้อง
  const cv = renderer.domElement;
  cv.addEventListener('pointerdown', e => { dragging = true; dragX = e.clientX; dragY = e.clientY; sfx.init(); });
  window.addEventListener('pointermove', e => {
    if (!dragging || !inRun() || game.mode === 'split') return;
    const P = mainP(); P.lookYaw -= (e.clientX - dragX) * 0.006; P.lookPitch = clamp(P.lookPitch + (e.clientY - dragY) * 0.004, -0.5, 1.2);
    dragX = e.clientX; dragY = e.clientY;
  });
  window.addEventListener('pointerup', () => { dragging = false; });
  cv.addEventListener('wheel', e => { game.camDist = clamp(game.camDist + e.deltaY * 0.001, 0.6, 2.5); }, { passive: true });

  const on = (id, fn) => $(id).addEventListener('click', fn);
  on('m-solo', () => { sfx.init(); sfx.click(); startSolo(); });
  on('m-split', () => { sfx.init(); sfx.click(); startSplitSelect(); });
  on('m-turns', () => { sfx.init(); sfx.click(); game.state = 'count'; showScreen('scr-count'); });
  document.querySelectorAll('[data-count]').forEach(b => b.addEventListener('click', () => { sfx.click(); startTurns(+b.dataset.count); }));
  document.querySelectorAll('[data-back="menu"]').forEach(b => b.addEventListener('click', toMenu));
  on('b-drone-ok', () => {
    sfx.click(); const P = game.players[game.pickFor]; if (P) P.type = game.pickType;
    if (game.mode === 'solo') store('lastDrone', game.pickType);
    if (droneOk) droneOk();
  });
  on('drone-back', () => { sfx.click(); if (droneBack) droneBack(); });
  on('b-level-ok', () => { sfx.click(); if (levelOk) levelOk(); });
  on('level-back', () => { sfx.click(); if (levelBack) levelBack(); else toMenu(); });
  on('b-pause', togglePause); on('b-pause2', togglePause);
  on('b-shot', snapPhoto); on('b-video', toggleVideo); on('b-view', cycleView); on('b-zoom', cycleZoom);
  on('b-mode', cycleMode); on('b-tod', cycleTod); on('b-rain', toggleRain); on('b-light', toggleLight); on('b-rth', toggleRth);
  on('b-gal', openGallery); on('gal-x', () => $('gal').classList.add('hidden'));
  on('b-touch', () => { game.touchOn = !game.touchOn; $('pads').classList.toggle('hidden', !game.touchOn); $('b-touch').classList.toggle('on', game.touchOn); });
}

/* ---------- HUD ---------- */
const _txt = {};
function setText(id, v) { if (_txt[id] !== v) { _txt[id] = v; $(id).textContent = v; } }
function updateHud() {
  if (!inRun()) return;
  if (game.mode === 'split') {
    setText('sp-timer', fmtTime(game.elapsed));
    game.flyers.forEach((P, i) => {
      const el = $('sp' + (i + 1)); el.style.borderColor = P.css;
      const html = `<h3 style="color:${P.css}">${P.name}</h3><div class="row">${DRONES[P.type].name}</div><div class="big">${P.finished ? '🏁 ถึงเส้นชัย!' : 'ห่วง ' + P.next + ' / ' + LV.rings.length}</div>`;
      if (el._h !== html) { el._h = html; el.innerHTML = html; }
    });
    return;
  }
  const P = mainP(), d = P.drone, N = LV.rings.length;
  setText('timer', fmtTime(game.elapsed));
  const tg = guideTarget(P);
  if (P.stage === 'rings') setText('mission', (game.mode === 'turns' ? '🏁 ' : '🎯 ') + 'บินลอดห่วง ' + P.next + '/' + N);
  else if (P.stage === 'photo') setText('mission', '📸 ถ่ายรูป: ' + LV.landmark.name);
  else setText('mission', '✅ สำเร็จ!');
  const g = $('guide');
  if (tg && game.state === 'play') {
    const dist = d.pos.distanceTo(tg); g.classList.remove('hidden');
    if (P.stage === 'rings') setText('guide', '➜ ห่วงที่ ' + (P.next + 1) + ' อีก ' + Math.round(dist) + ' ม.');
    else { const ok = dist <= LV.landmark.radius * d.spec.photoBonus; setText('guide', (ok ? '📷 ถ่ายได้แล้ว! หันไปหา ' : '📸 บินไปหา ') + LV.landmark.name + ' • ' + Math.round(dist) + ' ม.'); }
  } else g.classList.add('hidden');
  setText('t-d', Math.hypot(d.pos.x - LV.spawn.x, d.pos.z - LV.spawn.z).toFixed(1));
  setText('t-h', (d.pos.y - LV.ground(d.pos.x, d.pos.z) - 0.3 * d.spec.scale).toFixed(1));
  setText('t-hs', (Math.hypot(d.vel.x, d.vel.z) * 3.6).toFixed(1));
  setText('t-vs', d.vel.y.toFixed(1));
  setText('batt', Math.round(game.battery) + '%');
  setText('gimbal', Math.round(game.gimbal) + '°');
  if (rec) { const s = Math.floor((performance.now() - recStart) / 1000); setText('rec-t', String(Math.floor(s / 60)).padStart(2, '0') + ':' + String(s % 60).padStart(2, '0')); }
}

/* ---------- ลูปหลัก ---------- */
function step(dt, t) {
  if (game.state === 'countdown') {
    game.countdown -= dt; const n = Math.ceil(game.countdown);
    if (n !== game._lastCount && n <= 3) { game._lastCount = n; if (n > 0) { showCount(String(n)); sfx.count(false); } else { showCount('GO!'); sfx.count(true); game.state = 'play'; } }
    game.flyers.forEach(P => P.drone.update(dt, null, t, true));
  } else if (game.state === 'play') {
    game.elapsed += dt; game.battery = Math.max(0, game.battery - dt * 0.1);
    game.flyers.forEach((P, i) => { readInput(P, i); P.drone.update(dt, P.finished ? null : P.input, t, true); checkMission(P); });
    if (held.has('KeyT') || touch.gup) game.gimbal = Math.min(20, game.gimbal + 45 * dt);
    if (held.has('KeyG') || touch.gdn) game.gimbal = Math.max(-90, game.gimbal - 45 * dt);
  } else if (game.state === 'result') {
    game.flyers.forEach(P => P.drone.update(dt, null, t, true));
  }
  game.flyers.forEach(P => { updateCam(P, dt); updateArrow(P, t); });
  if (game.mode === 'split' && game.flyers.length === 2) focus.copy(game.flyers[0].drone.pos).add(game.flyers[1].drone.pos).multiplyScalar(0.5);
  else focus.copy(mainP().drone.pos);
  const d = mainP().drone; sfx.hum(game.state === 'paused' ? 0 : clamp(d.spin / 60, 0, 1), 80 + d.spin * 2.2);
}
function stepShowroom(dt, t) {
  const d = showroom.drone; if (!d || !LV.spawn) return;
  d.pos.set(LV.spawn.x, LV.spawn.y + 1.7 + Math.sin(t * 1.5) * 0.15, LV.spawn.z);
  d.flying = true; d.spin = 48; d.pitch = d.roll = 0; d.yaw += dt * 0.3; d.sync(t, dt);
  const st = game.state, a = t * 0.12;
  const R = st === 'drone' ? 3.6 * d.spec.scale + 1.6 : st === 'level' ? 30 : 13, H = st === 'drone' ? 0.9 : st === 'level' ? 12 : 4;
  menuCam.position.set(d.pos.x + Math.sin(a) * R, d.pos.y + H, d.pos.z + Math.cos(a) * R);
  menuCam.lookAt(d.pos.x, d.pos.y - (st === 'drone' ? 0.9 : st === 'level' ? 6 : 0), d.pos.z);
  focus.copy(d.pos); sfx.hum(0, 100);
}
function render() {
  const W = window.innerWidth, H = window.innerHeight;
  renderer.shadowMap.needsUpdate = true;
  if (inRun() && game.mode === 'split' && game.flyers.length === 2) {
    renderer.setScissorTest(true);
    game.flyers.forEach((P, i) => {
      const w = Math.floor(W / 2), x = i ? W - w : 0;
      renderer.setViewport(x, 0, w, H); renderer.setScissor(x, 0, w, H);
      P.cam.aspect = w / H; P.cam.updateProjectionMatrix(); renderer.render(scene, P.cam);
    });
    renderer.setScissorTest(false);
  } else {
    const cam = inRun() ? mainP().cam : menuCam;
    renderer.setViewport(0, 0, W, H); cam.aspect = W / H; cam.updateProjectionMatrix(); renderer.render(scene, cam);
  }
}
function frame() {
  requestAnimationFrame(frame);
  const dt = Math.min(clock.getDelta(), 0.05), t = clock.elapsedTime;
  if (inRun()) step(dt, t); else stepShowroom(dt, t);
  updateRings(t); updateFx(dt); updateEnv(dt, t);
  render(); updateHud();
}

window.addEventListener('load', () => {
  if (!window.THREE) { document.body.innerHTML = '<p style="padding:40px;font-size:20px">โหลดเกมไม่สำเร็จ ตรวจสอบอินเทอร์เน็ตแล้วลองใหม่นะ</p>'; return; }
  initEngine();
  renderer.shadowMap.autoUpdate = false;
  game.touchOn = window.matchMedia('(pointer: coarse)').matches;
  game.pickType = load('lastDrone', 'mavic');
  loadLevel('city');
  setupInput();
  toMenu();
  frame();
});
</script>
</body>
</html>
