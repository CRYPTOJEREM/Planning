<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Planning Hebdomadaire - Groupe Crypto</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700;900&family=Inter:wght@400;600;700&family=Rajdhani:wght@700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0A0E27 0%, #1A1F3A 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            width: 100%;
            max-width: 1080px;
            background: linear-gradient(135deg, #0D1229 0%, #1A1F3A 100%);
            border-radius: 24px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(0, 217, 255, 0.15),
                        0 0 0 1px rgba(123, 47, 247, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #00D9FF 0%, #7B2FF7 50%, #FFD700 100%);
        }
        
        .header {
            text-align: center;
            margin-bottom: 35px;
            position: relative;
        }
        
        .week-badge {
            display: inline-block;
            background: linear-gradient(135deg, #00D9FF, #7B2FF7);
            color: #0A0E27;
            padding: 8px 24px;
            border-radius: 20px;
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 16px;
            margin-bottom: 15px;
            letter-spacing: 1px;
        }
        
        h1 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 900;
            font-size: 42px;
            color: #FFFFFF;
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: 0 0 30px rgba(0, 217, 255, 0.5);
        }
        
        .subtitle {
            font-family: 'Inter', sans-serif;
            font-size: 16px;
            color: #00D9FF;
            font-weight: 600;
            letter-spacing: 1px;
        }
        
        .schedule {
            display: grid;
            gap: 16px;
        }
        
        .day-card {
            background: rgba(26, 31, 58, 0.6);
            border-radius: 16px;
            padding: 20px 24px;
            border: 1px solid rgba(123, 47, 247, 0.2);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .day-card::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 4px;
            background: linear-gradient(180deg, #00D9FF, #7B2FF7);
        }
        
        .day-card:hover {
            transform: translateX(5px);
            border-color: rgba(0, 217, 255, 0.4);
            box-shadow: 0 8px 24px rgba(0, 217, 255, 0.2);
        }
        
        .day-header {
            display: flex;
            align-items: center;
            margin-bottom: 12px;
        }
        
        .day-name {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            font-size: 20px;
            color: #FFFFFF;
            text-transform: uppercase;
            letter-spacing: 1px;
            min-width: 120px;
        }
        
        .events {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-left: 15px;
        }
        
        .event {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        
        .event-icon {
            width: 40px;
            height: 40px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            flex-shrink: 0;
        }
        
        .icon-live {
            background: linear-gradient(135deg, #FF3366, #FF6B9D);
            box-shadow: 0 4px 12px rgba(255, 51, 102, 0.3);
        }
        
        .icon-news {
            background: linear-gradient(135deg, #00D9FF, #0099CC);
            box-shadow: 0 4px 12px rgba(0, 217, 255, 0.3);
        }
        
        .icon-video {
            background: linear-gradient(135deg, #FFD700, #FFA500);
            box-shadow: 0 4px 12px rgba(255, 215, 0, 0.3);
        }
        
        .icon-web3 {
            background: linear-gradient(135deg, #7B2FF7, #B47FF7);
            box-shadow: 0 4px 12px rgba(123, 47, 247, 0.3);
        }
        
        .event-content {
            flex: 1;
        }
        
        .event-title {
            font-family: 'Inter', sans-serif;
            font-weight: 600;
            font-size: 15px;
            color: #E0E6F0;
            margin-bottom: 3px;
        }
        
        .event-host {
            font-size: 13px;
            color: #00D9FF;
            font-weight: 500;
        }
        
        .event-time {
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            font-size: 18px;
            color: #FFD700;
            min-width: 60px;
            text-align: right;
        }
        
        .tag {
            display: inline-block;
            padding: 4px 10px;
            border-radius: 6px;
            font-size: 11px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-left: 8px;
        }
        
        .tag-debutant {
            background: rgba(0, 217, 255, 0.15);
            color: #00D9FF;
            border: 1px solid rgba(0, 217, 255, 0.3);
        }
        
        .tag-trading {
            background: rgba(255, 215, 0, 0.15);
            color: #FFD700;
            border: 1px solid rgba(255, 215, 0, 0.3);
        }
        
        .tag-web3 {
            background: rgba(123, 47, 247, 0.15);
            color: #B47FF7;
            border: 1px solid rgba(123, 47, 247, 0.3);
        }
        
        .footer {
            margin-top: 30px;
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(123, 47, 247, 0.2);
        }
        
        .footer-text {
            color: #7B8BA8;
            font-size: 14px;
            font-weight: 500;
        }
        
        .glow-effect {
            position: absolute;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(0, 217, 255, 0.1), transparent);
            pointer-events: none;
            top: -150px;
            right: -150px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="glow-effect"></div>
        
        <div class="header">
            <div class="week-badge">SEMAINE 4 • JANVIER 2026</div>
            <h1>Planning</h1>
            <div class="subtitle">Programme de la semaine</div>
        </div>
        
        <div class="schedule">
            <div class="day-card">
                <div class="day-header">
                    <div class="day-name">Lundi</div>
                </div>
                <div class="events">
                    <div class="event">
                        <div class="event-icon icon-live">🎥</div>
                        <div class="event-content">
                            <div class="event-title">Live Débutant<span class="tag tag-debutant">Débutant</span></div>
                            <div class="event-host">avec Cuillère</div>
                        </div>
                        <div class="event-time">18h00</div>
                    </div>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-header">
                    <div class="day-name">Mardi</div>
                </div>
                <div class="events">
                    <div class="event">
                        <div class="event-icon icon-news">📰</div>
                        <div class="event-content">
                            <div class="event-title">News Économique US</div>
                            <div class="event-host">Actualités & Analyse</div>
                        </div>
                        <div class="event-time">14h00</div>
                    </div>
                    <div class="event">
                        <div class="event-icon icon-web3">🌐</div>
                        <div class="event-content">
                            <div class="event-title">Live Web3<span class="tag tag-web3">Web3</span></div>
                            <div class="event-host">avec 2Ssouz</div>
                        </div>
                        <div class="event-time">16h00</div>
                    </div>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-header">
                    <div class="day-name">Mercredi</div>
                </div>
                <div class="events">
                    <div class="event">
                        <div class="event-icon icon-live">📈</div>
                        <div class="event-content">
                            <div class="event-title">Live Trading<span class="tag tag-trading">Trading</span></div>
                            <div class="event-host">avec CryptoJerem</div>
                        </div>
                        <div class="event-time">20h00</div>
                    </div>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-header">
                    <div class="day-name">Jeudi</div>
                </div>
                <div class="events">
                    <div class="event">
                        <div class="event-icon icon-live">🎥</div>
                        <div class="event-content">
                            <div class="event-title">Live Débutant<span class="tag tag-debutant">Débutant</span></div>
                            <div class="event-host">avec Cuillère</div>
                        </div>
                        <div class="event-time">18h00</div>
                    </div>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-header">
                    <div class="day-name">Vendredi</div>
                </div>
                <div class="events">
                    <div class="event">
                        <div class="event-icon icon-news">📊</div>
                        <div class="event-content">
                            <div class="event-title">Récap Hebdo Éco</div>
                            <div class="event-host">Bilan de la semaine</div>
                        </div>
                        <div class="event-time">17h00</div>
                    </div>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-header">
                    <div class="day-name">Samedi</div>
                </div>
                <div class="events">
                    <div class="event">
                        <div class="event-icon icon-video">▶️</div>
                        <div class="event-content">
                            <div class="event-title">Sortie Vidéo YouTube</div>
                            <div class="event-host">Nouvelle analyse disponible</div>
                        </div>
                        <div class="event-time">16h00</div>
                    </div>
                </div>
            </div>
            
            <div class="day-card">
                <div class="day-header">
                    <div class="day-name">Dimanche</div>
                </div>
                <div class="events">
                    <div class="event">
                        <div class="event-icon icon-live">📈</div>
                        <div class="event-content">
                            <div class="event-title">Live Trading<span class="tag tag-trading">Trading</span></div>
                            <div class="event-host">avec CryptoJerem</div>
                        </div>
                        <div class="event-time">20h00</div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <div class="footer-text">📌 Rejoins-nous et ne rate aucun événement !</div>
        </div>
    </div>
</body>
</html>
