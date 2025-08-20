<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Teste de Conhecimento – Jovem Aprendiz Neoro Corpe</title>
<style>
  :root{
    --primary:#007bff;
    --primary-dark:#0056b3;
    --accent:#00b894;
  }
  *{box-sizing:border-box}
  body{font-family:Arial,Helvetica,sans-serif;margin:0;background:#f0f4f8;color:#222}
  header{background:linear-gradient(90deg,var(--primary),var(--accent));color:#fff;padding:16px;text-align:center}
  header h1{margin:0;font-size:1.3rem}
  main{max-width:760px;margin:22px auto;background:#fff;padding:20px;border-radius:12px;box-shadow:0 6px 16px rgba(0,0,0,.08)}
  .userInfo,.question{margin-bottom:18px;padding:12px;border-left:4px solid var(--primary);background:#f9fbfe;border-radius:8px}
  .userInfo p,.question p{margin:0 0 8px;font-weight:bold}
  input[type="text"],input[type="email"],input[type="tel"]{
    width:100%;padding:10px;border:1px solid #cfd8dc;border-radius:8px;margin-bottom:10px;font-size:15px
  }
  button{
    width:100%;padding:12px 18px;border:0;border-radius:10px;cursor:pointer;
    background:var(--primary);color:#fff;font-size:1rem;font-weight:600;
    box-shadow:0 4px 12px rgba(0,0,0,.12)
  }
  button:hover{background:var(--primary-dark)}
  #submitBtn{margin-top:8px}

  /* TELA FINAL EM TELA CHEIA BRANCA */
  #finalScreen{
    display:none;position:fixed;inset:0;background:#ffffff;color:#111;
    overflow:auto;padding:32px;text-align:center
  }
  #finalScreen h2{font-size:2rem;margin-bottom:10px}
  #finalScreen p{font-size:1.1rem;margin:6px 0}
  #finalScreen .email{font-size:2rem;font-weight:800;color:var(--primary);margin-top:14px}
  #finalScreen .lists{max-width:720px;margin:18px auto;display:grid;gap:14px}
  .list{background:#f6f9ff;border:1px solid #e5eefc;border-radius:10px;padding:14px;text-align:left}
  .list h3{margin:0 0 8px}
  .list ul{margin:0;padding-left:18px}
  .ok li{color:#1b5e20}      /* verde acertos */
  .bad li{color:#b71c1c}     /* vermelho erros */
  .alert{
    margin-top:14px;padding:10px;border:2px solid #ff5252;border-radius:10px;
    color:#b71c1c;font-weight:800;font-size:1.1rem;background:#fff2f2
  }

  /* Acessibilidade mínima pro foco */
  button:focus, input:focus{outline:3px solid #a5d8ff;outline-offset:2px}
</style>
</head>
<body>

<header>
  <h1>Teste de Conhecimento – Jovem Aprendiz <b>Neoro Corpe</b></h1>
</header>

<main id="mainContent">
  <!-- Tela de identificação -->
  <div id="userForm" class="userInfo">
    <p>Preencha suas informações para iniciar a prova:</p>
    <input type="text" id="userName" placeholder="Nome completo">
    <input type="email" id="userEmail" placeholder="Gmail">
    <input type="tel" id="userPhone" placeholder="Número de telefone">
    <button id="startBtn" onclick="startQuiz()">Iniciar Prova</button>
  </div>

  <!-- Quiz (renderizado via JS) -->
  <form id="quizForm" style="display:none;"></form>
  <button type="button" id="submitBtn" onclick="submitQuiz()" style="display:none;">Enviar Respostas</button>
</main>

<!-- Tela final branca -->
<div id="finalScreen" aria-live="polite">
  <h2>Resultado do Teste</h2>
  <p id="scoreText"></p>
  <p id="wrongText"></p>

  <div class="lists">
    <div class="list ok">
      <h3>✅ Questões acertadas:</h3>
      <ul id="correctList"></ul>
    </div>

    <div class="list bad">
      <h3>❌ Questões erradas:</h3>
      <ul id="wrongList"></ul>
    </div>
  </div>

  <p class="alert">⚠️ Mínimo de erros permitido: <b>3</b> ⚠️</p>

  <p><b>E-mail de contato:</b></p>
  <p>Não mande nada, apenas espere a gente enviar a sua resposta neste e-mail:</p>
  <p class="email">neorocorpesite@gmail.com</p>
</div>

<script>
/* ---------- Banco de questões ---------- */
const questions = [
  { text: "Assinale a frase escrita corretamente:", type: "radio", name: "q1",
    options: [["a","Nós vai aprender muito aqui."],["b","Nós vamos aprender muito aqui."],["c","Nós vai aprendermos muito aqui."]],
    correct: "b" },

  { text: "Coloque a vírgula no lugar correto na frase:<br><i>Maria João e Pedro chegaram cedo.</i>",
    type: "text", name: "q2", correct: "Maria, João e Pedro chegaram cedo." },

  { text: "Encontre o erro na frase e reescreva-a:<br><i>Os aluno chegou atrasado.</i>",
    type: "text", name: "q3", correct: "Os alunos chegaram atrasados." },

  { text: "Se um vale-refeição diário é de R$ 20,00, quanto será o valor total para 22 dias úteis?",
    type: "text", name: "q4", correct: "440" }, /* aceitamos variações via normalização */

  { text: "Qual é o próximo número da sequência? 2 – 4 – 8 – 16 – ___ – 64",
    type: "text", name: "q5", correct: "32" },

  { text: "Uma sala tem 8 fileiras com 6 cadeiras em cada. Quantas cadeiras há no total?",
    type: "text", name: "q6", correct: "48" },

  { text: "Para criar um documento no computador, qual programa você poderia usar?",
    type: "radio", name: "q7",
    options: [["a","Microsoft Word"],["b","WhatsApp"],["c","Google Chrome"]],
    correct: "a" },

  { text: "No teclado do computador, qual tecla usamos para apagar o que está à esquerda do cursor?",
    type: "text", name: "q8", correct: "backspace" },

  { text: "Se você terminar uma tarefa antes do horário, o que faria?",
    type: "radio", name: "q9",
    options: [["a","Esperaria até a hora acabar"],["b","Pediria outra tarefa ou ajudaria um colega"],["c","Iria embora mais cedo"]],
    correct: "b" },

  { text: "Um cliente chega com dúvida e você não sabe a resposta. O que faz?",
    type: "radio", name: "q10",
    options: [["a","Ignora e continua trabalhando"],["b","Diz que não sabe e tenta adivinhar"],["c","Explica que vai procurar a informação com alguém responsável"]],
    correct: "c" }
];

/* ---------- Utilidades ---------- */
function shuffle(arr){
  for(let i=arr.length-1;i>0;i--){
    const j = Math.floor(Math.random()*(i+1));
    [arr[i],arr[j]] = [arr[j],arr[i]];
  }
}
function stripHtml(s){ return s.replace(/<[^>]+>/g,''); }

/* Normaliza resposta de texto:
   - minúsculas
   - remove espaços extras
   - para números em dinheiro: remove "r$", pontos, vírgulas
*/
function normalizeTextAnswer(val){
  if(!val) return "";
  let v = val.toLowerCase().trim();
  // caso seja valor de dinheiro, aceitar "r$ 440,00", "440", "440,00", etc
  if(/\d/.test(v)){
    const vMoney = v.replace(/\s/g,'').replace(/r\$/g,'').replace(/\./g,'').replace(/,/g,'');
    // se virar só número, devolve número em string
    if(/^\d+$/.test(vMoney)) return vMoney;
  }
  return v.normalize("NFD").replace(/[\u0300-\u036f]/g,""); // remove acentos
}

/* ---------- Fluxo ---------- */
function startQuiz(){
  const name = document.getElementById("userName").value.trim();
  const email = document.getElementById("userEmail").value.trim();
  const phone = document.getElementById("userPhone").value.trim();

  if(!name || !email || !phone){
    alert("Por favor, preencha Nome, Gmail e Telefone para iniciar.");
    return;
  }

  // Oculta identificação e mostra quiz
  document.getElementById("userForm").style.display = "none";
  document.getElementById("quizForm").style.display = "block";
  document.getElementById("submitBtn").style.display = "block";

  // Embaralha perguntas (anti-cola ao recarregar)
  shuffle(questions);

  // Render
  const form = document.getElementById("quizForm");
  form.innerHTML = "";
  questions.forEach((q, idx)=>{
    const div = document.createElement("div");
    div.className = "question";
    div.innerHTML = `<p>${idx+1}. ${q.text}</p>`;
    if(q.type==="radio"){
      // embaralhar alternativas também
      shuffle(q.options);
      q.options.forEach(opt=>{
        div.innerHTML += `<label><input type="radio" name="${q.name}" value="${opt[0]}"> ${opt[1]}</label><br>`;
      });
    }else{
      div.innerHTML += `<input type="text" name="${q.name}" placeholder="Digite sua resposta">`;
    }
    form.appendChild(div);
  });
}

function submitQuiz(){
  let score = 0;
  const correctList = [];
  const wrongList = [];

  questions.forEach((q, idx)=>{
    let ansVal = "";
    if(q.type==="radio"){
      const checked = document.querySelector(`[name="${q.name}"]:checked`);
      ansVal = checked ? checked.value : "";
      if(ansVal && ansVal.toLowerCase() === q.correct.toLowerCase()){
        score++; correctList.push(`${idx+1}. ${stripHtml(q.text)}`);
      }else{
        wrongList.push(`${idx+1}. ${stripHtml(q.text)}`);
      }
    }else{
      const inp = document.querySelector(`[name="${q.name}"]`);
      ansVal = normalizeTextAnswer(inp?.value || "");
      const expected = normalizeTextAnswer(q.correct);
      if(ansVal && ansVal === expected){
        score++; correctList.push(`${idx+1}. ${stripHtml(q.text)}`);
      }else{
        wrongList.push(`${idx+1}. ${stripHtml(q.text)}`);
      }
    }
  });

  const total = questions.length;
  const wrong = total - score;

  // Some tudo e abre a tela final branca
  document.getElementById("mainContent").style.display = "none";
  const final = document.getElementById("finalScreen");
  final.style.display = "block";

  document.getElementById("scoreText").innerText = `Você acertou: ${score} de ${total}`;
  document.getElementById("wrongText").innerText = `Você errou: ${wrong} de ${total}`;

  const ulOk = document.getElementById("correctList");
  const ulBad = document.getElementById("wrongList");
  ulOk.innerHTML = ""; ulBad.innerHTML = "";
  correctList.forEach(t=> ulOk.innerHTML += `<li>${t}</li>`);
  wrongList.forEach(t=> ulBad.innerHTML += `<li>${t}</li>`);
}
</script>
</body>
</html>
