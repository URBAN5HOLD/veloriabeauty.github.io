<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Fragrance</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Playfair+Display:ital,wght@0,700;1,400&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* 1. تصفير كاع الهوامش باش يبدا الفيديو من راس الصفحة */
        * { 
            margin: 0; 
            padding: 0; 
            box-sizing: border-box; 
            text-decoration: none; 
            border: none; 
            outline: none;
        }

        body, html {
            width: 100%;
            height: 100%;
            background-color: #000;
            color: #fff;
            font-family: 'Montserrat', sans-serif;
            overflow-x: hidden;
        }

        .logo-fixed { 
            position: fixed; 
            top: 25px; 
            left: 50%; 
            transform: translateX(-50%); 
            z-index: 1000; 
            font-family: 'Cinzel', serif; 
            font-size: 1.5rem; 
            letter-spacing: 12px; 
            color: #fff; 
            text-shadow: 0 0 15px rgba(0,0,0,0.8); 
        }

        .product-section { width: 100%; position: relative; }

        /* 2. الـ Video Header: لاصق لفوق */
        .v-header { 
            height: 100vh; 
            width: 100%; 
            margin: 0; 
            padding: 0; 
            overflow: hidden; 
            position: relative;
        }
        .bg-v { 
            width: 100%; 
            height: 100%; 
            object-fit: cover; 
            filter: brightness(0.5); 
            display: block; /* كيحيد الفراغ الصغير اللي كيكون تحت الفيديو */
        }

        /* 3. Central Bottle Section */
        .bottle-center { text-align: center; padding: 100px 0; background: #000; }
        .img-bottle { width: 85vw; max-width: 420px; filter: drop-shadow(0 0 50px var(--glow)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 3.2rem; margin-top: 20px; letter-spacing: 8px; }

        /* 4. Wide Rows: الصور أقصى اليمين وأقصى اليسار */
        .row { 
            display: flex; 
            align-items: center; 
            width: 100%; 
            min-height: 600px; 
            margin: 0; /* حيدنا المارجن باش نتحكمو في الفراغ داخليا */
            padding: 50px 0;
        }
        .row.rev { flex-direction: row-reverse; }

        /* الصندوق ديال الصورة: لاصق في الحافة */
        .img-box { width: 50%; display: flex; }
        .row .img-box { justify-content: flex-start; } /* الصورة الأولى أقصى اليسار */
        .row.rev .img-box { justify-content: flex-end; } /* الصورة الثانية أقصى اليمين */
        
        .img-box img { 
            width: 100%; 
            max-width: 700px; 
            height: auto; 
            filter: brightness(0.8); 
            object-fit: cover;
        }

        /* الصندوق ديال النص */
        .txt-box { 
            width: 50%; 
            padding: 0 6%; 
            position: relative; 
            z-index: 5; 
            text-align: center; 
        }
        
        /* تقوية الانعكاس الضبابي الملون */
        .glow-effect { 
            position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); 
            width: 130%; height: 130%; 
            background: radial-gradient(circle, var(--glow) 0%, transparent 75%); 
            opacity: 0.45; /* جهدت اللون ورا الكتابة */
            filter: blur(100px); 
            z-index: -1; 
        }

        h3 { font-family: 'Playfair Display', serif; font-size: 2.8rem; color: var(--color); margin-bottom: 25px; text-transform: uppercase; }
        .desc-full { font-size: 1.05rem; line-height: 1.9; color: #eee; text-align: center; }

        .specs-list { margin-top: 25px; list-style: none; display: inline-block; text-align: left; }
        .specs-list li { margin-bottom: 10px; font-size: 0.95rem; }
        .specs-list b { color: var(--color); letter-spacing: 1px; }
        
        .tech-notes { font-size: 0.85rem; color: #888; margin-top: 30px; line-height: 1.7; font-style: italic; border-top: 1px solid rgba(255,255,255,0.1); padding-top: 20px; max-width: 500px; margin-left: auto; margin-right: auto; }

        /* Form */
        .f-wrap { padding: 100px 0; text-align: center; background: #000; }
        .f-glass { max-width: 480px; margin: 0 auto; padding: 40px; }
        .in-f { width: 100%; padding: 20px; margin-bottom: 12px; background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.1); color: #fff; border-radius: 4px; text-align: center; }
        .btn-f { width: 100%; padding: 22px; background: #fff; color: #000; font-weight: 800; cursor: pointer; letter-spacing: 2px; border-radius: 4px; transition: 0.4s; }
        .btn-f:hover { transform: translateY(-5px); box-shadow: 0 10px 30px rgba(255,255,255,0.2); }
        .pri-txt { color: var(--color); margin-top: 20px; font-weight: 600; font-size: 0.9rem; }

        /* Themes */
        .gg-t { --glow: #b30000; --color: #E31E24; }
        .sauv-t { --glow: #0033cc; --color: #4A90E2; }
        .arman-t { --glow: #8b4513; --color: #CD7F32; }
        .libre-t { --glow: #b8860b; --color: #D4AF37; }

        @media (max-width: 1000px) { 
            .row, .row.rev { flex-direction: column; text-align: center; } 
            .img-box, .txt-box { width: 100%; padding: 30px 5%; }
            .img-box { justify-content: center !important; }
        }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div class="product-section gg-t">
        
        <div class="v-header">
            <video autoplay muted loop playsinline class="bg-v">
                <source src="assets/goodgirl.mp4" type="video/mp4">
            </video>
        </div>

        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
        </div>
        
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>The Fragrance</h3>
                <p class="desc-full">
                    The sweet, alluring qualities of jasmine bring Good Girl a bright femininity. Richly fragrant cocoa and intoxicating tonka express Good Girl’s mysterious side, while almond and coffee bring notes of bold vibrancy.
                    <br><br>
                    Combining haute couture aesthetics with technical expertise, the iconic Good Girl stiletto reflects the powerful women who inspire its silhouette.
                </p>
                <ul class="specs-list">
                    <li><b>For:</b> Her</li>
                    <li><b>She Is:</b> Seductive & Strong</li>
                    <li><b>Occasion:</b> Day & Night</li>
                    <li><b>Olfactive Family:</b> AMBERY Ambery Floral</li>
                    <li><b>The Fragrance:</b> Powerful & Provocative</li>
                </ul>
            </div>
        </div>

        <div class="row rev">
            <div class="img-box"><img src="assets/gg-detail-right.jpg"></div>
            <div class="txt-box">
                <div class="glow-effect"></div>
                <h3>Notes & Ingredients</h3>
                <div class="desc-full">
                    <p><b>Key Ingredients:</b> Jasmine, Tuberose, Tonka Bean</p>
                    <p><b>Top Notes:</b> Almond</p>
                    <p><b>Heart Notes:</b> Jasmine Sambac & Tuberose Chrystal</p>
                    <p><b>Bottom Notes:</b> Tonka Bean & Cocoa</p>
                </div>
                <div class="tech-notes">
                    <p>*Top notes: First impression of a perfume, last 5-15 minutes after applying to skin.</p>
                    <p>*Heart notes: Start to come through as the top notes fade, last approximately 20-60 minutes.</p>
                    <p>*Base notes: The underlying aroma throughout the wear of the perfume. Lingers the longest on skin (up to 6 hours) after the other notes have faded.</p>
                </div>
            </div>
        </div>

        <div class="f-wrap">
            <form class="f-glass">
                <input type="text" placeholder="الاسم الكامل" class="in-f" required>
                <input type="tel" placeholder="رقم الهاتف" class="in-f" required>
                <input type="text" placeholder="المدينة والعنوان" class="in-f" required>
                <button type="submit" class="btn-f">احجز الآن | 299 DH</button>
                <p class="pri-txt" dir="rtl">أولوية المعالجة والشحن تمنح لأسبقية الحجز</p>
            </form>
        </div>
    </div>

</body>
</html>
