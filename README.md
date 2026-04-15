<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria | تجربة الحجز الملكي</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; }

        .logo-fixed {
            position: fixed; top: 25px; left: 50%; transform: translateX(-50%);
            z-index: 1000; font-family: 'Playfair Display';
            font-size: 1.4rem; letter-spacing: 10px; color: #fff;
        }

        .section {
            height: 100vh; width: 100%; display: flex; flex-direction: column;
            align-items: center; justify-content: center;
            position: relative; scroll-snap-align: start; overflow: hidden;
        }

        .bg-wrapper { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; }
        .bg-wrapper video { width: 100%; height: 100%; object-fit: cover; filter: brightness(0.5); }

        .content { position: relative; z-index: 10; text-align: center; width: 90%; max-width: 450px; }

        .product-img {
            width: 150px; height: auto; margin-bottom: 10px;
            filter: drop-shadow(0px 10px 20px rgba(0,0,0,0.9));
        }

        /* تعديل الفورم باش تبان واضحة */
        .glass-form {
            background: rgba(0, 0, 0, 0.6); /* خلفية داكنة شوية باش تبان واضحة */
            backdrop-filter: blur(20px); 
            -webkit-backdrop-filter: blur(20px);
            padding: 30px; 
            border: 1px solid rgba(212, 175, 55, 0.4); /* إطار ذهبي خفيف */
            border-radius: 8px;
            
            /* أنيميشن الظهور */
            opacity: 0; 
            transform: translateY(20px);
            animation: showForm 1s cubic-bezier(0.4, 0, 0.2, 1) forwards;
            animation-delay: 4s; /* كادوز 4 ثواني عاد كتبان */
        }

        @keyframes showForm {
            to { opacity: 1; transform: translateY(0); }
        }

        h2 { font-family: 'Playfair Display', serif; font-size: 2.2rem; color: #fff; margin-bottom: 15px; letter-spacing: 2px; }

        input {
            width: 100%; background: rgba(255,255,255,0.05); border: none; 
            border-bottom: 1px solid rgba(255,255,255,0.3);
            color: #fff; padding: 12px; margin-bottom: 12px; 
            outline: none; font-family: 'Montserrat';
        }
        input:focus { border-bottom-color: #D4AF37; background: rgba(255,255,255,0.1); }
        input::placeholder { color: rgba(255,255,255,0.6); font-style: italic; }

        .order-btn {
            background: #fff; color: #000; border: none; padding: 15px; width: 100%;
            font-weight: 600; text-transform: uppercase; letter-spacing: 2px;
            cursor: pointer; transition: 0.4s; margin-top: 5px;
        }
        .order-btn:hover { background: #D4AF37; color: #fff; }

        .priority-tag { font-size: 0.75rem; color: #D4AF37; margin-top: 15px; font-weight: 600; }
        .batch-alert { font-size: 0.7rem; color: rgba(255,255,255,0.8); margin-top: 5px; }

        @media (max-width: 768px) { h2 { font-size: 1.8rem; } .product-img { width: 120px; } }
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
                <h2>Sauvage Elixir</h2>
                <input type="text" placeholder="تفضل بوضع اسمك يا سيدي..." required>
                <input type="tel" placeholder="رقم هاتفك الخاص..." required>
                <input type="text" placeholder="مدينتكم الموقرة..." required>
                <button type="submit" class="order-btn">احجز الآن | 319 DH</button>
                <p class="priority-tag">📅 الدفعة الأولى: قيد التحضير اليدوي</p>
                <p class="batch-alert">تم حجز 17 مكان من أصل 20 في هذه الدفعة</p>
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
                <h2>Intensely You</h2>
                <input type="text" placeholder="تفضل بوضع اسمك يا سيدي..." required>
                <input type="tel" placeholder="رقم هاتفك الخاص..." required>
                <input type="text" placeholder="مدينتكم الموقرة..." required>
                <button type="submit" class="order-btn">احجز الآن | 289 DH</button>
                <p class="priority-tag">📅 الدفعة الأولى: قيد التحضير اليدوي</p>
                <p class="batch-alert">المقاعد المتبقية: 3 فقط</p>
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
                <h2>YSL Libre</h2>
                <input type="text" placeholder="اسمكِ سيدتي الجميلة..." required>
                <input type="tel" placeholder="رقم هاتفكِ الخاص..." required>
                <input type="text" placeholder="مدينتكم الموقرة..." required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="priority-tag">👑 أسبقية التوصيل حسب ترتيب الحجز</p>
                <p class="batch-alert">المقاعد المتبقية في هذه الدفعة: 5 فقط</p>
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
                <h2>Good Girl Glam</h2>
                <input type="text" placeholder="اسمكِ سيدتي الجميلة..." required>
                <input type="tel" placeholder="رقم هاتفكِ الخاص..." required>
                <input type="text" placeholder="مدينتكم الموقرة..." required>
                <button type="submit" class="order-btn">احجز الآن | 299 DH</button>
                <p class="priority-tag">📅 الدفعة قيد التجهيز</p>
                <p class="batch-alert">احجزي مكانكِ قبل اكتمال العدد</p>
            </form>
        </div>
    </section>

</body>
</html>
