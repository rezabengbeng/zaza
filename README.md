<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surat Motivasi untuk Risma</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Dancing+Script:wght@400;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }

        /* Animated Ocean Background */
        .ocean-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            overflow: hidden;
            z-index: -1;
        }

        .wave {
            position: absolute;
            width: 200%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 300"><path d="M0,160 C150,200 350,0 500,160 C650,320 850,120 1000,160 L1000,300 L0,300 Z" fill="%23ffffff" fill-opacity="0.1"/></svg>');
            background-size: 1000px 300px;
            animation: wave-animation 20s linear infinite;
        }

        .wave:nth-child(2) {
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 300"><path d="M0,200 C150,240 350,40 500,200 C650,360 850,160 1000,200 L1000,300 L0,300 Z" fill="%23ffffff" fill-opacity="0.05"/></svg>');
            background-size: 1000px 300px;
            animation: wave-animation 15s linear infinite reverse;
            animation-delay: -5s;
        }

        .wave:nth-child(3) {
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 300"><path d="M0,180 C150,220 350,20 500,180 C650,340 850,140 1000,180 L1000,300 L0,300 Z" fill="%23ffffff" fill-opacity="0.03"/></svg>');
            background-size: 1000px 300px;
            animation: wave-animation 25s linear infinite;
            animation-delay: -10s;
        }

        @keyframes wave-animation {
            0% { transform: translateX(0); }
            100% { transform: translateX(-1000px); }
        }

        /* Floating particles */
        .particle {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            pointer-events: none;
            animation: float-particles 8s linear infinite;
        }

        @keyframes float-particles {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }

        .container {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 100vh;
        }

        /* Letter Symbol */
        .letter-symbol {
            width: 120px;
            height: 120px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            position: relative;
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255, 255, 255, 0.3);
        }

        .letter-symbol:hover {
            transform: scale(1.1) rotate(5deg);
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
        }

        .letter-symbol::before {
            content: '';
            position: absolute;
            top: -5px;
            left: -5px;
            right: -5px;
            bottom: -5px;
            background: linear-gradient(45deg, #667eea, #764ba2, #667eea);
            border-radius: 25px;
            z-index: -1;
            animation: rotate-border 3s linear infinite;
            opacity: 0.5;
        }

        @keyframes rotate-border {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .letter-icon {
            font-size: 4rem;
            color: #2a5298;
            animation: pulse-icon 2s ease-in-out infinite;
        }

        @keyframes pulse-icon {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        /* Message Modal */
        .message-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(5px);
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 1000;
        }

        .message-modal.active {
            opacity: 1;
            visibility: visible;
        }

        .message-content {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 60px;
            text-align: center;
            position: relative;
            max-width: 600px;
            width: 90%;
            transform: scale(0.5) rotate(10deg);
            transition: all 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            box-shadow: 0 40px 80px rgba(0, 0, 0, 0.3);
            border: 2px solid rgba(255, 255, 255, 0.5);
        }

        .message-modal.active .message-content {
            transform: scale(1) rotate(0deg);
        }

        .message-content::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            right: -20px;
            bottom: -20px;
            background: linear-gradient(45deg, #667eea, #764ba2, #667eea, #764ba2);
            border-radius: 35px;
            z-index: -1;
            animation: rainbow-border 4s linear infinite;
            opacity: 0.3;
        }

        @keyframes rainbow-border {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .message-text {
            font-family: 'Dancing Script', cursive;
            font-size: 3rem;
            color: #2a5298;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
            animation: text-glow 3s ease-in-out infinite;
        }

        @keyframes text-glow {
            0%, 100% { text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1); }
            50% { text-shadow: 2px 2px 20px rgba(42, 82, 152, 0.5); }
        }

        .message-subtitle {
            font-size: 1.2rem;
            color: #667eea;
            margin-bottom: 40px;
            font-weight: 400;
        }

        .close-btn {
            position: absolute;
            top: 20px;
            right: 25px;
            background: none;
            border: none;
            font-size: 2rem;
            color: #2a5298;
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: all 0.3s ease;
        }

        .close-btn:hover {
            background: rgba(42, 82, 152, 0.1);
            transform: rotate(90deg);
        }

        .decorative-elements {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .heart {
            position: absolute;
            color: #ff6b9d;
            font-size: 1.5rem;
            animation: float-hearts 6s linear infinite;
        }

        @keyframes float-hearts {
            0% {
                transform: translateY(100%) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100%) rotate(360deg);
                opacity: 0;
            }
        }

        .sparkle {
            position: absolute;
            color: #ffd700;
            font-size: 1rem;
            animation: twinkle 2s ease-in-out infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0; transform: scale(0); }
            50% { opacity: 1; transform: scale(1); }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .letter-symbol {
                width: 100px;
                height: 100px;
            }
            
            .letter-icon {
                font-size: 3rem;
            }
            
            .message-content {
                padding: 40px 30px;
            }
            
            .message-text {
                font-size: 2.5rem;
            }
            
            .message-subtitle {
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            .message-content {
                padding: 30px 20px;
            }
            
            .message-text {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Ocean Background -->
    <div class="ocean-container">
        <div class="wave"></div>
        <div class="wave"></div>
        <div class="wave"></div>
    </div>

    <!-- Main Container -->
    <div class="container">
        <!-- Letter Symbol -->
        <div class="letter-symbol" onclick="openMessage()">
            <div class="letter-icon">💌</div>
        </div>
    </div>

    <!-- Message Modal -->
    <div class="message-modal" id="messageModal">
        <div class="message-content">
            <button class="close-btn" onclick="closeMessage()">×</button>
            <div class="message-text">
                Semangat ngonten nya Captain Risma wkwkwk
            </div>
            <div class="message-subtitle">
                ✨ Keep creating amazing content ! ✨
            </div>
            <div class="decorative-elements">
                <div class="sparkle" style="top: 20%; left: 10%;">⭐</div>
                <div class="sparkle" style="top: 30%; right: 15%;">✨</div>
                <div class="sparkle" style="bottom: 25%; left: 20%;">⭐</div>
                <div class="sparkle" style="bottom: 35%; right: 25%;">✨</div>
            </div>
        </div>
    </div>

    <script>
        // Open message modal
        function openMessage() {
            const modal = document.getElementById('messageModal');
            modal.classList.add('active');
            
            // Add some celebratory effects
            createHearts();
            createParticles();
        }

        // Close message modal
        function closeMessage() {
            const modal = document.getElementById('messageModal');
            modal.classList.remove('active');
        }

        // Close modal when clicking outside
        document.getElementById('messageModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeMessage();
            }
        });

        // Create floating hearts
        function createHearts() {
            for (let i = 0; i < 15; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.innerHTML = '💖';
                    heart.style.left = Math.random() * 100 + '%';
                    heart.style.animationDelay = Math.random() * 2 + 's';
                    heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
                    document.body.appendChild(heart);
                    
                    setTimeout(() => {
                        heart.remove();
                    }, 7000);
                }, i * 200);
            }
        }

        // Create floating particles
        function createParticles() {
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const particle = document.createElement('div');
                    particle.className = 'particle';
                    particle.style.left = Math.random() * 100 + '%';
                    particle.style.width = Math.random() * 8 + 4 + 'px';
                    particle.style.height = particle.style.width;
                    particle.style.animationDelay = Math.random() * 3 + 's';
                    particle.style.animationDuration = (Math.random() * 4 + 6) + 's';
                    document.body.appendChild(particle);
                    
                    setTimeout(() => {
                        particle.remove();
                    }, 10000);
                }, i * 100);
            }
        }

        // Auto-create ambient particles
        setInterval(createParticles, 15000);

        // Keyboard shortcuts
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                closeMessage();
            }
            if (e.key === 'Enter' || e.key === ' ') {
                if (!document.getElementById('messageModal').classList.contains('active')) {
                    openMessage();
                }
            }
        });

        // Add some interactive sparkles on mouse move
        document.addEventListener('mousemove', function(e) {
            if (Math.random() < 0.1) {
                const sparkle = document.createElement('div');
                sparkle.innerHTML = '✨';
                sparkle.style.position = 'fixed';
                sparkle.style.left = e.clientX + 'px';
                sparkle.style.top = e.clientY + 'px';
                sparkle.style.pointerEvents = 'none';
                sparkle.style.fontSize = '12px';
                sparkle.style.color = '#ffd700';
                sparkle.style.animation = 'twinkle 1s ease-out';
                sparkle.style.zIndex = '999';
                document.body.appendChild(sparkle);
                
                setTimeout(() => {
                    sparkle.remove();
                }, 1000);
            }
        });

        // Initialize ambient particles
        createParticles();
    </script>
</body>
</html>
