<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SADNESS-MD - L'Évolution Ultime des Bots WhatsApp</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400;1,700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #FF3E80;
            --secondary: #2E86C1;
            --accent: #FFD166;
            --dark: #1A1A2E;
            --light: #F8F9FA;
            --success: #06D6A0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: var(--light);
            overflow-x: hidden;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .serif-italic {
            font-family: 'Playfair Display', serif;
            font-style: italic;
        }
        
        /* Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        @keyframes glow {
            0%, 100% { text-shadow: 0 0 10px var(--primary); }
            50% { text-shadow: 0 0 20px var(--primary), 0 0 30px var(--primary); }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        @keyframes shimmer {
            0% { background-position: -1000px 0; }
            100% { background-position: 1000px 0; }
        }
        
        /* Header Styles */
        .hero-header {
            text-align: center;
            padding: 60px 20px;
            position: relative;
            overflow: hidden;
        }
        
        .hero-header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle at center, transparent 0%, rgba(0,0,0,0.7) 100%);
            z-index: 1;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
        }
        
        .main-title {
            font-size: 4.5rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--primary), var(--accent), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: glow 3s infinite;
            font-family: 'Playfair Display', serif;
            font-style: italic;
        }
        
        .tagline {
            font-size: 1.8rem;
            margin-bottom: 40px;
            color: var(--accent);
            font-family: 'Playfair Display', serif;
            font-style: italic;
        }
        
        .bot-avatar {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 5px solid var(--primary);
            animation: float 6s ease-in-out infinite;
            box-shadow: 0 0 50px rgba(255, 62, 128, 0.5);
            margin: 30px auto;
        }
        
        /* Feature Cards */
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }
        
        .feature-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            border-color: var(--primary);
        }
        
        .feature-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        /* CTA Buttons */
        .cta-button {
            display: inline-block;
            padding: 20px 40px;
            font-size: 1.2rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 50px;
            margin: 10px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            z-index: 1;
            border: 2px solid transparent;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            animation: pulse 2s infinite;
        }
        
        .cta-button:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(255, 62, 128, 0.4);
        }
        
        .cta-button.secondary {
            background: transparent;
            border-color: var(--accent);
            color: var(--accent);
        }
        
        /* Stats */
        .stats-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 60px 0;
        }
        
        .stat-item {
            text-align: center;
            padding: 20px;
        }
        
        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-family: 'Playfair Display', serif;
            font-style: italic;
        }
        
        /* Footer */
        .footer {
            text-align: center;
            padding: 40px;
            margin-top: 60px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .star-button {
            background: linear-gradient(45deg, #FFD700, #FFA500);
            color: #000;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
        }
        
        .star-button:hover {
            transform: rotate(5deg) scale(1.1);
            box-shadow: 0 10px 30px rgba(255, 215, 0, 0.4);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .main-title {
                font-size: 2.5rem;
            }
            
            .tagline {
                font-size: 1.2rem;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <header class="hero-header">
            <div class="hero-content">
                <h1 class="main-title serif-italic">🤖 SADNESS-MD</h1>
                <h2 class="tagline">L'Évolution Ultime des Bots WhatsApp</h2>
                <img src="https://files.catbox.moe/zcg6kh.jpg" alt="SADNESS-MD Avatar" class="bot-avatar">
                <div class="cta-buttons">
                    <a href="#deploy" class="cta-button">🚀 Déployer Maintenant</a>
                    <a href="#features" class="cta-button secondary">✨ Voir les Fonctionnalités</a>
                </div>
            </div>
        </header>

        <!-- Features Section -->
        <section id="features" class="features-section">
            <h2 class="section-title serif-italic" style="text-align: center; font-size: 2.5rem; margin-bottom: 50px;">
                ✨ Révolution Technologique
            </h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3 class="serif-italic">Performance Extrême</h3>
                    <p>Optimisé pour une vitesse de réponse ultrarapide et une stabilité inégalée, même sous forte charge.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🎨</div>
                    <h3 class="serif-italic">Design Élégant</h3>
                    <p>Interface moderne avec animations fluides et expérience utilisateur raffinée.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🔒</div>
                    <h3 class="serif-italic">Sécurité Maximale</h3>
                    <p>Protection avancée et chiffrement des données pour une utilisation en toute confiance.</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">🔄</div>
                    <h3 class="serif-italic">Auto-Maintenance</h3>
                    <p>Mises à jour automatiques et surveillance continue pour une disponibilité 24/7.</p>
                </div>
            </div>
        </section>

        <!-- Deployment Section -->
        <section id="deploy" style="text-align: center; margin: 80px 0;">
            <h2 class="serif-italic" style="font-size: 2.5rem; margin-bottom: 40px;">
                🚀 Déploiement Instantané
            </h2>
            
            <div style="margin: 40px 0;">
                <h3 class="serif-italic" style="color: var(--accent); margin-bottom: 20px;">
                    Étape 1 : Générer votre Session
                </h3>
                <a href="https://sadness-session-id.vercel.app" class="cta-button" target="_blank">
                    🔑 Générer Session
                </a>
                <p style="margin-top: 20px; opacity: 0.9;">
                    <em class="serif-italic">Connectez votre bot via Pair Code ou QR Code — simple, sécurisé, efficace.</em>
                </p>
            </div>
            
            <div style="margin: 40px 0;">
                <h3 class="serif-italic" style="color: var(--accent); margin-bottom: 20px;">
                    Étape 2 : Déployer Gratuitement
                </h3>
                <a href="https://dashboard.katabump.com/auth/login#483bf6" class="cta-button secondary" target="_blank">
                    ☁️ Déployer sur Katabump
                </a>
                <div style="margin-top: 30px; max-width: 600px; margin-left: auto; margin-right: auto;">
                    <ul style="list-style: none; text-align: left;">
                        <li style="margin: 10px 0; padding-left: 30px; position: relative;">
                            <span style="position: absolute; left: 0;">✨</span>
                            <strong>Serveur gratuit</strong> et haute performance
                        </li>
                        <li style="margin: 10px 0; padding-left: 30px; position: relative;">
                            <span style="position: absolute; left: 0;">⚡</span>
                            Support <strong>Node.js natif</strong> optimisé
                        </li>
                        <li style="margin: 10px 0; padding-left: 30px; position: relative;">
                            <span style="position: absolute; left: 0;">🛡️</span>
                            Monitoring et redémarrage automatique
                        </li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Stats -->
        <div class="stats-container">
            <div class="stat-item">
                <div class="stat-number">99.9%</div>
                <div class="stat-label">Disponibilité</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">⚡ 0.2s</div>
                <div class="stat-label">Temps de Réponse</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">10k+</div>
                <div class="stat-label">Utilisateurs</div>
            </div>
        </div>

        <!-- Community Section -->
        <section style="text-align: center; margin: 80px 0;">
            <h2 class="serif-italic" style="font-size: 2.5rem; margin-bottom: 40px;">
                📢 Rejoignez la Révolution
            </h2>
            <div style="margin: 30px 0;">
                <a href="https://whatsapp.com/channel/0029VbCMzVZKWEKvtoE9Jk43" class="cta-button" target="_blank">
                    💬 WhatsApp Channel
                </a>
                <a href="https://t.me/kurona_tech_channel" class="cta-button secondary" target="_blank">
                    📡 Telegram Channel
                </a>
            </div>
        </section>

        <!-- Footer -->
        <footer class="footer">
            <p class="serif-italic" style="font-size: 1.5rem; margin-bottom: 30px;">
                Prêt à révolutionner votre expérience WhatsApp ?
            </p>
            <a href="#" class="star-button">
                ⭐ Donner une Étoile sur GitHub
            </a>
            <p style="margin-top: 40px; opacity: 0.7;">
                <strong>CRAZY KLEIN TECH</strong> • Innovateur derrière SADNESS-MD
            </p>
            <p style="margin-top: 20px; font-size: 0.9rem; opacity: 0.6;">
                ⚖️ À des fins éducatives uniquement • Respectez les conditions d'utilisation de WhatsApp
            </p>
        </footer>
    </div>

    <script>
        // Animation on scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Animate feature cards
        document.querySelectorAll('.feature-card').forEach(card => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(20px)';
            card.style.transition = 'all 0.6s ease';
            observer.observe(card);
        });

        // Add floating particles
        function createParticle() {
            const particle = document.createElement('div');
            particle.style.position = 'fixed';
            particle.style.width = Math.random() * 5 + 2 + 'px';
            particle.style.height = particle.style.width;
            particle.style.background = `rgba(255, ${Math.random() * 100 + 155}, ${Math.random() * 100 + 155}, ${Math.random() * 0.5})`;
            particle.style.borderRadius = '50%';
            particle.style.left = Math.random() * 100 + 'vw';
            particle.style.top = '-10px';
            particle.style.pointerEvents = 'none';
            particle.style.zIndex = '1';
            document.body.appendChild(particle);

            const animation = particle.animate([
                { transform: `translateY(0) rotate(0deg)`, opacity: 1 },
                { transform: `translateY(${window.innerHeight}px) rotate(${Math.random() * 360}deg)`, opacity: 0 }
            ], {
                duration: Math.random() * 3000 + 2000,
                easing: 'cubic-bezier(0.215, 0.61, 0.355, 1)'
            });

            animation.onfinish = () => particle.remove();
        }

        // Create particles periodically
        setInterval(createParticle, 300);

        // Add click effects
        document.addEventListener('click', function(e) {
            const ripple = document.createElement('div');
            ripple.style.position = 'fixed';
            ripple.style.borderRadius = '50%';
            ripple.style.background = 'rgba(255, 255, 255, 0.3)';
            ripple.style.transform = 'translate(-50%, -50%) scale(0)';
            ripple.style.animation = 'ripple 0.6s linear';
            ripple.style.left = e.clientX + 'px';
            ripple.style.top = e.clientY + 'px';
            ripple.style.width = '100px';
            ripple.style.height = '100px';
            ripple.style.pointerEvents = 'none';
            document.body.appendChild(ripple);
            
            setTimeout(() => ripple.remove(), 600);
        });

        // Add ripple animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple {
                to {
                    transform: translate(-50%, -50%) scale(4);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html></div>

---

⚠️ Avertissement Légal

⚖️ Ce projet est fourni à des fins éducatives et d'apprentissage uniquement.
L'utilisateur est seul responsable de l'utilisation de ce bot et doit se conformer aux Conditions d'Utilisation de WhatsApp.
L'auteur ne peut être tenu responsable d'une mauvaise utilisation.

---

👑 Créateur & Contributeur

<p align="center">
  <strong>SADNESS TECH</strong><br>
  <em>Innovateur derrière SADNESS-MD</em>
</p>

<p align="center">
  <a href="https://t.me/kurona_tech_channel" target="_blank">
  <img src="https://img.shields.io/badge/📢_Telegram_Channel-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram Channel" height="40">
  </a>
  <a href="https://whatsapp.com/channel/0029VbCMzVZKWEKvtoE9Jk43" target="_blank">
    <img src="https://img.shields.io/badge/📲_WhatsApp_Channel-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp Channel" height="40">
  </a>
</p>

---

<p align="center">
  <strong>Si ce projet vous a plu, montrez votre soutien en lui donnant une étoile ! ⭐</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/your-repo?style=social" alt="GitHub Stars">
</p>

---

✨ Prêt à révolutionner votre expérience WhatsApp ? Déployez SADNESS-MD dès maintenant !
