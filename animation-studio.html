<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, viewport-fit=cover">
<meta name="theme-color" content="#FFFFFF">
<title>2D 애니메이션 스튜디오</title>
<style>
:root{--bg:#E9ECF2;--panel:#FFFFFF;--ink:#1E2A3B;--muted:#6B7689;--line:#D3D8E2;--soft:#EEF2FA;--accent:#3B6FD8;--accent-ink:#fff;--pen-color:#1E2A3B;color-scheme:light}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]):not([data-theme="paper"]){--bg:#161B24;--panel:#212835;--ink:#E6EAF2;--muted:#9AA4B6;--line:#343D4E;--soft:#2A3344;--accent-ink:#0E1420;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#161B24;--panel:#212835;--ink:#E6EAF2;--muted:#9AA4B6;--line:#343D4E;--soft:#2A3344;--accent-ink:#0E1420;color-scheme:dark}
:root[data-theme="paper"]{--bg:#EFE6D6;--panel:#FBF6EC;--ink:#3A2E22;--muted:#857360;--line:#DCCDB4;--soft:#F3EBDC;--accent-ink:#fff;color-scheme:light}
:root[data-theme="midnight"]{--bg:#0B0E14;--panel:#121722;--ink:#D8DEEA;--muted:#7D879A;--line:#252D3D;--soft:#1A2130;--accent-ink:#0B0E14;color-scheme:dark}
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html,body{margin:0;height:100%;overflow:hidden;overscroll-behavior:none}
body{background:var(--bg);color:var(--ink);font-family:"Pretendard","Apple SD Gothic Neo","Noto Sans KR",system-ui,sans-serif;display:flex;flex-direction:column;height:100dvh;user-select:none;-webkit-user-select:none}
button,label.btn{touch-action:manipulation;background:var(--soft);color:var(--ink);border:1px solid var(--line);border-radius:10px;min-height:44px;min-width:44px;padding:0 12px;font:inherit;font-size:15px;cursor:pointer;display:inline-flex;align-items:center;justify-content:center;gap:6px}
button:focus-visible{outline:2px solid var(--accent);outline-offset:2px}
button.on{background:var(--accent);color:var(--accent-ink);border-color:var(--accent)}
button.primary{background:var(--accent);color:var(--accent-ink);border-color:var(--accent);font-weight:600}
button:disabled{opacity:.6}
.ic{font-size:20px;padding:0}

/* 상단 바 */
header{display:flex;align-items:center;gap:8px;padding:calc(env(safe-area-inset-top,0px) + 8px) 10px 8px;background:var(--panel);border-bottom:1px solid var(--line)}
header h1{font-size:16px;margin:0;flex:1;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
#status{font-size:12px;color:var(--muted);display:block;font-weight:400}

/* 캔버스 */
.layer-list{display:flex;flex-direction:column;gap:6px}
.layer-row{display:flex;gap:6px;align-items:stretch}
.layer-row .eye{flex:0 0 48px;font-size:18px;padding:0}
.layer-row .lname{flex:1;justify-content:flex-start;gap:10px;padding:5px 8px;min-width:0}
.layer-row .lname img{width:64px;height:36px;background:#fff;border:1px solid var(--line);border-radius:4px;flex:0 0 auto;
  background-image:linear-gradient(45deg,#e4e7ee 25%,transparent 25%,transparent 75%,#e4e7ee 75%),linear-gradient(45deg,#e4e7ee 25%,transparent 25%,transparent 75%,#e4e7ee 75%);background-size:10px 10px;background-position:0 0,5px 5px}
.layer-row .lname span{overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.layer-row.on .lname{background:var(--accent);color:var(--accent-ink);border-color:var(--accent)}
.dlg-wrap{position:fixed;inset:0;z-index:50;background:rgba(10,15,30,.45);display:flex;align-items:center;justify-content:center;padding:20px}
.dlg-wrap[hidden]{display:none}
.dlg{background:var(--panel);color:var(--ink);border-radius:16px;padding:20px;width:min(360px,100%);box-shadow:0 10px 40px rgba(0,0,0,.3)}
.dlg p{margin:0 0 16px;white-space:pre-line;line-height:1.5;font-size:15px}
.dlg input{width:100%;min-height:44px;margin-bottom:16px;padding:0 12px;font:inherit;font-size:16px;border:1px solid var(--line);border-radius:10px;background:var(--soft);color:var(--ink)}
.dlg-btns{display:flex;gap:8px;justify-content:flex-end}
.merge-bar{display:flex;gap:6px;align-items:center;margin-top:10px;padding:8px;border-radius:12px;background:var(--soft);border:1px solid var(--accent)}
.merge-bar[hidden],.layer-actions[hidden],.menu[hidden]{display:none}
.merge-bar span{flex:1;font-size:14px}
.layer-row.chk .lname{border-style:dashed}
.layer-row.chk.picked .lname{background:var(--soft);border:2px solid var(--accent);color:var(--ink)}
.layer-actions{display:grid;grid-template-columns:repeat(3,1fr);gap:6px;margin-top:10px}
.layer-actions button{padding:0 4px;font-size:14px}
.selbar{position:absolute;top:8px;left:50%;transform:translateX(-50%);z-index:5;display:flex;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:14px;padding:6px;box-shadow:0 4px 16px rgba(20,30,60,.18);white-space:nowrap}
.selbar[hidden]{display:none}
.selbar button{font-size:14px;padding:0 10px}
.stage{position:relative;flex:1;min-height:0;display:flex;align-items:center;justify-content:center;padding:10px}
.canvas-wrap{position:relative;background:#fff;box-shadow:0 2px 14px rgba(20,30,60,.18);aspect-ratio:16/9;width:100%;max-width:min(960px,calc((100dvh - 250px) * 16 / 9));border-radius:4px;overflow:hidden}
#selc{pointer-events:none}
.canvas-wrap canvas{position:absolute;inset:0;width:100%;height:100%;touch-action:none}

/* 타임라인 */
.timeline{background:var(--panel);border-top:1px solid var(--line);padding:8px 10px calc(env(safe-area-inset-bottom,0px) + 8px)}
.tl-bar{display:flex;gap:6px;overflow-x:auto;margin-bottom:8px;scrollbar-width:none}
.tl-bar::-webkit-scrollbar{display:none}
.tl-bar button{flex:0 0 auto;font-size:14px}
.frames{display:flex;gap:8px;overflow-x:auto;scroll-snap-type:x proximity;padding-bottom:2px}
.thumb{flex:0 0 auto;width:88px;height:50px;min-height:0;padding:0;border:2px solid var(--line);border-radius:6px;background:#fff;position:relative;overflow:hidden;scroll-snap-align:center}
.thumb.on{border-color:var(--accent);box-shadow:0 0 0 2px var(--accent)}
.thumb img{width:100%;height:100%;display:block}
.thumb span{position:absolute;left:3px;top:2px;font-size:11px;color:#445;background:rgba(255,255,255,.85);border-radius:3px;padding:0 3px}

/* 하단 도구 막대 */
.workspace{flex:1;min-height:0;display:flex}
.toolbar{flex:0 0 auto;width:70px;display:flex;flex-direction:column;align-items:center;gap:6px;background:var(--panel);border-right:1px solid var(--line);
  padding:8px 6px;padding-left:calc(env(safe-area-inset-left,0px) + 6px);overflow-y:auto;overflow-x:hidden;scrollbar-width:none;overscroll-behavior:contain}
.toolbar::-webkit-scrollbar{display:none}
.toolbar .pens{display:flex;flex-direction:column;gap:6px}
.tool{width:56px;min-width:0;min-height:54px;flex:0 0 auto;flex-direction:column;gap:2px;padding:5px 2px;line-height:1.1;border-radius:12px}
.tool small{font-size:10px;max-width:54px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.tool.on{box-shadow:0 2px 8px color-mix(in srgb,var(--accent) 40%,transparent)}
.sep{height:1px;width:40px;background:var(--line);flex:0 0 auto}
.ico{width:26px;height:26px;flex:0 0 auto;fill:none;stroke:currentColor;stroke-width:1.7;stroke-linecap:round;stroke-linejoin:round;overflow:visible}
.ico .tip{fill:var(--pen-color);stroke:currentColor;stroke-width:1.2}
.ico .soft{fill:currentColor;opacity:.16;stroke:none}
.ico .dash{stroke-dasharray:2.4 2.6}
.ic .ico{width:24px;height:24px}
.eye .ico{width:22px;height:22px}
.menu .ico{width:22px;height:22px}
.theme-modes{display:grid;grid-template-columns:repeat(5,1fr);gap:6px}
.theme-modes button{flex-direction:column;gap:4px;min-height:64px;padding:6px 2px;font-size:12px}
.theme-modes i{width:30px;height:22px;border-radius:6px;border:1px solid var(--line);display:block}
.accents{display:flex;gap:10px;flex-wrap:wrap}
.accents button{width:40px;height:40px;min-width:0;min-height:0;border-radius:50%;padding:0;border:2px solid var(--line)}
.accents button.on{outline:3px solid var(--ink);outline-offset:2px}
#colorBtn{width:48px;height:48px;min-height:0;padding:0;border-radius:50%;flex:0 0 auto}
#colorBtn i{width:30px;height:30px;border-radius:50%;border:2px solid var(--line);display:block}
#alphaBox[hidden]{display:none}
#sizeBtn{flex:0 0 auto;width:56px;min-width:0}
#sizeDot{background:currentColor;border-radius:50%;display:block}

/* 바텀 시트 */
.scrim{position:fixed;inset:0;background:rgba(10,15,30,.35);opacity:0;pointer-events:none;transition:opacity .2s;z-index:10}
.sheet{position:fixed;left:0;right:0;bottom:0;background:var(--panel);border-radius:18px 18px 0 0;padding:10px 16px calc(env(safe-area-inset-bottom,0px) + 18px);transform:translateY(105%);transition:transform .25s ease;z-index:11;max-height:75dvh;overflow:auto;max-width:560px;margin:0 auto}
.sheet.open{transform:none}
.scrim.open{opacity:1;pointer-events:auto}
.grip{width:40px;height:5px;border-radius:3px;background:var(--line);margin:0 auto 12px}
.sheet h2{font-size:14px;color:var(--muted);margin:16px 0 8px;font-weight:600}
.sheet h2:first-of-type{margin-top:0}
.swatches{display:grid;grid-template-columns:repeat(5,1fr);gap:10px}
.sw{aspect-ratio:1;border-radius:50%;border:2px solid var(--line);padding:0;min-height:0}
.sw.on{outline:3px solid var(--accent);outline-offset:2px}
input[type=color]{width:100%;height:48px;border:1px solid var(--line);border-radius:10px;background:none;padding:2px}
input[type=range]{width:100%;height:36px;accent-color:var(--accent)}
.row{display:flex;gap:8px;align-items:center}
.row>*{flex:1}
.menu{display:grid;gap:8px}
.menu button[data-erase]{flex-direction:column;align-items:flex-start;justify-content:center;gap:2px;padding:8px 14px;text-align:left}
.menu button,.menu label.btn{justify-content:flex-start;width:100%;min-height:50px;font-size:16px}
.stepper{display:flex;align-items:center;gap:8px}
.stepper input{width:64px;min-height:44px;text-align:center;font:inherit;font-size:17px;border:1px solid var(--line);border-radius:10px;background:var(--soft);color:var(--ink)}
.preview{display:flex;align-items:center;justify-content:center;height:70px;background:var(--soft);border-radius:10px}

/* 큰 화면: 도구를 넉넉하게 */
@media (min-width:900px){
  .thumb{width:112px;height:63px}
  .canvas-wrap{max-width:min(960px,calc((100dvh - 270px) * 16 / 9))}
}
@media (prefers-reduced-motion:reduce){.sheet,.scrim{transition:none}}
</style>
</head>
<body>
<svg width="0" height="0" style="position:absolute" aria-hidden="true">
  <symbol id="i-pen" viewBox="0 0 24 24"><path class="soft" d="M7.6 18.6 18.4 7.8l-2.2-2.2L5.4 16.4z"/><path d="M5.4 16.4 16.2 5.6a1.6 1.6 0 0 1 2.2 0l0 0a1.6 1.6 0 0 1 0 2.2L7.6 18.6"/><path class="tip" d="M5.4 16.4 4 20l3.6-1.4z"/><path d="M14.4 7.4l2.2 2.2"/></symbol>
  <symbol id="i-marker" viewBox="0 0 24 24"><path class="tip" d="M3 21.2c2.6.2 5.4-.1 8-.6" style="fill:none;stroke:var(--pen-color);stroke-width:3;opacity:.55"/><path class="soft" d="M8 15.6 15.8 7.8l2.8 2.8-7.8 7.8z"/><path d="M8 15.6 15.8 7.8l2.8 2.8-7.8 7.8z"/><path d="M15.8 7.8l2-2a1.4 1.4 0 0 1 2 0l.8.8a1.4 1.4 0 0 1 0 2l-2 2"/><path class="tip" d="M8 15.6l-2.4 3.6 1.2 1.2 4-1.8z"/></symbol>
  <symbol id="i-brush" viewBox="0 0 24 24"><path d="M20.6 3.4c-1.6.4-6.6 5.2-8.4 7.6"/><path d="M20.6 3.4c-.4 1.6-5.2 6.6-7.6 8.4"/><path d="M11.6 10.4l2 2"/><path class="tip" d="M11 11.6c-2.4-.4-4.4 1-4.8 3.4-.3 1.8-1 3-3 3.6 3.6 1.6 8.8.6 9.6-3 .4-1.6-.2-3.2-1.8-4z"/></symbol>
  <symbol id="i-spray" viewBox="0 0 24 24"><rect class="soft" x="4" y="10" width="9" height="11" rx="2.2"/><rect x="4" y="10" width="9" height="11" rx="2.2"/><path d="M6.4 10V7.6h4.2V10"/><path d="M8.5 7.6V5.4h3"/><path d="M4 14h9"/><circle class="tip" cx="16" cy="5" r="1"/><circle class="tip" cx="19" cy="3.2" r=".9"/><circle class="tip" cx="18.4" cy="7" r="1.1"/><circle class="tip" cx="21" cy="6.2" r=".8"/><circle class="tip" cx="20.6" cy="9.6" r=".9"/><circle class="tip" cx="17.4" cy="10" r=".7"/></symbol>
  <symbol id="i-eraser" viewBox="0 0 24 24"><path class="soft" d="M9.2 9.6l6.8 6.8-3.6 3.6H7.8L4 16.2z"/><path d="M4 16.2 13.6 6.6a1.8 1.8 0 0 1 2.6 0l3.2 3.2a1.8 1.8 0 0 1 0 2.6L12 20H7.8z"/><path d="M9.2 11l6 6"/><path d="M14 20h6.4"/></symbol>
  <symbol id="i-erase-obj" viewBox="0 0 24 24"><path class="dash" d="M2.6 7.4c2.4-3.4 4.8 2.4 7.4-.4s4.4-2.6 6-1"/><path class="soft" d="M11.8 14.2l4.4 4.4-1.6 1.6h-3.4l-2.4-2.4z"/><path d="M8.8 17.8l7.4-7.4a1.6 1.6 0 0 1 2.2 0l2.4 2.4a1.6 1.6 0 0 1 0 2.2l-5.6 5.2h-3.4z"/><path d="M12.8 13.8l4.4 4.4"/><path d="M18.4 3.2l2.8 2.8M21.2 3.2l-2.8 2.8"/></symbol>
  <symbol id="i-select" viewBox="0 0 24 24"><path class="dash" d="M12.4 3.6c4.8 0 8.6 2.4 8.6 5.6s-3.8 5.6-8.6 5.6S3.6 12.4 3.6 9.2 7.6 3.6 12.4 3.6z"/><path d="M5.6 13.2c-1 1.8-.8 3.6.6 4.6"/><path class="soft" d="M8.4 14.4l4.4 7 1-3 3-1z"/><path d="M8.4 14.4l4.4 7 1-3 3-1z"/></symbol>
  <symbol id="i-fill" viewBox="0 0 24 24"><path class="soft" d="M4.6 11.4 10.8 5.2l7.2 7.2-6.2 6.2z"/><path d="M4.6 11.4 10.8 5.2l7.2 7.2-6.2 6.2a1.6 1.6 0 0 1-2.2 0l-5-5a1.6 1.6 0 0 1 0-2.2z"/><path d="M4.6 11.4h13.4"/><path d="M10.8 5.2 8.4 2.8"/><path class="tip" d="M19.8 14.6c1.2 1.6 1.8 2.8 1.8 3.8a1.8 1.8 0 0 1-3.6 0c0-1 .6-2.2 1.8-3.8z"/></symbol>
  <symbol id="i-layers" viewBox="0 0 24 24"><path class="soft" d="M12 3.4l8.6 4.6-8.6 4.6L3.4 8z"/><path d="M12 3.4l8.6 4.6-8.6 4.6L3.4 8z"/><path d="M3.4 12.2l8.6 4.6 8.6-4.6"/><path d="M3.4 16.2l8.6 4.6 8.6-4.6"/></symbol>
  <symbol id="i-undo" viewBox="0 0 24 24"><path d="M8.6 4.6 4.4 8.8l4.2 4.2"/><path d="M4.6 8.8h9.6a5.6 5.6 0 0 1 0 11.2H9"/></symbol>
  <symbol id="i-menu" viewBox="0 0 24 24"><circle cx="5.4" cy="12" r="1.4" style="fill:currentColor"/><circle cx="12" cy="12" r="1.4" style="fill:currentColor"/><circle cx="18.6" cy="12" r="1.4" style="fill:currentColor"/></symbol>
  <symbol id="i-eye" viewBox="0 0 24 24"><path d="M2.6 12c2.4-4.4 5.6-6.6 9.4-6.6s7 2.2 9.4 6.6c-2.4 4.4-5.6 6.6-9.4 6.6S5 16.4 2.6 12z"/><circle cx="12" cy="12" r="3"/><circle cx="12" cy="12" r="1" style="fill:currentColor"/></symbol>
  <symbol id="i-eye-off" viewBox="0 0 24 24"><path d="M4.6 8.6C3.8 9.6 3.2 10.8 2.6 12c2.4 4.4 5.6 6.6 9.4 6.6 1.6 0 3-.4 4.4-1.2"/><path d="M9 5.8c1-.3 2-.4 3-.4 3.8 0 7 2.2 9.4 6.6-.6 1.2-1.4 2.4-2.2 3.4"/><path d="M3.4 3.4l17.2 17.2"/></symbol>
  <symbol id="i-palette" viewBox="0 0 24 24"><path d="M12 3.2c-5 0-8.8 3.6-8.8 8.4 0 4.6 3.6 8.2 8 8.2 1.4 0 2-.8 2-1.8 0-1.4-1.2-1.8-1.2-3 0-1 .8-1.6 1.8-1.6h2.4c2.6 0 4.6-1.6 4.6-4.4 0-3.4-3.8-5.8-8.8-5.8z"/><circle cx="7.6" cy="11.4" r="1.2" style="fill:currentColor"/><circle cx="10" cy="7.4" r="1.2" style="fill:currentColor"/><circle cx="14.6" cy="7.4" r="1.2" style="fill:currentColor"/></symbol>
</svg>
<header>
  <button class="ic" id="undo" aria-label="실행 취소"><svg class="ico"><use href="#i-undo"/></svg></button>
  <h1>애니메이션 스튜디오<span id="status"></span></h1>
  <button id="play" class="primary" aria-label="재생">▶ 재생</button>
  <button class="ic" data-open="menuSheet" aria-label="메뉴"><svg class="ico"><use href="#i-menu"/></svg></button>
</header>

<div class="workspace">
<nav class="toolbar" aria-label="그리기 도구">
  <button id="layerBtn" class="tool" data-open="layerSheet" aria-label="레이어"><svg class="ico"><use href="#i-layers"/></svg><small id="layerLabel">레이어 1</small></button>
  <span class="sep"></span>
  <button id="colorBtn" data-open="colorSheet" aria-label="색상"><i id="colorDot"></i></button>
  <button id="sizeBtn" class="tool" data-open="sizeSheet" aria-label="굵기 · 불투명도"><span id="sizeDot"></span></button>
  <span class="sep"></span>
  <div class="pens">
    <button class="tool on" data-pen="pen" aria-label="연필"><svg class="ico"><use href="#i-pen"/></svg><small>연필</small></button>
    <button class="tool" data-pen="marker" aria-label="마커"><svg class="ico"><use href="#i-marker"/></svg><small>마커</small></button>
    <button class="tool" data-pen="brush" aria-label="붓"><svg class="ico"><use href="#i-brush"/></svg><small>붓</small></button>
    <button class="tool" data-pen="spray" aria-label="스프레이"><svg class="ico"><use href="#i-spray"/></svg><small>스프레이</small></button>
    <button class="tool" data-pen="eraser" aria-label="지우개"><svg class="ico"><use href="#i-eraser"/></svg><small id="eraserLabel">픽셀</small></button>
    <button class="tool" data-pen="lasso" aria-label="선택"><svg class="ico"><use href="#i-select"/></svg><small>선택</small></button>
    <button class="tool" data-pen="fill" aria-label="채우기"><svg class="ico"><use href="#i-fill"/></svg><small>채우기</small></button>
  </div>
</nav>
<div class="stage">
  <div id="selBar" class="selbar" hidden>
    <button id="selDup">⧉ 복제</button>
    <button id="selRot">↻ 90°</button>
    <button id="selDel">🗑 삭제</button>
    <button id="selDone" class="primary">✓ 완료</button>
  </div>
  <div class="canvas-wrap">
    <canvas id="bgc" width="960" height="540"></canvas>
    <canvas id="onionc" width="960" height="540"></canvas>
    <canvas id="draw" width="960" height="540"></canvas>
    <canvas id="selc" width="960" height="540"></canvas>
  </div>
</div>

</div>
<section class="timeline">
  <div class="tl-bar">
    <button id="add">＋ 새 프레임</button>
    <button id="dup">⧉ 복제</button>
    <button id="del">🗑 삭제</button>
    <button id="left" aria-label="앞으로 이동">◀</button>
    <button id="right" aria-label="뒤로 이동">▶</button>
    <button id="clear">지우기</button>
  </div>
  <div class="frames" id="frames"></div>
</section>


<div class="scrim" id="scrim"></div>
<div class="dlg-wrap" id="dlg" hidden>
  <div class="dlg" role="alertdialog" aria-modal="true" aria-labelledby="dlgMsg">
    <p id="dlgMsg"></p>
    <input id="dlgInput" type="text" maxlength="30" hidden>
    <div class="dlg-btns"><button id="dlgNo">취소</button><button id="dlgOk" class="primary">확인</button></div>
  </div>
</div>

<div class="sheet" id="layerSheet" role="dialog" aria-label="레이어">
  <div class="grip"></div>
  <h2>레이어 <span style="font-weight:400">· 위에 있을수록 앞에 보여요</span></h2>
  <div id="layerList" class="layer-list"></div>
  <div class="layer-actions">
    <button id="layerAdd">＋ 추가</button>
    <button id="layerDup">⧉ 복제</button>
    <button id="layerUp" aria-label="위로">⬆</button>
    <button id="layerDown" aria-label="아래로">⬇</button>
    <button id="layerRename">✎ 이름</button>
    <button id="layerDel">🗑</button>
  </div>
  <div id="mergeBar" class="merge-bar" hidden>
    <span id="mergeInfo">합칠 레이어를 2개 이상 고르세요</span>
    <button id="mergeCancel">취소</button>
    <button id="mergeGo" class="primary" disabled>합치기</button>
  </div>
  <div class="menu" style="margin-top:10px"><button id="mergeBtn">🔗 레이어 합치기</button></div>
  <div class="menu" style="margin-top:8px"><button id="dimBtn" class="on">🌫 다른 레이어 흐리게 보기</button></div>
  <h2>불투명도 <span id="opVal">100</span>%</h2>
  <input type="range" id="layerOp" min="0" max="100" value="100">
</div>

<div class="sheet" id="eraserSheet" role="dialog" aria-label="지우개 종류">
  <div class="grip"></div>
  <h2>지우개 종류</h2>
  <div class="menu">
    <button data-erase="pixel" class="on"><span style="display:flex;gap:8px;align-items:center"><svg class="ico"><use href="#i-eraser"/></svg> 픽셀 지우개</span><small style="font-weight:400">문지른 부분만 지워요</small></button>
    <button data-erase="object"><span style="display:flex;gap:8px;align-items:center"><svg class="ico"><use href="#i-erase-obj"/></svg> 대상 지우개</span><small style="font-weight:400">닿은 선을 한 획 통째로 지워요</small></button>
  </div>
</div>

<div class="sheet" id="colorSheet" role="dialog" aria-label="색상">
  <div class="grip"></div>
  <h2>색상</h2>
  <div class="swatches" id="swatches"></div>
  <h2>직접 고르기</h2>
  <input type="color" id="picker" value="#1e2a3b">
  <h2>배경색</h2>
  <input type="color" id="bgColor" value="#ffffff">
</div>

<div class="sheet" id="sizeSheet" role="dialog" aria-label="굵기">
  <div class="grip"></div>
  <h2>굵기 <span id="sizeVal">4</span>px</h2>
  <div class="preview"><span id="sizePrev" style="background:currentColor;border-radius:50%;display:block"></span></div>
  <input type="range" id="size" min="1" max="60" value="4">
  <div id="alphaBox">
    <h2><span>불투명도</span> <span id="alphaVal">100</span>% <span id="alphaTool" style="font-weight:400"></span></h2>
    <input type="range" id="alpha" min="5" max="100" value="100">
  </div>
</div>

<div class="sheet" id="menuSheet" role="dialog" aria-label="메뉴">
  <div class="grip"></div>
  <h2>언어 · Language</h2>
  <div class="theme-modes" style="grid-template-columns:1fr 1fr">
    <button data-lang="ko">한국어</button>
    <button data-lang="en">English</button>
  </div>
  <h2>테마</h2>
  <div class="theme-modes" id="themeModes">
    <button data-theme-mode="auto"><i style="background:linear-gradient(135deg,#fff 50%,#212835 50%)"></i>자동</button>
    <button data-theme-mode="light"><i style="background:#fff"></i>라이트</button>
    <button data-theme-mode="dark"><i style="background:#212835"></i>다크</button>
    <button data-theme-mode="paper"><i style="background:#FBF6EC"></i>종이</button>
    <button data-theme-mode="midnight"><i style="background:#0B0E14"></i>미드나잇</button>
  </div>
  <h2>강조 색</h2>
  <div class="accents" id="accents"></div>
  <h2>재생 속도 (FPS)</h2>
  <div class="stepper">
    <button id="fpsDown" aria-label="FPS 줄이기">−</button>
    <input type="number" id="fps" min="1" max="60" value="12" inputmode="numeric">
    <button id="fpsUp" aria-label="FPS 늘리기">＋</button>
  </div>
  <h2>보기</h2>
  <div class="menu"><button id="onion" class="on">👻 어니언 스킨 (이전 프레임 표시)</button></div>
  <h2>파일</h2>
  <div class="menu">
    <button id="save">💾 작업 저장 (.json)</button>
    <label class="btn">📂 작업 불러오기<input type="file" id="load" accept=".json,application/json" hidden></label>
    <button id="export" class="primary">🎞 MP4로 내보내기</button>
  </div>
</div>

<script>
/* ===== 언어 (한국어 / English) =====
 원문(한국어)을 키로 쓰고, 영어일 때만 사전에서 바꿔 끼움. {n} 같은 자리표시자 지원 */
const EN={
'2D 애니메이션 스튜디오':'2D Animation Studio','애니메이션 스튜디오':'Animation Studio','실행 취소':'Undo','재생':'Play','▶ 재생':'▶ Play','■ 정지':'■ Stop','정지':'Stop','메뉴':'Menu',
'그리기 도구':'Drawing tools','레이어':'Layers','색상':'Color','굵기':'Size','연필':'Pencil','마커':'Marker','붓':'Brush','스프레이':'Spray','지우개':'Eraser',
'픽셀':'Pixel','대상':'Stroke','선택':'Select','채우기':'Fill','⧉ 복제':'⧉ Duplicate','🗑 삭제':'🗑 Delete','✓ 완료':'✓ Done','↻ 90°':'↻ 90°',
'＋ 새 프레임':'＋ New frame','앞으로 이동':'Move earlier','뒤로 이동':'Move later','지우기':'Clear','취소':'Cancel','확인':'OK',
'· 위에 있을수록 앞에 보여요':'· Upper layers appear in front','＋ 추가':'＋ Add','위로':'Move up','아래로':'Move down','✎ 이름':'✎ Rename',
'합칠 레이어를 2개 이상 고르세요':'Pick 2 or more layers to merge','합치기':'Merge','🔗 레이어 합치기':'🔗 Merge layers','🌫 다른 레이어 흐리게 보기':'🌫 Dim other layers','불투명도':'Opacity',
'지우개 종류':'Eraser type','픽셀 지우개':'Pixel eraser','문지른 부분만 지워요':'Erases only where you rub','대상 지우개':'Stroke eraser','닿은 선을 한 획 통째로 지워요':'Erases every stroke it touches, whole',
'직접 고르기':'Custom color','배경색':'Background color','테마':'Theme','자동':'Auto','라이트':'Light','다크':'Dark','종이':'Paper','미드나잇':'Midnight','강조 색':'Accent color',
'재생 속도 (FPS)':'Playback speed (FPS)','FPS 줄이기':'Decrease FPS','FPS 늘리기':'Increase FPS','보기':'View','👻 어니언 스킨 (이전 프레임 표시)':'👻 Onion skin (show previous frames)',
'파일':'File','💾 작업 저장 (.json)':'💾 Save project (.json)','📂 작업 불러오기':'📂 Open project','🎞 MP4로 내보내기':'🎞 Export MP4','언어':'Language','굵기 · 불투명도':'Size · Opacity',
'프레임 {n}':'Frame {n}','{a} / {b} 프레임 · {f}fps':'Frame {a} / {b} · {f}fps','숨긴 레이어예요. 👁을 켜고 그려 주세요':'This layer is hidden. Turn on 👁 to draw on it.',
'레이어 {n}':'Layer {n}','{name} 복사':'{name} copy','숨기기':'Hide','보이기':'Show',
'파일을 읽지 못했습니다. 이 프로그램에서 저장한 .json 파일인지 확인하세요.':'Could not read the file. Make sure it is a .json file saved by this app.',
'합칠 레이어를 2개 이상 고르세요 ({n}개 선택)':'Pick 2 or more layers to merge ({n} selected)','{n}개 레이어 선택됨':'{n} layers selected',
'합칠 레이어가 2개 이상 있어야 해요':'You need at least 2 layers to merge',
"{n}개 레이어를 '{name}'(으)로 합칠까요?\n모든 프레임에 적용되며 되돌릴 수 없어요.":"Merge {n} layers into '{name}'?\nThis applies to every frame and can't be undone.",
'{n}개 레이어를 합쳤어요':'Merged {n} layers','레이어 이름':'Layer name',"'{name}' 레이어를 모든 프레임에서 삭제할까요?":"Delete layer '{name}' from every frame?",
'이 브라우저는 영상 녹화를 지원하지 않습니다. 최신 Chrome, Edge, Safari를 사용하세요.':'This browser cannot record video. Please use a recent Chrome, Edge or Safari.',
'이 브라우저는 MP4 녹화를 지원하지 않아 WebM으로 저장됩니다. 계속할까요?\n(최신 Chrome·Edge·Safari는 MP4를 지원합니다)':'This browser cannot record MP4, so the video will be saved as WebM. Continue?\n(Recent Chrome, Edge and Safari support MP4.)',
'내보내는 중 {p}%':'Exporting {p}%','강조 색 {name}':'Accent color {name}',
'블루':'Blue','민트':'Mint','퍼플':'Purple','코랄':'Coral','앰버':'Amber','핑크':'Pink','그래파이트':'Graphite'};
let lang='ko';
try{lang=localStorage.getItem('anim-lang')||((navigator.language||'').toLowerCase().startsWith('ko')?'ko':'en')}catch(e){}
function t(ko,v={}){let s=lang==='en'?(EN[ko]??ko):ko;for(const k in v)s=s.split('{'+k+'}').join(v[k]);return s}
// 화면에 고정된 글자(텍스트·aria-label·title)를 원문과 함께 기억
const I18N_NODES=[],I18N_ATTRS=[];
(function collect(){const w=document.createTreeWalker(document.body,NodeFilter.SHOW_TEXT);let n;
  while(n=w.nextNode()){const k=n.nodeValue.trim();if(k&&/[가-힣]/.test(k)&&!n.parentElement.closest('script'))I18N_NODES.push({n,k,raw:n.nodeValue})}
  document.querySelectorAll('[aria-label],[title]').forEach(el=>['aria-label','title'].forEach(a=>{const v=el.getAttribute(a);if(v&&/[가-힣]/.test(v))I18N_ATTRS.push({el,a,k:v})}))})();
function applyStaticLang(){document.documentElement.lang=lang;document.title=t('2D 애니메이션 스튜디오');
  I18N_NODES.forEach(o=>o.n.nodeValue=o.raw.replace(o.k,t(o.k)));I18N_ATTRS.forEach(o=>o.el.setAttribute(o.a,t(o.k)))}
const W=960,H=540,$=id=>document.getElementById(id);
const draw=$('draw'),ctx=draw.getContext('2d');
const octx=$('onionc').getContext('2d'),bctx=$('bgc').getContext('2d'),sctx=$('selc').getContext('2d');
const COLORS=['#1E2A3B','#FFFFFF','#E5484D','#F76B15','#FFC53D','#46A758','#12A594','#0090FF','#3E63DD','#8E4EC6','#D6409F','#A18072','#8B8D98','#FFB3C6','#B8E3FF'];
let state={alpha:{pen:1,marker:.4,brush:1,spray:1,fill:1},dimOthers:true,pen:'pen',eraseMode:'pixel',color:'#1E2A3B',size:4,onion:true,bg:'#ffffff'};

/* ===== 데이터 구조 =====
 프레임 = { items:[선1, 선2, ...], comp:합성 캔버스 }
 선(item) = { c:선만 담긴 잘라낸 캔버스, x, y }  — 손을 떼지 않고 그은 한 번의 선 = item 하나
 item은 변경 불가로 취급(수정 시 복제) → 실행 취소 기록은 배열 얕은 복사로 충분 */
let frames=[],cur=0,history=[],playing=false,timer=null;
const blank=(w=W,h=H)=>{const c=document.createElement('canvas');c.width=w;c.height=h;return c};
let layers=[{id:'L1',name:t('레이어 {n}',{n:1}),visible:true,opacity:1}],activeL='L1',layerSeq=1; // layers[0] = 맨 아래
const newFrame=()=>({layers:{},comp:blank()});
const F=()=>frames[cur];
const curLayer=()=>layers.find(L=>L.id===activeL);
const items=(fr=F(),lid=activeL)=>fr.layers[lid]||(fr.layers[lid]=[]);
const setItems=(arr,fr=F(),lid=activeL)=>{fr.layers[lid]=arr};
function cloneItem(it){const c=blank(it.c.width,it.c.height);c.getContext('2d').drawImage(it.c,0,0);return{c,x:it.x,y:it.y}}
function itemData(it){return it.d||(it.d=it.c.getContext('2d',{willReadFrequently:true}).getImageData(0,0,it.c.width,it.c.height).data)}
const lc=blank(),lcx=lc.getContext('2d');
function compose(fr,o={}){const x=o.target||fr.comp.getContext('2d');x.clearRect(0,0,W,H);
  layers.forEach(L=>{if(!L.visible)return;lcx.clearRect(0,0,W,H);
    (fr.layers[L.id]||[]).forEach(it=>{if(!o.skip||!o.skip.has(it))lcx.drawImage(it.c,it.x,it.y)});
    if(o.scratch&&L.id===activeL){lcx.globalAlpha=toolAlpha();lcx.drawImage(o.scratch,0,0);lcx.globalAlpha=1}
    x.globalAlpha=L.opacity*(o.dim&&state.dimOthers&&L.id!==activeL?.3:1);x.drawImage(lc,0,0);x.globalAlpha=1})}
function refresh(){compose(F());compose(F(),{target:ctx,dim:true,skip:sel?sel.set:null});updateThumb(cur);renderSel();
  if($('layerSheet').classList.contains('open'))renderLayers()}
let rafPending=false;
function liveRender(){if(rafPending)return;rafPending=true;requestAnimationFrame(()=>{rafPending=false;
  compose(F(),{target:ctx,dim:true,skip:sel?sel.set:null,scratch:drawing?sc:null})})}
function recomposeAll(){frames.forEach(fr=>compose(fr));refresh();renderOnion();renderTimeline()}
function pushHistory(){history.push({lid:activeL,items:items().slice()});if(history.length>50)history.shift()}

/* ===== 색상·도구 UI ===== */
COLORS.forEach(c=>{const b=document.createElement('button');b.className='sw';b.style.background=c;b.title=c;
  b.onclick=()=>{state.color=c;$('picker').value=c.toLowerCase();markSw()};$('swatches').appendChild(b)});
function markSw(){[...$('swatches').children].forEach(b=>b.classList.toggle('on',b.title.toLowerCase()===state.color.toLowerCase()))}
$('picker').oninput=e=>{state.color=e.target.value;markSw()};
$('bgColor').oninput=e=>{state.bg=e.target.value;paintBg();renderTimeline()};
$('size').oninput=e=>{state.size=+e.target.value;$('sizeVal').textContent=state.size};
document.querySelectorAll('[data-pen]').forEach(b=>b.onclick=()=>{if(sel&&b.dataset.pen!=='lasso')commitSel();state.pen=b.dataset.pen;
  document.querySelectorAll('[data-pen]').forEach(x=>x.classList.toggle('on',x===b))});
markSw();
function paintBg(){bctx.fillStyle=state.bg;bctx.fillRect(0,0,W,H)}
function renderOnion(){octx.clearRect(0,0,W,H);if(!state.onion||playing)return;
  if(cur>0){octx.globalAlpha=.25;octx.drawImage(frames[cur-1].comp,0,0)}
  if(cur>1){octx.globalAlpha=.1;octx.drawImage(frames[cur-2].comp,0,0)}octx.globalAlpha=1}

/* ===== 포인터 ===== */
function pos(e){const r=draw.getBoundingClientRect();return{x:(e.clientX-r.left)*W/r.width,y:(e.clientY-r.top)*H/r.height}}
const ui=()=>W/draw.getBoundingClientRect().width;
const sc=blank(),scx=sc.getContext('2d');
let drawing=false,last=null,bb=null,touched=null;
draw.addEventListener('pointerdown',e=>{if(playing)return;
  if(!curLayer().visible){flash(t('숨긴 레이어예요. 👁을 켜고 그려 주세요'));return}
  if(state.pen==='lasso'){lassoDown(e);return}
  draw.setPointerCapture(e.pointerId);const p=pos(e);
  pushHistory();
  if(state.pen==='fill'){floodFill(p.x|0,p.y|0);return}
  drawing=true;last=p;touched=new Map();bb={x0:1e9,y0:1e9,x1:-1e9,y1:-1e9};scx.clearRect(0,0,W,H);
  stroke(p,p,e.pressure)});
draw.addEventListener('pointermove',e=>{if(state.pen==='lasso'){lassoMove(e);return}
  if(!drawing)return;const evs=e.getCoalescedEvents?e.getCoalescedEvents():[e];
  for(const ev of evs.length?evs:[e]){const p=pos(ev);stroke(last,p,ev.pressure);last=p}});
['pointerup','pointercancel','pointerleave'].forEach(t=>draw.addEventListener(t,e=>{
  if(state.pen==='lasso'){if(t!=='pointerleave')lassoUp(e);return}
  if(!drawing)return;drawing=false;endStroke()}));

function strokeParams(a,b,pr){let s=state.size,alpha=1,cap='round';
  if(state.pen==='marker'){s*=2;cap='square'}
  if(state.pen==='brush'){const p=pr&&pr>0&&pr!==.5?pr:Math.max(.3,1-Math.hypot(b.x-a.x,b.y-a.y)/40);s=state.size*1.8*p}
  if(state.pen==='eraser')s*=2;return{s:Math.max(1,s),alpha,cap}}
function paintSeg(c,a,b,P,dots){c.save();c.lineCap=P.cap;c.lineJoin='round';c.globalAlpha=P.alpha;
  if(state.pen==='eraser'){c.globalCompositeOperation='destination-out';c.globalAlpha=1}
  c.strokeStyle=c.fillStyle=state.color;
  if(dots)dots.forEach(([x,y])=>c.fillRect(x,y,1.4,1.4));
  else{c.lineWidth=P.s;c.beginPath();c.moveTo(a.x,a.y);c.lineTo(b.x+.01,b.y);c.stroke()}c.restore()}
function stroke(a,b,pr){
  if(state.pen==='eraser'&&state.eraseMode==='object'){eraseObjectsAlong(a,b);return}
  const P=strokeParams(a,b,pr);let dots=null,r=P.s/2+2;
  if(state.pen==='spray'){r=state.size*1.5+2;dots=[];const n=Math.max(8,state.size*2);
    for(let i=0;i<n;i++){const g=Math.random()*Math.PI*2,q=Math.random()*state.size*1.5;dots.push([b.x+Math.cos(g)*q,b.y+Math.sin(g)*q])}}
  const sx0=Math.min(a.x,b.x)-r,sy0=Math.min(a.y,b.y)-r,sx1=Math.max(a.x,b.x)+r,sy1=Math.max(a.y,b.y)+r;
  if(state.pen==='eraser'){ // 픽셀 지우개: 닿는 선들의 픽셀을 직접 지움(수정 전 복제)
    const arr=items();
    for(let i=0;i<arr.length;i++){let it=arr[i];
      if(sx1<it.x||sy1<it.y||sx0>it.x+it.c.width||sy0>it.y+it.c.height)continue;
      if(!touched.has(it)){const cl=cloneItem(it);arr[i]=cl;touched.set(cl,1);it=cl}
      const c=it.c.getContext('2d');c.save();c.translate(-it.x,-it.y);paintSeg(c,a,b,P);c.restore();it.d=null}
    liveRender();return}
  bb.x0=Math.min(bb.x0,sx0);bb.y0=Math.min(bb.y0,sy0);bb.x1=Math.max(bb.x1,sx1);bb.y1=Math.max(bb.y1,sy1);
  paintSeg(scx,a,b,P,dots);liveRender()}
function endStroke(){
  if(state.pen==='eraser'){
    if(state.eraseMode==='pixel'){ // 반투명 찌꺼기 정리 + 다 지워진 선 제거
      setItems(items().filter(it=>{if(!touched.has(it))return true;
        const id=it.c.getContext('2d').getImageData(0,0,it.c.width,it.c.height),d=id.data;let any=false;
        for(let i=3;i<d.length;i+=4){if(d[i]<24)d[i]=0;else any=true}
        it.c.getContext('2d').putImageData(id,0,0);it.d=null;return any}))}
    refresh();return}
  const x0=Math.max(0,Math.floor(bb.x0)),y0=Math.max(0,Math.floor(bb.y0)),x1=Math.min(W,Math.ceil(bb.x1)),y1=Math.min(H,Math.ceil(bb.y1));
  if(x1>x0&&y1>y0){const c=blank(x1-x0,y1-y0),cc=c.getContext('2d');cc.globalAlpha=toolAlpha();cc.drawImage(sc,x0,y0,x1-x0,y1-y0,0,0,x1-x0,y1-y0);items().push({c,x:x0,y:y0})}
  scx.clearRect(0,0,W,H);refresh()}

// 앱 안 대화상자 (일부 앱 내 브라우저·미리보기 화면은 confirm/prompt/alert를 막아서 직접 구현)
function uiDialog(msg,{input=null,cancel=true}={}){return new Promise(res=>{
  const d=$('dlg'),inp=$('dlgInput');$('dlgMsg').textContent=msg;inp.hidden=input===null;inp.value=input??'';
  $('dlgNo').hidden=!cancel;d.hidden=false;(input!==null?inp:$('dlgOk')).focus();
  const done=v=>{d.hidden=true;$('dlgOk').onclick=$('dlgNo').onclick=inp.onkeydown=null;res(v)};
  $('dlgOk').onclick=()=>done(input!==null?inp.value:true);$('dlgNo').onclick=()=>done(input!==null?null:false);
  inp.onkeydown=e=>{if(e.key==='Enter')done(inp.value);if(e.key==='Escape')done(null)}})}
const uiConfirm=m=>uiDialog(m);const uiPrompt=(m,v)=>uiDialog(m,{input:v});const uiAlert=m=>uiDialog(m,{cancel:false});
const TOOL_NAMES={pen:'연필',marker:'마커',brush:'붓',spray:'스프레이',fill:'채우기'};
const toolAlpha=()=>state.alpha[state.pen]??1;
function flash(msg){$('status').textContent=msg;clearTimeout(flash.t);flash.t=setTimeout(renderTimeline,2200)}
/* ===== 선 맞히기(대상 지우개·선택 공용) ===== */
function hits(it,px,py,r){
  if(px<it.x-r||py<it.y-r||px>it.x+it.c.width+r||py>it.y+it.c.height+r)return false;
  const d=itemData(it),w=it.c.width,h=it.c.height,st=Math.max(1,r/4|0);
  for(let dy=-r;dy<=r;dy+=st)for(let dx=-r;dx<=r;dx+=st){if(dx*dx+dy*dy>r*r)continue;
    const lx=Math.round(px+dx-it.x),ly=Math.round(py+dy-it.y);
    if(lx>=0&&ly>=0&&lx<w&&ly<h&&d[(ly*w+lx)*4+3]>40)return true}return false}
function itemsAlong(a,b,r,list,out){const n=Math.max(1,Math.ceil(Math.hypot(b.x-a.x,b.y-a.y)/Math.max(2,r/2)));
  for(let k=0;k<=n;k++){const x=a.x+(b.x-a.x)*k/n,y=a.y+(b.y-a.y)*k/n;list.forEach(it=>{if(!out.has(it)&&hits(it,x,y,r))out.add(it)})}return out}
function eraseObjectsAlong(a,b){const r=Math.max(4,state.size*.75+3*ui());
  const del=itemsAlong(a,b,r,items(),new Set());if(del.size){setItems(items().filter(it=>!del.has(it)));refresh()}}

/* ===== 채우기: 채워진 영역도 하나의 대상 ===== */
function floodFill(x,y){
  const d=ctx.getImageData(0,0,W,H).data,i0=(y*W+x)*4,t=[d[i0],d[i0+1],d[i0+2],d[i0+3]];
  const m=new Uint8Array(W*H);const match=p=>{const i=p*4;return !m[p]&&Math.abs(d[i]-t[0])<32&&Math.abs(d[i+1]-t[1])<32&&Math.abs(d[i+2]-t[2])<32&&Math.abs(d[i+3]-t[3])<32};
  let x0=W,y0=H,x1=0,y1=0;const st=[y*W+x];
  while(st.length){const p=st.pop();if(!match(p))continue;let l=p,rr=p;const row=p-p%W;
    while(l>row&&match(l-1))l--;while(rr<row+W-1&&match(rr+1))rr++;
    for(let q=l;q<=rr;q++){m[q]=1;if(q>=W&&match(q-W))st.push(q-W);if(q<W*H-W&&match(q+W))st.push(q+W)}
    const yy=(p-p%W)/W;x0=Math.min(x0,l-row);x1=Math.max(x1,rr-row);y0=Math.min(y0,yy);y1=Math.max(y1,yy)}
  if(x1<x0){history.pop();return}
  const w=x1-x0+1,h=y1-y0+1,c=blank(w,h),cx=c.getContext('2d'),id=cx.createImageData(w,h);
  const col=parseInt(state.color.slice(1),16),f=[col>>16&255,col>>8&255,col&255,Math.round(255*toolAlpha())];
  for(let yy=0;yy<h;yy++)for(let xx=0;xx<w;xx++)if(m[(yy+y0)*W+xx+x0])id.data.set(f,(yy*w+xx)*4);
  cx.putImageData(id,0,0);items().push({c,x:x0,y:y0});refresh()}

/* ===== 선택 도구: 선을 그어 닿은 선 전체 선택 → 이동/확대·축소/회전/복제 =====
 sel = { set, items, 원래 상자(x0,y0,w0,h0), 현재 중심(cx,cy), 배율 k, 회전 rot(라디안) } */
let sel=null,pick=null,drag=null;const ptrs=new Map();
const selC0=()=>({x:sel.x0+sel.w0/2,y:sel.y0+sel.h0/2});
const selHalf=()=>({hw:sel.w0*sel.k/2,hh:sel.h0*sel.k/2});
function selMatrix(s=sel){const c={x:s.x0+s.w0/2,y:s.y0+s.h0/2};
  return new DOMMatrix().translate(s.cx,s.cy).rotate(s.rot*180/Math.PI).scale(s.k).translate(-c.x,-c.y)}
function toLocal(p){const dx=p.x-sel.cx,dy=p.y-sel.cy,c=Math.cos(-sel.rot),s=Math.sin(-sel.rot);return{x:dx*c-dy*s,y:dx*s+dy*c}}
function toGlobal(l){const c=Math.cos(sel.rot),s=Math.sin(sel.rot);return{x:sel.cx+l.x*c-l.y*s,y:sel.cy+l.x*s+l.y*c}}
function localCorners(){const{hw,hh}=selHalf();return[[-hw,-hh],[hw,-hh],[-hw,hh],[hw,hh]]}
const rotHandleLocal=()=>({x:0,y:-selHalf().hh-34*ui()});
function hitKind(p){const r=22*ui(),l=toLocal(p),rh=rotHandleLocal();
  if(Math.hypot(l.x-rh.x,l.y-rh.y)<r)return'rotate';
  if(localCorners().some(([x,y])=>Math.hypot(l.x-x,l.y-y)<r))return'scale';
  const{hw,hh}=selHalf(),m=10*ui();if(Math.abs(l.x)<=hw+m&&Math.abs(l.y)<=hh+m)return'move';return null}
const ang=(p)=>Math.atan2(p.y-sel.cy,p.x-sel.cx);
function snapRot(r){const st=Math.PI/2,n=Math.round(r/st);return Math.abs(r-n*st)<0.07?n*st:r}

function lassoDown(e){draw.setPointerCapture(e.pointerId);const p=pos(e);ptrs.set(e.pointerId,p);
  if(sel){
    if(ptrs.size===2){const[a,b]=[...ptrs.values()];
      drag={type:'pinch',d0:Math.hypot(a.x-b.x,a.y-b.y)||1,a0:Math.atan2(b.y-a.y,b.x-a.x),k0:sel.k,rot0:sel.rot,cx0:sel.cx,cy0:sel.cy,mx:(a.x+b.x)/2,my:(a.y+b.y)/2};return}
    const kind=hitKind(p);
    if(kind==='rotate'){drag={type:'rotate',a0:ang(p),rot0:sel.rot};return}
    if(kind==='scale'){const l=toLocal(p);drag={type:'scale',d0:Math.hypot(l.x,l.y)||1,k0:sel.k};return}
    if(kind==='move'){drag={type:'move',ox:p.x-sel.cx,oy:p.y-sel.cy};return}
    commitSel()}
  if(ptrs.size===1){pick={pts:[p],set:new Set()};itemsAlong(p,p,8*ui(),items(),pick.set);renderSel()}}
function lassoMove(e){if(!ptrs.has(e.pointerId))return;const p=pos(e);ptrs.set(e.pointerId,p);
  if(pick){const a=pick.pts[pick.pts.length-1];pick.pts.push(p);itemsAlong(a,p,8*ui(),items(),pick.set);renderSel();return}
  if(!drag||!sel)return;const minK=8/Math.min(sel.w0,sel.h0);
  if(drag.type==='move'){sel.cx=p.x-drag.ox;sel.cy=p.y-drag.oy}
  else if(drag.type==='scale'){const l=toLocal(p);sel.k=Math.max(minK,drag.k0*Math.hypot(l.x,l.y)/drag.d0)}
  else if(drag.type==='rotate'){sel.rot=snapRot(drag.rot0+ang(p)-drag.a0)}
  else if(drag.type==='pinch'&&ptrs.size>=2){const[a,b]=[...ptrs.values()];
    sel.k=Math.max(minK,drag.k0*Math.hypot(a.x-b.x,a.y-b.y)/drag.d0);
    sel.rot=snapRot(drag.rot0+Math.atan2(b.y-a.y,b.x-a.x)-drag.a0);
    sel.cx=drag.cx0+(a.x+b.x)/2-drag.mx;sel.cy=drag.cy0+(a.y+b.y)/2-drag.my}
  renderSel()}
function lassoUp(e){ptrs.delete(e.pointerId);
  if(pick){const set=pick.set;pick=null;if(set.size)makeSel(set);else renderSel();return}
  if(drag&&drag.type==='pinch'&&ptrs.size===1){const q=[...ptrs.values()][0];drag={type:'move',ox:q.x-sel.cx,oy:q.y-sel.cy};return}
  if(!ptrs.size)drag=null}
function makeSel(set,noHist){if(!noHist)pushHistory();let x0=1e9,y0=1e9,x1=-1e9,y1=-1e9;
  set.forEach(it=>{x0=Math.min(x0,it.x);y0=Math.min(y0,it.y);x1=Math.max(x1,it.x+it.c.width);y1=Math.max(y1,it.y+it.c.height)});
  sel={set,items:items().filter(it=>set.has(it)),x0,y0,w0:x1-x0,h0:y1-y0,cx:(x0+x1)/2,cy:(y0+y1)/2,k:1,rot:0};refresh()}
function transformItem(it,m,s){
  if(s.k===1&&s.rot===0){const dx=s.cx-(s.x0+s.w0/2),dy=s.cy-(s.y0+s.h0/2);return{c:it.c,x:Math.round(it.x+dx),y:Math.round(it.y+dy),d:null}}
  const pts=[[it.x,it.y],[it.x+it.c.width,it.y],[it.x,it.y+it.c.height],[it.x+it.c.width,it.y+it.c.height]].map(([x,y])=>m.transformPoint(new DOMPoint(x,y)));
  const bx=Math.floor(Math.min(...pts.map(p=>p.x)))-1,by=Math.floor(Math.min(...pts.map(p=>p.y)))-1;
  const w=Math.ceil(Math.max(...pts.map(p=>p.x)))+1-bx,h=Math.ceil(Math.max(...pts.map(p=>p.y)))+1-by;
  const c=blank(Math.max(1,w),Math.max(1,h)),cx=c.getContext('2d');cx.imageSmoothingQuality='high';
  cx.setTransform(new DOMMatrix().translate(-bx,-by).multiply(m));cx.drawImage(it.c,it.x,it.y);return{c,x:bx,y:by}}
function commitSel(){if(!sel)return[];const s=sel,m=selMatrix(s);sel=null;drag=null;
  const changed=s.k!==1||s.rot!==0||s.cx!==s.x0+s.w0/2||s.cy!==s.y0+s.h0/2;const out=[];
  if(changed)setItems(items().map(it=>{if(!s.set.has(it))return it;const n=transformItem(it,m,s);out.push(n);return n}));
  else{history.pop();out.push(...s.items)}
  refresh();return out}
function duplicateSel(){if(!sel)return;const placed=commitSel();pushHistory();
  const off=20;const copies=placed.map(it=>({c:it.c,x:it.x+off,y:it.y+off}));items().push(...copies);makeSel(new Set(copies),true)}
function deleteSel(){if(!sel)return;const s=sel;sel=null;drag=null;setItems(items().filter(it=>!s.set.has(it)));refresh()}
function rotateSel90(){if(!sel)return;sel.rot=snapRot(sel.rot+Math.PI/2);renderSel()}

function renderSel(){sctx.clearRect(0,0,W,H);const u=ui(),acc=getComputedStyle(document.documentElement).getPropertyValue('--accent').trim()||'#3B6FD8';
  $('selBar').hidden=!sel;
  sctx.save();sctx.strokeStyle=acc;
  if(pick){sctx.lineWidth=2*u;sctx.setLineDash([6*u,4*u]);sctx.beginPath();pick.pts.forEach((p,i)=>i?sctx.lineTo(p.x,p.y):sctx.moveTo(p.x,p.y));sctx.stroke();
    sctx.setLineDash([]);sctx.lineWidth=1.5*u;sctx.fillStyle='rgba(59,111,216,.12)';
    pick.set.forEach(it=>{sctx.fillRect(it.x,it.y,it.c.width,it.c.height);sctx.strokeRect(it.x,it.y,it.c.width,it.c.height)})}
  if(sel){sctx.save();sctx.setTransform(selMatrix());sctx.imageSmoothingQuality='high';sel.items.forEach(it=>sctx.drawImage(it.c,it.x,it.y));sctx.restore();
    const{hw,hh}=selHalf(),rh=rotHandleLocal();
    sctx.translate(sel.cx,sel.cy);sctx.rotate(sel.rot);
    sctx.lineWidth=1.5*u;sctx.setLineDash([6*u,4*u]);sctx.strokeRect(-hw,-hh,hw*2,hh*2);sctx.setLineDash([]);
    sctx.beginPath();sctx.moveTo(0,-hh);sctx.lineTo(rh.x,rh.y);sctx.stroke();
    localCorners().forEach(([x,y])=>{sctx.beginPath();sctx.arc(x,y,9*u,0,Math.PI*2);sctx.fillStyle='#fff';sctx.fill();sctx.lineWidth=2.5*u;sctx.stroke()});
    sctx.beginPath();sctx.arc(rh.x,rh.y,11*u,0,Math.PI*2);sctx.fillStyle=acc;sctx.fill();
    sctx.strokeStyle='#fff';sctx.lineWidth=2*u;sctx.beginPath();sctx.arc(rh.x,rh.y,5*u,-Math.PI*.9,Math.PI*.5);sctx.stroke()}
  sctx.restore()}
window.addEventListener('resize',renderSel);


$('selDup').onclick=duplicateSel;$('selRot').onclick=rotateSel90;$('selDel').onclick=deleteSel;$('selDone').onclick=()=>commitSel();
/* ===== 실행 취소 / 지우기 ===== */
function undo(){if(drawing)return;if(sel){sel=null;drag=null}if(!history.length){refresh();return}{const h=history.pop();F().layers[h.lid]=h.items}refresh()}
$('undo').onclick=undo;
$('clear').onclick=()=>{sel=null;pushHistory();setItems([]);refresh()};
document.addEventListener('keydown',e=>{if((e.ctrlKey||e.metaKey)&&e.key==='z'){e.preventDefault();undo()}
  if(e.target.tagName==='INPUT')return;
  if(e.key==='ArrowLeft'&&cur>0)loadFrame(cur-1);if(e.key==='ArrowRight'&&cur<frames.length-1)loadFrame(cur+1);
  if(e.key===' '){e.preventDefault();togglePlay()}});

/* ===== 타임라인 ===== */
function loadFrame(i){if(sel)commitSel();cur=i;history=[];refresh();renderOnion();renderTimeline()}
function thumbURL(fr){const c=blank(192,108),x=c.getContext('2d');x.fillStyle=state.bg;x.fillRect(0,0,192,108);x.drawImage(fr.comp,0,0,192,108);return c.toDataURL()}
function updateThumb(i){const img=$('frames').children[i]?.querySelector('img');if(img)img.src=thumbURL(frames[i])}
function renderTimeline(){const box=$('frames');box.innerHTML='';
  frames.forEach((f,i)=>{const b=document.createElement('button');b.className='thumb'+(i===cur?' on':'');
    b.innerHTML=`<img alt="${t('프레임 {n}',{n:i+1})}"><span>${i+1}</span>`;b.querySelector('img').src=thumbURL(f);
    b.onclick=()=>{if(!playing)loadFrame(i)};box.appendChild(b)});
  box.children[cur]?.scrollIntoView({block:'nearest',inline:'nearest'});
  $('status').textContent=t('{a} / {b} 프레임 · {f}fps',{a:cur+1,b:frames.length,f:fpsVal()})}
function withCommit(fn){return()=>{if(playing)return;if(sel)commitSel();fn()}}
$('add').onclick=withCommit(()=>{frames.splice(cur+1,0,newFrame());loadFrame(cur+1)});
$('dup').onclick=withCommit(()=>{const f=newFrame();for(const k in F().layers)f.layers[k]=F().layers[k].slice();compose(f);frames.splice(cur+1,0,f);loadFrame(cur+1)});
$('del').onclick=withCommit(()=>{if(frames.length===1){pushHistory();setItems([]);refresh();return}frames.splice(cur,1);loadFrame(Math.min(cur,frames.length-1))});
$('left').onclick=withCommit(()=>{if(cur>0){[frames[cur-1],frames[cur]]=[frames[cur],frames[cur-1]];loadFrame(cur-1)}});
$('right').onclick=withCommit(()=>{if(cur<frames.length-1){[frames[cur+1],frames[cur]]=[frames[cur],frames[cur+1]];loadFrame(cur+1)}});
$('onion').onclick=e=>{state.onion=!state.onion;e.currentTarget.classList.toggle('on',state.onion);renderOnion()};

/* ===== 재생 ===== */
function fpsVal(){return Math.min(60,Math.max(1,+$('fps').value||12))}
$('fps').onchange=()=>{$('fps').value=fpsVal();renderTimeline();if(playing){togglePlay();togglePlay()}};
$('play').onclick=togglePlay;
function togglePlay(){if(sel)commitSel();
  if(playing){clearInterval(timer);playing=false;$('play').textContent=t('▶ 재생');loadFrame(cur);return}
  playing=true;$('play').textContent=t('■ 정지');octx.clearRect(0,0,W,H);let i=cur;
  timer=setInterval(()=>{i=(i+1)%frames.length;ctx.clearRect(0,0,W,H);ctx.drawImage(frames[i].comp,0,0);cur=i;
    [...$('frames').children].forEach((b,k)=>b.classList.toggle('on',k===i))},1000/fpsVal())}

/* ===== 저장 / 불러오기 (선 단위로 저장) ===== */
function download(blob,name){const a=document.createElement('a');a.href=URL.createObjectURL(blob);a.download=name;
  document.body.appendChild(a);a.click();a.remove();setTimeout(()=>URL.revokeObjectURL(a.href),2000)}
$('save').onclick=()=>{if(sel)commitSel();
  const ser=it=>({x:it.x,y:it.y,src:it.c.toDataURL('image/png')});
  const data={version:3,width:W,height:H,fps:fpsVal(),bg:state.bg,activeL,layers:layers.map(L=>({...L})),
    frames:frames.map(fr=>({layers:Object.fromEntries(layers.map(L=>[L.id,(fr.layers[L.id]||[]).map(ser)]))}))};
  download(new Blob([JSON.stringify(data)],{type:'application/json'}),'animation.json')};
const loadImg=src=>new Promise((res,rej)=>{const im=new Image();im.onload=()=>res(im);im.onerror=rej;im.src=src});
const imgItem=(im,x,y)=>{const c=blank(im.width,im.height);c.getContext('2d').drawImage(im,0,0);return{c,x,y}};
const loadItems=list=>Promise.all(list.map(async it=>imgItem(await loadImg(it.src),it.x,it.y)));
$('load').onchange=async e=>{const file=e.target.files[0];if(!file)return;
  try{const data=JSON.parse(await file.text());let L,fr;
    if(data.version>=3){L=data.layers.map(l=>({id:String(l.id),name:l.name,visible:l.visible!==false,opacity:l.opacity??1}));
      fr=await Promise.all(data.frames.map(async f=>{const n=newFrame();for(const l of L)n.layers[l.id]=await loadItems(f.layers[l.id]||[]);return n}))}
    else{L=[{id:'L1',name:t('레이어 {n}',{n:1}),visible:true,opacity:1}];
      fr=await Promise.all(data.frames.map(async f=>{const n=newFrame();
        n.layers.L1=data.version>=2?await loadItems(f.items):[imgItem(await loadImg(f),0,0)];return n}))}
    sel=null;layers=L;activeL=L.some(l=>l.id===data.activeL)?data.activeL:L[L.length-1].id;
    layerSeq=Math.max(L.length,...L.map(l=>parseInt(String(l.id).replace(/\D/g,''))||0));
    frames=fr.length?fr:[newFrame()];$('fps').value=data.fps||12;state.bg=data.bg||'#ffffff';$('bgColor').value=state.bg;paintBg();
    cur=0;frames.forEach(f=>compose(f));renderLayers();loadFrame(0)}
  catch(err){console.error(err);uiAlert(t('파일을 읽지 못했습니다. 이 프로그램에서 저장한 .json 파일인지 확인하세요.'))}
  e.target.value=''};

/* ===== 레이어 ===== */
function layerThumb(L){const c=blank(96,54),x=c.getContext('2d'),k=96/W;
  (F().layers[L.id]||[]).forEach(it=>x.drawImage(it.c,it.x*k,it.y*k,it.c.width*k,it.c.height*k));return c.toDataURL()}
function renderLayers(){const box=$('layerList');box.innerHTML='';
  $('mergeBar').hidden=!mergeMode;$('mergeBtn').parentElement.hidden=mergeMode;document.querySelector('.layer-actions').hidden=mergeMode;
  [...layers].reverse().forEach(L=>{const row=document.createElement('div');row.className='layer-row'+(mergeMode?' chk'+(mergeSel.has(L.id)?' picked':''):(L.id===activeL?' on':''));
    const eye=document.createElement('button');eye.className='eye';eye.innerHTML=`<svg class="ico"><use href="#${L.visible?'i-eye':'i-eye-off'}"/></svg>`;eye.setAttribute('aria-label',t(L.visible?'숨기기':'보이기'));
    eye.onclick=()=>{L.visible=!L.visible;if(sel)commitSel();recomposeAll();renderLayers()};
    const pick=document.createElement('button');pick.className='lname';
    pick.innerHTML=`<img alt=""><span></span>`;pick.querySelector('img').src=layerThumb(L);
    pick.querySelector('span').textContent=(mergeMode?(mergeSel.has(L.id)?'☑ ':'☐ '):'')+L.name+(L.opacity<1?` · ${Math.round(L.opacity*100)}%`:'');
    pick.onclick=()=>{if(mergeMode){mergeSel.has(L.id)?mergeSel.delete(L.id):mergeSel.add(L.id);renderLayers();return}
      if(L.id===activeL)return;if(sel)commitSel();activeL=L.id;refresh();renderLayers()};
    row.append(eye,pick);box.appendChild(row)});
  const n=mergeSel.size;$('mergeInfo').textContent=n<2?t('합칠 레이어를 2개 이상 고르세요 ({n}개 선택)',{n}):t('{n}개 레이어 선택됨',{n});$('mergeGo').disabled=n<2;
  const C=curLayer();$('layerLabel').textContent=C.name;$('layerOp').value=Math.round(C.opacity*100);$('opVal').textContent=Math.round(C.opacity*100);
  $('layerUp').disabled=layers.indexOf(C)===layers.length-1;$('layerDown').disabled=layers.indexOf(C)===0;$('layerDel').disabled=layers.length===1}
function addLayer(copyFrom){if(sel)commitSel();layerSeq++;const id='L'+layerSeq,i=layers.indexOf(curLayer());
  const L={id,name:copyFrom?t('{name} 복사',{name:copyFrom.name}):t('레이어 {n}',{n:layerSeq}),visible:true,opacity:copyFrom?copyFrom.opacity:1};
  layers.splice(i+1,0,L);if(copyFrom)frames.forEach(fr=>fr.layers[id]=(fr.layers[copyFrom.id]||[]).slice());
  activeL=id;copyFrom?recomposeAll():refresh();renderLayers()}
$('dimBtn').onclick=e=>{state.dimOthers=!state.dimOthers;e.currentTarget.classList.toggle('on',state.dimOthers);refresh()};
let mergeMode=false;const mergeSel=new Set();
$('mergeBtn').onclick=()=>{if(layers.length<2){flash(t('합칠 레이어가 2개 이상 있어야 해요'));return}
  if(sel)commitSel();mergeMode=true;mergeSel.clear();mergeSel.add(activeL);renderLayers()};
$('mergeCancel').onclick=()=>{mergeMode=false;mergeSel.clear();renderLayers()};
function bakeAlpha(it,a){const c=blank(it.c.width,it.c.height),x=c.getContext('2d');x.globalAlpha=a;x.drawImage(it.c,0,0);return{c,x:it.x,y:it.y}}
$('mergeGo').onclick=async()=>{const chosen=layers.filter(L=>mergeSel.has(L.id)); // 아래 → 위 순서
  if(chosen.length<2)return;const target=chosen[chosen.length-1];
  if(!await uiConfirm(t("{n}개 레이어를 '{name}'(으)로 합칠까요?\n모든 프레임에 적용되며 되돌릴 수 없어요.",{n:chosen.length,name:target.name})))return;
  frames.forEach(fr=>{const arr=[];
    chosen.forEach(L=>(fr.layers[L.id]||[]).forEach(it=>arr.push(L.opacity<1?bakeAlpha(it,L.opacity):it)));
    chosen.forEach(L=>delete fr.layers[L.id]);fr.layers[target.id]=arr});
  layers=layers.filter(L=>L===target||!mergeSel.has(L.id));target.opacity=1;target.visible=true;
  activeL=target.id;history=[];mergeMode=false;mergeSel.clear();recomposeAll();renderLayers();
  flash(t('{n}개 레이어를 합쳤어요',{n:chosen.length}))};
$('layerAdd').onclick=()=>addLayer();
$('layerDup').onclick=()=>addLayer(curLayer());
function moveLayer(d){if(sel)commitSel();const i=layers.indexOf(curLayer()),j=i+d;if(j<0||j>=layers.length)return;
  [layers[i],layers[j]]=[layers[j],layers[i]];recomposeAll();renderLayers()}
$('layerUp').onclick=()=>moveLayer(1);$('layerDown').onclick=()=>moveLayer(-1);
$('layerRename').onclick=async()=>{const C=curLayer(),n=await uiPrompt(t('레이어 이름'),C.name);if(n&&n.trim()){C.name=n.trim().slice(0,30);renderLayers()}};
$('layerDel').onclick=async()=>{if(layers.length===1)return;const C=curLayer();if(!await uiConfirm(t("'{name}' 레이어를 모든 프레임에서 삭제할까요?",{name:C.name})))return;
  if(sel){sel=null;drag=null}const i=layers.indexOf(C);layers.splice(i,1);frames.forEach(fr=>delete fr.layers[C.id]);
  history=history.filter(h=>h.lid!==C.id);activeL=layers[Math.max(0,i-1)].id;recomposeAll();renderLayers()};
$('layerOp').oninput=e=>{curLayer().opacity=e.target.value/100;$('opVal').textContent=e.target.value;refresh()};
$('layerOp').onchange=()=>{recomposeAll();renderLayers()};
$('layerBtn').addEventListener('click',()=>renderLayers());

/* ===== 영상 내보내기 ===== */
$('export').onclick=async()=>{if(sel)commitSel();if(playing)togglePlay();
  const types=['video/mp4;codecs=avc1','video/mp4','video/webm;codecs=vp9','video/webm'];
  const mime=types.find(t=>window.MediaRecorder&&MediaRecorder.isTypeSupported(t));
  if(!mime){uiAlert(t('이 브라우저는 영상 녹화를 지원하지 않습니다. 최신 Chrome, Edge, Safari를 사용하세요.'));return}
  const isMp4=mime.startsWith('video/mp4');
  if(!isMp4&&!await uiConfirm(t('이 브라우저는 MP4 녹화를 지원하지 않아 WebM으로 저장됩니다. 계속할까요?\n(최신 Chrome·Edge·Safari는 MP4를 지원합니다)')))return;
  const out=blank(),o=out.getContext('2d'),fps=fpsVal();
  const rec=new MediaRecorder(out.captureStream(fps),{mimeType:mime,videoBitsPerSecond:6e6}),chunks=[];
  rec.ondataavailable=e=>e.data.size&&chunks.push(e.data);const done=new Promise(r=>rec.onstop=r);
  const btn=$('export');btn.disabled=true;
  const paint=i=>{o.fillStyle=state.bg;o.fillRect(0,0,W,H);o.drawImage(frames[i].comp,0,0)};
  paint(0);rec.start();
  const loops=frames.length<fps?Math.ceil(fps/frames.length):1,total=frames.length*loops;
  for(let k=0;k<total;k++){paint(k%frames.length);btn.textContent=$('status').textContent=t('내보내는 중 {p}%',{p:Math.round(k/total*100)});
    await new Promise(r=>setTimeout(r,1000/fps))}
  rec.stop();await done;
  download(new Blob(chunks,{type:mime.split(';')[0]}),isMp4?'animation.mp4':'animation.webm');
  btn.disabled=false;btn.textContent=t('🎞 MP4로 내보내기');renderTimeline()};

/* ===== 모바일 UI ===== */
const sheets=['colorSheet','sizeSheet','menuSheet','eraserSheet','layerSheet'];
function closeSheets(){if(typeof mergeMode!=='undefined'&&mergeMode){mergeMode=false;mergeSel.clear()}sheets.forEach(s=>$(s).classList.remove('open'));$('scrim').classList.remove('open')}
function openSheet(id){closeSheets();$(id).classList.add('open');$('scrim').classList.add('open')}
document.querySelectorAll('[data-open]').forEach(b=>b.addEventListener('click',()=>{const was=$(b.dataset.open).classList.contains('open');closeSheets();if(!was)openSheet(b.dataset.open)}));
$('scrim').onclick=closeSheets;
sheets.forEach(id=>{const s=$(id);let y0=null;
  s.addEventListener('touchstart',e=>{if(s.scrollTop<=0)y0=e.touches[0].clientY},{passive:true});
  s.addEventListener('touchmove',e=>{if(y0!==null&&e.touches[0].clientY-y0>70){closeSheets();y0=null}},{passive:true});
  s.addEventListener('touchend',()=>y0=null)});
function syncTool(){
  const hasA=state.pen in state.alpha,a=toolAlpha();$('alphaBox').hidden=!hasA;
  if(hasA){$('alpha').value=Math.round(a*100);$('alphaVal').textContent=Math.round(a*100);$('alphaTool').textContent='· '+t(TOOL_NAMES[state.pen])}
  $('sizeDot').style.opacity=hasA?Math.max(.15,a):1;$('sizePrev').style.opacity=hasA?Math.max(.05,a):1;document.documentElement.style.setProperty('--pen-color',state.color);$('colorDot').style.background=state.color;
  const d=Math.min(30,Math.max(4,state.size));Object.assign($('sizeDot').style,{width:d+'px',height:d+'px'});
  const p=Math.min(60,state.size);Object.assign($('sizePrev').style,{width:p+'px',height:p+'px',background:state.color})}
['picker','size'].forEach(id=>$(id).addEventListener('input',syncTool));
$('alpha').addEventListener('input',e=>{if(state.pen in state.alpha){state.alpha[state.pen]=e.target.value/100;syncTool()}});
document.querySelectorAll('[data-pen]').forEach(b=>b.addEventListener('click',syncTool));
$('swatches').addEventListener('click',()=>{syncTool();setTimeout(closeSheets,150)});
$('fpsDown').onclick=()=>{$('fps').value=fpsVal()-1;$('fps').onchange()};
$('fpsUp').onclick=()=>{$('fps').value=fpsVal()+1;$('fps').onchange()};
['export','save'].forEach(id=>$(id).addEventListener('click',closeSheets));$('load').addEventListener('change',closeSheets);
const eraserBtn=document.querySelector('[data-pen="eraser"]');
eraserBtn.addEventListener('pointerdown',()=>{eraserBtn.dataset.was=state.pen==='eraser'?'1':''});
eraserBtn.addEventListener('click',()=>{if(eraserBtn.dataset.was)openSheet('eraserSheet')});
document.querySelectorAll('[data-erase]').forEach(b=>b.onclick=()=>{state.eraseMode=b.dataset.erase;
  document.querySelectorAll('[data-erase]').forEach(x=>x.classList.toggle('on',x===b));
  $('eraserLabel').textContent=t(state.eraseMode==='pixel'?'픽셀':'대상');
  eraserBtn.querySelector('use').setAttribute('href',state.eraseMode==='pixel'?'#i-eraser':'#i-erase-obj');setTimeout(closeSheets,150)});
document.addEventListener('gesturestart',e=>e.preventDefault());

/* ===== GUI 테마 ===== */
const ACCENTS=[{n:'블루',l:'#3B6FD8',d:'#6E9CF0'},{n:'민트',l:'#0F9D84',d:'#3FD1B3'},{n:'퍼플',l:'#7A4FD6',d:'#A88BF2'},
  {n:'코랄',l:'#E0543F',d:'#FF8A73'},{n:'앰버',l:'#C77A00',d:'#F5B83D'},{n:'핑크',l:'#D23C86',d:'#F27BB5'},{n:'그래파이트',l:'#3D4656',d:'#AEB7C6'}];
let theme={mode:'auto',accent:0};
try{Object.assign(theme,JSON.parse(localStorage.getItem('anim-theme')||'{}'))}catch(e){}
const darkMQ=matchMedia('(prefers-color-scheme: dark)');
function isDark(){return theme.mode==='dark'||theme.mode==='midnight'||(theme.mode==='auto'&&darkMQ.matches)}
function applyTheme(){const root=document.documentElement;
  if(theme.mode==='auto')root.removeAttribute('data-theme');else root.setAttribute('data-theme',theme.mode);
  const A=ACCENTS[theme.accent]||ACCENTS[0];root.style.setProperty('--accent',isDark()?A.d:A.l);
  document.querySelector('meta[name="theme-color"]').content=getComputedStyle(root).getPropertyValue('--panel').trim();
  document.querySelectorAll('[data-theme-mode]').forEach(b=>b.classList.toggle('on',b.dataset.themeMode===theme.mode));
  [...$('accents').children].forEach((b,i)=>{b.classList.toggle('on',i===theme.accent);b.style.background=isDark()?ACCENTS[i].d:ACCENTS[i].l});
  try{localStorage.setItem('anim-theme',JSON.stringify(theme))}catch(e){}
  renderSel()}
ACCENTS.forEach((A,i)=>{const b=document.createElement('button');b.dataset.an=A.n;
  b.onclick=()=>{theme.accent=i;applyTheme()};$('accents').appendChild(b)});
document.querySelectorAll('[data-theme-mode]').forEach(b=>b.onclick=()=>{theme.mode=b.dataset.themeMode;applyTheme()});
darkMQ.addEventListener?.('change',applyTheme);

function applyLang(){applyStaticLang();
  // 기본 이름 형식인 레이어는 이름도 함께 바꿈
  layers.forEach(L=>{const m=L.name.match(/^(?:레이어|Layer) (\d+)$/);if(m)L.name=t('레이어 {n}',{n:m[1]})});
  [...$('accents').children].forEach(b=>{b.title=t(b.dataset.an);b.setAttribute('aria-label',t('강조 색 {name}',{name:t(b.dataset.an)}))});
  document.querySelectorAll('[data-lang]').forEach(b=>b.classList.toggle('on',b.dataset.lang===lang));
  $('play').textContent=t(playing?'■ 정지':'▶ 재생');$('play').setAttribute('aria-label',t(playing?'정지':'재생'));
  if(!$('export').disabled)$('export').textContent=t('🎞 MP4로 내보내기');
  $('eraserLabel').textContent=t(state.eraseMode==='pixel'?'픽셀':'대상');syncTool();
  try{localStorage.setItem('anim-lang',lang)}catch(e){}
  if(frames.length){renderLayers();renderTimeline()}}
document.querySelectorAll('[data-lang]').forEach(b=>b.onclick=()=>{lang=b.dataset.lang;applyLang()});

/* ===== 시작 ===== */
applyTheme();paintBg();frames=[newFrame()];syncTool();applyLang();loadFrame(0);
</script>
</body>
</html>
