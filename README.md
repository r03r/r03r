<!DOCTYPE html>
<html lang="es">
<head>
    <!-- Metatags SEO y Social -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Desarrollador Full Stack especializado en Java, Spring y Angular | Apasionado por la creación de soluciones tecnológicas innovadoras">
    <meta name="keywords" content="desarrollador, full stack, java, spring, angular, typescript, cloud, docker">
    <meta property="og:title" content="r03r - Desarrollador Full Stack">
    <meta property="og:description" content="Portfolio técnico y experiencia en desarrollo de software">
    <meta property="og:image" content="https://example.com/your-image.jpg">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:creator" content="@tu_usuario">
    
    <!-- Estilos y Fuentes -->
    <style>
        :root {
            --primary: #2F80ED;
            --secondary: #27AE60;
            --accent: #EB5757;
        }

        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem;
            background: #f8f9fa;
            color: #333;
        }

        .skill-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1rem;
            margin: 2rem 0;
        }

        .skill-card {
            background: white;
            padding: 1rem;
            border-radius: 12px;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }

        .skill-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0,0,0,0.2);
        }

        .skill-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(47,128,237,0.1), transparent);
            transform: rotate(45deg);
            transition: 0.5s;
        }

        .skill-card:hover::before {
            animation: shine 1.5s;
        }

        @keyframes shine {
            0% { left: -50%; }
            100% { left: 150%; }
        }

        .skill-icon {
            width: 48px;
            height: 48px;
            margin: 0 auto 0.5rem;
            transition: transform 0.3s;
        }

        .skill-card:hover .skill-icon {
            transform: scale(1.2) rotate(360deg);
        }

        .badge {
            display: inline-block;
            padding: 0.35em 0.65em;
            font-size: 0.75em;
            font-weight: 700;
            line-height: 1;
            text-align: center;
            white-space: nowrap;
            vertical-align: baseline;
            border-radius: 0.25rem;
            background: var(--primary);
            color: white;
            margin: 0.2rem;
        }

        .interactive-section {
            margin: 2rem 0;
            padding: 1.5rem;
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .animate-on-scroll {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease-out;
        }

        .animate-on-scroll.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Perfil Principal -->
    <header class="interactive-section animate-on-scroll">
        <h1>👋 Hola, Soy r03r</h1>
        <p class="tagline">Desarrollador Full Stack | Especialista en Soluciones Cloud</p>
        
        <div class="skill-grid">
            <!-- Tecnologías Principales -->
            <div class="skill-card">
                <img src="https://www.vectorlogo.zone/logos/java/java-icon.svg" class="skill-icon" alt="Java">
                <div class="badge">Experto</div>
            </div>
            
            <div class="skill-card">
                <img src="https://www.vectorlogo.zone/logos/springio/springio-icon.svg" class="skill-icon" alt="Spring">
                <div class="badge">Avanzado</div>
            </div>
            
            <div class="skill-card">
                <img src="https://www.vectorlogo.zone/logos/angular/angular-icon.svg" class="skill-icon" alt="Angular">
                <div class="badge">Intermedio</div>
            </div>
        </div>
    </header>

    <!-- Sección de Habilidades -->
    <section class="interactive-section animate-on-scroll">
        <h2>🛠 Tech Stack</h2>
        <div class="skill-grid">
            <!-- Lista completa de habilidades con animaciones -->
            <div class="skill-card">
                <img src="https://www.vectorlogo.zone/logos/docker/docker-icon.svg" class="skill-icon" alt="Docker">
                <span class="badge">Containerización</span>
            </div>
            
            <div class="skill-card">
                <img src="https://www.vectorlogo.zone/logos/amazon_aws/amazon_aws-icon.svg" class="skill-icon" alt="AWS">
                <span class="badge">Cloud</span>
            </div>
            
            <!-- Añade más habilidades aquí -->
        </div>
    </section>

    <!-- Sección de Contacto -->
    <section class="interactive-section animate-on-scroll">
        <h2>📫 Conéctate Conmigo</h2>
        <div class="skill-grid">
            <a href="mailto:tu@email.com" class="skill-card">
                <img src="https://www.vectorlogo.zone/logos/gmail/gmail-icon.svg" class="skill-icon" alt="Email">
                <span class="badge">Email</span>
            </a>
            
            <a href="https://linkedin.com/in/tuperfil" target="_blank" class="skill-card">
                <img src="https://www.vectorlogo.zone/logos/linkedin/linkedin-icon.svg" class="skill-icon" alt="LinkedIn">
                <span class="badge">LinkedIn</span>
            </a>
        </div>
    </section>

    <!-- Scripts de Animación -->
    <script>
        // Animación al hacer scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.animate-on-scroll').forEach((element) => {
            observer.observe(element);
        });

        // Efecto interactivo para las tarjetas
        document.querySelectorAll('.skill-card').forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                card.style.setProperty('--mouse-x', `${x}px`);
                card.style.setProperty('--mouse-y', `${y}px`);
            });
        });
    </script>
</body>
</html>
