<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Signori Bistró | Café de Especialidad & Restaurante</title>
    
    <style>
        /* Paleta de Colores Inspirada en Café */
        :root {
            --cafe-oscuro: #3E2723;
            --cafe-medio: #5D4037;
            --cafe-claro: #8D6E63;
            --crema: #EFEBE9;
            --beige: #D7CCC8;
            --blanco: #FFFFFF;
            --dorado: #D4AF37;
        }

        /* Configuración Global */
        * {
            box-sizing: border-box; /* [cite: 152] */
            margin: 0;
            padding: 0;
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif; /* [cite: 190] */
        }

        body {
            background-color: var(--crema);
            color: var(--cafe-oscuro);
            line-height: 1.6;
        }

        /* Encabezado y Navegación */
        header {
            background-color: var(--cafe-oscuro);
            color: var(--blanco);
            padding: 1rem 0;
            position: sticky; /* Barra fija superior */
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--dorado);
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        nav a {
            color: var(--blanco);
            text-decoration: none; /* [cite: 195] */
            margin-left: 20px;
            font-size: 0.9rem;
            transition: color 0.3s;
            text-transform: uppercase;
        }

        nav a:hover {
            color: var(--dorado);
        }

        /* Sección Hero (Bienvenida) */
        .hero {
            background-image: linear-gradient(rgba(62, 39, 35, 0.7), rgba(62, 39, 35, 0.7)), url('https://images.unsplash.com/photo-1509042239860-f550ce710b93?ixlib=rb-1.2.1&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--blanco);
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.5rem;
            max-width: 700px;
            margin: 0 auto 2rem auto;
            font-weight: 300;
        }

        .btn {
            background-color: var(--dorado);
            color: var(--cafe-oscuro);
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: transform 0.3s, background-color 0.3s;
            display: inline-block;
        }

        .btn:hover {
            background-color: #bfa15f;
            transform: scale(1.05);
        }

        /* Estructura Principal */
        main {
            max-width: 1200px;
            margin: 40px auto;
            padding: 0 20px;
        }

        /* Secciones Generales */
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--cafe-oscuro);
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background-color: var(--dorado);
            margin: 10px auto 0;
        }

        /* Quiénes Somos (Diseño a dos columnas) */
        .about-row {
            display: flex; /* [cite: 155] */
            flex-wrap: wrap; /* [cite: 156] */
            align-items: center;
            gap: 40px;
            margin-bottom: 80px;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-image {
            flex: 1;
            min-width: 300px;
        }

        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 10px 10px 0px var(--beige);
        }

        /* Grid de Servicios */
        .services-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .service-card {
            background-color: var(--blanco);
            flex: 0 1 calc(25% - 20px); /* 4 columnas */
            min-width: 250px;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
            display: flex;
            flex-direction: column;
        }

        .service-card:hover {
            transform: translateY(-10px);
        }

        .service-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .service-content {
            padding: 20px;
            text-align: center;
            flex-grow: 1;
        }

        .service-content h3 {
            color: var(--cafe-medio);
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        .service-content p {
            font-size: 0.9rem;
            color: #666;
        }

        /* Banner de Cita/Frase */
        .quote-banner {
            background-color: var(--cafe-medio);
            color: var(--blanco);
            text-align: center;
            padding: 60px 20px;
            margin: 60px 0;
            font-style: italic;
            font-size: 1.5rem;
        }

        /* Pie de Página */
        footer {
            background-color: var(--cafe-oscuro);
            color: var(--beige);
            padding: 40px 0 20px;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--cafe-medio);
        }

        .footer-column {
            margin: 10px;
            min-width: 200px;
        }

        .footer-column h4 {
            color: var(--dorado);
            margin-bottom: 15px;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 8px;
        }

        .footer-column a {
            color: var(--beige);
            text-decoration: none;
        }

        .copyright {
            padding-top: 20px;
            font-size: 0.8rem;
            opacity: 0.7;
        }

        /* Media Queries para móviles */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .header-container { flex-direction: column; gap: 10px; }
            .service-card { flex: 0 1 100%; }
        }
    </style>
</head>

