<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria Fragrance | The Core 4</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-snap-type: y mandatory; scroll-behavior: smooth; }
        body { background-color: #000; color: #fff; font-family: 'Montserrat', sans-serif; }

        .section {
            height: 100vh;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            scroll-snap-align: start;
            overflow: hidden;
        }

        /* حاوية الخلفية - الفيديو هو اللي كايعطي اللون */
        .bg-wrapper {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            z-index: 1;
        }
        
        .bg-wrapper video {
            width: 100%; height: 100%; object-fit: cover;
        }

        /* هاد الطبقة كاتخلي ألوان الفيديو تبان ولكن كاتحمي وضوح النص */
        .bg-overlay {
            position: absolute;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.3); /* شفافة بزاف باش تخلي لون المنتج يطغى */
            background: linear-gradient(to bottom, rgba(0,0,0,0.2) 0%, rgba(0,0,0,0.5) 100%);
            z-index: 2;
        }

        .content {
            position: relative;
            z-index: 10;
            text-align: center;
            width: 90%;
            max-width: 600px;
        }

        h2 { font-family: 'Playfair Display', serif; font-size: clamp(2.5rem, 8vw, 4.5rem); color: #fff; margin-bottom: 10px; text-transform: uppercase; letter-spacing: 4px; text-shadow: 2px 2px 10px rgba(0,0,0,0.5); }
        .tagline { font-size: 1.1rem; font-weight: 300; margin-bottom: 30px; letter-spacing: 1px; color: rgba(255,255,255,0.9); }

        /* فورم الحجز الزجاجية - كاتشف الألوان اللي وراها */
        .glass-form {
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        input {
            background: rgba(0, 0, 0, 0.2);
            border: none;
            border-bottom: 1px solid rgba(255, 255, 255, 0.3);
            color: #fff;
            padding: 12px;
            outline: none;
            font-family: 'Montserrat';
            transition: 0.3s;
        }
        input:focus { border-bottom-color: #D4AF37; background: rgba(0,0,0,0.4); }

        .order-btn {
            background: #fff; color: #000; border: none;
            padding: 18px; font-weight: 600; cursor: pointer;
            text-transform: uppercase; letter-spacing: 2px; transition: 0.4s;
            margin-top: 10px;
        }
        .order-btn:hover { background: #D4AF37; color: #fff; letter-spacing: 4px; }

        .logo-fixed { position: fixed; top: 25px; left: 50%; transform: translateX(-50%); z-index: 100; font-family: 'Playfair Display'; font-size: 1.4rem; letter-spacing: 8px; color: #fff; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/sauvage.mp4" type="video/mp4"></video>
            <div class="bg-overlay"></div>
        </div>
        <div class="content">
            <h2>Sauvage Elixir</h2>
            <p class="tagline">قوة الغسق.. في عبوة 10ml</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="المدينة" required>
                <button type="submit" class="order-btn">حجز الآن | 319 DH</button>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/armani.mp4" type="video/mp4"></video>
            <div class="bg-overlay"></div>
        </div>
        <div class="content">
            <h2>Intensely You</h2>
            <p class="tagline">دفء العاطفة.. في عبوة 10ml</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="المدينة" required>
                <button type="submit" class="order-btn">حجز الآن | 289 DH</button>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/libre.mp4" type="video/mp4"></video>
            <div class="bg-overlay"></div>
        </div>
        <div class="content">
            <h2>YSL Libre</h2>
            <p class="tagline">عبير الحرية.. في عبوة 10ml</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="المدينة" required>
                <button type="submit" class="order-btn">حجز الآن | 299 DH</button>
            </form>
        </div>
    </section>

    <section class="section">
        <div class="bg-wrapper">
            <video autoplay muted loop playsinline><source src="assets/goodgirl.mp4" type="video/mp4"></video>
            <div class="bg-overlay"></div>
        </div>
        <div class="content">
            <h2>Good Girl Glam</h2>
            <p class="tagline">جرأة الكرز.. في عبوة 10ml</p>
            <form class="glass-form">
                <input type="text" placeholder="الاسم الكامل" required>
                <input type="tel" placeholder="رقم الهاتف" required>
                <input type="text" placeholder="المدينة" required>
                <button type="submit" class="order-btn">حجز الآن | 299 DH</button>
            </form>
        </div>
    </section>

</body>
</html>
