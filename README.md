<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Punit Alagoudar - Software Architect</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #1a1a1a;
            line-height: 1.6;
            min-height: 100vh;
        }

        .wrapper {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            position: sticky;
            top: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2563eb;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 0.95rem;
        }

        nav a:hover {
            color: #2563eb;
        }

        /* Hero Section */
        .hero {
            padding: 120px 0 80px;
            text-align: center;
        }

        .hero-content {
            max-width: 900px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 800;
            color: #1e3a8a;
            margin-bottom: 20px;
            letter-spacing: -1px;
        }

        .hero .subtitle {
            font-size: 1.4rem;
            color: #64748b;
            margin-bottom: 15px;
            font-weight: 300;
        }

        .hero .description {
            font-size: 1.05rem;
            color: #64748b;
            max-width: 700px;
            margin: 0 auto 30px;
            line-height: 1.8;
        }

        .hero-badges {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 40px;
        }

        .badge {
            background: white;
            padding: 12px 24px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .badge.primary {
            background: #2563eb;
            color: white;
        }

        .cta-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 12px 32px;
            border-radius: 8px;
            border: none;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: #2563eb;
            color: white;
        }

        .btn-primary:hover {
            background: #1e40af;
            transform: translateY(-2px);
            box-shadow: 0 8px 16px rgba(37, 99, 235, 0.3);
        }

        .btn-secondary {
            background: white;
            color: #2563eb;
            border: 2px solid #2563eb;
        }

        .btn-secondary:hover {
            background: #f0f4ff;
            transform: translateY(-2px);
        }

        /* Sections */
        section {
            padding: 100px 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
        }

        section:last-child {
            border-bottom: none;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header h2 {
            font-size: 2.5rem;
            color: #1e3a8a;
            margin-bottom: 20px;
        }

        .section-header p {
            font-size: 1.1rem;
            color: #64748b;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Cards Grid */
        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .card {
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            border-left: 4px solid #2563eb;
            position: relative;
            overflow: hidden;
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 100px;
            height: 100px;
            background: rgba(37, 99, 235, 0.05);
            border-radius: 50%;
            transform: translate(30%, -30%);
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 24px rgba(0, 0, 0, 0.12);
        }

        .card-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .card h3 {
            font-size: 1.3rem;
            color: #1e3a8a;
            margin-bottom: 15px;
        }

        .card p {
            color: #64748b;
            font-size: 0.95rem;
            line-height: 1.7;
        }

        .card-list {
            list-style: none;
            margin-top: 20px;
        }

        .card-list li {
            padding: 8px 0;
            color: #64748b;
            font-size: 0.95rem;
            padding-left: 24px;
            position: relative;
        }

        .card-list li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: #2563eb;
            font-weight: bold;
        }

        /* Project Cards */
        .project-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
        }

        .project-header {
            padding: 30px;
            background: linear-gradient(135deg, #2563eb 0%, #1e40af 100%);
            color: white;
        }

        .project-icon {
            font-size: 2.5rem;
            margin-bottom: 12px;
        }

        .project-title {
            font-size: 1.5rem;
            margin-bottom: 8px;
        }

        .project-subtitle {
            font-size: 0.9rem;
            opacity: 0.9;
        }

        .project-body {
            padding: 30px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .project-description {
            color: #64748b;
            margin-bottom: 20px;
            line-height: 1.7;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        .tech-tag {
            background: #f0f4ff;
            color: #2563eb;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
        }

        .metrics-list {
            background: #f8fafc;
            padding: 20px;
            border-radius: 8px;
            margin-top: auto;
        }

        .metric {
            margin-bottom: 12px;
            font-size: 0.95rem;
            color: #64748b;
        }

        .metric:last-child {
            margin-bottom: 0;
        }

        .metric-value {
            color: #2563eb;
            font-weight: 600;
        }

        /* Stats */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .stat {
            text-align: center;
            padding: 30px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: #2563eb;
            margin-bottom: 10px;
        }

        .stat-label {
            color: #64748b;
            font-size: 0.95rem;
        }

        /* Timeline */
        .timeline {
            position: relative;
            padding: 20px 0;
        }

        .timeline-item {
            padding: 30px;
            background: white;
            border-radius: 8px;
            margin-bottom: 20px;
            border-left: 4px solid #2563eb;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
        }

        .timeline-item h4 {
            color: #1e3a8a;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .timeline-item p {
            color: #64748b;
            line-height: 1.7;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, #1e3a8a 0%, #1e40af 100%);
            color: white;
            padding: 60px 0;
            text-align: center;
        }

        .footer-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .footer-content h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }

        .footer-content p {
            font-size: 1.05rem;
            margin-bottom: 30px;
            opacity: 0.95;
            line-height: 1.8;
        }

        .footer-links {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }

        .footer-link {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            padding: 10px 20px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .footer-link:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: translateY(-2px);
        }

        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.2);
            padding-top: 30px;
            font-size: 0.9rem;
            opacity: 0.85;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .section-header h2 {
                font-size: 1.8rem;
            }

            nav ul {
                gap: 15px;
            }

            nav a {
                font-size: 0.85rem;
            }
        }
    </style>
