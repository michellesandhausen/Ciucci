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
      about: `<b>WHO WE ARE</b><br><br>
We are everyday people who believe in peace and safety for everyone, children above all.<br><br>
We are independent, international, and unaffiliated with any government or political party. Our aim is peace and protection of human lives. The siege and the killing of children must end.`,
      getinvolved: `As a result of the Gaza war, children have been disproportionately impacted in the Gaza Strip, where 40% of the population is 14 or under. More than 700,000 children in Gaza were displaced. UN Secretary General Antonio Guterres warned that "Gaza is becoming a graveyard for children. Hundreds of girls and boys are reportedly being killed or injured every day." More than 50,000 children had been killed or injured in Gaza. In late September 2024, Oxfam and Action on Armed Violence reported that the number of children killed in Gaza over the past year was the highest recorded in a single year for any conflict worldwide in the last 20 years.<br><br>
<b>HOW YOU CAN HELP</b><br>
- Contact your representatives and demand immediate ceasefire<br>
- Spread awareness about the humanitarian crisis<br>
- Advocate for children's rights and protection<br><br>
<div class="share-links">
  Share this page:
  <a href="https://twitter.com/intent/tweet?text=Break+the+Siege,+Save+Children&url=https://yourwebsite.com" target="_blank">Twitter</a>
  <a href="https://www.instagram.com" target="_blank">Instagram</a>
  <a href="#" onclick="navigator.clipboard.writeText(window.location.href); alert('Link copied to clipboard!')">Copy Link</a>
</div>`
    },
    de: {
      about: `<b>WER WIR SIND</b><br><br>
Wir sind ganz normale Menschen, die an Frieden und Sicherheit für alle glauben, vor allem für Kinder.<br><br>
Wir sind unabhängig, international und mit keiner Regierung oder politischen Partei verbunden. Unser Ziel ist Frieden und Schutz des menschlichen Lebens. Die Belagerung und das Töten von Kindern muss beendet werden.`,
      getinvolved: `Als Folge des Gaza-Krieges sind Kinder im Gazastreifen unverhältnismäßig stark betroffen, wo 40 % der Bevölkerung 14 Jahre oder jünger sind. Mehr als 700.000 Kinder in Gaza wurden vertrieben. UN-Generalsekretär Antonio Guterres warnte, dass "Gaza zu einem Friedhof für Kinder wird. Hunderte von Mädchen und Jungen werden Berichten zufolge jeden Tag getötet oder verletzt". Mehr als 50.000 Kinder wurden in Gaza getötet oder verletzt. Ende September 2024 berichteten Oxfam und Action on Armed Violence, dass die Zahl der in Gaza getöteten Kinder im vergangenen Jahr die höchste für jeden Konflikt weltweit in den letzten 20 Jahren war.<br><br>
<b>WIE SIE HELFEN KÖNNEN</b><br>
- Kontaktieren Sie Ihre Vertreter und fordern Sie sofortigen Waffenstillstand<br>
- Verbreiten Sie Informationen über die humanitäre Krise<br>
- Setzen Sie sich für Kinderrechte und -schutz ein<br><br>
<div class="share-links">
  Diese Seite teilen:
  <a href="https://twitter.com/intent/tweet?text=Break+the+Siege,+Save+Children&url=https://yourwebsite.com" target="_blank">Twitter</a>
  <a href="https://www.instagram.com" target="_blank">Instagram</a>
  <a href="#" onclick="navigator.clipboard.writeText(window.location.href); alert('Link kopiert!')">Link kopieren</a>
</div>`
    }
  };

  function switchLanguage(lang) {
    aboutText.innerHTML = translations[lang].about;
    getInvolvedText.innerHTML = translations[lang].getinvolved;

    langEn.classList.toggle("active", lang === "en");
    langDe.classList.toggle("active", lang === "de");
  }

  langEn.addEventListener("click", () => switchLanguage("en"));
  langDe.addEventListener("click", () => switchLanguage("de"));
</script>
