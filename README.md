<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Break the Siege, Save Lives</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #cce7f6, #e6f4f9);
      color: #00334d;
    }

    header {
      background: linear-gradient(to right, #0077b6, #00b4d8);
      padding: 20px;
      color: white;
      text-align: center;
      font-size: 1.5rem;
    }

    .language-toggle {
      display: flex;
      justify-content: center;
      margin: 10px;
      gap: 15px;
    }

    .language-toggle span {
      cursor: pointer;
      padding: 6px 12px;
      border-radius: 4px;
      border: 2px solid transparent;
      font-weight: bold;
    }

    .language-toggle span.active {
      border-color: #0077b6;
      background-color: #dff6fd;
    }

    nav {
      display: flex;
      justify-content: center;
      background: #caf0f8;
    }

    nav button {
      padding: 12px 25px;
      background: none;
      border: none;
      cursor: pointer;
      font-size: 1rem;
      color: #0077b6;
      border-bottom: 3px solid transparent;
    }

    nav button.active {
      border-bottom: 3px solid #0077b6;
      font-weight: bold;
    }

    main {
      max-width: 1000px;
      margin: 30px auto;
      padding: 20px;
      background: white;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0, 119, 182, 0.1);
    }

    .tab-content {
      display: none;
      gap: 20px;
      align-items: flex-start;
      flex-wrap: wrap;
    }

    .tab-content.active {
      display: flex;
    }

    .tab-content img {
      max-width: 100%;
      width: 350px;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }

    .tab-text {
      flex: 1;
      min-width: 250px;
      line-height: 1.6;
      font-size: 1rem;
      text-align: justify;
    }

    .tab-text b {
      display: block;
      margin-bottom: 10px;
    }

    .share-links {
      margin-top: 20px;
      font-size: 0.95rem;
    }

    .share-links a {
      margin-right: 10px;
      text-decoration: none;
      color: #0077b6;
    }

    @media (max-width: 768px) {
      .tab-content {
        flex-direction: column;
        align-items: center;
      }

      .tab-content img {
        width: 100%;
      }

      .tab-text {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>

  <header>Break the Siege, Save Lives</header>

  <div class="language-toggle">
    <span id="lang-en" class="active">ENGLISH</span>
    <span id="lang-de">DEUTSCH</span>
  </div>

  <nav>
    <button class="tab-button active" data-tab="about">ABOUT</button>
    <button class="tab-button" data-tab="getinvolved">GET INVOLVED</button>
  </nav>

  <main>
    <div id="about" class="tab-content active">
      <img src="about-image.jpg" alt="About">
      <div class="tab-text" id="about-text">
        <b>WHO WE ARE</b>
        We are everyday people who believe in peace and safety for everyone, children above all.

        We are independent, international, and unaffiliated with any government or political party. Our aim is peace and protection of human lives. The siege and the killing of children must end.
      </div>
    </div>

    <div id="getinvolved" class="tab-content">
      <img src="getinvolved-image.jpg" alt="Get Involved">
      <div class="tab-text" id="getinvolved-text">
        As a result of the Gaza war, children have been disproportionately impacted in the Gaza Strip, where 40% of the population is 14 or under. More than 700,000 children in Gaza were displaced. UN Secretary General Antonio Guterres warned that "Gaza is becoming a graveyard for children. Hundreds of girls and boys are reportedly being killed or injured every day." More than 50,000 children had been killed or injured in Gaza. In late September 2024, Oxfam and Action on Armed Violence reported that the number of children killed in Gaza over the past year was the highest recorded in a single year for any conflict worldwide in the last 20 years.

        <b>HOW YOU CAN HELP</b>
        - Contact your representatives and demand immediate ceasefire  
        - Spread awareness about the humanitarian crisis  
        - Advocate for children's rights and protection

        <div class="share-links">
          Share this page:
          <a href="https://twitter.com/intent/tweet?text=Break+the+Siege,+Save+Children&url=https://yourwebsite.com" target="_blank">Twitter</a>
          <a href="https://www.instagram.com" target="_blank">Instagram</a>
          <a href="#" onclick="navigator.clipboard.writeText(window.location.href); alert('Link copied to clipboard!')">Copy Link</a>
        </div>
      </div>
    </div>
  </main>

  <script>
    const tabs = document.querySelectorAll(".tab-button");
    const contents = document.querySelectorAll(".tab-content");

    tabs.forEach(btn => {
      btn.addEventListener("click", () => {
        const target = btn.getAttribute("data-tab");

        tabs.forEach(b => b.classList.remove("active"));
        btn.classList.add("active");

        contents.forEach(c => {
          c.classList.remove("active");
          if (c.id === target) c.classList.add("active");
        });
      });
    });

    const langEn = document.getElementById("lang-en");
    const langDe = document.getElementById("lang-de");
    const aboutText = document.getElementById("about-text");
    const getInvolvedText = document.getElementById("getinvolved-text");

    const translations = {
      en: {
        about: `<b>WHO WE ARE</b>
We are everyday people who believe in peace and safety for everyone, children above all.

We are independent, international, and unaffiliated with any government or political party. Our aim is peace and protection of human lives. The siege and the killing of children must end.`,
        getinvolved: `As a result of the Gaza war, children have been disproportionately impacted in the Gaza Strip, where 40% of the population is 14 or under. More than 700,000 children in Gaza were displaced. UN Secretary General Antonio Guterres warned that "Gaza is becoming a graveyard for children. Hundreds of girls and boys are reportedly being killed or injured every day." More than 50,000 children had been killed or injured in Gaza. In late September 2024, Oxfam and Action on Armed Violence reported that the number of children killed in Gaza over the past year was the highest recorded in a single year for any conflict worldwide in the last 20 years.

<b>HOW YOU CAN HELP</b>
- Contact your representatives and demand immediate ceasefire  
- Spread awareness about the humanitarian crisis  
- Advocate for children's rights and protection`
      },
      de: {
        about: `<b>WER WIR SIND</b>
Wir sind ganz normale Menschen, die an Frieden und Sicherheit für alle glauben, vor allem für Kinder.

Wir sind unabhängig, international und mit keiner Regierung oder politischen Partei verbunden. Unser Ziel ist Frieden und Schutz des menschlichen Lebens. Die Belagerung und das Töten von Kindern muss beendet werden.`,
        getinvolved: `Als Folge des Gaza-Krieges sind Kinder im Gazastreifen unverhältnismäßig stark betroffen, wo 40 % der Bevölkerung 14 Jahre oder jünger sind. Mehr als 700.000 Kinder in Gaza wurden vertrieben. UN-Generalsekretär Antonio Guterres warnte, dass "Gaza zu einem Friedhof für Kinder wird. Hunderte von Mädchen und Jungen werden Berichten zufolge jeden Tag getötet oder verletzt". Mehr als 50.000 Kinder wurden in Gaza getötet oder verletzt. Ende September 2024 berichteten Oxfam und Action on Armed Violence, dass…the number of children killed in Gaza im vergangenen Jahr die höchste für jeden Konflikt weltweit in den letzten 20 Jahren war.**
