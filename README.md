<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Professional GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: #e8e8e8;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        /* Animated background particles */
        .bg-particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.6;
        }
        
        .particle {
            position: absolute;
            background: linear-gradient(45deg, #64ffda, #bb86fc);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
            z-index: 1;
        }
        
        .profile-header {
            text-align: center;
            margin-bottom: 3rem;
            animation: slideDown 1s ease-out;
        }
        
        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .greeting {
            font-size: clamp(2rem, 5vw, 3.5rem);
            font-weight: 700;
            background: linear-gradient(135deg, #64ffda 0%, #bb86fc 50%, #03dac6 100%);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from {
                text-shadow: 0 0 20px rgba(100, 255, 218, 0.3);
            }
            to {
                text-shadow: 0 0 30px rgba(100, 255, 218, 0.6);
            }
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: #a0a0a0;
            font-weight: 300;
            margin-bottom: 2rem;
        }
        
        .section {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2rem;
            border: 1px solid rgba(100, 255, 218, 0.1);
            transition: all 0.3s ease;
            animation: slideUp 1s ease-out;
            animation-fill-mode: both;
        }
        
        .section:nth-child(2) { animation-delay: 0.2s; }
        .section:nth-child(3) { animation-delay: 0.4s; }
        .section:nth-child(4) { animation-delay: 0.6s; }
        .section:nth-child(5) { animation-delay: 0.8s; }
        
        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(100, 255, 218, 0.15);
            border-color: rgba(100, 255, 218, 0.3);
        }
        
        .section-title {
            display: flex;
            align-items: center;
            font-size: 1.4rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
            color: #64ffda;
        }
        
        .section-icon {
            font-size: 1.8rem;
            margin-right: 1rem;
            animation: pulse 2s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        
        .section-content {
            font-size: 1rem;
            line-height: 1.7;
            color: #e0e0e0;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .tech-item {
            background: linear-gradient(135deg, rgba(100, 255, 218, 0.1), rgba(187, 134, 252, 0.1));
            padding: 0.8rem 1rem;
            border-radius: 12px;
            text-align: center;
            font-weight: 500;
            border: 1px solid rgba(100, 255, 218, 0.2);
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .tech-item:hover {
            transform: scale(1.05);
            background: linear-gradient(135deg, rgba(100, 255, 218, 0.2), rgba(187, 134, 252, 0.2));
            box-shadow: 0 5px 15px rgba(100, 255, 218, 0.3);
        }
        
        .highlight {
            color: #64ffda;
            font-weight: 600;
        }
        
        .fun-fact {
            background: linear-gradient(135deg, rgba(187, 134, 252, 0.1), rgba(3, 218, 198, 0.1));
            border-left: 4px solid #bb86fc;
            padding: 1.5rem;
            margin-top: 1rem;
            border-radius: 0 12px 12px 0;
            font-style: italic;
            position: relative;
            overflow: hidden;
        }
        
        .fun-fact::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            animation: shine 3s ease-in-out infinite;
        }
        
        @keyframes shine {
            0% { left: -100%; }
            50% { left: 100%; }
            100% { left: 100%; }
        }
        
        .status-indicator {
            display: inline-flex;
            align-items: center;
            background: rgba(0, 255, 0, 0.1);
            color: #00ff88;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            border: 1px solid rgba(0, 255, 0, 0.3);
            margin-top: 1rem;
            font-size: 0.9rem;
        }
        
        .status-dot {
            width: 8px;
            height: 8px;
            background: #00ff88;
            border-radius: 50%;
            margin-right: 0.5rem;
            animation: blink 1.5s ease-in-out infinite;
        }
        
        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0.3; }
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            padding: 1rem;
            background: rgba(100, 255, 218, 0.05);
            border-radius: 12px;
            border: 1px solid rgba(100, 255, 218, 0.1);
            transition: all 0.3s ease;
        }
        
        .contact-item:hover {
            background: rgba(100, 255, 218, 0.1);
            transform: translateX(5px);
        }
        
        .contact-icon {
            font-size: 1.5rem;
            margin-right: 0.8rem;
            color: #64ffda;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            }
        }
        
        /* Loading animation */
        .loading {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0f0f23;
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 1000;
            animation: fadeOut 1s ease-out 2s forwards;
        }
        
        .loader {
            width: 50px;
            height: 50px;
            border: 3px solid rgba(100, 255, 218, 0.3);
            border-top: 3px solid #64ffda;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        @keyframes fadeOut {
            to {
                opacity: 0;
                visibility: hidden;
            }
        }
    </style>
