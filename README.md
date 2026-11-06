# francesco-mariapia
wedding francesco&amp;mariapia
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Francesco & Maria Pia | 30 Agosto 2027</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Alex+Brush&family=Cinzel:wght@400;600;700&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --bg-ivory: #FDFBF5;
            --dark-green: #3E4B40;
            --gold: #C09A55;
            --light-gold: #E5D6B6;
            --font-cursive: 'Alex Brush', cursive;
            --font-serif: 'Cinzel', serif;
            --font-sans: 'Montserrat', sans-serif;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        /* SFONDO FISSO CON LA GRAFICA SICILIANA */
        body {
            font-family: var(--font-sans);
            /* Richiama l'immagine "sfondo.jpg" che salverai nella cartella */
            background: url('sfondo.jpg') center top / cover fixed no-repeat;
            color: var(--dark-green);
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* COLONNA CENTRALE PIÙ STRETTA PER MOSTRARE I LATI DELLO SFONDO */
        .main-wrapper {
            max-width: 850px; /* Stretto per far vedere Teste di Moro e Maioliche ai lati */
            margin: 40px auto;
            background: rgba(253, 251, 245, 0.92); /* Avorio quasi opaco per leggere bene i testi */
            box-shadow: 0 0 40px rgba(0,0,0,0.3);
            position: relative;
            z-index: 2;
            border-radius: 20px;
            overflow: hidden;
            border: 2px solid var(--gold);
        }

        /* --- HEADER & HERO --- */
        .hero {
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 80px 20px 40px 20px;
            border-bottom: 2px solid var(--light-gold);
        }

        .top-bar {
            position: absolute;
            top: 20px;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 30px;
            z-index: 10;
        }

        .monogram {
            font-family: var(--font-serif);
            font-size: 22px;
            color: var(--dark-green);
            border: 2px solid var(--gold);
            border-radius: 50%;
            width: 60px;
            height: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
            background: var(--bg-ivory);
        }

        .music-control {
            display: flex;
            align-items: center;
            gap: 10px;
            font-family: var(--font-serif);
            font-size: 14px;
            color: var(--dark-green);
            cursor: pointer;
        }

        .music-btn {
            background: var(--dark-green);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            font-size: 18px;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: transform 0.3s;
        }

        .hero-content {
            z-index: 2;
            margin-top: 20px;
        }

        .hero h1 {
            font-family: var(--font-cursive);
            font-size: 6.5rem;
            color: var(--dark-green);
            line-height: 0.9;
            margin-bottom: 15px;
            font-weight: 400;
        }

        .hero h2 {
            font-family: var(--font-serif);
            font-size: 1.2rem;
            letter-spacing: 5px;
            color: var(--gold);
            margin-bottom: 25px;
            font-weight: 700;
        }

        .hero p.quote {
            max-width: 450px;
            margin: 0 auto 30px auto;
            font-style: italic;
            font-size: 1.1rem;
            color: var(--dark-green);
        }

        .btn-scroll {
            background: var(--dark-green);
            color: white;
            border: none;
            padding: 12px 30px;
            font-family: var(--font-sans);
            font-size: 0.85rem;
            font-weight: 500;
            letter-spacing: 2px;
            border-radius: 30px;
            cursor: pointer;
            text-transform: uppercase;
        }

        /* --- CONTENUTO (Countdown, Timeline, Info) --- */
        .section-container {
            padding: 60px 40px;
            text-align: center;
        }

        .section-title {
            font-family: var(--font-serif);
            color: var(--gold);
            letter-spacing: 3px;
            margin-bottom: 30px;
            font-size: 1.5rem;
        }

        .countdown {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .cd-box {
            background: white;
            border: 1px solid var(--light-gold);
            border-radius: 8px;
            padding: 20px 15px;
            width: 120px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .cd-icon { font-size: 24px; color: var(--gold); margin-bottom: 8px; }
        .cd-number { font-family: var(--font-serif); font-size: 2.5rem; color: var(--dark-green); line-height: 1; }
        .cd-label { font-size: 0.75rem; letter-spacing: 1px; font-weight: 600; color: #888; margin-top: 5px; }

        /* --- TIMELINE --- */
        .timeline-wrapper { margin-top: 60px; }

        .timeline-row {
            display: flex;
            align-items: center;
            gap: 30px;
            margin-bottom: 50px;
            text-align: left;
        }

        .tl-image {
            flex: 1;
            height: 220px;
            border-radius: 10px;
            background-color: #eee;
            background-position: center;
            background-size: cover;
            border: 2px solid var(--gold);
        }

        /* Immagine 1: LA TUA FOTO DELLA CHIESA */
        .img-chiesa {
            background-image: url('chiesa.jpg');
        }

        /* Immagine 2: RICEVIMENTO (Placeholder elegante) */
        .img-ricevimento {
            background-image: url('https://images.unsplash.com/photo-1519225421980-715cb0215aed?auto=format&fit=crop&w=800&q=80');
        }

        .tl-content {
            flex: 1.2;
            position: relative;
            padding-left: 30px;
            border-left: 2px solid var(--gold);
        }

        .tl-number {
            position: absolute;
            left: -20px;
            top: -5px;
            width: 38px;
            height: 38px;
            background: var(--gold);
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: var(--font-serif);
            font-size: 1.1rem;
            border: 3px solid var(--bg-ivory);
        }

        .tl-content h3 { font-family: var(--font-serif); font-size: 1.4rem; color: var(--dark-green); }
        .tl-content h4 { font-weight: 600; margin-bottom: 15px; color: #444; font-size: 1rem; }
        .tl-detail { display: flex; align-items: flex-start; gap: 10px; margin-bottom: 8px; font-size: 0.9rem; color: #555; }
        
        .btn-outline {
            display: inline-block;
            margin-top: 15px;
            padding: 10px 20px;
            border: 1px solid var(--dark-green);
            color: var(--dark-green);
            text-decoration: none;
            font-size: 0.8rem;
            font-weight: 600;
            border-radius: 4px;
        }

        /* --- 4 COLONNE INFO --- */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
            padding: 40px;
            background: rgba(229, 214, 182, 0.2);
            border-top: 1px solid var(--light-gold);
            border-bottom: 1px solid var(--light-gold);
        }

        .info-item { text-align: center; }
        .info-icon { font-size: 35px; margin-bottom: 15px; }
        .info-item h4 { font-family: var(--font-serif); color: var(--dark-green); margin-bottom: 10px; font-size: 1rem; }
        .info-item p { font-size: 0.85rem; color: #666; }

        /* --- RSVP --- */
        .rsvp-section {
            padding: 50px 40px;
            text-align: center;
        }

        .rsvp-section h2 { font-family: var(--font-cursive); font-size: 3.5rem; color: var(--dark-green); margin-bottom: 10px; }
        .rsvp-section p { color: #555; margin-bottom: 25px; }
        
        .btn-solid {
            background: var(--dark-green);
            color: white;
            border: none;
            padding: 14px 35px;
            font-family: var(--font-sans);
            font-size: 1rem;
            border-radius: 8px;
            cursor: pointer;
        }

        .footer {
            background: var(--dark-green);
            color: var(--light-gold);
            text-align: center;
            padding: 30px 20px;
        }
        .footer h3 { font-family: var(--font-cursive); font-size: 2.5rem; color: white; margin-bottom: 5px; font-weight: normal;}

        /* Responsive Mobile */
        @media (max-width: 768px) {
            .main-wrapper { margin: 10px; }
            .hero h1 { font-size: 4.5rem; }
            .timeline-row { flex-direction: column; }
            .tl-image { width: 100%; height: 200px; }
            .tl-content { border-left: none; padding-left: 0; border-top: 2px solid var(--gold); padding-top: 20px; text-align: center; }
            .tl-number { left: 50%; transform: translateX(-50%); top: -20px; }
            .tl-detail { justify-content: center; }
            .timeline-row:nth-child(2) .tl-content { border-right: none; padding-right: 0; }
            .info-grid { grid-template-columns: 1fr; }
        }

        /* MODALE RSVP */
        .modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.8); z-index: 2000; justify-content: center; align-items: center; }
        .modal-content { background: var(--bg-ivory); padding: 30px; border-radius: 10px; width: 90%; max-width: 450px; position: relative; border: 2px solid var(--gold); }
        .modal-content label { font-family: var(--font-sans); font-weight: 600; font-size: 0.85rem; }
        .modal-content input, .modal-content select { width: 100%; padding: 10px; margin: 5px 0 15px; border: 1px solid #ccc; border-radius: 4px; font-family: var(--font-sans); }
        .close-modal { position: absolute; top: 10px; right: 15px; font-size: 24px; cursor: pointer; }
    </style>
</head>
<body>

    <!-- MUSICA -->
    <audio id="bg-music" loop>
        <source src="cocciu_damuri.mp3" type="audio/mpeg">
    </audio>

    <div class="main-wrapper">
        
        <section class="hero">
            <div class="top-bar">
                <div class="monogram">F&M</div>
                <div class="music-control" onclick="toggleMusic()">
                    <span>Musica</span>
                    <button class="music-btn" id="music-btn">🎵</button>
                </div>
            </div>

            <div class="hero-content">
                <h1>Francesco<br>&<br>Maria Pia</h1>
                <h2>30 AGOSTO 2027</h2>
                <p class="quote">"L'amore non consiste nel guardarsi l'un l'altro, ma nel guardare insieme nella stessa direzione."</p>
                <button class="btn-scroll" onclick="document.getElementById('countdown').scrollIntoView({behavior: 'smooth'})">↓ Scopri il nostro giorno</button>
            </div>
        </section>

        <div class="section-container" id="countdown">
            <h3 class="section-title">MANCANO</h3>
            <div class="countdown">
                <div class="cd-box"><div class="cd-icon">📅</div><span class="cd-number" id="days">00</span><span class="cd-label">GIORNI</span></div>
                <div class="cd-box"><div class="cd-icon">🕒</div><span class="cd-number" id="hours">00</span><span class="cd-label">ORE</span></div>
                <div class="cd-box"><div class="cd-icon">⏳</div><span class="cd-number" id="minutes">00</span><span class="cd-label">MINUTI</span></div>
                <div class="cd-box"><div class="cd-icon">🤍</div><span class="cd-number" id="seconds">00</span><span class="cd-label">SECONDI</span></div>
            </div>

            <div class="timeline-wrapper">
                <div class="timeline-row">
                    <!-- QUI CARICA LA FOTO DELLA CHIESA (chiesa.jpg) -->
                    <div class="tl-image img-chiesa"></div>
                    <div class="tl-content">
                        <div class="tl-number">1</div>
                        <h3 style="text-transform: uppercase;">Cerimonia</h3>
                        <h4>Chiesa Madre di Santa Maria del Rosario</h4>
                        <div class="tl-detail">📅 30 AGOSTO 2027</div>
                        <div class="tl-detail">🕒 ORE 15:30</div>
                        <div class="tl-detail">📍 Salita Duomo, 57<br>92044 Palma di Montechiaro AG</div>
                        <a href="https://maps.app.goo.gl/kX7pZ4D8JqR5J6J7A" target="_blank" class="btn-outline">🗺 APRI GOOGLE MAPS</a>
                    </div>
                </div>

                <div class="timeline-row">
                    <div class="tl-content" style="border-left: none; border-right: 2px solid var(--gold); padding-left: 0; padding-right: 30px; text-align: right;">
                        <div class="tl-number" style="left: auto; right: -20px;">2</div>
                        <h3 style="text-transform: uppercase;">Ricevimento</h3>
                        <h4>Casale del Bosco</h4>
                        <div class="tl-detail" style="justify-content: flex-end;">📍 Casale Bosco, SS115, Km. 201<br>92044 Agrigento AG</div>
                        <a href="https://maps.app.goo.gl/vG3bZ7Y8KqW9L8M8A" target="_blank" class="btn-outline">🗺 APRI GOOGLE MAPS</a>
                    </div>
                    <div class="tl-image img-ricevimento"></div>
                </div>
            </div>
        </div>

        <div class="info-grid">
            <div class="info-item">
                <div class="info-icon">👒</div>
                <h4>DRESS CODE</h4>
                <p>Vestitevi comodi! Pensate ad una festa tra amici, immersi nei colori della Sicilia.</p>
            </div>
            <div class="info-item">
                <div class="info-icon">💌</div>
                <h4>IL NOSTRO REGALO</h4>
                <p>Il regalo più bello sarà condividere questo giorno insieme a voi. Gradito regalo in busta con gratta e vinci! 🍀</p>
            </div>
            <div class="info-item">
                <div class="info-icon">🗺️</div>
                <h4>COME ARRIVARE</h4>
                <p>Tutte le indicazioni dettagliate per raggiungere le location con facilità.</p>
            </div>
            <div class="info-item">
                <div class="info-icon">🍋</div>
                <h4>SICILIA</h4>
                <p>Un giorno speciale nella nostra terra, tra sole, mare e tradizione.</p>
            </div>
        </div>

        <div class="rsvp-section">
            <h2>Conferma la tua presenza</h2>
            <p>La tua presenza renderà questo giorno ancora più speciale.</p>
            <button class="btn-solid" onclick="openModal()">✉ CONFERMA ORA</button>
        </div>

        <div class="footer">
            <h3>Francesco ♥ Maria Pia</h3>
            <p style="font-family: var(--font-serif); letter-spacing: 2px; font-size: 0.9rem;">30 AGOSTO 2027</p>
        </div>
    </div>

    <!-- Modale RSVP -->
    <div id="rsvp-modal" class="modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal()">&times;</span>
            <h2 style="font-family: var(--font-serif); color: var(--dark-green); margin-bottom: 20px; text-align: center;">Conferma</h2>
            
            <label>Nome e Cognome</label>
            <input type="text" id="guest-name" required>

            <label>Presenza</label>
            <select id="guest-attendance">
                <option value="Parteciperò">Parteciperò con gioia</option>
                <option value="Non potrò esserci">Purtroppo non potrò esserci</option>
            </select>

            <div style="display: flex; gap: 10px;">
                <div style="flex: 1;"><label>Adulti</label><input type="number" id="guest-adults" value="1" min="0"></div>
                <div style="flex: 1;"><label>Bambini</label><input type="number" id="guest-kids" value="0" min="0"></div>
            </div>

            <label>Intolleranze (Opzionale)</label>
            <input type="text" id="guest-allergies">

            <button class="btn-solid" style="width: 100%; margin-top: 10px;" onclick="sendWhatsApp()">Invia tramite WhatsApp ✓</button>
        </div>
    </div>

    <script>
        const audio = document.getElementById('bg-music');
        const musicBtn = document.getElementById('music-btn');
        let isPlaying = false;

        function toggleMusic() {
            if (isPlaying) { audio.pause(); musicBtn.textContent = '🔇'; }
            else { audio.play(); musicBtn.textContent = '🎵'; }
            isPlaying = !isPlaying;
        }

        const countDownDate = new Date("Aug 30, 2027 15:30:00").getTime();
        setInterval(function() {
            const now = new Date().getTime();
            const distance = countDownDate - now;
            document.getElementById("days").innerText = Math.floor(distance / (1000 * 60 * 60 * 24)).toString().padStart(2, '0');
            document.getElementById("hours").innerText = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)).toString().padStart(2, '0');
            document.getElementById("minutes").innerText = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60)).toString().padStart(2, '0');
            document.getElementById("seconds").innerText = Math.floor((distance % (1000 * 60)) / 1000).toString().padStart(2, '0');
        }, 1000);

        const modal = document.getElementById('rsvp-modal');
        function openModal() { modal.style.display = 'flex'; }
        function closeModal() { modal.style.display = 'none'; }
        window.onclick = function(event) { if (event.target == modal) { modal.style.display = "none"; } }

        function sendWhatsApp() {
            const name = document.getElementById('guest-name').value;
            const attendance = document.getElementById('guest-attendance').value;
            const adults = document.getElementById('guest-adults').value;
            const kids = document.getElementById('guest-kids').value;
            const allergies = document.getElementById('guest-allergies').value || "Nessuna";
            if(!name) { alert("Inserisci il tuo nome per favore!"); return; }
            let waText = `Ciao Francesco e Maria Pia! 🍋\nSono *${name}*.\n\n*Conferma:* ${attendance}\n*Adulti:* ${adults}\n*Bambini:* ${kids}\n*Intolleranze:* ${allergies}`;
            window.open(`https://wa.me/?text=${encodeURIComponent(waText)}`, '_blank');
            closeModal();
        }
    </script>
</body>
</html>
