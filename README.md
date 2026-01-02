import os

def crear_sitio_signori_bistro():
    # PASO 1 y 2: Planificación y Contenido [cite: 17, 80]
    # Definimos las URLs de las imágenes para cada servicio (Café, Almuerzo, Bebidas, etc.)
    img_hero = "https://images.unsplash.com/photo-1509042239860-f550ce710b93?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
    img_almuerzo = "https://images.unsplash.com/photo-1546069901-ba9599a7e63c?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
    img_refaccion = "https://images.unsplash.com/photo-1509440159596-0249088772ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
    img_cafe = "https://images.unsplash.com/photo-1497935586351-b67a49e012bf?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
    img_bebida = "https://images.unsplash.com/photo-1514362545857-3bc16c4c7d1b?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"

    # PASO 3, 4 y 5: Estructura HTML y Elementos [cite: 33, 48, 80]
    html_content = f"""<!DOCTYPE html>
<html>
<head>
    <title>Signori Bistró - Café & Restaurante</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Signori Bistró</h1>
        <p>Donde el café es un arte y la comida una experiencia</p>
        <nav>
            <a href="#inicio">Inicio</a>
            <a href="#nosotros">Quiénes Somos</a>
            <a href="#servicios">Menú y Servicios</a>
            <a href="#contacto">Contacto</a>
        </nav>
    </header>

    <main>
        <div id="inicio" class="hero-section">
            <h2>Bienvenidos</h2>
            <p>Disfruta de un ambiente acogedor con el mejor aroma de la ciudad.</p>
            <img src="{img_hero}" alt="Interior de cafetería acogedora" class="main-img">
        </div>

        <div id="nosotros" class="section-container">
            <h2>Quiénes Somos</h2>
            <p>En Signori Bistró nos dedicamos a crear experiencias gastronómicas únicas. 
            Desde nuestro café de especialidad hasta nuestros almuerzos ejecutivos, 
            cada detalle está pensado para tu deleite.</p>
        </div>

        <div id="servicios" class="section-container">
            <h2>Nuestros Servicios</h2>
            <div class="row">
                <div class="card">
                    <img src="{img_almuerzo}" alt="Almuerzo saludable">
                    <h3>Almuerzos</h3>
                    <p>Platos balanceados y deliciosos para tu mediodía.</p>
                </div>
                
                <div class="card">
                    <img src="{img_refaccion}" alt="Postres y refacciones">
                    <h3>Refacciones</h3>
                    <p>Acompaña tu tarde con repostería fresca.</p>
                </div>

                <div class="card">
                    <img src="{img_cafe}" alt="Café de especialidad">
                    <h3>Café de Especialidad</h3>
                    <p>Granos selectos y métodos de extracción artesanales.</p>
                </div>

                <div class="card">
                    <img src="{img_bebida}" alt="Bebidas preparadas y sangrías">
                    <h3>Bebidas Preparadas</h3>
                    <p>Sangrías, cócteles y bebidas refrescantes.</p>
                </div>
            </div>
        </div>
    </main>

    <footer>
        <p>© 2024 Signori Bistró. Síguenos en nuestras redes.</p>
    </footer>
</body>
</html>
    """

    # PASO 6 y 7: Diseño CSS y Personalización [cite: 131, 139, 179]
    # Se usan colores café/beige como se solicitó 
    css_content = """
/* Configuración básica */
* { box-sizing: border-box; font-family: 'Verdana', sans-serif; }

body {
    margin: 0;
    background-color: #FDF5E6; /* Color OldLace (Beige claro) */
    color: #4E342E; /* Café oscuro para texto */
}

/* Encabezado */
header {
    background-color: #3E2723; /* Café muy oscuro */
    color: #FFF;
    padding: 20px;
    text-align: center;
}

/* Navegación */
nav {
    background-color: #D7CCC8; /* Café suave */
    padding: 10px;
    margin-top: 10px;
}

nav a {
    color: #3E2723;
    text-decoration: none;
    margin: 0 15px;
    font-weight: bold;
    font-size: 1.1em;
}

nav a:hover { color: #8D6E63; }

/* Contenedores */
.section-container {
    padding: 40px 20px;
    text-align: center;
}

.hero-section {
    text-align: center;
    padding: 20px;
    background-color: #EFEBE9;
}

.main-img {
    width: 80%;
    max-width: 600px;
    border-radius: 10px;
    margin-top: 10px;
}

/* Flexbox para los servicios (Columnas)  */
.row {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
}

/* Tarjetas de servicios con imágenes */
.card {
    background-color: #FFF;
    border: 1px solid #A1887F;
    border-radius: 8px;
    width: 250px;
    padding: 15px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.card img {
    width: 100%;
    height: 150px;
    object-fit: cover; /* Para que la imagen no se deforme */
    border-radius: 5px;
}

.card h3 { color: #5D4037; }

footer {
    background-color: #3E2723;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 30px;
}
    """

    # Escritura de archivos
    try:
        with open("index.html", "w", encoding="utf-8") as file:
            file.write(html_content)
            print("✅ Archivo index.html creado exitosamente.")

        with open("style.css", "w", encoding="utf-8") as file:
            file.write(css_content)
            print("✅ Archivo style.css creado exitosamente.")
            
        print("\\n¡Listo! Abre el archivo 'index.html' en tu navegador para ver Signori Bistró.")

    except Exception as e:
        print(f"❌ Ocurrió un error al crear los archivos: {e}")

# Ejecutamos la función
if __name__ == "__main__":
    crear_sitio_signori_bistro()
