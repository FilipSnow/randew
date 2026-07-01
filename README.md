<!DOCTYPE html>
<html lang="sk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pozvanie na rande 💌</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Segoe UI', system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      min-height: 100vh;
      background:
        radial-gradient(circle at top left, rgba(255,255,255,.35), transparent 35%),
        linear-gradient(135deg, #ff8fb3, #a36bff 45%, #5cc8ff);
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 24px;
      overflow-x: hidden;
    }
    .card {
      width: 100%;
      max-width: 780px;
      background: rgba(255, 255, 255, 0.16);
      border: 1px solid rgba(255,255,255,.35);
      backdrop-filter: blur(18px);
      border-radius: 32px;
      padding: 34px;
      box-shadow: 0 24px 80px rgba(0,0,0,.25);
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .card::before {
      content: "";
      position: absolute;
      inset: -80px;
      background: radial-gradient(circle, rgba(255,255,255,.18), transparent 35%);
      animation: floatGlow 7s ease-in-out infinite alternate;
      pointer-events: none;
    }
    @keyframes floatGlow {
      from { transform: translate(-30px, -20px); }
      to { transform: translate(30px, 20px); }
    }
    .content { position: relative; z-index: 1; }
    .badge {
      display: inline-block;
      padding: 8px 14px;
      border-radius: 999px;
      background: rgba(255,255,255,.22);
      font-size: 14px;
      margin-bottom: 12px;
    }
    h1 {
      font-size: clamp(34px, 7vw, 68px);
      margin: 8px 0 12px;
      line-height: 1.02;
      text-shadow: 0 8px 30px rgba(0,0,0,.22);
    }
    p {
      font-size: 18px;
      line-height: 1.55;
      margin: 10px auto;
      max-width: 620px;
    }
    .mini-story {
      margin: 24px auto;
      display: grid;
      gap: 12px;
      grid-template-columns: repeat(3, 1fr);
    }
    .story-box {
      background: rgba(255,255,255,.18);
      border: 1px solid rgba(255,255,255,.24);
      border-radius: 22px;
      padding: 18px 12px;
      min-height: 116px;
    }
    .emoji { font-size: 34px; display: block; margin-bottom: 8px; }
    .question {
      font-size: clamp(26px, 5vw, 44px);
      font-weight: 800;
      margin-top: 24px;
    }
    .buttons {
      min-height: 110px;
      margin: 20px 0;
      position: relative;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 18px;
      flex-wrap: wrap;
    }
    button, select, input {
      font: inherit;
    }
    .btn {
      border: 0;
      border-radius: 999px;
      padding: 15px 26px;
      cursor: pointer;
      font-weight: 800;
      box-shadow: 0 10px 25px rgba(0,0,0,.18);
      transition: transform .18s ease, box-shadow .18s ease;
    }
    .btn:hover { transform: translateY(-2px) scale(1.03); }
    .yes {
      background: #fff;
      color: #d94685;
      font-size: 21px;
    }
    .no {
      background: rgba(0,0,0,.35);
      color: white;
      position: relative;
    }
    .planner {
      margin-top: 26px;
      background: rgba(255,255,255,.16);
      border: 1px solid rgba(255,255,255,.22);
      border-radius: 24px;
      padding: 22px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
      text-align: left;
    }
    label {
      display: block;
      font-weight: 700;
      margin-bottom: 8px;
    }
    input, select {
      width: 100%;
      border: 0;
      border-radius: 15px;
      padding: 13px 14px;
      background: rgba(255,255,255,.9);
      color: #2d1b45;
      outline: none;
    }
    .full { grid-column: 1 / -1; }
    .result {
      margin-top: 20px;
      display: none;
      background: rgba(255,255,255,.92);
      color: #2d1b45;
      border-radius: 24px;
      padding: 22px;
      text-align: center;
      animation: pop .35s ease;
    }
    @keyframes pop {
      from { transform: scale(.9); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
    .footer-note {
      opacity: .88;
      font-size: 14px;
      margin-top: 18px;
    }
    .heart {
      position: fixed;
      top: -30px;
      font-size: 22px;
      animation: fall linear forwards;
      pointer-events: none;
      z-index: 999;
    }
    @keyframes fall {
      to { transform: translateY(110vh) rotate(360deg); opacity: 0; }
    }
    @media (max-width: 700px) {
      .card { padding: 24px 18px; border-radius: 24px; }
      .mini-story { grid-template-columns: 1fr; }
      .planner { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>
  <main class="card">
    <div class="content">
      <div class="badge">špeciálna pozvánka 💌</div>
      <h1>Ahoj, kráska ✨</h1>
      <p>
        Táto stránka bola vytvorená s veľmi vážnym, vedecky podloženým cieľom:
        zistiť, či pôjdeš so mnou na rande.
      </p>
      <section class="mini-story">
        <div class="story-box">
          <span class="emoji">😎</span>
          Ja sa tvárim, že som úplne pokojný.
        </div>
        <div class="story-box">
          <span class="emoji">🧠</span>
          Môj mozog: “Prosím, klikni áno.”
        </div>
        <div class="story-box">
          <span class="emoji">❤️</span>
          A moje srdce má už rezervovaný stôl.
        </div>
      </section>
      <div class="question">Pôjdeš so mnou na rande?</div>
      <div class="buttons" id="buttonArea">
        <button class="btn yes" id="yesBtn">Áno 😌❤️</button>
        <button class="btn no" id="noBtn">Nie 😭</button>
      </div>
      <section class="planner" id="planner">
        <div>
          <label for="date">Kedy?</label>
          <input type="date" id="date" />
        </div>
        <div>
          <label for="activity">Čo podnikneme?</label>
          <select id="activity">
            <option value="jedlo">Dobré jedlo 🍕</option>
            <option value="výlet">Menší výlet 🌲</option>
            <option value="kino">Kino alebo filmový večer 🎬</option>
            <option value="káva">Káva / drink ☕</option>
            <option value="prekvapenie">Prekvapenie, dôveruj procesu ✨</option>
            <option value="ona vymyslí">Ty vymyslíš a ja poslúchnem 😇</option>
          </select>
        </div>
        <div class="full">
          <label for="note">Mini poznámka pre mňa</label>
          <input id="note" placeholder="Napr. nech je tam jedlo, inak nejdem 😄" />
        </div>
      </section>
      <div class="result" id="resultBox">
        <h2>Výborne. Historická udalosť potvrdená. 🎉</h2>
        <p id="summary"></p>
        <p><strong>Screenshotni mi toto alebo mi pošli dátum a plán. Ja sa už budem tváriť, že nie som nervózny.</strong></p>
      </div>
      <p class="footer-note">P.S. Tlačidlo „Nie“ má vlastnú vôľu. Netreba ho brať vážne.</p>
    </div>
  </main>

  <script>
    const noBtn = document.getElementById('noBtn');
    const yesBtn = document.getElementById('yesBtn');
    const area = document.getElementById('buttonArea');
    const resultBox = document.getElementById('resultBox');
    const summary = document.getElementById('summary');
    const dateInput = document.getElementById('date');
    const activityInput = document.getElementById('activity');
    const noteInput = document.getElementById('note');

    const today = new Date().toISOString().split('T')[0];
    dateInput.min = today;

    function moveNoButton() {
      const areaRect = area.getBoundingClientRect();
      const maxX = Math.max(0, areaRect.width - noBtn.offsetWidth);
      const maxY = Math.max(0, areaRect.height - noBtn.offsetHeight);
      const x = Math.random() * maxX;
      const y = Math.random() * maxY;
      noBtn.style.position = 'absolute';
      noBtn.style.left = x + 'px';
      noBtn.style.top = y + 'px';
      noBtn.textContent = ['Nie 😭', 'Skús inam 😌', 'Nedá sa 😇', 'Error 404 😂'][Math.floor(Math.random() * 4)];
    }

    noBtn.addEventListener('mouseenter', moveNoButton);
    noBtn.addEventListener('click', moveNoButton);
    noBtn.addEventListener('touchstart', function(e) {
      e.preventDefault();
      moveNoButton();
    });

    function rainHearts() {
      const symbols = ['❤️','💖','✨','💕','🎉','💌'];
      for (let i = 0; i < 55; i++) {
        const heart = document.createElement('div');
        heart.className = 'heart';
        heart.textContent = symbols[Math.floor(Math.random() * symbols.length)];
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = (2.2 + Math.random() * 2.2) + 's';
        heart.style.fontSize = (18 + Math.random() * 18) + 'px';
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 5000);
      }
    }

    yesBtn.addEventListener('click', () => {
      const date = dateInput.value ? new Date(dateInput.value).toLocaleDateString('sk-SK') : 'dátum ešte vyberieme';
      const activity = activityInput.options[activityInput.selectedIndex].text;
      const note = noteInput.value.trim();
      summary.innerHTML = `Plán: <strong>${activity}</strong><br>Dátum: <strong>${date}</strong>${note ? `<br>Poznámka: <strong>${note}</strong>` : ''}`;
      resultBox.style.display = 'block';
      resultBox.scrollIntoView({ behavior: 'smooth', block: 'center' });
      rainHearts();
    });
  </script>
</body>
</html>
