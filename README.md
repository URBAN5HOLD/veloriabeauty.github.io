
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Fragrance</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* [كود الـ Scroll Snap - خدام غير ف الحاسوب] */
        html { scroll-behavior: smooth; }
        * { margin: 0; padding: 0; box-sizing: border-box; text-decoration: none; border: none !important; outline: none; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        
        /* [ضبط اللوغو الفوق] */
        .logo-fixed { position: fixed; top: 15px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.2rem; letter-spacing: 8px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }
        
        /* [ضبط الأقسام] */
        .product-section { width: 100%; position: relative; background: #000; padding-bottom: 50px; }

        /* [الفيديو من القنت للقنت] */
        .v-header { width: 100%; height: 56.25vw; max-height: 80vh; overflow: hidden; position: relative; }
        .bg-v { width: 100%; height: 100%; object-fit: cover; display: block; }
        
        /* [ضبط القرعة والعنوان ف الوسط] */
        .bottle-center { text-align: center; padding: 60px 0; }
        /* الحجم عادي وطبيعي ف الحاسوب */
        .img-bottle { width: 40%; max-width: 220px; height: auto; transition: 0.4s; cursor: zoom-in; }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 2.5rem; margin-top: 15px; letter-spacing: 6px; }

        /* [ضبط الصفوف] */
        .row { display: flex; align-items: center; width: 100%; padding: 40px 5%; position: relative; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 50%; display: flex; justify-content: center; z-index: 2; }
        .img-box img { width: 85%; max-width: 500px; border-radius: 2px; cursor: zoom-in; transition: 0.4s; }

        /* [ضبط النصوص والـ Glow] */
        .txt-box { width: 50%; padding: 0 5%; text-align: center; position: relative; z-index: 2; }
        .glow-effect { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 140%; height: 140%; background: radial-gradient(circle, var(--glow) 0%, transparent 75%); opacity: 0.3; z-index: -1; pointer-events: none; }

        h3 { font-family: 'Playfair Display', serif; font-size: 1.8rem; color: var(--color); margin-bottom: 15px; text-transform: uppercase; }
        .desc-full { font-size: 0.95rem; line-height: 1.7; color: #eee; }
        
        .specs-list { margin-top: 15px; list-style: none; display: inline-block; text-align: left; }
        .specs-list li { margin-bottom: 8px; font-size: 0.9rem; color: #fff; }
        .specs-list b { color: var(--color); }
        
        .tech-notes { font-size: 0.75rem; color: #bbb; margin-top: 20px; border-top: 1px solid rgba(255,255,255,0.2) !important; padding-top: 10px; max-width: 400px; margin: auto; }

        /* [ضبط الفورم] */
        .f-wrap { padding: 80px 0; text-align: center; }
        .f-glass { max-width: 420px; margin: 0 auto; padding: 30px; background: rgba(255,255,255,0.05); border-radius: 8px; border: 1px solid rgba(255,255,255,0.1) !important; }
        .in-f { width: 100%; padding: 18px; margin-bottom: 12px; background: rgba(255,255,255,0.1); color: #fff; border-radius: 4px; text-align: center; font-family: 'Montserrat'; font-size: 1rem; }
        .btn-f { width: 100%; padding: 20px; background: #fff; color: #000; font-weight: 800; cursor: pointer; letter-spacing: 2px; border-radius: 4px; transition: 0.3s; font-size: 1rem; }
        .btn-f:hover { background: var(--color); color: #fff; box-shadow: 0 5px 25px var(--glow); }
        .pri-txt { color: var(--color); margin-top: 15px; font-weight: 600; font-size: 0.85rem; }

        /* [تحسينات الموبايل - Smart Mobile Adjustments] */
        @media (max-width: 900px) {
            .logo-fixed { font-size: 1rem; letter-spacing: 5px; top: 10px; }
            .v-header { max-height: 70vh; }
            .bottle-center { padding: 40px 0; }
            /* الحجم ف الموبايل عادي ومريح (ماشي 80%) */
            .img-bottle { width: 45%; max-width: 250px; }
            .brand-logo { font-size: 1.8rem; letter-spacing: 4px; }
            .row, .row.rev { flex-direction: column; padding: 25px 5%; text-align: center; }
            .img-box, .txt-box { width: 100%; }
            .img-box img { width: 90%; margin-bottom: 15px; }
            h3 { font-size: 1.5rem; }
            .desc-full { font-size: 0.85rem; line-height: 1.6; }
            .f-wrap { padding: 50px 0; }
            .f-glass { padding: 20px; max-width: 380px; }
            /* إلغاء الـ Snap ف الموبايل لسهولة التصفح */
            .product-section { height: auto; scroll-snap-align: none; }
            html { scroll-snap-type: none; }
        }

        /* [ضبط الـ Zoom Overlay] */
        .zoom-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.95); display: none; justify-content: center; align-items: center; z-index: 2000; cursor: zoom-out; }
        .zoom-overlay img { max-width: 90%; max-height: 90%; object-fit: contain; }

        /* الألوان المميزة */
        .sauv-t { --glow: #0044ff; --color: #4A90E2; }
        .stron-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }
        .gg-t { --glow: #001a4d; --color: #1a4d99; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
    <div class="zoom-overlay" id="zoomOverlay"><img src="" id="zoomedImg"></div>

    <div class="product-section sauv-t">
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle" onclick="zoom(this)">
            <h1 class="brand-logo">SAUVAGE</h1>
        </div>
        
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-left.jpg" onclick="zoom(this)"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>La fragrance</h3>
                <p class="desc-full">Une composition haute couture infusée d'une fraîcheur sauvage.</p>
            </div>
        </div>

        <div class="f-wrap"><form class="f-glass">
            <input type="text" placeholder="Nom Complet" class="in-f" required>
            <input type="tel" placeholder="Numéro de Téléphone" class="in-f" required>
            <input type="text" placeholder="Ville et Adresse" class="in-f" required>
            <button type="submit" class="btn-f">COMMANDER | 319 DH</button>
            <p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p>
        </form></div>
    </div>

    <script>
        // كود الـ Zoom
        function zoom(img) {
            const overlay = document.getElementById('zoomOverlay');
            const zoomedImg = document.getElementById('zoomedImg');
            zoomedImg.src = img.src;
            overlay.style.display = 'flex';
        }
        document.getElementById('zoomOverlay').onclick = function() {
            this.style.display = 'none';
        }
    </script>

</body>
</html>
