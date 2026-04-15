<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Fragrance Collection</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Bodoni+Moda:ital,wght@1,600&family=Montserrat:wght@300;400;600;800&family=Playfair+Display:ital,wght@1,500&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body { margin: 0; padding: 0; width: 100%; background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; scroll-behavior: smooth; }

        .logo-fixed { position: fixed; top: 25px; left: 50%; transform: translateX(-50%); z-index: 1000; font-family: 'Cinzel', serif; font-size: 1.5rem; letter-spacing: 12px; color: #fff; text-shadow: 0 0 10px rgba(0,0,0,0.8); }

        .product-master-wrapper { margin-bottom: 40px; border-bottom: 1px solid rgba(255,255,255,0.05); }

        /* Hero */
        .hero-section { height: 100vh; width: 100%; position: relative; display: flex; flex-direction: column; align-items: center; justify-content: center; }
        .bg-video { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; object-fit: cover; filter: brightness(0.4); }
        .hero-content { position: relative; z-index: 10; text-align: center; }
        .product-img-main { width: 75vw; max-width: 360px; filter: drop-shadow(0px 20px 60px rgba(0,0,0,1)); }

        /* Sections */
        .details-section { min-height: 60vh; width: 100%; display: flex; align-items: center; padding: 40px 8%; gap: 40px; background: #080808; }
        .details-section.reverse { flex-direction: row-reverse; background: #000; }

        .text-side { flex: 1.2; text-align: center; }
        .image-side { flex: 0.8; display: flex; justify-content: center; }
        .side-img { width: 100%; max-width: 380px; border-radius: 4px; filter: brightness(0.8); }

        h2 { border: none !important; margin-bottom: 15px; } /* إزالة الخط نهائياً */
        h3 { font-family: 'Playfair Display', serif; font-size: 2rem; margin-bottom: 15px; }
        .desc-text { font-size: 0.95rem; line-height: 1.7; color: #bbb; max-width: 550px; margin: 0 auto; text-align: center; }
        
        .specs-list { list-style: none; margin-top: 20px; color: #fff; font-size: 0.9rem; }
        .specs-list li { margin: 8px 0; }
        .specs-list b { color: var(--theme-color); }

        /* Form */
        .form-container { padding: 60px 5%; text-align: center; background: #000; }
        .glass-form { background: rgba(255, 255, 255, 0.04); backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px); padding: 40px 30px; border-radius: 25px; border: 1px solid rgba(255,255,255,0.08); max-width: 450px; margin: 0 auto; }
        
        .input-field { width: 100%; background: rgba(255,255,255,0.06); border: none; padding: 16px; margin-bottom: 15px; border-radius: 12px; color: #fff; text-align: center; outline: none; border: 1px solid rgba(255,255,255,0.1); }
        
        /* الزر الأبيض الفخم */
        .order-btn { width: 100%; padding: 20px; border-radius: 12px; font-weight: 800; cursor: pointer; border: none; text-transform: uppercase; letter-spacing: 2px; background: #f5f5f5; color: #000; transition: 0.4s; }
        .order-btn:hover { background: #fff; transform: translateY(-3px); box-shadow: 0 10px 20px rgba(255,255,255,0.1); }

        .priority-msg { font-size: 0.85rem; margin-top: 15px; font-weight: 500; font-style: italic; letter-spacing: 0.5px; }

        /* الألوان المخصصة */
        .sauvage-theme { --theme-color: #4A90E2; }
        .armani-theme { --theme-color: #CD7F32; }
        .libre-theme { --theme-color: #D4AF37; }
        .goodgirl-theme { --theme-color: #E31E24; }

        .theme-text { color: var(--theme-color) !important; }

        @media (max-width: 900px) { .details-section, .details-section.reverse { flex-direction: column; padding: 40px 5%; } .product-img-main { width: 85vw; } }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-master-wrapper goodgirl-theme">
        
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video"><source src="assets/goodgirl.mp4" type="video/mp4"></video>
            <div class="hero-content">
                <img src="assets/goodgirl-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Playfair Display', serif; font-size: 3rem;">Good Girl Glam</h2>
            </div>
        </section>

        <section class="details-section">
            <div class="image-side"><img src="assets/gg-detail-1.jpg" class="side-img"></div>
            <div class="text-side">
                <h3 class="theme-text">The Fragrance</h3>
                <p class="desc-text">
                    Very Good Girl Glam Parfum showcases intense cherry top notes echoed in its shimmering stiletto bottle. Upcycled rose water amplifies the feminine heart of the fragrance, elevating it from an eau de parfum to a concentrated parfum, while a base of sustainably sourced vetiver and vanilla bourbon intensify its depth and lend contrast.
                </p>
                <ul class="specs-list">
                    <li><b>For:</b> Her</li>
                    <li><b>She Is:</b> Captivating & Bold</li>
                    <li><b>Occasion:</b> Day & Night</li>
                    <li><b>Olfactive Family:</b> Floral Woody Amber</li>
                    <li><b>The Fragrance:</b> Exuberant & Unique</li>
                </ul>
            </div>
        </section>

        <section class="details-section reverse">
            <div class="image-side"><img src="assets/gg-detail-2.jpg" class="side-img"></div>
            <div class="text-side">
                <h3 class="theme-text">The Bottle & Ingredients</h3>
                <p class="desc-text" style="margin-bottom: 20px;">
                    Very Good Girl Glam Parfum elevates the iconic Good Girl flacon with its glossy cherry-red stiletto, drenched in a dazzling cascade of glitter - a spectacular expression of femininity.
                </p>
                <div class="desc-text">
                    <p><b>Top Ingredients:</b> Black Cherry, Rose, Vanilla Bourbon</p>
                    <p><b>Top Notes:</b> Cherry & Bitter Almond</p>
                    <p><b>Heart Notes:</b> Rose & Ambrette Seeds</p>
                    <p><b>Bottom Notes:</b> Rose, Ambrette Seeds & Tonka Bean</p>
                    <hr style="margin: 20px auto; width: 30%; border: 0.5px solid rgba(227,30,36,0.3);">
                    <p style="font-size: 0.8rem; opacity: 0.6; font-style: italic;">
                        *Top notes: First impression, last 5-15 mins.<br>
                        *Heart notes: Full character, last 20-60 mins.<br>
                        *Base notes: The underlying aroma, lingers up to 6 hours.
                    </p>
                </div>
            </div>
        </section>

        <section class="form-container">
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="priority-msg theme-text">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p>
            </form>
        </section>
    </div>

    </body>
</html>
