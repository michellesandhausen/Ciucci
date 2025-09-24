<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Break the Siege, Save Lives</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #20b2aa, #40e0d0);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background: rgba(255, 255, 255, 0.95);
            min-height: 100vh;
            box-shadow: 0 0 50px rgba(0, 0, 0, 0.1);
        }

        header {
            text-align: center;
            padding: 40px 0;
            border-bottom: 3px solid #ff6b35;
        }

        h1 {
            font-size: 2.8em;
            color: #20b2aa;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        .language-selector {
            margin: 20px 0;
            text-align: center;
        }

        .language-btn {
            background: #ff6b35;
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 0 10px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 107, 53, 0.3);
        }

        .language-btn:hover {
            background: #e5592f;
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(255, 107, 53, 0.4);
        }

        .language-btn.active {
            background: #20b2aa;
            box-shadow: 0 4px 15px rgba(32, 178, 170, 0.3);
        }

        .tab-container {
            margin: 40px 0;
        }

        .tab-buttons {
            display: flex;
            justify-content: center;
            margin-bottom: 30px;
            border-bottom: 3px solid #20b2aa;
        }

        .tab-btn {
            background: none;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            font-weight: bold;
            color: #666;
            cursor: pointer;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
        }

        .tab-btn:hover {
            color: #20b2aa;
            background: rgba(32, 178, 170, 0.1);
        }

        .tab-btn.active {
            color: #20b2aa;
            border-bottom-color: #ff6b35;
            background: rgba(32, 178, 170, 0.1);
        }

        .tab-content {
            display: none;
            animation: fadeIn 0.5s ease-in;
        }

        .tab-content.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .content-section {
            display: flex;
            align-items: flex-start;
            gap: 30px;
            margin-bottom: 40px;
        }

        .content-image {
            flex: 0 0 300px;
            max-width: 300px;
        }

        .content-image img {
            width: 100%;
            height: auto;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease;
        }

        .content-image img:hover {
            transform: scale(1.05);
        }

        .content-text {
            flex: 1;
        }

        .content-text h2 {
            color: #20b2aa;
            margin-bottom: 20px;
            font-size: 1.8em;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1);
        }

        .content-text p {
            text-align: justify;
            margin-bottom: 20px;
            font-size: 1.1em;
            line-height: 1.8;
        }

        .content-text ul {
            text-align: justify;
            margin-left: 20px;
            margin-bottom: 20px;
        }

        .content-text li {
            margin-bottom: 10px;
            font-size: 1.1em;
            line-height: 1.6;
        }

        .share-section {
            text-align: center;
            margin-top: 40px;
            padding: 30px;
            background: linear-gradient(135deg, rgba(32, 178, 170, 0.1), rgba(255, 107, 53, 0.1));
            border-radius: 15px;
            border: 2px solid #20b2aa;
        }

        .share-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }

        .share-btn {
            display: inline-flex;
            align-items: center;
            padding: 12px 24px;
            border-radius: 25px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .share-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }

        .twitter { background: #1da1f2; }
        .instagram { background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888); }
        .facebook { background: #4267b2; }

        /* Tablet Responsiveness */
        @media (max-width: 1024px) {
            .container {
                padding: 15px;
            }

            .content-section {
                gap: 20px;
            }

            .content-image {
                flex: 0 0 250px;
                max-width: 250px;
            }
        }

        /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .container {
                padding: 10px;
                margin: 0;
            }

            header {
                padding: 20px 0;
            }

            h1 {
                font-size: 1.8em;
                line-height: 1.2;
                margin-bottom: 15px;
            }

            .language-selector {
                margin: 15px 0;
            }

            .language-btn {
                padding: 8px 15px;
                margin: 0 5px;
                font-size: 0.9em;
            }

            .tab-buttons {
                flex-direction: row;
                justify-content: space-around;
                margin-bottom: 20px;
            }

            .tab-btn {
                padding: 10px 15px;
                font-size: 1em;
                flex: 1;
                margin: 0 5px;
            }

            .content-section {
                flex-direction: column;
                gap: 15px;
                margin-bottom: 20px;
            }

            .content-image {
                flex: none;
                max-width: 100%;
                width: 100%;
                order: 0;
                align-self: center;
            }

            .content-image img {
                max-width: 300px;
                width: 100%;
                height: auto;
                margin: 0 auto;
                display: block;
            }

            .content-text {
                text-align: left;
                width: 100%;
            }

            .content-text h2 {
                font-size: 1.4em;
                text-align: center;
                margin-bottom: 15px;
            }

            .content-text p {
                font-size: 0.95em;
                line-height: 1.6;
                margin-bottom: 15px;
                text-align: justify;
            }

            .content-text ul {
                margin-left: 15px;
                margin-bottom: 15px;
            }

            .content-text li {
                font-size: 0.95em;
                line-height: 1.5;
                margin-bottom: 8px;
                text-align: justify;
            }

            .share-section {
                margin-top: 20px;
                padding: 20px 15px;
            }

            .share-section h3 {
                font-size: 1.2em;
                margin-bottom: 15px;
            }

            .share-buttons {
                flex-direction: column;
                align-items: stretch;
                gap: 10px;
                max-width: 280px;
                margin: 0 auto;
            }

            .share-btn {
                justify-content: center;
                padding: 12px 20px;
                font-size: 0.9em;
                width: 100%;
                text-align: center;
            }
        }

        /* Small Mobile Phones */
        @media (max-width: 480px) {
            .container {
                padding: 8px;
            }

            h1 {
                font-size: 1.5em;
            }

            .language-btn {
                padding: 6px 12px;
                font-size: 0.8em;
                margin: 0 3px;
            }

            .tab-btn {
                padding: 8px 10px;
                font-size: 0.9em;
            }

            .content-text h2 {
                font-size: 1.2em;
            }

            .content-text p, .content-text li {
                font-size: 0.9em;
                line-height: 1.5;
            }

            .share-section {
                padding: 15px 10px;
            }

            .share-buttons {
                gap: 8px;
            }

            .share-btn {
                padding: 10px 15px;
                font-size: 0.85em;
            }
        }

        /* Very Small Screens */
        @media (max-width: 360px) {
            h1 {
                font-size: 1.3em;
            }

            .content-text p, .content-text li {
                font-size: 0.85em;
            }

            .language-btn {
                padding: 5px 10px;
                font-size: 0.75em;
            }

            .tab-btn {
                padding: 6px 8px;
                font-size: 0.8em;
            }
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 id="main-title">Break the Siege, Save Lives</h1>
            <div class="language-selector">
                <button class="language-btn active" onclick="switchLanguage('en')">ENGLISH</button>
                <button class="language-btn" onclick="switchLanguage('de')">DEUTSCH</button>
            </div>
        </header>

        <div class="tab-container">
            <div class="tab-buttons">
                <button class="tab-btn active" onclick="showTab('about')" id="about-tab">ABOUT</button>
                <button class="tab-btn" onclick="showTab('involved')" id="involved-tab">GET INVOLVED</button>
            </div>

            <div id="about-content" class="tab-content active">
                <div class="content-section">
                    <div class="content-image">
                        <img src="about-image.jpg" alt="About Us Image">
                    </div>
                    <div class="content-text">
                        <h2 id="about-title">WHO WE ARE</h2>
                        <p id="about-text">We are everyday people who believe in peace and safety for everyone, children above all. We are independent, international, and unaffiliated with any government or political party. Our aim is peace and protection of human lives. The siege and childslaughter must end.</p>
                    </div>
                </div>
            </div>

            <div id="involved-content" class="tab-content">
                <div class="content-section">
                    <div class="content-image">
                        <img src="getinvolved-image.jpg" alt="Get Involved Image">
                    </div>
                    <div class="content-text">
                        <p id="involved-description">As a result of the Gaza war, children have been disproportionately impacted in the Gaza Strip, where 40% of the population is 14 or under. More than 700,000 children in Gaza were displaced. UN Secretary General Antonio Guterres warned that 'Gaza is becoming a graveyard for children. Hundreds of girls and boys are reportedly being killed or injured every day'. More than 50,000 children had been killed or injured in Gaza. In late September 2024, Oxfam and Action on Armed Violence reported that the number of children killed in Gaza over the past year was the highest recorded in a single year for any conflict worldwide in the last 20 years.</p>
                        
                        <h2 id="help-title">HOW YOU CAN HELP</h2>
                        <ul id="help-list">
                            <li>Contact your representatives and demand immediate ceasefire</li>
                            <li>Spread awareness about the humanitarian crisis</li>
                            <li>Advocate for children's rights and protection</li>
                        </ul>
                    </div>
                </div>
                
                <div class="share-section">
                    <h3 id="share-title">Share Our Message</h3>
                    <div class="share-buttons">
                        <a href="#" class="share-btn twitter" onclick="shareOnTwitter()">Share on Twitter</a>
                        <a href="#" class="share-btn instagram" onclick="shareOnInstagram()">Share on Instagram</a>
                        <a href="#" class="share-btn facebook" onclick="shareOnFacebook()">Share on Facebook</a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const translations = {
            en: {
                'main-title': 'Break the Siege, Save Lives',
                'about-tab': 'ABOUT',
                'involved-tab': 'GET INVOLVED',
                'about-title': 'WHO WE ARE',
                'about-text': 'We are everyday people who believe in peace and safety for everyone, children above all. We are independent, international, and unaffiliated with any government or political party. Our aim is peace and protection of human lives. The siege and childslaughter must end.',
                'involved-description': 'As a result of the Gaza war, children have been disproportionately impacted in the Gaza Strip, where 40% of the population is 14 or under. More than 700,000 children in Gaza were displaced. UN Secretary General Antonio Guterres warned that \'Gaza is becoming a graveyard for children. Hundreds of girls and boys are reportedly being killed or injured every day\'. More than 50,000 children had been killed or injured in Gaza. In late September 2024, Oxfam and Action on Armed Violence reported that the number of children killed in Gaza over the past year was the highest recorded in a single year for any conflict worldwide in the last 20 years.',
                'help-title': 'HOW YOU CAN HELP',
                'help-list': '<li>Contact your representatives and demand immediate ceasefire</li><li>Spread awareness about the humanitarian crisis</li><li>Advocate for children\'s rights and protection</li>',
                'share-title': 'Share Our Message'
            },
            de: {
                'main-title': 'Durchbrecht die Belagerung, Rettet Leben',
                'about-tab': 'ÜBER UNS',
                'involved-tab': 'MITMACHEN',
                'about-title': 'WER WIR SIND',
                'about-text': 'Wir sind gewöhnliche Menschen, die an Frieden und Sicherheit für alle glauben, vor allem für Kinder. Wir sind unabhängig, international und keiner Regierung oder politischen Partei angeschlossen. Unser Ziel ist Frieden und der Schutz menschlichen Lebens. Die Belagerung und das Kindermorden müssen beendet werden.',
                'involved-description': 'Infolge des Gaza-Krieges wurden Kinder im Gazastreifen unverhältnismäßig stark beeinträchtigt, wo 40% der Bevölkerung 14 Jahre oder jünger sind. Mehr als 700.000 Kinder in Gaza wurden vertrieben. UN-Generalsekretär Antonio Guterres warnte, dass „Gaza zu einem Friedhof für Kinder wird. Berichten zufolge werden täglich Hunderte von Mädchen und Jungen getötet oder verletzt". Mehr als 50.000 Kinder wurden in Gaza getötet oder verletzt. Ende September 2024 berichteten Oxfam und Action on Armed Violence, dass die Zahl der in Gaza getöteten Kinder im vergangenen Jahr die höchste war, die jemals in einem einzigen Jahr für einen Konflikt weltweit in den letzten 20 Jahren verzeichnet wurde.',
                'help-title': 'WIE SIE HELFEN KÖNNEN',
                'help-list': '<li>Kontaktieren Sie Ihre Vertreter und fordern Sie einen sofortigen Waffenstillstand</li><li>Schaffen Sie Bewusstsein für die humanitäre Krise</li><li>Setzen Sie sich für die Rechte und den Schutz von Kindern ein</li>',
                'share-title': 'Teilen Sie unsere Botschaft'
            }
        };

        let currentLanguage = 'en';

        function switchLanguage(lang) {
            currentLanguage = lang;
            
            // Update active language button
            document.querySelectorAll('.language-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');

            // Update all translated elements
            Object.keys(translations[lang]).forEach(id => {
                const element = document.getElementById(id);
                if (element) {
                    if (id === 'help-list') {
                        element.innerHTML = translations[lang][id];
                    } else {
                        element.textContent = translations[lang][id];
                    }
                }
            });

            // Update document language attribute
            document.documentElement.lang = lang;
        }

        function showTab(tabName) {
            // Hide all tabs
            document.querySelectorAll('.tab-content').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Remove active class from all tab buttons
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            
            // Show selected tab
            document.getElementById(tabName + '-content').classList.add('active');
            
            // Add active class to clicked button
            event.target.classList.add('active');
        }

        function shareOnTwitter() {
            const text = currentLanguage === 'en' 
                ? 'Break the Siege, Save Lives - Join us in advocating for peace and children\'s rights'
                : 'Durchbrecht die Belagerung, Rettet Leben - Schließen Sie sich uns an, um für Frieden und Kinderrechte einzutreten';
            const url = window.location.href;
            window.open(`https://twitter.com/intent/tweet?text=${encodeURIComponent(text)}&url=${encodeURIComponent(url)}`, '_blank');
        }

        function shareOnFacebook() {
            const url = window.location.href;
            window.open(`https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(url)}`, '_blank');
        }

        function shareOnInstagram() {
            // Instagram doesn't support direct link sharing, so we'll copy to clipboard
            const text = currentLanguage === 'en' 
                ? 'Break the Siege, Save Lives - Join us in advocating for peace and children\'s rights. Visit: ' + window.location.href
                : 'Durchbrecht die Belagerung, Rettet Leben - Schließen Sie sich uns an, um für Frieden und Kinderrechte einzutreten. Besuchen Sie: ' + window.location.href;
            
            navigator.clipboard.writeText(text).then(() => {
                alert(currentLanguage === 'en' 
                    ? 'Link copied to clipboard! You can now paste it in your Instagram story or bio.'
                    : 'Link in die Zwischenablage kopiert! Sie können ihn jetzt in Ihrer Instagram-Story oder Bio einfügen.');
            });
        }
    </script>
</body>
</html>