<body>

    <header>
        <div class="header-container">
            <div class="logo">Signori Bistró</div>
            <nav>
                <a href="#inicio">Inicio</a>
                <a href="#nosotros">Historia</a>
                <a href="#servicios">Menú</a>
                <a href="#contacto">Visítanos</a>
            </nav>
        </div>
    </header>

    <main>
        
        <section id="inicio" class="hero">
            <div>
                <h1>El Arte del Buen Café</h1>
                <p>Descubre un espacio donde los granos de especialidad y la gastronomía artesanal se encuentran.</p>
                <a href="#servicios" class="btn">Ver Menú</a>
            </div>
        </section>

        <section id="nosotros" style="padding-top: 60px;">
            <h2 class="section-title">Nuestra Esencia</h2>
            <div class="about-row">
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1554118811-1e0d58224f24?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Interior Signori Bistró">
                </div>
                <div class="about-text">
                    <h3>Más que una cafetería</h3>
                    <br>
                    <p>En <strong>Signori Bistró</strong>, somos apasionados por los detalles. Nacimos con la misión de ofrecer un refugio para los amantes del buen gusto. No solo servimos café; curamos experiencias.</p>
                    <br>
                    <p>Nuestro equipo de baristas expertos y chefs trabajan en armonía para traerte lo mejor de dos mundos: la intensidad de un café de altura y el confort de un almuerzo casero con toque gourmet.</p>
                </div>
            </div>
        </section>

        <div class="quote-banner">
            "La vida comienza después de una taza de café."
        </div>

        <section id="servicios">
            <h2 class="section-title">Nuestros Servicios</h2>
            
            <div class="services-grid">
                
                <div class="service-card">
                    <img src="https://images.unsplash.com/photo-1546069901-ba9599a7e63c?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Almuerzo Ejecutivo">
                    <div class="service-content">
                        <h3>Almuerzos Ejecutivos</h3>
                        <p>Menús diarios balanceados preparados con ingredientes frescos. Desde pastas artesanales hasta cortes de carne seleccionados.</p>
                    </div>
                </div>

                <div class="service-card">
                    <img src="https://images.unsplash.com/photo-1509440159596-0249088772ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Refacciones">
                    <div class="service-content">
                        <h3>Refacciones & Repostería</h3>
                        <p>El acompañamiento perfecto. Disfruta de nuestros croissants recién horneados, tartas de frutas y sándwiches gourmet.</p>
                    </div>
                </div>

                <div class="service-card">
                    <img src="https://images.unsplash.com/photo-1497935586351-b67a49e012bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Café de Especialidad">
                    <div class="service-content">
                        <h3>Café de Especialidad</h3>
                        <p>Trabajamos con microlotes de fincas locales. Ofrecemos métodos de extracción como V60, Chemex y Aeropress.</p>
                    </div>
                </div>

                <div class="service-card">
                    <img src="https://images.unsplash.com/photo-1514362545857-3bc16c4c7d1b?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Bebidas">
                    <div class="service-content">
                        <h3>Bebidas de Autor</h3>
                        <p>Refresca tu día con nuestras famosas sangrías, licuados naturales y bebidas frías diseñadas por nuestros mixólogos.</p>
                    </div>
                </div>

            </div>
        </section>

    </main>

    <footer id="contacto">
        <div class="footer-content">
            <div class="footer-column">
                <h4>Signori Bistró</h4>
                <p>Visitanos en: https://maps.app.goo.gl/DcTzPc7GkCqaKCRo8?g_st=aw</p>
            </div>
            <div class="footer-column">
                <h4>Horarios</h4>
                <ul>
                    <li>Lunes - Viernes: 8:00 AM - 4:00 PM</li>
                    <li>Sábado y Domingo: Cerrado</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>Contacto</h4>
                <ul>
                    <li><a href="#">Tel: +502 30795536</a></li>
                    <li><a href="#">Email: info@signoribistro.com</a></li>
                    <li><a href="#">Instagram: @signoribistro</a></li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2024 Signori Bistró. Todos los derechos reservados.</p>
        </div>
    </footer>

</body>
</html>
