# gaming-senegal
Mon site de jeux vidéo

<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#101020">
  <title>GAMING SENEGAL | Jeux vidéo</title>

  <style>
    :root {
      --fond: #101020;
      --carte: #1b1b35;
      --turquoise: #00ffcc;
      --texte: #ffffff;
      --gris: #b8bfd3;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, sans-serif;
      background: var(--fond);
      color: var(--texte);
      line-height: 1.6;
    }

    header {
      background: #080812;
      border-bottom: 2px solid var(--turquoise);
      padding: 18px 5%;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 15px;
    }

    .logo {
      color: var(--turquoise);
      font-size: 22px;
      font-weight: bold;
    }

    nav {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    nav a:hover {
      color: var(--turquoise);
    }

    .hero {
      text-align: center;
      padding: 75px 20px;
      background:
        radial-gradient(ellipse at top, #24315a, transparent 70%);
    }

    .hero h1 {
      font-size: clamp(32px, 7vw, 56px);
      line-height: 1.2;
      margin-bottom: 18px;
    }

    .hero h1 span {
      color: var(--turquoise);
    }

    .hero p {
      color: var(--gris);
      max-width: 600px;
      margin: 0 auto 25px;
    }

    .button {
      display: inline-block;
      border: none;
      border-radius: 8px;
      background: var(--turquoise);
      color: #07151a;
      padding: 12px 20px;
      font-weight: bold;
      text-decoration: none;
      cursor: pointer;
      font-size: 15px;
    }

    .button:hover {
      transform: translateY(-2px);
      filter: brightness(1.1);
    }

    section {
      padding: 45px 5%;
      scroll-margin-top: 85px;
    }

    .section-title {
      color: var(--turquoise);
      font-size: 30px;
      text-align: center;
      margin-bottom: 10px;
    }

    .section-intro {
      text-align: center;
      color: var(--gris);
      margin-bottom: 30px;
    }

    .games {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 22px;
    }

    .game-card {
      background: var(--carte);
      border: 1px solid #30304e;
      border-radius: 14px;
      overflow: hidden;
      transition: transform 0.2s;
    }

    .game-card:hover {
      transform: translateY(-5px);
    }

    .game-card img {
      width: 100%;
      height: 170px;
      object-fit: cover;
      display: block;
      background: #292945;
    }

    .game-content {
      padding: 18px;
    }

    .game-content h3 {
      margin-bottom: 8px;
    }

    .game-content p {
      color: var(--gris);
      margin-bottom: 15px;
      font-size: 14px;
    }

    .game-content .button {
      width: 100%;
    }

    .mini-game {
      background: var(--carte);
      max-width: 600px;
      margin: auto;
      padding: 25px;
      border-radius: 15px;
      text-align: center;
      border: 1px solid #30304e;
    }

    .score {
      font-size: 20px;
      margin: 12px 0;
    }

    #target {
      display: none;
      width: 75px;
      height: 75px;
      border-radius: 50%;
      border: 3px solid white;
      background: var(--turquoise);
      color: #07151a;
      font-size: 28px;
      cursor: pointer;
      margin: 20px auto;
      touch-action: manipulation;
    }

    #message {
      color: var(--gris);
      margin: 15px 0;
    }

    .contact {
      text-align: center;
      background: #15152a;
    }

    .contact p {
      color: var(--gris);
      margin: 10px 0 20px;
    }

    footer {
      text-align: center;
      padding: 22px;
      background: #080812;
      color: var(--gris);
      font-size: 13px;
    }

    @media (max-width: 500px) {
      .navbar {
        justify-content: center;
      }

      nav {
        justify-content: center;
      }

      .hero {
        padding: 55px 15px;
      }

      section {
        padding: 35px 16px;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="navbar">
      <div class="logo">🎮 GAMING SENEGAL</div>

      <nav>
        <a href="#accueil">Accueil</a>
        <a href="#jeux">Jeux</a>
        <a href="#mini-jeu">Mini-jeu</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="accueil">
      <h1>Bienvenue sur <span>GAMING SENEGAL</span></h1>

      <p>
        Découvre l'univers du gaming, explore tes jeux préférés
        et amuse-toi avec notre mini-jeu gratuit !
      </p>

      <a class="button" href="#jeux">Découvrir les jeux</a>
    </section>

    <section id="jeux">
      <h2 class="section-title">🎯 Nos jeux</h2>
      <p class="section-intro">
        Découvre notre sélection de jeux vidéo.
      </p>

      <div class="games">

        <article class="game-card">
          <img
            src="https://placehold.co/600x350/263b2c/ffffff?text=MINECRAFT"
            alt="Illustration Minecraft"
          >

          <div class="game-content">
            <h3>Minecraft</h3>
            <p>
              Explore, construis et laisse libre cours à ton imagination.
            </p>

            <button class="button" onclick="ouvrirJeu('Minecraft')">
              JOUER
            </button>
          </div>
        </article>

        <article class="game-card">
          <img
            src="https://placehold.co/600x350/18345b/ffffff?text=ASPHALT"
            alt="Illustration jeu de course"
          >

          <div class="game-content">
            <h3>Asphalt Legends</h3>
            <p>
              Découvre les courses automobiles et la vitesse.
            </p>

            <button class="button" onclick="ouvrirJeu('Asphalt Legends')">
              JOUER
            </button>
          </div>
        </article>

        <article class="game-card">
          <img
            src="https://placehold.co/600x350/17452c/ffffff?text=EFOOTBALL"
            alt="Illustration jeu de football"
          >

          <div class="game-content">
            <h3>eFootball</h3>
            <p>
              Entre sur le terrain et vis ta passion du football.
            </p>

            <button class="button" onclick="ouvrirJeu('eFootball')">
              JOUER
            </button>
          </div>
        </article>

      </div>

      <p id="game-message" style="text-align:center; margin-top:20px; color:#00ffcc;"></p>
    </section>

    <section id="mini-jeu">
      <h2 class="section-title">⚡ Mini-jeu : Attrape la cible</h2>

      <p class="section-intro">
        Appuie sur la cible le plus de fois possible en 10 secondes.
      </p>

      <div class="mini-game">
        <p>Prêt à tester tes réflexes ?</p>

        <div class="score">
          Score : <span id="score">0</span>
        </div>

        <div>
          Temps : <span id="time">10</span> secondes
        </div>

        <button class="button" id="start-button" onclick="demarrerJeu()">
          COMMENCER
        </button>

        <button id="target" onclick="marquerPoint()" aria-label="Attraper la cible">
          🎯
        </button>

        <p id="message">Appuie sur Commencer pour jouer.</p>

        <p>
          🏆 Record :
          <strong id="record">0</strong>
        </p>
      </div>
    </section>

    <section class="contact" id="contact">
      <h2 class="section-title">📩 Contact</h2>

      <p>
        Une idée ou une suggestion pour GAMING SENEGAL ?
      </p>

      <a
        class="button"
        href="mailto:contact@gamingsenegal.com?subject=GAMING%20SENEGAL"
      >
        Nous contacter
      </a>
    </section>
  </main>

  <footer>
    <p>© <span id="year"></span> GAMING SENEGAL — Tous droits réservés.</p>
    <p>Site de démonstration créé pour les passionnés de jeux vidéo.</p>
  </footer>

  <script>
    // Affiche l'année actuelle.
    document.getElementById("year").textContent =
      new Date().getFullYear();

    // Boutons des jeux : les jeux complets ne sont pas intégrés.
    function ouvrirJeu(nom) {
      document.getElementById("game-message").textContent =
        nom + " n'est pas encore jouable sur ce site. Le jeu complet doit être ajouté ou lié séparément.";
    }

    // Mini-jeu de réflexes.
    let score = 0;
    let temps = 10;
    let actif = false;
    let chronometre = null;

    let record = 0;

    try {
      record = Number(localStorage.getItem("recordGamingSenegal")) || 0;
    } catch (e) {
      record = 0;
    }

    document.getElementById("record").textContent = record;

    function demarrerJeu() {
      if (actif) return;

      score = 0;
      temps = 10;
      actif = true;

      document.getElementById("score").textContent = score;
      document.getElementById("time").textContent = temps;
      document.getElementById("message").textContent = "Vite ! Attrape la cible !";
      document.getElementById("target").style.display = "block";
      document.getElementById("start-button").disabled = true;
      document.getElementById("start-button").textContent = "EN COURS...";

      chronometre = setInterval(function() {
        temps--;
        document.getElementById("time").textContent = temps;

        if (temps <= 0) {
          terminerJeu();
        }
      }, 1000);
    }

    function marquerPoint() {
      if (!actif) return;

      score++;
      document.getElementById("score").textContent = score;

      // Change la cible pour rendre le jeu plus amusant.
      const couleurs = ["#00ffcc", "#ffcc00", "#ff5c8a", "#8a7dff"];
      const couleur = couleurs[Math.floor(Math.random() * couleurs.length)];

      const cible = document.getElementById("target");
      cible.style.background = couleur;
      cible.style.transform = "scale(0.9)";

      setTimeout(function() {
        cible.style.transform = "scale(1)";
      }, 80);
    }

    function terminerJeu() {
      actif = false;
      clearInterval(chronometre);

      document.getElementById("target").style.display = "none";
      document.getElementById("start-button").disabled = false;
      document.getElementById("start-button").textContent = "REJOUER";

      document.getElementById("message").textContent =
        "Temps écoulé ! Tu as marqué " + score + " point(s).";

      if (score > record) {
        record = score;

        try {
          localStorage.setItem("recordGamingSenegal", String(record));
        } catch (e) {
          // Le record reste affiché pendant cette session.
        }

        document.getElementById("record").textContent = record;
        document.getElementById("message").textContent +=
          " Nouveau record ! Bravo !";
      }
    }
  </script>

</body>
</html>
