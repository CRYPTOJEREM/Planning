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
    padding: 30px;
}

.container {
    max-width: 1600px;
    margin: auto;
    background: linear-gradient(135deg, #0D1229 0%, #1A1F3A 100%);
    border-radius: 24px;
    padding: 40px;
    box-shadow: 0 20px 60px rgba(0, 217, 255, 0.15);
}

.header {
    text-align: center;
    margin-bottom: 40px;
}

.week-badge {
    display: inline-block;
    padding: 8px 24px;
    border-radius: 20px;
    background: linear-gradient(135deg, #00D9FF, #7B2FF7);
    color: #0A0E27;
    font-family: 'Rajdhani';
    font-weight: 700;
}

h1 {
    margin-top: 10px;
    font-family: 'Montserrat';
    font-weight: 900;
    font-size: 40px;
    color: white;
    letter-spacing: 2px;
}

.subtitle {
    color: #00D9FF;
    margin-top: 6px;
}

/* === VRAI MODE HORIZONTAL === */
.schedule {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    gap: 18px;
}

/* === COLONNE JOUR === */
.day-card {
    background: rgba(26, 31, 58, 0.7);
    border-radius: 18px;
    padding: 20px;
    border: 1px solid rgba(123, 47, 247, 0.25);
    display: flex;
    flex-direction: column;
}

.day-name {
    text-align: center;
    font-family: 'Montserrat';
    font-weight: 700;
    font-size: 18px;
    color: white;
    margin-bottom: 16px;
    text-transform: uppercase;
}

.events {
    display: flex;
    flex-direction: column;
    gap: 14px;
}

.event {
    background: rgba(13, 18, 41, 0.9);
    border-radius: 14px;
    padding: 12px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.event-icon {
    width: 36px;
    height: 36px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
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
}

.event-host {
    font-size: 12px;
    color: #00D9FF;
}

.event-time {
    font-family: 'Rajdhani';
    font-weight: 700;
    color: #FFD700;
    font-size: 16px;
}

.tag {
    margin-left: 6px;
    padding: 3px 7px;
    font-size: 10px;
    font-weight: 700;
    border-radius: 6px;
    text-transform: uppercase;
}

.tag-debutant { color: #00D9FF; border: 1px solid rgba(0,217,255,.4); }
.tag-trading { color: #FFD700; border: 1px solid rgba(255,215,0,.4); }
.tag-web3 { color: #B47FF7; border: 1px solid rgba(123,47,247,.4); }

.footer {
    margin-top: 30px;
    text-align: center;
    color: #7B8BA8;
    font-size: 14px;
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
                    <div class="event-host">Cuillère</div>
                </div>
                <div class="event-time">18h</div>
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
                    <div class="event-host">Analyse</div>
                </div>
                <div class="event-time">14h</div>
            </div>
            <div class="event">
                <div class="event-icon icon-web3">🌐</div>
                <div class="event-content">
                    <div class="event-title">Live Web3 <span class="tag tag-web3">Web3</span></div>
                    <div class="event-host">2Ssouz</div>
                </div>
                <div class="event-time">16h</div>
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
                <div class="event-time">20h</div>
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
                <div class="event-time">18h</div>
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
                    <div class="event-host">Marché</div>
                </div>
                <div class="event-time">17h</div>
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
                    <div class="event-host">Analyse</div>
                </div>
                <div class="event-time">16h</div>
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
                <div class="event-time">20h</div>
            </div>
        </div>
    </div>

</div>

<div class="footer">📌 Rejoins-nous et ne rate aucun événement</div>

</div>
</body>
</html>
