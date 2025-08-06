<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 20th Birthday My Love</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@700;900&family=Montserrat:wght@700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #0f0f0f;
            color: #e0e0e0;
            overflow-x: hidden;
        }
        .heart {
            position: absolute;
            pointer-events: none;
            animation: float 4s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }
        .page {
            min-height: 100vh;
            padding: 2rem;
            display: none;
        }
        .active-page {
            display: block;
            animation: fadeIn 1s ease-in;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .nav-btn {
            transition: all 0.3s ease;
        }
        .nav-btn:hover {
            transform: scale(1.1);
        }
        .photo-card {
            transform-style: preserve-3d;
            transition: transform 0.5s ease;
        }
        .photo-card:hover {
            transform: translateZ(10px);
        }
    </style>
</head>
<body class="relative">
    <!-- Background Hearts Animation -->
    <div id="hearts-container"></div>

    <!-- Audio Player -->
    <audio id="bg-music" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>

    <!-- Navigation -->
    <nav class="fixed bottom-0 left-0 right-0 bg-black bg-opacity-70 backdrop-blur-sm z-50 p-4">
        <div class="flex justify-center space-x-6">
            <button onclick="showPage('home')" class="nav-btn text-pink-400 font-bold">
                Home
            </button>
            <button onclick="showPage('gallery')" class="nav-btn text-pink-400 font-bold">
                Gallery
            </button>
            <button onclick="showPage('message')" class="nav-btn text-pink-400 font-bold">
                Message
            </button>
            <button onclick="showPage('moments')" class="nav-btn text-pink-400 font-bold">
                Moments
            </button>
        </div>
    </nav>

    <!-- Home Page -->
    <div id="home" class="page active-page flex flex-col items-center justify-center text-center">
        <div class="max-w-2xl mx-auto">
            <h1 class="text-5xl md:text-7xl font-black text-transparent bg-clip-text bg-gradient-to-r from-pink-400 to-red-600 mb-6">
                Happy 20th Birthday
            </h1>
            <p class="text-xl md:text-2xl mb-8 font-bold text-gray-300">
                For The Most Beautiful Woman In My Life
            </p>
            <div class="relative">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/296e6cbc-45b9-400d-9ca6-a0273760392e.png" 
                     alt="Couple silhouette against a romantic sunset with heart-shaped clouds in the sky" 
                     class="rounded-xl shadow-2xl border-4 border-pink-500 mx-auto w-full max-w-md">
                <div class="absolute -inset-4 border-pink-300 border-2 rounded-xl opacity-70 animate-pulse"></div>
            </div>
            <button onclick="createHearts(50)" class="mt-10 px-8 py-3 bg-gradient-to-r from-pink-500 to-red-600 rounded-full font-bold text-white text-lg hover:scale-105 transition-all duration-300 shadow-lg hover:shadow-pink-500/30">
                Click for Love!
            </button>
        </div>
    </div>

    <!-- Gallery Page -->
    <div id="gallery" class="page">
        <h1 class="text-4xl md:text-6xl font-black text-center mb-12 text-transparent bg-clip-text bg-gradient-to-r from-pink-400 to-red-600">
            Our Precious Moments
        </h1>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 px-4">
            <!-- Photo 1 -->
            <div class="photo-card bg-gray-900 rounded-xl p-4 shadow-2xl hover:shadow-pink-500/30 transition-all">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a7cbbf6f-d158-4813-83a2-0df9a7f05438.png" 
                     alt="Black and white portrait of a happy couple laughing together in a park with bokeh lights in background" 
                     class="w-full h-64 object-cover rounded-lg mb-4">
                <h3 class="text-xl font-bold text-pink-400">First Date</h3>
                <p class="text-gray-300">The day our story began</p>
            </div>
            
            <!-- Photo 2 -->
            <div class="photo-card bg-gray-900 rounded-xl p-4 shadow-2xl hover:shadow-pink-500/30 transition-all">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/e56aa707-4a74-42c9-afe9-fe0338c497c5.png" 
                     alt="Romantic candlelight dinner with wine glasses and city lights as backdrop" 
                     class="w-full h-64 object-cover rounded-lg mb-4">
                <h3 class="text-xl font-bold text-pink-400">Anniversary</h3>
                <p class="text-gray-300">Celebrating 1 year together</p>
            </div>
            
            <!-- Photo 3 -->
            <div class="photo-card bg-gray-900 rounded-xl p-4 shadow-2xl hover:shadow-pink-500/30 transition-all">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ccd3e4f7-83e5-4197-a04d-e3c016c72dd6.png" 
                     alt="Beach sunset with couple holding hands and walking along the shore" 
                     class="w-full h-64 object-cover rounded-lg mb-4">
                <h3 class="text-xl font-bold text-pink-400">Vacation</h3>
                <p class="text-gray-300">Our summer getaway</p>
            </div>
        </div>
    </div>

    <!-- Message Page -->
    <div id="message" class="page">
        <div class="max-w-4xl mx-auto p-6">
            <h1 class="text-4xl md:text-6xl font-black text-center mb-12 text-transparent bg-clip-text bg-gradient-to-r from-pink-400 to-red-600">
                My Message For You
            </h1>
            
            <div class="bg-gray-900 bg-opacity-70 rounded-xl p-8 shadow-2xl relative">
                <div class="absolute -inset-1 bg-gradient-to-r from-pink-500 to-red-600 rounded-xl opacity-30"></div>
                <div class="relative">
                    <div class="text-xl leading-relaxed space-y-4">
                        <p>My Dearest,</p>
                        
                        <p>Happy 20th birthday to the woman who fills my life with joy, laughter, and endless love. Twenty years of bringing light into the world, and the brightest days are the ones I get to spend with you.</p>
                        
                        <p>You are my greatest adventure, my favorite love story, and my safest place all in one. Every moment with you is a gift I treasure deeply.</p>
                        
                        <p>On your special day, I want you to know how incredibly special you are - not just to me, but to everyone whose life you've touched with your kindness, warmth, and beautiful spirit.</p>
                        
                        <p>Here's to another year of creating beautiful memories together. I love you more than words can express.</p>
                        
                        <p class="text-right mt-8 text-pink-400 font-bold text-2xl">Forever yours,<br>[Your Name]</p>
                    </div>
                </div>
            </div>
            
            <div class="mt-10 flex justify-center">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/9e8f7fb2-edea-4d99-a6fe-ced71eb746e0.png" 
                     alt="Romantic handwritten letter with pink roses and candlelight illumination" 
                     class="rounded-lg border-2 border-pink-500">
            </div>
        </div>
    </div>

    <!-- Moments Page -->
    <div id="moments" class="page">
        <div class="max-w-4xl mx-auto p-6">
            <h1 class="text-4xl md:text-6xl font-black text-center mb-12 text-transparent bg-clip-text bg-gradient-to-r from-pink-400 to-red-600">
                Our Countdown Moments
            </h1>
            
            <div class="space-y-10">
                <!-- Countdown Item 1 -->
                <div class="bg-gray-900 bg-opacity-70 rounded-xl p-6 shadow-2xl flex flex-col md:flex-row items-center gap-6">
                    <div class="flex-shrink-0">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/01446262-3064-499a-a30e-bc5de77816c7.png" 
                             alt="Countdown calendar with heart-shaped dates marking important relationship milestones" 
                             class="w-40 h-40 object-cover rounded-full border-4 border-pink-500">
                    </div>
                    <div>
                        <h3 class="text-2xl font-bold text-pink-400 mb-2">Days Since We Met</h3>
                        <div id="days-counter" class="text-4xl font-black mb-2">0</div>
                        <p class="text-gray-300">Every day with you has been a blessing</p>
                    </div>
                </div>
                
                <!-- Countdown Item 2 -->
                <div class="bg-gray-900 bg-opacity-70 rounded-xl p-6 shadow-2xl flex flex-col md:flex-row items-center gap-6">
                    <div class="flex-shrink-0">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/89b48d7d-d96d-4bde-84b5-cfdf650db1db.png" 
                             alt="Romantic couple silhouette with timeline of important dates in glowing text" 
                             class="w-40 h-40 object-cover rounded-full border-4 border-pink-500">
                    </div>
                    <div>
                        <h3 class="text-2xl font-bold text-pink-400 mb-2">Next Special Date</h3>
                        <div id="next-date" class="text-2xl font-black mb-2">Our Anniversary in <span id="anniversary-countdown">0</span> days</div>
                        <p class="text-gray-300">Can't wait to celebrate another milestone with you</p>
                    </div>
                </div>
            </div>
            
            <div class="mt-12 text-center">
                <button onclick="launchConfetti()" class="px-6 py-3 bg-pink-600 rounded-full font-bold text-white hover:bg-pink-700 transition-all">
                    Celebrate with Confetti!
                </button>
            </div>
        </div>
    </div>

    <script>
        // Initialize music
        document.addEventListener('DOMContentLoaded', function() {
            const music = document.getElementById('bg-music');
            music.volume = 0.3;
            music.play().catch(e => console.log("Autoplay was prevented. Please interact to play audio."));
            
            // Create initial hearts
            createHearts(15);
            
            // Set counters
            updateCountdowns();
            setInterval(updateCountdowns, 1000);
        });

        // Page navigation
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(page => {
                page.classList.remove('active-page');
            });
            document.getElementById(pageId).classList.add('active-page');
            
            // Scroll to top of the page
            window.scrollTo(0, 0);
        }

        // Create floating hearts
        function createHearts(count) {
            const container = document.getElementById('hearts-container');
            
            for (let i = 0; i < count; i++) {
                const heart = document.createElement('div');
                heart.innerHTML = '❤️';
                heart.classList.add('heart');
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.top = Math.random() * 100 + 'vh';
                heart.style.fontSize = (Math.random() * 20 + 10) + 'px';
                heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
                container.appendChild(heart);
                
                // Remove heart after animation
                setTimeout(() => {
                    heart.remove();
                }, 5000);
            }
        }

        // Update countdowns
        function updateCountdowns() {
            // Example: Days since we met (set your own date)
            const meetDate = new Date('2022-01-01');
            const today = new Date();
            const diffTime = today - meetDate;
            const diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));
            document.getElementById('days-counter').textContent = diffDays;
            
            // Example: Next anniversary countdown (set your own date)
            const nextAnniversary = new Date(today.getFullYear(), 0, 1); // January 1st
            if (today > nextAnniversary) {
                nextAnniversary.setFullYear(nextAnniversary.getFullYear() + 1);
            }
            const daysToAnniversary = Math.ceil((nextAnniversary - today) / (1000 * 60 * 60 * 24));
            document.getElementById('anniversary-countdown').textContent = daysToAnniversary;
        }

        // Confetti effect
        function launchConfetti() {
            createHearts(100);
            
            const colors = ['#ff0000', '#ff69b4', '#ff1493', '#db7093', '#ff6347'];
            
            for (let i = 0; i < 150; i++) {
                const confetti = document.createElement('div');
                confetti.classList.add('heart');
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.top = -10 + 'vh';
                confetti.style.color = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.fontSize = (Math.random() * 15 + 8) + 'px';
                confetti.innerHTML = ['❤️', '🎉', '🎊', '✨', '🎁'][Math.floor(Math.random() * 5)];
                document.getElementById('hearts-container').appendChild(confetti);
                
                gsap.to(confetti, {
                    y: '120vh',
                    x: Math.random() * 200 - 100 + 'px',
                    rotation: Math.random() * 360,
                    duration: Math.random() * 3 + 2,
                    ease: 'power1.out',
                    onComplete: () => confetti.remove()
                });
            }
        }
    </script>
</body>
</html>

