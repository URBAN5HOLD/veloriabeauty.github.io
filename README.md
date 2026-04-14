<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria Fragrance | الحقيقة في كل رشة</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --gold: #D4AF37;
            --deep-black: #050505;
            --soft-white: #f4f4f4;
            --transition: all 0.8s cubic-bezier(0.2, 1, 0.3, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            background-color: var(--deep-black);
            color: var(--soft-white);
            font-family: 'Montserrat', sans-serif;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* Logo Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 30px;
            z-index: 1000;
            text-align: center;
            background: linear-gradient(to bottom, rgba(0,0,0,0.8), transparent);
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            letter-spacing: 5px;
            color: var(--gold);
            text-decoration: none;
            text-transform: uppercase;
        }

        /* Full Screen Section */
        .perfume-section {
            position: relative;
            height: 100vh;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: flex-start;
            padding: 0 10%;
            overflow: hidden;
            border-bottom: 1px solid #1a1a1a;
        }

        /* Background Video/Image */
        .bg-media {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            object-fit: cover;
            filter: brightness(0.4);
        }

        /* Content Animation */
        .content {
            max-width: 500px;
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .perfume-section.active .content {
            opacity: 1;
            transform: translateY(0);
        }

        h2 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            color: var(--gold);
            margin-bottom: 15px;
            text-transform: uppercase;
        }

        .description {
            font-weight: 200;
            font-size: 1.1rem;
            letter-spacing: 1px;
            margin-bottom: 30px;
        }

        /* Form Design */
        .order-box {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(15px);
            padding: 25px;
            border: 1px solid rgba(212, 175, 55, 0.2);
            border-radius: 2px;
        }

        input {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            background: transparent;
            border: none;
            border-bottom: 1px solid #444;
            color: white;
            font-family: 'Montserrat', sans-serif;
            outline: none;
        }

        input:focus { border-bottom-color: var(--gold); }

        .btn-submit {
            width: 100%;
            padding: 15px;
            background: var(--gold);
            color: black;
            border: none;
            font-weight: 600;
            text-transform: uppercase;
            cursor: pointer;
            margin-top: 15px;
            transition: 0.4s;
        }

        .btn-submit:hover {
            background: white;
            letter-spacing: 2px;
        }

        /* Mobile Adjustments */
        @media (max-width: 768px) {
            h2 { font-size: 2.2rem; }
            .perfume-section { padding: 0 5%; justify-content: center; }
            .content { text-align: center; }
        }
    </style>
</head>
<body>

    <header>
        <a href="#" class="logo">VELOORIA</a>
    </header>

    <section class="perfume-section active" id="sauvage">
        <video autoplay muted loop class="bg-media">
            <source src="رابط_فيديو_ديور_هنا" type="video/mp4">
        </video>
        <div class="content">
            <h2>Sauvage Elixir</h2>
            <p class="description">مستخلص نقي من قلب الطبيعة. الأصالة التي لا تُقهر في عبوة 10ml.</p>
            <div class="order-box">
                <form id="form-sauvage">
                    <input type="text" placeholder="الاسم الكامل" required>
                    <input type="tel" placeholder="رقم الهاتف" required>
                    <input type="text" placeholder="المدينة" required>
                    <button type="submit" class="btn-submit">تأكيد الحجز - 319 DH</button>
                </form>
            </div>
        </div>
    </section>

    <section class="perfume-section" id="swy">
        <img src="رابط_صورة_ارماني_هنا" class="bg-media" alt="SWY">
        <div class="content">
            <h2>Intensely You</h2>
            <p class="description">دفء الفانيليا وجاذبية العنبر. عطر الرجل العصري.</p>
            <div class="order-box">
                <form id="form-swy">
                    <input type="text" placeholder="الاسم الكامل" required>
                    <input type="tel" placeholder="رقم الهاتف" required>
                    <input type="text" placeholder="المدينة" required>
                    <button type="submit" class="btn-submit">تأكيد الحجز - 289 DH</button>
                </form>
            </div>
        </div>
    </section>

    <script>
        // أنيميشن عند الهبوط (Scroll Observer)
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, { threshold: 0.5 });

        document.querySelectorAll('.perfume-section').forEach(section => {
            observer.observe(section);
        });
    </script>

</body>
</html>
