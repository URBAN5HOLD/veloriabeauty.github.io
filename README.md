<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Veloria Beauty - Amazon Experience</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        :root { --amzn-orange: #FFD814; --amzn-orange-hover: #F7CA00; --amzn-link: #007185; }
        body { font-family: 'Cairo', sans-serif; margin: 0; padding: 0; color: #0F1111; background: #fff; }
        
        /* Layout */
        .amazon-container { display: flex; max-width: 1300px; margin: 20px auto; padding: 0 20px; gap: 40px; }
        
        /* Left: Image Gallery */
        .gallery-section { flex: 1.2; display: flex; flex-direction: column; }
        .main-images-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-bottom: 20px; }
        .main-images-grid img { width: 100%; border: 1px solid #ddd; border-radius: 4px; cursor: crosshair; }
        
        .thumbs-grid { display: grid; grid-template-columns: repeat(6, 1fr); gap: 10px; }
        .thumb-box { border: 1px solid #ddd; border-radius: 4px; padding: 2px; cursor: pointer; transition: 0.2s; }
        .thumb-box:hover { border-color: #e77600; box-shadow: 0 0 3px 2px rgba(228,121,17,.5); }
        .thumb-box img { width: 100%; height: auto; display: block; }

        /* Right: Product Details */
        .details-section { flex: 0.8; }
        .product-title { font-size: 24px; font-weight: 500; line-height: 32px; border-bottom: 1px solid #eee; padding-bottom: 10px; }
        .rating-row { color: var(--amzn-link); font-size: 14px; margin: 10px 0; display: flex; align-items: center; gap: 10px; }
        .stars { color: #FFA41C; font-size: 18px; }

        .price-table { margin: 20px 0; background: #fafafa; padding: 15px; border-radius: 8px; }
        .price-row { display: flex; align-items: baseline; gap: 10px; }
        .perc-off { color: #CC0C39; font-size: 28px; font-weight: 300; }
        .price-big { font-size: 28px; font-weight: 500; }
        .list-price { color: #565959; text-decoration: line-through; font-size: 14px; }

        .buy-box { border: 1px solid #D5D9D9; border-radius: 8px; padding: 20px; margin-top: 20px; }
        .instock { color: #007600; font-size: 18px; display: block; margin-bottom: 15px; }
        .cta-button { background: var(--amzn-orange); border: 1px solid #FCD200; border-radius: 20px; width: 100%; padding: 10px; font-weight: 400; cursor: pointer; font-size: 15px; text-decoration: none; display: block; text-align: center; color: #000; margin-bottom: 10px; }
        .cta-button:hover { background: var(--amzn-orange-hover); }

        /* Description & Specs */
        .bullets { margin-top: 20px; font-size: 14px; line-height: 20px; }
        .bullets ul { padding-right: 20px; }
        .bullets li { margin-bottom: 10px; }

        /* Reviews Section (The logic you asked for) */
        .reviews-area { margin-top: 60px; display: flex; gap: 50px; border-top: 1px solid #eee; padding-top: 40px; }
        .reviews-sidebar { width: 300px; }
        .review-bar { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; font-size: 13px; }
        .bar-gray { background: #F0F2F2; height: 20px; flex: 1; border-radius: 4px; box-shadow: inset 0 0 0 1px #E3E6E6; overflow: hidden; }
        .bar-gold { background: #FFA41C; height: 100%; }

        .reviews-list { flex: 1; }
        .review-card { margin-bottom: 40px; }
        .user-info { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; }
        .user-info img { width: 34px; height: 34px; border-radius: 50%; }
        .review-title { font-weight: 700; margin-right: 10px; }
        .review-content { font-size: 14px; line-height: 1.5; margin: 10px 0; }
        .review-pic { width: 150px; border-radius: 4px; margin-top: 10px; }

        @media (max-width: 900px) {
            .amazon-container, .reviews-area { flex-direction: column; }
            .reviews-sidebar { width: 100%; }
        }
    </style>
</head>
<body>

    <div class="amazon-container">
        <div class="gallery-section">
            <div class="main-images-grid">
                <img src="large1.jpg" alt="1">
                <img src="large2.jpg" alt="2">
                <img src="large3.jpg" alt="3">
                <img src="large4.jpg" alt="4">
                <img src="large5.jpg" alt="5">
                <img src="large6.jpg" alt="6">
            </div>
            
            <div class="thumbs-grid">
                <div class="thumb-box"><img src="thumb1.jpg"></div>
                <div class="thumb-box"><img src="thumb2.jpg"></div>
                <div class="thumb-box"><img src="thumb3.jpg"></div>
                <div class="thumb-box"><img src="thumb4.jpg"></div>
                <div class="thumb-box"><img src="thumb5.jpg"></div>
                <div class="thumb-box"><img src="thumb6.jpg"></div>
                <div class="thumb-box"><img src="thumb7.jpg"></div>
                <div class="thumb-box"><img src="thumb8.jpg"></div>
                <div class="thumb-box"><img src="thumb9.jpg"></div>
                <div class="thumb-box"><img src="thumb10.jpg"></div>
                <div class="thumb-box"><img src="thumb11.jpg"></div>
                <div class="thumb-box"><img src="thumb12.jpg"></div>
            </div>
        </div>

        <div class="details-section">
            <h1 class="product-title">حقيبة تجميل احترافية VELORIA مع مرآة LED ذكية قابلة للشحن + علبة مجوهرات مخملية فاخرة</h1>
            
            <div class="rating-row">
                <span class="stars">⭐⭐⭐⭐⭐</span>
                <span>854 تقييم</span> | <span>100+ سؤال مجاب عنه</span>
            </div>

            <div class="price-table">
                <div class="price-row">
                    <span class="perc-off">-33%</span>
                    <span class="price-big">319.00 درهم</span>
                </div>
                <div class="list-price">الثمن الأصلي: 479.00 درهم</div>
                <p style="font-size: 13px;">الأسعار تشمل التوصيل المجاني لجميع المدن المغربية.</p>
            </div>

            <div class="buy-box">
                <span class="instock">متوفر حالياً.</span>
                <p style="font-size: 14px;">يصلك خلال 24 - 48 ساعة فقط.</p>
                <a href="https://wa.me/2126XXXXXXXX" class="cta-button">اطلبي الآن (الدفع عند الاستلام)</a>
            </div>

            <div class="bullets">
                <h3>حول هذه السلعة</h3>
                <ul>
                    <li><strong>جلد فاخر مقاوم للماء:</strong> مصنوعة من جلد PU عالي الجودة سهل التنظيف ويحمي محتوياتك.</li>
                    <li><strong>مرآة ذكية بـ 3 ألوان:</strong> إضاءة احترافية (أبيض، دافئ، طبيعي) لتطبيق ماكياج مثالي في أي مكان.</li>
                    <li><strong>تنظيم ذكي:</strong> فواصل قابلة للإزالة لتنظيم المساحة حسب احتياجاتك الخاصة.</li>
                    <li><strong>حقيبة مجوهرات مدمجة:</strong> تأتي مع علبة صغيرة مخصصة للسلاسل والخواتم لمنع التشابك.</li>
                </ul>
            </div>
        </div>
    </div>

    <div class="container" style="max-width: 1300px; margin: auto; padding: 20px;">
        <div class="reviews-area">
            <div class="reviews-sidebar">
                <h3>مراجعات المستخدمين</h3>
                <div class="stars" style="font-size: 24px;">⭐⭐⭐⭐⭐</div>
                <p>4.8 من أصل 5</p>
                <div class="review-bar"><span>5 نجوم</span><div class="bar-gray"><div class="bar-gold" style="width: 88%;"></div></div><span>88%</span></div>
                <div class="review-bar"><span>4 نجوم</span><div class="bar-gray"><div class="bar-gold" style="width: 7%;"></div></div><span>7%</span></div>
                <div class="review-bar"><span>3 نجوم</span><div class="bar-gray"><div class="bar-gold" style="width: 3%;"></div></div><span>3%</span></div>
                <button style="width:100%; margin-top:20px; padding:10px; border-radius:8px; border:1px solid #ddd; background:#fff; cursor:pointer;">كتابة مراجعة</button>
            </div>

            <div class="reviews-list">
                <div class="review-card">
                    <div class="user-info">
                        <img src="https://api.dicebear.com/7.x/avataaars/svg?seed=Nora">
                        <span class="user-name">ليلى الفاسي</span>
                    </div>
                    <div class="stars">⭐⭐⭐⭐⭐ <span class="review-title">أحسن تجربة شراء أونلاين</span></div>
                    <p style="color: #565959; font-size: 13px;">تمت المراجعة في المغرب يوم 2 أبريل 2026</p>
                    <div class="review-content">
                        بصراحة، هاد الشنطة فاقت التوقعات ديالي بزااااف! كنت ديما كنعاني مع المكياج فاش كنكون مسافرة، كولشي كيتخلط ليا والمرايا ديال لوتيل ديما ناقصة ضوء. هاد الحقيبة حلات ليا المشكل، الإضاءة ديالها واعرة وفيها 3 ديال الدرجات كتحكمي فيهم باللمس، والبطارية كتدوم مدة طويلة بلا شحن. الجلد ديالها من برا كيبان فخم وصحيح، واللون الوردي ديالها غزال بزاف (Rose Gold). الفواصل اللي لداخل نفعوني حيت قاديتهم على قياس Palette ديالي وLes pinceaux. أما علبة المجوهرات فهي الصدمة الجميلة، صغيرة وكتهز السلاسل والخواتم بطريقة منظمة بلا ما يتشابكوا. شكراً لـ Veloria Beauty على الجودة وسرعة التوصيل، وصلتني في أقل من 24 ساعة للدار البيضاء. كنصح بها أي بنت كتهتم بمكياجها ومنظرها!
                    </div>
                    <img src="real-review1.jpg" class="review-pic">
                </div>

                <div class="review-card">
                    <div class="user-info">
                        <img src="https://api.dicebear.com/7.x/avataaars/svg?seed=Sara">
                        <span class="user-name">مريم العمراني</span>
                    </div>
                    <div class="stars">⭐⭐⭐⭐⭐ <span class="review-title">جودة الجلد رائعة</span></div>
                    <div class="review-content">
                        المنتج مطابق للوصف 100%. الجلد نوعية ممتازة ومقاوم للماء، جربت رشيت عليه شوية د الماء وما وقع ليه والو. المرآة وضوحها عالي والعلبة د المجوهرات كلاس بزاف. التوصيل كان سريع والتعامل جد محترم. شكراً ليكم بزااف.
                    </div>
                    <img src="real-review2.jpg" class="review-pic">
                </div>

                <div class="review-card">
                    <div class="user-info">
                        <img src="https://api.dicebear.com/7.x/avataaars/svg?seed=Hala">
                        <span class="user-name">هالة الناصري</span>
                    </div>
                    <div class="stars">⭐⭐⭐⭐⭐</div>
                    <div class="review-content">طوب! 😍✨</div>
                </div>
            </div>
        </div>
    </div>

    <div style="background: #f3f3f3; padding: 40px; text-align: center; margin-top: 50px;">
        <img src="delivery-logo.png" style="width: 150px;">
        <h3 style="color: #232f3e;">VELORIA BEAUTY: نضمن لك الجودة أو استرجاع أموالك.</h3>
    </div>

</body>
</html>
