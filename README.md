<html lang="en">
<head>
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-4BSNJLYWR0"></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      gtag('config', 'G-4BSNJLYWR0');
    </script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Parfum | Official Luxury Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&family=Playfair+Display:italic@400&display=swap" rel="stylesheet">
    
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; outline: none !important; border: none !important; text-decoration: none !important; background: none !important; -webkit-tap-highlight-color: transparent; }
        html, body { width: 100%; background-color: #000 !important; scroll-snap-type: y mandatory; scroll-behavior: smooth; font-family: 'Montserrat', sans-serif; color: #fff; overflow-x: hidden; }
        
        /* Logo Styling */
        .logo-container { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); z-index: 1000; text-align: center; pointer-events: none; }
        .logo-main { font-family: 'Cinzel', serif; font-size: 1.4rem; letter-spacing: 12px; color: #fff !important; line-height: 1; }
        .logo-sub { font-family: 'Playfair Display', serif; font-style: italic; font-size: 0.7rem; letter-spacing: 4px; color: #aaa !important; margin-top: 5px; opacity: 0.8; }

        .scroll-trigger { position: fixed; top: 85%; right: 25px; transform: translateY(-50%); width: 40px; height: 40px; z-index: 2000; cursor: pointer; display: flex; align-items: center; justify-content: center; }
        .arrow-icon { width: 15px; height: 15px; border-right: 2px solid var(--current-arrow-color, #fff) !important; border-bottom: 2px solid var(--current-arrow-color, #fff) !important; transform: rotate(45deg); animation: bounce 2s infinite; transition: 0.5s ease; }
        .arrow-up { transform: rotate(-135deg) !important; }
        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }
        
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; padding-bottom: 100px; background-color: #000 !important; border-bottom: 1px solid rgba(255,255,255,0.05) !important; }
        .glow-center { position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%); width: 100%; max-width: 600px; height: 600px; background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 70%) !important; opacity: 0.25; z-index: 0; pointer-events: none; }
        
        .v-header { width: 100%; position: relative; z-index: 1; overflow: hidden; }
        .bg-v { width: 100%; height: auto; object-fit: cover; display: block; }
        
        .bottle-center { text-align: center; position: relative; z-index: 2; margin-top: -60px; padding-bottom: 40px; }
        .img-bottle { width: 60%; max-width: 320px; margin: 0 auto; filter: drop-shadow(0 0 30px rgba(0,0,0,0.8)); }
        .brand-logo { font-family: 'Cinzel', serif; font-size: 1.8rem; letter-spacing: 5px; margin-top: 15px; }
        .perfume-sub { font-size: 0.65rem; color: var(--color) !important; letter-spacing: 3px; font-weight: 600; margin-top: 5px; }

        .row { display: flex; align-items: center; width: 100%; padding: 60px 10%; gap: 50px; z-index: 2; position: relative; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 45%; }
        .img-box img { width: 100%; border-radius: 2px; box-shadow: 0 15px 35px rgba(0,0,0,0.6); }
        .txt-box { width: 55%; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.3rem; margin-bottom: 15px; color: var(--color) !important; }
        .txt-box p { font-size: 0.9rem; line-height: 1.8; color: #ccc !important; font-weight: 300; }

        .purchase-area { max-width: 1100px; margin: 50px auto; display: flex; gap: 50px; padding: 50px; background: rgba(255,255,255,0.02) !important; border: 1px solid rgba(255,255,255,0.05) !important; width: 90%; z-index: 2; position: relative; }
        .size-container { display: flex; gap: 12px; margin-top: 20px; }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.1) !important; text-align: center; cursor: pointer; transition: 0.3s; }
        .size-box span { display: block; font-size: 8px; color: #666; margin-top: 4px; }
        .active-size { border-color: var(--color) !important; background: rgba(255,255,255,0.05) !important; }
        
        .form-box { flex: 1.2; display: flex; flex-direction: column; gap: 15px; }
        input, textarea { width: 100%; padding: 15px 5px; color: #fff !important; border-bottom: 1px solid rgba(255,255,255,0.2) !important; font-family: 'Montserrat'; font-size: 0.85rem; }
        textarea { height: 60px; resize: none; }
        .order-btn { width: 100%; padding: 20px; background-color: #fff !important; color: #000 !important; font-weight: 700; cursor: pointer; letter-spacing: 3px; margin-top: 10px; transition: 0.3s; }
        .order-btn:hover { background-color: var(--color) !important; color: #fff !important; }

        .footer-support { text-align: center; padding: 40px; font-size: 0.8rem; letter-spacing: 2px; color: #666; }
        .support-link { color: #888 !important; transition: 0.3s; }
        .support-link:hover { color: #fff !important; }

        @media (max-width: 900px) { 
            .row, .row.rev { flex-direction: column; padding: 40px 8%; text-align: center; } 
            .img-box, .txt-box { width: 100%; }
            .purchase-area { flex-direction: column; padding: 30px 20px; }
            .logo-main { font-size: 1.1rem; letter-spacing: 8px; }
        }

        /* Color Themes */
        .sauv-t { --color: #4A90E2; --glow-color: rgba(74, 144, 226, 0.4); }
        .stron-t { --color: #CD7F32; --glow-color: rgba(205, 127, 50, 0.4); }
        .libre-t { --color: #D4AF37; --glow-color: rgba(212, 175, 55, 0.4); }
        .gg-t { --color: #1a4d99; --glow-color: rgba(26, 77, 153, 0.4); }
    </style>
</head>
<body>

    <div class="logo-container">
        <div class="logo-main">VELOORIA</div>
        <div class="logo-sub">Parfum</div>
    </div>
    
    <div class="scroll-trigger" id="scrollBtn"><div class="arrow-icon"></div></div>

    <section class="product-section sauv-t" id="sec1">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/sauvage.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/sauvage-bottle.png" class="img-bottle">
            <h1 class="brand-logo">SAUVAGE ELIXIR</h1>
            <div class="perfume-sub">EXTRAIT DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/sauvage-detail-left.jpg"></div>
            <div class="txt-box">
                <h3>THE LEGENDARY DEPTH</h3>
                <p>Sauvage Elixir is an extraordinary concentration, a masterpiece of wild freshness. It intoxicates the senses with a custom-made heart of spices and a rich, woody trail.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <h4 style="font-family:'Cinzel'; margin-bottom:10px;">Select Size</h4>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 223, 'sec1')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 361, 'sec1')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-box">
                <input name="name" placeholder="FULL NAME (REQUIRED)" required>
                <input name="phone" placeholder="PHONE NUMBER (REQUIRED)" required>
                <input name="city" placeholder="CITY (REQUIRED)" required>
                <textarea name="note" placeholder="Note (Optional)"></textarea>
                <button type="button" class="order-btn" onclick="sendOrder('sec1', 'SAUVAGE ELIXIR')">RESERVE NOW | 361 DH</button>
            </div>
        </div>
    </section>

    <section class="product-section stron-t" id="sec2">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/stronger.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/stronger-bottle.png" class="img-bottle">
            <h1 class="brand-logo">STRONGER WITH YOU</h1>
            <div class="perfume-sub">INTENSELY EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/stronger-detail-left.jpg"></div>
            <div class="txt-box">
                <h3>MAGNETIC SENSUALITY</h3>
                <p>A vibrant and bold fragrance for the modern individual. Featuring notes of pink pepper and vanilla, it creates an unforgettable presence.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <h4 style="font-family:'Cinzel'; margin-bottom:10px;">Select Size</h4>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 146, 'sec2')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 207, 'sec2')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-box">
                <input name="name" placeholder="FULL NAME (REQUIRED)" required>
                <input name="phone" placeholder="PHONE NUMBER (REQUIRED)" required>
                <input name="city" placeholder="CITY (REQUIRED)" required>
                <textarea name="note" placeholder="Note (Optional)"></textarea>
                <button type="button" class="order-btn" onclick="sendOrder('sec2', 'STRONGER WITH YOU')">RESERVE NOW | 207 DH</button>
            </div>
        </div>
    </section>

    <section class="product-section libre-t" id="sec3">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/libre.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/libre-bottle.png" class="img-bottle">
            <h1 class="brand-logo">LIBRE INTENSE</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/libre-detail-left.jpg"></div>
            <div class="txt-box">
                <h3>BORN TO BE FREE</h3>
                <p>The iconic structure of Libre intensified. A floral duality between French lavender and Moroccan orange blossom enveloped in orchid.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <h4 style="font-family:'Cinzel'; margin-bottom:10px;">Select Size</h4>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 179, 'sec3')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 273, 'sec3')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-box">
                <input name="name" placeholder="FULL NAME (REQUIRED)" required>
                <input name="phone" placeholder="PHONE NUMBER (REQUIRED)" required>
                <input name="city" placeholder="CITY (REQUIRED)" required>
                <textarea name="note" placeholder="Note (Optional)"></textarea>
                <button type="button" class="order-btn" onclick="sendOrder('sec3', 'LIBRE INTENSE')">RESERVE NOW | 273 DH</button>
            </div>
        </div>
    </section>

    <section class="product-section gg-t" id="sec4">
        <div class="glow-center"></div>
        <div class="v-header"><video autoplay muted loop playsinline class="bg-v"><source src="assets/goodgirl.mp4" type="video/mp4"></video></div>
        <div class="bottle-center">
            <img src="assets/goodgirl-bottle.png" class="img-bottle">
            <h1 class="brand-logo">GOOD GIRL</h1>
            <div class="perfume-sub">EAU DE PARFUM</div>
        </div>
        <div class="row">
            <div class="img-box"><img src="assets/gg-detail-left.jpg"></div>
            <div class="txt-box">
                <h3>SO GOOD TO BE BAD</h3>
                <p>Inspired by the duality of women: bold and sexy, elegant and enigmatic. A mix of dark and light elements for a vibrant femininity.</p>
            </div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <h4 style="font-family:'Cinzel'; margin-bottom:10px;">Select Size</h4>
                <div class="size-container">
                    <div class="size-box" onclick="selectSize(this, 160, 'sec4')">5ML<span>± 80 SPRAYS</span></div>
                    <div class="size-box active-size" onclick="selectSize(this, 235, 'sec4')">10ML<span>± 160 SPRAYS</span></div>
                </div>
            </div>
            <div class="form-box">
                <input name="name" placeholder="FULL NAME (REQUIRED)" required>
                <input name="phone" placeholder="PHONE NUMBER (REQUIRED)" required>
                <input name="city" placeholder="CITY (REQUIRED)" required>
                <textarea name="note" placeholder="Note (Optional)"></textarea>
                <button type="button" class="order-btn" onclick="sendOrder('sec4', 'GOOD GIRL')">RESERVE NOW | 235 DH</button>
            </div>
        </div>
    </section>

    <footer class="footer-support">
        FOR EMERGENCY OR HELP: <a href="https://wa.me/212691444558" class="support-link">0691444558</a>
    </footer>

    <script>
        // Currency Protection: Prevents translation tools from changing "DH"
        setInterval(() => {
            document.querySelectorAll('.order-btn, .size-box, footer').forEach(el => {
                if (el.innerText.includes('DH')) {
                    el.setAttribute('translate', 'no');
                    el.classList.add('notranslate');
                }
            });
        }, 1000);

        function selectSize(element, price, sectionId) {
            const section = document.getElementById(sectionId);
            section.querySelectorAll('.size-box').forEach(box => box.classList.remove('active-size'));
            element.classList.add('active-size');
            section.querySelector('.order-btn').innerText = `RESERVE NOW | ${price} DH`;
        }

        function sendOrder(sectionId, productName) {
            const section = document.getElementById(sectionId);
            const name = section.querySelector('input[name="name"]').value;
            const phone = section.querySelector('input[name="phone"]').value;
            const city = section.querySelector('input[name="city"]').value;
            const note = section.querySelector('textarea[name="note"]').value || "No note";
            const size = section.querySelector('.active-size').firstChild.textContent;
            const price = section.querySelector('.order-btn').innerText.split('|')[1].trim();

            if(!name || !phone || !city) {
                alert("Please fill all required fields.");
                return;
            }

            const botToken = "8751066528:AAFJOYkbqi3bSxncJh4tKSQeH_0wCT660ps";
            const chatId = "7635707772"; 
            
            const message = `🚀 *New Reservation: Velooria*\n\n` +
                            `📦 *Product:* ${productName}\n` +
                            `📏 *Size:* ${size}\n` +
                            `💰 *Price:* ${price}\n` +
                            `--------------------------\n` +
                            `👤 *Name:* ${name}\n` +
                            `📞 *Phone:* ${phone}\n` +
                            `📍 *City:* ${city}\n` +
                            `📝 *Note:* ${note}\n\n` +
                            `✅ Younes, a new customer is waiting!`;

            fetch(`https://api.telegram.org/bot${botToken}/sendMessage`, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify({ chat_id: chatId, text: message, parse_mode: 'Markdown' })
            })
            .then(res => {
                alert("Success! Your reservation has been sent.");
                section.querySelector('form').reset();
            })
            .catch(err => alert("Connection error, please try again."));
        }

        // Scroll Logic
        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        const colors = ['#4A90E2', '#CD7F32', '#D4AF37', '#1a4d99'];
        let currentIdx = 0;
        const scrollBtn = document.getElementById('scrollBtn');
        const arrow = scrollBtn.querySelector('.arrow-icon');

        window.addEventListener('scroll', () => {
            sections.forEach((id, index) => {
                const rect = document.getElementById(id).getBoundingClientRect();
                if(rect.top >= -window.innerHeight/2 && rect.top <= window.innerHeight/2) {
                    currentIdx = index;
                    document.documentElement.style.setProperty('--current-arrow-color', colors[index]);
                    if(currentIdx === sections.length - 1) {
                        arrow.classList.add('arrow-up');
                    } else {
                        arrow.classList.remove('arrow-up');
                    }
                }
            });
        });

        scrollBtn.onclick = () => {
            if(currentIdx === sections.length - 1) {
                window.scrollTo({ top: 0, behavior: 'smooth' });
            } else {
                document.getElementById(sections[currentIdx + 1]).scrollIntoView({ behavior: 'smooth' });
            }
        };
    </script>
</body>
</html>
