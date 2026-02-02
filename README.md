<!DOCTYPE html>
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
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            width: 100%;
            max-width: 1400px;
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
            margin-bottom: 40px;
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
            letter-spacing: 2px;
            text-transform: uppercase;
            text-shadow: 0 0 30px rgba(0, 217, 255, 0.5);
        }

        .subtitle {
            color: #00D9FF;
            font-weight: 600;
            letter-spacing: 1px;
        }

        /* === HORIZONTAL LAYOUT === */
        .schedule {
            display: flex;
            gap: 20px;
            overflow-x: auto;
            padding-bottom: 10px;
        }

        .schedule::-webkit-scrollbar {
            height: 8px;
        }

        .schedule::-webkit-scrollbar-thumb {
            background: linear-gradient(90deg, #00D9FF, #7B2FF7);
            border-radius: 10px;
        }

        .day-card {
            min-width: 260px;
            background: rgba(26, 31, 58, 0.6);
            border-radius: 18px;
            padding: 20px;
            border: 1px solid rgba(123, 47, 247, 0.2);
            position: relative;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .day-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, #00D9FF, #7B2FF7);
        }

        .day-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 12px 30px rgba(0, 217, 255, 0.25);
            border-color: rgba(0, 217, 255, 0.4);
        }

        .day-name {
            font-family: 'Montserrat', sans-serif;
            font-size: 20px;
            font-weight: 700;
            color: #FFFFFF;
            text-align: center;
            margin-bottom: 16px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .events {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .event {
            background: rgba(13, 18, 41, 0.8);
            border-radius: 14px;
            padding: 12px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .event-icon {
            width: 38px;
            height: 38px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            flex-shrink: 0;
        }

        .icon-live { background: linear-gradient(135deg, #FF3366, #FF6B9D); }
        .icon-news { background: linear-gradient(135deg, #00D9FF, #0099CC); }
        .icon-video { background: linear-gradient(135deg, #FFD700, #FFA500); }
        .icon-web3 { background: linear-gradient(135deg, #7B2FF7, #B47FF7); }

        .event-content {
            flex: 1;
        }

        .event-title {
            color: #E0E6F0;
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 4px;
        }

        .event-host {
            font-size: 12px;
            color: #00D9FF;
        }

        .event-time {
            font-family: 'Rajdhani', sans-serif;
            font-weight: 700;
            color: #FFD700;
            font-size: 16px;
            margin-left: auto;
        }

        .tag {
            margin-left: 6px;
            padding: 3px 8px;
            font-size: 10px;
            font-weight: 700;
            border-radius: 6px;
            text-transform: uppercase;
        }

        .tag-debutant {
            color: #00D9FF;
            border: 1px solid rgba(0, 217, 255, 0.4);
        }

        .tag-trading {
            color: #FFD700;
            border: 1px solid rgba(255, 215, 0, 0.4);
        }

        .tag-web3 {
            color: #B47FF7;
            border: 1px solid rgba(123, 47, 247, 0.4);
        }

        .footer {
            margin-top: 30px;
            text-align: center;
            border-top: 1px solid rgba(123, 47, 247, 0.2);
            padding-top: 20px;
            color: #7B8BA8;
        }
    </style>
</head>

<body>
<div class="container">

    <div class="header">
        <div class="week-badge">SEMAINE 4 • JANVIER 2026</div>
        <h1>Planning</h1>
        <div class="subtitle">Programme de la semaine</div>
    </div>

    <div class="schedule">

        <div class="day-card">
            <div class="day-name">Lundi</div>
            <div class="events">
                <div class="event">
                    <div class="event-icon icon-live">🎥</div>
                    <div class="event-content">
                        <div class="event-title">Live Débutant <span class="tag tag-debutant">Débutant</span></div>
                        <div class="event-host">avec Cuillère</div>
                    </div>
                    <div class="event-time">18h00</div>
                </div>
            </div>
        </div>

        <div class="day-card">
            <div class="day-name">Mardi</div>
            <div class="events">
                <div class="event">
                    <div class="event-icon icon-news">📰</div>
                    <div class="event-content">
                        <div class="event-title">News Éco US</div>
                        <div class="event-host">Analyse & actu</div>
                    </div>
                    <div class="event-time">14h00</div>
                </div>
                <div class="event">
                    <div class="event-icon icon-web3">🌐</div>
                    <div class="event-content">
                        <div class="event-title">Live Web3 <span class="tag tag-web3">Web3</span></div>
                        <div class="event-host">avec 2Ssouz</div>
                    </div>
                    <div class="event-time">16h00</div>
                </div>
            </div>
        </div>

        <div class="day-card">
            <div class="day-name">Mercredi</div>
            <div class="events">
                <div class="event">
                    <div class="event-icon icon-live">📈</div>
                    <div class="event-content">
                        <div class="event-title">Live Trading <span class="tag tag-trading">Trading</span></div>
                        <div class="event-host">CryptoJerem</div>
                    </div>
                    <div class="event-time">20h00</div>
                </div>
            </div>
        </div>

        <div class="day-card">
            <div class="day-name">Jeudi</div>
            <div class="events">
                <div class="event">
                    <div class="event-icon icon-live">🎥</div>
                    <div class="event-content">
                        <div class="event-title">Live Débutant <span class="tag tag-debutant">Débutant</span></div>
                        <div class="event-host">Cuillère</div>
                    </div>
                    <div class="event-time">18h00</div>
                </div>
            </div>
        </div>

        <div class="day-card">
            <div class="day-name">Vendredi</div>
            <div class="events">
                <div class="event">
                    <div class="event-icon icon-news">📊</div>
                    <div class="event-content">
                        <div class="event-title">Récap Hebdo</div>
                        <div class="event-host">Bilan marché</div>
                    </div>
                    <div class="event-time">17h00</div>
                </div>
            </div>
        </div>

        <div class="day-card">
            <div class="day-name">Samedi</div>
            <div class="events">
                <div class="event">
                    <div class="event-icon icon-video">▶️</div>
                    <div class="event-content">
                        <div class="event-title">Vidéo YouTube</div>
                        <div class="event-host">Nouvelle analyse</div>
                    </div>
                    <div class="event-time">16h00</div>
                </div>
            </div>
        </div>

        <div class="day-card">
            <div class="day-name">Dimanche</div>
            <div class="events">
                <div class="event">
                    <div class="event-icon icon-live">📈</div>
                    <div class="event-content">
                        <div class="event-title">Live Trading <span class="tag tag-trading">Trading</span></div>
                        <div class="event-host">CryptoJerem</div>
                    </div>
                    <div class="event-time">20h00</div>
                </div>
            </div>
        </div>

    </div>

    <div class="footer">
        📌 Rejoins-nous et ne rate aucun événement !
    </div>

</div>
</body>
</html>
