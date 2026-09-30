<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Deepsikha Kar - Data Analyst & Designer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #0d1117;
            --bg-secondary: #161b22;
            --bg-tertiary: #21262d;
            --border-color: #30363d;
            --text-primary: #c9d1d9;
            --text-secondary: #8b949e;
            --accent-blue: #1f6feb;
            --accent-purple: #8957e5;
            --accent-green: #3fb950;
            --accent-orange: #fb8500;
            --success: #238636;
            --danger: #da3633;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: linear-gradient(135deg, var(--bg-primary) 0%, #0a0e12 100%);
            color: var(--text-primary);
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Animated background elements */
        .background-float {
            position: fixed;
            opacity: 0.05;
            pointer-events: none;
        }

        .float-1 {
            width: 400px;
            height: 400px;
            background: var(--accent-blue);
            border-radius: 50%;
            top: -100px;
            right: -100px;
            animation: float 20s ease-in-out infinite;
        }

        .float-2 {
            width: 300px;
            height: 300px;
            background: var(--accent-purple);
            border-radius: 50%;
            bottom: -50px;
            left: -100px;
            animation: float 15s ease-in-out infinite reverse;
        }

        .float-3 {
            width: 250px;
            height: 250px;
            background: var(--accent-green);
            border-radius: 50%;
            top: 50%;
            right: 5%;
            animation: float 18s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(30px); }
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes glow {
            0%, 100% { text-shadow: 0 0 10px rgba(31, 111, 235, 0.5); }
            50% { text-shadow: 0 0 20px rgba(137, 87, 229, 0.8); }
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 1;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 60px 20px;
            animation: slideInUp 0.8s ease-out;
        }

        .hero-content h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 10px;
            background: linear-gradient(135deg, var(--accent-blue), var(--accent-purple), var(--accent-green));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: glow 3s ease-in-out infinite;
        }

        .hero-content p {
            font-size: 1.4rem;
            color: var(--text-secondary);
            margin-bottom: 20px;
            font-weight: 300;
        }

        .hero-badges {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 30px;
        }

        .badge {
            display: inline-block;
            padding: 8px 16px;
            background: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            font-size: 0.9rem;
            color: var(--text-secondary);
            transition: all 0.3s ease;
        }

        .badge:hover {
            border-color: var(--accent-blue);
            color: var(--accent-blue);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(31, 111, 235, 0.2);
        }

        /* Section Styles */
        section {
            padding: 80px 0;
            border-top: 1px solid var(--border-color);
        }

        section:first-of-type {
            border-top: none;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 50px;
            text-align: center;
            position: relative;
            display: inline-block;
            width: 100%;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-blue), var(--accent-purple));
            margin: 15px auto 0;
            border-radius: 2px;
        }

        /* About Section */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
            margin-top: 40px;
        }

        .about-card {
            background: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 30px;
            transition: all 0.3s ease;
            animation: slideInUp 0.8s ease-out;
        }

        .about-card:hover {
            border-color: var(--accent-purple);
            transform: translateY(-5px);
            box-shadow: 0 8px 24px rgba(137, 87, 229, 0.15);
        }

        .about-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: var(--accent-purple);
        }

        .about-card p {
            color: var(--text-secondary);
            line-height: 1.8;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .skill-category {
            background: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 25px;
            transition: all 0.3s ease;
        }

        .skill-category:hover {
            border-color: var(--accent-green);
            box-shadow: 0 8px 24px rgba(63, 185, 80, 0.15);
        }

        .skill-category h4 {
            color: var(--accent-green);
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .skill-tag {
            display: inline-block;
            background: var(--bg-tertiary);
            border: 1px solid var(--border-color);
            color: var(--text-secondary);
            padding: 6px 12px;
            border-radius: 6px;
            margin: 5px 5px 5px 0;
            font-size: 0.85rem;
            transition: all 0.2s ease;
        }

        .skill-tag:hover {
            background: var(--accent-green);
            border-color: var(--accent-green);
            color: var(--bg-primary);
        }

        /* Workflow Diagram */
        .workflow-container {
            margin-top: 50px;
            display: flex;
            justify-content: center;
            overflow-x: auto;
            padding: 30px 0;
        }

        .workflow-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 0 20px;
            min-width: 150px;
            position: relative;
        }

        .workflow-circle {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background: var(--bg-secondary);
            border: 2px solid var(--accent-blue);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            margin-bottom: 15px;
        }

        .workflow-item:nth-child(2) .workflow-circle {
            border-color: var(--accent-purple);
        }

        .workflow-item:nth-child(3) .workflow-circle {
            border-color: var(--accent-green);
        }

        .workflow-circle:hover {
            transform: scale(1.1);
            box-shadow: 0 0 20px currentColor;
        }

        .workflow-arrow {
            position: absolute;
            top: 45px;
            width: 60px;
            height: 2px;
            background: var(--border-color);
        }

        .workflow-arrow::after {
            content: '';
            position: absolute;
            right: -8px;
            top: -4px;
            width: 0;
            height: 0;
            border-left: 8px solid var(--border-color);
            border-top: 4px solid transparent;
            border-bottom: 4px solid transparent;
        }

        .workflow-item:last-child .workflow-arrow {
            display: none;
        }

        .workflow-label {
            font-size: 0.85rem;
            color: var(--text-secondary);
            text-align: center;
            margin-top: 10px;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .project-card {
            background: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 30px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, var(--accent-blue), var(--accent-purple), var(--accent-green));
            transition: left 0.3s ease;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            border-color: var(--accent-blue);
            transform: translateY(-8px);
            box-shadow: 0 12px 32px rgba(31, 111, 235, 0.2);
        }

        .project-icon {
            font-size: 2rem;
            margin-bottom: 15px;
        }

        .project-card h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--text-primary);
        }

        .project-tag {
            display: inline-block;
            background: rgba(31, 111, 235, 0.1);
            color: var(--accent-blue);
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.75rem;
            margin-right: 8px;
            margin-bottom: 10px;
        }

        .project-card p {
            color: var(--text-secondary);
            font-size: 0.95rem;
            line-height: 1.7;
        }

        /* Timeline / Vision Section */
        .timeline {
            position: relative;
            padding: 40px 0;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: var(--border-color);
        }

        .timeline-item {
            margin-bottom: 50px;
            position: relative;
        }

        .timeline-item:nth-child(odd) {
            padding-right: 52%;
            text-align: right;
        }

        .timeline-item:nth-child(even) {
            padding-left: 52%;
        }

        .timeline-dot {
            position: absolute;
            left: 50%;
            top: 0;
            transform: translateX(-50%);
            width: 16px;
            height: 16px;
            background: var(--accent-blue);
            border: 3px solid var(--bg-primary);
            border-radius: 50%;
            transition: all 0.3s ease;
        }

        .timeline-item:nth-child(2) .timeline-dot {
            background: var(--accent-purple);
        }

        .timeline-item:nth-child(3) .timeline-dot {
            background: var(--accent-green);
        }

        .timeline-dot:hover {
            transform: translateX(-50%) scale(1.5);
            box-shadow: 0 0 15px currentColor;
        }

        .timeline-content {
            background: var(--bg-secondary);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 20px;
            transition: all 0.3s ease;
        }

        .timeline-content:hover {
            border-color: var(--accent-blue);
            box-shadow: 0 8px 24px rgba(31, 111, 235, 0.1);
        }

        .timeline-content h4 {
            color: var(--text-primary);
            margin-bottom: 8px;
        }

        .timeline-period {
            color: var(--text-secondary);
            font-size: 0.85rem;
            margin-bottom: 10px;
        }

        /* Footer */
        footer {
            border-top: 1px solid var(--border-color);
            padding: 40px 0;
            text-align: center;
            color: var(--text-secondary);
        }

        .footer-content {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-bottom: 20px;
        }

        .footer-link {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-link:hover {
            color: var(--accent-blue);
        }

        .philosophy-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .philosophy-card {
            background: linear-gradient(135deg, rgba(31, 111, 235, 0.1), rgba(137, 87, 229, 0.1));
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 25px;
            transition: all 0.3s ease;
        }

        .philosophy-card:hover {
            border-color: var(--accent-blue);
            transform: translateY(-5px);
        }

        .philosophy-card h4 {
            color: var(--accent-blue);
            margin-bottom: 12px;
            font-size: 1.1rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.5rem;
            }

            .hero-content p {
                font-size: 1.1rem;
            }

            .about-grid, 
            .timeline::before {
                grid-template-columns: 1fr;
                display: block;
            }

            .timeline::before {
                left: 10px;
            }

            .timeline-item:nth-child(odd),
            .timeline-item:nth-child(even) {
                padding-left: 50px;
                padding-right: 0;
                text-align: left;
            }

            .timeline-dot {
                left: 0;
            }

            .section-title {
                font-size: 1.8rem;
            }

            .workflow-container {
                flex-direction: column;
                align-items: center;
            }

            .workflow-arrow {
                display: none;
            }

            .workflow-item {
                margin: 20px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Floating background elements -->
    <div class="background-float float-1"></div>
    <div class="background-float float-2"></div>
    <div class="background-float float-3"></div>

    <div class="container">
        <!-- Hero Section -->
        <section class="hero">
            <div class="hero-content">
                <h1>Deepsikha Kar</h1>
                <p>Data Analyst • Designer • Strategic Thinker</p>
                <div class="hero-badges">
                    <div class="badge">📊 Data Analytics</div>
                    <div class="badge">🎨 Design & UX</div>
                    <div class="badge">👥 Management</div>
                    <div class="badge">🚀 Problem Solver</div>
                    <div class="badge">📈 Growth Mindset</div>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section>
            <h2 class="section-title">About Me</h2>
            <div class="about-grid">
                <div class="about-card">
                    <h3>🎯 My Mission</h3>
                    <p>I'm a second-year BCA student at RCC Institute of Information Technology, driven by the intersection of data, design, and people management. My goal is to become a data-driven designer and strategic analyst who bridges the gap between technical solutions and human-centered decision-making.</p>
                </div>
                <div class="about-card">
                    <h3>💡 My Philosophy</h3>
                    <p>I believe in transforming raw data into compelling stories through beautiful visualization. Every number has a narrative, and every design should empower decision-makers. I'm passionate about building solutions that are not just analytically sound but also intuitively beautiful and strategically impactful.</p>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section>
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h4>💻 Programming</h4>
                    <span class="skill-tag">C</span>
                    <span class="skill-tag">Java</span>
                    <span class="skill-tag">HTML</span>
                    <span class="skill-tag">Python (Learning)</span>
                </div>
                <div class="skill-category">
                    <h4>📊 Data Analytics</h4>
                    <span class="skill-tag">SQL Workbench</span>
                    <span class="skill-tag">Tableau</span>
                    <span class="skill-tag">Excel (Advanced)</span>
                    <span class="skill-tag">Data Visualization</span>
                </div>
                <div class="skill-category">
                    <h4>🎨 Design & Creative</h4>
                    <span class="skill-tag">Canva</span>
                    <span class="skill-tag">UI/UX Thinking</span>
                    <span class="skill-tag">Design Thinking</span>
                    <span class="skill-tag">Visual Communication</span>
                </div>
                <div class="skill-category">
                    <h4>🌍 Languages</h4>
                    <span class="skill-tag">English</span>
                    <span class="skill-tag">Bengali</span>
                    <span class="skill-tag">Hindi</span>
                </div>
                <div class="skill-category">
                    <h4>🤝 Soft Skills</h4>
                    <span class="skill-tag">Project Management</span>
                    <span class="skill-tag">Team Leadership</span>
                    <span class="skill-tag">Communication</span>
                    <span class="skill-tag">Problem Solving</span>
                </div>
                <div class="skill-category">
                    <h4>📚 Certifications</h4>
                    <span class="skill-tag">Deloitte Analytics (Forage)</span>
                    <span class="skill-tag">SIH Hackathon</span>
                </div>
