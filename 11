<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Descubra a Verdade Sobre Seu Relacionamento</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: url('https://images.unsplash.com/photo-1522199755839-a2bacb67c546?auto=format&fit=crop&w=1050&q=80') no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      min-height: 100vh;
    }

    .intro-container {
      background: rgba(0, 0, 0, 0.8);
      backdrop-filter: blur(10px);
      border: 2px solid #e60000;
      border-radius: 15px;
      max-width: 700px;
      padding: 40px 30px;
      margin: 40px auto;
      box-shadow: 0 0 30px rgba(255, 0, 0, 0.5);
      text-align: center;
      animation: fadeIn 1s ease-in-out;
    }

    .intro-container h1, .intro-container h2 {
      font-size: 28px;
      color: #ff4d4d;
      margin-bottom: 20px;
    }

    .intro-container p {
      font-size: 18px;
      color: #ffd6d6;
      margin-bottom: 30px;
    }

    .start-btn {
      background-color: #e60000;
      color: white;
      border: none;
      padding: 15px 30px;
      font-size: 18px;
      border-radius: 10px;
      cursor: pointer;
      text-decoration: none;
      transition: background-color 0.3s ease;
    }

    .start-btn:hover {
      background-color: #b30000;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    #quiz-section {
      display: none;
      padding: 20px;
      max-width: 600px;
      margin: 0 auto;
    }

    .question-box {
      background: rgba(0, 0, 0, 0.85);
      border-radius: 15px;
      padding: 20px;
      margin-bottom: 20px;
      box-shadow: 0 0 15px rgba(255, 0, 0, 0.4);
      text-align: center;
    }

    .question-box h2 {
      font-size: 22px;
      color: #fff;
      margin-bottom: 20px;
    }

    .question-box button {
      display: block;
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      font-size: 16px;
      background-color: #333;
      color: white;
      border: 1px solid #555;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .question-box button:hover {
      background-color: #e60000;
    }

    #final-step {
      display: none;
      text-align: center;
      margin-top: 40px;
    }

    .pay-btn {
      background: #e60000;
      color: white;
      padding: 15px 25px;
      margin: 10px;
      border-radius: 10px;
      text-decoration: none;
      font-size: 18px;
      display: inline-block;
    }

    .input-field {
      margin: 20px auto;
      display: flex;
      flex-direction: column;
      max-width: 400px;
      gap: 10px;
    }

    .input-field input {
      padding: 12px;
      border-radius: 8px;
      border: none;
      font-size: 16px;
    }

    .input-field input::placeholder {
      color: #999;
    }
  </style>
