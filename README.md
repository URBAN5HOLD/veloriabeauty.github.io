<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria Beauty | Official Store</title>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* ستايل الصفحة الأساسي */
        body { margin: 0; background: #000; color: #fff; font-family: 'Montserrat', sans-serif; overflow-x: hidden; }
        .logo-fixed { position: fixed; top: 0; width: 100%; text-align: center; padding: 20px; background: #000; z-index: 100; font-family: 'Cinzel', serif; letter-spacing: 5px; }
        
        /* ستايل الشات */
        #chat-trigger { position: fixed; bottom: 20px; left: 20px; width: 60px; height: 60px; background: #fff; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; z-index: 1000; box-shadow: 0 4px 15px rgba(0,0,0,0.5); }
        #chat-window { display: none; position: fixed; bottom: 90px; left: 20px; width: 320px; height: 450px; background: #0b0b0b; border: 1px solid #333; border-radius: 15px; flex-direction: column; z-index: 1000; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,1); }
        #chat-header { background: #fff; color: #000; padding: 15px; font-weight: bold; display: flex; justify-content: space-between; align-items: center; }
        #chat-msgs { flex: 1; padding: 15px; overflow-y: auto; display: flex; flex-direction: column; gap: 10px; background: #000; }
        .msg-ai { background: #222; color: #fff; padding: 10px 15px; border-radius: 15px 15px 15px 0; align-self: flex-start; font-size: 0.85rem; max-width: 85%; border: 1px solid #333; }
        .msg-user { background: #fff; color: #000; padding: 10px 15px; border-radius: 15px 15px 0 15px; align-self: flex-end; font-size: 0.85rem; max-width: 85%; }
        .chat-input-area { padding: 15px; border-top: 1px solid #222; display: flex; gap: 10px; background: #0b0b0b; }
        #chat-input { flex: 1; background: #1a1a1a; border: 1px solid #333; color: #fff; padding: 10px; border-radius: 5px; outline: none; }
        #send-btn { background: #fff; color: #000; border: none; padding: 10px 15px; border-radius: 5px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>

    <div class="logo-fixed">VELOORIA</div>

    <div id="chat-trigger">
        <img src="https://cdn-icons-png.flaticon.com/512/134/134914.png" width="30" style="filter: invert(1);">
    </div>

    <div id="chat-window">
        <div id="chat-header">
            <span>VELOORIA AI</span>
            <span id="close-chat" style="cursor: pointer; font-size: 20px;">&times;</span>
        </div>
        <div id="chat-msgs">
            <div class="msg-ai">أهلاً بك فـ Velooria! ✨ كيف نقدر نعاونك اليوم؟</div>
        </div>
        <div class="chat-input-area">
            <input id="chat-input" type="text" placeholder="كتب ميساj...">
            <button id="send-btn">صيفط</button>
        </div>
    </div>

    <script>
        // 1. الإعدادات (مصلحة بالكامل)
        const API_KEY = "AIzaSyDNR5p5cQYntUfOBM4ox9E_th2ZNWJ0awl";
        const BOT_TOKEN = "8751066528:AAG3zm-hNENKPnAqEAHb1zBsFVSB6mVatT8";
        const CHAT_ID = "7635707772";

        const trigger = document.getElementById('chat-trigger');
        const windowChat = document.getElementById('chat-window');
        const closeBtn = document.getElementById('close-chat');
        const input = document.getElementById('chat-input');
        const sendBtn = document.getElementById('send-btn');
        const msgsContainer = document.getElementById('chat-msgs');

        // 2. تفتيح وشد الشات
        trigger.onclick = () => {
            windowChat.style.display = (windowChat.style.display === 'none' || windowChat.style.display === '') ? 'flex' : 'none';
        };
        closeBtn.onclick = () => windowChat.style.display = 'none';

        // 3. وظيفة جلب الجواب من Gemini
        async function getGeminiResponse(userText) {
            try {
                const response = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash:generateContent?key=${API_KEY}`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        contents: [{
                            parts: [{ text: "أنت مساعد مبيعات في متجر عطور Velooria. جاوب بالدارجة المغربية فقط وبأسلوب راقي. المستخدم يسأل: " + userText }]
                        }]
                    })
                });

                const data = await response.json();
                // التأكد من أن الجواب وصل بشكل صحيح
                if (data.candidates && data.candidates[0].content.parts[0].text) {
                    return data.candidates[0].content.parts[0].text;
                }
                return "سمحي ليا، وقع مشكل بسيط. عاودي صيفطي الميساج.";
            } catch (error) {
                console.error("Error:", error);
                return "وقع مشكل فالاتصال. تأكدي من الأنترنت.";
            }
        }

        // 4. إرسال الرسالة
        sendBtn.onclick = async () => {
            const text = input.value.trim();
            if (!text) return;

            // عرض رسالة المستخدم
            msgsContainer.innerHTML += `<div class="msg-user">${text}</div>`;
            input.value = "";
            msgsContainer.scrollTop = msgsContainer.scrollHeight;

            // جلب وعرض رد الذكاء الاصطناعي
            const aiResponse = await getGeminiResponse(text);
            msgsContainer.innerHTML += `<div class="msg-ai">${aiResponse}</div>`;
            msgsContainer.scrollTop = msgsContainer.scrollHeight;

            // إشعار تلغرام إذا كان هناك رقم هاتف
            if (/(06|07|05)\d{8}/.test(text)) {
                fetch(`https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ chat_id: CHAT_ID, text: `⚠️ زبون وضع رقمه في الشات: ${text}` })
                });
            }
        };

        // الإرسال بزر Enter
        input.onkeypress = (e) => { if (e.key === 'Enter') sendBtn.click(); };
    </script>
</body>
</html>
