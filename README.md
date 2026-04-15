<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | The Elite Experience</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root { --main-gold: #D4AF37; }
        * { box-sizing: border-box; margin: 0; padding: 0; border: none !important; -webkit-tap-highlight-color: transparent; }
        
        body, html { height: 100%; background: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow: hidden; }

        .logo-fixed { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 8px; text-shadow: 0 0 15px rgba(0,0,0,0.9); }

        /* حاوية السلايدر */
        .swiper { width: 100%; height: 100vh; }
        .swiper-slide { 
            height: 100vh; 
            overflow-y: auto; /* كيسمح بالسكول وسط العطر الواحد إلا كانت الهضرة كثيرة */
            display: flex; 
            flex-direction: column; 
            background: #000;
        }

        /* الفيديو العريض */
        .v-header { width: 100%; background: #000; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; object-fit: contain; }

        .content-wrapper { padding: 40px 20px 100px; }

        .bottle-center { text-align: center; margin-bottom: 40px; }
        .img-bottle { width: 45%; max-width: 180px; margin: 0 auto; display: block; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; margin-top: 15px; letter-spacing: 6px; }
        .perfume-sub { font-size: 0.75rem; color: var(--color); letter-spacing: 4px; text-transform: uppercase; margin-top: 5px; }

        /* صفوف المعلومات */
        .info-row { display: flex; align-items: center; margin-bottom: 50px; gap: 20px; }
        .info-row.rev { flex-direction: row-reverse; }
        .info-img { width: 50%; position: relative; }
        .info-img img { width: 100%; border-radius: 2px; }
        .info-txt { width: 50%; position: relative; }
        
        .glow { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 150%; height: 150%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.25; z-index: -1; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.4rem; margin-bottom: 10px; text-transform: uppercase; border-bottom: 1px solid var(--color) !important; display: inline-block; }
        p { font-size: 0.9rem; line-height: 1.6; color: #ddd; margin-bottom: 10px; }
        b { color: var(--color); }

        .perf-box { margin-top: 15px; padding: 10px; border: 0.5px solid rgba(255,255,255,0.1) !important; font-size: 0.8rem; background: rgba(255,255,255,0.02); }

        /* منطقة الشراء */
        .buy-zone { margin-top: 40px; padding: 25px; background: rgba(255,255,255,0.03); border-radius: 4px; }
        .buy-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; }
        
        /* الصورة الصغيرة: +5% وجامدة */
        .mini-thumb { width: 72px; height: 72px; object-fit: cover; border: 1px solid rgba(255,255,255,0.1) !important; pointer-events: none; }
        
        .size-grid { display: flex; gap: 10px; margin-bottom: 25px; }
        .size-btn { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.2) !important; text-align: center; cursor: pointer; transition: 0.3s; }
        .size-btn.active { border-color: var(--color) !important; color: var(--color); background: rgba(255,255,255,0.05); }

        input { width: 100%; padding: 18px; margin-bottom: 15px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.1) !important; font-size: 1rem; }
        .order-btn { width: 100%; padding: 22px; background: #fff; color: #000; font-weight: 800; font-size: 1.1rem; letter-spacing: 2px; cursor: pointer; }

        /* ألوان العطور */
        .sauvage { --glow: #0044ff; --color: #4A90E2; }
        .stronger { --glow: #8b4513; --color: #CD7F32; }
        .libre { --glow: #b8860b; --color: #D4AF37; }
        .goodgirl { --glow: #001a4d; --color: #1a4d99; }

        @media (max-width: 600px) {
            .info-row, .info-row.rev { flex-direction: column; text-align: center; }
            .info-img, .info-txt { width: 100%; }
        }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="swiper mySwiper">
        <div class="swiper-wrapper">
            
            <div class="swiper-slide sauvage">
                <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
                <div class="content-wrapper">
                    <div class="bottle-center">
                        <img src="assets/sauvage-bottle.png" class="img-bottle">
                        <h1 class="brand-logo">SAUVAGE</h1>
                        <div class="perfume-sub">ELIXIR / EXTRAIT DE PARFUM</div>
                    </div>
                    <div class="info-row">
                        <div class="info-img"><img src="assets/sauvage-left.jpg"></div>
                        <div class="info-txt"><div class="glow"></div><h3>The Fragrance</h3><p>A high-fashion composition infused with wild freshness. Noble and raw.</p></div>
                    </div>
                    <div class="info-row rev">
                        <div class="info-img"><img src="assets/sauvage-right.jpg"></div>
                        <div class="info-txt"><div class="glow"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Spices | <b>Heart:</b> Lavender | <b>Base:</b> Woods</p>
                        <div class="perf-box">Longevity: 12h+ | Sillage: Powerful</div></div>
                    </div>
                    <div class="buy-zone">
                        <div class="buy-header"><div><h2>SAUVAGE ELIXIR</h2><p>Premium Decant</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb"></div>
                        <div class="size-grid"><div class="size-btn">5ML</div><div class="size-btn active">10ML</div></div>
                        <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><button class="order-btn">GET IT NOW | 319 DH</button></form>
                    </div>
                </div>
            </div>

            <div class="swiper-slide stronger">
                <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
                <div class="content-wrapper">
                    <div class="bottle-center">
                        <img src="assets/stronger-bottle.png" class="img-bottle">
                        <h1 class="brand-logo">STRONGER WITH YOU</h1>
                        <div class="perfume-sub">ABSOLUTELY / PARFUM INTENSE</div>
                    </div>
                    <div class="info-row">
                        <div class="info-img"><img src="assets/stronger-left.jpg"></div>
                        <div class="info-txt"><div class="glow"></div><h3>The Scent</h3><p>Magnetic energy. Bold, unpredictable and sensual.</p></div>
                    </div>
                    <div class="info-row rev">
                        <div class="info-img"><img src="assets/stronger-right.jpg"></div>
                        <div class="info-txt"><div class="glow"></div><h3>Notes</h3><p><b>Top:</b> Cardamom | <b>Heart:</b> Sage | <b>Base:</b> Chestnut</p>
                        <div class="perf-box">Longevity: 10h+ | Sillage: Heavy</div></div>
                    </div>
                    <div class="buy-zone">
                        <div class="buy-header"><div><h2>SWY ABSOLUTELY</h2><p>Intense Male</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb"></div>
                        <div class="size-grid"><div class="size-btn">5ML</div><div class="size-btn active">10ML</div></div>
                        <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><button class="order-btn">GET IT NOW | 319 DH</button></form>
                    </div>
                </div>
            </div>

            <div class="swiper-slide libre">
                <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
                <div class="content-wrapper">
                    <div class="bottle-center">
                        <img src="assets/libre-bottle.png" class="img-bottle">
                        <h1 class="brand-logo">LIBRE</h1>
                        <div class="perfume-sub">EAU DE PARFUM / FEMME</div>
                    </div>
                    <div class="info-row">
                        <div class="info-img"><img src="assets/libre-left.jpg"></div>
                        <div class="info-txt"><div class="glow"></div><h3>Freedom</h3><p>A floral masterpiece mixing orange blossom and French lavender.</p></div>
                    </div>
                    <div class="buy-zone">
                        <div class="buy-header"><div><h2>YSL LIBRE EDP</h2><p>Chic Female</p></div><img src="assets/libre-hand.jpg" class="mini-thumb"></div>
                        <div class="size-grid"><div class="size-btn">5ML</div><div class="size-btn active">10ML</div></div>
                        <form><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><button class="order-btn">GET IT NOW | 319 DH</button></form>
                    </div>
                </div>
            </div>

        </div>
        <div class="swiper-pagination"></div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
    <script>
        var swiper = new Swiper(".mySwiper", {
            direction: "vertical", // كينقز من الفوق لتحت بحال تيك توك
            slidesPerView: 1,
            spaceBetween: 0,
            mousewheel: true,
            pagination: {
                el: ".swiper-pagination",
                clickable: true,
            },
        });
    </script>
</body>
</html>
