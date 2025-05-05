<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FAYE Building Contractor - Architecte Ibrahima FAYE</title>
    <style>
        :root {
            --primary-color: #0e5397;
            --secondary-color: #7c1004;
            --light-color: beige;
            --dark-color: rgb(3, 3, 61);
            --accent-color: #3498db;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark-color);
            background-color: #f9f9f9;
        }
        
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {

            height: 150px;
            margin-right: 15px;
        }
        
        .logo-text h1 {
            font-size: 1.5rem;
            font-weight: 700;
        }
        
        .logo-text p {
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 2rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--accent-color);
        }
        
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1487958449943-2429e8be8625?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            padding-top: 80px;
        }
        
        .hero-content h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero-content p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
            margin: 0 10px;
        }
        
        .btn:hover {
            background-color: #c0392b;
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--dark-color);
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--secondary-color);
        }
        
        .services {
            background-color: white;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background-color: var(--light-color);
            padding: 2rem;
            border-radius: 5px;
            text-align: center;
            transition: transform 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
        }
        
        .service-card i {
            font-size: 3rem;
            color: var(--secondary-color);
            margin-bottom: 1.5rem;
        }
        
        .service-card h3 {
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .projects {
            background-color: var(--light-color);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            position: relative;
            overflow: hidden;
            border-radius: 5px;
            height: 250px;
        }
        
        .project-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .project-card:hover img {
            transform: scale(1.1);
        }
        
        .project-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.8), transparent);
            color: white;
            padding: 1rem;
            transform: translateY(100%);
            transition: transform 0.3s;
        }
        
        .project-card:hover .project-overlay {
            transform: translateY(0);
        }
        
        .contact {
            background-color: white;
        }
        
        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }
        
        .contact-info {
            margin-bottom: 2rem;
        }
        
        .contact-info h3 {
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .contact-info p {
            margin-bottom: 0.5rem;
        }
        
        .contact-info a {
            color: var(--accent-color);
            text-decoration: none;
        }
        
        .contact-info a:hover {
            text-decoration: underline;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 1rem;
            margin-bottom: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        .contact-form textarea {
            height: 150px;
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            text-align: center;
            padding: 2rem 0;
        }
        
        .footer-content p {
            margin-bottom: 1rem;
        }
        
        .social-links a {
            color: white;
            margin: 0 10px;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent-color);
        }
        
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25D366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            text-align: center;
            font-size: 30px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .whatsapp-float:hover {
            background-color: #128C7E;
            transform: scale(1.1);
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
            }
            
            nav ul li {
                margin: 0 0.5rem;
            }
            
            .hero-content h2 {
                font-size: 2rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">
                <img scr="c:\Users\DELL\Desktop\Dossier Ibrahima FAYE\image.png" alt="">
                <img src="image.png" alt="FAYE Building Contractor Logo">
                <div class="logo-text">
                    <h1>FAYE Building Contractor</h1>
                    <p>Architecture & Construction</p>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Accueil</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#projects">Projets</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="container hero-content">
            <div>
                <h2>Conceptions Architecturales Exceptionnelles</h2>
                <p>Ibrahima FAYE, architecte principal avec plus de 20 ans d'expérience dans la création de bâtiments innovants et durables qui allient esthétique et fonctionnalité.</p>
                <a href="#contact" class="btn">Demander un devis</a>
                <a href="#projects" class="btn btn-outline">Voir nos projets</a>
            </div>
        </div>
    </section>

    <section id="services" class="services">
        <div class="container">
            <div class="section-title">
                <h2>Nos Services</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <i class="fas fa-drafting-compass"></i>
                    <h3>Conception Architecturale</h3>
                    <p>Création de plans sur mesure répondant à vos besoins spécifiques tout en respectant les normes de construction.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-home"></i>
                    <h3>Construction Résidentielle</h3>
                    <p>Réalisation de maisons individuelles, villas et résidences de qualité avec des matériaux haut de gamme.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-building"></i>
                    <h3>Bâtiments Commerciaux</h3>
                    <p>Conception et construction d'espaces commerciaux fonctionnels et attractifs pour votre entreprise.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-sync-alt"></i>
                    <h3>Rénovation</h3>
                    <p>Transformation et modernisation de bâtiments existants pour améliorer leur valeur et leur fonctionnalité.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-lightbulb"></i>
                    <h3>Conseil en Design</h3>
                    <p>Expertise en aménagement intérieur et sélection de matériaux pour un résultat harmonieux et durable.</p>
                </div>
                <div class="service-card">
                    <i class="fas fa-check-circle"></i>
                    <h3>Gestion de Projet</h3>
                    <p>Supervision complète du projet du concept à la réalisation finale, garantissant qualité et respect des délais.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" class="projects">
        <div class="container">
            <div class="section-title">
                <h2>Nos Réalisations</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Projet Résidentiel">
                    <div class="project-overlay">
                        <h3>Résidence Les Palmiers</h3>
                        <p>Dakar, Sénégal</p>
                    </div>
                </div>
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1493809842364-78817add7ffb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Projet Commercial">
                    <div class="project-overlay">
                        <h3>Centre Commercial Zenith</h3>
                        <p>Bamako, Mali</p>
                    </div>
                </div>
                <div class="project-card">
                    <img src="https://images.unsplash.com/photo-1513694203232-719a280e022f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Projet Rénovation">
                    <div class="project-overlay">
                        <h3>Rénovation Hôtel Savana</h3>
                        <p>Abidjan, Côte d'Ivoire</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contactez-nous</h2>
            </div>
            <div class="contact-content">
                <div>
                    <div class="contact-info">
                        <h3>Coordonnées</h3>
                        <p><i class="fas fa-user"></i> Ibrahima FAYE</p>
                        <p><i class="fas fa-briefcase"></i> Architecte Principal</p>
                        <p><i class="fas fa-phone"></i> +220 777 6563</p>
                        <p><i class="fas fa-phone"></i> +220 990 6563</p>
                        <p><i class="fas fa-phone"></i> +220 390 6563</p>
                        <p><i class="fas fa-phone"></i> +221 77 195 54 60</p>
                        <p><i class="fas fa-envelope"></i> <a href="mailto:faye1965ibrahima@gmail.com">faye1965ibrahima@gmail.com</a></p>
                    </div>
                    <div class="contact-info">
                        <h3>Heures d'ouverture</h3>
                        <p>Lundi - Jeudi: 11h00 - 18h00</p>
                        <p>Samedi - Dimanche: 13h00 - 17h00</p>
                        <p>Vendredi: Fermé</p>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <input type="text" placeholder="Votre nom" required>
                        <input type="email" placeholder="Votre email" required>
                        <input type="tel" placeholder="Votre téléphone">
                        <textarea placeholder="Votre message" required></textarea>
                        <button type="submit" class="btn">Envoyer le message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container footer-content">
            <div class="logo">
                <img src="image.png" alt="FAYE Building Contractor Logo" style="height: 40px;">
                <div class="logo-text">
                    <h1 style="font-size: 1.2rem;">FAYE Building Contractor</h1>
                </div>
            </div>
            <p>© 2025 FAYE Building Contractor. Tous droits réservés.</p>
            </div>
    </footer>

    <!-- Bouton WhatsApp flottant -->
    <a href="https://wa.me/2207776563" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Smooth scrolling pour les liens d'ancrage
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Animation au défilement
        window.addEventListener('scroll', reveal);
        
        function reveal() {
            const reveals = document.querySelectorAll('.service-card, .project-card');
            
            for(let i = 0; i < reveals.length; i++) {
                const windowHeight = window.innerHeight;
                const revealTop = reveals[i].getBoundingClientRect().top;
                const revealPoint = 150;
                
                if(revealTop < windowHeight - revealPoint) {
                    reveals[i].classList.add('active');
                }
            }
        }
        
        // Appeler la fonction une fois au chargement
        reveal();
    </script>
</body>
</html>
