<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VELORIA BEAUTY - العرض المتكامل</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --main-pink: #fff5f6;
            --dark-pink: #f06292;
            --black: #1a1a1a;
            --green-wa: #25D366;
        }
        h1 { display: none !important; }

        * { box-sizing: border-box; }
        body { font-family: 'Cairo', sans-serif; margin: 0; padding: 0; background-color: #fff; text-align: center; line-height: 1.6; color: #333; }

        .brand-header {
            padding: 20px 0;
            background-color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            border-bottom: 1px solid #f8f8f8;
        }
        .brand-logo { width: 75px; height: auto; margin-bottom: 8px; border-radius: 50%; }
        .brand-name { font-size: 22px; font-weight: bold; color: var(--dark-pink); letter-spacing: 2px; }

        .promo-bar { background: var(--black); color: #fff; padding: 12px; font-weight: bold; width: 100%; font-size: 14px; }
        
        .timer-container { background: #fff3f3; padding: 15px; border-bottom: 2px solid #ffcdd2; }
        #timer { font-size: 28px; font-weight: bold; color: #d32f2f; }

        .hero { padding: 20px; }
        .hero-img { width: 95%; max-width: 480px; border-radius: 15px; margin: 0 auto 20px; display: block; box-shadow: 0 4px 15px rgba(0,0,0,0.08); }

        .price-box { margin: 15px 0; }
        .new-price { font-size: 32px; color: #e91e63; font-weight: bold; }
        .badge { background: #ff5252; color: #fff; padding: 6px 15px; border-radius: 5px; font-size: 14px; display: inline-block; margin-top: 5px; font-weight: bold; }

        /* ستايل صور الإضاءة القابلة للضغط */
        .lighting-grid { 
            display: flex; 
            gap: 15px; 
            justify-content: center; 
            padding: 0 10px; 
            margin-top: 25px;
        }
        .light-item { 
            flex: 1; 
            min-width: 100px;
            max-width: 180px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        .light-item:active { transform: scale(0.95); }
        .light-item img { 
            width: 100%; 
            border-radius: 12px; 
            box-shadow: 0 4px 12px rgba(0,0,0,0.12); 
            border: 2px solid #fff;
        }
        .light-label { font-size: 12px; font-weight: bold; margin-top: 8px; color: var(--dark-pink); }

        /* ستايل المودال (نافذة الصورة المكبرة) */
        .modal {
            display: none; position: fixed; z-index: 20000; left: 0; top: 0;
            width: 100%; height: 100%; background-color: rgba(0,0,0,0.9);
            justify-content: center; align-items: center;
        }
        .modal-content { max-width: 90%; max-height: 80%; border-radius: 10px; }
        .close-modal { position: absolute; top: 20px; right: 30px; color: #fff; font-size: 40px; font-weight: bold; cursor: pointer; }

        .info-card { padding: 40px 15px; border-bottom: 1px solid #f0f0f0; }
        .info-card h3 { color: var(--dark-pink); margin-bottom: 15px; font-size: 1.3rem; }
        .info-card p { font-size: 1.1rem; color: #555; max-width: 550px; margin: 0 auto; padding: 0 15px; }

        /* ستايل قسم الأسئلة والأجوبة */
        .faq-section { padding: 40px 15px; background: #fff; text-align: right; }
        .faq-title { color: var(--dark-pink); margin-bottom: 25px; text-align: center; }
        .faq-item { border-bottom: 1px solid #eee; padding: 15px 0; }
        .faq-question { font-weight: bold; color: #333; cursor: pointer; display: flex; justify-content: space-between; align-items: center; }
        .faq-question::after { content: '+'; font-size: 20px; color: var(--dark-pink); }
        .faq-answer { display: none; padding-top: 10px; color: #666; font-size: 14px; line-height: 1.5; }

        .reviews-container { background: var(--main-pink); padding: 40px 15px; }
        .review-card { background: #fff; padding: 15px; border-radius: 15px; margin: 12px auto; width: 100%; max-width: 500px; text-align: right; display: flex; gap: 12px; box-shadow: 0 3px 10px rgba(0,0,0,0.04); }
        .profile-img { width: 50px; height: 50px; border-radius: 50%; object-fit: cover; }
        .stars { color: #ffc107; font-size: 12px; }
        .review-name { font-weight: bold; font-size: 15px; }

        .sticky-footer { position: fixed; bottom: 0; left: 0; width: 100%; background: #fff; padding: 15px 0; z-index: 10000; box-shadow: 0 -5px 20px rgba(0,0,0,0.1); display: flex; justify-content: center; }
        .cta-btn { background: var(--green-wa); color: #fff; width: 88%; max-width: 380px; padding: 18px; border-radius: 50px; text-decoration: none; font-weight: bold; font-size: 1.4rem; display: block; margin: 0 auto; animation: pulse 2.5s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.04); } 100% { transform: scale(1); } }
        .spacer { height: 120px; }
    </style>
</head>
<body>

    <header class="brand-header">
        <img src="logo.png" alt="Veloria Logo" class="brand-logo">
        <span class="brand-name">VELORIA BEAUTY</span>
    </header>

    <div class="promo-bar">🚚 توصيل مجاني + الدفع عند الاستلام 🤝</div>

    <div class="timer-container">
        <p style="margin:0; font-weight: bold;">مدة الخصم تنتهي في:</p>
        <div id="timer">12:00:00</div>
    </div>

    <section class="hero">
        <img src="1.jpg" class="hero-img" alt="حقيبة الماكياج">
        <div class="price-box">
            <span style="text-decoration: line-through; color: #999; font-size: 20px;">419 درهم</span><br>
            <span class="new-price">279 درهم فقط</span><br>
            <span class="badge">خصم حصري على المجموعة كاملة</span>
        </div>
    </section>

    <div class="info-card">
        <h3>مرآة ذكية بـ 3 مستويات إضاءة 💡</h3>
        <p style="margin-bottom: 10px;">(اضغطي على الصورة لتكبيرها)</p>
        
        <div class="lighting-grid">
            <div class="light-item" onclick="openModal('light1.jpg')">
                <img src="light1.jpg" alt="ضوء أبيض">
                <div class="light-label">أبيض طبيعي</div>
            </div>
            <div class="light-item" onclick="openModal('light2.jpg')">
                <img src="light2.jpg" alt="ضوء أصفر">
                <div class="light-label">أصفر دافئ</div>
            </div>
            <div class="light-item" onclick="openModal('light3.jpg')">
                <img src="light3.jpg" alt="ضوء ساطع">
                <div class="light-label">أبيض ناصع</div>
            </div>
        </div>

        <p style="margin-top: 25px; font-size: 1.1rem; color: #555;">
            المرآة تعمل باللمس، قابلة لإعادة الشحن (USB) ويمكن فصلها عن الحقيبة تماماً لاستعمالها بشكل مستقل.
        </p>
    </div>

    <div id="myModal" class="modal">
        <span class="close-modal" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="img01">
    </div>

    <div class="info-card">
        <h3>تنظيم مثالي لمجوهراتك 💍</h3>
        <img src="3.jpg" class="hero-img" alt="علبة المجوهرات">
        <p>علبة مجوهرات أنيقة مقسمة بذكاء لتنظيم الخواتم، السلاسل، والحلقات. حجم مثالي يوضع داخل الحقيبة أو يستعمل بشكل منفصل.</p>
    </div>

    <section class="faq-section">
        <h2 class="faq-title">أسئلة شائعة (FAQ) 🤔</h2>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">واش بصح التوصيل فابور؟</div>
            <div class="faq-answer">نعم أختي، التوصيل مجاني 100% لجميع المدن المغربية، وما كتخلصي حتى كتوصلك السلعة وتأكدي منها.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">شحال كيدوم شحن المرآة؟</div>
            <div class="faq-answer">المرآة مزودة ببطارية قوية كتشارجا بـ USB وكدوم لأسبوع كامل من الاستعمال اليومي.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">واش العلبة د الجواهر كتجي مع الحقيبة؟</div>
            <div class="faq-answer">نعم، العرض فيه الحقيبة الذكية + علبة المجوهرات الأنيقة + كابل الشحن، كولشي بـ 279 درهم فقط.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">إلى وصلاتني ولقيت فيها شي مشكل؟</div>
            <div class="faq-answer">عندنا ضمان الجودة! إلى كان فيها أي عيب مصنعي، كنبدلوها ليك فابور أو كنرجعو ليك فلوسك.</div>
        </div>

        <div class="faq-item">
            <div class="faq-question" onclick="toggleFaq(this)">واش الحقيبة واسعة؟</div>
            <div class="faq-answer">جداً! الحقيبة مصممة باش تهز ليك كاع الماكياج الأساسي مع فواصل تقدري تحركيهم كيف بغيتي.</div>
        </div>
    </section>

    <section class="reviews-container">
        <h2>شنو قالو البنات على المجموعة ديالنا؟ ⭐</h2>
        <div class="review-card">
            <img src="https://images.pexels.com/photos/1181690/pexels-photo-1181690.jpeg?auto=compress&cs=tinysrgb&w=150" class="profile-img">
            <div style="flex:1;">
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <span class="review-name">نهيلة - الرباط</span>
                <p style="font-size:14px; margin:5px 0; color: #444;">أحسن حاجة فهاد الحقيبة هي ديك المرايا! الإضاءة ديالها واعرة بزااف.</p>
            </div>
        </div>
    </section>

    <div class="spacer"></div>

    <div class="sticky-footer">
        <a href="https://wa.me/212691444558" class="cta-btn">اطلبي الآن عبر الواتساب</a>
    </div>

    <script>
        // دالة تكبير الصور
        function openModal(src) {
            document.getElementById("myModal").style.display = "flex";
            document.getElementById("img01").src = src;
        }
        function closeModal() {
            document.getElementById("myModal").style.display = "none";
        }

        // دالة الأسئلة والأجوبة
        function toggleFaq(element) {
            const answer = element.nextElementSibling;
            if (answer.style.display === "block") {
                answer.style.display = "none";
            } else {
                answer.style.display = "block";
            }
        }

        // المؤقت
        function startTimer(duration, display) {
            var timer = duration, hours, minutes, seconds;
            setInterval(function () {
                hours = parseInt(timer / 3600, 10);
                minutes = parseInt((timer % 3600) / 60, 10);
                seconds = parseInt(timer % 60, 10);
                display.textContent = (hours<10?"0"+hours:hours)+":"+(minutes<10?"0"+minutes:minutes)+":"+(seconds<10?"0"+seconds:seconds);
                if (--timer < 0) timer = duration;
            }, 1000);
        }
        window.onload = function () { startTimer(60*60*12, document.querySelector('#timer')); };
    </script>
</body>
</html>
