<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | The Elite Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root { --gold: #D4AF37; --bg: #000; }
        
        html, body { 
            width: 100%; margin: 0; padding: 0;
            overflow-x: hidden; background-color: var(--bg);
            scroll-snap-type: y mandatory; scroll-behavior: smooth;
            font-family: 'Montserrat', sans-serif;
        }

        * { box-sizing: border-box; outline: none; }

        .logo-fixed { 
            position: fixed; top: 20px; left: 50%; transform: translateX(-50%); 
            z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; 
            letter-spacing: 10px; color: #fff;
        }

        .product-section { 
            width: 100%; min-height: 100vh; scroll-snap-align: start; 
            scroll-snap-stop: always; position: relative; display: flex; 
            flex-direction: column; padding-bottom: 100px;
        }

        .v-header { width: 100%; line-height: 0; background: #000; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }

        .bottle-center { text-align: center; padding: 40px 0 10px; }
        .img-bottle { width: 38%; max-width: 150px; margin: 0 auto; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; letter-spacing: 8px; margin-top: 10px; border: none !important; }
        .perfume-sub { font-size: 0.75rem; color: var(--color); letter-spacing: 5px; text-transform: uppercase; font-weight: 200; }

        .row { display: flex; align-items: center; width: 100%; padding: 30px 8%; gap: 30px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; }
        .img-box img { width: 100%; border-radius: 2px; }
        
        .txt-box { width: 50%; color: #fff; position: relative; }
        .glow { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 150%; height: 150%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.15; z-index: -1; }

        h3 { font-family: 'Cinzel', serif; font-size: 1.4rem; margin-bottom: 15px; color: #fff; letter-spacing: 2px; }
        p { font-size: 0.9rem; line-height: 1.7; color: #bbb; font-weight: 300; margin-bottom: 10px; }
        b { color: var(--color); }

        .perf-data { border-left: 1px solid var(--color); padding-left: 15px; font-size: 0.8rem; margin-top: 15px; color: #888; }

        /* سهم السكرول الجديد - عصري وبسيط */
        .scroll-indicator {
            position: absolute; bottom: 40px; left: 50%; transform: translateX(-50%);
            cursor: pointer; z-index: 100; text-align: center;
        }
        .arrow-v {
            width: 25px; height: 15px; border-left: 2px solid var(--color); border-bottom: 2px solid var(--color);
            transform: rotate(-45deg); animation: blink-arrow 2s infinite;
        }
        @keyframes blink-arrow {
            0% { opacity: 0; transform: rotate(-45deg) translate(0, 0); }
            50% { opacity: 1; }
            100% { opacity: 0; transform: rotate(-45deg) translate(-10px, 10px); }
        }

        .purchase-area { max-width: 1000px; margin: 40px auto; display: flex; gap: 40px; padding: 30px; border-top: 1px solid rgba(255,255,255,0.05); width: 90%; }
        .mini-thumb { width: 75px; height: 75px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1); }
        .size-box { flex: 1; padding: 18px; border: 1px solid rgba(255,255,255,0.1); text-align: center; color: #fff; font-size: 0.8rem; }
        .active-size { border-color: var(--color); color: var(--color); background: rgba(255,255,255,0.02); }

        .order-btn { width: 100%; padding: 22px; background: #fff; color: #000; font-family: 'Montserrat'; font-weight: 800; font-size: 1rem; cursor: pointer; letter-spacing: 3px; margin-top: 10px; }

        /* إصلاح الخطوط اللي في الصورة */
        input { 
            width: 100%; padding: 18px 5px; margin-bottom: 15px; 
            background: transparent; color: #fff; 
            border: none !important;
            border-bottom: 1px solid rgba(255,255,255,0.15) !important; 
            font-family: 'Montserrat', sans-serif; font-size: 0.9rem;
        }
        input:focus { border-bottom: 1px solid var(--color) !important; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 20px 10%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; gap: 30px; }
        }

        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <section class="product-section sauv-t" id="s1">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE</h1>
            <div class="perfume-sub">ELIXIR / EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>THE ELIXIR</h3>
                <p>An extraordinary concentration. A nocturnal soul capturing the raw power of the desert.</p>
                <div class="perf-data"><b>Notes:</b> Cinnamon, Cardamom, Lavender essence & Rich Woods.</div>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">DECANT 10ML</h4><p style="color:#555; font-size:10px">PREMIUM QUALITY</p></div>
                    <img src="assets/sauvage-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><button class="order-btn">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
        <div class="scroll-indicator" onclick="document.getElementById('s2').scrollIntoView();"><div class="arrow-v"></div></div>
    </section>

    <section class="product-section stron-t" id="s2">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">ABSOLUTELY / PARFUM INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-left.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>THE INTENSITY</h3>
                <p>A magnetic power reflecting absolute love. Addictive and highly sophisticated.</p>
                <div class="perf-data"><b>Notes:</b> Rum Accord, Lavender & Madagascar Vanilla.</div>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">INTENSE 10ML</h4><p style="color:#555; font-size:10px">MALE ELEGANCE</p></div>
                    <img src="assets/stronger-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><button class="order-btn">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
        <div class="scroll-indicator" onclick="document.getElementById('s3').scrollIntoView();"><div class="arrow-v"></div></div>
    </section>

    <section class="product-section libre-t" id="s3">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE</h1>
            <div class="perfume-sub">EAU DE PARFUM / INTENSE</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-left.jpg"></div>
            <div class="txt-box"><div class="glow"></div>
                <h3>THE FREEDOM</h3>
                <p>The floral fire of a woman living by her own rules. Bold and couture.</p>
                <div class="perf-data"><b>Notes:</b> French Lavender, Moroccan Orange Blossom & Vanilla.</div>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div style="display:flex; justify-content:space-between; margin-bottom:20px">
                    <div><h4 style="color:#fff; font-family:'Cinzel'">LIBRE 10ML</h4><p style="color:#555; font-size:10px">FEMALE ELITE</p></div>
                    <img src="assets/libre-hand.jpg" class="mini-thumb">
                </div>
                <div style="display:flex; gap:10px"><div class="size-box">5ML</div><div class="size-box active-size">10ML</div></div>
            </div>
            <div style="flex:1.2">
                <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><button class="order-btn">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
    </section>

</body>
</html>
