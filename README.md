# flaxz-priv.github.io
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Campamento Facu 2000 · Summer Edition</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bowlby+One&family=Barlow+Condensed:wght@500;600;700&family=Reenie+Beanie&display=swap" rel="stylesheet">
<style>
:root{
  --forest:#23401f; --olive:#6c6b2b; --lime:#b7c06b; --butter:#f2d774; --mustard:#d49a1c;
  --choc:#35200f; --earth:#8b5b33; --cream:#efe4c4; --paper:#f9f4e2;
  --display:'Bowlby One','Arial Black',Impact,sans-serif;
  --cond:'Barlow Condensed','Arial Narrow',sans-serif;
  --hand:'Reenie Beanie','Segoe Print',cursive;
  box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
}
*,*::before,*::after{box-sizing:inherit}
html{scroll-behavior:smooth}
body{margin:0;background:var(--choc);color:var(--choc);font:500 19px/1.3 var(--cond);-webkit-text-size-adjust:100%}
body::after{content:"";position:fixed;inset:0;pointer-events:none;z-index:50;opacity:.16;
  background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='2' stitchTiles='stitch'/%3E%3CfeColorMatrix values='0 0 0 0 .2 0 0 0 0 .12 0 0 0 0 .05 0 0 0 .9 0'/%3E%3C/filter%3E%3Crect width='160' height='160' filter='url(%23n)'/%3E%3C/svg%3E")}
.mag{max-width:560px;margin:0 auto;background:var(--paper);overflow:hidden}
section{position:relative;padding:44px 22px 64px}
h2,h1{margin:0;font-family:var(--display);font-weight:400;line-height:.92;letter-spacing:-.01em}
p{margin:0 0 .7em}
.hand{font-family:var(--hand);font-size:30px;line-height:.9}
.folio{position:absolute;bottom:14px;font-size:15px;font-weight:700;letter-spacing:.08em;opacity:.75}
.folio.l{left:22px}.folio.r{right:22px}
.tape{position:absolute;width:84px;height:26px;background:rgba(242,215,116,.78);transform:rotate(-6deg);box-shadow:0 0 0 1px rgba(53,32,15,.08)}
.ht{position:absolute;pointer-events:none;background-image:radial-gradient(circle,var(--choc) 1.5px,transparent 2px);background-size:7px 7px;
  -webkit-mask-image:linear-gradient(to bottom,#000,transparent);mask-image:linear-gradient(to bottom,#000,transparent)}
.stamp{opacity:0;transform:scale(1.7) rotate(0deg);transition:opacity .25s,transform .35s cubic-bezier(.3,1.6,.5,1)}
.stamp.on{opacity:1;transform:scale(1) rotate(var(--r,-8deg))}

/* PORTADA */
.cover{background:var(--butter);padding:18px 18px 40px;min-height:100svh;display:flex;flex-direction:column}
.strip{display:flex;justify-content:space-between;gap:6px;font-weight:700;font-size:15px;letter-spacing:.1em;text-transform:uppercase;border-top:3px solid var(--choc);border-bottom:1px solid var(--choc);padding:5px 0}
.mast{position:relative;margin-top:22px}
.mast h1{font-size:clamp(38px,12.4vw,70px);color:var(--choc);text-shadow:3px 2px 0 var(--mustard);transform:rotate(-2.5deg);transform-origin:left}
.mast .facu{display:inline-block;margin:6px 0 0 4px;padding:4px 14px 8px;background:var(--forest);color:var(--paper);font-size:clamp(70px,25vw,150px);transform:rotate(1.8deg);text-shadow:4px 3px 0 var(--olive)}
.mast .yr{display:inline-block;font-family:var(--display);font-size:clamp(46px,17vw,100px);color:transparent;-webkit-text-stroke:2.5px var(--choc);transform:rotate(-4deg) translate(6px,-10px);letter-spacing:.02em}
.art{position:relative;margin:10px -4px 0;height:min(56vw,300px);flex:none}
.art svg{position:absolute;inset:0;width:100%;height:100%;clip-path:polygon(1% 4%,30% 0,62% 3%,99% 1%,100% 40%,98% 96%,64% 100%,30% 97%,0 99%,2% 50%)}
.lines{position:relative;margin-top:14px;display:grid;gap:10px}
.line{background:var(--choc);color:var(--butter);padding:8px 12px;font-size:25px;font-weight:700;line-height:1;text-transform:uppercase;width:fit-content;max-width:88%;transform:rotate(-1.4deg)}
.line.b{background:var(--paper);color:var(--choc);border:2px solid var(--choc);margin-left:8%;transform:rotate(1.2deg)}
.seal{position:absolute;right:6px;top:-58px;width:104px;height:104px;border-radius:50%;background:var(--forest);color:var(--butter);display:grid;place-items:center;text-align:center;font:700 19px/1 var(--cond);text-transform:uppercase;border:3px dashed var(--butter);outline:3px solid var(--forest);z-index:2}
.note{position:absolute;right:16px;bottom:10px;color:var(--forest);transform:rotate(-6deg);text-align:center}
.btn{display:inline-block;font:700 24px/1 var(--cond);letter-spacing:.04em;text-transform:uppercase;text-decoration:none;color:var(--paper);background:var(--forest);padding:14px 22px;border:3px solid var(--choc);box-shadow:5px 5px 0 var(--choc);cursor:pointer;transition:transform .12s,box-shadow .12s}
.btn:hover,.btn:focus-visible{transform:translate(3px,3px);box-shadow:2px 2px 0 var(--choc)}
.cover .btn{margin-top:22px;align-self:flex-start}
:focus-visible{outline:3px solid var(--mustard);outline-offset:3px}

/* CAMPAMENTO */
.camp{background:var(--paper)}
.camp h2{font-size:clamp(40px,13vw,72px);color:var(--forest);transform:rotate(-1.5deg)}
.cols{columns:2;column-gap:18px;margin-top:22px;font-size:19px}
.cols p:first-child::first-letter{font:400 3.1em/.8 var(--display);float:left;margin:4px 6px 0 0;color:var(--earth)}
.cut{margin:26px -8px 0;background:var(--lime);border:3px solid var(--choc);padding:16px 18px 18px;transform:rotate(1.4deg);position:relative;clip-path:polygon(0 3%,50% 0,100% 2%,99% 100%,48% 97%,1% 100%)}
.cut b{font:400 26px/1 var(--display);display:block;margin-bottom:6px}
.cut .hand{position:absolute;right:14px;bottom:-4px;color:var(--forest)}

/* INFO */
.info{background:var(--forest);color:var(--paper)}
.info h2{font-size:clamp(40px,13vw,68px);color:var(--butter)}
.ficha{position:relative;margin-top:30px;background:var(--cream);color:var(--choc);padding:24px 18px 20px;border:3px solid var(--choc);box-shadow:7px 7px 0 var(--mustard);transform:rotate(-1deg)}
.ficha dl{margin:0;display:grid;gap:0}
.ficha .row{display:grid;grid-template-columns:92px 1fr;align-items:baseline;gap:10px;padding:12px 0;border-bottom:2px dashed var(--earth)}
.ficha .row:last-child{border:0}
.ficha dt{font:700 17px var(--cond);letter-spacing:.1em;text-transform:uppercase;color:var(--earth)}
.ficha dd{margin:0;font:400 28px/1 var(--display);word-break:break-word}
.ficha .tape{top:-14px;left:30px}
.ficha .hand{position:absolute;right:12px;top:-34px;color:var(--butter);transform:rotate(5deg)}

/* DRESS CODE */
.dress{background:var(--olive);color:var(--paper)}
.dress .ht{right:0;top:0;width:55%;height:190px;opacity:.35;background-image:radial-gradient(circle,var(--forest) 1.6px,transparent 2.1px)}
.dress h2{position:relative;font-size:clamp(40px,13vw,68px);color:var(--paper);text-shadow:3px 3px 0 var(--choc)}
.dress h2 span{display:block;color:var(--butter);transform:translateX(18px) rotate(-2deg);margin-top:4px}
.tags{position:relative;display:flex;flex-wrap:wrap;gap:12px 10px;margin:26px 0 0}
.tag{font:700 24px/1 var(--cond);text-transform:uppercase;padding:9px 14px 9px 12px;background:var(--paper);color:var(--choc);border:2px solid var(--choc);clip-path:polygon(0 0,92% 0,100% 50%,92% 100%,0 100%)}
.tag:nth-child(2n){background:var(--butter);transform:rotate(1.6deg)}
.tag:nth-child(3n){background:var(--lime);transform:rotate(-1.8deg)}
.no{position:relative;margin-top:26px;border-top:3px solid var(--butter);padding-top:12px;font-size:21px}
.no .hand{color:var(--butter);margin-right:6px}

/* ACTIVIDADES */
.acts{background:var(--cream)}
.acts h2{font-size:clamp(40px,13vw,68px);color:var(--choc)}
.ev{position:relative;display:grid;grid-template-columns:auto 1fr;gap:4px 16px;margin-top:26px;padding-top:14px;border-top:4px solid var(--choc)}
.ev:nth-of-type(2){margin-left:14px}
.ev:nth-of-type(3){margin-right:10px}
.ev .k{grid-row:span 2;font:400 64px/.85 var(--display);color:var(--mustard);-webkit-text-stroke:2px var(--choc)}
.ev h3{margin:0;font:700 29px/1 var(--cond);text-transform:uppercase}
.ev p{margin:0}
.ev .lab{position:absolute;top:-16px;right:0;background:var(--forest);color:var(--butter);font:700 15px var(--cond);letter-spacing:.1em;text-transform:uppercase;padding:3px 9px;transform:rotate(3deg)}

/* RSVP */
.rsvp{background:var(--choc);color:var(--paper);padding-bottom:84px}
.rsvp h2{font-size:clamp(44px,15vw,84px);color:var(--butter);transform:rotate(-2deg)}
.card{position:relative;margin-top:28px;background:var(--butter);color:var(--choc);padding:26px 18px 22px;transform:rotate(.8deg);clip-path:polygon(0 2%,100% 0,99% 98%,50% 100%,0 99%)}
.card label,.card legend{display:block;font:700 18px var(--cond);letter-spacing:.1em;text-transform:uppercase;margin-bottom:6px;padding:0}
.card input[type=text]{width:100%;font:500 24px var(--cond);padding:10px 12px;background:var(--paper);border:3px solid var(--choc);border-radius:0;color:var(--choc)}
fieldset{border:0;margin:18px 0 0;padding:0}
.opts{display:flex;gap:10px}
.opts label{flex:1;margin:0;cursor:pointer}
.opts input{position:absolute;opacity:0}
.opts span{display:block;text-align:center;font:700 23px/1 var(--cond);letter-spacing:.03em;padding:13px 6px;border:3px solid var(--choc);background:var(--paper);text-transform:none}
.opts input:checked+span{background:var(--forest);color:var(--butter);transform:rotate(-1.5deg)}
.opts input:focus-visible+span{outline:3px solid var(--mustard);outline-offset:3px}
.card .btn{width:100%;margin-top:22px;background:var(--choc);color:var(--butter);border-color:var(--choc);box-shadow:5px 5px 0 var(--forest)}
.msg{min-height:1.3em;margin:14px 0 0;font-weight:700}
.end{text-align:center;margin-top:30px;color:var(--lime)}
.end b{display:block;font:400 22px var(--display);color:var(--paper);margin-bottom:2px}

@media (min-width:560px){body{font-size:21px}.cols{font-size:20px}}
@media (prefers-reduced-motion:reduce){html{scroll-behavior:auto}*{animation:none!important;transition:none!important}.stamp{opacity:1;transform:rotate(var(--r,-8deg))}}
@keyframes drop{from{opacity:0;transform:translateY(-26px) rotate(-7deg)}}
@keyframes slap{from{opacity:0;transform:scale(1.8) rotate(10deg)}}
.mast h1{animation:drop .5s .05s both cubic-bezier(.3,1.4,.5,1)}
.mast .facu{animation:drop .5s .3s both cubic-bezier(.3,1.4,.5,1)}
.mast .yr{animation:drop .5s .55s both cubic-bezier(.3,1.4,.5,1)}
.seal{animation:slap .4s .95s both cubic-bezier(.3,1.5,.5,1);transform:rotate(9deg)}
.line{animation:slap .35s both}.line:nth-child(1){animation-delay:1.15s}.line.b{animation-delay:1.3s}
</style>
</head>
<body>
<main class="mag">

<!-- 1 · PORTADA -->
<section class="cover" id="portada">
  <div class="strip"><span>Issue 01</span><span>Summer Edition</span><span>Est. 2000</span></div>
  <div class="mast">
    <h1>Campamento</h1>
    <span class="facu h1">Facu</span><br>
    <span class="yr">2000</span>
  </div>
  <div class="art" aria-hidden="true">
    <svg viewBox="0 0 320 180" preserveAspectRatio="xMidYMid slice">
      <defs><pattern id="d" width="6" height="6" patternUnits="userSpaceOnUse"><circle cx="3" cy="3" r="1.7" fill="#d49a1c"/></pattern></defs>
      <rect width="320" height="180" fill="#b7c06b"/>
      <circle cx="238" cy="52" r="34" fill="#f9f4e2"/><circle cx="238" cy="52" r="34" fill="url(#d)"/>
      <path d="M0 120 Q70 70 140 112 T320 96 V180 H0Z" fill="#6c6b2b"/>
      <path d="M0 150 Q90 112 180 146 T320 136 V180 H0Z" fill="#23401f"/>
      <g fill="#23401f" stroke="#35200f" stroke-width="2"><path d="M28 132l16-44 16 44z"/><path d="M50 138l12-34 12 34z"/><path d="M270 130l14-40 14 40z"/></g>
      <path d="M96 150l46-78 46 78z" fill="#efe4c4" stroke="#35200f" stroke-width="3"/>
      <path d="M142 72l-22 78h22z" fill="#d49a1c" opacity=".55"/>
      <path d="M130 150l12-34 12 34z" fill="#35200f"/>
      <path d="M142 72V56l16 6-16 4" fill="#d49a1c" stroke="#35200f" stroke-width="2"/>
      <path d="M0 162h320" stroke="#35200f" stroke-width="3"/>
    </svg>
    <div class="ht" style="left:0;bottom:0;width:100%;height:40%;opacity:.25;-webkit-mask-image:linear-gradient(to top,#000,transparent);mask-image:linear-gradient(to top,#000,transparent)"></div>
    <div class="note hand">¡no faltes!<br>↓</div>
  </div>
  <div class="lines">
    <div class="seal">Verano<br>2000<br>todo el día</div>
    <div class="line">Facu cumple 25</div>
    <div class="line b">06/12 · QUINTA</div>
  </div>
  <a class="btn" href="#rsvp">Confirmá tu lugar</a>
</section>

<!-- 2 · EL CAMPAMENTO -->
<section class="camp" id="campamento">
  <div class="tape" style="top:10px;right:26px;transform:rotate(7deg)"></div>
  <h2>Bienvenidos al campamento</h2>
  <div class="cols">
    <p>Este verano el cumpleaños se arma como en los viejos campamentos: carpas, juegos, equipos y una tarde que nadie quiere que termine.</p>
    <p>Traé ganas, una buena gorra y el mejor humor. Lo demás lo ponemos nosotros.</p>
  </div>
  <div class="cut">
    <b>En esta edición</b>
    La info del evento, qué ponerse, los desafíos del campamento y cómo confirmar.
    <span class="hand">pág. 3 a 6</span>
  </div>
  <span class="folio l">Campamento Facu 2000 · 2</span>
</section>

<!-- 3 · INFORMACIÓN -->
<section class="info" id="info">
  <h2>Ficha del campamento</h2>
  <div class="ficha">
    <div class="tape"></div>
    <span class="hand">anotalo en la agenda</span>
    <dl>
      <div class="row"><dt>Quién</dt><dd>Facu</dd></div>
      <div class="row"><dt>Cumple</dt><dd>25</dd></div>
      <div class="row"><dt>Día</dt><dd>06/12</dd></div>
      <div class="row"><dt>Hora</dt><dd>10:00 hs a 20:00 hs</dd></div>
      <div class="row"><dt>Dónde</dt><dd>QUINTA</dd></div>
    </dl>
  </div>
  <span class="folio r">3</span>
</section>

<!-- 4 · DRESS CODE -->
<section class="dress" id="dresscode">
  <div class="ht"></div>
  <h2>Dress code<span>modo campamento</span></h2>
  <p style="position:relative;margin-top:22px;max-width:30ch">Ropa cómoda, de las que se pueden ensuciar. Vale inspirarse en los 2000.</p>
  <div class="tags">
    <span class="tag">Verdes y tierra</span><span class="tag">Gorra</span><span class="tag">Cargo</span><span class="tag">Zapatillas o botas</span><span class="tag">Remera de banda</span><span class="tag">Campera liviana</span>
  </div>
  <div class="no"><span class="hand">mejor evitar:</span> el rosa. Este campamento es verde, amarillo y marrón.</div>
  <span class="folio l">4</span>
</section>

<!-- 5 · ACTIVIDADES (textos de ejemplo: editar a gusto) -->
<section class="acts" id="actividades">
  <h2>En el programa</h2>
  <div class="ev"><span class="lab">Desafío</span><span class="k">A</span><h3>Búsqueda del tesoro</h3><p>Pistas, mapa y un premio escondido.</p></div>
  <div class="ev"><span class="lab">Juego</span><span class="k">B</span><h3>Olimpíadas del campamento</h3><p>Equipos, pruebas absurdas y puntos.</p></div>
  <div class="ev"><span class="lab">Fogón</span><span class="k">C</span><h3>Malvaviscos y música</h3><p>Para cerrar el día como corresponde.</p></div>
  <span class="folio r">5</span>
</section>

<!-- 6 · RSVP -->
<section class="rsvp" id="rsvp">
  <h2>¿Venís?</h2>
  <form class="card" id="f" novalidate>
    <label for="n">Tu nombre</label>
    <input type="text" id="n" name="n" autocomplete="name" required>
    <fieldset><legend>Confirmás asistencia</legend>
      <div class="opts">
        <label><input type="radio" name="r" value="Sí, voy" checked><span>Sí, voy</span></label>
        <label><input type="radio" name="r" value="No puedo ir"><span>No puedo</span></label>
      </div>
    </fieldset>
    <button class="btn" type="submit">Enviar respuesta</button>
    <p class="msg" id="m" role="status" aria-live="polite"></p>
  </form>
  <div class="end"><b>Campamento Facu 2000</b>Issue 01 · Summer Edition · nos vemos en el campamento</div>
  <span class="folio r" style="color:var(--lime)">6</span>
</section>

</main>
<script>
// Reemplazar por el link real de confirmación (WhatsApp wa.me, formulario, etc.)
const RSVP='[LINK / RSVP]';
const f=document.getElementById('f'),m=document.getElementById('m');
f.addEventListener('submit',e=>{
  e.preventDefault();
  const n=f.n.value.trim();
  if(!n){m.textContent='Escribí tu nombre para continuar.';f.n.focus();return}
  if(!/^https?:/.test(RSVP)){m.textContent='Falta completar el link de confirmación ([LINK / RSVP]).';return}
  const r=f.querySelector('input[name=r]:checked').value;
  const txt=encodeURIComponent('Hola, soy '+n+'. '+r+' al Campamento Facu 2000.');
  window.open(RSVP.includes('wa.me')?RSVP+(RSVP.includes('?')?'&':'?')+'text='+txt:RSVP,'_blank','noopener');
  m.textContent='Listo, '+n+'. Te esperamos.';
});
const io=new IntersectionObserver(es=>es.forEach(x=>{if(x.isIntersecting){x.target.classList.add('on');io.unobserve(x.target)}}),{threshold:.4});
document.querySelectorAll('.stamp').forEach(s=>io.observe(s));
</script>
</body>
</html>
