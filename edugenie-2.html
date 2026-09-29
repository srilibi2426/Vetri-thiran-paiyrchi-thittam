<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>EduGenie – Gemini Powered Learning Assistant</title>
<link href="https://fonts.googleapis.com/css2?family=Mukta:wght@400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#14213D; --teal:#0E7C7B; --saffron:#F2A900; --bg:#EEF3F8; --card:#fff; --line:#D5DEE9; --muted:#5B6B82;
    --user:#14213D; --bot:#fff;
  }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0}
  body{font-family:"Mukta","Noto Sans Tamil",system-ui,sans-serif;background:var(--bg);color:var(--ink);display:flex;flex-direction:column;font-size:16px;line-height:1.55}
  header{background:var(--ink);color:#fff;padding:14px 18px;display:flex;align-items:center;gap:12px}
  .logo{width:38px;height:38px;border-radius:50%;background:var(--saffron);display:grid;place-items:center;font-weight:800;color:var(--ink);font-size:20px}
  header h1{font-size:20px;margin:0;font-weight:800}
  header p{margin:0;font-size:13px;opacity:.75}
  .bar{background:var(--card);border-bottom:1px solid var(--line);padding:10px 14px;display:flex;flex-wrap:wrap;gap:8px;align-items:center}
  .modes{display:flex;gap:6px;flex-wrap:wrap}
  .mode{border:1.5px solid var(--line);background:#fff;color:var(--ink);padding:6px 12px;border-radius:999px;font:inherit;font-size:14px;cursor:pointer}
  .mode[aria-pressed="true"]{background:var(--teal);border-color:var(--teal);color:#fff}
  select,input[type=password],textarea{font:inherit;border:1.5px solid var(--line);border-radius:10px;padding:8px 10px;background:#fff;color:var(--ink)}
  select{font-size:14px}
  .spacer{flex:1}
  button.ghost{border:none;background:none;color:var(--teal);font:inherit;font-size:14px;cursor:pointer;text-decoration:underline}
  #setup{background:#FFF7DD;border-bottom:1px solid #EBD58A;padding:12px 14px;font-size:14px}
  #setup input{width:min(360px,100%);margin:6px 6px 0 0}
  #setup button{background:var(--ink);color:#fff;border:none;border-radius:10px;padding:9px 16px;font:inherit;cursor:pointer}
  #chat{flex:1;overflow-y:auto;padding:16px 14px;display:flex;flex-direction:column;gap:12px}
  .msg{max-width:min(720px,92%);padding:10px 14px;border-radius:14px;word-wrap:break-word}
  .msg.user{align-self:flex-end;background:var(--user);color:#fff;border-bottom-right-radius:4px}
  .msg.bot{align-self:flex-start;background:var(--bot);border:1px solid var(--line);border-bottom-left-radius:4px}
  .msg.err{border-color:#C0392B;color:#8E2A20;background:#FFF1EF}
  .msg h3{margin:.4em 0 .2em;font-size:17px}
  .msg ul,.msg ol{margin:.3em 0;padding-left:1.3em}
  .msg code{background:#EEF3F8;padding:1px 5px;border-radius:5px;font-size:14px}
  .msg pre{background:var(--ink);color:#fff;padding:10px;border-radius:10px;overflow-x:auto}
  .msg pre code{background:none;color:inherit}
  .hint{color:var(--muted);text-align:center;margin:auto;max-width:460px}
  .hint b{color:var(--ink)}
  .chips{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-top:12px}
  .chips button{border:1.5px dashed var(--teal);background:#fff;color:var(--teal);border-radius:12px;padding:7px 12px;font:inherit;font-size:14px;cursor:pointer}
  form{display:flex;gap:8px;padding:10px 14px;background:var(--card);border-top:1px solid var(--line);padding-bottom:max(10px,env(safe-area-inset-bottom))}
  textarea{flex:1;resize:none;height:46px;max-height:140px}
  form button{background:var(--saffron);border:none;color:var(--ink);font-weight:800;font:inherit;font-weight:800;border-radius:10px;padding:0 18px;cursor:pointer}
  form button:disabled{opacity:.5}
  :focus-visible{outline:3px solid var(--saffron);outline-offset:2px}
  .dots span{display:inline-block;width:7px;height:7px;margin-right:3px;border-radius:50%;background:var(--teal);animation:b 1s infinite}
  .dots span:nth-child(2){animation-delay:.15s}.dots span:nth-child(3){animation-delay:.3s}
  @keyframes b{0%,80%,100%{opacity:.25}40%{opacity:1}}
  @media (prefers-reduced-motion:reduce){.dots span{animation:none}}
</style>
</head>
<body>
<header>
  <div class="logo">E</div>
  <div>
    <h1>EduGenie</h1>
    <p>Gemini powered learning assistant · Vetri Thiran Payirchi Thittam</p>
  </div>
</header>

<div id="setup">
  Google Gemini API key venum (free-ah <b>aistudio.google.com/apikey</b> la edukalam). Key unga browser la mattum save aagum.<br>
  <input type="password" id="key" placeholder="Paste Gemini API key" autocomplete="off">
  <button id="saveKey" type="button">Save key</button>
</div>

<div class="bar">
  <div class="modes" role="group" aria-label="Learning mode">
    <button class="mode" data-mode="explain" aria-pressed="true" type="button">Explain</button>
    <button class="mode" data-mode="quiz" aria-pressed="false" type="button">Quiz</button>
    <button class="mode" data-mode="summary" aria-pressed="false" type="button">Summary</button>
    <button class="mode" data-mode="plan" aria-pressed="false" type="button">Study plan</button>
  </div>
  <span class="spacer"></span>
  <label class="sr" for="lang" style="position:absolute;left:-9999px">Language</label>
  <select id="lang">
    <option value="English">English</option>
    <option value="Tamil (தமிழ்)">தமிழ்</option>
    <option value="Tanglish (Tamil written in English letters)">Tanglish</option>
  </select>
  <select id="level" aria-label="Level">
    <option>Beginner</option><option>Intermediate</option><option>Advanced</option>
  </select>
  <button class="ghost" id="clear" type="button">Clear</button>
</div>

<main id="chat" aria-live="polite"></main>

<form id="form">
  <textarea id="input" placeholder="Topic or question type pannunga..." rows="1" aria-label="Your question"></textarea>
  <button id="send" type="submit">Send</button>
</form>

<script>
const MODEL = "gemini-2.5-flash";
const $ = s => document.querySelector(s);
const chat = $("#chat"), input = $("#input"), sendBtn = $("#send");
let mode = "explain", history = [];

const MODE_PROMPTS = {
  explain: "Explain the topic step by step with a simple real-life example, then end with a one-line takeaway.",
  quiz: "Create a 5-question multiple-choice quiz on the topic (options A-D). Put the answer key with short reasons at the very end under the heading 'Answers'.",
  summary: "Summarise the given text or topic into clear bullet points, then give 3 key terms with meanings.",
  plan: "Create a practical day-by-day study plan for the topic with daily goals, resources to look for, and a final self-test."
};
const SAMPLES = {
  explain: ["What is machine learning?", "Explain photosynthesis", "How does HTTP work?"],
  quiz: ["Python basics", "Indian Constitution", "Newton's laws"],
  summary: ["Summarise: Digital India initiative", "Summarise the water cycle"],
  plan: ["Learn Python in 14 days", "Prepare for TNPSC in 30 days"]
};

function esc(t){return t.replace(/[&<>]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;"}[c]))}
function md(text){
  let s = esc(text);
  s = s.replace(/```(\w*)\n([\s\S]*?)```/g,(_,l,c)=>`<pre><code>${c}</code></pre>`);
  s = s.replace(/`([^`\n]+)`/g,"<code>$1</code>");
  s = s.replace(/^#{1,4}\s+(.+)$/gm,"<h3>$1</h3>");
  s = s.replace(/\*\*([^*\n]+)\*\*/g,"<b>$1</b>");
  s = s.replace(/(^|\n)((?:[*-]\s+.+(?:\n|$))+)/g,(_,p,b)=>p+"<ul>"+b.trim().split("\n").map(l=>"<li>"+l.replace(/^[*-]\s+/,"")+"</li>").join("")+"</ul>");
  s = s.replace(/(^|\n)((?:\d+\.\s+.+(?:\n|$))+)/g,(_,p,b)=>p+"<ol>"+b.trim().split("\n").map(l=>"<li>"+l.replace(/^\d+\.\s+/,"")+"</li>").join("")+"</ol>");
  return s.replace(/\n{2,}/g,"<br><br>").replace(/\n/g,"<br>").replace(/(<\/(?:ul|ol|h3|pre)>)<br>/g,"$1");
}

function add(role, html, cls=""){
  const d = document.createElement("div");
  d.className = "msg " + role + " " + cls;
  d.innerHTML = html;
  chat.appendChild(d);
  chat.scrollTop = chat.scrollHeight;
  return d;
}

function renderHint(){
  chat.innerHTML = `<div class="hint"><b>Vanakkam! Naan EduGenie.</b><br>Edhaavadhu topic kelunga — explain, quiz, summary, study plan ellam panren.<div class="chips"></div></div>`;
  const box = chat.querySelector(".chips");
  SAMPLES[mode].forEach(t=>{
    const b = document.createElement("button"); b.type="button"; b.textContent = t;
    b.onclick = () => { input.value = t; form.requestSubmit(); };
    box.appendChild(b);
  });
}

document.querySelectorAll(".mode").forEach(b=>b.onclick=()=>{
  mode = b.dataset.mode;
  document.querySelectorAll(".mode").forEach(x=>x.setAttribute("aria-pressed", x===b));
  if(!history.length) renderHint();
});
$("#clear").onclick = () => { history = []; renderHint(); };

function getKey(){ try{return localStorage.getItem("edugenie_key")||""}catch(e){return window.__k||""} }
function setKey(k){ try{localStorage.setItem("edugenie_key",k)}catch(e){window.__k=k} }
function refreshSetup(){ $("#setup").style.display = getKey() ? "none" : "block"; }
$("#saveKey").onclick = () => { const k = $("#key").value.trim(); if(k){ setKey(k); $("#key").value=""; refreshSetup(); } };

input.addEventListener("keydown", e => { if(e.key==="Enter" && !e.shiftKey){ e.preventDefault(); form.requestSubmit(); }});
input.addEventListener("input", () => { input.style.height="46px"; input.style.height=Math.min(input.scrollHeight,140)+"px"; });

const form = $("#form");
form.addEventListener("submit", async e => {
  e.preventDefault();
  const text = input.value.trim();
  if(!text) return;
  const key = getKey();
  if(!key){ refreshSetup(); add("bot","Mudhalla API key save pannunga.","err"); return; }
  if(!history.length) chat.innerHTML = "";
  add("user", esc(text));
  input.value = ""; input.style.height="46px";
  sendBtn.disabled = true;
  const wait = add("bot", '<span class="dots"><span></span><span></span><span></span></span>');

  const system = `You are EduGenie, a friendly learning assistant for students in a skill-training programme (Vetri Thiran Payirchi Thittam). Learner level: ${$("#level").value}. Reply in ${$("#lang").value}. ${MODE_PROMPTS[mode]} Keep answers clear, accurate and not too long. Use short paragraphs, bullet points, and simple words.`;
  history.push({role:"user", parts:[{text}]});

  try{
    const res = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/${MODEL}:generateContent`,{
      method:"POST",
      headers:{"Content-Type":"application/json","x-goog-api-key":key},
      body: JSON.stringify({ systemInstruction:{parts:[{text:system}]}, contents: history })
    });
    const data = await res.json();
    if(!res.ok) throw new Error(data.error?.message || "Request failed");
    const reply = data.candidates?.[0]?.content?.parts?.map(p=>p.text||"").join("") || "";
    if(!reply) throw new Error("Empty response. Vera maadhiri kelunga.");
    history.push({role:"model", parts:[{text:reply}]});
    wait.innerHTML = md(reply);
  }catch(err){
    history.pop();
    wait.className = "msg bot err";
    wait.textContent = "Error: " + err.message;
  }
  sendBtn.disabled = false;
  chat.scrollTop = chat.scrollHeight;
  input.focus();
});

refreshSetup();
renderHint();
</script>
</body>
</html>