</head>
<body>

  <!-- TELA ANTI-CURIOSOS -->
  <div class="intro-container" id="pre-intro">
    <h1>❗Este conteúdo não é para qualquer um</h1>
    <p>
      O que você está prestes a ver pode ser doloroso, mas necessário.<br><br>
      Este teste é feito apenas para quem <strong>REALMENTE</strong> quer saber a verdade e está preparado(a) para lidar com ela.<br><br>
      Se você está apenas curioso(a), recomendamos sair agora mesmo.
    </p>
    <button class="start-btn" onclick="liberarIntro()">Estou preparado(a) para saber a verdade</button>
  </div>

  <!-- INTRO ORIGINAL -->
  <div class="intro-container" id="intro" style="display:none;">
    <h1>⚠️ Cuidado: Você Pode Estar Sendo Enganado</h1>
    <p>
      Muitas pessoas passaram anos ao lado de alguém que escondia uma traição silenciosa.<br>
      Não responder esse quiz agora pode significar viver uma mentira pelo resto da vida.<br><br>
      Se você sente que algo mudou, essa é a sua chance de descobrir a verdade.<br>
      Prepare-se para encarar perguntas diretas, baseadas em comportamentos reais de quem trai.<br><br>
      <strong>Você só precisa de 2 minutos. E pode mudar tudo.</strong>
    </p>
    <button class="start-btn" onclick="startQuiz()">Começar Análise Agora</button>
  </div>

  <!-- QUIZ -->
  <div id="quiz-section"></div>

  <!-- ETAPA FINAL -->
  <div id="final-step"></div>

  <script>
    const questions = [
      "Ele(a) começou a sair mais do que o normal sem você?",
      "Evita contato físico ou emocional ultimamente?",
      "Esconde o celular ou mudou senhas de forma repentina?",
      "Parece nervoso(a) ao receber mensagens perto de você?",
      "Passa muito tempo online, mas responde pouco?",
      "Começou a se arrumar demais para saídas simples?",
      "Te acusa de coisas que ele(a) mesmo poderia estar fazendo?",
      "Você sente que está sendo enganado(a)?"
    ];

    const comfortMessages = [
      "Você não está exagerando. Intuição raramente falha.",
      "Você merece saber a verdade. E estamos aqui por isso.",
      "Ninguém deve viver em dúvida. Você está sendo forte.",
      "Lembre-se: quem ama, não esconde. Você merece clareza.",
      "Seu desconforto é válido. E sua coragem é admirável.",
      "A dor da dúvida machuca — mas a verdade liberta.",
      "Você já foi forte demais por tempo demais. Agora é hora de resposta.",
      "Sigilo absoluto. Estamos com você nessa."
    ];

    let current = 0;

    function liberarIntro() {
      document.getElementById("pre-intro").style.display = "none";
      document.getElementById("intro").style.display = "block";
    }

    function startQuiz() {
      document.getElementById("intro").style.display = "none";
      document.getElementById("quiz-section").style.display = "block";
      showQuestion();
    }

    function showQuestion() {
      const container = document.getElementById("quiz-section");
      container.innerHTML = `
        <div class="question-box">
          <h2>${questions[current]}</h2>
          <button onclick="delayNext()">Sim</button>
          <button onclick="delayNext()">Não</button>
          <button onclick="delayNext()">Às vezes</button>
        </div>
      `;
    }

    function delayNext() {
      const container = document.getElementById("quiz-section");
      const message = comfortMessages[current % comfortMessages.length];
      container.innerHTML = `
        <div class="question-box">
          <h2>Analisando sua resposta...</h2>
          <p>${message}</p>
        </div>
      `;
      setTimeout(nextQuestion, 5000);
    }

    function nextQuestion() {
      current++;
      if (current < questions.length) {
        showQuestion();
      } else {
        document.getElementById("quiz-section").innerHTML = `
          <div class="question-box">
            <h2>Finalizando sua análise...</h2>
            <p>Você está mais perto da verdade. E nós estamos aqui por você.</p>
            <p>A decisão de continuar ignorando ou encarar é sua. Mas saiba: sua intuição não falha.</p>
          </div>
        `;
        setTimeout(showFinalStep, 5000);
      }
    }

    function showFinalStep() {
      document.getElementById("quiz-section").style.display = "none";
      const final = document.getElementById("final-step");
      final.style.display = "block";

      let minutes = 9;
      let seconds = 59;

      const countdown = setInterval(() => {
        if (seconds === 0) {
          if (minutes === 0) {
            clearInterval(countdown);
            document.getElementById("countdown-text").innerText = "Expirado!";
            return;
          }
          minutes--;
          seconds = 59;
        } else {
          seconds--;
        }
        document.getElementById("countdown-text").innerText = `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
      }, 1000);

      final.innerHTML = `
        <div class="intro-container">
          <h2>⚠️ Você sente que algo está errado — e está certo em investigar</h2>
          <p>Muitas pessoas vivem com dúvidas por anos, sem nunca encarar a verdade. Mas você decidiu olhar de frente. Isso exige coragem.</p>
          <p>Nossa análise é 100% sigilosa e feita para ajudar pessoas como você — que estão cansadas de mentiras e querem respostas reais.</p>
          <p><strong>Sigilo absoluto. Ele(a) jamais saberá.</strong></p>

          <div style="background:#1a0000;padding:15px;border-radius:10px;margin:20px 0;">
            <p style="color:#ff6666;font-weight:bold;">🎯 Oferta exclusiva para você!<br>Validade: <span id="countdown-text">10:00</span></p>
            <p style="color:#ffd6d6;">Após esse tempo, essa oportunidade será encerrada para sempre.</p>
          </div>

          <div class="input-field">
            <input type="text" placeholder="Instagram do(a) parceiro(a)">
            <input type="text" placeholder="Seu WhatsApp para envio do PDF">
          </div>

          <a class="pay-btn" href="https://buy.stripe.com/7sYdRa6Uc5OF8BybyFfUQ01" target="_blank">Quero a varredura secreta - R$19,90</a>
          <a class="pay-btn" href="https://buy.stripe.com/bJecN6a6ogtjaJG46dfUQ00" target="_blank">Ver resultado do quiz - R$9,90</a>
        </div>
      `;
    }
  </script>
</body>
</html>
