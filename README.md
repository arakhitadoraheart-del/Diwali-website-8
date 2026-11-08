<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#090711">
<title>Happy Diwali ✨</title>
<style>
  :root { --gold:#ffd978; --cream:#fff2cf; --pink:#ff91bb; }
  * { box-sizing:border-box; }
  html,body { margin:0; min-height:100%; background:#090711; color:var(--cream); font-family:Georgia,"Noto Serif Devanagari",serif; }
  body { overflow-x:hidden; }
  .sky {
    min-height:100svh; position:relative; overflow:hidden; isolation:isolate;
    display:flex; flex-direction:column; align-items:center; text-align:center;
    background:radial-gradient(ellipse at 50% 70%,#332044 0%,#171126 38%,#090711 78%);
  }
  .stars,.fireworks { position:absolute; inset:0; width:100%; height:100%; pointer-events:none; }
  .stars { z-index:-1; }
  .fireworks { z-index:1; }
  .top-banner {
    position:relative; width:100%; padding:25px 12px 20px; color:#ffe7a0;
    font-size:clamp(1.25rem,4vw,2.25rem); letter-spacing:.04em;
    text-shadow:0 0 12px #ffbd55,0 0 28px #d77b37;
    border-bottom:1px solid #d7a94a55;
    background:linear-gradient(180deg,#120d1dcc,#120d1d55);
  }
  .top-banner:before,.top-banner:after {
    content:"✦  •  ✦  •  ✦  •  ✦  •  ✦"; display:block; color:#f6c96d;
    font:12px Arial,sans-serif; letter-spacing:.7em; margin:0 auto 9px;
    white-space:nowrap; overflow:hidden; max-width:95%;
  }
  .top-banner:after { margin:10px auto 0; }
  .lights { position:absolute; top:0; left:0; width:100%; height:48px; display:flex; justify-content:space-around; pointer-events:none; }
  .lights span { width:7px;height:13px;border-radius:50%;background:#ffd86a;box-shadow:0 0 8px 3px #ffbd4b; margin-top:35px; animation:twinkle 1.4s infinite alternate; }
  .lights span:nth-child(2n){animation-delay:.5s;background:#ff8c9c;box-shadow:0 0 8px 3px #ff8c9c}
  @keyframes twinkle {to{opacity:.35;filter:brightness(.7)}}
  main { width:min(760px,92vw); min-height:calc(100svh - 118px); display:flex; align-items:center; justify-content:center; padding:45px 0 70px; position:relative; z-index:2; }
  .card { width:100%; animation:appear 1s ease both; }
  @keyframes appear {from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
  .eyebrow { color:#e8bd76; letter-spacing:.28em; text-transform:uppercase; font:12px Arial,sans-serif; margin-bottom:18px; }
  h1 { color:#ffe4a0; font-size:clamp(2.7rem,9vw,5.7rem); line-height:1.05; font-weight:normal; margin:12px 0 18px; text-shadow:0 0 18px #ffb94d77,0 0 45px #ff8a4c44; }
  .subtitle { color:#f5dcb8; font-size:clamp(1rem,3vw,1.3rem); line-height:1.8; margin:0 auto 28px; max-width:560px; }
  .name-box { display:flex; gap:8px; justify-content:center; margin:0 auto 22px; max-width:430px; }
  input { min-width:0; flex:1; border:1px solid #e7bd7655; border-radius:30px; padding:13px 18px; color:#fff1cf; background:#ffffff0c; outline:none; font-size:16px; text-align:center; }
  input:focus { border-color:var(--gold); box-shadow:0 0 0 3px #ffd97822; }
  button { border:1px solid #ffe1a0; border-radius:30px; padding:14px 28px; color:#28152a; background:linear-gradient(135deg,#ffe9a9,#e7ae55); font-size:15px; letter-spacing:.05em; cursor:pointer; box-shadow:0 0 24px #ffbf5a44; transition:transform .2s,box-shadow .2s; }
  button:hover { transform:translateY(-2px); box-shadow:0 0 32px #ffbf5a88; }
  button:focus-visible { outline:3px solid white; outline-offset:4px; }
  .actions { display:flex; justify-content:center; flex-wrap:wrap; gap:12px; }
  .secondary { background:transparent; color:#ffe6b2; border-color:#d8b87888; box-shadow:none; }
  .diya { width:110px;height:60px; margin:0 auto 26px; position:relative; }
  .flame { position:absolute; left:50%; top:-13px; width:23px;height:35px; transform:translateX(-50%); background:radial-gradient(ellipse at 50% 75%,#fff8b7 0 18%,#ffc34e 42%,#ff6b31 75%,transparent 77%); border-radius:80% 10% 80% 10%; rotate:45deg; filter:drop-shadow(0 0 12px #ffb32c); animation:flicker .8s infinite alternate; }
  @keyframes flicker {to{transform:translateX(-50%) scale(.85) rotate(-8deg)}}
  .bowl { position:absolute; bottom:0; left:0; width:110px;height:37px; background:linear-gradient(#ffcf72,#9b4c27); border-radius:8px 8px 55px 55px; box-shadow:0 9px 20px #ff9e2d55; }
  .bowl:after { content:""; position:absolute; left:0;right:0;top:0;height:8px;border-radius:50%;background:#ffe5a0; }
  .hidden { display:none !important; }
  .final h1 { font-size:clamp(3.3rem,11vw,7rem); }
  .final .subtitle { font-size:clamp(1.15rem,3.3vw,1.5rem); }
  .footer { position:absolute; bottom:15px; color:#bba5a0; font:11px Arial,sans-serif; letter-spacing:.16em; z-index:2; }
  @media(max-width:480px){ .top-banner{padding-top:28px}.name-box{flex-direction:column}input{flex:auto}.lights{height:38px} }
  @media(prefers-reduced-motion:reduce){*,*:before,*:after{animation-duration:.01ms!important;animation-iteration-count:1!important;scroll-behavior:auto!important}}
</style>
</head>
<body>
<div class="sky">
  <canvas class="stars" id="stars"></canvas>
  <canvas class="fireworks" id="fireworks"></canvas>
  <div class="lights" aria-hidden="true"><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span></div>
  <header class="top-banner">दीपावली की हार्दिक शुभकामनाएँ</header>
  <main>
    <section class="card" id="welcome">
      <div class="eyebrow">A little light, a lot of love</div>
      <h1>For <span id="welcomeName">Jay Shree Ram</span></h1>
      <p class="subtitle">A little celebration is waiting for you.<br>Ready to make this Diwali sparkle?</p>
      <div class="name-box">
        <input id="recipient" type="text" maxlength="32" placeholder="Enter a name (optional)" aria-label="Greeting recipient name">
      </div>
      <button id="begin">Open your Diwali surprise ✨</button>
    </section>

    <section class="card hidden" id="message">
      <div class="diya" aria-hidden="true"><div class="flame"></div><div class="bowl"></div></div>
      <div class="eyebrow">May your home shine bright</div>
      <h1>जय श्री राम</h1>
      <p class="subtitle"><span id="messageName">Jay Shree Ram</span>, this Diwali may your days be filled with light, your heart with peace, and your life with happiness.</p>
      <p class="subtitle">There's a little magic waiting above…</p>
      <button id="launch">Tap the sky! 🎆</button>
    </section>

    <section class="card final hidden" id="final">
      <div class="eyebrow">A festival of light • love • new beginnings</div>
      <h1>Happy<br>Diwali!</h1>
      <p class="subtitle">Wishing <strong id="finalName">you</strong> and your family a Diwali filled with joy, prosperity, good health and countless beautiful moments.</p>
      <p class="subtitle">दीपों की रोशनी आपके जीवन में सुख, शांति और समृद्धि लाए।<br>शुभ दीपावली! 🪔</p>
      <div class="actions">
        <button id="replay">Celebrate again ↻</button>
        <button class="secondary" id="edit">Change name</button>
      </div>
    </section>
  </main>
  <div class="footer">✦ &nbsp; LIGHT • LOVE • HAPPINESS &nbsp; ✦</div>
</div>
<script>
(() => {
  const $ = id => document.getElementById(id);
  const welcome = $('welcome'), message = $('message'), final = $('final');
  let name = 'Jay Shree Ram';
  const show = section => [welcome,message,final].forEach(s => s.classList.toggle('hidden',s !== section));
  $('begin').addEventListener('click', () => {
    name = $('recipient').value.trim() || 'Jay Shree Ram';
    $('welcomeName').textContent = name;
    $('messageName').textContent = name;
    $('finalName').textContent = name;
    show(message);
  });
  $('launch').addEventListener('click', () => {
    show(final); burstShow();
  });
  $('replay').addEventListener('click', () => { show(welcome); $('recipient').value = name === 'Jay Shree Ram' ? '' : name; });
  $('edit').addEventListener('click', () => { show(welcome); $('recipient').value = name === 'Jay Shree Ram' ? '' : name; });

  const stars = $('stars'), sctx = stars.getContext('2d');
  const fire = $('fireworks'), ctx = fire.getContext('2d');
  let W=0,H=0,particles=[],starDots=[];
  function resize(){
    const dpr=Math.min(devicePixelRatio||1,2);
    W=innerWidth; H=innerHeight;
    [stars,fire].forEach(c=>{c.width=W*dpr;c.height=H*dpr;c.style.width=W+'px';c.style.height=H+'px';c.getContext('2d').setTransform(dpr,0,0,dpr,0,0);});
    starDots=Array.from({length:100},()=>({x:Math.random()*W,y:Math.random()*H,r:Math.random()*1.5+.3,a:Math.random()*.7+.15,p:Math.random()*6}));
  }
  addEventListener('resize',resize); resize();
  function drawStars(t){
    sctx.clearRect(0,0,W,H);
    for(const s of starDots){sctx.globalAlpha=s.a*(.65+.35*Math.sin(t/700+s.p));sctx.fillStyle='#ffe9b4';sctx.beginPath();sctx.arc(s.x,s.y,s.r,0,Math.PI*2);sctx.fill();}
    sctx.globalAlpha=1;
  }
  function burst(x,y){
    const colors=['#ffd66b','#ff78a8','#8be8ff','#d5a1ff','#fff2c2','#ff935e'];
    const count=75;
    for(let i=0;i<count;i++){const a=Math.PI*2*i/count+Math.random()*.08, speed=1.2+Math.random()*4.3;particles.push({x,y,vx:Math.cos(a)*speed,vy:Math.sin(a)*speed,life:55+Math.random()*35,max:90,size:1.2+Math.random()*2.2,color:colors[Math.floor(Math.random()*colors.length)]});}
  }
  function burstShow(){
    const points=[[.22,.32],[.75,.27],[.5,.2],[.36,.48],[.82,.52],[.57,.38]];
    points.forEach((p,i)=>setTimeout(()=>burst(W*p[0],H*p[1]),i*380));
    setTimeout(()=>burst(W*.5,H*.3),2500);
  }
  let last=0;
  function animate(t){
    drawStars(t);
    ctx.clearRect(0,0,W,H);
    if(t-last>1250 && Math.random()<.025 && !final.classList.contains('hidden')){burst(W*(.15+Math.random()*.7),H*(.15+Math.random()*.45));last=t;}
    particles=particles.filter(p=>p.life>0);
    for(const p of particles){
      p.x+=p.vx;p.y+=p.vy;p.vx*=.985;p.vy=p.vy*.985+.025;p.life--;
      ctx.globalAlpha=Math.max(0,p.life/p.max);
      ctx.fillStyle=p.color;ctx.shadowBlur=12;ctx.shadowColor=p.color;
      ctx.beginPath();ctx.arc(p.x,p.y,p.size,0,Math.PI*2);ctx.fill();
    }
    ctx.globalAlpha=1;ctx.shadowBlur=0;
    requestAnimationFrame(animate);
  }
  requestAnimationFrame(animate);
  fire.addEventListener('pointerdown',e=>{if(!final.classList.contains('hidden'))burst(e.clientX,e.clientY);});
})();
</script>
</body>
</html>
