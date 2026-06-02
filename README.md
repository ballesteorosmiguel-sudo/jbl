/* ==========================================================================
   CSS Variables & Tokens
   ========================================================================== */
   :root {
    /* Colors */
    --clr-bg-main: #0d0d0d;
    --clr-bg-darker: #050505;
    --clr-bg-card: #141414;
    --clr-bg-card-hover: #1a1a1a;
    
    --clr-primary: #D4AF37; /* Dorado metálico */
    --clr-primary-hover: #F3E5AB;
    --clr-primary-dark: #aa8a29;
    
    --clr-secondary: #0050FF; /* Azul eléctrico */
    --clr-secondary-hover: #3375ff;
    
    --clr-text-main: #f0f0f0;
    --clr-text-muted: #a0a0a0;
    
    --clr-whatsapp: #25D366;
    --clr-whatsapp-hover: #1EBE5D;
    
    /* Typography */
    --font-heading: 'Montserrat', sans-serif;
    --font-body: 'Inter', sans-serif;
    
    /* Spacing & Layout */
    --nav-height: 80px;
    --section-padding: 5rem 0;
    --container-width: 1200px;
    
    /* Border & Shadows */
    --border-radius: 8px;
    --border-radius-lg: 12px;
    --glass-border: 1px solid rgba(255, 255, 255, 0.05);
    --shadow-gold: 0 4px 20px rgba(212, 175, 55, 0.2);
    --shadow-blue: 0 4px 20px rgba(0, 80, 255, 0.3);
    --shadow-card: 0 10px 30px rgba(0,0,0,0.5);
    
    /* Transitions */
    --transition-fast: 0.2s ease-in-out;
    --transition-normal: 0.3s ease-in-out;
}

/* ==========================================================================
   Reset & Base Styles
   ========================================================================== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    font-size: 16px;
}

body {
    font-family: var(--font-body);
    background-color: var(--clr-bg-main);
    color: var(--clr-text-main);
    line-height: 1.6;
    overflow-x: hidden;
}

a {
    text-decoration: none;
    color: inherit;
}

ul {
    list-style: none;
}

img {
    max-width: 100%;
    height: auto;
    display: block;
}

h1, h2, h3, h4, h5, h6 {
    font-family: var(--font-heading);
    line-height: 1.2;
    color: #fff;
}

/* ==========================================================================
   Utility Classes
   ========================================================================== */
.container {
    max-width: var(--container-width);
    margin: 0 auto;
    padding: 0 1.5rem;
}

.section {
    padding: var(--section-padding);
}

.bg-darker {
    background-color: var(--clr-bg-darker);
}

.section-header {
    text-align: center;
    margin-bottom: 3.5rem;
}

.section-header h2 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.section-header h2 span {
    color: var(--clr-primary);
}

.section-header p {
    color: var(--clr-text-muted);
    font-size: 1.1rem;
    max-width: 600px;
    margin: 0 auto;
}

.mt-3 {
    margin-top: 1.5rem;
}

/* ==========================================================================
   Buttons
   ========================================================================== */
.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    padding: 0.8rem 1.8rem;
    font-family: var(--font-heading);
    font-weight: 700;
    font-size: 1rem;
    border-radius: var(--border-radius);
    cursor: pointer;
    transition: all var(--transition-normal);
    border: none;
    outline: none;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.btn-primary {
    background: linear-gradient(135deg, var(--clr-primary) 0%, var(--clr-primary-dark) 100%);
    color: #000;
    box-shadow: var(--shadow-gold);
}

.btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 25px rgba(212, 175, 55, 0.4);
    background: linear-gradient(135deg, var(--clr-primary-hover) 0%, var(--clr-primary) 100%);
}

.btn-secondary {
    background: linear-gradient(135deg, var(--clr-secondary) 0%, #003dbf 100%);
    color: #fff;
    box-shadow: var(--shadow-blue);
}

.btn-secondary:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 25px rgba(0, 80, 255, 0.5);
    background: linear-gradient(135deg, var(--clr-secondary-hover) 0%, var(--clr-secondary) 100%);
}

.btn-outline {
    background: transparent;
    color: var(--clr-text-main);
    border: 2px solid var(--clr-primary);
}

.btn-outline:hover {
    background: rgba(212, 175, 55, 0.1);
    transform: translateY(-3px);
}

