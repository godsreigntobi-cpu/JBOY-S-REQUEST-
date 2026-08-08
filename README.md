# JBOY-S-REQUEST-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SAYONARA | CODM</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
    }

    body {
      background: #050505;
      color: white;
      overflow-x: hidden;
    }

    /* Background grid */
    body::before {
      content: "";
      position: fixed;
      inset: 0;
      background:
        linear-gradient(rgba(255,255,255,.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.025) 1px, transparent 1px);
      background-size: 45px 45px;
      pointer-events: none;
      z-index: -2;
    }

    body::after {
      content: "";
      position: fixed;
      width: 600px;
      height: 600px;
      background: #e60000;
      opacity: .07;
      filter: blur(150px);
      top: -200px;
      right: -150px;
      z-index: -1;
    }

    /* NAVBAR */

    nav {
      height: 80px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 7%;
      border-bottom: 1px solid #222;
      background: rgba(0,0,0,.8);
      backdrop-filter: blur(10px);
      position: relative;
      z-index: 10;
    }

    .logo {
      font-size: 22px;
      font-weight: 900;
      letter-spacing: 4px;
    }

    .logo span {
      color: #e60000;
    }

    nav ul {
      display: flex;
      gap: 35px;
      list-style: none;
    }

    nav a {
      color: #aaa;
      text-decoration: none;
      font-size: 13px;
      text-transform: uppercase;
      letter-spacing: 2px;
      transition: .3s;
    }

    nav a:hover {
      color: white;
    }

    .status {
      border: 1px solid #333;
      padding: 10px 15px;
      font-size: 11px;
      color: #aaa;
      letter-spacing: 1px;
    }

    .status i {
      display: inline-block;
      width: 7px;
      height: 7px;
      background: #00ff66;
      border-radius: 50%;
      margin-right: 7px;
      box-shadow: 0 0 10px #00ff66;
    }

    /* HERO */

    .hero {
      min-height: 650px;
      padding: 100px 7%;
      display: flex;
      align-items: center;
      position: relative;
    }

    .hero-content {
      max-width: 850px;
    }

    .mini-title {
      color: #e60000;
      font-size: 12px;
      font-weight: bold;
      letter-spacing: 6px;
      margin-bottom: 20px;
    }

    .hero h1 {
      font-size: clamp(70px, 13vw, 180px);
      line-height: .8;
      font-weight: 1000;
      letter-spacing: -8px;
      text-transform: uppercase;
      text-shadow: 8px 8px 0 #111;
    }

    .hero h1 span {
      color: transparent;
      -webkit-text-stroke: 2px #fff;
    }

    .description {
      margin-top: 35px;
      max-width: 520px;
      color: #888;
      line-height: 1.8;
      font-size: 14px;
    }

    .buttons {
      margin-top: 35px;
      display: flex;
      gap: 15px;
    }

    .btn {
      padding: 16px 30px;
      text-decoration: none;
      text-transform: uppercase;
      font-weight: bold;
      font-size: 12px;
      letter-spacing: 2px;
      transition: .3s;
    }

    .primary {
      background: #e60000;
      color: white;
      box-shadow: 0 0 25px rgba(230,0,0,.25);
    }

    .primary:hover {
      background: white;
      color: black;
      transform: translateY(-3px);
    }

    .secondary {
      border: 1px solid #333;
      color: white;
    }

    .secondary:hover {
      border-color: #e60000;
    }

    /* SIDE DECOR */

    .crosshair {
      position: absolute;
      right: 10%;
      top: 28%;
      width: 250px;
      height: 250px;
      border: 1px solid #222;
      border-radius: 50%;
      opacity: .6;
    }

    .crosshair::before,
    .crosshair::after {
      content: "";
      position: absolute;
      background: #333;
    }

    .crosshair::before {
      width: 100%;
      height: 1px;
      top: 50%;
    }

    .crosshair::after {
      height: 100%;
      width: 1px;
      left: 50%;
    }

    .crosshair span {
      position: absolute;
      width: 25px;
      height: 25px;
      border: 2px solid #e60000;
      border-radius: 50%;
      left: calc(50% - 12px);
      top: calc(50% - 12px);
      box-shadow: 0 0 20px #e60000;
    }

    /* STATS */

    .stats {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      margin: 0 7%;
      border-top: 1px solid #222;
      border-bottom: 1px solid #222;
    }

    .stat {
      padding: 30px;
      border-right: 1px solid #222;
    }

    .stat:last-child {
      border-right: none;
    }

    .stat h2 {
      font-size: 30px;
      margin-bottom: 8px;
    }

    .stat p {
      color: #666;
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    /* LOADOUT */

    .section {
      padding: 100px 7%;
    }

    .section-title {
      margin-bottom: 45px;
    }

    .section-title small {
      color: #e60000;
      letter-spacing: 4px;
      font-size: 10px;
    }

    .section-title h2 {
      font-size: 45px;
      margin-top: 10px;
      text-transform: uppercase;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .card {
      min-height: 260px;
      background: #0b0b0b;
      border: 1px solid #222;
      padding: 30px;
      position: relative;
      overflow: hidden;
      transition: .3s;
    }

    .card:hover {
      border-color: #e60000;
      transform: translateY(-6px);
    }

    .card-number {
      position: absolute;
      right: 20px;
      top: 15px;
      color: #222;
      font-size: 70px;
      font-weight: bold;
    }

    .card h3 {
      position: relative;
      margin-top: 100px;
      font-size: 23px;
    }

    .card p {
      color: #666;
      margin-top: 10px;
      font-size: 12px;
      line-height: 1.6;
    }

    .weapon {
      color: #e60000;
      font-size: 10px;
      letter-spacing: 3px;
      text-transform: uppercase;
    }

    /* FOOTER */

    footer {
      border-top: 1px solid #222;
      padding: 35px 7%;
      display: flex;
      justify-content: space-between;
      color: #555;
      font-size: 10px;
      letter-spacing: 2px;
    }

    footer strong {
      color: white;
    }

    /* MOBILE */

    @media (max-width: 800px) {

      nav ul {
        display: none;
      }

      .status {
        display: none;
      }

      .hero {
        min-height: 600px;
        padding-top: 70px;
      }

      .hero h1 {
        font-size: 75px;
        letter-spacing: -4px;
      }

      .crosshair {
        opacity: .2;
        right: -80px;
        top: 40%;
      }

      .stats {
        grid-template-columns: repeat(2, 1fr);
      }

      .stat {
        border-bottom: 1px solid #222;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      footer {
        flex-direction: column;
        gap: 15px;
      }
    }
  </style>
</head>

<body>

  <nav>
    <div class="logo">SAYO<span>NARA</span></div>

    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#loadout">Loadout</a></li>
      <li><a href="#stats">Stats</a></li>
    </ul>

    <div class="status">
      <i></i> SYSTEM ONLINE
    </div>
  </nav>


  <section class="hero" id="home">

    <div class="hero-content">

      <div class="mini-title">CALL OF DUTY MOBILE // PLAYER PROFILE</div>

      <h1>SAYO<br><span>NARA</span></h1>

      <p class="description">
        Welcome to the battlefield. A dark space dedicated to
        precision, speed and domination. Load your weapon,
        lock your target and enter the match.
      </p>

      <div class="buttons">
        <a href="#loadout" class="btn primary">View Loadout</a>
        <a href="#stats" class="btn secondary">View Stats</a>
      </div>

    </div>

    <div class="crosshair">
      <span></span>
    </div>

  </section>


  <section class="stats" id="stats">

    <div class="stat">
      <h2>87%</h2>
      <p>Win Rate</p>
    </div>

    <div class="stat">
      <h2>2.41</h2>
      <p>K/D Ratio</p>
    </div>

    <div class="stat">
      <h2>1.8K</h2>
      <p>Matches</p>
    </div>

    <div class="stat">
      <h2>Legendary</h2>
      <p>Rank</p>
    </div>

  </section>


  <section class="section" id="loadout">

    <div class="section-title">
      <small>// CURRENT LOADOUT</small>
      <h2>Arsenal</h2>
    </div>

    <div class="cards">

      <div class="card">
        <div class="card-number">01</div>
        <div class="weapon">Primary Weapon</div>
        <h3>ASSAULT RIFLE</h3>
        <p>
          Balanced damage, accuracy and mobility.
          Built for aggressive mid-range fights.
        </p>
      </div>

      <div class="card">
        <div class="card-number">02</div>
        <div class="weapon">Secondary Weapon</div>
        <h3>HANDGUN</h3>
        <p>
          Fast draw speed for those moments when
          the primary weapon runs dry.
        </p>
      </div>

      <div class="card">
        <div class="card-number">03</div>
        <div class="weapon">Tactical</div>
        <h3>FLASH / SMOKE</h3>
        <p>
          Control the battlefield, break enemy
          sightlines and create the perfect opening.
        </p>
      </div>

    </div>

  </section>


  <footer>
    <div><strong>SAYONARA</strong> // PLAYER PROFILE</div>
    <div>CODM FAN PROJECT • 2026</div>
  </footer>


</body>
</html>
