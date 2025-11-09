

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Developer Portfolio</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.0/font/bootstrap-icons.css">
    <style>
        :root {
            --primary-color: #6366f1;
            --secondary-color: #8b5cf6;
            --dark-color: #1e293b;
            --light-bg: #f8fafc;
            --card-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background-color: var(--light-bg);
            color: var(--dark-color);
            overflow-x: hidden;
        }
        
        /* Navbar Styles */
        .navbar {
            background-color: white;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
            padding: 1rem 0;
            transition: all 0.3s ease;
        }
        
        .navbar-brand {
            font-weight: 700;
            font-size: 1.5rem;
            color: var(--primary-color) !important;
            display: flex;
            align-items: center;
        }
        
        .navbar-brand i {
            margin-right: 0.5rem;
        }
        
        .navbar-nav .nav-link {
            color: var(--dark-color) !important;
            font-weight: 500;
            margin: 0 0.5rem;
            transition: color 0.3s ease;
            position: relative;
        }
        
        .navbar-nav .nav-link:hover {
            color: var(--primary-color) !important;
        }
        
        .navbar-nav .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary-color);
            transition: width 0.3s ease;
        }
        
        .navbar-nav .nav-link:hover::after {
            width: 100%;
        }
        
        /* Dropdown Menu Styles */
        .dropdown-menu {
            border: none;
            box-shadow: var(--card-shadow);
            border-radius: 12px;
            padding: 0.5rem 0;
            margin-top: 0.5rem;
            animation: fadeIn 0.3s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .dropdown-item {
            padding: 0.75rem 1.5rem;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
        }
        
        .dropdown-item:hover {
            background-color: rgba(99, 102, 241, 0.1);
            color: var(--primary-color);
        }
        
        .dropdown-item i {
            margin-right: 0.75rem;
            color: var(--primary-color);
        }
        
        /* Hero Section */
        .hero-section {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 100px 0;
            position: relative;
            overflow: hidden;
        }
        
        .hero-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,96L48,112C96,128,192,160,288,160C384,160,480,128,576,122.7C672,117,768,139,864,154.7C960,171,1056,181,1152,165.3C1248,149,1344,107,1392,85.3L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>') no-repeat bottom;
            background-size: cover;
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
        }
        
        .hero-title {
            font-weight: 800;
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            animation: slideInDown 0.8s ease;
        }
        
        @keyframes slideInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: slideInUp 0.8s ease;
        }
        
        @keyframes slideInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .hero-buttons {
            animation: fadeIn 1s ease;
        }
        
        .btn-hero {
            padding: 12px 30px;
            font-weight: 600;
            border-radius: 50px;
            margin-right: 1rem;
            margin-bottom: 1rem;
            transition: all 0.3s ease;
        }
        
        .btn-primary-custom {
            background-color: white;
            color: var(--primary-color);
            border: none;
        }
        
        .btn-primary-custom:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .btn-outline-custom {
            background-color: transparent;
            color: white;
            border: 2px solid white;
        }
        
        .btn-outline-custom:hover {
            background-color: white;
            color: var(--primary-color);
            transform: translateY(-3px);
        }
        
        /* Featured Projects Section */
        .featured-projects {
            padding: 80px 0;
        }
        
        .section-title {
            font-weight: 700;
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--dark-color);
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            border-radius: 2px;
        }
        
        .section-subtitle {
            color: #64748b;
            margin-bottom: 3rem;
        }
        
        .project-card {
            background-color: white;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            height: 100%;
            display: flex;
            flex-direction: column;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .project-image {
            height: 200px;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .project-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .project-title {
            font-weight: 600;
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
            color: var(--dark-color);
        }
        
        .project-description {
            color: #64748b;
            margin-bottom: 1rem;
            flex-grow: 1;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .tech-badge {
            background-color: rgba(99, 102, 241, 0.1);
            color: var(--primary-color);
            padding: 0.25rem 0.75rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 500;
        }
        
        .project-link {
            color: var(--primary-color);
            font-weight: 500;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            transition: all 0.2s ease;
        }
        
        .project-link:hover {
            color: var(--secondary-color);
            transform: translateX(5px);
        }
        
        .project-link i {
            margin-left: 0.5rem;
        }
        
        /* Skills Section */
        .skills-section {
            padding: 80px 0;
            background-color: white;
        }
        
        .skill-card {
            background-color: var(--light-bg);
            border-radius: 12px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            height: 100%;
        }
        
        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .skill-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }
        
        .skill-title {
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        
        .skill-description {
            color: #64748b;
            font-size: 0.9rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 50px 0 30px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 50%;
            font-size: 1.25rem;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2.5rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg fixed-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="bi bi-code-slash"></i>DevPortfolio
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#home">Home</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="projectsDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                            Projects
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="projectsDropdown">
                            <li><a class="dropdown-item" href="https://github.com/your-username/paycheck-counter" target="_blank"><i class="bi bi-wallet2"></i>Paycheck Counter</a></li>
                            <li><a class="dropdown-item" href="https://github.com/your-username/project2" target="_blank"><i class="bi bi-calculator"></i>Calculator App</a></li>
                            <li><a class="dropdown-item" href="https://github.com/your-username/project3" target="_blank"><i class="bi bi-weather-sun"></i>Weather App</a></li>
                            <li><a class="dropdown-item" href="https://github.com/your-username/project4" target="_blank"><i class="bi bi-list-task"></i>Todo List</a></li>
                            <li><hr class="dropdown-divider"></li>
                            <li><a class="dropdown-item" href="https://github.com/your-username" target="_blank"><i class="bi bi-github"></i>View All on GitHub</a></li>
                        </ul>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#skills">Skills</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#contact">Contact</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-section">
        <div class="container hero-content">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <h1 class="hero-title">Hi, I'm a Developer</h1>
                    <p class="hero-subtitle">I build useful web applications and tools</p>
                    <div class="hero-buttons">
                        <a href="#projects" class="btn btn-hero btn-primary-custom">View Projects</a>
                        <a href="#contact" class="btn btn-hero btn-outline-custom">Get In Touch</a>
                    </div>
                </div>
                <div class="col-lg-6">
                    <div class="text-center">
                        <i class="bi bi-code-square" style="font-size: 15rem; opacity: 0.2;"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Projects -->
    <section id="projects" class="featured-projects">
        <div class="container">
            <div class="text-center mb-5">
                <h2 class="section-title">Featured Projects</h2>
                <p class="section-subtitle">Some of my recent work and experiments</p>
            </div>
            
            <div class="row">
                <div class="col-lg-4 col-md-6 mb-4">
                    <div class="project-card">
                        <div class="project-image">
                            <i class="bi bi-wallet2"></i>
                        </div>
                        <div class="project-content">
                            <h3 class="project-title">Paycheck Counter</h3>
                            <p class="project-description">Calculate how many more paychecks you'll receive before the 30th or end of the month.</p>
                            <div class="project-tech">
                                <span class="tech-badge">HTML</span>
                                <span class="tech-badge">CSS</span>
                                <span class="tech-badge">JavaScript</span>
                            </div>
                            <a href="https://github.com/your-username/paycheck-counter" target="_blank" class="project-link">
                                View on GitHub <i class="bi bi-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-4 col-md-6 mb-4">
                    <div class="project-card">
                        <div class="project-image">
                            <i class="bi bi-calculator"></i>
                        </div>
                        <div class="project-content">
                            <h3 class="project-title">Calculator App</h3>
                            <p class="project-description">A simple yet powerful calculator with advanced functions and beautiful UI.</p>
                            <div class="project-tech">
                                <span class="tech-badge">HTML</span>
                                <span class="tech-badge">CSS</span>
                                <span class="tech-badge">JavaScript</span>
                            </div>
                            <a href="https://github.com/your-username/calculator" target="_blank" class="project-link">
                                View on GitHub <i class="bi bi-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-4 col-md-6 mb-4">
                    <div class="project-card">
                        <div class="project-image">
                            <i class="bi bi-weather-sun"></i>
                        </div>
                        <div class="project-content">
                            <h3 class="project-title">Weather App</h3>
                            <p class="project-description">Get real-time weather information for any location with a clean interface.</p>
                            <div class="project-tech">
                                <span class="tech-badge">HTML</span>
                                <span class="tech-badge">CSS</span>
                                <span class="tech-badge">API</span>
                            </div>
                            <a href="https://github.com/your-username/weather-app" target="_blank" class="project-link">
                                View on GitHub <i class="bi bi-arrow-right"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills-section">
        <div class="container">
            <div class="text-center mb-5">
                <h2 class="section-title">Skills & Technologies</h2>
                <p class="section-subtitle">What I work with</p>
            </div>
            
            <div class="row">
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="skill-card">
                        <div class="skill-icon">
                            <i class="bi bi-filetype-html"></i>
                        </div>
                        <h4 class="skill-title">Frontend</h4>
                        <p class="skill-description">HTML, CSS, JavaScript, React, Bootstrap</p>
                    </div>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="skill-card">
                        <div class="skill-icon">
                            <i class="bi bi-server"></i>
                        </div>
                        <h4 class="skill-title">Backend</h4>
                        <p class="skill-description">Node.js, Express, Python, REST APIs</p>
                    </div>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="skill-card">
                        <div class="skill-icon">
                            <i class="bi bi-database"></i>
                        </div>
                        <h4 class="skill-title">Database</h4>
                        <p class="skill-description">MongoDB, MySQL, PostgreSQL, Firebase</p>
                    </div>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="skill-card">
                        <div class="skill-icon">
                            <i class="bi bi-git"></i>
                        </div>
                        <h4 class="skill-title">Tools</h4>
                        <p class="skill-description">Git, GitHub, VS Code, Chrome DevTools</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="text-center">
                <h3 class="mb-4">Let's Connect</h3>
                <div class="social-links">
                    <a href="https://github.com/your-username" target="_blank" class="social-link">
                        <i class="bi bi-github"></i>
                    </a>
                    <a href="https://linkedin.com/in/your-profile" target="_blank" class="social-link">
                        <i class="bi bi-linkedin"></i>
                    </a>
                    <a href="https://twitter.com/your-handle" target="_blank" class="social-link">
                        <i class="bi bi-twitter"></i>
                    </a>
                    <a href="mailto:your-email@example.com" class="social-link">
                        <i class="bi bi-envelope"></i>
                    </a>
                </div>
                <p class="mt-4 mb-0">&copy; 2023 Your Name. Built with <i class="bi bi-heart-fill text-danger"></i> and lots of <i class="bi bi-cup-hot-fill"></i></p>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    window.scrollTo({
                        top: target.offsetTop - 70,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Add active class to nav links on scroll
        window.addEventListener('scroll', function() {
            let current = '';
            const sections = document.querySelectorAll('section');
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 100) {
                    current = section.getAttribute('id');
                }
            });
            
            document.querySelectorAll('.navbar-nav .nav-link').forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').slice(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