.btn-whatsapp-small {
    background-color: var(--clr-whatsapp);
    color: #fff;
    padding: 0.5rem 1rem;
    font-size: 0.9rem;
    border-radius: 4px;
    width: 100%;
    margin-top: 1rem;
}

.btn-whatsapp-small:hover {
    background-color: var(--clr-whatsapp-hover);
    transform: translateY(-2px);
}

.btn-block {
    width: 100%;
}

.small-btn {
    padding: 0.5rem 1rem;
    font-size: 0.9rem;
}

/* Floating WhatsApp */
.float-wa {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 60px;
    height: 60px;
    background-color: var(--clr-whatsapp);
    color: #fff;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    box-shadow: 0 4px 15px rgba(37, 211, 102, 0.4);
    z-index: 1000;
    transition: transform var(--transition-normal);
}

.float-wa:hover {
    transform: scale(1.1) rotate(5deg);
}

/* ==========================================================================
   Navbar
   ========================================================================== */
.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: var(--nav-height);
    background: rgba(13, 13, 13, 0.95);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    border-bottom: var(--glass-border);
    z-index: 999;
    transition: all var(--transition-normal);
}

.header.scrolled {
    box-shadow: 0 4px 20px rgba(0,0,0,0.8);
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}

.logo {
    display: flex;
    flex-direction: column;
    line-height: 1;
}

.logo-jlb {
    font-family: var(--font-heading);
    font-size: 1.8rem;
    font-weight: 800;
    color: var(--clr-primary);
    letter-spacing: 1px;
}

.logo-sub {
    font-size: 0.8rem;
    text-transform: uppercase;
    color: var(--clr-secondary);
    font-weight: 600;
    letter-spacing: 1.5px;
}

.nav-list {
    display: flex;
    gap: 2rem;
}

.nav-link {
    font-family: var(--font-heading);
    font-size: 0.95rem;
    font-weight: 600;
    text-transform: uppercase;
    transition: color var(--transition-fast);
    position: relative;
}

.nav-link::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0%;
    height: 2px;
    background-color: var(--clr-primary);
    transition: width var(--transition-normal);
}

.nav-link:hover, .nav-link.active {
    color: var(--clr-primary);
}

.nav-link:hover::after, .nav-link.active::after {
    width: 100%;
}

.menu-toggle, .close-menu {
    display: none;
    background: none;
    border: none;
    color: #fff;
    font-size: 1.8rem;
    cursor: pointer;
}

/* ==========================================================================
   Hero Section
   ========================================================================== */
.hero {
    position: relative;
    height: 100vh;
    min-height: 600px;
    display: flex;
    align-items: center;
    background: url('https://images.unsplash.com/photo-1632823462991-88f115d96a79?auto=format&fit=crop&q=80&w=1920') center/cover no-repeat;
    padding-top: var(--nav-height);
}

.hero-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(90deg, rgba(5,5,5,0.95) 0%, rgba(13,13,13,0.7) 100%);
    z-index: 1;
}

.hero-content {
    position: relative;
    z-index: 2;
    max-width: 800px;
}

.hero .title {
    font-size: 4rem;
    margin-bottom: 1rem;
    animation: fadeInUp 1s ease;
}

.hero .title span {
    color: var(--clr-primary);
    display: block;
}

.hero .subtitle {
    font-size: 1.4rem;
    color: var(--clr-text-muted);
    margin-bottom: 2.5rem;
    max-width: 600px;
    animation: fadeInUp 1s ease 0.2s both;
}

.hero-buttons {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    animation: fadeInUp 1s ease 0.4s both;
}

@keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

/* ==========================================================================
   Services Section
   ========================================================================== */
.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.service-card {
    background: var(--clr-bg-card);
    border: var(--glass-border);
    border-radius: var(--border-radius-lg);
    padding: 2.5rem 2rem;
    text-align: center;
    transition: transform var(--transition-normal), background var(--transition-fast);
    position: relative;
    overflow: hidden;
}

.service-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 3px;
    background: linear-gradient(90deg, var(--clr-secondary), var(--clr-primary));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform var(--transition-normal);
}

.service-card:hover {
    transform: translateY(-10px);
    background: var(--clr-bg-card-hover);
    box-shadow: var(--shadow-card);
}

.service-card:hover::before {
    transform: scaleX(1);
}

.service-icon {
    font-size: 3rem;
    color: var(--clr-secondary);
    margin-bottom: 1.5rem;
}