</head>
<body>
    <div class="loading">
        <div class="loader"></div>
    </div>
    
    <div class="bg-particles" id="particles"></div>
    
    <div class="container">
        <div class="profile-header">
            <h1 class="greeting">Hello, I'm a Full-Stack Developer 👋</h1>
            <p class="subtitle">Crafting scalable solutions and exceptional user experiences</p>
        </div>
        
        <div class="section">
            <h2 class="section-title">
                <span class="section-icon">🚀</span>
                Currently Building
            </h2>
            <div class="section-content">
                I'm passionate about building <span class="highlight">scalable backend systems</span> and optimizing <span class="highlight">database performance</span> to handle enterprise-level workloads. My focus is on creating robust architectures that can grow with business needs.
                <div class="status-indicator">
                    <div class="status-dot"></div>
                    Available for new opportunities
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title">
                <span class="section-icon">🤝</span>
                Open to Collaboration
            </h2>
            <div class="section-content">
                I'm actively seeking collaboration opportunities on <span class="highlight">open-source projects</span> and innovative web applications. I believe in the power of community-driven development and love contributing to projects that make a difference.
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title">
                <span class="section-icon">📚</span>
                Currently Mastering
            </h2>
            <div class="section-content">
                I'm diving deep into <span class="highlight">advanced system design</span> and <span class="highlight">cloud-native architectures</span>. My journey includes exploring microservices, containerization, and distributed systems to build the next generation of web applications.
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title">
                <span class="section-icon">💻</span>
                Technical Expertise
            </h2>
            <div class="section-content">
                Feel free to ask me about any of these technologies:
                <div class="tech-grid">
                    <div class="tech-item">JavaScript</div>
                    <div class="tech-item">Node.js</div>
                    <div class="tech-item">Express.js</div>
                    <div class="tech-item">SQL</div>
                    <div class="tech-item">React</div>
                    <div class="tech-item">Tailwind CSS</div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2 class="section-title">
                <span class="section-icon">⚡</span>
                What Drives Me
            </h2>
            <div class="section-content">
                <div class="fun-fact">
                    I have a passion for transforming complex backend challenges into simple, elegant solutions that seamlessly power exceptional user experiences. There's nothing more satisfying than seeing clean, efficient code running smoothly in production.
                </div>
            </div>
        </div>
    </div>
    
    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 20;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.width = Math.random() * 6 + 2 + 'px';
                particle.style.height = particle.style.width;
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 4 + 4) + 's';
                particlesContainer.appendChild(particle);
            }
        }
        
        // Tech item click animation
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
            
            const techItems = document.querySelectorAll('.tech-item');
            techItems.forEach(item => {
                item.addEventListener('click', function() {
                    this.style.animation = 'none';
                    setTimeout(() => {
                        this.style.animation = 'pulse 0.6s ease-in-out';
                    }, 10);
                });
            });
            
            // Parallax effect for sections
            window.addEventListener('scroll', function() {
                const sections = document.querySelectorAll('.section');
                const scrolled = window.pageYOffset;
                
                sections.forEach((section, index) => {
                    const rate = scrolled * -0.5;
                    section.style.transform = `translateY(${rate * 0.1 * index}px)`;
                });
            });
        });
        
        // Remove loading screen
        window.addEventListener('load', function() {
            setTimeout(() => {
                document.querySelector('.loading').style.display = 'none';
            }, 2000);
        });
    </script>
</body>
</html>
