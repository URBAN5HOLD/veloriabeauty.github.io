<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | Luxury Fragrance Experience</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Bodoni+Moda:ital,wght@1,600&family=Montserrat:wght@700;800&family=Playfair+Display:ital,wght@1,700&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; }

        .logo-fixed {
            position: fixed; top: 30px; left: 50%; transform: translateX(-50%);
            z-index: 1000; font-family: 'Cinzel', serif;
            font-size: 1.5rem; letter-spacing: 12px; color: #fff;
        }

        .section {
            height: 100vh; width: 100%; display: flex; flex-direction: column;
            align-items: center; justify-content: space-around;
            position: relative; scroll-snap-align: start; overflow: hidden; padding-top: 50px;
        }

        .bg-wrapper { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; }
        .bg-wrapper video { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.4); }

        .content { position: relative; z-index: 10; text-align: center; width: 100%; max-width: 500px; }

        /* حجم القرعة الكبير والفخم */
        .product-img {
            width: 80%; max-width: 350px; height: auto;
            margin-bottom: -15px;
            filter: drop-shadow(0px 20px 50px rgba(0,0,0,1));
        }

        /* تصميم الفورم الحديث (Modern Rounded) */
        .glass-form {
            background: rgba(255, 255, 255, 0.06);
            backdrop-filter: blur(20px); -webkit-backdrop-filter: blur(20px);
            padding: 30px 25px; border-radius: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            width: 90%; margin: 0 auto;
            opacity: 0; transform: translateY(30px);
            animation: fadeIn 1s ease forwards; animation-delay: 4s;
        }

        @keyframes fadeIn { to { opacity: 1; transform: translateY(0); } }

        /* تنسيقات العناوين حسب كل ماركة */
        .dior-font { font-family: 'Cinzel', serif; font-size: 2.6rem; letter-spacing: 5px; margin-bottom: 10px; }
        .ysl-font { font-family: 'Bodoni Moda', serif; font-size: 3.2rem; font-style: italic; margin-bottom: 10px; }
        .armani-font { font-family: 'Montserrat', sans-serif; font-weight: 800; font-size: 2.2rem; text-transform: uppercase; letter-spacing: -1px; margin-bottom: 10px; }
        .ch-font { font-family: 'Playfair Display', serif; font-size: 2.8rem; font-style: italic; margin-bottom: 10px; }

        .input-field {
            width: 100%; background: rgba(255,255,255,0.08); border: none;
            border-radius: 15px; color: #fff; padding: 15px; margin-bottom: 12px;
            outline: none; font-size: 0.9rem; text-align: center;
        }

        .order-btn {
            background: #fff; color: #000; border: none; padding: 18px; width: 100%;
            border-radius: 15px; font-weight: 600; text-transform: uppercase; 
            letter-spacing: 2px; cursor: pointer; transition: 0.4s;
        }
        .order-btn:hover { background: #D4AF37; color: #fff; transform: scale(1.02); }

        .status-line { font-size: 0.8rem; color: #fff; margin-top: 15px; opacity: 0.9; }
        .batch-line { font-size: 0.75rem; color: #aaa; margin-top: 5px; }

    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/sauvage.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <img src="assets/sauvage-bottle.png" class="product-img">
            <form class="glass-form">
                <h2 class="dior-font">SAUVAGE</h2>
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 319 DH</button>
                <p class="status-line">الدفعة الأولى قيد التحضير</p>
                <p class="batch-line">تم حجز 14 مكان من أصل 20 حتى الآن</p>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/armani.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <img src="assets/armani-bottle.png" class="product-img">
            <form class="glass-form">
                <h2 class="armani-font">STRONGER WITH YOU</h2>
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 289 DH</button>
                <p class="status-line">أسبقية التوصيل للحجز المسبق</p>
                <p class="batch-line">تم حجز 14 مكان من أصل 20</p>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/libre.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <img src="assets/libre-bottle.png" class="product-img">
            <form class="glass-form">
                <h2 class="ysl-font">Libre</h2>
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="status-line">إصدار محدود - حجز مسبق</p>
                <p class="batch-line">تم حجز 14 مكان من أصل 20</p>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/goodgirl.mp4" type="video/mp4"></video>
        </div>
        <div class="content">
            <img src="assets/goodgirl-bottle.png" class="product-img">
            <form class="glass-form">
                <h2 class="ch-font">Good Girl Glam</h2>
                <input type="text" placeholder="الاسم الكامل" class="input-field" required>
                <input type="tel" placeholder="رقم الهاتف" class="input-field" required>
                <input type="text" placeholder="المدينة والعنوان" class="input-field" required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="status-line">احجزي مكانكِ في الدفعة القادمة</p>
                <p class="batch-line">تم حجز 14 مكان من أصل 20</p>
            </form>
        </div>
    </section>

</body>
</html>
