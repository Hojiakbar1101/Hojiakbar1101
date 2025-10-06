<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khojiakbar Saidrasulov - Full Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            padding: 60px 20px;
            position: relative;
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            margin: 0 auto 20px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        h1 {
            font-size: 3em;
            margin-bottom: 10px;
            animation: slideInDown 1s ease;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        @keyframes slideInDown {
            from {
                transform: translateY(-100px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .subtitle {
            font-size: 1.3em;
            opacity: 0.9;
            margin-bottom: 30px;
        }

        .tech-icons {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin: 40px 0;
        }

        .tech-icon {
            width: 100px;
            height: 100px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
            border: 2px solid rgba(255, 255, 255, 0.2);
            cursor: pointer;
        }

        .tech-icon:hover {
            transform: translateY(-10px) scale(1.1);
            background: rgba(255, 255, 255, 0.2);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .tech-icon img {
            width: 50px;
            height: 50px;
            margin-bottom: 8px;
        }

        .tech-icon span {
            font-size: 0.9em;
            font-weight: 600;
        }

        .section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            margin: 30px 0;
            border: 1px solid rgba(255, 255, 255, 0.2);
            animation: fadeIn 1s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h2 {
            font-size: 2em;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        h2::before {
            content: '';
            width: 40px;
            height: 40px;
            display: inline-block;
            background: linear-gradient(45deg, #f093fb 0%, #f5576c 100%);
            border-radius: 10px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .skill-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .skill-card:hover {
            transform: translateX(10px);
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.3);
        }

        .skill-card h3 {
            font-size: 1.3em;
            margin-bottom: 15px;
            color: #ffd700;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            padding: 8px 0;
            padding-left: 25px;
            position: relative;
        }

        .skill-list li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #4facfe;
            font-size: 1.5em;
        }

        .roadmap {
            position: relative;
            padding: 20px 0;
        }

        .roadmap-item {
            background: rgba(255, 255, 255, 0.08);
            padding: 25px;
            border-radius: 15px;
            margin: 20px 0;
            border-left: 5px solid;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .roadmap-item:nth-child(1) { border-color: #4facfe; }
        .roadmap-item:nth-child(2) { border-color: #f093fb; }
        .roadmap-item:nth-child(3) { border-color: #43e97b; }

        .roadmap-item:hover {
            transform: translateX(15px);
            background: rgba(255, 255, 255, 0.12);
        }

        .roadmap-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .roadmap-item h3 {
            font-size: 1.5em;
            margin-bottom: 15px;
        }

        .roadmap-steps {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .step {
            background: rgba(255, 255, 255, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9em;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }

        .step:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: scale(1.05);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.08);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255,255,255,0.1), transparent);
            transform: rotate(45deg);
            transition: all 0.5s ease;
        }

        .project-card:hover::after {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.4);
            border-color: rgba(255, 255, 255, 0.3);
        }

        .project-card h3 {
            font-size: 1.4em;
            margin-bottom: 15px;
            color: #4facfe;
        }

        .tech-stack {
            font-weight: 600;
            color: #ffd700;
            margin: 10px 0;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(79, 172, 254, 0.2) 0%, rgba(0, 242, 254, 0.2) 100%);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .stat-number {
            font-size: 3em;
            font-weight: bold;
            color: #4facfe;
            margin-bottom: 10px;
        }

        .contact-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .contact-btn {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 40px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid rgba(255, 255, 255, 0.3);
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .contact-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
        }

        .interests {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        .interest-tag {
            background: rgba(255, 255, 255, 0.1);
            padding: 12px 25px;
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
        }

        .interest-tag:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: scale(1.1);
        }

        footer {
            text-align: center;
            padding: 40px 20px;
            font-size: 1.2em;
            font-style: italic;
        }

        .wave {
            animation: wave 2s ease-in-out infinite;
            display: inline-block;
            transform-origin: 70% 70%;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        @media (max-width: 768px) {
            h1 { font-size: 2em; }
            .section { padding: 25px; }
            .tech-icons { gap: 15px; }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-image">👨‍💻</div>
            <h1>Khojiakbar Saidrasulov <span class="wave">👋</span></h1>
            <p class="subtitle">Full Stack Developer | Algorithm Enthusiast | Problem Solver</p>
            
            <div class="tech-icons">
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java">
                    <span>Java</span>
                </div>
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript">
                    <span>JavaScript</span>
                </div>
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" alt="TypeScript">
                    <span>TypeScript</span>
                </div>
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" alt="C++">
                    <span>C++</span>
                </div>
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React">
                    <span>React</span>
                </div>
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" alt="Spring">
                    <span>Spring</span>
                </div>
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" alt="Node.js">
                    <span>Node.js</span>
                </div>
                <div class="tech-icon">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" alt="MongoDB">
                    <span>MongoDB</span>
                </div>
            </div>
        </header>

        <div class="section">
            <h2>📊 Professional Stats</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">500+</div>
                    <div>Problems Solved</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1+</div>
                    <div>Years Experience</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">10+</div>
                    <div>Technologies</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">∞</div>
                    <div>Learning Mode</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>💼 Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-card">
                    <h3>🔧 Backend Development</h3>
                    <ul class="skill-list">
                        <li>Spring Boot & Spring Security</li>
                        <li>Node.js & Express.js</li>
                        <li>RESTful APIs & WebSocket</li>
                        <li>Microservices Architecture</li>
                        <li>JWT & OAuth2</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>⚛️ Frontend Development</h3>
                    <ul class="skill-list">
                        <li>React.js & TypeScript</li>
                        <li>HTML5 & CSS3</li>
                        <li>State Management</li>
                        <li>Responsive Design</li>
                        <li>Webpack & Vite</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>🗄️ Database & Tools</h3>
                    <ul class="skill-list">
                        <li>PostgreSQL & MySQL</li>
                        <li>MongoDB & Mongoose</li>
                        <li>Git & Docker</li>
                        <li>IntelliJ IDEA & VS Code</li>
                        <li>Maven & Gradle</li>
                    </ul>
                </div>
                <div class="skill-card">
                    <h3>🧮 Algorithms & DS</h3>
                    <ul class="skill-list">
                        <li>Graph Theory</li>
                        <li>Dynamic Programming</li>
                        <li>Greedy Algorithms</li>
                        <li>Binary Search & Trees</li>
                        <li>STL Mastery</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🚀 Development Roadmap</h2>
            <div class="roadmap">
                <div class="roadmap-item">
                    <h3>☕ Java Full Stack</h3>
                    <div class="roadmap-steps">
                        <span class="step">Core Java</span>
                        <span class="step">OOP Principles</span>
                        <span class="step">Collections</span>
                        <span class="step">Spring Boot</span>
                        <span class="step">Spring Security</span>
                        <span class="step">Microservices</span>
                        <span class="step">JPA/Hibernate</span>
                        <span class="step">REST APIs</span>
                        <span class="step">WebSocket</span>
                        <span class="step">JHipster</span>
                        <span class="step">Deployment</span>
                    </div>
                </div>
                <div class="roadmap-item">
                    <h3>⚡ JavaScript/TypeScript Stack</h3>
                    <div class="roadmap-steps">
                        <span class="step">ES6+ Syntax</span>
                        <span class="step">TypeScript</span>
                        <span class="step">React.js</span>
                        <span class="step">Node.js</span>
                        <span class="step">Express.js</span>
                        <span class="step">MongoDB</span>
                        <span class="step">Authentication</span>
                        <span class="step">State Management</span>
                        <span class="step">API Integration</span>
                        <span class="step">Testing</span>
                        <span class="step">CI/CD</span>
                    </div>
                </div>
                <div class="roadmap-item">
                    <h3>🏆 C++ Competitive Programming</h3>
                    <div class="roadmap-steps">
                        <span class="step">STL Mastery</span>
                        <span class="step">Algorithm Design</span>
                        <span class="step">Data Structures</span>
                        <span class="step">Problem Patterns</span>
                        <span class="step">Optimization</span>
                        <span class="step">Contest Participation</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🎯 Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>📝 Blog Platform</h3>
                    <p class="tech-stack">Java • Spring Boot • React • TypeScript • PostgreSQL</p>
                    <p>Full-featured blogging system with user authentication, CRUD operations, and real-time updates</p>
                </div>
                <div class="project-card">
                    <h3>💬 Real-Time Chat App</h3>
                    <p class="tech-stack">Node.js • WebSocket • React • MongoDB</p>
                    <p>Scalable chat application with private messaging and group chat functionality</p>
                </div>
                <div class="project-card">
                    <h3>✅ Task Management System</h3>
                    <p class="tech-stack">React • TypeScript • Express • MongoDB</p>
                    <p>Comprehensive todo application with user management and JWT authentication</p>
                </div>
                <div class="project-card">
                    <h3>🔐 Authentication Microservice</h3>
                    <p class="tech-stack">Spring Security • JWT • React • TypeScript</p>
                    <p>Secure authentication system with role-based access control</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>🎨 Professional Interests</h2>
            <div class="interests">
                <span class="interest-tag">Backend Architecture</span>
                <span class="interest-tag">Design Patterns</span>
                <span class="interest-tag">Algorithm Optimization</span>
                <span class="interest-tag">Web Performance</span>
                <span class="interest-tag">Clean Code</span>
                <span class="interest-tag">Open Source</span>
                <span class="interest-tag">Cloud Computing</span>
                <span class="interest-tag">DevOps</span>
            </div>
        </div>

        <div class="section">
            <h2>📬 Contact Me</h2>
            <div class="contact-buttons">
                <a href="mailto:saidrasulovhojiakbar7@gmail.com" class="contact-btn">
                    📧 Email
                </a>
                <a href="https://github.com/Hojiakbar1101" class="contact-btn" target="_blank">
                    🐙 GitHub
                </a>
                <a href="#" class="contact-btn">
                    💼 LinkedIn
                </a>
                <a href="#" class="contact-btn">
                    📱 Telegram
                </a>
            </div>
        </div>

        <footer>
            <p>"Building robust solutions through clean code and continuous learning"</p>
            <p style="margin-top: 20px; opacity: 0.8;">📍 Tashkent, Uzbekistan | 🎓 TATU - Cybersecurity</p>
        </footer>
    </div>
</body>
</html>
