<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mayur Shetty - Dream it, Code it, and Conquer it.</title>
    <!-- Tailwind CSS CDN --><script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts (Inter) --><link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    <!-- Devicon CDN --><link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@v2.15.1/devicon.min.css">
    
    <style>
        /* --- Base Styling --- */
        body {
            font-family: 'Inter', sans-serif;
            /* Animated gradient background */
            background: linear-gradient(-45deg, #1d1a2f, #2a254d, #5a4f9d, #23a6d5);
            background-size: 400% 400%;
            animation: gradientBG 20s ease infinite;
            color: #ffffff;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        /* Gradient animation keyframes */
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Particle canvas (sits behind content) */
        #particle-canvas {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            opacity: 0.5;
        }

        /* Main content container (sits on top of canvas) */
        .main-content {
            position: relative;
            z-index: 10;
        }

        /* --- Glassmorphism Card Style --- */
        .glass-card {
            background: rgba(255, 255, 255, 0.05); /* Slight white tint */
            backdrop-filter: blur(12px); /* The "glass" effect */
            -webkit-backdrop-filter: blur(12px);
            border-radius: 1.5rem; /* 24px */
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
            transition: all 0.3s ease;
        }

        .glass-card:hover {
            box-shadow: 0 8px 40px 0 rgba(0, 0, 0, 0.4);
            transform: translateY(-5px);
        }

        /* --- Animated Gradient Text for Headers --- */
        .animated-gradient-text {
            background-image: linear-gradient(90deg, #c3a6ff, #61dafb, #c3a6ff);
            background-size: 200% auto;
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            animation: text-glow 4s linear infinite;
        }

        @keyframes text-glow {
            to {
                background-position: 200% center;
            }
        }

        /* --- Scroll Animation Classes (for JS) --- */
        .scroll-animate {
            opacity: 0;
            transform: translateY(40px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }

        .scroll-animate.visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Social Link Hover Effect --- */
        .social-link {
            transition: all 0.3s ease;
            filter: grayscale(30%);
            opacity: 0.8;
        }
        .social-link:hover {
            transform: scale(1.1) translateY(-3px);
            filter: grayscale(0%);
            opacity: 1;
            box-shadow: 0 0 20px rgba(97, 218, 251, 0.5); /* React blue glow */
        }

        /* --- Tech Icon Style --- */
        .tech-icon {
            font-size: 4rem; /* 64px */
            color: rgba(255, 255, 255, 0.7);
            transition: all 0.3s ease;
        }
        .tech-icon:hover {
            color: rgba(255, 255, 255, 1);
            transform: scale(1.15);
            filter: drop-shadow(0 0 10px rgba(255, 255, 255, 0.5));
        }

        /* --- Cute Bot Animations --- */
        @keyframes floatBot {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-10px); /* Smaller float for seated bot */
            }
            100% {
                transform: translateY(0px);
            }
        }

        @keyframes blinkCursor {
            0%, 49% { opacity: 1; }
            50%, 100% { opacity: 0; }
        }

        .floating-bot {
            animation: floatBot 4s ease-in-out infinite;
            filter: drop-shadow(0 5px 15px rgba(0, 0, 0, 0.3)); /* For a subtle lift effect */
        }

        .cursor {
            animation: blinkCursor 1s step-end infinite;
        }
    </style>
</head>
<body class="antialiased">

    <!-- Particle background canvas --><canvas id="particle-canvas"></canvas>

    <!-- Main content container --><div class="main-content min-h-screen w-full max-w-7xl mx-auto px-4 py-12 md:py-20">
        
        <!-- ================================== --><!-- HEADER SECTION --><!-- ================================== --><header class="glass-card scroll-animate flex flex-col md:flex-row items-center justify-between p-8 md:p-12 text-center md:text-left">
            <!-- Left Side: Your Photo --><img 
                src="https://placehold.co/150x150/5a4f9d/ffffff?text=Mayur&font=inter" 
                alt="Mayur Shetty" 
                class="w-36 h-36 rounded-full object-cover border-4 border-white/30 shadow-lg mb-6 md:mb-0"
                onerror="this.src='https://placehold.co/150x150/5a4f9d/ffffff?text=Photo&font=inter'"
            />
            
            <!-- Center: Title and Tagline --><div class="flex-1 md:mx-10">
                <h1 class="text-4xl md:text-6xl font-black tracking-tighter animated-gradient-text">
                    MAYUR SHETTY
                </h1>
                <h3 class="text-xl md:text-2xl font-light text-gray-200 mt-2 tracking-wide">
                    Dream it, code it, and conquer it.
                </h3>
            </div>

            <!-- Right Side: Cute 3D-ish Laptop Bot (Animated SVG) --><div class="w-64 h-64 mt-6 md:mt-0 floating-bot">
                <svg viewBox="0 0 300 300" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <!-- Gradients for 3D effect --><linearGradient id="screenGradient" x1="0" y1="0" x2="1" y2="1">
                            <stop offset="0%" stop-color="#2a254d" />
                            <stop offset="100%" stop-color="#1d1a2f" />
                        </linearGradient>
                        <linearGradient id="bodyGradient" x1="0" y1="0" x2="1" y2="1">
                            <stop offset="0%" stop-color="#764ABC" />
                            <stop offset="100%" stop-color="#5a4f9d" />
                        </linearGradient>
                        <radialGradient id="eyeShine" cx="0.6" cy="0.4" r="0.7">
                            <stop offset="0%" stop-color="white"/>
                            <stop offset="100%" stop-color="#C3A6FF"/>
                        </radialGradient>
                    </defs>

                    <!-- Bot's Chair/Base --><rect x="60" y="210" width="180" height="30" rx="10" fill="#4d4177"></rect>
                    <rect x="100" y="240" width="20" height="20" rx="5" fill="#4d4177"></rect>
                    <rect x="180" y="240" width="20" height="20" rx="5" fill="#4d4177"></rect>

                    <!-- Laptop Base (Body - Bottom Layer for Depth) --><path d="M50,160 L250,160 L240,210 L60,210 Z" fill="url(#bodyGradient)"></path>
                    <path d="M60,210 Q150,220 240,210 L250,160 L240,210 Z" fill="rgba(0,0,0,0.1)" transform="translate(0, -5)"></path> <!-- Base Shadow --><!-- Laptop Screen (Head - Front Layer for Depth) --><rect x="70" y="70" width="160" height="100" rx="12" fill="url(#screenGradient)" stroke="#61DAFB" stroke-width="4"></rect>
                    
                    <!-- Screen Content (console log and cursor) --><text x="85" y="110" font-family="monospace" font-size="16" fill="#C3A6FF">console.log("Hello, </text>
                    <text x="85" y="135" font-family="monospace" font-size="16" fill="#C3A6FF">Mayur!");</text>
                    <rect x="175" y="98" width="8" height="18" fill="#C3A6FF" class="cursor"></rect> <!-- Blinking cursor --><!-- Bot's Face (Cute eyes) --><!-- Eyes --><circle cx="110" cy="115" r="8" fill="white" stroke="#61DAFB" stroke-width="1"></circle>
                    <circle cx="110" cy="115" r="4" fill="#1D1A2F"></circle>
                    <circle cx="112" cy="113" r="1.5" fill="url(#eyeShine)"></circle> <!-- Eye highlight --><circle cx="190" cy="115" r="8" fill="white" stroke="#61DAFB" stroke-width="1"></circle>
                    <circle cx="190" cy="115" r="4" fill="#1D1A2F"></circle>
                    <circle cx="192" cy="113" r="1.5" fill="url(#eyeShine)"></circle> <!-- Eye highlight --><!-- Mouth --><path d="M120 140 Q150 150 180 140" stroke="#C3A6FF" stroke-width="3" fill="none" stroke-linecap="round"></path>
                    
                    <!-- Arms (typing position) --><rect x="55" y="150" width="25" height="10" rx="5" fill="#C3A6FF" transform="rotate(-10 67.5 155)"></rect> <!-- Left Arm upper --><rect x="60" y="160" width="20" height="10" rx="5" fill="#C3A6FF" transform="rotate(20 70 165)"></rect> <!-- Left Arm lower --><rect x="220" y="150" width="25" height="10" rx="5" fill="#C3A6FF" transform="rotate(10 232.5 155)"></rect> <!-- Right Arm upper --><rect x="220" y="160" width="20" height="10" rx="5" fill="#C3A6FF" transform="rotate(-20 230 165)"></rect> <!-- Right Arm lower --><!-- Hands (on keyboard) --><circle cx="80" cy="165" r="8" fill="#A78BFA"></circle>
                    <circle cx="220" cy="165" r="8" fill="#A78BFA"></circle>

                    <!-- Keyboard detail --><rect x="75" y="170" width="150" height="15" rx="3" fill="#4d4177"></rect>
                    <rect x="80" y="173" width="140" height="9" rx="2" fill="#2a254d"></rect> <!-- Keys area --><!-- Small shadow to emphasize floating --><ellipse cx="150" cy="280" rx="90" ry="20" fill="rgba(0,0,0,0.2)" transform="scale(0.8)"></ellipse>
                </svg>
            </div>
        </header>

        <!-- ================================== --><!-- CONNECT WITH ME SECTION --><!-- ================================== --><section class="glass-card scroll-animate mt-12 p-8">
            <h2 class="text-3xl font-bold text-center mb-8 animated-gradient-text">
                Connect With Me :-)
            </h2>
            <div class="flex flex-wrap justify-center gap-4">
                <!-- Replace '#' with your actual profile links --><a href="#" target="_blank" class="social-link">
                    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
                </a>
                <a href="#" target="_blank" class="social-link">
                    <img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram"/>
                </a>
                <a href="mailto:your-email@gmail.com" target="_blank" class="social-link">
                    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/>
                </a>
                <a href="#" target="_blank" class="social-link">
                    <img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white" alt="X"/>
                </a>
                <a href="#" target="_blank" class="social-link">
                    <img src="https://img.shields.io/badge/Agent.ai-764abc?style=for-the-badge&logo=openai&logoColor=white" alt="Agent.ai"/>
                </a>
            </div>
        </section>

        <!-- ================================== --><!-- TECH & CODING PROFILES (Combined) --><!-- ================================== --><div class="grid grid-cols-1 lg:grid-cols-3 gap-12 mt-12">
            
            <!-- Tech Universe (Takes 2/3 width on large screens) --><section class="glass-card scroll-animate lg:col-span-2 p-8">
                <h2 class="text-3xl font-bold text-center mb-8 animated-gradient-text">
                    My Tech Universe
                </h2>
                <div class="flex flex-wrap justify-center gap-8 items-center"> <!-- Increased gap for icons --><!-- Devicons: https://devicon.dev/ --><i class="devicon-html5-plain tech-icon" title="HTML5"></i>
                    <i class="devicon-css3-plain tech-icon" title="CSS3"></i>
                    <i class="devicon-javascript-plain tech-icon" title="JavaScript"></i>
                    <i class="devicon-express-original tech-icon" title="Express.js"></i>
                    <i class="devicon-nodejs-plain tech-icon" title="Node.js"></i>
                    <i class="devicon-tailwindcss-plain tech-icon" title="Tailwind CSS"></i>
                    <i class="devicon-bootstrap-plain tech-icon" title="Bootstrap"></i>
                    <i class="devicon-react-original tech-icon" title="React"></i>
                    <i class="devicon-mysql-plain tech-icon" title="MySQL"></i>
                    <i class="devicon-postgresql-plain tech-icon" title="SQL"></i>
                    <i class="devicon-docker-plain tech-icon" title="Docker"></i>
                    <i class="devicon-git-plain tech-icon" title="Git"></i>
                    <i class="devicon-github-original tech-icon" title="GitHub"></i>
                    <i class="devicon-java-plain tech-icon" title="Java"></i>
                    <i class="devicon-python-plain tech-icon" title="Python"></i>
                    <i class="devicon-vercel-original tech-icon" title="Vercel"></i>
                    <i class="devicon-firebase-plain tech-icon" title="Firebase"></i>
                    <i class="devicon-supabase-plain tech-icon" title="Supabase"></i>
                    <i class="devicon-nextjs-original tech-icon" title="Next.js"></i>
                </div>
            </section>
            
            <!-- Coding Profiles (Takes 1/3 width on large screens) --><section class="glass-card scroll-animate p-8">
                <h2 class="text-3xl font-bold text-center mb-8 animated-gradient-text">
                    Coding Profiles
                </h2>
                <div class="flex flex-col items-center gap-4">
                    <!-- Replace 'YOUR_USERNAME' with your actual usernames --><a href="https://leetcode.com/YOUR_USERNAME/" target="_blank" class="social-link">
                        <img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode"/>
                    </a>
                    <a href="https://www.codechef.com/users/YOUR_USERNAME" target="_blank" class="social-link">
                        <img src="https://img.shields.io/badge/CodeChef-5B4638?style=for-the-badge&logo=codechef&logoColor=white" alt="CodeChef"/>
                    </a>
                </div>
            </section>
        </div>

        <!-- ================================== --><!-- GITHUB PULSE & TROPHIES --><!-- ================================== --><section class="glass-card scroll-animate mt-12 p-8">
            <h2 class="text-3xl font-bold text-center mb-8 animated-gradient-text">
                My GitHub Pulse
            </h2>
            
            <!-- Stats & Languages --><div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
                <!-- 
                Replace 'YOUR_GITHUB_USERNAME' with your GitHub username.
                I'm using the 'transparent' theme with a custom color to match our vibe.
                --><img 
                    src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=transparent&text_color=ffffff&icon_color=61dafb&title_color=c3a6ff&include_all_commits=true&count_private=true&hide_border=true&border_radius=10" 
                    alt="GitHub Stats"
                    class="w-full h-auto"
                />
                <img 
                    src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=transparent&text_color=ffffff&title_color=c3a6ff&hide_border=true&border_radius=10&langs_count=8" 
                    alt="Top Languages"
                    class="w-full h-auto"
                />
            </div>
            
            <!-- Trophies --><div class="mt-6">
                <img 
                    src="https://github-profile-trophy.vercel.app/?username=YOUR_GITHUB_USERNAME&theme=transparent&no-frame=true&no-bg=true&margin-w=15&margin-h=15&column=-1&text_color=ffffff&title_color=61dafb"
                    alt="GitHub Trophies"
                    class="w-full"
                />
            </div>

            <!-- Badges: Streak & Views --><div class="flex flex-wrap justify-center items-center gap-6 mt-6">
                <img 
                    src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_GITHUB_USERNAME&theme=transparent&hide_border=true&border_radius=5&date_format=M%20j%5B%2C%20Y%5D&background=00000000&stroke=ffffff&ring=61dafb&fire=61dafb&currStreakNum=ffffff&currStreakLabel=ffffff&sideNums=ffffff&sideLabels=ffffff" 
                    alt="GitHub Streak"
                />
                <img 
                    src="https://komarev.com/ghpvc/?username=YOUR_GITHUB_USERNAME&style=for-the-badge&color=00000000&labelColor=00000000" 
                    alt="Profile Views"
                />
            </div>
        </section>

        <!-- ================================== --><!-- ACHIEVEMENTS & CERTIFICATIONS --><!-- ================================== --><section class="scroll-animate mt-12">
            <h2 class="text-3xl font-bold text-center mb-8 animated-gradient-text">
                My Achievements & Certifications
            </h2>
            <!-- We use a grid for the card layout --><div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                
                <!-- Card 1 --><div class="glass-card p-6">
                    <img 
                        src="https://placehold.co/600x400/2c2c2c/61dafb?text=Certificate+Image&font=inter" 
                        alt="Certificate 1" 
                        class="w-full rounded-lg shadow-lg"
                        onerror="this.src='https://placehold.co/600x400/2c2c2c/61dafb?text=Certificate+Image&font=inter'"
                    />
                    <h3 class="text-xl font-bold mt-4">Awesome Certification Name</h3>
                    <p class="text-gray-300 mt-2">
                        A brief description of what this certificate is about and what I learned. This shows my dedication to mastering new skills.
                    </p>
                </div>
                
                <!-- Card 2 --><div class="glass-card p-6">
                    <img 
                        src="https://placehold.co/600x400/2c2c2c/764abc?text=Hackathon+Winner&font=inter" 
                        alt="Certificate 2" 
                        class="w-full rounded-lg shadow-lg"
                        onerror="this.src='https://placehold.co/600x400/2c2c2c/764abc?text=Hackathon+Winner&font=inter'"
                    />
                    <h3 class="text-xl font-bold mt-4">Another Cool Achievement</h3>
                    <p class="text-gray-300 mt-2">
                        This one was for a hackathon where we built an amazing project from scratch in 24 hours.
                    </p>
                </div>

                <!-- Add more cards here... --></div>
        </section>

        <!-- ================================== --><!-- PROJECTS SECTION --><!-- ================================== --><section class="glass-card scroll-animate mt-12 p-8">
            <h2 class="text-3xl font-bold text-center mb-8 animated-gradient-text">
                My Projects
            </h2>
            <div class="space-y-8">
                
                <!-- Project 1 --><div class="border-b border-white/10 pb-6">
                    <h3 class="text-2xl font-bold">
                        🚀 <a href="#" target="_blank" class="hover:underline text-blue-300">Awesome Project Title</a>
                    </h3>
                    <p class="text-gray-300 mt-2">
                        A short but impactful description of your project. Talk about the 'what', 'why', and the tech stack used (e.g., React, Node.js, and MongoDB).
                    </p>
                </div>
                
                <!-- Project 2 --><div class="border-b border-white/10 pb-6">
                    <h3 class="text-2xl font-bold">
                        🤖 <a href="#" target="_blank" class="hover:underline text-blue-300">AI-Powered App</a>
                    </h3>
                    <p class="text-gray-300 mt-2">
                        This project uses FastAPI and Python to deliver real-time AI insights. A very challenging but rewarding build.
                    </p>
                </div>

                <!-- Project 3 --><div>
                    <h3 class="text-2xl font-bold">
                        🌐 <a href="#" target="_blank" class="hover:underline text-blue-300">This Magical Portfolio</a>
                    </h3>
                    <p class="text-gray-300 mt-2">
                        The very page you're on! Built with pure HTML, Tailwind CSS, and vanilla JavaScript for a lightweight, animated experience.
                    </p>
                </div>

            </div>
        </section>

    </div>

    <!-- JavaScript for Animations --><script>
        document.addEventListener('DOMContentLoaded', () => {

            // --- Particle Background Animation ---
            const canvas = document.getElementById('particle-canvas');
            if (canvas) {
                const ctx = canvas.getContext('2d');
                let particles = [];
                
                // Set canvas size
                function resizeCanvas() {
                    canvas.width = window.innerWidth;
                    canvas.height = window.innerHeight;
                }
                resizeCanvas();
                window.addEventListener('resize', resizeCanvas);

                // Particle object
                function Particle(x, y, dx, dy, radius, color) {
                    this.x = x;
                    this.y = y;
                    this.dx = dx;
                    this.dy = dy;
                    this.radius = radius;
                    this.color = color;

                    this.draw = function() {
                        ctx.beginPath();
                        ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2, false);
                        ctx.fillStyle = this.color;
                        ctx.fill();
                        ctx.closePath();
                    }

                    this.update = function() {
                        if (this.x + this.radius > canvas.width || this.x - this.radius < 0) {
                            this.dx = -this.dx;
                        }
                        if (this.y + this.radius > canvas.height || this.y - this.radius < 0) {
                            this.dy = -this.dy;
                        }
                        this.x += this.dx;
                        this.y += this.dy;
                        this.draw();
                    }
                }

                // Create particles
                function initParticles() {
                    particles = [];
                    let numberOfParticles = (canvas.width * canvas.height) / 9000;
                    for (let i = 0; i < numberOfParticles; i++) {
                        let radius = Math.random() * 2 + 1;
                        let x = Math.random() * (canvas.width - radius * 2) + radius;
                        let y = Math.random() * (canvas.height - radius * 2) + radius;
                        let dx = (Math.random() - 0.5) * 0.5;
                        let dy = (Math.random() - 0.5) * 0.5;
                        let color = 'rgba(255, 255, 255, 0.7)';
                        particles.push(new Particle(x, y, dx, dy, radius, color));
                    }
                }

                // Animation loop
                function animateParticles() {
                    requestAnimationFrame(animateParticles);
                    ctx.clearRect(0, 0, canvas.width, canvas.height);
                    for (let i = 0; i < particles.length; i++) {
                        particles[i].update();
                    }
                }

                initParticles();
                animateParticles();
                window.addEventListener('resize', initParticles);
            }

            // --- Fade-in on Scroll Animation ---
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                        // Optional: stop observing once it's visible
                        // observer.unobserve(entry.target);
                    }
                    // Optional: remove 'visible' class if you want it to fade out when scrolling up
                    // else {
                    //     entry.target.classList.remove('visible');
                    // }
                });
            }, {
                threshold: 0.1 // Trigger when 10% of the element is visible
            });

            // Target all elements with the .scroll-animate class
            const elements = document.querySelectorAll('.scroll-animate');
            elements.forEach(el => observer.observe(el));
        });
    </script>

</body>
</html>

