<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VELORIA BEAUTY - Amazon Style</title>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        :root { --amazon-orange: #ff9900; --amazon-blue: #232f3e; --text-color: #111; --light-gray: #565959; }
        body { font-family: 'Cairo', sans-serif; margin: 0; padding: 0; background: #fff; color: var(--text-color); }
        
        /* Header & Brand */
        .brand-header { padding: 15px; border-bottom: 1px solid #ddd; text-align: center; }
        .brand-name { font-size: 24px; font-weight: bold; color: #f06292; letter-spacing: 1px; }

        .container { max-width: 1200px; margin: auto; padding: 20px; display: grid; grid-template-columns: 1fr 350px; gap: 30px; }

        /* Left Side: Images & Info */
        .main-product { display: flex; flex-direction: column; }
        .image-grid-large { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 20px; }
        .large-img { width: 100%; border-radius: 8px; cursor: zoom-in; border: 1px solid #eee; }
        
        .thumbnails-container { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 30px; }
        .thumb { width: 60px; height: 60px; border: 1px solid #ddd; border-radius: 4px; cursor: pointer; object-fit: cover; }
        .thumb:hover { border-color: var(--amazon-orange); box-shadow: 0 0 5px rgba(255,153,0,0.5); }

        .product-info h2 { font-size: 22px; margin-bottom: 10px; }
        .price-section { border-top: 1px solid #eee; padding-top: 15px; }
        .old-price { text-decoration: line-through; color: var(--light-gray); font-size: 18px; }
        .current-price { color: #B12704; font-size: 28px; font-weight: bold; }
        .discount-tag { background: #CC0C39; color: #fff; padding: 4px 8px; border-radius: 4px; font-size: 14px; margin-right: 10px; }

        /* Features List */
        .specs { margin: 20px 0; background: #f9f9f9; padding: 20px; border-radius: 10px; }
        .specs h3 { font-size: 18px; border-bottom: 1px solid #ddd; padding-bottom: 10px; }
        .specs ul { list-style: none; padding: 0; }
        .specs li { margin-bottom: 10px; padding-right: 25px; position: relative; }
        .specs li::before { content: "✓"; position: absolute; right: 0; color: #007600; font-weight: bold; }

        /* Right Side: Rating Sidebar */
        .rating-sidebar { border: 1px solid #ddd; padding: 20px; border-radius: 8px; height: fit-content; position: sticky; top: 20px; }
        .rating-summary h3 { margin: 0; font-size: 20px; }
        .stars-big { color: var(--amazon-orange); font-size: 24px; }
        .bar-container { display: flex; align-items: center; gap: 10px; margin: 10px 0; }
        .bar-bg { background: #f0f2f2; height: 20px; flex: 1; border-radius: 4px; border: 1px solid #ccc; overflow: hidden; }
        .bar-fill { background: var(--amazon-orange); height: 100%; }

        /* Reviews Feed */
        .reviews-feed { margin-top: 50px; border-top: 1px solid #eee; padding-top: 30px; }
        .review-item { border-bottom: 1px solid #eee; padding: 25px 0; text-align: right; }
        .user-profile { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; }
        .user-avatar { width: 34px; height: 34px; border-radius: 50%; }
        .user-name { font-weight: bold; font-size: 14px; }
        .review-text { font-size: 15px; color: #333; margin-top: 10px; line-height: 1.8; }
        .review-img { width: 120px; height: 120px; border-radius: 8px; object-fit: cover; margin-top: 10px; border: 1px solid #eee; }

        .add-review-btn { background: #f0f2f2; border: 1px solid #d5d9d9; padding: 10px 20px; border-radius: 8px; cursor: pointer; font-size: 14px; margin-top: 20px; }

        /* Footer */
        .shipping-section { margin-top: 40px; text-align: center; background: #f3f3f3; padding: 40px; }
        .slogan { font-size: 20px; font-weight: bold; color: var(--amazon-blue); margin-top: 20px; }

        @media (max-width: 768px) {
            .container { grid-template-columns: 1fr; }
            .rating-sidebar { position: static; }
        }
    </style>
</head>
<body>

    <header class="brand-header">
        <span class="brand-name">VELORIA BEAUTY</span>
    </header>

    <div class="container">
        <main class="main-product">
            <div class="image-grid-large">
                <img src="1.jpg" class="large-img" onclick="openZoom(this.src)">
                <img src="2.jpg" class="large-img" onclick="openZoom(this.src)">
                <img src="3.jpg" class="large-img" onclick="openZoom(this.src)">
                <img src="4.jpg" class="large-img" onclick="openZoom(this.src)">
                <img src="5.jpg" class="large-img" onclick="openZoom(this.src)">
                <img src="6.jpg" class="large-img" onclick="openZoom(this.src)">
            </div>

            <div class="thumbnails-container">
                <img src="t1.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t2.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t3.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t4.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t5.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t6.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t7.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t8.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t9.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t10.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t11.jpg" class="thumb" onclick="openZoom(this.src)">
                <img src="t12.jpg" class="thumb" onclick="openZoom(this.src)">
            </div>

            <div class="product-info">
                <h2>مجموعة التجميل المتكاملة: حقيبة بمرآة LED ذكية + علبة مجوهرات فاخرة</h2>
                <div class="price-section">
                    <span class="discount-tag">خصم 33%</span>
                    <span class="old-price">479.00 درهم</span>
                    <div class="current-price">319.00 درهم</div>
                    <p style="color:#007600; font-weight:bold;">متوفر في المخزون حالياً.</p>
                </div>

                <div class="specs">
                    <h3>تفاصيل المنتج الفنية:</h3>
                    <ul>
                        <li><strong>المادة:</strong> جلد PU فاخر عالي الجودة ومقاوم تماماً للماء والخدوش.</li>
                        <li><strong>نظام الإضاءة:</strong> مرآة LED بـ 3 درجات حرارة (طبيعي، دافئ، بارد) قابلة للشحن.</li>
                        <li><strong>التنظيم:</strong> فواصل داخلية قابلة للتعديل والتحريك حسب حجم الماكياج.</li>
                        <li><strong>علبة المجوهرات:</strong> تصميم مدمج ببطانة مخملية لحماية الخواتم والسلاسل.</li>
                        <li><strong>الاستخدام:</strong> مثالية للسفر، المناسبات، والاستخدام اليومي المنظم.</li>
                    </ul>
                </div>
            </div>
        </main>

        <aside class="rating-sidebar">
            <div class="rating-summary">
                <h3>آراء الزبناء</h3>
                <div class="stars-big">⭐⭐⭐⭐⭐</div>
                <p>4.8 من أصل 5 نجوم</p>
                
                <div class="bar-container">
                    <span>5 نجوم</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 88%;"></div></div>
                    <span>88%</span>
                </div>
                <div class="bar-container">
                    <span>4 نجوم</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 7%;"></div></div>
                    <span>7%</span>
                </div>
                <div class="bar-container">
                    <span>3 نجوم</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 3%;"></div></div>
                    <span>3%</span>
                </div>
                <div class="bar-container">
                    <span>2 نجوم</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 1%;"></div></div>
                    <span>1%</span>
                </div>
                <div class="bar-container">
                    <span>نجمة</span>
                    <div class="bar-bg"><div class="bar-fill" style="width: 1%;"></div></div>
                    <span>1%</span>
                </div>
            </div>
            <button class="add-review-btn">إضافة تقييمك أو صورتك</button>
        </aside>
    </div>

    <section class="container">
        <div class="reviews-feed">
            <h2>أهم المراجعات من المغرب</h2>

            <div class="review-item">
                <div class="user-profile">
                    <img src="https://api.dicebear.com/7.x/avataaars/svg?seed=Nabila" class="user-avatar">
                    <span class="user-name">نبيلة السكوري</span>
                </div>
                <div class="stars">⭐⭐⭐⭐⭐ <span style="font-weight:bold; margin-right:10px;">أحسن حاجة شريت هاد العام!</span></div>
                <div class="review-text">
                    بصراحة كنت مترددة في الأول واش نطلبها ولكن فاش وصلاتني تيقنت بلي السلعة طوب. الحقيبة الجلد ديالها رطب وكيبان غالي، والمرايا الضوء ديالها مجهد بزاف كينفعني فاش كنكون كنقاد الماكياج بالليل أو في بلاصة ناقصة إضاءة. اللي عجبني بزاف هو دوك الفواصل اللي لداخل، حيدتهم وقاديتهم على حساب القياس ديال Palette ديالي وديال العكر، دابا كولشي ولا منظم وما بقيت كنقلب على حتى حاجة. أما العلبة ديال المجوهرات فهي لمسة واعرة، وليت كندير فيها السلاسل اللي كنخاف عليهم يتخبلوا ليا وسط الصاك. الجودة صراحة هربانة والتوصيل كان سريع، وصلاتني في 24 ساعة للرباط. شكراً فيلوريا على هاد المصداقية!
                </div>
                <img src="r1.jpg" class="review-img">
            </div>

            <div class="review-item">
                <div class="user-profile">
                    <img src="https://api.dicebear.com/7.x/avataaars/svg?seed=Siham" class="user-avatar">
                    <span class="user-name">سهام بناني</span>
                </div>
                <div class="stars">⭐⭐⭐⭐⭐ <span style="font-weight:bold; margin-right:10px;">عملية جداً للسفر</span></div>
                <div class="review-text">
                    المرآة ذكية بزاف حيت كتشحن بـ USB وما كنحتاجش خيوط. الصاك كيهز بزاف ديال السلعة والعلبة د الخواتم فكرة رائعة. جودة الجلد ممتازة ومقاوم للماء كيف مكتوب.
                </div>
                <img src="r2.jpg" class="review-img">
            </div>

            <div class="review-item">
                <div class="user-profile">
                    <img src="https://api.dicebear.com/7.x/avataaars/svg?seed=Zineb" class="user-avatar">
                    <span class="user-name">زينب العلوية</span>
                </div>
                <div class="stars">⭐⭐⭐⭐⭐</div>
                <div class="review-text">واعرة بزااااف 😍 جودة هربانة!</div>
            </div>

            <div class="review-item">
                <div class="user-profile">
                    <img src="https://api.dicebear.com/7.x/avataaars/svg?seed=Hanan" class="user-avatar">
                    <span class="user-name">حنان المرابط</span>
                </div>
                <div class="stars">⭐⭐⭐⭐⭐ <span style="font-weight:bold; margin-right:10px;">العلبة د المجوهرات كلاس</span></div>
                <div class="review-text">
                    عجباتني العلبة بزاف، اللون الوردي غزال ومن الداخل رطبة كتحمي الذهب من الخدوش. الحقيبة حتى هي فالمستوى.
                </div>
                <img src="r3.jpg" class="review-img">
            </div>

            </div>
    </section>

    <div class="shipping-section">
        <img src="delivery.jpg" class="large-img" style="max-width: 400px; margin: auto;">
        <div class="slogan">VELORIA BEAUTY: الجودة التي تستحقينها، بضمانتنا الشخصية.</div>
        <p>توصيل مجاني لجميع المدن - الدفع عند الاستلام</p>
    </div>

    <div id="zoomModal" style="display:none; position:fixed; z-index:9999; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.9); justify-content:center; align-items:center;" onclick="this.style.display='none'">
        <img id="zoomImg" style="max-width:90%; max-height:90%; border-radius:10px;">
    </div>

    <script>
        function openZoom(src) {
            document.getElementById('zoomModal').style.display = 'flex';
            document.getElementById('zoomImg').src = src;
        }
    </script>

</body>
</html>
