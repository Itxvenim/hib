<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sorry My Love</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background: linear-gradient(135deg, #ffe6f2, #ffb3d9, #ff69b4);
            color: #333;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
            animation: backgroundPulse 5s ease-in-out infinite;
        }
        @keyframes backgroundPulse {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        .page {
            display: none;
            height: 100vh;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 20px;
            position: relative;
        }
        .page.active {
            display: flex;
        }
        .emoji {
            font-size: 3em;
            margin: 10px;
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
        .button {
            background: linear-gradient(45deg, #ff69b4, #ff1493, #ffb3d9);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            border-radius: 50px;
            cursor: pointer;
            margin-top: 20px;
            transition: all 0.3s;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            font-family: 'Dancing Script', cursive;
        }
        .button:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 12px rgba(0,0,0,0.3);
            animation: sparkle 1s infinite;
        }
        @keyframes sparkle {
            0% { filter: brightness(1); }
            50% { filter: brightness(1.2); }
            100% { filter: brightness(1); }
        }
        .letter-button {
            background: linear-gradient(45deg, #ff69b4, #ffb3d9);
            border: 3px solid #ff1493;
            padding: 20px;
            border-radius: 15px;
            max-width: 300px;
            margin: 20px auto;
            cursor: pointer;
            font-size: 1.5em;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }
        .letter-button:hover {
            transform: scale(1.05);
        }
        .letter {
            background: linear-gradient(135deg, #ff6b6b, #ff8e53, #ff4757);
            border: 5px double #ff1493;
            padding: 60px;
            border-radius: 30px;
            max-width: 1000px;
            margin: 20px auto;
            font-size: 1.5em;
            line-height: 1.8;
            box-shadow: 0 15px 30px rgba(0,0,0,0.4);
            position: relative;
            overflow: hidden;
            display: none;
            animation: fadeIn 1s ease-in-out;
            color: #fff;
            font-family: 'Dancing Script', cursive;
        }
        .letter::before {
            content: "💌 🌸 💖 🐱 🌹 💕 🥰";
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 1.5em;
            z-index: 1;
            opacity: 0.6;
        }
        .letter::after {
            content: "🐱 💖 🌸 🐾 💕 🌹 🥺";
            position: absolute;
            bottom: 10px;
            left: 10px;
            font-size: 1.5em;
            z-index: 1;
            opacity: 0.6;
        }
        @keyframes fadeIn {
            0% { opacity: 0; transform: scale(0.9) rotateY(180deg); }
            100% { opacity: 1; transform: scale(1) rotateY(0deg); }
        }
        .flower {
            position: absolute;
            font-size: 2.5em;
            animation: fall 5s linear infinite;
            pointer-events: none;
            z-index: 10;
        }
        @keyframes fall {
            0% { top: -50px; opacity: 1; transform: rotate(0deg) scale(1); }
            100% { top: 100vh; opacity: 0; transform: rotate(360deg) scale(0.5); }
        }
        .heart {
            position: absolute;
            font-size: 2em;
            animation: float 4s ease-in-out infinite;
            pointer-events: none;
            z-index: 10;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-30px) rotate(180deg); }
        }
        .cat-image {
            width: 250px;
            height: auto;
            margin-bottom: 20px;
            border-radius: 50%;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            animation: wiggle 2s infinite;
        }
        @keyframes wiggle {
            0%, 7% { transform: rotateZ(0); }
            15% { transform: rotateZ(-15deg); }
            20% { transform: rotateZ(10deg); }
            25% { transform: rotateZ(-10deg); }
            30% { transform: rotateZ(6deg); }
            35% { transform: rotateZ(-4deg); }
            40%, 100% { transform: rotateZ(0); }
        }
        .bouquet-image {
            width: 180px;
            height: auto;
            margin-top: 10px;
            animation: sway 3s ease-in-out infinite;
        }
        @keyframes sway {
            0%, 100% { transform: rotate(-5deg); }
            50% { transform: rotate(5deg); }
        }
        .stylish-text {
            font-family: 'Dancing Script', cursive;
            font-size: 3em;
            color: #ff69b4;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.2);
            animation: glow 2s ease-in-out infinite alternate;
        }
        @keyframes glow {
            from { text-shadow: 3px 3px 6px rgba(0,0,0,0.2); }
            to { text-shadow: 3px 3px 6px rgba(255,105,180,0.8); }
        }
        .final-message {
            font-size: 3em;
            color: #ff1493;
            display: none;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.2);
            animation: pulse 1s infinite;
            font-family: 'Dancing Script', cursive;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        .party-popper {
            font-size: 5em;
            position: absolute;
            animation: pop 1.5s ease-in-out;
            z-index: 10;
        }
        .left-popper {
            left: 5%;
            top: 30%;
        }
        .right-popper {
            right: 5%;
            top: 30%;
        }
        @keyframes pop {
            0% { transform: scale(0) rotate(0deg); opacity: 0; }
            50% { transform: scale(1.2) rotate(180deg); opacity: 1; }
            100% { transform: scale(1) rotate(360deg); opacity: 1; }
        }
        .confetti {
            position: absolute;
            font-size: 1.5em;
            animation: confettiFall 6s linear infinite;
            pointer-events: none;
            z-index: 10;
        }
        @keyframes confettiFall {
            0% { top: -10px; opacity: 1; transform: rotate(0deg); }
            100% { top: 100vh; opacity: 0; transform: rotate(720deg); }
        }
        .sorry-text {
            font-family: 'Dancing Script', cursive;
            font-size: 2.5em;
            color: #ff69b4;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            animation: fadeInUp 2s ease-in-out;
        }
        @keyframes fadeInUp {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(0); }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Page 1: Intro with Stylish Text -->
    <div id="page1" class="page active">
        <div class="emoji">🐱 💕 🙏 🌸 🐾</div>
        <p class="sorry-text">I'm so sorry, my love! Please forgive me. 💖 🌹 🥺</p>
        <div class="emoji">💌 💕 🐱</div>
        <button class="button" onclick="nextPage(2)">Next 💖 🌸</button>
    </div>

    <!-- Page 2: Letter -->
    <div id="page2" class="page">
        <div class="emoji">💌 🌹 💖 🐱</div>
        <p>Click the cute envelope to open my heartfelt apology! 💕 🌸</p>
        <div class="letter-button" id="letter-button" onclick="openLetter()">
            <div class="emoji">💌</div>
            <p>Open My Letter 💖</p>
        </div>
        <div class="letter" id="letter">
            <div id="letter-content">
                Begam i wana say the sorry to you bcz i dont wanna lose you in every condition i am addicted to you and you know thi sbetter you are addicted to me ham dono eik dosare ke begar ni rah sakta bass ham larne lag jate jaldi yarr ap plz meri bat man lya karo ma jo kah raha hota ho souch samaj ke kah raha hota ho so plzz ap meri bat ka gussa jaldi na kya kare ager ham eik dosare se bate chupay ge to ase kam ni chale ga ham waha tak jane ke lya eik dosare ko hazar bar maff karna hoga uske begar ni hoga or ma wah tak apn asafar leke jana chata ho bass ap mere upper ankhe band kar ke yaqeen karo ma waah tak in sha allah safar leke jao ga bass ap chor ke mat jana or mere upper yaqeen rakho 💕 🌸 🐱 💖
            </div>
        </div>
        <button class="button" id="next-btn" style="display: none;" onclick="nextPage(3)">Next 💕 🌸</button>
    </div>

    <!-- Page 3: Final Apology -->
    <div id="page3" class="page">
        <div id="cat-section">
            <img src="https://via.placeholder.com/250x250/ffb3d9/ffffff?text=Cute+Cat" alt="Cute Cat" class="cat-image">
            <p class="stylish-text">plss accept this 💐 🌸</p>
            <img src="https://via.placeholder.com/180x250/ff69b4/ffffff?text=Bouquet" alt="Bouquet" class="bouquet-image">
            <div class="emoji">💐 🌸 💖 🐱</div>
            <button class="button" onclick="accept()">Accept 💖 🌹</button>
        </div>
        <div class="final-message" id="final-message">
            <p>Love you so much wifey! 💕 🐱 🌸 💖 🥰 🎉</p>
        </div>
        <div class="party-popper left-popper" id="left-popper" style="display: none;">🎉</div>
        <div class="party-popper right-popper" id="right-popper" style="display: none;">🎉</div>
    </div>

    <script>
        function nextPage(pageNum) {
            document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
            document.getElementById('page' + pageNum).classList.add('active');
        }

        function openLetter() {
            document.getElementById('letter-button').style.display = 'none';
            document.getElementById('letter').style.display = 'block';
            document.getElementById('next-btn').style.display = 'block';
            // Add falling flowers, hearts, and emojis
            const emojis = ['🌸', '💖', '🐱', '🌹', '💕'];
            for (let i = 0; i < 20; i++) {
                const flower = document.createElement('div');
                flower.className = 'flower';
                flower.textContent = emojis[Math.floor(Math.random() * emojis.length)];
                flower.style.left = Math.random() * 100 + '%';
                flower.style.animationDelay = Math.random() * 3 + 's';
                document.body.appendChild(flower);
                setTimeout(() => flower.remove(), 5000);

                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.textContent = '💖';
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDelay = Math.random() * 3 + 's';
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 4000);
            }
        }

        function accept() {
            document.getElementById('cat-section').style.display = 'none';
            document.getElementById('final-message').style.display = 'block';
            document.getElementById('left-popper').style.display = 'block';
            document.getElementById('right-popper').style.display = 'block';
            // Add falling flowers, hearts, confetti, and emojis
            const emojis = ['🌸', '💖', '🐱', '🌹', '💕', '🎉', '✨'];
            for (let i = 0; i < 30; i++) {
                const flower = document.createElement('div');
                flower.className = 'flower';
                flower.textContent = emojis[Math.floor(Math.random() * emojis.length)];
                flower.style.left = Math.random() * 100 + '%';
                flower.style.animationDelay = Math.random() * 3 + 's';
                document.body.appendChild(flower);
                setTimeout(() => flower.remove(), 6000);

                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.textContent = '💖';
                heart.style.left = Math.random() * 100 + '%';
                heart.style.animationDelay = Math.random() * 3 + 's';
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 4000);

                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.textContent = ['🎊', '✨', '🎉', '💫'][Math.floor(Math.random() * 4)];
                confetti.style.left = Math.random() * 100 + '%';
                confetti.style.animationDelay = Math.random() * 3 + 's';
                document.body.appendChild(confetti);
                setTimeout(() => confetti.remove(), 6000);
            }
        }
    </script>
</body>
</html>
