<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Luxury Perfumes</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* التنقيزة ومنع الهروب الجانبي */
        html, body { 
            width: 100%; 
            margin: 0; padding: 0;
            overflow-x: hidden; 
            background-color: #000; 
            scroll-snap-type: y mandatory; 
            scroll-behavior: smooth;
            -webkit-overflow-scrolling: touch;
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
            padding-bottom: 100px;
        }

        /* الفيديو 100% عرض */
        .v-header { width: 100%; position: relative; overflow: hidden; }
        .bg-v { width: 100%; height: auto; display: block; }
        
        .bottle-center { text-align: center; padding: 60px 0; }
        .img-bottle { width: 40%; max-width: 180px; cursor: zoom-in; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.2rem; color: #fff; margin-top: 15px; letter-spacing: 6px; }

        /* الصفوف (ليمن وليسر) مع المعلومات كاملة */
        .row { display: flex; align-items: center; width: 100%; padding: 50px 5%; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; }
        .img-box img { width: 90%; max-width: 450px; border-radius: 2px; cursor: zoom-in; }
        
        .txt-box { width: 50%; padding: 0 5%; text-align: left; position: relative; color: #fff; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 140%; height: 140%; background: radial-gradient(circle, var(--glow) 0%, transparent 75%); opacity: 0.3; z-index: -1; pointer-events: none; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.8rem; color: var(--color); margin-bottom: 15px; text-transform: uppercase; border-bottom: 1px solid var(--color) !important; display: inline-block; padding-bottom: 5px; }
        p { font-family: 'Montserrat', sans-serif; font-size: 0.9rem; line-height: 1.6; color: #eee; margin-bottom: 10px; }
        b { color: var(--color); }

        .tech-notes { font-size: 0.75rem; color: #bbb; margin-top: 20px; font-style: italic; border-top: 1px solid rgba(255,255,255,0.2) !important; padding-top: 15px; line-height: 1.5; }

        /* منطقة الشراء */
        .purchase-area { max-width: 1000px; margin: 80px auto 0; display: flex; gap: 50px; padding: 20px; align-items: flex-start; }
        .details-side { width: 45%; }
        .form-side { width: 55%; }
        .product-meta { display: flex; justify-content: space-between; align-items: center; margin-bottom: 25px; border-bottom: 1px solid rgba(255,255,255,0.1) !important; padding-bottom: 10px; }
        .mini-thumb { width: 60px; height: 60px; object-fit: cover; }
        
        .size-container { display: flex; gap: 15px; margin-top: 20px; }
        .size-item { flex: 1; cursor: pointer; text-align: center; }
        .size-box { padding: 15px; border: 1px solid rgba(255,255,255,0.1) !important; border-radius: 2px; transition: 0.4s; }
        .size-item.active .size-box { border-color: var(--color) !important; background: rgba(255,255,255,0.05); color: var(--color); }

        .form-side input { width: 100%; padding: 18px; margin-bottom: 12px; background: transparent; color: #fff; border-bottom: 1px solid rgba(255,255,255,0.15) !important; }
        .buy-btn { width: 100%; padding: 22px; background: #fff; color: #000; font-weight: 800; font-size: 1.1rem; cursor: pointer; letter-spacing: 2px; }

        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; }

        @media (max-width: 900px) {
            .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; }
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column-reverse; width: 100%; }
            .details-side, .form-side { width: 100%; }
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
        <div class="bottle-center"><img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">SAUVAGE</h1></div>
        
        <div class="row"><div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>A high-fashion composition infused with wild freshness. A raw elegance that reveals an authentic and true man.</p><h3>The Bottle</h3><p>A luxurious design object with dark lines, reflecting the power of the desert at twilight.</p></div></div>
        
        <div class="row rev"><div class="img-box"><img src="assets/sauvage-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Calabria Bergamot</p><p><b>Heart:</b> Sichuan Pepper & Lavender</p><p><b>Base:</b> Ambroxan & Musk</p><div class="tech-notes"><p>* Top: First impression (5-15 min).</p><p>* Heart: Emerges after (20-60 min).</p><p>* Base: Longest lasting (up to 6 hours).</p></div></div></div>

        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>SAUVAGE</h2><p style="font-size:10px; color:#666;">PREMIUM DECANT</p></div><img src="assets/sauvage-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 's1')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 's1')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="s1" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
    </div>

    <div class="product-section stron-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/stronger-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">STRONGER WITH YOU</h1></div>
        <div class="row"><div class="img-box"><img src="assets/stronger-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>A fragrance that surprises with its originality. It lives in the present with modern energy.</p><h3>The Bottle</h3><p>The curves recall masculine shoulders. A clean design for a powerful essence.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/stronger-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Cardamom & Pink Pepper</p><p><b>Heart:</b> Sage & Violet Leaf</p><p><b>Base:</b> Vanilla & Chestnut</p><div class="tech-notes"><p>* Top: First impression (5-15 min).</p><p>* Heart: Emerges after (20-60 min).</p><p>* Base: Longest lasting (up to 6 hours).</p></div></div></div>
        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>STRONGER WITH YOU</h2><p style="font-size:10px; color:#666;">INTENSE MALE</p></div><img src="assets/stronger-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 's2')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 's2')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="s2" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
    </div>

    <div class="product-section libre-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/libre-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">LIBRE (EDP)</h1></div>
        <div class="row"><div class="img-box"><img src="assets/libre-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>The perfume of freedom. A floral masterpiece mixing orange blossom and lavender.</p><h3>The Bottle</h3><p>A couture bottle with an oversized logo, reflecting luxury and strength.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/libre-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Mandarin & Lavender</p><p><b>Heart:</b> Orange Blossom & Jasmine</p><p><b>Base:</b> Vanilla & Musk</p><div class="tech-notes"><p>* Top: First impression (5-15 min).</p><p>* Heart: Emerges after (20-60 min).</p><p>* Base: Longest lasting (up to 6 hours).</p></div></div></div>
        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>YSL LIBRE EDP</h2><p style="font-size:10px; color:#666;">CHIC FEMALE</p></div><img src="assets/libre-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 's3')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 's3')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="s3" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
    </div>

    <div class="product-section gg-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center"><img src="assets/goodgirl-bottle.png" class="img-bottle" onclick="zoom(this.src)"><h1 class="brand-logo">GOOD GIRL</h1></div>
        <div class="row"><div class="img-box"><img src="assets/gg-detail-left.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>The Fragrance</h3><p>A mysterious and sensual scent. The power of jasmine and the warmth of cocoa.</p><h3>The Bottle</h3><p>The iconic stiletto is the image of a powerful and modern woman.</p></div></div>
        <div class="row rev"><div class="img-box"><img src="assets/gg-detail-right.jpg" onclick="zoom(this.src)"></div><div class="txt-box"><div class="glow-effect"></div><h3>Olfactory Notes</h3><p><b>Top:</b> Almond</p><p><b>Heart:</b> Tuberose & Jasmine</p><p><b>Base:</b> Tonka Bean & Cocoa</p><div class="tech-notes"><p>* Top: First impression (5-15 min).</p><p>* Heart: Emerges after (20-60 min).</p><p>* Base: Longest lasting (up to 6 hours).</p></div></div></div>
        <div class="purchase-area"><div class="details-side"><div class="product-meta"><div><h2>CH GOOD GIRL</h2><p style="font-size:10px; color:#666;">SEDUCTIVE FEMALE</p></div><img src="assets/gg-hand.jpg" class="mini-thumb"></div><div class="size-container"><div class="size-item" onclick="selectSize(this, '5ml', 's4')"><div class="size-box"><span>5ML</span><p style="font-size:9px">~ 75 SPRAYS</p></div></div><div class="size-item active" onclick="selectSize(this, '10ml', 's4')"><div class="size-box"><span>10ML</span><p style="font-size:9px">~ 150 SPRAYS</p></div></div></div></div><div class="form-side"><form><input type="hidden" id="s4" value="10ml"><input type="text" placeholder="NAME"><input type="tel" placeholder="PHONE"><input type="text" placeholder="CITY"><button class="buy-btn">ORDER NOW | 319 DH</button></form></div></div>
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
