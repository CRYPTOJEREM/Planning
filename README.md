<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Planning Horizontal</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700;900&family=Inter:wght@400;600;700&family=Rajdhani:wght@700&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html, body {
    width: 100%;
    height: 100%;
    overflow: hidden;
    background: linear-gradient(135deg, #0A0E27 0%, #1A1F3A 100%);
    font-family: 'Inter', sans-serif;
}

/* === ROTATION GLOBALE === */
.rotate-wrapper {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100vh;
    height: 100vw;
    transform: translate(-50%, -50%) rotate(-90deg);
    transform-origin: center;
}

/* === CONTENU === */
.container {
    width: 100%;
    height: 100%;
    padding: 40px;
    background: linear-gradient(135deg, #0D1229 0%, #1A1F3A 100%);
    border-radius: 24px;
    box-shadow: 0 20px 60px rgba(0, 217, 255, 0.2);
    overflow-y: auto;
}

.header {
    text-align: center;
    margin-bottom: 40px;
}

.week-badge {
    display: inline-block;
    background: linear-gradient(135deg, #00D9FF, #7B2FF7);
    padding: 8px 24px;
    border-radius: 20px;
    color: #0A0E27;
    font-family: 'Rajdhani';
    font-weight: 700;
}

h1 {
    margin-top: 12px;
    font-family: 'Montserrat';
    font-weight: 900;
    font-size: 42px;
    color: white;
}

.subtitle {
    color: #00D9FF;
}

/* === PROGRAMME (RESTE NORMAL MAIS PAGE COUCHÉE) === */
.schedule {
    display: flex;
    flex-direction: column;
    gap: 16px;
}

.day-card {
    background: rgba(26, 31, 58, 0.75);
    border-radius: 16px;
    padding: 20px;
    border-left: 5px solid #00D9FF;
}

.day-name {
    font-family: 'Montserrat';
    font-weight: 700;
    color: white;
    margin-bottom: 10px;
    text-transform: uppercase;
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
    font-weight: 600;
}

.event-host {
    color: #00D9FF;
    font-size: 13px;
}

.event-time {
    font-family: 'Rajdhani';
    color: #FFD700;
    font-weight: 700;
    font-size: 18px;
}
</style>
</head>

<body>

<div class="rotate-wrapper">
    <div class="container">

        <div class="header">
            <div class="week-badge">SEMAINE 4 • JANVIER 2026</div>
            <h1>Planning</h1>
            <div class="subtitle">Programme de la semaine</div>
        </div>

        <div class="schedule">

            <div class="day-card">
                <div class="day-name">Lundi</div>
                <div class="event">
                    <div class="event-icon icon-live">🎥</div>
                    <div class="event-content">
                        <div class="event-title">Live Débutant</div>
                        <div class="event-host">Cuillère</div>
                    </div>
                    <div class="event-time">18h</div>
                </div>
            </div>

            <div class="day-card">
                <div class="day-name">Mardi</div>
                <div class="event">
                    <div class="event-icon icon-news">📰</div>
                    <div class="event-content">
                        <div class="event-title">News Éco US</div>
                        <div class="event-host">Analyse</div>
                    </div>
                    <div class="event-time">14h</div>
                </div>
            </div>

            <div class="day-card">
                <div class="day-name">Mercredi</div>
                <div class="event">
                    <div class="event-icon icon-live">📈</div>
                    <div class="event-content">
                        <div class="event-title">Live Trading</div>
                        <div class="event-host">CryptoJerem</div>
                    </div>
                    <div class="event-time">20h</div>
                </div>
            </div>

        </div>

    </div>
</div>

</body>
</html>
