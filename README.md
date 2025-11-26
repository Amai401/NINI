<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NINI_service - Impulsa tus Redes Sociales</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #ff6b6b;
            --secondary: #4ecdc4;
            --dark: #2c3e50;
            --light: #f8f9fa;
            --accent: #ffd166;
            --whatsapp: #25D366;
        }

        body {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: var(--light);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            padding: 20px 0;
            position: relative;
        }

        .logo {
            text-align: center;
            margin-bottom: 30px;
        }

        .logo h1 {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(45deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 2px 10px rgba(0,0,0,0.1);
            letter-spacing: 2px;
        }

        .logo p {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-top: 10px;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 60px 0;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            margin: 30px 0;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--accent);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }

        /* Services Grid */
        .services {
            padding: 50px 0;
        }

        .services h2 {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 40px;
            color: var(--secondary);
        }

        .platforms-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .platform-card {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease, background 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .platform-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.15);
            border-color: var(--primary);
        }

        .platform-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .platform-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: white;
        }

        /* Contact Section */
        .contact {
            padding: 60px 0;
            text-align: center;
            background: rgba(0, 0, 0, 0.2);
            border-radius: 20px;
            margin: 40px 0;
        }

        .contact h2 {
            font-size: 2.2rem;
            margin-bottom: 30px;
            color: var(--primary);
        }

        .contact-text {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }
        
        /* Botones de Contacto */
        .contact-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .contact-btn {
            display: inline-flex;
            align-items: center;
            padding: 15px 30px;
            font-size: 1.2rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 50px;
            transition: background 0.3s ease, transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            min-width: 250px;
            justify-content: center;
        }

        /* Estilos específicos del Botón de WhatsApp */
        .whatsapp-btn {
            background-color: var(--whatsapp);
            color: var(--light);
            border: 2px solid var(--whatsapp);
        }
        
        .whatsapp-btn:hover {
            background-color: #1DA84E;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(37, 211, 102, 0.4);
        }

        /* Estilos específicos del Botón de Llamada */
        .call-btn {
            background-color: transparent;
            color: var(--accent);
            border: 2px solid var(--accent);
        }

        .call-btn:hover {
            background-color: var(--accent);
            color: var(--dark);
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(255, 209, 102, 0.4);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        footer p {
            opacity: 0.7;
            font-size: 1rem;
        }

        /* Icons Colors */
        .youtube { color: #ff0000; }
        .facebook { color: #1877f2; }
        .twitch { color: #9146ff; }
        .instagram { color: #e1306c; }
        .spotify { color: #1ed760; }
        .telegram { color: #0088cc; }
        .x-twitter { color: #000000; }
        .tiktok { color: #000000; }
        .kick-icon { 
            background: linear-gradient(45deg, #ff0055, #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .logo h1 {
                font-size: 2.5rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .platforms-grid {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            }
            
            .contact-btn {
                font-size: 1rem;
                padding: 12px 20px;
                min-width: 100%;
            }
            
            .contact-buttons {
                flex-direction: column;
            }
        }

        @media (max-width: 480px) {
            .logo h1 {
                font-size: 2rem;
            }
            
            .hero h2 {
                font-size: 1.5rem;
            }
            
            .platforms-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <h1>NINI_service</h1>
                <p>Expertos en impulsar tu presencia digital</p>
            </div>
        </header>

        <section class="hero">
            <h2>¡Impulsa tu Presencia en Redes Sociales!</h2>
            <p>Te ayudo a crecer en todas las plataformas digitales, aumentar tu audiencia y convertir seguidores en verdaderos fans. Estrategias personalizadas para cada red social.</p>
        </section>

        <section class="services">
            <h2>Plataformas que Impulso</h2>
            <div class="platforms-grid">
                <div class="platform-card">
                    <i class="fab fa-youtube platform-icon youtube"></i>
                    <h3>YouTube</h3>
                    <p>Crecimiento de suscriptores,likes vistas y optimización de SEO, estrategias de contenido</p>
                </div>
                <div class="platform-card">
                    <i class="fab fa-facebook platform-icon facebook"></i>
                    <h3>Facebook</h3>
                    <p>Alcance orgánico, publicaciones efectivas, manejo de comunidad y acceso a partner </p>
                </div>
                <div class="platform-card">
                    <i class="fab fa-twitch platform-icon twitch"></i>
                    <h3>Twitch</h3>
                    <p>Crecimiento de viewers, emotes, seguidores y comunidad activa</p>
                </div>
                <div class="platform-card">
                    <i class="fab fa-instagram platform-icon instagram"></i>
                    <h3>Instagram</h3>
                    <p>Hashtags estratégicos, stories virales, engagement y seguidores reales</p>
                </div>
                <div class="platform-card">
                    <i class="fab fa-spotify platform-icon spotify"></i>
                    <h3>Spotify</h3>
                    <p>Playlists, descubrimiento de artistas, seguidores y streams orgánicos</p>
                </div>
                <div class="platform-card">
                    <i class="fab fa-telegram platform-icon telegram"></i>
                    <h3>Telegram</h3>
                    <p>Canales, bots, automatización y crecimiento de miembros</p>
                </div>
                <div class="platform-card">
                    <i class="fab fa-x-twitter platform-icon x-twitter"></i>
                    <h3>X (Twitter)</h3>
                    <p>Trending topics, engagement, seguidores y viralización de contenido</p>
                </div>
                <div class="platform-card">
                    <i class="fab fa-tiktok platform-icon tiktok"></i>
                    <h3>TikTok</h3>
                    <p>Algoritmo, tendencias, seguidores y contenido viral</p>
                </div>
                <div class="platform-card">
                    <i class="fas fa-microphone platform-icon kick-icon"></i>
                    <h3>Kick</h3>
                    <p>Crecimiento en la nueva plataforma de streaming, viewers y comunidad</p>
                </div>
            </div>
        </section>

        <section class="contact">
            <h2>¡Contáctame Ahora!</h2>
            <p class="contact-text">¿Listo para llevar tu presencia digital al siguiente nivel? ¡Hablemos hoy mismo!</p>

            <div class="contact-buttons">
                <a href="https://wa.me/524423964192" target="_blank" class="contact-btn whatsapp-btn">
                    <i class="fab fa-whatsapp"></i>&nbsp; Chatea por WhatsApp
                </a>
                
                <a href="tel:+5214423964192" class="contact-btn call-btn">
                    <i class="fas fa-phone"></i>&nbsp; Llama Ahora
                </a>
            </div>

            <p style="margin-top: 20px;">Disponible para consultas y estrategias personalizadas: +52 1 442 396 4192</p>
        </section>

        <footer>
            <p>&copy; 2025 NINI_service - Todos los derechos reservados</p>
            <p>Especialista en crecimiento digital y marketing de redes sociales</p>
        </footer>
    </div>

    <script>
        // Add hover effect to platform cards
        const cards = document.querySelectorAll('.platform-card');
        cards.forEach(card => {
            card.addEventListener('mouseenter', () => {
                card.style.transform = 'translateY(-10px)';
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'translateY(0)';
            });
        });
    </script>
</body>
</html>


