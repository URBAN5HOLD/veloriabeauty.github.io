<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* رجعنا السكول اللي كينقز ومنعنا التحرك الجانبي */
        html, body { 
            width: 100%; 
            margin: 0; padding: 0;
            overflow-x: hidden; 
            background-color: #000; 
            scroll-snap-type: y mandatory; 
            scroll-behavior: smooth;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 6px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { 
            width: 100%; 
            min-height: 100vh; 
            scroll-snap-align: start; 
            position: relative; 
            background: #000;
            overflow: hidden;
            padding-bottom: 80px;
        }

        /* تعديل الفيديو: عريض 100% وشكل مستطيل ناضي */
        .v-header { 
            width: 100%; 
            height: 50vh; /* هادي كتخليه مستطيل عريض */
            overflow: hidden; 
            position: relative; 
        }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }
        
        .bottle-center { text-align: center; padding: 50px 0; }
        .img-bottle { width: 40%; max-width: 180px; cursor: zoom-in; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; margin-top: 15px; letter-spacing: 6px; }

        /* رجعنا الصفوف ديال التصاور (ليمن وليسر) */
        .row { display: flex; align-items: center; width: 100%; padding: 40px 5%; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; }
        .img-box img { width: 90%; max-width: 450px; border-radius: 2px; cursor: zoom-in; }
        .txt-box { width: 50%; padding: 0 5%; text-align: left; position: relative; color: #fff; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 130%; height: 130%; background: radial-gradient(circle, var(--glow) 0%, transparent 75%); opacity: 0.3; z-index: -1; pointer-events: none; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.6rem; color: var(--color); margin-bottom: 15px; text-transform: uppercase; border-bottom: 1px solid var(--color); display: inline-block; padding-bottom: 5px; }
        p, b { font-family: 'Montserrat', sans-serif; font-size: 0.9rem; line-height: 1.6; margin-bottom: 10px; }
        b { color: var(--color); }

        /* منطقة الشراء */
        .purchase-area { max-width: 1100px; margin: 60px auto 0; display: flex; gap: 40px; padding: 20px; align-items: flex-start; }
        .details-side { width: 45%; }
        .form-side { width: 55%; }

        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px; border-bottom: 1px solid rgba(255,255,255,0.1); padding-bottom: 15px; }
        .product-meta h2 { font-family: 'Cinzel', serif; font-size: 1rem; color: #fff; letter-spacing: 2px; }
        .mini-thumb { width: 65px; height: 65px; object-fit: cover; border: 1px solid rgba(255,255,255,0.2); }
        
        .size-container { display: flex; gap: 15px; margin-top: 20px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; color: #fff; }
        .size-box { padding: 15px; border: 1px solid rgba(255,255,255,0.15); border-radius: 2px; transition: 0.4s; }
        .size-item.active .size-box { border-color: var(--color); background: rgba(255,255,255,0.05); color: var(--color); box-shadow: 0 0 15px var(--glow); }

        .form-side input { width: 100%; padding: 18px; margin-bottom: 15px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.2); font-size: 0.9rem; }
        .buy-btn { width: 100%; padding: 22px; background: #fff; color: #000; font-weight: 800; cursor: pointer; font-size: 1rem; letter-spacing: 2px; transition: 0.4s; }
        .buy-btn:hover { background: var(--color); color: #fff; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; cursor: zoom-out; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 30px 5%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; gap: 40px; }
            .details-side, .form-side { width: 100%; }
        }

        /* Colors per product */
        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="zoom-overlay" id="zoomOverlay" onclick="this.style.display='none'"><img src="" id="zoomedImg" style="max-width: 90%;"></div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">SAUVAGE</h1></div>
        <div class="row"><div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>A high-fashion composition infused with wild freshness. Raw elegance at its peak.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/sauvage-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Notes</h3><p><b>Top:</b> Bergamot | <b>Heart:</b> Lavender | <b>Base:</b> Ambroxan</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>SAUVAGE ELIXIR</h2><p style="font-size:10px; color:#666;">PREMIUM DECANT</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i1')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i1')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i1" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        <div class="row"><div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>A magnetic fragrance for the modern man. Bold and unpredictable.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/stronger-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Notes</h3><p><b>Top:</b> Cardamom | <b>Heart:</b> Sage | <b>Base:</b> Vanilla</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>STRONGER WITH YOU</h2><p style="font-size:10px; color:#666;">INTENSE MALE</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i2')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i2')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i2" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/libre-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">LIBRE (EDP)</h1></div>
        <div class="row"><div class="img-box"><img src="assets/libre-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The scent of freedom. A floral masterpiece for the bold woman.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/libre-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Notes</h3><p><b>Top:</b> Lavender | <b>Heart:</b> Orange Blossom | <b>Base:</b> Vanilla</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>YSL LIBRE EDP</h2><p style="font-size:10px; color:#666;">CHIC FEMALE</p></div><img src="assets/libre-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i3')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i3')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i3" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/goodgirl-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">GOOD GIRL</h1></div>
        <div class="row"><div class="img-box"><img src="assets/gg-detail-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>It's so good to be bad. A mysterious and sensual combination.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/gg-detail-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Notes</h3><p><b>Top:</b> Almond | <b>Heart:</b> Jasmine | <b>Base:</b> Cocoa</p></div></div>
        <div class="purchase-area">
            <div class="details-side">
                <div class="product-meta"><div><h2>CH GOOD GIRL</h2><p style="font-size:10px; color:#666;">SEDUCTIVE FEMALE</p></div><img src="assets/gg-hand.jpg" class="mini-thumb"></div>
                <div class="size-container">
                    <div class="size-item" onclick="selectSize(this, '5ml', 'i4')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div>
                    <div class="size-item active" onclick="selectSize(this, '10ml', 'i4')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div>
                </div>
            </div>
            <div class="form-side"><form><input type="hidden" id="i4" value="10ml"><input type="text" placeholder="FULL NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div>
        </div>
    </div>

    <script>
        function zoom(src) {
            const overlay = document.getElementById('zoomOverlay');
            const zoomedImg = document.getElementById('zoomedImg');
            zoomedImg.src = src;
            overlay.style.display = 'flex';
        }
        function selectSize(element, size, inputId) {
            element.parentElement.querySelectorAll('.size-item').forEach(i => i.classList.remove('active'));
            element.classList.add('active');
            document.getElementById(inputId).value = size;
        }
    </script>
</body>
</html>
