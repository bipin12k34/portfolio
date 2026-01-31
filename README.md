# portfolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dr. Bipin Kumar Chaurasia - R&D Manager & Mechanical Engineering Researcher</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;900&family=Source+Sans+Pro:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-navy: #0d1b2a;
            --secondary-blue: #1b263b;
            --accent-burgundy: #8b2635;
            --accent-gold: #c5a572;
            --accent-teal: #2a9d8f;
            --text-cream: #f1faee;
            --text-gray: #a8b2c1;
            --bg-deep: #0a1118;
            --border-subtle: #1e2936;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Source Sans Pro', sans-serif;
            background: var(--primary-navy);
            color: var(--text-cream);
            line-height: 1.8;
            overflow-x: hidden;
        }

        /* Elegant Background */
        .bg-pattern {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.03;
            background-image: 
                repeating-linear-gradient(45deg, transparent, transparent 35px, var(--accent-gold) 35px, var(--accent-gold) 36px),
                repeating-linear-gradient(-45deg, transparent, transparent 35px, var(--accent-burgundy) 35px, var(--accent-burgundy) 36px);
            pointer-events: none;
            z-index: 0;
        }

        .bg-overlay {
            position: fixed;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle at 30% 50%, rgba(139, 38, 53, 0.08) 0%, transparent 50%),
                        radial-gradient(circle at 70% 80%, rgba(197, 165, 114, 0.06) 0%, transparent 50%);
            pointer-events: none;
            z-index: 0;
            animation: drift 30s ease-in-out infinite;
        }

        @keyframes drift {
            0%, 100% { transform: translate(0, 0) rotate(0deg); }
            50% { transform: translate(-5%, -5%) rotate(2deg); }
        }

        /* Container */
        .container {
            position: relative;
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 3rem;
            z-index: 1;
        }

        /* Header */
        header {
            padding: 2.5rem 0;
            border-bottom: 1px solid var(--border-subtle);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            background: rgba(13, 27, 42, 0.9);
            z-index: 100;
            animation: slideDown 0.6s ease-out;
        }

        @keyframes slideDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .logo-section {
            display: flex;
            flex-direction: column;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--accent-gold);
            letter-spacing: 0.02em;
        }

        .logo-subtitle {
            font-size: 0.85rem;
            color: var(--text-gray);
            margin-top: 0.25rem;
        }

        nav ul {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        nav a {
            color: var(--text-gray);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            position: relative;
            transition: color 0.3s ease;
            letter-spacing: 0.03em;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 2px;
            background: var(--accent-burgundy);
            transition: width 0.3s ease;
        }

        nav a:hover {
            color: var(--text-cream);
        }

        nav a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            padding: 8rem 0 6rem;
            animation: fadeIn 1s ease-out 0.2s both;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 5rem;
            align-items: center;
        }

        .hero-content h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(3rem, 6vw, 4.5rem);
            font-weight: 900;
            line-height: 1.1;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--text-cream) 0%, var(--accent-gold) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-title-sub {
            font-size: clamp(1.3rem, 2.5vw, 1.8rem);
            color: var(--accent-burgundy);
            font-weight: 600;
            margin-bottom: 2rem;
            font-family: 'Playfair Display', serif;
        }

        .hero-tagline {
            font-size: 1.2rem;
            color: var(--text-gray);
            margin-bottom: 2.5rem;
            line-height: 1.9;
            max-width: 600px;
        }

        .hero-meta {
            display: flex;
            flex-direction: column;
            gap: 0.75rem;
            margin-bottom: 3rem;
        }

        .meta-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            color: var(--text-gray);
            font-size: 0.95rem;
        }

        .meta-icon {
            width: 24px;
            height: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--accent-gold);
            font-size: 1.2rem;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1.1rem 2.8rem;
            border: none;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.4s ease;
            text-decoration: none;
            display: inline-block;
            letter-spacing: 0.03em;
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background: var(--accent-burgundy);
            color: var(--text-cream);
            box-shadow: 0 10px 30px rgba(139, 38, 53, 0.3);
        }

        .btn-primary:hover {
            background: #a32f45;
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(139, 38, 53, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: var(--accent-gold);
            border: 2px solid var(--accent-gold);
        }

        .btn-secondary:hover {
            background: var(--accent-gold);
            color: var(--primary-navy);
            transform: translateY(-3px);
        }

        /* Credentials Box */
        .credentials-box {
            background: linear-gradient(135deg, var(--secondary-blue) 0%, var(--bg-deep) 100%);
            padding: 3rem;
            border-radius: 8px;
            border: 1px solid var(--border-subtle);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4);
        }

        .credential-item {
            margin-bottom: 2rem;
            padding-bottom: 2rem;
            border-bottom: 1px solid var(--border-subtle);
        }

        .credential-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
            border-bottom: none;
        }

        .credential-label {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            color: var(--accent-gold);
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .credential-value {
            font-size: 1.1rem;
            color: var(--text-cream);
            font-weight: 600;
        }

        /* Section Styling */
        section {
            padding: 6rem 0;
            border-bottom: 1px solid var(--border-subtle);
            animation: fadeIn 1s ease-out both;
        }

        .section-header {
            margin-bottom: 4rem;
            text-align: center;
        }

        .section-tag {
            font-size: 0.85rem;
            color: var(--accent-burgundy);
            text-transform: uppercase;
            letter-spacing: 0.2em;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 4vw, 3.8rem);
            font-weight: 900;
            color: var(--text-cream);
            margin-bottom: 1.5rem;
        }

        .section-description {
            max-width: 800px;
            margin: 0 auto;
            color: var(--text-gray);
            font-size: 1.1rem;
            line-height: 1.9;
        }

        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2.5rem;
            margin: 4rem 0;
        }

        .stat-card {
            background: linear-gradient(135deg, var(--secondary-blue) 0%, var(--bg-deep) 100%);
            padding: 3rem 2rem;
            border-radius: 8px;
            border-left: 4px solid var(--accent-burgundy);
            transition: all 0.4s ease;
            text-align: center;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            border-left-color: var(--accent-gold);
            box-shadow: 0 20px 60px rgba(139, 38, 53, 0.2);
        }

        .stat-number {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 900;
            color: var(--accent-gold);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            color: var(--text-gray);
            font-size: 1rem;
            font-weight: 500;
        }

        /* Expertise Grid */
        .expertise-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .expertise-card {
            background: var(--secondary-blue);
            padding: 2.5rem;
            border-radius: 8px;
            border: 1px solid var(--border-subtle);
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .expertise-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 4px;
            height: 0;
            background: var(--accent-burgundy);
            transition: height 0.4s ease;
        }

        .expertise-card:hover {
            transform: translateX(10px);
            border-color: var(--accent-gold);
        }

        .expertise-card:hover::before {
            height: 100%;
        }

        .expertise-icon {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }

        .expertise-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--text-cream);
            margin-bottom: 1rem;
        }

        .expertise-description {
            color: var(--text-gray);
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .expertise-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            background: rgba(197, 165, 114, 0.1);
            color: var(--accent-gold);
            padding: 0.4rem 0.9rem;
            border-radius: 4px;
            font-size: 0.85rem;
            font-weight: 500;
            border: 1px solid rgba(197, 165, 114, 0.2);
        }

        /* Experience Timeline */
        .timeline {
            position: relative;
            max-width: 1000px;
            margin: 0 auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(to bottom, var(--accent-burgundy), var(--accent-gold));
        }

        .timeline-item {
            position: relative;
            margin-bottom: 4rem;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .timeline-content {
            background: var(--secondary-blue);
            padding: 2.5rem;
            border-radius: 8px;
            border: 1px solid var(--border-subtle);
            position: relative;
            transition: all 0.4s ease;
        }

        .timeline-item:nth-child(odd) .timeline-content {
            grid-column: 1;
        }

        .timeline-item:nth-child(even) .timeline-content {
            grid-column: 2;
        }

        .timeline-content:hover {
            border-color: var(--accent-burgundy);
            transform: scale(1.02);
            box-shadow: 0 15px 50px rgba(139, 38, 53, 0.2);
        }

        .timeline-marker {
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 20px;
            height: 20px;
            background: var(--accent-burgundy);
            border-radius: 50%;
            border: 4px solid var(--primary-navy);
            z-index: 10;
        }

        .timeline-date {
            color: var(--accent-gold);
            font-size: 0.9rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            margin-bottom: 1rem;
        }

        .timeline-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--text-cream);
            margin-bottom: 0.75rem;
        }

        .timeline-company {
            color: var(--accent-teal);
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 1.5rem;
        }

        .timeline-description {
            color: var(--text-gray);
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .timeline-highlights {
            list-style: none;
        }

        .timeline-highlights li {
            color: var(--text-gray);
            padding-left: 1.8rem;
            margin-bottom: 1rem;
            position: relative;
            line-height: 1.7;
        }

        .timeline-highlights li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: var(--accent-burgundy);
            font-weight: bold;
        }

        /* Publications Grid */
        .publications-grid {
            display: grid;
            gap: 2rem;
        }

        .publication-card {
            background: var(--secondary-blue);
            padding: 2rem;
            border-radius: 8px;
            border-left: 4px solid var(--accent-gold);
            transition: all 0.4s ease;
        }

        .publication-card:hover {
            transform: translateX(8px);
            border-left-color: var(--accent-burgundy);
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
        }

        .publication-type {
            display: inline-block;
            background: var(--accent-burgundy);
            color: var(--text-cream);
            padding: 0.4rem 1rem;
            border-radius: 4px;
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            margin-bottom: 1rem;
        }

        .publication-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--text-cream);
            margin-bottom: 1rem;
            line-height: 1.5;
        }

        .publication-authors {
            color: var(--text-gray);
            font-size: 0.95rem;
            margin-bottom: 0.75rem;
            font-style: italic;
        }

        .publication-venue {
            color: var(--accent-teal);
            font-size: 0.9rem;
            font-weight: 600;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 3rem;
        }

        .project-card {
            background: linear-gradient(135deg, var(--secondary-blue) 0%, var(--bg-deep) 100%);
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid var(--border-subtle);
            transition: all 0.4s ease;
            cursor: pointer;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 70px rgba(0, 0, 0, 0.4);
            border-color: var(--accent-gold);
        }

        .project-number {
            background: var(--accent-burgundy);
            padding: 1.5rem;
            text-align: center;
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 900;
            color: var(--text-cream);
        }

        .project-body {
            padding: 2.5rem;
        }

        .project-title {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--text-cream);
            margin-bottom: 1rem;
            line-height: 1.4;
        }

        .project-description {
            color: var(--text-gray);
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .project-tag {
            background: rgba(139, 38, 53, 0.2);
            color: var(--accent-burgundy);
            padding: 0.4rem 0.9rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: 600;
            border: 1px solid rgba(139, 38, 53, 0.3);
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .contact-card {
            background: var(--secondary-blue);
            padding: 2.5rem;
            border-radius: 8px;
            border: 1px solid var(--border-subtle);
            text-align: center;
            transition: all 0.4s ease;
            text-decoration: none;
            display: block;
        }

        .contact-card:hover {
            border-color: var(--accent-burgundy);
            transform: translateY(-8px);
            box-shadow: 0 15px 50px rgba(139, 38, 53, 0.3);
        }

        .contact-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }

        .contact-label {
            color: var(--accent-gold);
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 0.1em;
            font-weight: 700;
            margin-bottom: 0.75rem;
        }

        .contact-value {
            color: var(--text-cream);
            font-weight: 600;
            font-size: 1.1rem;
            word-break: break-word;
        }

        /* Footer */
        footer {
            padding: 4rem 0;
            text-align: center;
            color: var(--text-gray);
            border-top: 1px solid var(--border-subtle);
        }

        footer p {
            margin-bottom: 1rem;
        }

        footer a {
            color: var(--accent-gold);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        footer a:hover {
            color: var(--accent-burgundy);
        }

        .orcid-link {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            margin-top: 1rem;
            color: var(--accent-teal);
            text-decoration: none;
            font-weight: 600;
        }

        .orcid-link:hover {
            color: var(--accent-gold);
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .hero-grid {
                grid-template-columns: 1fr;
                gap: 3rem;
            }

            .timeline::before {
                left: 0;
            }

            .timeline-item {
                grid-template-columns: 1fr;
                gap: 0;
            }

            .timeline-item:nth-child(odd) .timeline-content,
            .timeline-item:nth-child(even) .timeline-content {
                grid-column: 1;
            }

            .timeline-marker {
                left: 0;
                transform: translateX(-50%);
            }

            .timeline-content {
                margin-left: 3rem;
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 0 1.5rem;
            }

            .header-content {
                flex-direction: column;
                align-items: flex-start;
            }

            nav ul {
                flex-direction: column;
                gap: 1rem;
            }

            .hero {
                padding: 4rem 0 3rem;
            }

            section {
                padding: 4rem 0;
            }

            .projects-grid,
            .expertise-grid {
                grid-template-columns: 1fr;
            }

            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: var(--primary-navy);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--accent-burgundy);
            border-radius: 5px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: var(--accent-gold);
        }
    </style>
</head>
<body>
    <div class="bg-pattern"></div>
    <div class="bg-overlay"></div>

    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo-section">
                    <div class="logo">Dr. Bipin Kumar Chaurasia</div>
                    <div class="logo-subtitle">Ph.D. Mechanical Engineering | R&D Manager</div>
                </div>
                <nav>
                    <ul>
                        <li><a href="#about">About</a></li>
                        <li><a href="#expertise">Expertise</a></li>
                        <li><a href="#experience">Experience</a></li>
                        <li><a href="#research">Research</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-grid">
                <div class="hero-content">
                    <h1>Advancing Safety Through Innovation</h1>
                    <p class="hero-title-sub">R&D Manager & Research Scholar</p>
                    <p class="hero-tagline">
                        Leading cutting-edge research in composite materials, impact dynamics, and safety systems. 
                        Bridging academic excellence with industrial innovation in high-risk environment protection.
                    </p>
                    <div class="hero-meta">
                        <div class="meta-item">
                            <span class="meta-icon">📍</span>
                            <span>Ahmedabad, Gujarat, India</span>
                        </div>
                        <div class="meta-item">
                            <span class="meta-icon">🏢</span>
                            <span>Indian Inovatix Limited, R&D Department</span>
                        </div>
                        <div class="meta-item">
                            <span class="meta-icon">🎓</span>
                            <span>Ph.D., NIT Jamshedpur | M.Tech., NIT Rourkela</span>
                        </div>
                    </div>
                    <div class="hero-buttons">
                        <a href="#contact" class="btn btn-primary">Connect With Me</a>
                        <a href="#research" class="btn btn-secondary">View Publications</a>
                    </div>
                </div>
                <div class="credentials-box">
                    <div class="credential-item">
                        <div class="credential-label">Current Position</div>
                        <div class="credential-value">R&D Manager</div>
                    </div>
                    <div class="credential-item">
                        <div class="credential-label">Specialization</div>
                        <div class="credential-value">Composite Materials & Safety Systems</div>
                    </div>
                    <div class="credential-item">
                        <div class="credential-label">Research Focus</div>
                        <div class="credential-value">High Strain Rate Impact Dynamics</div>
                    </div>
                    <div class="credential-item">
                        <div class="credential-label">Patent Granted</div>
                        <div class="credential-value">Portable Ball Milling Machine</div>
                    </div>
                    <div class="credential-item">
                        <div class="credential-label">ORCID</div>
                        <div class="credential-value" style="font-size: 0.9rem;">0000-0001-7577-7242</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section id="stats" style="padding: 4rem 0; border: none;">
        <div class="container">
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number">6+</div>
                    <div class="stat-label">SCI/SCIE Publications</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">6+</div>
                    <div class="stat-label">Major Projects</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1</div>
                    <div class="stat-label">Design Patent Granted</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">5+</div>
                    <div class="stat-label">Years Teaching Experience</div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Professional Summary</div>
                <h2 class="section-title">About Me</h2>
                <p class="section-description">
                    Mechanical Engineer and researcher with Ph.D.-level expertise in composite materials, impact dynamics, 
                    damage mechanics, and structural design, complemented by industrial R&D management experience in safety 
                    and rescue systems. Currently serving as R&D Manager at Indian Inovatix Limited with responsibility for 
                    magnetic braking systems, emergency escape devices, and fall-arrest solutions for high-risk environments.
                </p>
            </div>
            <p class="section-description" style="margin-top: 2rem;">
                My research track record includes SCI/SCIE publications, a granted design patent, funded projects, and 
                extensive postgraduate teaching assistance across mechanical engineering laboratories. I maintain active 
                research collaborations in multifunctional composites and impact dynamics, bridging the gap between academic 
                innovation and industrial application.
            </p>
        </div>
    </section>

    <!-- Expertise Section -->
    <section id="expertise">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Core Competencies</div>
                <h2 class="section-title">Areas of Expertise</h2>
            </div>
            <div class="expertise-grid">
                <div class="expertise-card">
                    <div class="expertise-icon">🔬</div>
                    <h3 class="expertise-title">Composite Materials</h3>
                    <p class="expertise-description">
                        Advanced research in laminated composites, damage mechanics, and failure analysis under various loading conditions.
                    </p>
                    <div class="expertise-tags">
                        <span class="tag">CFRP</span>
                        <span class="tag">GFRP</span>
                        <span class="tag">Hybrid Composites</span>
                    </div>
                </div>
                <div class="expertise-card">
                    <div class="expertise-icon">⚡</div>
                    <h3 class="expertise-title">Impact Dynamics</h3>
                    <p class="expertise-description">
                        High strain rate modeling and impact testing of advanced materials for defense and aerospace applications.
                    </p>
                    <div class="expertise-tags">
                        <span class="tag">High Strain Rate</span>
                        <span class="tag">Dynamic Loading</span>
                        <span class="tag">Damage Evolution</span>
                    </div>
                </div>
                <div class="expertise-card">
                    <div class="expertise-icon">🛡️</div>
                    <h3 class="expertise-title">Safety Systems Design</h3>
                    <p class="expertise-description">
                        Development of magnetic braking systems, emergency escape devices, and fall-arrest solutions for industrial safety.
                    </p>
                    <div class="expertise-tags">
                        <span class="tag">Magnetic Brakes</span>
                        <span class="tag">Eddy Current</span>
                        <span class="tag">Emergency Systems</span>
                    </div>
                </div>
                <div class="expertise-card">
                    <div class="expertise-icon">💻</div>
                    <h3 class="expertise-title">Computational Analysis</h3>
                    <p class="expertise-description">
                        Expert in finite element analysis using COMSOL Multiphysics, ANSYS, and ABAQUS for structural validation.
                    </p>
                    <div class="expertise-tags">
                        <span class="tag">COMSOL</span>
                        <span class="tag">ANSYS</span>
                        <span class="tag">ABAQUS</span>
                        <span class="tag">FEA</span>
                    </div>
                </div>
                <div class="expertise-card">
                    <div class="expertise-icon">⚙️</div>
                    <h3 class="expertise-title">Product Development</h3>
                    <p class="expertise-description">
                        CAD/CAM-based design, prototype testing, and certification of safety-critical systems for industrial deployment.
                    </p>
                    <div class="expertise-tags">
                        <span class="tag">SolidWorks</span>
                        <span class="tag">CATIA V5</span>
                        <span class="tag">AutoCAD</span>
                    </div>
                </div>
                <div class="expertise-card">
                    <div class="expertise-icon">📊</div>
                    <h3 class="expertise-title">Research & Innovation</h3>
                    <p class="expertise-description">
                        Leading interdisciplinary research teams, managing funded projects, and publishing in high-impact journals.
                    </p>
                    <div class="expertise-tags">
                        <span class="tag">SCI Publications</span>
                        <span class="tag">Patent Design</span>
                        <span class="tag">Project Management</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Career Trajectory</div>
                <h2 class="section-title">Professional Experience</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">January 2024 - Present</div>
                        <h3 class="timeline-title">R&D Manager</h3>
                        <div class="timeline-company">Indian Inovatix Limited</div>
                        <p class="timeline-description">
                            Leading R&D activities and product development for magnetic braking systems, emergency escape devices, 
                            and fall-arrest solutions for high-risk industrial environments.
                        </p>
                        <ul class="timeline-highlights">
                            <li>Managing cross-functional teams across design, testing, certification, and deployment of safety-critical systems</li>
                            <li>Overseeing COMSOL Multiphysics and FEA-based electromagnetic and structural validation of braking and safety devices</li>
                            <li>Developing product roadmaps and technical specifications for next-generation safety systems</li>
                            <li>Collaborating with academic partners (Ahmedabad University) and industrial stakeholders for advanced research and commercialization</li>
                        </ul>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-marker"></div>
                    <div class="timeline-content">
                        <div class="timeline-date">January 2023 - January 2024</div>
                        <h3 class="timeline-title">R&D Engineer</h3>
                        <div class="timeline-company">Indian Inovatix Limited</div>
                        <p class="timeline-description">
                            Designed and developed magnetic braking systems using Samarium-Cobalt permanent magnets for safety and rescue applications.
                        </p>
                        <ul class="timeline-highlights">
                            <li>Executed COMSOL Multiphysics simulations for coupled electromagnetic and structural response validation</li>
                            <li>Developed Top Man Emergency Escape Devices, confined-space safety systems, and fall-arrest solutions</li>
                            <li>Performed prototype testing and validation of safety-critical systems for high-risk industrial environments</li>
                            <li>Collaborated cross-functionally with design, testing, and compliance teams for product certification</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Research Section -->
    <section id="research">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Academic Contributions</div>
                <h2 class="section-title">Research & Publications</h2>
                <p class="section-description">
                    Published research in high-impact SCI/SCIE journals focusing on composite materials, impact dynamics, 
                    and structural analysis. Active presenter at international conferences with ongoing research collaborations.
                </p>
            </div>

            <h3 style="font-family: 'Playfair Display', serif; font-size: 2rem; color: var(--accent-gold); margin: 3rem 0 2rem;">
                Peer-Reviewed Journal Publications
            </h3>
            <div class="publications-grid">
                <div class="publication-card">
                    <span class="publication-type">SCI Journal</span>
                    <h4 class="publication-title">
                        Experimental studies of failure in L-shaped carbon fiber-reinforced polymer composite under pullout and four-point bending
                    </h4>
                    <p class="publication-authors">Chaurasia, B.K., Kumar, D., & Paswan, M.K.</p>
                    <p class="publication-venue">
                        Journal of The Institution of Engineers (India) Series D, 103, 889–897 (2022)
                    </p>
                </div>

                <div class="publication-card">
                    <span class="publication-type">SCIE Journal</span>
                    <h4 class="publication-title">
                        Water immersion test and its effect on the mechanical behavior of reinforced natural fiber composites
                    </h4>
                    <p class="publication-authors">Haque, S.A., Ghosh, I., Chaurasia, B.K., & Paswan, M.K.</p>
                    <p class="publication-venue">
                        Annals of the Bhandarkar Oriental Research Institute, 104(7), 45–62 (2023)
                    </p>
                </div>

                <div class="publication-card">
                    <span class="publication-type">Under Review</span>
                    <h4 class="publication-title">
                        Damage interaction in carbon fiber reinforced polymer laminates under in-plane loading
                    </h4>
                    <p class="publication-authors">Chaurasia, B.K., Kumar, D., & Paswan, M.K.</p>
                    <p class="publication-venue">Composite Structures (SCI)</p>
                </div>

                <div class="publication-card">
                    <span class="publication-type">Under Review</span>
                    <h4 class="publication-title">
                        Dynamic compressive impact behavior of CFRP composite under high strain rate loading
                    </h4>
                    <p class="publication-authors">Chaurasia, B.K., Kumar, D., & Paswan, M.K.</p>
                    <p class="publication-venue">Part C: Journal of Mechanical Engineering Science (ESCI)</p>
                </div>

                <div class="publication-card">
                    <span class="publication-type">Under Review</span>
                    <h4 class="publication-title">
                        Modeling of damage evolution of laminated composites under high strain rate loading
                    </h4>
                    <p class="publication-authors">Chaurasia, B.K., Kumar, D., & Paswan, M.K.</p>
                    <p class="publication-venue">Composite Part B: Engineering (SCI)</p>
                </div>
            </div>

            <h3 style="font-family: 'Playfair Display', serif; font-size: 2rem; color: var(--accent-gold); margin: 4rem 0 2rem;">
                Book Chapters
            </h3>
            <div class="publications-grid">
                <div class="publication-card">
                    <span class="publication-type">Book Chapter</span>
                    <h4 class="publication-title">
                        Investigation of failure in L-shaped woven carbon fiber-reinforced polymer composite under pull-out and four-point bending
                    </h4>
                    <p class="publication-authors">Chaurasia, B.K., Kumar, D., & Acharya, S.K.</p>
                    <p class="publication-venue">
                        Recent Advances in Manufacturing, Automation, Design and Energy Technologies, pp. 693–703. Springer, Singapore (2022)
                    </p>
                </div>

                <div class="publication-card">
                    <span class="publication-type">Book Chapter</span>
                    <h4 class="publication-title">
                        Damage studies in curved hybrid laminates under pull-out loading
                    </h4>
                    <p class="publication-authors">Chaurasia, B.K., Kumar, D., & Roy, R.</p>
                    <p class="publication-venue">
                        Advance Composite Material and Structures: Modeling and Analysis (In Press)
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Innovation Portfolio</div>
                <h2 class="section-title">Major Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-number">01</div>
                    <div class="project-body">
                        <h3 class="project-title">Food Wastage Recycler Machine</h3>
                        <p class="project-description">
                            Developed prototype with waste segregation and processing capabilities. Sponsored by National Institute 
                            of Design (NID), Ministry of Education, Government of India.
                        </p>
                        <div class="project-tags">
                            <span class="project-tag">Government Funded</span>
                            <span class="project-tag">Prototype Development</span>
                            <span class="project-tag">Sustainability</span>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-number">02</div>
                    <div class="project-body">
                        <h3 class="project-title">Portable Ball Milling Machine</h3>
                        <p class="project-description">
                            Design patent granted (Application No: 356784-001). Engineered cost-effective grinding solution with 
                            improved efficiency and portability for industrial applications.
                        </p>
                        <div class="project-tags">
                            <span class="project-tag">Patent Granted</span>
                            <span class="project-tag">Industrial Design</span>
                            <span class="project-tag">Innovation</span>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-number">03</div>
                    <div class="project-body">
                        <h3 class="project-title">High Strain Rate Modelling of CFRP Composite</h3>
                        <p class="project-description">
                            Dynamic compressive loading analysis and damage evolution mechanisms using ANSYS/ABAQUS. 
                            Core component of Ph.D. thesis work on advanced composites.
                        </p>
                        <div class="project-tags">
                            <span class="project-tag">FEA Analysis</span>
                            <span class="project-tag">CFRP</span>
                            <span class="project-tag">Ph.D. Research</span>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-number">04</div>
                    <div class="project-body">
                        <h3 class="project-title">C-shaped Hybrid Laminates Design</h3>
                        <p class="project-description">
                            International collaborative project with Gyeongsang National University, Jinju, South Korea. 
                            Explored novel laminate geometries for improved structural performance.
                        </p>
                        <div class="project-tags">
                            <span class="project-tag">International Collaboration</span>
                            <span class="project-tag">Hybrid Composites</span>
                            <span class="project-tag">Structural Analysis</span>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-number">05</div>
                    <div class="project-body">
                        <h3 class="project-title">Aluminium Riveted Joint Analysis</h3>
                        <p class="project-description">
                            Experimental and numerical investigations for failure prediction and load capacity assessment 
                            in aerospace applications with focus on joint reliability.
                        </p>
                        <div class="project-tags">
                            <span class="project-tag">Aerospace</span>
                            <span class="project-tag">Joint Analysis</span>
                            <span class="project-tag">Failure Prediction</span>
                        </div>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-number">06</div>
                    <div class="project-body">
                        <h3 class="project-title">Cost-effective Vehicle Axle Development</h3>
                        <p class="project-description">
                            Industrial collaboration with RSB Transmission (I) Ltd., Jamshedpur. Designed front and rear axle 
                            for 12-14 ton load-carrying vehicle, reducing material costs while maintaining structural integrity.
                        </p>
                        <div class="project-tags">
                            <span class="project-tag">Industry Partnership</span>
                            <span class="project-tag">Cost Optimization</span>
                            <span class="project-tag">Heavy Vehicle</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Let's Connect</div>
                <h2 class="section-title">Contact Information</h2>
                <p class="section-description">
                    Open to research partnerships, consulting projects, and faculty positions in mechanical engineering, 
                    composite materials, and safety systems design. Available for collaboration and professional engagement.
                </p>
            </div>
            <div class="contact-grid">
                <a href="mailto:bipinkumarnit1617@gmail.com" class="contact-card">
                    <div class="contact-icon">📧</div>
                    <div class="contact-label">Primary Email</div>
                    <div class="contact-value">bipinkumarnit1617@gmail.com</div>
                </a>
                <a href="mailto:2018rsme005@nitjsr.ac.in" class="contact-card">
                    <div class="contact-icon">🎓</div>
                    <div class="contact-label">Academic Email</div>
                    <div class="contact-value">2018rsme005@nitjsr.ac.in</div>
                </a>
                <a href="tel:+918596873411" class="contact-card">
                    <div class="contact-icon">📱</div>
                    <div class="contact-label">Mobile (Primary)</div>
                    <div class="contact-value">+91-8596873411</div>
                </a>
                <a href="tel:+919348589634" class="contact-card">
                    <div class="contact-icon">📞</div>
                    <div class="contact-label">Mobile (Alternate)</div>
                    <div class="contact-value">+91-9348589634</div>
                </a>
                <a href="https://orcid.org/0000-0001-7577-7242" target="_blank" class="contact-card">
                    <div class="contact-icon">🔬</div>
                    <div class="contact-label">ORCID</div>
                    <div class="contact-value">0000-0001-7577-7242</div>
                </a>
                <div class="contact-card" style="cursor: default;">
                    <div class="contact-icon">📍</div>
                    <div class="contact-label">Location</div>
                    <div class="contact-value">Ahmedabad, Gujarat, India</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p style="font-family: 'Playfair Display', serif; font-size: 1.2rem; font-weight: 700; color: var(--accent-gold); margin-bottom: 1.5rem;">
                Dr. Bipin Kumar Chaurasia
            </p>
            <p>Ph.D. Mechanical Engineering | R&D Manager | Safety & Rescue Systems Specialist</p>
            <p style="margin-top: 1rem;">Indian Inovatix Limited | Ahmedabad, Gujarat, India</p>
            <a href="https://orcid.org/0000-0001-7577-7242" target="_blank" class="orcid-link">
                <span>🔗</span> ORCID: 0000-0001-7577-7242
            </a>
            <p style="margin-top: 2rem; font-size: 0.9rem; color: var(--text-gray);">
                &copy; 2026 Dr. Bipin Kumar Chaurasia. All rights reserved.
            </p>
            <p style="font-size: 0.85rem; margin-top: 0.5rem;">
                Document prepared for professional use across academic, industrial, and consulting contexts.
            </p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Intersection Observer for scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe sections
        document.querySelectorAll('section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(40px)';
            section.style.transition = 'opacity 1s ease, transform 1s ease';
            observer.observe(section);
        });

        // Active navigation state
        window.addEventListener('scroll', () => {
            let current = '';
            const sections = document.querySelectorAll('section');
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            document.querySelectorAll('nav a').forEach(link => {
                link.style.color = 'var(--text-gray)';
                if (link.getAttribute('href') === `#${current}`) {
                    link.style.color = 'var(--accent-gold)';
                }
            });
        });

        // Parallax effect for background
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const bgOverlay = document.querySelector('.bg-overlay');
            bgOverlay.style.transform = `translate(-50%, -50%) translateY(${scrolled * 0.3}px)`;
        });
    </script>
</body>
</html>
