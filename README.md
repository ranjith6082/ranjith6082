<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ranjith Krishna - Software Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            padding: 40px;
            animation: fadeIn 1s ease-in;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        .header h1 {
            font-size: 3em;
            color: #667eea;
            margin-bottom: 10px;
            animation: slideDown 1s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header h2 {
            font-size: 1.5em;
            color: #764ba2;
            font-weight: 400;
            animation: slideUp 1s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .wave {
            display: inline-block;
            animation: wave 2s ease-in-out infinite;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        .profile-views {
            display: inline-block;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 8px 20px;
            border-radius: 25px;
            margin-top: 20px;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .content-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin: 40px 0;
        }

        .section {
            background: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
        }

        .section h3 {
            color: #667eea;
            margin-bottom: 20px;
            font-size: 1.8em;
            border-bottom: 3px solid #764ba2;
            padding-bottom: 10px;
        }

        .about-item {
            display: flex;
            align-items: center;
            margin: 15px 0;
            padding: 15px;
            background: #f8f9ff;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .about-item:hover {
            background: linear-gradient(135deg, #667eea15, #764ba215);
            transform: translateX(10px);
        }

        .about-item::before {
            content: "▶";
            color: #667eea;
            font-weight: bold;
            margin-right: 15px;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
        }

        .social-btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 15px 30px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .social-btn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(102, 126, 234, 0.6);
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .tech-item {
            text-align: center;
            padding: 20px;
            background: linear-gradient(135deg, #f8f9ff, #fff);
            border-radius: 15px;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .tech-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(102, 126, 234, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .tech-item:hover::before {
            left: 100%;
        }

        .tech-item:hover {
            transform: translateY(-10px) rotate(5deg);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.4);
        }

        .tech-icon {
            font-size: 2.5em;
            margin-bottom: 10px;
            display: block;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .tech-name {
            font-weight: bold;
            color: #667eea;
            font-size: 0.9em;
        }

        .full-width {
            grid-column: 1 / -1;
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .stat-card {
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .stat-card img {
            max-width: 100%;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .stat-card:hover img {
            transform: scale(1.05);
        }

        .coding-animation {
            text-align: center;
            margin: 30px 0;
        }

        .coding-animation img {
            max-width: 400px;
            width: 100%;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .email-link {
            color: #667eea;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        .email-link:hover {
            color: #764ba2;
            text-decoration: underline;
        }

        @media (max-width: 768px) {
            .content-grid {
                grid-template-columns: 1fr;
            }
            
            .header h1 {
                font-size: 2em;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
            }
            
            .container {
                padding: 20px;
            }
        }

        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            background: white;
            border-radius: 50%;
            opacity: 0.3;
            animation: particle-float 10s infinite ease-in-out;
        }

        @keyframes particle-float {
            0%, 100% { transform: translate(0, 0); }
            25% { transform: translate(100px, -100px); }
            50% { transform: translate(-50px, -200px); }
            75% { transform: translate(-150px, -100px); }
        }
    </style>
</head>
<body>
    <div class="particles" id="particles"></div>
    
    <div class="container">
        <div class="header">
            <h1>Hi <span class="wave">👋</span>, I'm Ranjith Krishna</h1>
            <h2>A passionate Software Engineer from India</h2>
            <div class="profile-views">👁️ Profile Views: Growing Daily!</div>
        </div>

        <div class="coding-animation">
            <img src="https://camo.githubusercontent.com/4d9f5ecceb711eec6e2018f38a5677dc657c9738d4a65ba3b928c41c0a45b439/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f313336302f302a37513379765349765f7430696f4a2d5a2e676966" alt="Coding Animation">
        </div>

        <div class="content-grid">
            <div class="section">
                <h3>🚀 About Me</h3>
                <div class="about-item">🌱 Currently learning DevOps and Cloud</div>
                <div class="about-item">💻 All projects on <a href="https://github.com/ranjith6082?tab=repositories" class="email-link">GitHub</a></div>
                <div class="about-item">📝 Writing about DevOps and Cloud</div>
                <div class="about-item">📫 Reach me: <a href="mailto:akurathiranjith11@gmail.com" class="email-link">akurathiranjith11@gmail.com</a></div>
                <div class="about-item">📄 <a href="https://drive.google.com/file/d/1J1B3z3korOFt6P_KA9ZOYKcSfja5e4Ro/view?usp=sharing" class="email-link">View My Resume</a></div>
            </div>

            <div class="section">
                <h3>🔗 Connect With Me</h3>
                <div class="social-links">
                    <a href="https://linkedin.com/in/ranjithkrishna11" class="social-btn" target="_blank">
                        💼 LinkedIn
                    </a>
                    <a href="https://instagram.com/ranjithkrishna_11" class="social-btn" target="_blank">
                        📸 Instagram
                    </a>
                </div>
            </div>
        </div>

        <div class="section full-width">
            <h3>🛠️ Languages and Tools</h3>
            <div class="tech-grid">
                <div class="tech-item">
                    <span class="tech-icon">☁️</span>
                    <div class="tech-name">AWS</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🔷</span>
                    <div class="tech-name">Azure</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">💻</span>
                    <div class="tech-name">Bash</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🐳</span>
                    <div class="tech-name">Docker</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">☁️</span>
                    <div class="tech-name">GCP</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">📦</span>
                    <div class="tech-name">Git</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">☕</span>
                    <div class="tech-name">Java</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🔧</span>
                    <div class="tech-name">Jenkins</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">☸️</span>
                    <div class="tech-name">Kubernetes</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🐧</span>
                    <div class="tech-name">Linux</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🗄️</span>
                    <div class="tech-name">MySQL</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🐘</span>
                    <div class="tech-name">PostgreSQL</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🐍</span>
                    <div class="tech-name">Python</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🍃</span>
                    <div class="tech-name">Spring</div>
                </div>
            </div>
        </div>

        <div class="section full-width">
            <h3>📊 GitHub Statistics</h3>
            <div class="stats-container">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs?username=ranjith6082&show_icons=true&locale=en&layout=compact&theme=radical" alt="Top Languages">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=ranjith6082&show_icons=true&locale=en&theme=radical" alt="GitHub Stats">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=ranjith6082&theme=radical" alt="GitHub Streak">
                </div>
            </div>
        </div>
    </div>

    <script>
        // Create floating particles
        const particlesContainer = document.getElementById('particles');
        for (let i = 0; i < 20; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.width = Math.random() * 10 + 5 + 'px';
            particle.style.height = particle.style.width;
            particle.style.left = Math.random() * 100 + '%';
            particle.style.top = Math.random() * 100 + '%';
            particle.style.animationDelay = Math.random() * 10 + 's';
            particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
            particlesContainer.appendChild(particle);
        }

        // Add stagger animation to tech items
        const techItems = document.querySelectorAll('.tech-item');
        techItems.forEach((item, index) => {
            item.style.animation = `fadeIn 0.5s ease-in ${index * 0.05}s both`;
        });
    </script>
</body>
</html>
