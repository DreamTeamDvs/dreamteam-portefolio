<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - DreamTeam Dev</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            line-height: 1.6;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 20px 0;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #444;
        }
        nav a {
            color: #fff;
            padding: 14px 20px;
            text-decoration: none;
            text-align: center;
        }
        nav a:hover {
            background-color: #555;
        }
        .container {
            padding: 20px;
        }
        .section {
            margin-bottom: 40px;
        }
        .project {
            background-color: #fff;
            margin: 10px 0;
            padding: 15px;
            border-radius: 5px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
        }
        .project small {
            display: block;
            margin-top: 10px;
            font-size: 0.9em;
            color: #666;
        }
        .achievement {
            background-color: #f9f9f9;
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 15px;
            margin: 10px 0;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            display: flex;
            gap: 20px;
            align-items: center;
        }
        .achievement img {
            width: 100px;
            height: 100px;
            object-fit: cover;
            border-radius: 5px;
            cursor: pointer;
        }
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }
        .modal img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 5px;
        }
        .modal .close {
            position: absolute;
            top: 20px;
            right: 20px;
            color: #fff;
            font-size: 2em;
            cursor: pointer;
        }
        footer {
            text-align: center;
            padding: 20px 0;
            background-color: #333;
            color: #fff;
        }
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .skill {
            background-color: #eee;
            border: 1px solid #ccc;
            border-radius: 5px;
            padding: 10px;
            text-align: center;
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const modals = document.querySelectorAll('.modal');
            const images = document.querySelectorAll('.achievement img');
            const closeButtons = document.querySelectorAll('.modal .close');

            images.forEach((img, index) => {
                img.addEventListener('click', () => {
                    modals[index].style.display = 'flex';
                });
            });

            closeButtons.forEach((button, index) => {
                button.addEventListener('click', () => {
                    modals[index].style.display = 'none';
                });
            });

            modals.forEach(modal => {
                modal.addEventListener('click', (e) => {
                    if (e.target === modal) {
                        modal.style.display = 'none';
                    }
                });
            });
        });
    </script>
</head>
<body>

<header>
    <h1>DreamTeam dev</h1>
    <p>Développeur Full Stack passionné par le développement d'applications web et mobiles</p>
</header>

<nav>
    <a href="#about">À Propos</a>
    <a href="#projects">Projets</a>
    <a href="#skills">Compétences</a>
    <a href="#contact">Contact</a>
</nav>

<div class="container">
    <section id="about" class="section">
        <h2>À Propos</h2>
        <p>Développeur Full Stack avec plus de 3 ans d'expérience dans la conception, le développement et la maintenance d'applications web et mobiles. Passionné par la résolution de problèmes complexes et l'optimisation des performances.</p>
    </section>

    <section id="projects" class="section">
        <h2>Projets</h2>
        <div class="project">
            <h3>Système de Gestion de Bourses</h3>
            <p>Conception d'une application pour la gestion des bourses d'études, incluant des fonctionnalités d'inscription, de gestion des demandes et d'intégration bancaire.</p>
            <small>Projet réalisé chez CAPDATA Software</small>
        </div>
        <div class="project">
            <h3>Tableau de Bord Comptable</h3>
            <p>Développement d'un tableau de bord React pour la gestion financière, avec calcul automatisé des budgets et suivi des échéances.</p>
            <small>Projet réalisé chez SCRIPTURA</small>
        </div>
        <div class="project">
            <h3>Site Web d'Entreprise</h3>
            <p>Création et maintenance du site web de Scriptura, intégrant des outils SEO, des systèmes de suivi de trafic et un chat interactif.</p>
            <small>Projet réalisé chez SCRIPTURA</small>
        </div>
    </section>

    <section id="achievements" class="section">
        <h2>Réalisations</h2>
		<div class="achievement">
			<img src="images/food-court.png" alt="Pipeline d'Extraction de Données">
			<div>
				<h3>Application mobile pour fast-food</h3>
				<p>Implémentation d'une Application mobile avec géolocalisation.</p>
			</div>
		</div>
		<div class="modal">
            <span class="close">&times;</span>
            <img src="images/food-court.png" alt="Pipeline d'Extraction de Données">
        </div>
		<div class="achievement">
			<img src="images/ticket.png" alt="Pipeline d'Extraction de Données">
			<div>
				<h3>Plateforme pour réservation de Parking</h3>
				<p>Page d'accueil pour la réservation.</p>
			</div>
		</div>
		<div class="modal">
            <span class="close">&times;</span>
            <img src="images/ticket.png" alt="Pipeline d'Extraction de Données">
        </div>
		<div class="achievement">
			<img src="images/facture-ticket.png" alt="Pipeline d'Extraction de Données">
			<div>
				<h3>Plateforme pour réservation de Parking</h3>
				<p>Champ de saisie pour réserver une place avec payement.</p>
			</div>
		</div>
		<div class="modal">
            <span class="close">&times;</span>
            <img src="images/facture-ticket.png" alt="Pipeline d'Extraction de Données">
        </div>
    </section>
	
	
	
    <section id="skills" class="section">
        <h2>Compétences</h2>
        <div class="skills">
            <div class="skill">Java</div>
            <div class="skill">C#/.NET</div>
            <div class="skill">JavaScript (React, Angular, Node.js)</div>
            <div class="skill">PHP (CodeIgniter, Symfony)</div>
            <div class="skill">Python</div>
            <div class="skill">HTML5 & CSS3</div>
            <div class="skill">Bases de Données (PostgreSQL, MySQL, MongoDB)</div>
            <div class="skill">Outils (Git, Visual Studio Code, MySQL Workbench)</div>
        </div>
    </section>

    <section id="contact" class="section">
        <h2>Contact</h2>
        <p>Email : <a href="mailto:dreamteamdvs@gmail.com">dreamteamdvs@gmail.com</a></p>
        <p>Téléphone : <a href="tel:+261347452459">+261 34 74 524 59</a></p>
        <p>Adresse : Antananarivo Madagascar</p>
    </section>
</div>

<footer>
    &copy; 2024 DreamTeam Dev. Tous droits réservés.
</footer>

</body>
</html>