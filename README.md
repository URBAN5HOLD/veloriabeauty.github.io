<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Velooria Beauty | Official Luxury Collection</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@200;400;600&display=swap" rel="stylesheet">
    
    <style>
        * { 
            margin: 0; padding: 0; box-sizing: border-box; 
            text-decoration: none !important;
            -webkit-tap-highlight-color: transparent;
        }

        html, body { 
            width: 100%; background-color: #000 !important; 
            scroll-snap-type: y mandatory; scroll-behavior: smooth; 
            font-family: 'Montserrat', sans-serif; color: #fff; overflow-x: hidden;
        }

        /* Fixed Logo */
        .logo-fixed { 
            position: fixed; top: 0; left: 0; width: 100%; 
            background-color: #000 !important; padding: 25px 0; 
            z-index: 10000; font-family: 'Cinzel', serif; 
            font-size: 1.2rem; letter-spacing: 10px; color: #fff !important; 
            text-align: center; box-shadow: 0 5px 20px rgba(0,0,0,0.5);
        }

        /* Scroll Trigger */
        .scroll-trigger { 
            position: fixed; bottom: 40%; right: 15px; 
            width: 50px; height: 50px; z-index: 10001; 
            cursor: pointer; display: flex; align-items: center; justify-content: center;
            background: rgba(255,255,255,0.1); border-radius: 50%;
        }
        
        .arrow-icon { 
            width: 15px; height: 15px; 
            border-right: 3px solid var(--current-arrow-color, #fff); 
            border-bottom: 3px solid var(--current-arrow-color, #fff); 
            transform: rotate(45deg); transition: all 0.5s ease;
            animation: bounce 2s infinite;
        }
        .arrow-up { transform: rotate(-135deg) !important; }

        @keyframes bounce { 0%, 100% { transform: translateY(-5px) rotate(45deg); } 50% { transform: translateY(5px) rotate(45deg); } }
        @keyframes bounce-up { 0%, 100% { transform: translateY(5px) rotate(-135deg); } 50% { transform: translateY(-5px) rotate(-135deg); } }

        /* Sections */
        .product-section { width: 100%; min-height: 100vh; scroll-snap-align: start; position: relative; padding-bottom: 80px; background-color: #000 !important; }
        .glow-center { position: absolute; top: 40%; left: 50%; transform: translate(-50%, -50%); width: 600px; height: 600px; background: radial-gradient(circle, var(--glow-color) 0%, rgba(0,0,0,0) 75%) !important; opacity: 0.3; z-index: 0; pointer-events: none; }
        .v-header { width: 100%; position: relative; z-index: 1; line-height: 0; }
        .bg-v { width: 100%; height: auto; display: block; }

        .bottle-center { text-align: center; padding: 40px 0; position: relative; z-index: 2; }
        .img-bottle { width: 100%; max-width: 160px; height: 250px; object-fit: contain; margin: 0 auto; display: block; filter: drop-shadow(0 0 30px rgba(0,0,0,0.8)); }

        .brand-logo { font-family: 'Cinzel', serif; font-size: 2rem; color: #fff !important; letter-spacing: 6px; margin: 10px 0; }
        .perfume-sub { font-size: 0.7rem; color: var(--color) !important; letter-spacing: 4px; text-transform: uppercase; font-weight: 600; }

        .row { display: flex; align-items: center; width: 100%; padding: 50px 10%; gap: 60px; position: relative; z-index: 2; }
        .row.rev { flex-direction: row-reverse; }
        .img-box { width: 45%; }
        .img-box img { width: 100%; border-radius: 4px; display: block; box-shadow: 0 10px 30px rgba(0,0,0,0.5); }
        .txt-box { width: 55%; text-align: left; }
        .txt-box h3 { font-family: 'Cinzel', serif; font-size: 1.5rem; margin-bottom: 20px; color: var(--color) !important; letter-spacing: 2px; }
        .txt-box p { font-size: 0.95rem; line-height: 1.9; color: #f0f0f0 !important; font-weight: 300; }
        .highlight { color: var(--color) !important; font-weight: 600; }
        
        .purchase-area { max-width: 1000px; margin: 40px auto; display: flex; gap: 40px; padding: 40px; border-top: 1px solid rgba(255,255,255,0.1); width: 90%; position: relative; z-index: 2; }
        .size-box { flex: 1; padding: 15px; border: 1px solid rgba(255,255,255,0.2); text-align: center; cursor: pointer; }
        .active-size { border-color: var(--color); background: rgba(255,255,255,0.05); }

        /* Form Inputs Fix */
        .purchase-area input { 
            width: 100%; padding: 15px; margin-bottom: 10px; 
            background: rgba(255,255,255,0.05) !important; 
            border: 1px solid rgba(255,255,255,0.1) !important; 
            color: #fff !important; font-family: 'Montserrat';
        }
        .order-btn { width: 100%; padding: 20px; background: #fff !important; color: #000 !important; font-weight: 800; cursor: pointer; letter-spacing: 2px; border: none; }

        @media (max-width: 900px) { .row, .row.rev { flex-direction: column; text-align: center; padding: 40px 5%; } .img-box, .txt-box { width: 100%; } .purchase-area { flex-direction: column-reverse; } }

        /* Themes */
        .sauv-t { --color: #4A90E2; --glow-color: rgba(74, 144, 226, 0.35); }
        .stron-t { --color: #CD7F32; --glow-color: rgba(205, 127, 50, 0.35); }
        .libre-t { --color: #D4AF37; --glow-color: rgba(212, 175, 55, 0.35); }
        .gg-t { --color: #1a4d99; --glow-color: rgba(26, 77, 153, 0.35); }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>
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
            <div class="txt-box"><h3>THE LEGENDARY DEPTH</h3><p>Sauvage Elixir is an extraordinary concentration, a masterpiece of wild freshness.</p></div>
        </div>
        <div class="purchase-area">
            <div style="flex:1">
                <div class="size-container" style="display:flex; gap:10px;">
                    <div class="size-box" onclick="selectSize(this, 199, 'sec1')">5ML</div>
                    <div class="size-box active-size" onclick="selectSize(this, 319, 'sec1')">10ML</div>
                </div>
            </div>
            <div style="flex:1.2">
                <form><input name="name" placeholder="FULL NAME"><input name="phone" placeholder="PHONE NUMBER"><input name="city" placeholder="CITY"><button type="button" class="order-btn" onclick="sendOrder('sec1', 'SAUVAGE ELIXIR')">ORDER NOW | 319 DH</button></form>
            </div>
        </div>
    </section>

    <div id="chat-trigger-final" style="position: fixed; bottom: 20px; left: 20px; width: 60px; height: 60px; background: #fff; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; z-index: 10005; box-shadow: 0 4px 15px rgba(0,0,0,0.3);">
        <img src="https://cdn-icons-png.flaticon.com/512/134/134914.png" width="30">
    </div>

    <div id="chat-box-final" style="display: none; position: fixed; bottom: 90px; left: 20px; width: 320px; height: 450px; background: #000; border: 1px solid #333; border-radius: 15px; flex-direction: column; z-index: 10005; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.5);">
        <div style="background: #fff; color: #000; padding: 15px; font-weight: bold; display: flex; justify-content: space-between;">
            <span>VELOORIA AI</span>
            <span id="close-chat-final" style="cursor: pointer;">✕</span>
        </div>
        <div id="chat-msgs-final" style="flex: 1; padding: 15px; overflow-y: auto; display: flex; flex-direction: column; gap: 10px;">
            <div style="background: #222; padding: 10px; border-radius: 10px; align-self: flex-start; font-size: 0.85rem;">أهلاً بك فـ Velooria! ✨ كيف نقدر نعاونك اليوم؟</div>
        </div>
        <div style="padding: 10px; border-top: 1px solid #333; display: flex; background: #111;">
            <input id="chat-input-final" type="text" placeholder="كتب ميساج..." style="flex: 1; background: transparent; border: 1px solid #333 !important; color: #fff; padding: 8px; border-radius: 5px;">
            <button id="send-btn-final" style="background: #fff; color: #000; margin-left: 5px; padding: 8px 15px; border-radius: 5px; font-weight: bold; cursor: pointer;">صيفط</button>
        </div>
    </div>

    <script>
        // 1. Logic of Sections & Scrolling
        const sections = ['sec1', 'sec2', 'sec3', 'sec4'];
        const colors = ['#4A90E2', '#CD7F32', '#D4AF37', '#1a4d99'];
        let currentIdx = 0;

        window.addEventListener('scroll', () => {
            sections.forEach((id, index) => {
                const rect = document.getElementById(id).getBoundingClientRect();
                if(rect.top >= -window.innerHeight/2 && rect.top <= window.innerHeight/2) {
                    currentIdx = index;
                    document.documentElement.style.setProperty('--current-arrow-color', colors[index]);
                    const arrow = document.querySelector('.arrow-icon');
                    if(index === sections.length - 1) arrow.classList.add('arrow-up');
                    else arrow.classList.remove('arrow-up');
                }
            });
        });

        document.getElementById('scrollBtn').onclick = () => {
            if(currentIdx === sections.length - 1) window.scrollTo({top: 0, behavior: 'smooth'});
            else window.scrollTo({top: document.getElementById(sections[currentIdx+1]).offsetTop - 70, behavior: 'smooth'});
        };

        function selectSize(el, price, secId) {
            const sec = document.getElementById(secId);
            sec.querySelectorAll('.size-box').forEach(b => b.classList.remove('active-size'));
            el.classList.add('active-size');
            sec.querySelector('.order-btn').innerText = `ORDER NOW | ${price} DH`;
        }

        // 2. Chatbot Logic
        const API_KEY = "AIzaSyDNR5p5cQYntUfOBM4ox9E_th2ZNWJ0awl";
        const trigger = document.getElementById('chat-trigger-final');
        const box = document.getElementById('chat-box-final');
        const close = document.getElementById('close-chat-final');
        const input = document.getElementById('chat-input-final');
        const send = document.getElementById('send-btn-final');
        const msgs = document.getElementById('chat-msgs-final');

        trigger.onclick = () => box.style.display = box.style.display === 'none' ? 'flex' : 'none';
        close.onclick = () => box.style.display = 'none';

        async function getAIResponse(userText) {
            const system = "أنت مساعد مبيعات في متجر Velooria للعطور. جاوب بالدارجة المغربية فقط. كن مؤدب ومقنع.";
            try {
                const r = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=${API_KEY}`, {
                    method: 'POST',
                    headers: {'Content-Type': 'application/json'},
                    body: JSON.stringify({ contents: [{ parts: [{ text: system + "\nUser: " + userText }] }] })
                });
                const d = await r.json();
                return d.candidates[0].content.parts[0].text;
            } catch(e) { return "سمح ليا وقع مشكل، عاود صيفط الميساج."; }
        }

        send.onclick = async () => {
            const text = input.value.trim();
            if(!text) return;

            msgs.innerHTML += `<div style="background: #fff; color: #000; padding: 10px; border-radius: 10px; align-self: flex-end; font-size: 0.85rem;">${text}</div>`;
            input.value = "";
            
            const wait = document.createElement('div');
            wait.innerText = "جاري الرد...";
            msgs.appendChild(wait);
            
            const aiRes = await getAIResponse(text);
            wait.remove();
            
            msgs.innerHTML += `<div style="background: #222; padding: 10px; border-radius: 10px; align-self: flex-start; font-size: 0.85rem;">${aiRes}</div>`;
            msgs.scrollTop = msgs.scrollHeight;
        };
    </script>
</body>
</html>