</head>
<body>
    <div class="wrapper">
        <!-- Navigation -->
        <nav>
            <div class="logo">PA</div>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#expertise">Expertise</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>

        <!-- Hero Section -->
        <section class="hero" id="about">
            <div class="hero-content">
                <h1>Punit Alagoudar</h1>
                <p class="subtitle">Software Architect & Systems Engineer</p>
                <p class="description">
                    Designing and deploying production-grade systems that serve millions of users. Specialized in building scalable backends, optimizing databases, and orchestrating infrastructure. Passionate about solving complex technical problems and mentoring engineering teams.
                </p>
                <div class="hero-badges">
                    <span class="badge primary">🇮🇳 India</span>
                    <span class="badge">🟢 Open to Opportunities</span>
                    <span class="badge">📍 Remote Available</span>
                </div>
                <div class="cta-buttons">
                    <a href="https://github.com/punitalagoudar" class="btn btn-primary">View GitHub</a>
                    <a href="https://linkedin.com/in/punit-alagoudar-4932442a3/" class="btn btn-secondary">LinkedIn Profile</a>
                </div>
            </div>
        </section>

        <!-- Core Expertise -->
        <section id="expertise">
            <div class="section-header">
                <h2>Core Expertise</h2>
                <p>Comprehensive technical capabilities across full-stack architecture</p>
            </div>
            <div class="cards-grid">
                <div class="card">
                    <div class="card-icon">🏗️</div>
                    <h3>Backend Architecture</h3>
                    <ul class="card-list">
                        <li>RESTful API & GraphQL Design</li>
                        <li>Microservices Patterns</li>
                        <li>Event-Driven Systems</li>
                        <li>Message Queue Systems</li>
                        <li>Database Optimization</li>
                    </ul>
                </div>
                <div class="card">
                    <div class="card-icon">💻</div>
                    <h3>Frontend Engineering</h3>
                    <ul class="card-list">
                        <li>React Advanced Patterns</li>
                        <li>State Management</li>
                        <li>Performance Optimization</li>
                        <li>Responsive Design</li>
                        <li>Accessibility Standards</li>
                    </ul>
                </div>
                <div class="card">
                    <div class="card-icon">☸️</div>
                    <h3>Infrastructure & DevOps</h3>
                    <ul class="card-list">
                        <li>Kubernetes Orchestration</li>
                        <li>Docker Containerization</li>
                        <li>CI/CD Pipeline Design</li>
                        <li>Infrastructure as Code</li>
                        <li>Cloud Services (AWS)</li>
                    </ul>
                </div>
                <div class="card">
                    <div class="card-icon">📊</div>
                    <h3>System Design</h3>
                    <ul class="card-list">
                        <li>Scalable Architecture</li>
                        <li>Load Balancing</li>
                        <li>High-Availability Systems</li>
                        <li>Disaster Recovery</li>
                        <li>Capacity Planning</li>
                    </ul>
                </div>
                <div class="card">
                    <div class="card-icon">🔐</div>
                    <h3>Security & Compliance</h3>
                    <ul class="card-list">
                        <li>API Authentication</li>
                        <li>Data Encryption</li>
                        <li>OWASP Compliance</li>
                        <li>Audit Logging</li>
                        <li>Credential Management</li>
                    </ul>
                </div>
                <div class="card">
                    <div class="card-icon">📈</div>
                    <h3>Data Engineering</h3>
                    <ul class="card-list">
                        <li>Query Optimization</li>
                        <li>Index Strategy</li>
                        <li>Data Pipelines</li>
                        <li>ETL Workflows</li>
                        <li>Stream Processing</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Projects -->
        <section id="projects">
            <div class="section-header">
                <h2>Featured Projects</h2>
                <p>Production systems demonstrating architectural excellence and impact</p>
            </div>
            <div class="cards-grid">
                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🤖</div>
                        <h3 class="project-title">AI Document Platform</h3>
                        <p class="project-subtitle">Intelligent Automation System</p>
                    </div>
                    <div class="project-body">
                        <p class="project-description">
                            Automated document generation using advanced AI with intelligent content structuring and multi-format export capabilities.
                        </p>
                        <div class="tech-stack">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">Flask</span>
                            <span class="tech-tag">OpenAI</span>
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">PostgreSQL</span>
                        </div>
                        <div class="metrics-list">
                            <div class="metric">⚡ <span class="metric-value">85% faster</span> generation</div>
                            <div class="metric">📊 <span class="metric-value">1000+</span> monthly volume</div>
                            <div class="metric">✅ <span class="metric-value">99.2%</span> accuracy</div>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">🔐</div>
                        <h3 class="project-title">Auth Framework</h3>
                        <p class="project-subtitle">Enterprise Security System</p>
                    </div>
                    <div class="project-body">
                        <p class="project-description">
                            Production-ready authentication system with JWT token rotation, fine-grained permissions, and comprehensive audit trails.
                        </p>
                        <div class="tech-stack">
                            <span class="tech-tag">Node.js</span>
                            <span class="tech-tag">Express</span>
                            <span class="tech-tag">PostgreSQL</span>
                            <span class="tech-tag">JWT</span>
                            <span class="tech-tag">React</span>
                        </div>
                        <div class="metrics-list">
                            <div class="metric">🔑 JWT with <span class="metric-value">rotation</span></div>
                            <div class="metric">👥 <span class="metric-value">RBAC</span> system</div>
                            <div class="metric">🛡️ <span class="metric-value">OWASP</span> compliant</div>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <div class="project-icon">⚡</div>
                        <h3 class="project-title">Web Platform</h3>
                        <p class="project-subtitle">Performance-First Application</p>
                    </div>
                    <div class="project-body">
                        <p class="project-description">
                            Optimized responsive web platform with advanced animations, SEO optimization, and exceptional performance metrics.
                        </p>
                        <div class="tech-stack">
                            <span class="tech-tag">HTML5</span>
                            <span class="tech-tag">CSS3</span>
                            <span class="tech-tag">JavaScript</span>
                            <span class="tech-tag">GSAP</span>
                            <span class="tech-tag">Webpack</span>
                        </div>
                        <div class="metrics-list">
                            <div class="metric">⚡ <span class="metric-value">98/100</span> Lighthouse</div>
                            <div class="metric">🚀 <span class="metric-value">&lt;1.5s</span> FCP</div>
                            <div class="metric">♿ <span class="metric-value">WCAG 2.1 AA</span></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Statistics -->
        <section>
            <div class="section-header">
                <h2>Impact & Scale</h2>
                <p>Quantifiable achievements in production systems</p>
            </div>
            <div class="stats-grid">
                <div class="stat">
                    <div class="stat-number">500+</div>
                    <div class="stat-label">GitHub Contributions/Year</div>
                </div>
                <div class="stat">
                    <div class="stat-number">10+</div>
                    <div class="stat-label">Production Systems</div>
                </div>
                <div class="stat">
                    <div class="stat-number">99.9%</div>
                    <div class="stat-label">System Uptime</div>
                </div>
                <div class="stat">
                    <div class="stat-number">100K+</div>
                    <div class="stat-label">Monthly Active Users</div>
                </div>
                <div class="stat">
                    <div class="stat-number">1000+</div>
                    <div class="stat-label">Transactions/Second</div>
                </div>
                <div class="stat">
                    <div class="stat-number">2B+</div>
                    <div class="stat-label">Records Processed</div>
                </div>
            </div>
        </section>

        <!-- Learning Path -->
        <section>
            <div class="section-header">
                <h2>Continuous Learning</h2>
                <p>Current focus areas for growth and mastery</p>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <h4>📚 Distributed Systems</h4>
                    <p>Deep focus on consensus algorithms (Raft, PBFT), distributed transaction patterns, and eventual consistency models for globally distributed systems.</p>
                </div>
                <div class="timeline-item">
                    <h4>☸️ Advanced Kubernetes</h4>
                    <p>Mastering advanced Kubernetes patterns, service mesh architecture (Istio), and production-scale orchestration strategies.</p>
                </div>
                <div class="timeline-item">
                    <h4>🤖 ML Model Serving</h4>
                    <p>Exploring machine learning model serving at scale, ML pipeline orchestration, and operational best practices for production ML systems.</p>
                </div>
                <div class="timeline-item">
                    <h4>📊 Real-time Processing</h4>
                    <p>Advanced stream processing, real-time analytics pipelines, and event sourcing patterns for handling massive data streams at scale.</p>
                </div>
            </div>
        </section>

        <!-- Contact Footer -->
        <footer id="contact">
            <div class="footer-content">
                <h3>Let's Build Together</h3>
                <p>
                    I'm available for senior engineering roles, architecture consulting, technical mentorship, and strategic partnerships. Let's discuss how I can contribute to your team's success.
                </p>
                <div class="footer-links">
                    <a href="mailto:alagoudarpunit@gmail.com" class="footer-link">📧 Email</a>
                    <a href="https://linkedin.com/in/punit-alagoudar-4932442a3/" class="footer-link">💼 LinkedIn</a>
                    <a href="https://github.com/punitalagoudar" class="footer-link">⚙️ GitHub</a>
                    <a href="https://twitter.com/alagoudar93779" class="footer-link">𝕏 Twitter</a>
                    <a href="https://smart-ai-report-generator.onrender.com" class="footer-link">🌐 Portfolio</a>
                </div>
                <div class="footer-bottom">
                    <p>© 2025 Punit Alagoudar | Crafted with precision and passion</p>
                    <p>Building production-grade systems that scale, perform, and inspire</p>
                </div>
            </div>
        </footer>
    </div>
</body>
</html>