.service-card h3 {
    font-size: 1.3rem;
    margin-bottom: 1rem;
}

.service-card p {
    color: var(--clr-text-muted);
    font-size: 0.95rem;
    margin-bottom: 1.5rem;
}

/* ==========================================================================
   About Section
   ========================================================================== */
.about-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
}

.about-image {
    position: relative;
    border-radius: var(--border-radius-lg);
    overflow: hidden;
}

.about-image img {
    width: 100%;
    object-fit: cover;
    display: block;
    filter: brightness(0.8);
    transition: filter var(--transition-normal);
}

.about-image:hover img {
    filter: brightness(1);
}

.about-experience {
    position: absolute;
    bottom: -20px;
    right: -20px;
    background: linear-gradient(135deg, var(--clr-primary), var(--clr-primary-dark));
    color: #000;
    padding: 2rem;
    border-radius: var(--border-radius);
    text-align: center;
    box-shadow: var(--shadow-gold);
    display: flex;
    flex-direction: column;
}

.exp-number {
    font-family: var(--font-heading);
    font-size: 3rem;
    font-weight: 800;
    line-height: 1;
}

.exp-text {
    font-weight: 700;
    text-transform: uppercase;
    font-size: 0.9rem;
}

.about-content h2 {
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
}

.about-content h2 span {
    color: var(--clr-secondary);
}

.about-content > p {
    color: var(--clr-text-muted);
    margin-bottom: 2rem;
    font-size: 1.1rem;
}

.features-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.features-list li {
    display: flex;
    gap: 1.2rem;
    align-items: flex-start;
}

.features-list i {
    font-size: 1.8rem;
    color: var(--clr-primary);
    background: rgba(212, 175, 55, 0.1);
    padding: 1rem;
    border-radius: 50%;
}

.features-list h3 {
    font-size: 1.2rem;
    margin-bottom: 0.3rem;
}

.features-list p {
    color: var(--clr-text-muted);
    font-size: 0.95rem;
}

/* ==========================================================================
   Gallery Section
   ========================================================================== */
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
}

.gallery-item {
    position: relative;
    border-radius: var(--border-radius);
    overflow: hidden;
    cursor: pointer;
    aspect-ratio: 4/3;
}

.gallery-item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.gallery-overlay {
    position: absolute;
    inset: 0;
    background: rgba(0, 80, 255, 0.6);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: opacity var(--transition-normal);
}

.gallery-overlay i {
    font-size: 3rem;
    color: #fff;
    transform: scale(0.5);
    transition: transform var(--transition-normal);
}

.gallery-item:hover img {
    transform: scale(1.1);
}

.gallery-item:hover .gallery-overlay {
    opacity: 1;
}

.gallery-item:hover .gallery-overlay i {
    transform: scale(1);
}

/* Lightbox */
.lightbox {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, 0.95);
    z-index: 2000;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    visibility: hidden;
    transition: opacity var(--transition-normal);
}

.lightbox.active {
    opacity: 1;
    visibility: visible;
}

.lightbox-img {
    max-width: 90%;
    max-height: 90vh;
    border: 2px solid var(--clr-primary);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-gold);
}

.lightbox-close {
    position: absolute;
    top: 20px;
    right: 30px;
    color: #fff;
    font-size: 3rem;
    cursor: pointer;
    transition: color var(--transition-fast);
}

.lightbox-close:hover {
    color: var(--clr-primary);
}

/* ==========================================================================
   Location Section
   ========================================================================== */
.location-container {
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 2rem;
    background: var(--clr-bg-card);
    border-radius: var(--border-radius-lg);
    overflow: hidden;
    border: var(--glass-border);
}

.location-info {
    padding: 3rem 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.info-card i {
    font-size: 2.5rem;
    color: var(--clr-primary);
    margin-bottom: 1rem;
}

.info-card h3 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
}

.info-card p {
    color: var(--clr-text-muted);
    font-size: 1.1rem;
    margin-bottom: 0.5rem;
}

.location-map iframe {
    width: 100%;
    height: 100%;
    min-height: 400px;
    display: block;
}

/* ==========================================================================
   Contact Section
   ========================================================================== */
.contact-container {
    display: grid;
    grid-template-columns: 1fr 1.5fr;
    gap: 3rem;
}

