<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lisseur Pro - شعر ناعم في دقائق</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* الألوان والستايل */
        :root {
            --main-pink: #fce4ec;
            --dark-pink: #f06292;
            --gold: #d4af37;
            --black: #212121;
        }

        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #fff;
            color: var(--black);
            overflow-x: hidden;
        }

        /* تحذير: هاد الكود غيغطي الصفحة كاملة باش تجي طويلة */
        section { padding: 60px 20px; text-align: center; }

        .promo-bar { background: var(--black); color: #fff; padding: 10px; font-weight: bold; font-size: 14px; position: sticky; top: 0; z-index: 1000; }

        .hero-img { width: 100%; max-width: 500px; border-radius: 20px; margin-top: 20px; }

        h1 { color: var(--dark-pink); font-size: 1.8rem; margin-top: 10px; }

        /* الأقسام الزايدة باش تطوال الصفحة */
        .how-to-use { background: var(--main-pink); }
        .steps { display: flex; flex-direction: column; gap: 20px; text-align: right; max-width: 500px; margin: 0 auto; }
        .step { background: #fff; padding: 15px; border-radius: 10px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); }

        .guarantee { border: 2px solid var(--gold); margin: 20px; padding: 20px; border-radius: 15px; }

        .price-tag { font-size: 30px; color: #e91e63; font-weight: bold; margin: 20px 0; }
        .old-price { text-decoration: line-through; color: #999; font-size: 20px; }

        /* زر الطلب العائم */
        .sticky-footer {
            position: fixed;
            bottom: 0;
            width: 100%;
            background: #fff;
            padding: 15px;
            box-shadow: 0 -5px 15px rgba(0,0,0,0.1);
            display: flex;
            justify-content: center;
            z-index: 10000;
        }

        .cta-btn {
            background: #4caf50; /* لون أخضر للواتساب */
            color: white;
            padding: 15px 50px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.2rem;
            box-shadow: 0 4px 15px rgba(76, 175, 80, 0.4);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .spacer { height: 100px; } /* فراغ باش ما يتغطاش المحتوى بالزر */
    </style>
</head>
<body>

    <div class="promo-bar">توصيل مجاني لجميع المدن + الدفع عند الاستلام 🚚</div>

    <section>
        <h1>صالون التجميل في منزلك مع المشط الاحترافي ✨</h1>
        <p>وفري وقتك وفلوسك وحصلي على نتيجة مبهرة في 5 دقائق فقط</p>
        <img src="https://via.placeholder.com/500x500" class="hero-img" alt="Product">
        
        <div class="price-tag">
            <span class="old-price">499 درهم</span> <br>
            249 درهم فقط!
        </div>
    </section>

    <section style="background: #fafafa;">
        <h2>علاش آلاف النساء كيختارو هاد المنتج؟ 🤔</h2>
        <div class="steps">
            <div class="step">✅ <strong>حماية فائقة:</strong> تقنية السيراميك اللي كتحمي شعرك من الحرق.</div>
            <div class="step">✅ <strong>سرعة خيالية:</strong> كيسخن في 30 ثانية فقط.</div>
            <div class="step">✅ <strong>نتيجة دايما:</strong> كيبقى شعرك رطب وحريري النهار كامل.</div>
        </div>
    </section>

    <section class="how-to-use">
        <h2>طريقة الاستعمال بسيطة بزااف 💆‍♀️</h2>
        <p>1. نشفي شعرك مزيان.</p>
        <p>2. اختاري الحرارة اللي كتناسبك.</p>
        <p>3. دوزي المشط بكل سهولة وشوفي الفرق!</p>
    </section>

    <section class="guarantee">
        <img src="https://cdn-icons-png.flaticon.com/512/9333/9333991.png" width="60" alt="Icon">
        <h3>ضمان لمدة 12 شهر</h3>
        <p>حنا واثقين في جودة المنتجات ديالنا، إلا كان فيه أي مشكل كنعوضوك!</p>
    </section>

    <section>
        <h2>شنو قالو البنات اللي جربوه؟ ⭐⭐⭐⭐⭐</h2>
        <p>"والله حتى هناني من السيشوار، خفيف وسهل في الاستعمال." - <strong>خديجة، الرباط</strong></p>
        <hr>
        <p>"وصلني دغيا، والتعامل ديالكم راقي بزاف. شكراً على المصداقية." - <strong>سلمى، أكادير</strong></p>
    </section>

    <div class="spacer"></div>

    <div class="sticky-footer">
        <a href="https://wa.me/2126XXXXXXXX" class="cta-btn">طلب عبر الواتساب الآن</a>
    </div>

</body>
</html>
