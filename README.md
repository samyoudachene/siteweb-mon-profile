<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Samy Oudachene - Portfolio</title>
    <style>
        /* Variables CSS */
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --text-color: #333;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        /* Reset et styles de base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--light-color);
        }

        a {
            text-decoration: none;
            color: var(--secondary-color);
            transition: color 0.3s ease;
        }

        a:hover {
            color: var(--accent-color);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 80px 0;
        }

        h1, h2, h3 {
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        p {
            margin-bottom: 15px;
        }

        /* Header */
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: white;
            font-weight: 500;
        }

        .hamburger {
            display: none;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            text-align: center;
            padding: 150px 0 100px;
            margin-top: 60px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            color: white;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }

        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: white;
            padding: 12px 30px;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }

        .btn:hover {
            background-color: #c0392b;
            color: white;
        }

        /* About Section */
        .about {
            background-color: white;
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-text {
            flex: 1;
        }

        .about-image {
            flex: 1;
            text-align: center;
        }

        .profile-img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--secondary-color);
            box-shadow: var(--shadow);
        }

        /* Skills Section */
        .skills {
            background-color: var(--light-color);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-category {
            background-color: white;
            padding: 30px;
            border-radius: 5px;
            box-shadow: var(--shadow);
        }

        .skill-category h3 {
            color: var(--secondary-color);
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 10px;
            margin-bottom: 20px;
        }

        .skill-list {
            list-style: none;
        }

        .skill-list li {
            margin-bottom: 10px;
            padding-left: 20px;
            position: relative;
        }

        .skill-list li:before {
            content: "▸";
            position: absolute;
            left: 0;
            color: var(--secondary-color);
        }

        /* Contact Section */
        .contact {
            background-color: white;
        }

        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 40px;
        }

        .contact-item {
            flex: 1;
            min-width: 250px;
            background-color: var(--light-color);
            padding: 20px;
            border-radius: 5px;
            text-align: center;
            box-shadow: var(--shadow);
        }

        .contact-item i {
            font-size: 2rem;
            color: var(--secondary-color);
            margin-bottom: 15px;
        }

        /* Footer */
        footer {
            background-color: var(--primary-color);
            color: white;
            text-align: center;
            padding: 30px 0;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background-color: var(--primary-color);
                padding: 20px;
                box-shadow: var(--shadow);
            }

            .nav-links.active {
                display: flex;
            }

            .nav-links li {
                margin: 10px 0;
            }

            .hamburger {
                display: block;
            }

            .about-content {
                flex-direction: column;
            }

            .hero h1 {
                font-size: 2.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Samy Oudachene</div>
                <ul class="nav-links">
                    <li><a href="#accueil">Accueil</a></li>
                    <li><a href="#apropos">À propos</a></li>
                    <li><a href="#competences">Compétences</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="hamburger">☰</div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="accueil" class="hero">
        <div class="container">
            <h1>Samy Oudachene</h1>
            <p>Développeur passionné par la création de solutions innovantes</p>
            <a href="#contact" class="btn">Me contacter</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="apropos" class="about">
        <div class="container">
            <h2>À propos de moi</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Je m'appelle Samy Oudachene, j'ai 20 ans et je vis en Algérie. Je suis étudiant en informatique, spécialisé en systèmes informatiques à l'Université Mouloud Mammeri de Tizi Ouzou.</p>
                    <p>Passionné par le développement et les nouvelles technologies, je cherche constamment à améliorer mes compétences et à relever de nouveaux défis dans le domaine de l'informatique.</p>
                    <p>En dehors de mes études, je m'intéresse particulièrement à la musculation, au sport en général, à la gym et à l'intelligence artificielle.</p>
                </div>
                <div class="about-image">
                    <!-- Image de profil fictive -->
                    <div class="profile-img" style="background-color: #3498db; display: flex; align-items: center; justify-content: center; color: white; font-size: 1.5rem;">
                        SO
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="competences" class="skills">
        <div class="container">
            <h2>Mes compétences</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Langages de programmation</h3>
                    <ul class="skill-list">
                        <li>C/C++</li>
                        <li>Python</li>
                        <li>JavaScript</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Développement Web</h3>
                    <ul class="skill-list">
                        <li>HTML</li>
                        <li>CSS</li>
                        <li>JavaScript</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Systèmes d'exploitation</h3>
                    <ul class="skill-list">
                        <li>Linux</li>
                        <li>Windows</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Langues</h3>
                    <ul class="skill-list">
                        <li>Tamazight</li>
                        <li>Arabe</li>
                        <li>Français</li>
                        <li>Anglais</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Centres d'intérêt</h3>
                    <ul class="skill-list">
                        <li>Musculation</li>
                        <li>Sport</li>
                        <li>Gym</li>
                        <li>Intelligence Artificielle</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2>Contact</h2>
            <div class="contact-info">
                <div class="contact-item">
                    <i>✉️</i>
                    <h3>Email</h3>
                    <p><a href="mailto:samyoudachene@gmail.com">samyoudachene@gmail.com</a></p>
                </div>
                <div class="contact-item">
                    <i>📱</i>
                    <h3>Téléphone</h3>
                    <p><a href="tel:0557413218">0557413218</a></p>
                </div>
                <div class="contact-item">
                    <i>🔗</i>
                    <h3>LinkedIn</h3>
                    <p><a href="https://linkedin.com/in/samy-oudachene" target="_blank">Samy Oudachene</a></p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2023 Samy Oudachene. Tous droits réservés.</p>
        </div>
    </footer>

    <script>
        // Menu hamburger pour mobile
        document.querySelector('.hamburger').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });

        // Fermer le menu mobile en cliquant sur un lien
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                document.querySelector('.nav-links').classList.remove('active');
            });
        });

        // Animation simple au défilement
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.backgroundColor = 'rgba(44, 62, 80, 0.95)';
            } else {
                header.style.backgroundColor = 'var(--primary-color)';
            }
        });
    </script>
</body>
</html>
