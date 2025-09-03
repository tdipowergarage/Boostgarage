# <!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BoostGarage Performance</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Roboto', sans-serif; }
        body { background-color: #121212; color: #f5f5f5; scroll-behavior: smooth; }
        a { color: inherit; text-decoration: none; }

        header { background-color: #1a1a1a; padding: 20px 30px; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 0; z-index: 1000; }
        header h1 { color: #e10600; }
        nav a { margin-left: 20px; font-weight: bold; transition: color 0.3s; }
        nav a:hover { color: #ff4500; }

        /* Hero */
        .hero { background: url('hero.jpg') center/cover no-repeat; height: 90vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; overflow: hidden; }
        .hero h2 { font-size: 3.5rem; color: #ff0000; text-shadow: 2px 2px #000; animation: slideInDown 1s ease-out forwards; opacity: 0; }
        .hero p { font-size: 1.3rem; margin-top: 20px; text-shadow: 1px 1px #000; animation: fadeIn 2s ease-out forwards; opacity: 0; }

        @keyframes slideInDown {
            0% { transform: translateY(-100px); opacity: 0; }
            100% { transform: translateY(0); opacity: 1; }
        }
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }

        /* Leistungen */
        .services { padding: 60px 30px; display: flex; flex-wrap: wrap; justify-content: space-around; gap: 30px; background-color: #1e1e1e; }
        .service { background-color: #2a2a2a; padding: 25px; border-radius: 10px; flex: 1 1 250px; transition: transform 0.3s, box-shadow 0.3s; opacity: 0; transform: translateY(50px); }
        .service:hover { transform: scale(1.05); box-shadow: 0 0 20px #ff0000; }
        .service.animate { opacity: 1; transform: translateY(0); transition: all 0.6s ease-out; }
        .service h3 { color: #e10600; margin-bottom: 12px; }
        .service p { color: #ccc; }

        /* Galerie */
        .gallery { padding: 60px 30px; display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; }
        .gallery img { width: 100%; border-radius: 10px; transition: transform 0.3s, box-shadow 0.3s; opacity: 0; transform: scale(0.8); }
        .gallery img:hover { transform: scale(1.1); box-shadow: 0 0 15px #ff0000; }
        .gallery img.animate { opacity: 1; transform: scale(1); transition: all 0.5s ease-out; }

        /* Über uns */
        .about { padding: 60px 30px; text-align: center; }
        .about h2 { color: #e10600; margin-bottom: 20px; }
        .about p { max-width: 700px; margin: 0 auto; color: #ccc; }

        /* Kontakt */
        .contact { padding: 60px 30px; background-color: #1e1e1e; }
        .contact h2 { color: #e10600; margin-bottom: 20px; text-align: center; }
        .contact form { max-width: 600px; margin: 0 auto; display: flex; flex-direction: column; gap: 15px; }
        .contact input, .contact textarea { padding: 12px; border-radius: 5px; border: none; }
        .contact button { padding: 12px; background-color: #e10600; border: none; color: #fff; font-weight: bold; cursor: pointer; transition: background 0.3s; }
        .contact button:hover { background-color: #ff4500; }

        footer { background-color: #111; text-align: center; padding: 20px; margin-top: 40px; color: #777; }

    </style>
</head>
<body>

<header>
    <h1>BoostGarage</h1>
    <nav>
        <a href="#services">Leistungen</a>
        <a href="#gallery">Galerie</a>
        <a href="#about">Über uns</a>
        <a href="#contact">Kontakt</a>
    </nav>
</header>

<section class="hero">
    <h2>Power & Performance</h2>
    <p>Chiptuning | DPF & AdBlue | AGR Off | Motorsport</p>
</section>

<section id="services" class="services">
    <div class="service">
        <h3>Chiptuning</h3>
        <p>Optimale Leistung, perfektes Drehmoment, Motorsport-Feeling.</p>
    </div>
    <div class="service">
        <h3>DPF & AdBlue</h3>
        <p>Saubere, leistungsoptimierte Lösungen für jeden Anspruch.</p>
    </div>
    <div class="service">
        <h3>AGR Off</h3>
        <p>Für Motorsportzwecke – maximale Performance ohne Kompromisse.</p>
    </div>
    <div class="service">
        <h3>Motorperformance</h3>
        <p>Komplette Leistungssteigerung, Turbo-Upgrades und Tuning-Optimierung.</p>
    </div>
</section>

<section id="gallery" class="gallery">
    <img src="project1.jpg" alt="Projekt 1">
    <img src="project2.jpg" alt="Projekt 2">
    <img src="project3.jpg" alt="Projekt 3">
    <img src="project4.jpg" alt="Projekt 4">
</section>

<section id="about" class="about">
    <h2>Über BoostGarage</h2>
    <p>BoostGarage ist dein Partner für Motorsport-Performance und Tuning. Mit Leidenschaft für Motoren, Drehmoment und Speed bringen wir jedes Fahrzeug auf das nächste Level.</p>
</section>

<section id="contact" class="contact">
    <h2>Kontakt</h2>
    <form>
        <input type="text" placeholder="Name" required>
        <input type="email" placeholder="E-Mail" required>
        <input type="text" placeholder="Betreff" required>
        <textarea rows="6" placeholder="Nachricht" required></textarea>
        <button type="submit">Senden</button>
    </form>
</section>

<footer>
    &copy; 2025 BoostGarage. Alle Rechte vorbehalten.
</footer>

<script>
    // Animation beim Scrollen
    const services = document.querySelectorAll('.service');
    const galleryImgs = document.querySelectorAll('.gallery img');

    const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
            if(entry.isIntersecting){
                entry.target.classList.add('animate');
            }
        });
    }, { threshold: 0.3 });

    services.forEach(service => observer.observe(service));
    galleryImgs.forEach(img => observer.observe(img));
</script>

</body>
</html>
