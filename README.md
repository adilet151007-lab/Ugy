<!DOCTYPE html>
<html lang="kk"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Дәріс 5: Тапсырмаларды жоспарлау</title>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@400;600;700&family=IBM+Plex+Mono:wght@500;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#060914;--pn:#0d1330;--ln:#26305f;--tx:#e8ecff;--mu:#93a0d6;--c:#22d3ee;--v:#8b5cf6;--b:#3b82f6;--m:#e879f9;--g:#34d399;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:dark}
*{box-sizing:inherit;margin:0}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
html,body{height:100%;background:var(--bg);color:var(--tx);font:400 clamp(15px,1.7vw,22px)/1.45 'IBM Plex Sans','Segoe UI',system-ui,sans-serif;overflow:hidden}
body{background:radial-gradient(60% 50% at 80% 0,#1b1450 0,transparent 70%),radial-gradient(50% 40% at 0 100%,#062a4a 0,transparent 70%),var(--bg)}
body:before{content:"";position:fixed;inset:0;background:linear-gradient(var(--ln) 1px,transparent 1px) 0 0/48px 48px,linear-gradient(90deg,var(--ln) 1px,transparent 1px) 0 0/48px 48px;opacity:.14;pointer-events:none}
.s{position:absolute;inset:0;display:none;flex-direction:column;justify-content:center;gap:1.1rem;padding:clamp(18px,4vw,64px) clamp(18px,6vw,96px) 72px;overflow:auto;animation:in .6s both}
.s.on{display:flex}
@keyframes in{from{opacity:0;transform:scale(.98)}}
h1{font-size:clamp(2rem,6.4vw,5rem);line-height:1.02;font-weight:700;letter-spacing:-.02em}
h2{font-size:clamp(1.5rem,3.8vw,3rem);line-height:1.1;font-weight:700;letter-spacing:-.01em}
.mo{font-family:'IBM Plex Mono',ui-monospace,monospace}
.k{color:var(--c)}.v{color:var(--m)}.mu{color:var(--mu)}
.tag{font:500 .8rem 'IBM Plex Mono',monospace;color:var(--c)}
.q{border-left:3px solid var(--v);padding:.4rem 1rem;font-size:1.05em;background:linear-gradient(90deg,#8b5cf622,transparent)}
.row{display:flex;gap:.8rem;flex-wrap:wrap;align-items:stretch}
.bx{flex:1 1 150px;background:var(--pn);border:1px solid var(--ln);border-radius:14px;padding:.8rem 1rem}
.bx b{display:block;color:var(--c);font-family:'IBM Plex Mono',monospace}
.bx small{color:var(--mu);font-size:.85em}
.hot{border-color:var(--v);box-shadow:0 0 28px #8b5cf655;animation:pl 2s infinite}
@keyframes pl{50%{box-shadow:0 0 44px #8b5cf6aa}}
.ar{align-self:center;color:var(--c);font-family:'IBM Plex Mono',monospace}
.fl{display:flex;flex-direction:column;gap:.2rem;align-items:center;max-width:340px}
.fl .bx{width:100%;text-align:center;padding:.5rem}
.fl .ar{transform:rotate(90deg);height:1.2rem;line-height:1}
.p1{background:var(--c)}.p2{background:var(--v)}.p3{background:var(--b)}.p4{background:var(--m)}.p5{background:var(--g)}
.ch{display:inline-grid;place-items:center;min-width:48px;height:38px;padding:0 .6rem;border-radius:9px;color:#04101f;font:700 .9rem 'IBM Plex Mono',monospace}
.cpu{display:grid;place-items:center;width:110px;height:110px;border-radius:22px;background:#0a1030;border:2px solid var(--c);box-shadow:0 0 40px #22d3ee66,inset 0 0 24px #22d3ee33;font:700 1.6rem 'IBM Plex Mono',monospace;color:var(--c);animation:pl 2.4s infinite}
.g{display:flex;gap:3px;height:60px}
.g i{display:grid;place-items:center;border-radius:8px;color:#04101f;font:700 1rem 'IBM Plex Mono',monospace;font-style:normal;transform-origin:left;animation:gr .5s both;animation-delay:calc(var(--i)*.35s + .3s)}
@keyframes gr{from{opacity:0;transform:scaleX(0)}}
.ax{position:relative;height:26px;font:.8rem 'IBM Plex Mono',monospace;color:var(--mu)}
.ax b{position:absolute;top:4px;transform:translateX(-50%);font-weight:500}
.gw{position:relative}
.cur{position:absolute;top:-8px;bottom:-8px;width:2px;background:var(--c);box-shadow:0 0 12px var(--c);animation:cur 6s linear infinite}
@keyframes cur{from{left:0}to{left:100%}}
.term{background:#050816;border:1px solid var(--ln);border-radius:12px;padding:.8rem 1rem;font:500 .95rem/1.7 'IBM Plex Mono',monospace;color:#b7c4ff}
/* s1 orbit */
.orb{position:relative;width:min(300px,70vw);aspect-ratio:1;flex:none;margin:auto}
.orb:before{content:"";position:absolute;inset:8%;border:1px dashed var(--ln);border-radius:50%}
.orb .cpu{position:absolute;left:50%;top:50%;margin:-55px}
.orb .ch{position:absolute;left:50%;top:50%;margin:-19px -24px;animation:orb 14s linear infinite}
@keyframes orb{from{transform:rotate(var(--a)) translateX(min(115px,26vw)) rotate(calc(-1*var(--a)))}to{transform:rotate(calc(var(--a) + 360deg)) translateX(min(115px,26vw)) rotate(calc(-1*var(--a) - 360deg))}}
.split{display:flex;gap:2rem;align-items:center;flex-wrap:wrap}.split>div:first-child{flex:1 1 320px}
/* states */
.st{animation:hl 10s infinite;animation-delay:calc(var(--i)*2s)}
@keyframes hl{0%,18%{border-color:var(--c);box-shadow:0 0 26px #22d3ee88;transform:translateY(-4px)}20%,100%{}}
/* slide 5 */
.tree{line-height:1.8}
/* donut */
.don{width:min(230px,55vw);aspect-ratio:1;border-radius:50%;flex:none;background:conic-gradient(var(--c) 0 30%,var(--v) 0 55%,var(--b) 0 75%,var(--m) 0 90%,var(--g) 0 100%);display:grid;place-items:center;animation:in 1s both}
.don span{display:grid;place-items:center;width:62%;height:62%;border-radius:50%;background:var(--bg);font:700 1.1rem 'IBM Plex Mono',monospace;text-align:center}
.lg div{display:flex;gap:.6rem;align-items:center;font:500 1rem 'IBM Plex Mono',monospace;margin:.3rem 0}.lg i{width:14px;height:14px;border-radius:4px}
.bar{height:8px;border-radius:5px;background:#1a2350;overflow:hidden;margin-top:.5rem}.bar i{display:block;height:100%;background:linear-gradient(90deg,var(--v),var(--c));animation:bw 1.4s both .4s}
@keyframes bw{from{width:0}}
.pk{width:14px;height:14px;border-radius:50%;background:var(--c);box-shadow:0 0 14px var(--c);animation:mv 3s linear infinite;align-self:flex-start;margin-top:-1px}
@keyframes mv{from{margin-left:0}to{margin-left:calc(100% - 14px)}}
.qz button{font:inherit;color:var(--tx);background:var(--pn);border:1px solid var(--ln);border-radius:12px;padding:.6rem 1rem;text-align:left;cursor:pointer;flex:1 1 200px}
.qz button:hover,.qz button:focus-visible{border-color:var(--c);outline:none}
.qz .ok{border-color:var(--g);background:#0d3a2c}.qz .no{border-color:#f43f5e;opacity:.6}
#ans{display:none}#ans.sh{display:block}
nav{position:fixed;left:0;right:0;bottom:0;display:flex;align-items:center;gap:1rem;padding:.7rem clamp(18px,6vw,96px) calc(.7rem + env(safe-area-inset-bottom,0px));background:linear-gradient(transparent,var(--bg) 60%);z-index:9}
nav button{font:700 1rem 'IBM Plex Mono',monospace;color:var(--c);background:var(--pn);border:1px solid var(--ln);border-radius:10px;width:44px;height:38px;cursor:pointer}
#pr{flex:1;height:3px;background:#1a2350;border-radius:2px}#pr i{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--v),var(--c));transition:width .5s}
#no{font:500 .85rem 'IBM Plex Mono',monospace;color:var(--mu);min-width:48px;text-align:right}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01s!important;animation-iteration-count:1!important}}
</style></head><body>

<section class="s on">
 <div class="split"><div>
  <div class="tag">$ ./lecture --number=5</div>
  <h1>ДӘРІС 5<br><span class="k">ТАПСЫРМАЛАРДЫ ЖОСПАРЛАУ</span></h1>
  <p class="mu" style="max-width:34ch;margin-top:.8rem">Операциялық жүйелердегі CPU уақытын процестер мен ағындар арасында тиімді бөлу</p>
  <p class="tag" style="margin-top:1.4rem">Операциялық жүйелер | Computer Science</p></div>
  <div class="orb"><div class="cpu">CPU</div>
   <span class="ch p1" style="--a:0deg">P1</span><span class="ch p2" style="--a:90deg">P2</span><span class="ch p3" style="--a:180deg">P3</span><span class="ch p4" style="--a:270deg">P4</span></div></div>
</section>

<section class="s">
 <h2>Неге тапсырмаларды жоспарлау қажет?</h2>
 <p class="mu">CPU бір уақытта көптеген тапсырмалармен жұмыс істеуі керек.</p>
 <div class="split"><div class="lg">
  <div><span class="ch p1">P1</span>Browser</div><div><span class="ch p2">P2</span>Music</div><div><span class="ch p3">P3</span>IDE</div><div><span class="ch p4">P4</span>System</div><div><span class="ch p5">P5</span>Background task</div></div>
  <div class="ar" style="font-size:2rem">⇢</div><div class="cpu">CPU</div></div>
 <div class="q">CPU бір сәтте шектеулі мөлшерде нұсқауларды орындай алады, сондықтан операциялық жүйе процессор уақытын тиімді бөлуі керек.</div>
</section>

<section class="s">
 <h2>Тапсырмаларды жоспарлау (scheduling) дегеніміз не?</h2>
 <div class="q">Операциялық жүйенің процестер мен ағындардың орындалу кезегін анықтап, CPU уақытын олардың арасында бөлу механизмі.</div>
 <div class="fl" style="margin:auto">
  <div class="bx">PROCESS</div><div class="ar">→</div><div class="bx">READY QUEUE</div><div class="ar">→</div><div class="bx hot"><b>SCHEDULER</b></div><div class="ar">→</div><div class="bx">CPU</div><div class="ar">→</div><div class="bx">PROCESS</div></div>
</section>

<section class="s">
 <h2>Операциялық жүйедегі процесс (process)</h2>
 <p class="mu">Өмірлік цикл (life cycle)</p>
 <div class="row">
  <div class="bx st" style="--i:0"><b>NEW</b>Процесс құрылды</div><div class="ar">→</div>
  <div class="bx st" style="--i:1"><b>READY</b>CPU күтіп тұр</div><div class="ar">→</div>
  <div class="bx st" style="--i:2"><b>RUNNING</b>CPU орындап жатыр</div><div class="ar">→</div>
  <div class="bx st" style="--i:3"><b>WAITING</b>Оқиға немесе I/O күтіп тұр</div><div class="ar">→</div>
  <div class="bx st" style="--i:4"><b>TERMINATED</b>Орындалуы аяқталды</div></div>
 <div class="term">RUNNING → READY <span class="mu">// уақыт кванты біткенде</span><br>WAITING → READY <span class="mu">// I/O аяқталғанда</span></div>
</section>

<section class="s">
 <h2>Процесс пен ағынның (thread) айырмашылығы</h2>
 <div class="row">
  <div class="bx"><b>PROCESS</b>• жеке ресурстар<br>• жеке адрес кеңістігі<br>• ауырлау контекст ауыстыру</div>
  <div class="bx"><b>THREAD</b>• процесс ішінде орындалады<br>• ресурстарды ортақ пайдаланады<br>• жеңілірек орындалады</div>
  <div class="term tree" style="flex:1 1 200px">PROCESS<br>├── Thread 1<br>├── Thread 2<br>└── Thread 3</div></div>
 <div class="q">Процесс — контейнер, ағын — сол контейнер ішіндегі орындалатын жұмыс.</div>
</section>

<section class="s">
 <h2>CPU уақытын бөлу</h2>
 <div class="split"><div class="don"><span>CPU TIME<br>100%</span></div>
  <div class="lg"><div><i class="p1"></i>P1 = 30%</div><div><i class="p2"></i>P2 = 25%</div><div><i class="p3"></i>P3 = 20%</div><div><i class="p4"></i>P4 = 15%</div><div><i class="p5"></i>System = 10%</div></div></div>
 <div class="q">Бұл нақты тұрақты үлес емес, жоспарлаушының алгоритмі мен жүйе жағдайына байланысты өзгеріп отырады.</div>
</section>

<section class="s">
 <h2>Жоспарлаушы қалай жұмыс істейді?</h2>
 <div class="split"><div class="term">1. Процестер READY QUEUE-ға түседі.<br>2. Scheduler келесісін таңдайды.<br>3. CPU таңдалған процеске беріледі.<br>4. Процесс орындалады.<br>5. Квант біткенде немесе процесс күтуге кетсе, Scheduler қайта таңдайды.</div>
  <div class="fl"><div class="bx">READY QUEUE</div><div class="ar">→</div><div class="bx hot"><b>SCHEDULER</b></div><div class="ar">→</div><div class="bx">CPU</div><div class="ar">→</div><div class="bx">CONTEXT SWITCH</div><div class="ar">→</div><div class="bx hot"><b>SCHEDULER</b></div></div></div>
</section>

<section class="s">
 <h2>CPU scheduling алгоритмдері</h2>
 <div class="row">
  <div class="bx"><b>FCFS</b><small>First Come, First Served: келу ретімен</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p1">P1</span><span class="ch p2">P2</span><span class="ch p3">P3</span></div></div>
  <div class="bx"><b>SJF</b><small>Shortest Job First: ең қысқа жұмыс бірінші</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p3" style="min-width:30px">P3</span><span class="ch p2" style="min-width:50px">P2</span><span class="ch p1" style="min-width:80px">P1</span></div></div>
  <div class="bx"><b>Round Robin</b><small>Кезекпен орындау</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p1">P1</span><span class="ch p2">P2</span><span class="ch p3">P3</span><span class="ch" style="background:none;color:var(--c)">↻</span></div></div>
  <div class="bx"><b>Priority</b><small>Басымдық бойынша жоспарлау</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p4">P4·1</span><span class="ch p1">P1·2</span><span class="ch p3">P3·3</span></div></div></div>
</section>

<section class="s">
 <h2>Round Robin — кезекпен орындау</h2>
 <p class="mu mo">Quantum = 2 ms</p>
 <div class="gw"><div class="g"><i class="p1" style="--i:0;flex:1">P1</i><i class="p2" style="--i:1;flex:1">P2</i><i class="p3" style="--i:2;flex:1">P3</i><i class="p4" style="--i:3;flex:1">P4</i><i class="p1" style="--i:4;flex:1">P1</i><i class="p2" style="--i:5;flex:1">P2</i></div><div class="cur"></div></div>
 <div class="q">Әр процесс CPU уақытын кезекпен алады.</div>
 <div class="row"><div class="bx"><b>✓</b>әділ бөлу</div><div class="bx"><b>✓</b>интерактивті жүйелерге ыңғайлы</div></div>
</section>

<section class="s">
 <h2>Context Switch</h2>
 <div class="q">CPU бір процестен екіншісіне ауысқан кезде ағымдағы процестің күйін сақтап, келесі процестің күйін қалпына келтіру процесі.</div>
 <div class="row" style="align-items:center"><span class="ch p1">P1</span><span class="ar">→</span><div class="bx hot"><b>SAVE STATE</b></div><span class="ar">→</span><div class="bx hot"><b>LOAD P2</b></div><span class="ar">→</span><span class="ch p2">P2</span></div>
 <div class="pk"></div>
 <div class="bx"><b>Overhead</b><small>Ауысу кезінде CPU пайдалы жұмыс істемейді</small></div>
 <div class="q" style="border-color:var(--m)">Тым көп ауысу → артық шығын → өнімділіктің төмендеуі.</div>
</section>

<section class="s">
 <h2>Жоспарлау критерийлері</h2>
 <div class="row">
  <div class="bx"><b>CPU Utilization</b><small>CPU қаншалықты тиімді қолданылды?</small><div class="bar"><i style="width:92%"></i></div></div>
  <div class="bx"><b>Throughput</b><small>Бір уақытта қанша процесс аяқталды?</small><div class="bar"><i style="width:70%"></i></div></div>
  <div class="bx"><b>Turnaround Time</b><small>Процестің толық орындалу уақыты</small><div class="bar"><i style="width:55%"></i></div></div>
  <div class="bx"><b>Waiting Time</b><small>Процестің кезекте күткен уақыты</small><div class="bar"><i style="width:35%"></i></div></div>
  <div class="bx"><b>Response Time</b><small>Алғашқы реакцияға дейінгі уақыт</small><div class="bar"><i style="width:25%"></i></div></div></div>
</section>

<section class="s">
 <h2>Практикалық мысал</h2>
 <p class="mu mo">P1 = 5 ms · P2 = 3 ms · P3 = 2 ms · Round Robin, Quantum = 2 ms</p>
 <div class="gw"><div class="g"><i class="p1" style="--i:0;flex:2">P1</i><i class="p2" style="--i:1;flex:2">P2</i><i class="p3" style="--i:2;flex:2">P3</i><i class="p1" style="--i:3;flex:2">P1</i><i class="p2" style="--i:4;flex:1">P2</i><i class="p1" style="--i:5;flex:1">P1</i></div><div class="cur"></div></div>
 <div class="ax"><b style="left:0">0</b><b style="left:20%">2</b><b style="left:40%">4</b><b style="left:60%">6</b><b style="left:80%">8</b><b style="left:90%">9</b><b style="left:100%">10</b></div>
 <div class="term">P1: 5 → 3 → 1 → 0<br>P2: 3 → 1 → 0<br>P3: 2 → 0</div>
 <p class="mu">Ешбір процесс кванттан ұзақ CPU ұстамайды, сондықтан олар кезекпен орындалады.</p>
</section>

<section class="s">
 <h2>Қазіргі операциялық жүйелер</h2>
 <div class="row"><span class="ch p1">Windows</span><span class="ch p2">Linux</span><span class="ch p3">Android</span><span class="ch p4">macOS</span></div>
 <div class="row">
  <div class="bx hot"><b>CORE 1</b><span class="ch p1">P1</span></div><div class="bx hot"><b>CORE 2</b><span class="ch p3">P3</span></div><div class="bx hot"><b>CORE 3</b><span class="ch p2">P2</span></div><div class="bx hot"><b>CORE 4</b><span class="ch p4">P4</span></div></div>
 <div class="q">Қазіргі жоспарлаушылар тек кезекпен орындаумен шектелмейді. Олар басымдықтарды, интерактивтілікті, көпядролы CPU-ды және жүйелік жүктемені ескереді.</div>
</section>

<section class="s">
 <h1 style="font-size:clamp(1.6rem,4.6vw,3.6rem)"><span class="k">CPU — ШЕКТЕУЛІ РЕСУРС.</span><br>SCHEDULER — ОНЫ БАСҚАРАТЫН МЕХАНИЗМ.</h1>
 <div class="term" style="font-family:'IBM Plex Sans',sans-serif">• Процестер мен ағындар CPU үшін кезектеседі.<br>• Scheduler келесі тапсырманы таңдайды.<br>• Алгоритм жүйенің өнімділігіне әсер етеді.<br>• Context Switch процестер арасында ауысуды қамтамасыз етеді.<br>• Дұрыс жоспарлау CPU уақытын тиімді пайдаланады.</div>
 <p class="mo k" style="font-size:.9rem">MULTIPLE PROCESSES → SCHEDULER → CPU → FAST + FAIR + EFFICIENT SYSTEM</p>
 <p class="v">Егер барлық процестер бір уақытта CPU талап етсе, қай процесс бірінші орындалуы керек?</p>
 <div class="qz"><p style="margin-bottom:.5rem">Қай алгоритм интерактивті жүйелер үшін тиімді болуы мүмкін?</p>
  <div class="row"><button data-k="0">A) FCFS</button><button data-k="1">B) Round Robin</button><button data-k="0">C) Random Scheduling</button><button data-k="0">D) Барлығын бір уақытта орындау</button></div>
  <div id="ans" class="q" style="margin-top:.6rem"><b class="k">B) Round Robin</b> — CPU уақыты процестер арасында кезекпен бөлінеді және жауап беру уақыты қысқарады.</div></div>
</section>

<nav><button id="pv" aria-label="Алдыңғы">←</button><div id="pr"><i></i></div><span id="no"></span><button id="nx" aria-label="Келесі">→</button></nav>
<script>
var S=[].slice.call(document.querySelectorAll('.s')),n=0;
function go(i){n=Math.max(0,Math.min(S.length-1,i));S.forEach(function(s,j){s.classList.toggle('on',j==n)});S[n].scrollTop=0;
document.querySelector('#pr i').style.width=((n+1)/S.length*100)+'%';document.getElementById('no').textContent=(n+1)+'/'+S.length;
try{history.replaceState(null,'','#'+(n+1))}catch(e){}}
document.getElementById('pv').onclick=function(){go(n-1)};document.getElementById('nx').onclick=function(){go(n+1)};
document.addEventListener('keydown',function(e){if(e.key=='ArrowRight'||e.key==' '||e.key=='PageDown')go(n+1);if(e.key=='ArrowLeft'||e.key=='PageUp')go(n-1)});
var x0=null;document.addEventListener('touchstart',function(e){x0=e.touches[0].clientX},{passive:true});
document.addEventListener('touchend',function(e){if(x0===null)return;var d=e.changedTouches[0].clientX-x0;if(Math.abs(d)>60)go(n+(d<0?1:-1));x0=null});
[].forEach.call(document.querySelectorAll('.qz button'),function(b){b.onclick=function(){
[].forEach.call(document.querySelectorAll('.qz button'),function(o){o.classList.add(o.dataset.k=='1'?'ok':'no')});document.getElementById('ans').classList.add('sh')}});
var h=parseInt(location.hash.slice(1));go(h?h-1:0);
</script></body></html>
<!DOCTYPE html>
<html lang="kk"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Дәріс 5: Тапсырмаларды жоспарлау</title>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@400;600;700&family=IBM+Plex+Mono:wght@500;700&display=swap" rel="stylesheet">
<style>
:root{--bg:#060914;--pn:#0d1330;--ln:#26305f;--tx:#e8ecff;--mu:#93a0d6;--c:#22d3ee;--v:#8b5cf6;--b:#3b82f6;--m:#e879f9;--g:#34d399;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:dark}
*{box-sizing:inherit;margin:0}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
html,body{height:100%;background:var(--bg);color:var(--tx);font:400 clamp(15px,1.7vw,22px)/1.45 'IBM Plex Sans','Segoe UI',system-ui,sans-serif;overflow:hidden}
body{background:radial-gradient(60% 50% at 80% 0,#1b1450 0,transparent 70%),radial-gradient(50% 40% at 0 100%,#062a4a 0,transparent 70%),var(--bg)}
body:before{content:"";position:fixed;inset:0;background:linear-gradient(var(--ln) 1px,transparent 1px) 0 0/48px 48px,linear-gradient(90deg,var(--ln) 1px,transparent 1px) 0 0/48px 48px;opacity:.14;pointer-events:none}
.s{position:absolute;inset:0;display:none;flex-direction:column;justify-content:center;gap:1.1rem;padding:clamp(18px,4vw,64px) clamp(18px,6vw,96px) 72px;overflow:auto;animation:in .6s both}
.s.on{display:flex}
@keyframes in{from{opacity:0;transform:scale(.98)}}
h1{font-size:clamp(2rem,6.4vw,5rem);line-height:1.02;font-weight:700;letter-spacing:-.02em}
h2{font-size:clamp(1.5rem,3.8vw,3rem);line-height:1.1;font-weight:700;letter-spacing:-.01em}
.mo{font-family:'IBM Plex Mono',ui-monospace,monospace}
.k{color:var(--c)}.v{color:var(--m)}.mu{color:var(--mu)}
.tag{font:500 .8rem 'IBM Plex Mono',monospace;color:var(--c)}
.q{border-left:3px solid var(--v);padding:.4rem 1rem;font-size:1.05em;background:linear-gradient(90deg,#8b5cf622,transparent)}
.row{display:flex;gap:.8rem;flex-wrap:wrap;align-items:stretch}
.bx{flex:1 1 150px;background:var(--pn);border:1px solid var(--ln);border-radius:14px;padding:.8rem 1rem}
.bx b{display:block;color:var(--c);font-family:'IBM Plex Mono',monospace}
.bx small{color:var(--mu);font-size:.85em}
.hot{border-color:var(--v);box-shadow:0 0 28px #8b5cf655;animation:pl 2s infinite}
@keyframes pl{50%{box-shadow:0 0 44px #8b5cf6aa}}
.ar{align-self:center;color:var(--c);font-family:'IBM Plex Mono',monospace}
.fl{display:flex;flex-direction:column;gap:.2rem;align-items:center;max-width:340px}
.fl .bx{width:100%;text-align:center;padding:.5rem}
.fl .ar{transform:rotate(90deg);height:1.2rem;line-height:1}
.p1{background:var(--c)}.p2{background:var(--v)}.p3{background:var(--b)}.p4{background:var(--m)}.p5{background:var(--g)}
.ch{display:inline-grid;place-items:center;min-width:48px;height:38px;padding:0 .6rem;border-radius:9px;color:#04101f;font:700 .9rem 'IBM Plex Mono',monospace}
.cpu{display:grid;place-items:center;width:110px;height:110px;border-radius:22px;background:#0a1030;border:2px solid var(--c);box-shadow:0 0 40px #22d3ee66,inset 0 0 24px #22d3ee33;font:700 1.6rem 'IBM Plex Mono',monospace;color:var(--c);animation:pl 2.4s infinite}
.g{display:flex;gap:3px;height:60px}
.g i{display:grid;place-items:center;border-radius:8px;color:#04101f;font:700 1rem 'IBM Plex Mono',monospace;font-style:normal;transform-origin:left;animation:gr .5s both;animation-delay:calc(var(--i)*.35s + .3s)}
@keyframes gr{from{opacity:0;transform:scaleX(0)}}
.ax{position:relative;height:26px;font:.8rem 'IBM Plex Mono',monospace;color:var(--mu)}
.ax b{position:absolute;top:4px;transform:translateX(-50%);font-weight:500}
.gw{position:relative}
.cur{position:absolute;top:-8px;bottom:-8px;width:2px;background:var(--c);box-shadow:0 0 12px var(--c);animation:cur 6s linear infinite}
@keyframes cur{from{left:0}to{left:100%}}
.term{background:#050816;border:1px solid var(--ln);border-radius:12px;padding:.8rem 1rem;font:500 .95rem/1.7 'IBM Plex Mono',monospace;color:#b7c4ff}
/* s1 orbit */
.orb{position:relative;width:min(300px,70vw);aspect-ratio:1;flex:none;margin:auto}
.orb:before{content:"";position:absolute;inset:8%;border:1px dashed var(--ln);border-radius:50%}
.orb .cpu{position:absolute;left:50%;top:50%;margin:-55px}
.orb .ch{position:absolute;left:50%;top:50%;margin:-19px -24px;animation:orb 14s linear infinite}
@keyframes orb{from{transform:rotate(var(--a)) translateX(min(115px,26vw)) rotate(calc(-1*var(--a)))}to{transform:rotate(calc(var(--a) + 360deg)) translateX(min(115px,26vw)) rotate(calc(-1*var(--a) - 360deg))}}
.split{display:flex;gap:2rem;align-items:center;flex-wrap:wrap}.split>div:first-child{flex:1 1 320px}
/* states */
.st{animation:hl 10s infinite;animation-delay:calc(var(--i)*2s)}
@keyframes hl{0%,18%{border-color:var(--c);box-shadow:0 0 26px #22d3ee88;transform:translateY(-4px)}20%,100%{}}
/* slide 5 */
.tree{line-height:1.8}
/* donut */
.don{width:min(230px,55vw);aspect-ratio:1;border-radius:50%;flex:none;background:conic-gradient(var(--c) 0 30%,var(--v) 0 55%,var(--b) 0 75%,var(--m) 0 90%,var(--g) 0 100%);display:grid;place-items:center;animation:in 1s both}
.don span{display:grid;place-items:center;width:62%;height:62%;border-radius:50%;background:var(--bg);font:700 1.1rem 'IBM Plex Mono',monospace;text-align:center}
.lg div{display:flex;gap:.6rem;align-items:center;font:500 1rem 'IBM Plex Mono',monospace;margin:.3rem 0}.lg i{width:14px;height:14px;border-radius:4px}
.bar{height:8px;border-radius:5px;background:#1a2350;overflow:hidden;margin-top:.5rem}.bar i{display:block;height:100%;background:linear-gradient(90deg,var(--v),var(--c));animation:bw 1.4s both .4s}
@keyframes bw{from{width:0}}
.pk{width:14px;height:14px;border-radius:50%;background:var(--c);box-shadow:0 0 14px var(--c);animation:mv 3s linear infinite;align-self:flex-start;margin-top:-1px}
@keyframes mv{from{margin-left:0}to{margin-left:calc(100% - 14px)}}
.qz button{font:inherit;color:var(--tx);background:var(--pn);border:1px solid var(--ln);border-radius:12px;padding:.6rem 1rem;text-align:left;cursor:pointer;flex:1 1 200px}
.qz button:hover,.qz button:focus-visible{border-color:var(--c);outline:none}
.qz .ok{border-color:var(--g);background:#0d3a2c}.qz .no{border-color:#f43f5e;opacity:.6}
#ans{display:none}#ans.sh{display:block}
nav{position:fixed;left:0;right:0;bottom:0;display:flex;align-items:center;gap:1rem;padding:.7rem clamp(18px,6vw,96px) calc(.7rem + env(safe-area-inset-bottom,0px));background:linear-gradient(transparent,var(--bg) 60%);z-index:9}
nav button{font:700 1rem 'IBM Plex Mono',monospace;color:var(--c);background:var(--pn);border:1px solid var(--ln);border-radius:10px;width:44px;height:38px;cursor:pointer}
#pr{flex:1;height:3px;background:#1a2350;border-radius:2px}#pr i{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--v),var(--c));transition:width .5s}
#no{font:500 .85rem 'IBM Plex Mono',monospace;color:var(--mu);min-width:48px;text-align:right}
@media(prefers-reduced-motion:reduce){*{animation-duration:.01s!important;animation-iteration-count:1!important}}
</style></head><body>

<section class="s on">
 <div class="split"><div>
  <div class="tag">$ ./lecture --number=5</div>
  <h1>ДӘРІС 5<br><span class="k">ТАПСЫРМАЛАРДЫ ЖОСПАРЛАУ</span></h1>
  <p class="mu" style="max-width:34ch;margin-top:.8rem">Операциялық жүйелердегі CPU уақытын процестер мен ағындар арасында тиімді бөлу</p>
  <p class="tag" style="margin-top:1.4rem">Операциялық жүйелер | Computer Science</p></div>
  <div class="orb"><div class="cpu">CPU</div>
   <span class="ch p1" style="--a:0deg">P1</span><span class="ch p2" style="--a:90deg">P2</span><span class="ch p3" style="--a:180deg">P3</span><span class="ch p4" style="--a:270deg">P4</span></div></div>
</section>

<section class="s">
 <h2>Неге тапсырмаларды жоспарлау қажет?</h2>
 <p class="mu">CPU бір уақытта көптеген тапсырмалармен жұмыс істеуі керек.</p>
 <div class="split"><div class="lg">
  <div><span class="ch p1">P1</span>Browser</div><div><span class="ch p2">P2</span>Music</div><div><span class="ch p3">P3</span>IDE</div><div><span class="ch p4">P4</span>System</div><div><span class="ch p5">P5</span>Background task</div></div>
  <div class="ar" style="font-size:2rem">⇢</div><div class="cpu">CPU</div></div>
 <div class="q">CPU бір сәтте шектеулі мөлшерде нұсқауларды орындай алады, сондықтан операциялық жүйе процессор уақытын тиімді бөлуі керек.</div>
</section>

<section class="s">
 <h2>Тапсырмаларды жоспарлау (scheduling) дегеніміз не?</h2>
 <div class="q">Операциялық жүйенің процестер мен ағындардың орындалу кезегін анықтап, CPU уақытын олардың арасында бөлу механизмі.</div>
 <div class="fl" style="margin:auto">
  <div class="bx">PROCESS</div><div class="ar">→</div><div class="bx">READY QUEUE</div><div class="ar">→</div><div class="bx hot"><b>SCHEDULER</b></div><div class="ar">→</div><div class="bx">CPU</div><div class="ar">→</div><div class="bx">PROCESS</div></div>
</section>

<section class="s">
 <h2>Операциялық жүйедегі процесс (process)</h2>
 <p class="mu">Өмірлік цикл (life cycle)</p>
 <div class="row">
  <div class="bx st" style="--i:0"><b>NEW</b>Процесс құрылды</div><div class="ar">→</div>
  <div class="bx st" style="--i:1"><b>READY</b>CPU күтіп тұр</div><div class="ar">→</div>
  <div class="bx st" style="--i:2"><b>RUNNING</b>CPU орындап жатыр</div><div class="ar">→</div>
  <div class="bx st" style="--i:3"><b>WAITING</b>Оқиға немесе I/O күтіп тұр</div><div class="ar">→</div>
  <div class="bx st" style="--i:4"><b>TERMINATED</b>Орындалуы аяқталды</div></div>
 <div class="term">RUNNING → READY <span class="mu">// уақыт кванты біткенде</span><br>WAITING → READY <span class="mu">// I/O аяқталғанда</span></div>
</section>

<section class="s">
 <h2>Процесс пен ағынның (thread) айырмашылығы</h2>
 <div class="row">
  <div class="bx"><b>PROCESS</b>• жеке ресурстар<br>• жеке адрес кеңістігі<br>• ауырлау контекст ауыстыру</div>
  <div class="bx"><b>THREAD</b>• процесс ішінде орындалады<br>• ресурстарды ортақ пайдаланады<br>• жеңілірек орындалады</div>
  <div class="term tree" style="flex:1 1 200px">PROCESS<br>├── Thread 1<br>├── Thread 2<br>└── Thread 3</div></div>
 <div class="q">Процесс — контейнер, ағын — сол контейнер ішіндегі орындалатын жұмыс.</div>
</section>

<section class="s">
 <h2>CPU уақытын бөлу</h2>
 <div class="split"><div class="don"><span>CPU TIME<br>100%</span></div>
  <div class="lg"><div><i class="p1"></i>P1 = 30%</div><div><i class="p2"></i>P2 = 25%</div><div><i class="p3"></i>P3 = 20%</div><div><i class="p4"></i>P4 = 15%</div><div><i class="p5"></i>System = 10%</div></div></div>
 <div class="q">Бұл нақты тұрақты үлес емес, жоспарлаушының алгоритмі мен жүйе жағдайына байланысты өзгеріп отырады.</div>
</section>

<section class="s">
 <h2>Жоспарлаушы қалай жұмыс істейді?</h2>
 <div class="split"><div class="term">1. Процестер READY QUEUE-ға түседі.<br>2. Scheduler келесісін таңдайды.<br>3. CPU таңдалған процеске беріледі.<br>4. Процесс орындалады.<br>5. Квант біткенде немесе процесс күтуге кетсе, Scheduler қайта таңдайды.</div>
  <div class="fl"><div class="bx">READY QUEUE</div><div class="ar">→</div><div class="bx hot"><b>SCHEDULER</b></div><div class="ar">→</div><div class="bx">CPU</div><div class="ar">→</div><div class="bx">CONTEXT SWITCH</div><div class="ar">→</div><div class="bx hot"><b>SCHEDULER</b></div></div></div>
</section>

<section class="s">
 <h2>CPU scheduling алгоритмдері</h2>
 <div class="row">
  <div class="bx"><b>FCFS</b><small>First Come, First Served: келу ретімен</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p1">P1</span><span class="ch p2">P2</span><span class="ch p3">P3</span></div></div>
  <div class="bx"><b>SJF</b><small>Shortest Job First: ең қысқа жұмыс бірінші</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p3" style="min-width:30px">P3</span><span class="ch p2" style="min-width:50px">P2</span><span class="ch p1" style="min-width:80px">P1</span></div></div>
  <div class="bx"><b>Round Robin</b><small>Кезекпен орындау</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p1">P1</span><span class="ch p2">P2</span><span class="ch p3">P3</span><span class="ch" style="background:none;color:var(--c)">↻</span></div></div>
  <div class="bx"><b>Priority</b><small>Басымдық бойынша жоспарлау</small><div class="row" style="margin-top:.6rem;gap:4px"><span class="ch p4">P4·1</span><span class="ch p1">P1·2</span><span class="ch p3">P3·3</span></div></div></div>
</section>

<section class="s">
 <h2>Round Robin — кезекпен орындау</h2>
 <p class="mu mo">Quantum = 2 ms</p>
 <div class="gw"><div class="g"><i class="p1" style="--i:0;flex:1">P1</i><i class="p2" style="--i:1;flex:1">P2</i><i class="p3" style="--i:2;flex:1">P3</i><i class="p4" style="--i:3;flex:1">P4</i><i class="p1" style="--i:4;flex:1">P1</i><i class="p2" style="--i:5;flex:1">P2</i></div><div class="cur"></div></div>
 <div class="q">Әр процесс CPU уақытын кезекпен алады.</div>
 <div class="row"><div class="bx"><b>✓</b>әділ бөлу</div><div class="bx"><b>✓</b>интерактивті жүйелерге ыңғайлы</div></div>
</section>

<section class="s">
 <h2>Context Switch</h2>
 <div class="q">CPU бір процестен екіншісіне ауысқан кезде ағымдағы процестің күйін сақтап, келесі процестің күйін қалпына келтіру процесі.</div>
 <div class="row" style="align-items:center"><span class="ch p1">P1</span><span class="ar">→</span><div class="bx hot"><b>SAVE STATE</b></div><span class="ar">→</span><div class="bx hot"><b>LOAD P2</b></div><span class="ar">→</span><span class="ch p2">P2</span></div>
 <div class="pk"></div>
 <div class="bx"><b>Overhead</b><small>Ауысу кезінде CPU пайдалы жұмыс істемейді</small></div>
 <div class="q" style="border-color:var(--m)">Тым көп ауысу → артық шығын → өнімділіктің төмендеуі.</div>
</section>

<section class="s">
 <h2>Жоспарлау критерийлері</h2>
 <div class="row">
  <div class="bx"><b>CPU Utilization</b><small>CPU қаншалықты тиімді қолданылды?</small><div class="bar"><i style="width:92%"></i></div></div>
  <div class="bx"><b>Throughput</b><small>Бір уақытта қанша процесс аяқталды?</small><div class="bar"><i style="width:70%"></i></div></div>
  <div class="bx"><b>Turnaround Time</b><small>Процестің толық орындалу уақыты</small><div class="bar"><i style="width:55%"></i></div></div>
  <div class="bx"><b>Waiting Time</b><small>Процестің кезекте күткен уақыты</small><div class="bar"><i style="width:35%"></i></div></div>
  <div class="bx"><b>Response Time</b><small>Алғашқы реакцияға дейінгі уақыт</small><div class="bar"><i style="width:25%"></i></div></div></div>
</section>

<section class="s">
 <h2>Практикалық мысал</h2>
 <p class="mu mo">P1 = 5 ms · P2 = 3 ms · P3 = 2 ms · Round Robin, Quantum = 2 ms</p>
 <div class="gw"><div class="g"><i class="p1" style="--i:0;flex:2">P1</i><i class="p2" style="--i:1;flex:2">P2</i><i class="p3" style="--i:2;flex:2">P3</i><i class="p1" style="--i:3;flex:2">P1</i><i class="p2" style="--i:4;flex:1">P2</i><i class="p1" style="--i:5;flex:1">P1</i></div><div class="cur"></div></div>
 <div class="ax"><b style="left:0">0</b><b style="left:20%">2</b><b style="left:40%">4</b><b style="left:60%">6</b><b style="left:80%">8</b><b style="left:90%">9</b><b style="left:100%">10</b></div>
 <div class="term">P1: 5 → 3 → 1 → 0<br>P2: 3 → 1 → 0<br>P3: 2 → 0</div>
 <p class="mu">Ешбір процесс кванттан ұзақ CPU ұстамайды, сондықтан олар кезекпен орындалады.</p>
</section>

<section class="s">
 <h2>Қазіргі операциялық жүйелер</h2>
 <div class="row"><span class="ch p1">Windows</span><span class="ch p2">Linux</span><span class="ch p3">Android</span><span class="ch p4">macOS</span></div>
 <div class="row">
  <div class="bx hot"><b>CORE 1</b><span class="ch p1">P1</span></div><div class="bx hot"><b>CORE 2</b><span class="ch p3">P3</span></div><div class="bx hot"><b>CORE 3</b><span class="ch p2">P2</span></div><div class="bx hot"><b>CORE 4</b><span class="ch p4">P4</span></div></div>
 <div class="q">Қазіргі жоспарлаушылар тек кезекпен орындаумен шектелмейді. Олар басымдықтарды, интерактивтілікті, көпядролы CPU-ды және жүйелік жүктемені ескереді.</div>
</section>

<section class="s">
 <h1 style="font-size:clamp(1.6rem,4.6vw,3.6rem)"><span class="k">CPU — ШЕКТЕУЛІ РЕСУРС.</span><br>SCHEDULER — ОНЫ БАСҚАРАТЫН МЕХАНИЗМ.</h1>
 <div class="term" style="font-family:'IBM Plex Sans',sans-serif">• Процестер мен ағындар CPU үшін кезектеседі.<br>• Scheduler келесі тапсырманы таңдайды.<br>• Алгоритм жүйенің өнімділігіне әсер етеді.<br>• Context Switch процестер арасында ауысуды қамтамасыз етеді.<br>• Дұрыс жоспарлау CPU уақытын тиімді пайдаланады.</div>
 <p class="mo k" style="font-size:.9rem">MULTIPLE PROCESSES → SCHEDULER → CPU → FAST + FAIR + EFFICIENT SYSTEM</p>
 <p class="v">Егер барлық процестер бір уақытта CPU талап етсе, қай процесс бірінші орындалуы керек?</p>
 <div class="qz"><p style="margin-bottom:.5rem">Қай алгоритм интерактивті жүйелер үшін тиімді болуы мүмкін?</p>
  <div class="row"><button data-k="0">A) FCFS</button><button data-k="1">B) Round Robin</button><button data-k="0">C) Random Scheduling</button><button data-k="0">D) Барлығын бір уақытта орындау</button></div>
  <div id="ans" class="q" style="margin-top:.6rem"><b class="k">B) Round Robin</b> — CPU уақыты процестер арасында кезекпен бөлінеді және жауап беру уақыты қысқарады.</div></div>
</section>

<nav><button id="pv" aria-label="Алдыңғы">←</button><div id="pr"><i></i></div><span id="no"></span><button id="nx" aria-label="Келесі">→</button></nav>
<script>
var S=[].slice.call(document.querySelectorAll('.s')),n=0;
function go(i){n=Math.max(0,Math.min(S.length-1,i));S.forEach(function(s,j){s.classList.toggle('on',j==n)});S[n].scrollTop=0;
document.querySelector('#pr i').style.width=((n+1)/S.length*100)+'%';document.getElementById('no').textContent=(n+1)+'/'+S.length;
try{history.replaceState(null,'','#'+(n+1))}catch(e){}}
document.getElementById('pv').onclick=function(){go(n-1)};document.getElementById('nx').onclick=function(){go(n+1)};
document.addEventListener('keydown',function(e){if(e.key=='ArrowRight'||e.key==' '||e.key=='PageDown')go(n+1);if(e.key=='ArrowLeft'||e.key=='PageUp')go(n-1)});
var x0=null;document.addEventListener('touchstart',function(e){x0=e.touches[0].clientX},{passive:true});
document.addEventListener('touchend',function(e){if(x0===null)return;var d=e.changedTouches[0].clientX-x0;if(Math.abs(d)>60)go(n+(d<0?1:-1));x0=null});
[].forEach.call(document.querySelectorAll('.qz button'),function(b){b.onclick=function(){
[].forEach.call(document.querySelectorAll('.qz button'),function(o){o.classList.add(o.dataset.k=='1'?'ok':'no')});document.getElementById('ans').classList.add('sh')}});
var h=parseInt(location.hash.slice(1));go(h?h-1:0);
</script></body></html>
