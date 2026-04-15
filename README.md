<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Experience</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Bodoni+Moda:ital,wght@1,600&family=Montserrat:wght@300;400;600&family=Playfair+Display:ital,wght@1,500&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        
        /* القسم الرئيسي: الفيديو والقرعة */
        .hero-section {
            height: 100vh; width: 100%; position: relative;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            scroll-snap-align: start;
        }

        .bg-video {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            z-index: 1; object-fit: cover; filter: brightness(0.4);
        }

        .hero-content { position: relative; z-index: 10; text-align: center; }
        
        .product-img-main {
            width: 70vw; max-width: 350px; 
            filter: drop-shadow(0px 20px 50px rgba(0,0,0,1));
            margin-bottom: 20px;
        }

        /* أقسام التفاصيل (اليمين واليسار) */
        .details-section {
            min-height: 80vh; width: 100%; display: flex; align-items: center;
            padding: 80px 5%; gap: 40px; background: #080808;
        }

        .details-section.reverse { flex-direction: row-reverse; background: #000; }

        .text-side { flex: 1; text-align: center; padding: 20px; }
        .image-side { flex: 1; display: flex; justify-content: center; }
        
        .side-img { 
            width: 100%; max-width: 400px; border-radius: 4px; 
            filter: grayscale(20%) brightness(0.8);
        }

        h3 { font-family: 'Playfair Display', serif; font-size: 2.2rem; margin-bottom: 25px; color: #D4AF37; }
        .desc-text { 
            font-size: 1rem; line-height: 1.8; color: #ccc; 
            max-width: 500px; margin: 0 auto; text-align: center; 
        }

        .specs-list { list-style: none; margin-top: 20px; }
        .specs-list li { margin: 10px 0; font-size: 0.9rem; letter-spacing: 1px; }
        .specs-list b { color: #fff; display: block; margin-bottom: 2px; }

        /* فورم الحجز (تحت في الأخير) */
        .form-container {
            padding: 60px 5%; text-align: center; background: linear-gradient(to bottom, #000, #080808);
        }

        .glass-form {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
            padding: 40px; border-radius: 20px; border: 1px solid rgba(255,255,255,0.1);
            max-width: 450px; margin: 0 auto;
            opacity: 0; transform: translateY(30px);
            animation: formAppear 1s ease forwards; animation-delay: 2s;
        }

        @keyframes formAppear { to { opacity: 1; transform: translateY(0); } }

        .input-field {
            width: 100%; background: rgba(255,255,255,0.07); border: none;
            padding: 15px; margin-bottom: 15px; border-radius: 10px; color: #fff; text-align: center;
        }

        .order-btn {
            background: #fff; color: #000; width: 100%; padding: 18px;
            border-radius: 10px; font-weight: 600; cursor: pointer; border: none;
            text-transform: uppercase; letter-spacing: 2px;
        }

        .batch-info { font-size: 0.75rem; color: #aaa; margin-top: 15px; }

        @media (max-width: 768px) {
            .details-section, .details-section.reverse { flex-direction: column; padding: 40px 5%; }
            h3 { font-size: 1.8rem; }
        }
    </style>
</head>
<body>

    <div id="good-girl-section">
        
        <section class="hero-section">
            <video autoplay muted loop playsinline class="bg-video">
                <source src="assets/goodgirl.mp4" type="video/mp4">
            </video>
            <div class="hero-content">
                <img src="assets/goodgirl-bottle.png" class="product-img-main">
                <h2 style="font-family: 'Playfair Display', serif; font-size: 3rem; letter-spacing: 5px;">Good Girl Glam</h2>
            </div>
        </section>

        <section class="details-section">
            <div class="image-side">
                <img src="assets/gg-detail-1.jpg" class="side-img" alt="The Fragrance">
            </div>
            <div class="text-side">
                <h3>The Fragrance</h3>
                <p class="desc-text">
                    Very Good Girl Glam Parfum showcases intense cherry top notes echoed in its shimmering stiletto bottle. 
                    Upcycled rose water amplifies the feminine heart of the fragrance, while a base of sustainably sourced vetiver and vanilla bourbon intensify its depth.
                </p>
                <ul class="specs-list">
                    <li><b>For:</b> Her</li>
                    <li><b>She Is:</b> Captivating & Bold</li>
                    <li><b>Olfactive Family:</b> Floral Woody Amber</li>
                </ul>
            </div>
        </section>

        <section class="details-section reverse">
            <div class="image-side">
                <img src="assets/gg-detail-2.jpg" class="side-img" alt="The Ingredients">
            </div>
            <div class="text-side">
                <h3>The Ingredients</h3>
                <div class="desc-text">
                    <p><b>Top Notes:</b> Cherry & Bitter Almond</p>
                    <p><b>Heart Notes:</b> Rose & Ambrette Seeds</p>
                    <p><b>Bottom Notes:</b> Vanilla Bourbon & Tonka Bean</p>
                    <hr style="margin: 20px auto; width: 50%; border: 0.5px solid rgba(212,175,55,0.3);">
                    <p style="font-size: 0.8rem; font-style: italic; opacity: 0.7;">
                        *Base notes: The underlying aroma throughout the wear of the perfume. Lingers the longest on skin (up to 6 hours).
                    </p>
                </div>
            </div>
        </section>

        <section class="form-container">
            <form class="glass-form">
                <h3 style="font-size: 1.5rem;">تأكيد الحجز المسبق</h3>
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="batch-info">تم حجز 14 مكان من أصل 20 في هذه الدفعة</p>
            </form>
        </section>

    </div>

</body>
</html>