.contact-details {
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

.contact-item {
    display: flex;
    gap: 1.5rem;
    align-items: center;
    background: var(--clr-bg-card);
    padding: 1.5rem;
    border-radius: var(--border-radius);
    border: var(--glass-border);
    transition: transform var(--transition-fast);
}

.contact-item:hover {
    transform: translateX(10px);
    border-color: var(--clr-secondary);
}

.contact-item .icon-box {
    width: 60px;
    height: 60px;
    background: rgba(0, 80, 255, 0.1);
    color: var(--clr-secondary);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.8rem;
}

.contact-item .content h3 {
    font-size: 1.1rem;
    margin-bottom: 0.3rem;
}

.contact-item .content p, .contact-item .content a {
    color: var(--clr-text-muted);
    font-size: 1rem;
    transition: color var(--transition-fast);
}

.contact-item .content a:hover {
    color: var(--clr-primary);
}

.contact-form {
    background: var(--clr-bg-card);
    padding: 3rem;
    border-radius: var(--border-radius-lg);
    border: var(--glass-border);
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group label {
    display: block;
    margin-bottom: 0.5rem;
    color: var(--clr-text-main);
    font-weight: 600;
}

.form-group input, .form-group textarea {
    width: 100%;
    padding: 1rem;
    background: var(--clr-bg-darker);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: var(--border-radius);
    color: #fff;
    font-family: var(--font-body);
    font-size: 1rem;
    transition: border-color var(--transition-fast);
}

.form-group input:focus, .form-group textarea:focus {
    outline: none;
    border-color: var(--clr-primary);
    background: #000;
}

.form-status {
    margin-top: 1rem;
    text-align: center;
    font-weight: 600;
}

.form-status.success { color: var(--clr-whatsapp); }
.form-status.error { color: #ff3333; }

/* ==========================================================================
   Footer
   ========================================================================== */
.footer {
    background: #000;
    padding-top: 4rem;
    border-top: 2px solid var(--clr-primary);
}

.footer-content {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    gap: 3rem;
    margin-bottom: 3rem;
}

.footer-desc {
    color: var(--clr-text-muted);
    margin-top: 1rem;
    max-width: 300px;
}

.footer-links h3, .footer-social h3 {
    margin-bottom: 1.5rem;
    color: #fff;
    font-size: 1.2rem;
}

.footer-links ul li {
    margin-bottom: 0.8rem;
}

.footer-links ul a {
    color: var(--clr-text-muted);
    transition: color var(--transition-fast);
}

.footer-links ul a:hover {
    color: var(--clr-primary);
    padding-left: 5px;
}

.social-icons {
    display: flex;
    gap: 1rem;
}

.social-icons a {
    width: 40px;
    height: 40px;
    background: var(--clr-bg-card);
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    color: #fff;
    transition: all var(--transition-fast);
}

.social-icons a:hover {
    background: var(--clr-secondary);
    transform: translateY(-3px);
}

.footer-bottom {
    text-align: center;
    padding: 1.5rem;
    background: #050505;
    color: var(--clr-text-muted);
    font-size: 0.9rem;
}

/* ==========================================================================
   Responsive Design
   ========================================================================== */
@media (max-width: 992px) {
    .hero .title { font-size: 3rem; }
    .about-container { grid-template-columns: 1fr; }
    .about-experience { right: 20px; }
    .location-container { grid-template-columns: 1fr; }
    .contact-container { grid-template-columns: 1fr; }
    .footer-content { grid-template-columns: 1fr 1fr; }
}

@media (max-width: 768px) {
    .menu-toggle { display: block; }
    
    .nav-menu {
        position: fixed;
        top: 0;
        right: -100%;
        width: 100%;
        height: 100vh;
        background: rgba(5,5,5,0.98);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transition: right 0.4s ease;
    }

    .nav-menu.open { right: 0; }
    
    .close-menu {
        display: block;
        position: absolute;
        top: 30px;
        right: 30px;
    }

    .nav-list {
        flex-direction: column;
        text-align: center;
        gap: 2rem;
    }

    .nav-link { font-size: 1.5rem; }
    
    .hero { text-align: center; }
    .hero-buttons { justify-content: center; }
    .hero .title { font-size: 2.5rem; }
    
    .section-header h2 { font-size: 2rem; }
    .footer-content { grid-template-columns: 1fr; text-align: center; }
    .footer-desc { margin: 1rem auto; }
    .social-icons { justify-content: center; }
}
