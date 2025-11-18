<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Kuis Islami + Mini Game (GitHub Pages)</title>
<link rel="icon" href="data:;base64,iVBORw0KGgo=">

<style>
  :root{
    --bg1:#071b12; --bg2:#083522; --card:#0b3d2e; --accent:#00ffae;
    --muted: rgba(255,255,255,0.75); --danger:#ff6666; --gold:#ffd166;
  }
  @media (prefers-color-scheme: light){
    :root{
      --bg1:#f3faf5; --bg2:#eaf7ec; --card:#ffffff; --accent:#0a7a50;
      --muted:#2b3a33; --danger:#c0392b; --gold:#d67a00;
    }
  }

  *{box-sizing:border-box}
  body{
    margin:0;
    min-height:100vh;
    font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    background: linear-gradient(135deg,var(--bg1),var(--bg2));
    color:var(--muted);
    display:flex;
    align-items:center;
    justify-content:center;
    padding:28px;
  }

  .wrap{
    width:100%;
    max-width:1100px;
    display:grid;
    grid-template-columns: 1fr 420px;
    gap:22px;
    align-items:start;
  }

  /* left: quiz/game area */
  .panel{
    background:linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
    border-radius:14px;
    padding:20px;
    box-shadow:0 10px 30px rgba(0,0,0,0.25);
    border:1px solid rgba(255,255,255,0.04);
  }

  header.site{
    display:flex;
    gap:16px;
    align-items:center;
    justify-content:space-between;
    margin-bottom:12px;
  }
  header.site h1{ margin:0; font-size:20px; color:var(--accent) }
  .controls{display:flex; gap:8px; align-items:center;}

  .btn{
    padding:8px 12px;
    border-radius:10px;
    border:0; cursor:pointer;
    background:linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
    color:var(--muted);
    box-shadow:0 3px 8px rgba(0,0,0,0.15);
    font-weight:600;
    transition:transform .12s ease, box-shadow .12s;
  }
  .btn:hover{ transform:translateY(-3px) }
  .btn.primary{
    background:linear-gradient(180deg,var(--accent), rgba(0,0,0,0.08));
    color:#01140f;
  }

  /* Quiz area */
  .quiz-area { margin-top:12px; }
  .card{
    background:var(--card);
    padding:18px;
    border-radius:12px;
    color:var(--muted);
    box-shadow:inset 0 1px 0 rgba(255,255,255,0.02);
  }
  .question{
    font-size:18px;
    margin-bottom:12px;
    font-weight:600;
  }
  .answers{ display:grid; gap:10px; }
  .answer{
    background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.04));
    border-radius:10px;
    padding:12px;
    cursor:pointer;
    transition:transform .12s ease, box-shadow .12s, background .2s;
    border:1px solid rgba(0,0,0,0.06);
    font-weight:600;
  }
  .answer:hover{ transform:translateY(-4px) }
  .answer.correct{ background:linear-gradient(90deg, rgba(0,255,174,0.12), rgba(0,255,174,0.04)); box-shadow:0 8px 20px rgba(0,255,174,0.06); }
  .answer.wrong{ background:linear-gradient(90deg, rgba(255,102,102,0.08), rgba(255,102,102,0.02)); box-shadow:0 8px 20px rgba(255,102,102,0.04); }

  .status-row{ display:flex; align-items:center; gap:12px; margin-top:12px; }
  .progress{
    flex:1;
    height:12px;
    background:rgba(255,255,255,0.05);
    border-radius:8px;
    overflow:hidden;
  }
  .progress > i{
    display:block; height:100%; width:0%;
    background:linear-gradient(90deg, var(--accent), var(--gold));
    transition:width .45s ease;
  }
  .timer-box{
    min-width:110px; text-align:center; font-weight:700;
  }

  .result-screen{
    text-align:center;
    padding:30px;
  }
  .score-big{
    font-size:36px;
    color:var(--accent);
    font-weight:800;
    margin:8px 0;
  }

  /* right column */
  .sidebar{
    display:flex;
    flex-direction:column;
    gap:14px;
  }
  .panel.small{ padding:14px; border-radius:12px; }

  .leaderboard h3{ margin:0 0 8px 0; color:var(--accent) }
  .list{ display:flex; flex-direction:column; gap:8px; }
  .list .item{
    padding:8px; border-radius:8px; background:linear-gradient(180deg, rgba(0,0,0,0.02), rgba(255,255,255,0.01));
    display:flex; justify-content:space-between; font-weight:700;
  }

  /* Reaction game */
  .reaction-area{ display:grid; gap:12px; align-items:center; justify-items:center; padding:18px; }
  .target{
    width:220px; height:220px; border-radius:18px; display:flex; align-items:center; justify-content:center;
    background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(0,0,0,0.04));
    cursor:pointer; user-select:none; font-weight:900; font-size:18px;
    transition:transform .08s ease;
  }
  .target.hidden{ opacity:0.15; transform:scale(.98); }
  .small-muted{ font-size:12px; color:rgba(255,255,255,0.6) }

  /* confetti canvas */
  #confettiCanvas{ position:fixed; pointer-events:none; left:0; top:0; width:100%; height:100%; z-index:9999; }

  /* responsive */
  @media (max-width:1024px){
    .wrap{ grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<canvas id="confettiCanvas"></canvas>

<div class="wrap">
  <div>
    <div class="panel">
      <header class="site">
        <h1>Kuis Islami & Mini Game</h1>
        <div class="controls">
          <button class="btn" id="themeToggle" title="Toggle theme">🌗</button>
          <button class="btn" id="resetAll" title="Reset semua leaderboard">Reset Data</button>
          <button class="btn primary" id="startQuizBtn">Mulai Kuis</button>
        </div>
      </header>

      <!-- QUIZ AREA -->
      <div id="quizArea" class="quiz-area">
        <div id="quizCard" class="card">
          <div class="question" id="questionText">Tekan "Mulai Kuis" untuk memulai.</div>

          <div class="answers" id="answersBox" style="display:none;">
            <div class="answer" data-index="0" id="a0"></div>
            <div class="answer" data-index="1" id="a1"></div>
            <div class="answer" data-index="2" id="a2"></div>
            <div class="answer" data-index="3" id="a3"></div>
          </div>

          <div class="status-row" style="display:none;" id="statusRow">
            <div class="progress" title="Progress">
              <i id="progressFill"></i>
            </div>
            <div class="timer-box" id="timerBox">00:15</div>
          </div>

          <div style="margin-top:12px; display:flex; gap:8px;">
            <button class="btn" id="prevQ" style="display:none;">Sebelumnya</button>
            <button class="btn primary" id="nextQ" style="display:none;">Berikutnya</button>
            <button class="btn" id="finishQ" style="display:none;">Selesai</button>
          </div>
        </div>

        <!-- final card -->
        <div id="finalCard" class="card" style="display:none; margin-top:12px;">
          <div class="result-screen">
            <div style="font-size:16px; opacity:0.9;">Hasil Kuis</div>
            <div class="score-big" id="finalScore">0 / 0</div>
            <div id="finalMessage" style="margin-bottom:12px;"></div>

            <div style="display:flex; gap:8px; justify-content:center; margin-bottom:8px;">
              <input id="nameInput" placeholder="Nama untuk leaderboard" style="padding:8px;border-radius:8px;border:0;min-width:180px" />
              <button class="btn primary" id="saveScoreBtn">Simpan</button>
            </div>

            <div style="display:flex; gap:8px; justify-content:center;">
              <button class="btn" id="playAgainBtn">Main Lagi</button>
              <button class="btn" id="toReactionBtn">Coba Reaction Game</button>
            </div>
          </div>
        </div>

      </div>
    </div>

    <!-- Reaction Game Panel -->
    <div class="panel" style="margin-top:16px;">
      <header style="display:flex; justify-content:space-between; align-items:center; margin-bottom:8px;">
        <strong>Mini-Game: Reaction Speed</strong>
        <small class="small-muted">Tes reaksi — klik saat kotak berubah</small>
      </header>

      <div class="reaction-area">
        <div id="reactionTarget" class="target hidden">Tunggu...</div>
        <div style="display:flex; gap:8px; align-items:center;">
          <button class="btn primary" id="startReaction">Mulai</button>
          <button class="btn" id="stopReaction" disabled>Berhenti</button>
        </div>
        <div style="display:flex; gap:8px;">
          <div style="text-align:center;">
            <div style="font-size:18px; font-weight:800;" id="bestReaction">- ms</div>
            <div class="small-muted">Best</div>
          </div>
          <div style="text-align:center;">
            <div style="font-size:18px; font-weight:800;" id="lastReaction">- ms</div>
            <div class="small-muted">Terakhir</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- RIGHT SIDEBAR -->
  <div class="sidebar">
    <div class="panel small">
      <h3>Leaderboard Kuis</h3>
      <div id="quizLeaderboard" class="list"></div>
    </div>

    <div class="panel small">
      <h3>Leaderboard Reaction</h3>
      <div id="reactLeaderboard" class="list"></div>
    </div>

    <div class="panel small">
      <h3>Info</h3>
      <div style="font-size:14px; line-height:1.5;">
        Kuis: 10 soal, timer per soal 15 detik.  
        Reaction game mencatat waktu reaksi (ms). Skor dan best disimpan di browser (localStorage).
      </div>
    </div>
  </div>
</div>

<script>
/* ==========================
   === Data Kuis (10 soal) ===
   ========================== */
const QUESTIONS = [
  {q:"Siapakah nabi pertama?", a:["Nabi Muhammad","Nabi Adam","Nabi Ibrahim","Nabi Musa"], c:1},
  {q:"Kitab suci umat Islam adalah?", a:["Injil","Zabur","Al-Qur'an","Taurat"], c:2},
  {q:"Puasa wajib dilakukan pada bulan?", a:["Ramadhan","Syawal","Rabiul Awal","Dzulhijjah"], c:0},
  {q:"Kota lahir Nabi Muhammad adalah?", a:["Madinah","Baghdad","Kairo","Mekkah"], c:3},
  {q:"Jumlah rakaat shalat Subuh adalah?", a:["4","3","2","5"], c:2},
  {q:"Nama alam akhir malam turunnya Al-Qur'an?", a:["Lailatul Qadar","Nuzulul Quran","Isra Mi'raj","Maulid"], c:0},
  {q:"Ibadah haji wajib dilakukan di?", a:["Madinah","Mekkah","Jeddah","Riyadh"], c:1},
  {q:"Nabi yang membelah laut adalah?", a:["Nabi Musa","Nabi Isa","Nabi Ibrahim","Nabi Yusuf"], c:0},
  {q:"Hari raya umat Islam adalah?", a:["Paskah & Natal","Idul Fitri & Idul Adha","Diwali","Vesak"], c:1},
  {q:"Kitab suci berbahasa Arab diturunkan pada nabi?", a:["Nabi Isa","Nabi Muhammad","Nabi Musa","Nabi Dawud"], c:1}
];

/* ==========================
   === Element refs =========
   ========================== */
const startQuizBtn = document.getElementById('startQuizBtn');
const questionText = document.getElementById('questionText');
const answersBox = document.getElementById('answersBox');
const statusRow = document.getElementById('statusRow');
const timerBox = document.getElementById('timerBox');
const progressFill = document.getElementById('progressFill');
const aEls = [document.getElementById('a0'),document.getElementById('a1'),document.getElementById('a2'),document.getElementById('a3')];
const prevQ = document.getElementById('prevQ'), nextQ = document.getElementById('nextQ'), finishQ = document.getElementById('finishQ');
const finalCard = document.getElementById('finalCard'), quizCard = document.getElementById('quizCard');
const finalScore = document.getElementById('finalScore'), finalMessage = document.getElementById('finalMessage');
const nameInput = document.getElementById('nameInput'), saveScoreBtn = document.getElementById('saveScoreBtn');
const playAgainBtn = document.getElementById('playAgainBtn'), toReactionBtn = document.getElementById('toReactionBtn');
const quizLeaderboard = document.getElementById('quizLeaderboard');
const reactLeaderboard = document.getElementById('reactLeaderboard');

const startReaction = document.getElementById('startReaction'), stopReaction = document.getElementById('stopReaction');
const reactionTarget = document.getElementById('reactionTarget');
const bestReactionEl = document.getElementById('bestReaction'), lastReactionEl = document.getElementById('lastReaction');

const themeToggle = document.getElementById('themeToggle');
const resetAll = document.getElementById('resetAll');
const confettiCanvas = document.getElementById('confettiCanvas');

/* ==========================
   === State management =====
   ========================== */
let quizState = {
  active:false,
  order: [...Array(QUESTIONS.length).keys()], // indices
  idx:0,
  score:0,
  perQuestionTime:15, // seconds
  timer:null,
  timeLeft:0,
  answers: Array(QUESTIONS.length).fill(null)
};

let reactionState = {
  waiting:true,
  running:false,
  startAt:0,
  endAt:0,
  lastTime:null,
  bestTime: loadBestReaction()
};

/* ==========================
   === Audio: WebAudio API ==
   ========================== */
const audioCtx = new (window.AudioContext || window.webkitAudioContext)();

function beep(freq=440, duration=0.08, type='sine', gain=0.08){
  const o = audioCtx.createOscillator();
  const g = audioCtx.createGain();
  o.type = type;
  o.frequency.value = freq;
  g.gain.value = gain;
  o.connect(g); g.connect(audioCtx.destination);
  o.start();
  o.stop(audioCtx.currentTime + duration);
}

/* short feedback sounds */
function soundClick(){ beep(880,0.06,'sine',0.05) }
function soundCorrect(){ beep(880,0.12,'sawtooth',0.09); setTimeout(()=>beep(1320,0.08,'sine',0.07),90) }
function soundWrong(){ beep(220,0.18,'sine',0.12) }
function soundTick(){ beep(1200,0.04,'square',0.035) }

/* ==========================
   === Quiz logic ===========
   ========================== */
function shuffle(arr){ // Fisher-Yates
  for(let i=arr.length-1;i>0;i--){
    const j=Math.floor(Math.random()*(i+1));
    [arr[i],arr[j]]=[arr[j],arr[i]];
  }
  return arr;
}

function startQuiz(){
  // prepare
  quizState.active=true;
  quizState.order = shuffle([...Array(QUESTIONS.length).keys()]);
  quizState.idx = 0;
  quizState.score = 0;
  quizState.answers = Array(QUESTIONS.length).fill(null);
  quizCard.style.display='block';
  finalCard.style.display='none';
  answersBox.style.display='grid';
  statusRow.style.display='flex';
  nextQ.style.display='inline-block';
  finishQ.style.display='inline-block';
  prevQ.style.display='inline-block';
  showQuestion();
}

function showQuestion(){
  const qIndex = quizState.order[quizState.idx];
  const qObj = QUESTIONS[qIndex];
  questionText.textContent = `${quizState.idx+1}. ${qObj.q}`;
  // show answers (shuffle choices to avoid static positions)
  const choices = qObj.a.map((t,i)=>({t,i}));
  shuffle(choices);
  aEls.forEach((el,i)=>{
    if(choices[i]){
      el.style.display='block';
      el.textContent = choices[i].t;
      el.dataset.origIndex = choices[i].i; // original index to check correctness
      el.classList.remove('correct','wrong');
      el.onclick = ()=> selectAnswer(el);
    } else {
      el.style.display='none';
    }
  });

  // timer
  quizState.timeLeft = quizState.perQuestionTime;
  timerBox.textContent = formatTime(quizState.timeLeft);
  progressFill.style.width = ((quizState.idx)/QUESTIONS.length*100)+'%';
  startTimer();
}

function startTimer(){
  clearInterval(quizState.timer);
  quizState.timer = setInterval(()=>{
    quizState.timeLeft--;
    timerBox.textContent = formatTime(quizState.timeLeft);
    if(quizState.timeLeft<=5) soundTick();
    if(quizState.timeLeft<=0){
      clearInterval(quizState.timer);
      autoMarkWrong();
    }
  },1000);
}

function formatTime(sec){
  const s = Math.max(0,sec);
  return "00:" + (s<10?('0'+s):s);
}

function selectAnswer(el){
  // prevent double click
  if(!quizState.active) return;
  clearInterval(quizState.timer);
  const chosen = Number(el.dataset.origindex);
  const qIndex = quizState.order[quizState.idx];
  const correct = QUESTIONS[qIndex].c;
  // mark answers accordingly
  aEls.forEach(a=>{
    const oi = Number(a.dataset.origindex);
    if(oi===correct) a.classList.add('correct');
    if(a===el && oi!==correct) a.classList.add('wrong');
    a.onclick = null;
  });

  if(chosen === correct){
    quizState.score++;
    soundCorrect();
    finalMessage.textContent = "Jawaban benar! +1";
  } else {
    soundWrong();
    finalMessage.textContent = "Salah!";
  }
  quizState.answers[quizState.idx]=chosen;
  // show next after brief delay
  progressFill.style.width = ((quizState.idx+1)/QUESTIONS.length*100)+'%';
}

function autoMarkWrong(){
  // no selection in time
  aEls.forEach(a=>{
    const oi = Number(a.dataset.origindex);
    const qIndex = quizState.order[quizState.idx];
    if(oi===QUESTIONS[qIndex].c) a.classList.add('correct');
    a.onclick = null;
  });
  finalMessage.textContent = "Waktu habis!";
  soundWrong();
  quizState.answers[quizState.idx]=null;
  progressFill.style.width = ((quizState.idx+1)/QUESTIONS.length*100)+'%';
}

nextQ.addEventListener('click',()=>{
  goToIndex(quizState.idx+1);
});
prevQ.addEventListener('click',()=>{
  goToIndex(quizState.idx-1);
});
finishQ.addEventListener('click', finishQuiz);

function goToIndex(newIdx){
  if(newIdx<0) newIdx=0;
  if(newIdx>=QUESTIONS.length) return finishQuiz();
  quizState.idx=newIdx;
  showQuestion();
}

function finishQuiz(){
  clearInterval(quizState.timer);
  quizState.active=false;
  // show result
  quizCard.style.display='none';
  finalCard.style.display='block';
  finalScore.textContent = `${quizState.score} / ${QUESTIONS.length}`;
  const percent = Math.round((quizState.score/QUESTIONS.length)*100);
  finalMessage.textContent = `Kamu mendapatkan ${percent}%`;
  // trigger confetti on good score
  if(percent >= 70) {
    playConfetti();
    soundCorrect();
  } else {
    soundWrong();
  }
}

/* ==========================
   === Leaderboard (localStorage)
   ========================== */
const QUIZ_KEY = 'islam_quiz_board_v1';
const REACT_KEY = 'islam_react_board_v1';

function loadBoard(key){ try{ return JSON.parse(localStorage.getItem(key)) || []; }catch(e){return []} }
function saveBoard(key,arr){ localStorage.setItem(key, JSON.stringify(arr)); }

// render leaders
function renderQuizBoard(){
  const data = loadBoard(QUIZ_KEY).slice(0,7);
  quizLeaderboard.innerHTML = '';
  if(!data.length) {
    quizLeaderboard.innerHTML = '<div class="small-muted">Belum ada skor</div>'; return;
  }
  data.forEach((it,idx)=>{
    const div = document.createElement('div'); div.className='item';
    div.innerHTML = `<div>${idx+1}. ${escapeHtml(it.name)}</div><div>${it.score}/${QUESTIONS.length}</div>`;
    quizLeaderboard.appendChild(div);
  });
}
function renderReactBoard(){
  const data = loadBoard(REACT_KEY).slice(0,7);
  reactLeaderboard.innerHTML = '';
  if(!data.length) { reactLeaderboard.innerHTML = '<div class="small-muted">Belum ada skor</div>'; return; }
  data.forEach((it,idx)=>{
    const div = document.createElement('div'); div.className='item';
    div.innerHTML = `<div>${idx+1}. ${escapeHtml(it.name)}</div><div>${it.ms} ms</div>`;
    reactLeaderboard.appendChild(div);
  });
}

function saveQuizScore(){
  const name = (nameInput.value || 'Anonim').trim();
  const arr = loadBoard(QUIZ_KEY);
  arr.push({name, score: quizState.score, created: Date.now()});
  // sort desc by score
  arr.sort((a,b)=> b.score - a.score || a.created - b.created);
  saveBoard(QUIZ_KEY, arr.slice(0,30));
  renderQuizBoard();
  nameInput.value='';
}

saveScoreBtn.addEventListener('click', saveQuizScore);
playAgainBtn.addEventListener('click', ()=> { startQuiz(); window.scrollTo({top:0,behavior:'smooth'}); });

startQuizBtn.addEventListener('click', ()=> {
  // resume audio context if suspended
  if(audioCtx.state === 'suspended') audioCtx.resume();
  startQuiz();
});

/* reset all data */
resetAll.addEventListener('click', ()=>{
  if(confirm('Hapus semua skor dan data lokal?')) {
    localStorage.removeItem(QUIZ_KEY);
    localStorage.removeItem(REACT_KEY);
    reactionState.bestTime=null;
    saveBestReaction(null);
    renderQuizBoard();
    renderReactBoard();
  }
});

/* safety: simple HTML escape */
function escapeHtml(s){ return s.replace(/[&<>"']/g, c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])); }

/* ==========================
   === Reaction Game ========
   ========================== */
let reactionTimer = null;
let reactionAppearTimeout = null;

function loadBestReaction(){
  const v = Number(localStorage.getItem(REACT_KEY+'_best'));
  return isFinite(v) && v>0 ? v : null;
}
function saveBestReaction(val){
  if(val==null) localStorage.removeItem(REACT_KEY+'_best'); else localStorage.setItem(REACT_KEY+'_best', String(val));
}

function startReactionGame(){
  if(audioCtx.state === 'suspended') audioCtx.resume();
  reactionState.running = true;
  startReaction.disabled = true;
  stopReaction.disabled = false;
  reactionTarget.classList.add('hidden');
  reactionTarget.textContent = 'Tunggu...';
  scheduleAppear();
}

function stopReactionGame(){
  reactionState.running = false;
  startReaction.disabled = false;
  stopReaction.disabled = true;
  clearTimeout(reactionAppearTimeout);
  reactionTarget.classList.add('hidden');
  reactionTarget.textContent = 'Tunggu...';
}

function scheduleAppear(){
  clearTimeout(reactionAppearTimeout);
  const delay = 800 + Math.random()*2200; // appear between 0.8s - 3s
  reactionAppearTimeout = setTimeout(()=> {
    // show active state
    reactionTarget.classList.remove('hidden');
    reactionTarget.style.background = `linear-gradient(180deg, ${randColor()}, rgba(0,0,0,0.06))`;
    reactionTarget.textContent = 'Klik!';
    reactionState.startAt = performance.now();
    // if user didn't click in 2s, mark missed and schedule again
    reactionTimer = setTimeout(()=> {
      reactionTarget.textContent = 'Terlambat!';
      reactionState.startAt = 0;
      setTimeout(()=> {
        reactionTarget.classList.add('hidden');
        reactionTarget.textContent = 'Tunggu...';
        if(reactionState.running) scheduleAppear();
      },600);
    }, 3000);
  }, delay);
}

function randColor(){
  const greens = ['#00b371','#00ffae','#08a05b','#29c17c','#4fd8a6'];
  return greens[Math.floor(Math.random()*greens.length)];
}

reactionTarget.addEventListener('click', ()=>{
  if(!reactionState.running) return;
  if(!reactionState.startAt) {
    // clicked too early or after timeout
    soundWrong();
    reactionTarget.textContent = 'Gagal!';
    reactionState.lastTime = null;
    lastReactionEl.textContent = '- ms';
    setTimeout(()=> {
      reactionTarget.classList.add('hidden');
      reactionTarget.textContent = 'Tunggu...';
      if(reactionState.running) scheduleAppear();
    },600);
    return;
  }
  const now = performance.now();
  const ms = Math.round(now - reactionState.startAt);
  clearTimeout(reactionTimer);
  reactionState.lastTime = ms;
  // update UI
  lastReactionEl.textContent = ms + ' ms';
  // update best
  if(reactionState.bestTime===null || ms < reactionState.bestTime){
    reactionState.bestTime = ms;
    bestReactionEl.textContent = ms + ' ms';
    // save best and leaderboard
    saveBestReaction(ms);
    playConfettiSmall();
  }
  soundClick();
  // show short feedback then schedule next
  reactionTarget.textContent = 'Bagus!';
  reactionState.startAt = 0;
  // also add to reaction leaderboard candidate
  addReactionRecordPrompt(ms);
  setTimeout(()=> {
    reactionTarget.classList.add('hidden');
    reactionTarget.textContent = 'Tunggu...';
    if(reactionState.running) scheduleAppear();
  },700);
});

/* add to reaction leaderboard (non-blocking prompt) */
function addReactionRecordPrompt(ms){
  // small prompt via window prompt (non-intrusive)
  const save = confirm(`Reaksi ${ms} ms. Simpan ke leaderboard?`);
  if(save){
    const name = prompt('Masukkan nama (untuk leaderboard)', 'Player') || 'Anonim';
    const arr = loadBoard(REACT_KEY);
    arr.push({name, ms, created: Date.now()});
    arr.sort((a,b)=> a.ms - b.ms || a.created - b.created);
    saveBoard(REACT_KEY, arr.slice(0,30));
    renderReactBoard();
  }
}

/* control buttons */
startReaction.addEventListener('click', ()=> {
  reactionState.bestTime = loadBestReaction();
  if(reactionState.bestTime) bestReactionEl.textContent = reactionState.bestTime + ' ms';
  startReactionGame();
});
stopReaction.addEventListener('click', stopReactionGame);

/* initialize reaction UI best from storage */
if(reactionState.bestTime) bestReactionEl.textContent = reactionState.bestTime + ' ms';
else bestReactionEl.textContent = '- ms';
lastReactionEl.textContent = '- ms';

/* ==========================
   === Confetti ============
   ========================== */
/* Minimal confetti implementation (canvas) */
const confetti = {
  ctx: confettiCanvas.getContext('2d'),
  pieces: [],
  running: false,
  w: window.innerWidth, h: window.innerHeight,
  resize(){
    confettiCanvas.width = window.innerWidth;
    confettiCanvas.height = window.innerHeight;
    confetti.w = confettiCanvas.width; confetti.h = confettiCanvas.height;
  },
  spawn(count=80){
    const colors = ['#ffd166','#00ffae','#ff6666','#ff9a00','#ffffff'];
    for(let i=0;i<count;i++){
      confetti.pieces.push({
        x: Math.random()*confetti.w,
        y: -20 - Math.random()*confetti.h*0.2,
        vx: (Math.random()-0.5)*6,
        vy: 2 + Math.random()*6,
        r: 6 + Math.random()*8,
        color: colors[Math.floor(Math.random()*colors.length)],
        rot: Math.random()*360,
        o: 1
      });
    }
    if(!confetti.running) confetti.run();
  },
  run(){
    confetti.running = true;
    (function frame(){
      confetti.ctx.clearRect(0,0, confetti.w, confetti.h);
      for(let i=confetti.pieces.length-1;i>=0;i--){
        const p = confetti.pieces[i];
        p.x += p.vx; p.y += p.vy; p.vy += 0.08;
        p.rot += p.vx*2;
        p.o -= 0.005;
        confetti.ctx.save();
        confetti.ctx.translate(p.x,p.y);
        confetti.ctx.rotate(p.rot * Math.PI/180);
        confetti.ctx.globalAlpha = Math.max(0,p.o);
        confetti.ctx.fillStyle = p.color;
        confetti.ctx.fillRect(-p.r/2, -p.r/2, p.r, p.r*0.6);
        confetti.ctx.restore();
        if(p.y > confetti.h + 50 || p.o <= 0) confetti.pieces.splice(i,1);
      }
      if(confetti.pieces.length>0) requestAnimationFrame(frame);
      else { confetti.running = false; confetti.ctx.clearRect(0,0, confetti.w, confetti.h); }
    })();
  }
};

function playConfetti(){ confetti.spawn(140); }
function playConfettiSmall(){ confetti.spawn(50); }
window.addEventListener('resize', ()=> confetti.resize());
confetti.resize();

/* ==========================
   === Theme toggle =========
   ========================== */
themeToggle.addEventListener('click', ()=>{
  // toggle by flipping media emulation: we set a 'light' class on body to override prefers-color-scheme
  if(document.documentElement.getAttribute('data-theme') === 'light'){
    document.documentElement.removeAttribute('data-theme');
    document.documentElement.style.colorScheme = 'dark';
  } else {
    document.documentElement.setAttribute('data-theme','light');
    document.documentElement.style.colorScheme = 'light';
  }
});
/* CSS for manual light mode via attribute */
const style = document.createElement('style');
style.textContent = `
  [data-theme="light"] { --bg1:#f3faf5; --bg2:#eaf7ec; --card:#ffffff; --accent:#0a7a50; --muted:#2b3a33; --danger:#c0392b; --gold:#d67a00; }
`;
document.head.appendChild(style);

/* ==========================
   === Util & Init =========
   ========================== */
function escapeHtml(s){ return String(s).replace(/[&<>"']/g, c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c])); }

function initialRender(){
  renderQuizBoard();
  renderReactBoard();
  // hide quiz controls until start
  answersBox.style.display='none';
  statusRow.style.display='none';
  prevQ.style.display='none';
  nextQ.style.display='none';
  finishQ.style.display='none';
}

initialRender();
confetti.resize();

/* Save reaction leaderboard initial */
renderReactBoard();

/* small helpers: save reaction leaderboard when best changed */
function saveReactionScore(name, ms){
  const arr = loadBoard(REACT_KEY);
  arr.push({name, ms, created: Date.now()});
  arr.sort((a,b)=> a.ms - b.ms || a.created - b.created);
  saveBoard(REACT_KEY, arr.slice(0,30));
  renderReactBoard();
}

/* load saved leaders on page load */
window.addEventListener('load', ()=> {
  renderQuizBoard(); renderReactBoard();
});

/* keyboard support: numbers 1-4 to answer quickly */
window.addEventListener('keydown', (e)=>{
  if(!quizState.active) return;
  if(['1','2','3','4'].includes(e.key)){
    const idx = Number(e.key) - 1;
    if(aEls[idx] && aEls[idx].onclick) aEls[idx].click();
  }
});
</script>

</body>
</html>
