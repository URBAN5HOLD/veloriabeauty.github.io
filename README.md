<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lisseur Pro - عرض محدود</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
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
            text-align: center; /* هادي باش كلشي يجي في الوسط */
        }

        /* شريط التوصيل - الوسط */
        .promo-bar { 
            background: var(--black); 
            color: #fff; 
            padding: 12px; 
            font-weight: bold; 
            font-size: 15px; 
            display: flex;
            justify-content: center;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        /* العد التنازلي */
        .timer-container {
            background: #fff3f3;
            padding: 15px;
            margin: 20px 0;
            border: 1px solid #ffcdd2;
        }
        #timer {
            font-size: 24px;
            font-weight: bold;
            color: #d32f2f;
        }

        .hero-img { width: 100%; max-width: 450px; border-radius: 15px; margin: 20px auto; display: block; }

        .price-tag { font-size: 28px; margin: 20px 0; }
        .discount-badge { background: #ff5252; color: #fff; padding: 5px 15px; border-radius: 5px; font-size: 18px; }

        /* قسم الصور مع التفسير */
        .product-info { padding: 40px 20px; }
        .info-card { margin-bottom: 40px; }
        .info-card img { width: 100%; max-width: 400px; border-radius: 10px; margin-bottom: 15px; }
        .info-card p { font-size: 1.1rem; color: #555; }

        /* التعاليق - الشكل الواقعي */
        .reviews-section { background: #fafafa; padding: 50px 20px; }
        .review-card {
            background: #fff;
            padding: 20px;
            border-radius: 12px;
            margin: 15px auto;
            max-width: 500px;
            text-align: right;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            display: flex;
            gap: 15px;
            align-items: flex-start;
        }
        .profile-img { width: 50px; height: 50px; border-radius: 50%; background: #eee; object-fit: cover; }
        .stars { color: #ffc107; font-size: 14px; margin-bottom: 5px; }
        .review-name { font-weight: bold; font-size: 16px; display: block; }
        .review-text { color: #444; font-size: 14px; margin-top: 5px; }

        /* زر الطلب - الوسط */
        .sticky-footer {
            position: fixed;
            bottom: 0;
            width: 100%;
            background: #fff;
            padding: 15px 0;
            box-shadow: 0 -5px 15px rgba(0,0,0,0.1);
            z-index: 10000;
            display: flex;
            justify-content: center;
        }

        .cta-btn {
            background: #25D366; /* لون الواتساب */
            color: white;
            padding: 15px 60px;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.3rem;
            animation: pulse 2s infinite;
        }

        @keyframes pulse { 0% {transform: scale(1);} 50% {transform: scale(1.05);} 100% {transform: scale(1);} }
        .spacer { height: 100px; }
    </style>
</head>
<body>

    <div class="promo-bar">🚚 توصيل مجاني + الدفع عند الاستلام 🤝</div>

    <div class="timer-container">
        <p style="margin:0; font-weight: bold;">سالي الخصم ديال 50% فـ:</p>
        <div id="timer">05:00:00</div>
    </div>

    <section>
        <h1 style="color: var(--dark-pink); padding: 0 15px;">احصلي على شعر حريري في أقل من 5 دقائق ✨</h1>
        <img src="https://via.placeholder.com/500x500" class="hero-img" alt="Product Image">
        <div class="price-tag">
            <span style="text-decoration: line-through; color: #999; font-size: 20px;">499 درهم</span><br>
            <strong>249 درهم فقط</strong> <span class="discount-badge">تخفيض 50%</span>
        </div>
    </section>

    <section class="product-info">
        <div class="info-card">
            <img src="https://via.placeholder.com/400x400" alt="شرح 1">
            <h3>سهل الاستعمال 💆‍♀️</h3>
            <p>بلا ما تحتاجي تمشي للصالون، هاد المشط كيسخن فـ 30 ثانية وكيسرح الشعر من الدوزة اللولة بكل سهولة.</p>
        </div>

        <div class="info-card">
            <img src="https://via.placeholder.com/400x400" alt="شرح 2">
            <h3>حماية كاملة من الحرق 🔥</h3>
            <p>تقنية السيراميك المتطورة كتحمي شعرك من الحرارة الزايدة وكتخليه ديما كيلمع وصحي.</p>
        </div>

        <div class="info-card">
            <img src="https://via.placeholder.com/400x400" alt="شرح 3">
            <h3>مناسب لجميع أنواع الشعر 🎀</h3>
            <p>سواء كان شعرك خشن، رقيق أو مصبوغ، تقدري تختاري الحرارة اللي كتناسبك وتحصلي على نتيجة مبهرة.</p>
        </div>
    </section>

    <section class="reviews-section">
        <h2 style="color: var(--dark-pink);">شنو قالو البنات على المنتج ديالنا؟ 😍</h2>
        
        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=1" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">سناء</span>
                <p class="review-text">بصراحة واعر بزااااف، هناني من السيشوار وتمارة ديالو. شكراً بزاف ❤️</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=2" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">ليلى</span>
                <p class="review-text">وصلني اليوم، التوصيل كان سريع والمنتج جودته عالية برافو 👍</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=3" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐</div>
                <span class="review-name">مريم</span>
                <p class="review-text">زوين عجبني، غير هو تعطل عليا الليفرور شوية ولكن السلعة طوب.</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=4" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">خديجة</span>
                <p class="review-text">خديت جوج ليا ولختي، عجبنا بزااف كيسرح دغيا ومكيحرقش الشعر 🎀</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=5" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">إيمان</span>
                <p class="review-text">أحسن حاجة شريتها هاد العام، كيهني فاش كتكوني زربانة.</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=6" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐</div>
                <span class="review-name">فاطمة</span>
                <p class="review-text">ممتاز، كيرد الشعر حرير فـ 5 دقايق. كنصحكم بيه البنات.</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=7" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">كوثر</span>
                <p class="review-text">تبارك الله عليكم، السلعة واصلة مقادة وكيفما فالتصاور ✨</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=8" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">حنان</span>
                <p class="review-text">عجبني بزااف وخاصة أنه خفيف فاليد، شكراً ليكم.</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=9" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐</div>
                <span class="review-name">سلمى</span>
                <p class="review-text">تجربة زوينة، النتيجة عجباتني بزااف 😍</p>
            </div>
        </div>

        <div class="review-card">
            <img src="https://i.pravatar.cc/150?u=10" class="profile-img">
            <div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">نادية</span>
                <p class="review-text">التعامل ديالكم راقي والمنتج يستاهل كل درهم 👌</p>
            </div>
        </div>
    </section>

    <div class="spacer"></div>

    <div class="sticky-footer">
        <a href="https://wa.me/212691444558" class="cta-btn">اطلبي الآن عبر الواتساب</a>
    </div>

    <script>
        function startTimer(duration, display) {
            var timer = duration, hours, minutes, seconds;
            setInterval(function () {
                hours = parseInt(timer / 3600, 10);
                minutes = parseInt((timer % 3600) / 60, 10);
                seconds = parseInt(timer % 60, 10);

                hours = hours < 10 ? "0" + hours : hours;
                minutes = minutes < 10 ? "0" + minutes : minutes;
                seconds = seconds < 10 ? "0" + seconds : seconds;

                display.textContent = hours + ":" + minutes + ":" + seconds;

                if (--timer < 0) {
                    timer = duration;
                }
            }, 1000);
        }

        window.onload = function () {
            var fiveHours = 60 * 60 * 5,
                display = document.querySelector('#timer');
            startTimer(fiveHours, display);
        };
    </script>

</body>
</html>
