<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Velooria AI Chat</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap" rel="stylesheet">
    <style>
        body { margin: 0; background: #000; color: #fff; font-family: 'Montserrat', sans-serif; }
        #chat-trigger { position: fixed; bottom: 20px; left: 20px; width: 60px; height: 60px; background: #fff; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; z-index: 1000; }
        #chat-window { display: none; position: fixed; bottom: 90px; left: 20px; width: 320px; height: 450px; background: #0b0b0b; border: 1px solid #333; border-radius: 15px; flex-direction: column; z-index: 1000; overflow: hidden; }
        #chat-header { background: #fff; color: #000; padding: 15px; font-weight: bold; display: flex; justify-content: space-between; }
        #chat-msgs { flex: 1; padding: 15px; overflow-y: auto; display: flex; flex-direction: column; gap: 10px; }
        .msg-ai { background: #222; color: #fff; padding: 10px; border-radius: 10px 10px 10px 0; align-self: flex-start; font-size: 0.85rem; max-width: 85%; }
        .msg-user { background: #fff; color: #000; padding: 10px; border-radius: 10px 10px 0 10px; align-self: flex-end; font-size: 0.85rem; max-width: 85%; }
        .chat-input-area { padding: 10px; border-top: 1px solid #222; display: flex; gap: 5px; }
        #chat-input { flex: 1; background: #1a1a1a; border: 1px solid #333; color: #fff; padding: 8px; border-radius: 5px; outline: none; }
        #send-btn { background: #fff; color: #000; border: none; padding: 8px 15px; border-radius: 5px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>

    <div id="chat-trigger">💬</div>

    <div id="chat-window">
        <div id="chat-header">
            <span>VELOORIA AI</span>
            <span id="close-chat" style="cursor: pointer;">&times;</span>
        </div>
        <div id="chat-msgs">
            <div class="msg-ai">أهلاً بك فـ Velooria! ✨ كيف نقدر نعاونك؟</div>
        </div>
        <div class="chat-input-area">
            <input id="chat-input" type="text" placeholder="كتب ميساج...">
            <button id="send-btn">صيفط</button>
        </div>
    </div>

    <script>
        // --- 1. CONFIGURATION ---
        // تنبيه: المفتاح القديم غالباً تبللوكا حيت منشور فـ GitHub
        const API_KEY = "حط_هنا_المفتاح_الجديد"; 

        const trigger = document.getElementById('chat-trigger');
        const windowChat = document.getElementById('chat-window');
        const closeBtn = document.getElementById('close-chat');
        const input = document.getElementById('chat-input');
        const sendBtn = document.getElementById('send-btn');
        const msgsBox = document.getElementById('chat-msgs');

        trigger.onclick = () => windowChat.style.display = (windowChat.style.display === 'none') ? 'flex' : 'none';
        closeBtn.onclick = () => windowChat.style.display = 'none';

        // --- 2. AI FUNCTION (CORRECTED) ---
        async function fetchAI(text) {
            try {
                // استعملنا gemini-1.5-pro حيت أتبت فالمناطق اللي فيها قيود
                const response = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-pro:generateContent?key=${API_KEY}`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        contents: [{ 
                            parts: [{ 
                                text: "أنت مساعد مبيعات في Velooria. جاوب بالدارجة المغربية فقط باختصار. السؤال: " + text 
                            }] 
                        }]
                    })
                });

                const data = await response.json();
                
                // تشخيص الخطأ فـ الـ Console (مهم بزاف)
                if (data.error) {
                    console.error("Google API Error:", data.error.message);
                    return "كاين مشكل فالمفتاح (API Key). تأكد منه فـ Google AI Studio.";
                }

                if (data.candidates && data.candidates[0].content) {
                    return data.candidates[0].content.parts[0].text;
                }
                return "سمح ليا، عاود صيفط الميساج.";
            } catch (err) {
                console.error("Fetch Error:", err);
                return "وقع مشكل فالاتصال.";
            }
        }

        // --- 3. SEND LOGIC ---
        sendBtn.onclick = async () => {
            const val = input.value.trim();
            if (!val) return;

            msgsBox.innerHTML += `<div class="msg-user">${val}</div>`;
            input.value = "";
            msgsBox.scrollTop = msgsBox.scrollHeight;

            const aiRes = await fetchAI(val);
            msgsBox.innerHTML += `<div class="msg-ai">${aiRes}</div>`;
            msgsBox.scrollTop = msgsBox.scrollHeight;
        };

        input.onkeypress = (e) => { if(e.key === 'Enter') sendBtn.click(); };
    </script>
</body>
</html>
