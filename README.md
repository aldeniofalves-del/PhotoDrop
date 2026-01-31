# PhotoDrop
Aqui está a estrutura de uma Landing Page (PWA Ready) para o PhotoDrop. Ela já conta com um design moderno, focado em conversão, cores vibrantes (Amarelo e Grafite) e é totalmente responsiva.

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PhotoDrop | Suas memórias em mãos</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #FFD700; /* Amarelo Vibrante */
            --dark: #1A1A1B;    /* Grafite */
            --light: #F4F4F9;
            --accent: #FF4500;  /* Laranja para CTAs */
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }

        body { background-color: var(--light); color: var(--dark); line-height: 1.6; }

        /* Header */
        header {
            background: var(--dark);
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .logo { color: var(--primary); font-weight: bold; font-size: 1.5rem; text-transform: uppercase; letter-spacing: 2px; }
        .logo span { color: white; }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1542038784456-1ea8e935640e?auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
            padding: 0 10%;
        }

        .hero h1 { font-size: 3rem; margin-bottom: 1rem; }
        .hero p { font-size: 1.2rem; margin-bottom: 2rem; max-width: 600px; }

        .btn-main {
            background: var(--primary);
            color: var(--dark);
            padding: 1rem 2.5rem;
            text-decoration: none;
            font-weight: bold;
            border-radius: 50px;
            font-size: 1.1rem;
            transition: transform 0.3s ease, background 0.3s ease;
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }

        .btn-main:hover { transform: scale(1.05); background: #e6c200; }

        /* Features */
        .features { padding: 5rem 10%; display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 2rem; background: white; }
        
        .feature-card { text-align: center; padding: 2rem; border-radius: 15px; transition: 0.3s; }
        .feature-card i { font-size: 2.5rem; color: var(--primary); margin-bottom: 1rem; }
        .feature-card h3 { margin-bottom: 0.5rem; }

        /* App Mockup Section (Simplified) */
        .app-demo { padding: 5rem 10%; text-align: center; background: var(--light); }
        .app-screen { 
            max-width: 300px; 
            height: 500px; 
            background: var(--dark); 
            margin: 2rem auto; 
            border: 8px solid #333; 
            border-radius: 40px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        /* Footer */
        footer { background: var(--dark); color: white; padding: 3rem 10% 1rem; text-align: center; }
        .footer-links { margin-bottom: 2rem; }
        .footer-links a { color: #888; text-decoration: none; margin: 0 1rem; font-size: 0.9rem; }
        .footer-links a:hover { color: var(--primary); }
        .legal-text { font-size: 0.7rem; color: #555; margin-top: 2rem; }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            .features { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">PHOTO<span>DROP</span></div>
        <div style="color: white; font-size: 0.8rem;"><i class="fa-solid fa-bicycle"></i> Recife, PE</div>
    </header>

    <section class="hero">
        <h1>Suas memórias não merecem ficar presas na nuvem.</h1>
        <p>Transforme fotos do seu celular em impressões premium entregues via bike em até 2 horas.</p>
        <a href="#pedir" class="btn-main" onclick="startApp()">CRIAR MEU PRIMEIRO DROP</a>
    </section>

    <section class="features">
        <div class="feature-card">
            <i class="fas fa-bolt"></i>
            <h3>Ultra Rápido</h3>
            <p>Impressão e entrega em tempo recorde em Recife.</p>
        </div>
        <div class="feature-card">
            <i class="fas fa-bicycle"></i>
            <h3>100% Sustentável</h3>
            <p>Logística limpa através de ciclo-entregadores parceiros.</p>
        </div>
        <div class="feature-card">
            <i class="fas fa-shield-heart"></i>
            <h3>Privacidade Total</h3>
            <p>Seus arquivos são deletados 24h após a entrega.</p>
        </div>
    </section>

    <section class="app-demo" id="pedir">
        <h2>Como funciona?</h2>
        <div class="app-screen">
            <i class="fa-solid fa-camera-retro" style="font-size: 4rem; color: var(--primary);"></i>
            <p style="margin-top: 20px; padding: 0 20px;">Selecione as fotos da sua galeria e pronto!</p>
            <div style="position: absolute; bottom: 20px; width: 80%; height: 40px; background: var(--primary); border-radius: 20px;"></div>
        </div>
        <p>Simples. Rápido. Físico.</p>
    </section>

    <footer>
        <div class="logo" style="margin-bottom: 1rem;">PHOTO<span>DROP</span></div>
        <div class="footer-links">
            <a href="#">Sobre Nós</a>
            <a href="#">Labs Parceiros</a>
            <a href="#">Termos de Uso</a>
            <a href="#">Privacidade</a>
        </div>
        <div class="socials">
            <i class="fab fa-instagram" style="font-size: 1.5rem; cursor: pointer;"></i>
        </div>
        <p class="legal-text">
            © 2026 PhotoDrop Tecnologia Ltda. <br>
            Protocolo de Dados Efêmeros: Fotos deletadas automaticamente em 24h.
        </p>
    </footer>

    <script>
        function startApp() {
            alert("Iniciando a ponte com o seletor de imagens do celular...");
            // Aqui entraria a lógica do Supabase que configuramos anteriormente.
        }
    </script>
</body>
</html>
