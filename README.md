<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Break the Siege, Save Lives</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #e0f7f9;
      color: #333;
    }

    header {
      background-color: #40e0d0; /* Turquoise */
      color: white;
      padding: 1em;
      text-align: center;
    }

    nav {
      display: flex;
      justify-content: center;
      background-color: #f76c3c; /* Orange */
      padding: 0.5em;
    }

    nav button {
      background: none;
      border: none;
      color: white;
      font-size: 1em;
      margin: 0 1em;
      cursor: pointer;
    }

    .language-toggle {
      position: absolute;
      top: 1em;
      right: 1em;
    }

    .language-toggle button {
      background-color: white;
      border: 1px solid #40e0d0;
      margin-left: 0.5em;
      padding: 0.2em 0.6em;
      cursor: pointer;
      color: #40e0d0;
    }

    .tab-content {
      display: none;
      padding: 2em;
    }

    .tab-content.active {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
    }

    .tab-image {
      max-width: 300px;
      width: 100%;
      margin-right: 2em;
      margin-bottom: 1em;
    }

    .tab-text {
      flex: 1;
      min-width: 280px;
      text-align: justify;
    }

    h2 {
      font-weight: bold;
    }

    .subsection {
      margin-top: 2em;
    }

    .subsection h3 {
      font-weight: bold;
    }

    .social-links {
      margin-top: 1em;
    }

    .social-links a {
      margin-right: 1em;
      text-decoration: none;
      color: #f76c3c;
      font-weight: bold;
    }

    @media (max-width: 768px) {
      .tab-content {
        flex-direction: column;
        align-items: center;
      }

      .tab-image {
        margin-right: 0;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Break the Siege, Save Lives</h1>
    <div class="language-toggle">
      <button onclick="setLanguage('en')">ENGLISH</button>
      <button onclick="setLanguage('de')">DEUTSCH</button>
    </div>
  </header>

  <nav>
    <button onclick="showTab('about')">ABOUT</button>
    <button onclick="showTab('getinvolved')">GET INVOLVED</button>
  </nav>

  <!-- ABOUT TAB -->
  <div id="about" class="tab-content active">
    <img class="tab-image" src="about-image.jpg" alt="About Image">
    <div class="tab-text" id="about-text">
      <h2>WHO WE ARE</h2>
      <p>
        We are everyday people who believe in peace and safety for everyone, children above all. We are independent, international, and unaffiliated with any government or political party.
        Our aim is peace and protection of human lives.
        The siege and childslaughter must end.
      </p>
    </div>
  </div>

  <!-- GET INVOLVED TAB -->
  <div id="getinvolved" class="tab-content">
    <img class="tab-image" src="getinvolved-image.jpg" alt="Get Involved Image">
    <div class="tab-text" id="getinvolved-text">
      <p>
        As a result of the Gaza war, children have been disproportionately impacted in the Gaza Strip, where 40% of the population is 14 or under. More than 700,000 children in Gaza were displaced. UN Secretary General Antonio Guterres warned that "Gaza is becoming a graveyard for children. Hundreds of girls and boys are reportedly being killed or injured every day". More than 50,000 children had been killed or injured in Gaza. In late September 2024, Oxfam and Action on Armed Violence reported that the number of children killed in Gaza over the past year was the highest recorded in a single year for any conflict worldwide in the last 20 years.
      </p>
      <div class="subsection">
        <h3>HOW YOU CAN HELP</h3>
        <p>
          - Contact your representatives and demand immediate ceasefire<br>
          - Spread awareness about the humanitarian crisis<br>
          - Advocate for children's rights and protection
        </p>

        <div class="social-links">
          <a href="https://twitter.com/intent/tweet?text=Break%20the%20Siege%2C%20Save%20Lives%20%23Gaza" target="_blank">Share on Twitter</a>
          <a href="https://www.instagram.com" target="_blank">Share on Instagram</a>
          <a href="#">More...</a>
        </div>
      </div>
    </div>
  </div>

  <script>
    const translations = {
      en: {
        about: {
          title: "WHO WE ARE",
          text: `We are everyday people who believe in peace and safety for everyone, children above all. We are independent, international, and unaffiliated with any government or political party.
          Our aim is peace and protection of human lives.
          The siege and childslaughter must end.`
        },
        getinvolved: {
          text: `As a result of the Gaza war, children have been disproportionately impacted in the Gaza Strip, where 40% of the population is 14 or under. More than 700,000 children in Gaza were displaced. UN Secretary General Antonio Guterres warned that "Gaza is becoming a graveyard for children. Hundreds of girls and boys are reportedly being killed or injured every day". More than 50,000 children had been killed or injured in Gaza. In late September 2024, Oxfam and Action on Armed Violence reported that the number of children killed in Gaza over the past year was the highest recorded in a single year for any conflict worldwide in the last 20 years.`,
          helpTitle: "HOW YOU CAN HELP",
          helpPoints: `- Contact your representatives and demand immediate ceasefire<br>
          - Spread awareness about the humanitarian crisis<br>
          - Advocate for children's rights and protection`
        }
      },
      de: {
        about: {
          title: "WER WIR SIND",
          text: `Wir sind gewöhnliche Menschen, die an Frieden und Sicherheit für alle glauben, vor allem für Kinder. Wir sind unabhängig, international und keiner Regierung oder politischen Partei zugehörig.
          Unser Ziel ist Frieden und der Schutz menschlichen Lebens.
          Die Belagerung und das Töten von Kindern müssen aufhören.`
        },
        getinvolved: {
          text: `Infolge des Krieges in Gaza sind Kinder im Gazastreifen überproportional betroffen, wo 40 % der Bevölkerung unter 14 Jahre alt sind. Über 700.000 Kinder in Gaza wurden vertrieben. UN-Generalsekretär António Guterres warnte, dass "Gaza zu einem Friedhof für Kinder wird. Hunderte Mädchen und Jungen sollen täglich getötet oder verletzt werden". Über 50.000 Kinder wurden in Gaza getötet oder verletzt. Ende September 2024 berichteten Oxfam und Action on Armed Violence, dass die Zahl der im letzten Jahr in Gaza getöteten Kinder die höchste in einem einzigen Jahr für jeden Konflikt weltweit in den letzten 20 Jahren war.`,
          helpTitle: "WIE SIE HELFEN KÖNNEN",
          helpPoints: `- Kontaktieren Sie Ihre Abgeordneten und fordern Sie einen sofortigen Waffenstillstand<br>
          - Verbreiten Sie Informationen über die humanitäre Krise<br>
          - Setzen Sie sich für Kinderrechte und Schutz ein`
        }
      }
    };

    function showTab(tabName) {
      document.querySelectorAll('.tab-content').forEach(tab => {
        tab.classList.remove('active');
      });
      document.getElementById(tabName).classList.add('active');
    }

    function setLanguage(lang) {
      const aboutText = document.getElementById('about-text');
      const getInvolvedText = document.getElementById('getinvolved-text');

      aboutText.innerHTML = `
        <h
