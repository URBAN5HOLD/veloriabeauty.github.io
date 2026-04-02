<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>صفحة الهبوط - المنتج ديالك</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #e67e22; /* لون زر الطلب - تقدر تبدلو */
            --text-dark: #2c3e50;
            --bg-light: #f9f9f9;
        }

        body {
            font-family: 'Cairo', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #fff;
            color: var(--text-dark);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        /* 1. Headline Section */
        header {
            padding: 40px 0;
            background-color: var(--bg-light);
        }

        h1 {
            font-size: 2rem;
            color: #d35400;
            margin-bottom: 10px;
        }

        .sub-headline {
            font-size: 1.2rem;
            color: #7f8c8d;
        }

        /* 2. Media Section */
        .media-container {
            margin: 20px 0;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .media-container img, .media-container video {
            width: 100%;
            display: block;
        }

        /* 3. Benefits Section */
        .benefits {
            padding: 40px 0;
            text-align: right;
        }

        .benefit-item {
            margin-bottom: 20px;
            padding: 15px;
            border-right: 4px solid var(--primary-color);
            background: #fff9f5;
        }

        /* 4. Social Proof */
        .testimonials {
            background: var(--bg-light);
            padding: 40px 0;
        }

        .testimonial-card {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 15px;
            font-style: italic;
        }

        /* 5. The Offer */
        .offer-box {
            border: 2px dashed #e74c3c;
            padding: 30px;
            margin: 40px 0;
            background-color: #fdf2f2;
        }

        .price {
            font-size: 2.5rem;
            font-weight: bold;
            color: #c0392b;
        }

        /* 6. Call to Action Button */
        .cta-button {
            display: inline-block;
            background-color: var(--primary-color);
            color: white;
            padding: 20px 40px;
            font-size: 1.5rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(230, 126, 34, 0.4);
            transition: transform 0.3s ease;
            margin-top: 20px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        footer {
            padding: 30px;
            font-size: 0.9rem;
            color: #95a5a6;
        }

        /* Responsive */
        @media (max-width: 600px) {
            h1 { font-size: 1.5rem; }
            .cta-button { width: 80%; font-size: 1.2rem; }
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <h1>هنا دير العنوان القوي (مثلا: تخلصي من مشاكل البشرة في 7 أيام فقط!)</h1>
            <p class="sub-headline">هنا دير وصف صغير كيشجع (مثلا: الحل الطبيعي والأكثر مبيعاً في المغرب)</p>
        </div>
    </header>

    <div class="container">
        <div class="media-container">
            <img src="https://via.placeholder.com/600x400" alt="صورة المنتج">
        </div>

        <section class="benefits">
            <h2>علاش غادي يعجبك هاد المنتج؟</h2>
            <div class="benefit-item">
                <strong>ميزة 1:</strong> هنا شرح كيفاش غينفع الكليان (مثلا: كيرطب البشرة بعمق).
            </div>
            <div class="benefit-item">
                <strong>ميزة 2:</strong> ميزة تانية (مثلا: مكونات طبيعية 100% بدون مواد كيماوية).
            </div>
            <div class="benefit-item">
                <strong>ميزة 3:</strong> ميزة تالتة (مثلا: سهل الاستعمال وكيناسب جميع أنواع البشرة).
            </div>
        </section>

        <section class="testimonials">
            <h2>شنو كايقولو الزبناء ديالينا؟</h2>
            <div class="testimonial-card">
                "بصراحة جربت بزاف ديال المنتجات ولكن هادا هو اللي عطاني نتيجة من السيمانة اللولة."
                <br><strong>- سناء من الدار البيضاء</strong>
            </div>
            <div class="testimonial-card">
                "التوصيل كان سريع والمنتج وصلني كيفما فالتصويرة، شكراً بزاف."
                <br><strong>- محمد من مراكش</strong>
            </div>
        </section>

        <div class="offer-box">
            <h3>عرض خاص ومحدود!</h3>
            <p>توصيل فابور + الدفع عند الاستلام</p>
            <div class="price">199 درهم</div>
            <p style="text-decoration: line-through; color: #7f8c8d;">عوض 399 درهم</p>
            
            <a href="رابط_الواتساب_أو_Google_Form_هنا" class="cta-button">إضغط هنا للطلب الآن</a>
        </div>
    </div>

    <footer>
        <div class="container">
            &copy; 2026 جميع الحقوق محفوظة لمتجركم
        </div>
    </footer>

</body>
</html>
