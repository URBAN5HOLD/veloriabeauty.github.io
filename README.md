<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* الحل النهائي لمشكل الهروب لليسر والتحرك الجانبي */
        html, body { 
            width: 100%; 
            margin: 0; padding: 0;
            overflow-x: hidden; /* منع التحرك الجانبي */
            background-color: #000; 
            color: #fff;
            font-family: 'Montserrat', sans-serif;
            scroll-snap-type: y mandatory; 
            scroll-behavior: smooth;
        }

        * { box-sizing: border-box; margin: 0; padding: 0; border: none !important; outline: none; }
        
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.1rem; letter-spacing: 6px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        .product-section { 
            width: 100%; 
            min-height: 100vh; 
            scroll-snap-align: start; 
            position: relative; 
            display: flex;
            flex-direction: column;
            align-items: center; /* سنترة المحتوى في الوسط */
            overflow: hidden;
            padding-bottom: 60px;
        }

        /* الفيديو المستطيل من القنت للقنت */
        .v-header { 
            width: 100%; 
            height: 50vh; /* مستطيل احترافي */
            overflow: hidden; 
            position: relative; 
        }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }
        
        .bottle-center { text-align: center; padding: 40px 20px; width: 100%; }
        .img-bottle { width: 45%; max-width: 170px; height: auto; cursor: zoom-in; margin: 0 auto; display: block; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2rem; margin-top: 15px; letter-spacing: 5px; text-transform: uppercase; }

        .row { display: flex; align-items: center; justify-content: center; width: 100%; padding: 30px 5%; gap: 20px; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; }
        .img-box img { width: 100%; max-width: 400px; border-radius: 2px; }
        .txt-box { width: 50%; padding: 0 20px; text-align: left; position: relative; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%; height: 100%; background: radial-gradient(circle, var(--glow) 0%, transparent 70%); opacity: 0.15; z-index: -1; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.4rem; color: var(--color); margin-bottom: 12px; text-transform: uppercase; border-bottom: 1px solid var(--color) !important; display: inline-block; }
        p { font-size: 0.85rem; line-height: 1.6; color: #eee; margin-bottom: 10px; }

        /* منطقة الشراء المودرن مسنترة */
        .purchase-area { width: 100%; max-width: 1000px; margin: 50px auto; display: flex; flex-wrap: wrap; gap: 40px; padding: 0 5%; align-items: flex-start; justify-content: center; }
        .details-side { width: 45%; min-width: 280px; }
        .form-side { width: 50%; min-width: 280px; }

        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; border-bottom: 1px solid rgba(255,255,255,0.1) !important; padding-bottom: 10px; }
        .mini-thumb { width: 60px; height: 60px; border-radius: 2px; object-fit: cover; }
        
        .size-container { display: flex; gap: 10px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { padding: 12px; border: 1px solid rgba(255,255,255,0.1) !important; border-radius: 2px; transition: 0.3s; }
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.05); color: var(--color); }

        .form-side input { width: 100%; padding: 15px; margin-bottom: 10px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.1) !important; }
        .buy-btn { width: 100%; padding: 20px; background: #fff; color: #000; font-weight: 800; font-size: 1rem; cursor: pointer; letter-spacing: 2px; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; }

        @media (max-width: 800px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 20px 5%; }
            .img-box, .txt-box { width: 100%; text-align: center; }
            .purchase-area { flex-direction: column-reverse; align-items: center; width: 100%; }
            .details-side, .form-side { width: 90%; }
            .brand-logo { font-size: 1.8rem; }
        }

        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="zoom-overlay" id="zoomOverlay" onclick="this.style.display='none'"><img src="" id="zoomedImg" style="max-width:90%"></div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">SAUVAGE</h1></div>
        <div class="row"><div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Raw elegance that reveals an authentic man. Fresh and powerful trail.</p></div></div>
        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>SAUVAGE</h2><p style="font-size:10px; color:#888;">PREMIUM DECANT</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 'i1')"><div class="size-box"><span>5ML</span><p style="font-size:9px">75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 'i1')"><div class="size-box"><span>10ML</span><p style="font-size:9px">150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="i1" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        <div class="row"><div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>Magnetic and sensual energy. A surprise of originality.</p></div></div>
        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>STRONGER WITH YOU</h2><p style="font-size:10px; color:#888;">INTENSE FRAGRANCE</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 'i2')"><div class="size-box"><span>5ML</span><p style="font-size:9px">75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 'i2')"><div class="size-box"><span>10ML</span><p style="font-size:9px">150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="i2" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/libre-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">LIBRE (EDP)</h1></div>
        <div class="row"><div class="img-box"><img src="assets/libre-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The perfume of freedom. Sensual orange blossom and bold lavender.</p></div></div>
        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>YSL LIBRE EDP</h2><p style="font-size:10px; color:#888;">FEMALE ELEGANCE</p></div><img src="assets/libre-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 'i3')"><div class="size-box"><span>5ML</span><p style="font-size:9px">75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 'i3')"><div class="size-box"><span>10ML</span><p style="font-size:9px">150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="i3" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/goodgirl-bottle.png" class="img-bottle" onclick="zoom(this)"><h1 class="brand-logo">GOOD GIRL</h1></div>
        <div class="row"><div class="img-box"><img src="assets/gg-detail-left.jpg" onclick="zoom(this)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The sweetness of jasmine mixed with rich cocoa and tonka bean.</p></div></div>
        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>CH GOOD GIRL</h2><p style="font-size:10px; color:#888;">POWDERED SEDUCTION</p></div><img src="assets/gg-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 'i4')"><div class="size-box"><span>5ML</span><p style="font-size:9px">75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 'i4')"><div class="size-box"><span>10ML</span><p style="font-size:9px">150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="i4" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
    </div>

    <script>
        function zoom(img) {
            document.getElementById('zoomOverlay').style.display = 'flex';
            document.getElementById('zoomedImg').src = img.src || img;
        }
        function selectSize(element, size, inputId) {
            element.parentElement.querySelectorAll('.size-item').forEach(i => i.classList.remove('active'));
            element.classList.add('active');
            document.getElementById(inputId).value = size;
        }
    </script>
</body>
</html>
