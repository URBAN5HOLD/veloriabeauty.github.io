<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Collection Privée</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root { --bg: #000; }
        html, body { width: 100%; margin: 0; padding: 0; overflow-x: hidden; background-color: var(--bg); scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        * { box-sizing: border-box; outline: none; -webkit-tap-highlight-color: transparent; }

        .logo-fixed { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 8px; color: #fff; }

        .scroll-trigger { position: fixed; bottom: 15%; right: 25px; width: 50px; height: 50px; z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; }
        .arrow-icon { width: 20px; height: 20px; border-right: 2.5px solid var(--current-color); border-bottom: 2.5px solid var(--current-color); transform: rotate(45deg); animation: bounce 2s infinite; }
        @keyframes bounce { 0%, 100% { transform: rotate(45deg) translate(0,0); } 50% { transform: rotate(45deg) translate(5px,5px); } }

        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; scroll-snap-stop: always; position: relative; padding-bottom: 60px; }
        .v-header-sauvage { width: 85%; margin: 0 auto; line-height: 0; }
        .v-header { width: 100%; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }

        .bottle-center { text-align: center; padding: 30px 0; }
        .img-bottle { width: 40%; max-width: 150px; margin: 0 auto; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; letter-spacing: 6px; margin: 10px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color); letter-spacing: 4px; text-transform: uppercase; }

        .row { display: flex; align-items: flex-start; width: 100%; padding: 25px 8%; gap: 30px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 45%; }
        .img-box img { width: 100%; border-radius: 2px; }
        
        .txt-box { width: 55%; color: #fff; text-align: left; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1rem; margin-bottom: 12px; color: var(--color); letter-spacing: 1px; text-transform: uppercase; }
        .txt-box p { font-size: 0.75rem; line-height: 1.6; color: #ccc; font-weight: 300; margin-bottom: 10px; }
        .txt-box ul { padding: 0; list-style: none; font-size: 0.75rem; color: #aaa; }
        .txt-box li { margin-bottom: 8px; line-height: 1.4; }
        .highlight { color: #fff; font-weight: 600; }

        .purchase-area { max-width: 1000px; margin: 30px auto; display: flex; gap: 30px; padding: 30px; border-top: 1px solid rgba(255,255,255,0.05); width: 90%; }
        .mini-thumb { width: 80px; height: 80px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1); }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.1); text-align: center; color: #fff; font-size: 0.8rem; }
        .active-size { border-color: var(--color); color: var(--color); background: rgba(255,255,255,0.02); }

        input { width: 100%; padding: 15px 5px; margin-bottom: 15px; background: transparent; color: #fff; border: none; border-bottom: 1px solid rgba(255,255,255,0.15); font-family: 'Montserrat'; font-size: 0.9rem; }
        .order-btn { width: 100%; padding: 20px; background: #fff; color: #000; font-family: 'Montserrat'; font-weight: 800; font-size: 1rem; cursor: pointer; letter-spacing: 2px; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 20px 8%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; }
            .v-header-sauvage { width: 100%; }
        }

        .sauv-t { --color: #4A90E2; }
        .stron-t { --color: #CD7F32; }
        .libre-t { --color: #D4AF37; }
        .gg-t { --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="v-header-sauvage"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE</h1>
            <div class="perfume-sub">ELIXIR / EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box">
                <h3>La Fragrance</h3>
                <p>Sauvage Elixir est un parfum d'une concentration hors normes. Une essence nocturne capturant la puissance brute du désert, où la fraîcheur est poussée à l'extrême.</p>
                <p><span class="highlight">Pour :</span> Lui | <span class="highlight">Il est :</span> Puissant et Mystérieux<br><span class="highlight">Occasion :</span> Soirée & Hiver</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/sauvage-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Cannelle & Cardamome (Impact immédiat)<br>
                <span class="highlight">Notes de Cœur :</span> Essence de Lavande exclusive Dior<br>
                <span class="highlight">Notes de Fond :</span> Réglisse & Bois de Santal (Sillage intense)</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">DECANT 10ML</h4><p style="color:#555; font-size:10px">EXTRAIT DE PARFUM</p></div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section stron-t" id="sec2">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">ABSOLUTELY / PARFUM INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box">
                <h3>La Fragrance</h3>
                <p>Stronger With You Absolutely est le parfum le plus intense de la collection. Une signature masculine raffinée avec un nouvel accord rhum addictif.</p>
                <p><span class="highlight">Pour :</span> Lui | <span class="highlight">Il est :</span> Captivant et Sensuel<br><span class="highlight">Occasion :</span> Rendez-vous galant</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/stronger-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Accord Rhum & Bergamote<br>
                <span class="highlight">Notes de Cœur :</span> Lavande & Davana<br>
                <span class="highlight">Notes de Fond :</span> Vanille de Madagascar & Bois de Cèdre</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">INTENSE 10ML</h4><p style="color:#555; font-size:10px">ABSOLUTE ELEGANCE</p></div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section libre-t" id="sec3">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box">
                <h3>La Fragrance</h3>
                <p>Libre Intense est le parfum d'une femme libre qui vit selon ses propres règles. Une dualité florale entre la lavande de France et la fleur d'oranger du Maroc.</p>
                <p><span class="highlight">Pour :</span> Elle | <span class="highlight">Elle est :</span> Audacieuse et Royale<br><span class="highlight">Occasion :</span> Luxe quotidien</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/libre-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <p><span class="highlight">Notes de Tête :</span> Lavande, Mandarine & Bergamote<br>
                <span class="highlight">Notes de Cœur :</span> Fleur d'Oranger & Jasmin Sambac<br>
                <span class="highlight">Notes de Fond :</span> Vanille de Madagascar & Ambre Gris</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">LIBRE 10ML</h4><p style="color:#555; font-size:10px">COUTURE FLOWERS</p></div>
                    <img src="assets/libre-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <section class="product-section gg-t" id="sec4">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box">
                <h3>La fragrance</h3>
                <p>La douceur et le pouvoir de séduction du jasmin renforcent encore l’éclat de Good Girl. Le côté mystérieux est révélé grâce au cacao riche et à l’enivrante fève tonka.</p>
                <p><span class="highlight">Pour :</span> Elle | <span class="highlight">Elle est :</span> Séductrice et Puissante<br><span class="highlight">Occasion :</span> Le jour et la nuit</p>
            </div>
        </div>
        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
            <div class="txt-box">
                <h3>Ingrédients & Notes</h3>
                <ul>
                    <li><span class="highlight">Notes de Tête :</span> Amande (Impression 5-15 min)</li>
                    <li><span class="highlight">Notes de Cœur :</span> Jasmin & Tubéreuse (Dure 20-60 min)</li>
                    <li><span class="highlight">Notes de Fond :</span> Fève Tonka & Cacao (Reste jusqu'à 6h)</li>
                </ul>
                <p style="font-size:10px; color:#666">Famille olfactive : AMBRÉE Florale</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">GOOD GIRL 10ML</h4><p style="color:#555; font-size:10px">POWERFUL SEDUCTION</p></div>
                    <img src="assets/gg-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NOM"><input type="tel" placeholder="TÉLÉPHONE"><input type="text" placeholder="VILLE"><button class="order-btn">COMMANDER | 319 DH</button></form>
            </div>
        </div>
    </section>

    <script>
        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        let currentIdx = 0;
        const btn = document.getElementById('scrollBtn');
        btn.onclick = () => {
            currentIdx = (currentIdx + 1) % sections.length;
            document.getElementById(sections[currentIdx]).scrollIntoView();
        };
        window.onscroll = () => {
            const scrollPos = window.scrollY + window.innerHeight / 2;
            sections.forEach((id, index) => {
                const el = document.getElementById(id);
                if (scrollPos >= el.offsetTop && scrollPos < el.offsetTop + el.offsetHeight) {
                    const color = getComputedStyle(el).getPropertyValue('--color');
                    document.documentElement.style.setProperty('--current-color', color);
                    currentIdx = index;
                }
            });
        };
    </script>
</body>
</html>
