<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes" />
    <meta name="theme-color" content="#6C3CE1" />
    <meta name="apple-mobile-web-app-capable" content="yes" />
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
    <title>Zeevanna Digital @ Service</title>

    <!-- Font & Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />

    <style>
        /* ===== RESET & BASE ===== */
        *,
        *::before,
        *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #6C3CE1;
            --primary-light: #8B5CF6;
            --primary-dark: #5B2FC9;
            --primary-gradient: linear-gradient(135deg, #6C3CE1 0%, #A78BFA 100%);
            --secondary: #F59E0B;
            --accent: #EC4899;
            --bg: #F8FAFC;
            --card-bg: #FFFFFF;
            --text-primary: #0F172A;
            --text-secondary: #475569;
            --text-muted: #94A3B8;
            --shadow: 0 8px 32px rgba(108, 60, 225, 0.15);
            --shadow-sm: 0 2px 12px rgba(0, 0, 0, 0.06);
            --radius: 20px;
            --radius-sm: 12px;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            --safe-bottom: env(safe-area-inset-bottom, 0px);
        }

        html {
            scroll-behavior: smooth;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: var(--bg);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            padding-bottom: calc(80px + var(--safe-bottom));
            min-height: 100vh;
            min-height: 100dvh;
        }

        /* ===== SCROLLBAR ===== */
        ::-webkit-scrollbar {
            width: 4px;
        }
        ::-webkit-scrollbar-track {
            background: transparent;
        }
        ::-webkit-scrollbar-thumb {
            background: var(--primary-light);
            border-radius: 10px;
        }

        /* ===== UTILITY ===== */
        .container {
            max-width: 480px;
            margin: 0 auto;
            padding: 0 18px;
        }

        .section-title {
            font-size: 1.5rem;
            font-weight: 800;
            letter-spacing: -0.03em;
            margin-bottom: 6px;
            color: var(--text-primary);
        }
        .section-subtitle {
            font-size: 0.9rem;
            color: var(--text-secondary);
            margin-bottom: 20px;
            font-weight: 400;
        }

        .badge {
            display: inline-block;
            background: var(--primary-gradient);
            color: #fff;
            font-size: 0.7rem;
            font-weight: 600;
            padding: 4px 14px;
            border-radius: 50px;
            letter-spacing: 0.3px;
            text-transform: uppercase;
        }

        /* ===== BUTTONS ===== */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 14px 28px;
            border: none;
            border-radius: 50px;
            font-family: inherit;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
            width: 100%;
            max-width: 100%;
            touch-action: manipulation;
        }

        .btn-primary {
            background: var(--primary-gradient);
            color: #fff;
            box-shadow: 0 4px 20px rgba(108, 60, 225, 0.35);
        }
        .btn-primary:hover,
        .btn-primary:active {
            transform: translateY(-2px) scale(1.02);
            box-shadow: 0 8px 30px rgba(108, 60, 225, 0.45);
        }

        .btn-whatsapp {
            background: #25D366;
            color: #fff;
            box-shadow: 0 4px 20px rgba(37, 211, 102, 0.35);
        }
        .btn-whatsapp:hover,
        .btn-whatsapp:active {
            transform: translateY(-2px) scale(1.02);
            box-shadow: 0 8px 30px rgba(37, 211, 102, 0.45);
        }

        .btn-outline {
            background: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }
        .btn-outline:hover,
        .btn-outline:active {
            background: var(--primary);
            color: #fff;
        }

        .btn-sm {
            padding: 10px 20px;
            font-size: 0.85rem;
        }

        /* ===== HEADER / NAV ===== */
        .header {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(16px) saturate(180%);
            -webkit-backdrop-filter: blur(16px) saturate(180%);
            border-bottom: 1px solid rgba(108, 60, 225, 0.08);
            padding: 12px 0;
        }
        .header .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        .header-brand {
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
        }
        .header-brand .logo-icon {
            width: 42px;
            height: 42px;
            background: var(--primary-gradient);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-size: 1.2rem;
            font-weight: 800;
            box-shadow: 0 4px 12px rgba(108, 60, 225, 0.3);
        }
        .header-brand .brand-text {
            font-weight: 800;
            font-size: 1.1rem;
            letter-spacing: -0.02em;
            color: var(--text-primary);
        }
        .header-brand .brand-text span {
            color: var(--primary);
        }
        .header-actions {
            display: flex;
            gap: 8px;
        }
        .header-actions a {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--bg);
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-secondary);
            font-size: 1.1rem;
            transition: var(--transition);
            text-decoration: none;
            border: 1px solid rgba(0, 0, 0, 0.04);
        }
        .header-actions a:active {
            transform: scale(0.92);
            background: var(--primary-light);
            color: #fff;
        }

        /* ===== HERO ===== */
        .hero {
            padding: 30px 0 24px;
            text-align: center;
        }
        .hero-badge {
            margin-bottom: 12px;
        }
        .hero h1 {
            font-size: 2.1rem;
            font-weight: 800;
            letter-spacing: -0.04em;
            line-height: 1.15;
            margin-bottom: 8px;
        }
        .hero h1 .highlight {
            background: var(--primary-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .hero p {
            font-size: 1rem;
            color: var(--text-secondary);
            max-width: 340px;
            margin: 0 auto 20px;
        }
        .hero .hero-stats {
            display: flex;
            justify-content: center;
            gap: 24px;
            margin-top: 16px;
        }
        .hero .hero-stats .stat {
            text-align: center;
        }
        .hero .hero-stats .stat .num {
            font-size: 1.4rem;
            font-weight: 800;
            color: var(--primary);
        }
        .hero .hero-stats .stat .label {
            font-size: 0.7rem;
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .hero-image {
            margin: 16px auto 0;
            width: 100%;
            max-width: 280px;
            aspect-ratio: 1/1;
            background: var(--primary-gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4.5rem;
            color: #fff;
            box-shadow: 0 20px 60px rgba(108, 60, 225, 0.3);
            position: relative;
            overflow: hidden;
        }
        .hero-image::after {
            content: '';
            position: absolute;
            inset: 0;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transform: scale(0);
            transition: transform 0.6s ease;
        }
        .hero-image:active::after {
            transform: scale(1);
        }

        /* ===== QUICK ACTION ===== */
        .quick-actions {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
            margin: 16px 0 8px;
        }
        .quick-actions .qa-btn {
            background: var(--card-bg);
            border: 1px solid rgba(0, 0, 0, 0.04);
            border-radius: var(--radius-sm);
            padding: 16px 12px;
            text-align: center;
            text-decoration: none;
            color: var(--text-primary);
            transition: var(--transition);
            box-shadow: var(--shadow-sm);
            touch-action: manipulation;
        }
        .quick-actions .qa-btn:active {
            transform: scale(0.96);
            border-color: var(--primary-light);
        }
        .quick-actions .qa-btn i {
            font-size: 1.6rem;
            color: var(--primary);
            display: block;
            margin-bottom: 4px;
        }
        .quick-actions .qa-btn span {
            font-size: 0.75rem;
            font-weight: 600;
            display: block;
        }

        /* ===== CARDS ===== */
        .card {
            background: var(--card-bg);
            border-radius: var(--radius);
            padding: 20px;
            box-shadow: var(--shadow-sm);
            margin-bottom: 16px;
            border: 1px solid rgba(0, 0, 0, 0.03);
            transition: var(--transition);
        }
        .card:active {
            transform: scale(0.995);
        }

        .card-glass {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        /* ===== SERVICES ===== */
        .services-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }
        .service-item {
            background: var(--card-bg);
            border-radius: var(--radius-sm);
            padding: 16px 12px;
            text-align: center;
            border: 1px solid rgba(0, 0, 0, 0.04);
            box-shadow: var(--shadow-sm);
            transition: var(--transition);
        }
        .service-item:active {
            transform: scale(0.96);
        }
        .service-item .icon {
            width: 48px;
            height: 48px;
            background: var(--primary-gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 8px;
            color: #fff;
            font-size: 1.3rem;
        }
        .service-item h4 {
            font-size: 0.85rem;
            font-weight: 700;
        }
        .service-item p {
            font-size: 0.7rem;
            color: var(--text-muted);
            margin-top: 2px;
        }

        /* ===== PRICE LIST ===== */
        .price-list {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        .price-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.04);
        }
        .price-row:last-child {
            border-bottom: none;
        }
        .price-row .item {
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .price-row .item .emoji {
            font-size: 1.2rem;
        }
        .price-row .item .name {
            font-weight: 600;
            font-size: 0.9rem;
        }
        .price-row .item .desc {
            font-size: 0.7rem;
            color: var(--text-muted);
            display: block;
        }
        .price-row .price {
            font-weight: 700;
            color: var(--primary);
            font-size: 1rem;
        }

        /* ===== ORDER FORM ===== */
        .form-group {
            margin-bottom: 16px;
        }
        .form-group label {
            display: block;
            font-weight: 600;
            font-size: 0.85rem;
            margin-bottom: 4px;
            color: var(--text-secondary);
        }
        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 14px 16px;
            border: 2px solid rgba(0, 0, 0, 0.06);
            border-radius: var(--radius-sm);
            font-family: inherit;
            font-size: 0.95rem;
            background: var(--bg);
            transition: var(--transition);
            outline: none;
            -webkit-appearance: none;
            appearance: none;
        }
        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            border-color: var(--primary);
            box-shadow: 0 0 0 4px rgba(108, 60, 225, 0.1);
            background: #fff;
        }
        .form-group textarea {
            resize: vertical;
            min-height: 80px;
        }
        .form-group select {
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%236C3CE1' stroke-width='2' fill='none'/%3E%3C/svg%3E");
            background-repeat: no-repeat;
            background-position: right 16px center;
            padding-right: 44px;
        }

        /* ===== CONTACT ===== */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }
        .contact-card {
            background: var(--card-bg);
            border-radius: var(--radius-sm);
            padding: 16px;
            text-align: center;
            border: 1px solid rgba(0, 0, 0, 0.04);
            box-shadow: var(--shadow-sm);
            text-decoration: none;
            color: var(--text-primary);
            transition: var(--transition);
            touch-action: manipulation;
        }
        .contact-card:active {
            transform: scale(0.96);
        }
        .contact-card i {
            font-size: 1.8rem;
            color: var(--primary);
            display: block;
            margin-bottom: 4px;
        }
        .contact-card .label {
            font-size: 0.7rem;
            color: var(--text-muted);
            display: block;
        }
        .contact-card .value {
            font-weight: 700;
            font-size: 0.85rem;
        }
        .contact-card.wa i {
            color: #25D366;
        }
        .contact-card.telp i {
            color: var(--primary);
        }

        /* ===== TESTIMONIALS ===== */
        .testimonial-item {
            background: var(--card-bg);
            border-radius: var(--radius-sm);
            padding: 16px;
            border: 1px solid rgba(0, 0, 0, 0.04);
            box-shadow: var(--shadow-sm);
            margin-bottom: 10px;
        }
        .testimonial-item .stars {
            color: var(--secondary);
            font-size: 0.9rem;
            letter-spacing: 2px;
        }
        .testimonial-item p {
            font-size: 0.9rem;
            color: var(--text-secondary);
            margin: 4px 0;
        }
        .testimonial-item .name {
            font-weight: 600;
            font-size: 0.8rem;
        }

        /* ===== FOOTER ===== */
        .footer {
            text-align: center;
            padding: 24px 0 12px;
            color: var(--text-muted);
            font-size: 0.75rem;
        }
        .footer .brand {
            font-weight: 700;
            color: var(--text-primary);
        }
        .footer .brand span {
            color: var(--primary);
        }

        /* ===== BOTTOM NAV ===== */
        .bottom-nav {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(16px) saturate(180%);
            -webkit-backdrop-filter: blur(16px) saturate(180%);
            border-top: 1px solid rgba(0, 0, 0, 0.04);
            padding: 8px 0 calc(8px + var(--safe-bottom));
            z-index: 200;
            display: flex;
            justify-content: space-around;
            align-items: center;
        }
        .bottom-nav a {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: var(--text-muted);
            font-size: 0.6rem;
            font-weight: 600;
            transition: var(--transition);
            padding: 4px 12px;
            touch-action: manipulation;
            min-width: 56px;
        }
        .bottom-nav a i {
            font-size: 1.3rem;
            margin-bottom: 1px;
            transition: var(--transition);
        }
        .bottom-nav a.active {
            color: var(--primary);
        }
        .bottom-nav a.active i {
            transform: translateY(-2px);
        }
        .bottom-nav a:active {
            transform: scale(0.9);
        }
        .bottom-nav .nav-wa {
            background: var(--primary-gradient);
            color: #fff !important;
            padding: 8px 18px;
            border-radius: 50px;
            flex-direction: row;
            gap: 8px;
            font-size: 0.7rem;
            box-shadow: 0 4px 20px rgba(108, 60, 225, 0.3);
        }
        .bottom-nav .nav-wa i {
            font-size: 1rem;
            margin-bottom: 0;
        }
        .bottom-nav .nav-wa:active {
            transform: scale(0.95);
        }

        /* ===== ANIMATIONS ===== */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .anim-fade-up {
            animation: fadeUp 0.5s ease forwards;
            opacity: 0;
        }
        .anim-delay-1 {
            animation-delay: 0.1s;
        }
        .anim-delay-2 {
            animation-delay: 0.2s;
        }
        .anim-delay-3 {
            animation-delay: 0.3s;
        }
        .anim-delay-4 {
            animation-delay: 0.4s;
        }

        /* ===== TOAST ===== */
        .toast {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%) translateY(-80px);
            background: var(--text-primary);
            color: #fff;
            padding: 12px 24px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            z-index: 999;
            transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            max-width: 90%;
            text-align: center;
            pointer-events: none;
        }
        .toast.show {
            transform: translateX(-50%) translateY(0);
        }

        /* ===== RESPONSIVE TWEAKS ===== */
        @media (max-width: 400px) {
            .hero h1 {
                font-size: 1.7rem;
            }
            .services-grid {
                grid-template-columns: 1fr 1fr;
                gap: 8px;
            }
            .service-item {
                padding: 12px 8px;
            }
            .service-item .icon {
                width: 40px;
                height: 40px;
                font-size: 1rem;
            }
            .quick-actions .qa-btn i {
                font-size: 1.3rem;
            }
            .contact-grid {
                grid-template-columns: 1fr 1fr;
                gap: 8px;
            }
        }

        @media (min-width: 600px) {
            body {
                padding: 0 24px calc(80px + var(--safe-bottom));
            }
            .container {
                max-width: 560px;
            }
        }

        /* ===== DARK MODE SUPPORT ===== */
        @media (prefers-color-scheme: dark) {
            :root {
                --bg: #0F172A;
                --card-bg: #1E293B;
                --text-primary: #F1F5F9;
                --text-secondary: #CBD5E1;
                --text-muted: #94A3B8;
                --shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
                --shadow-sm: 0 2px 12px rgba(0, 0, 0, 0.3);
            }
            .header {
                background: rgba(15, 23, 42, 0.85);
                border-bottom-color: rgba(255, 255, 255, 0.06);
            }
            .header-actions a {
                background: #1E293B;
                border-color: rgba(255, 255, 255, 0.06);
                color: var(--text-secondary);
            }
            .card-glass {
                background: rgba(30, 41, 59, 0.7);
                border-color: rgba(255, 255, 255, 0.05);
            }
            .bottom-nav {
                background: rgba(15, 23, 42, 0.92);
                border-top-color: rgba(255, 255, 255, 0.06);
            }
            .form-group input,
            .form-group select,
            .form-group textarea {
                background: #1E293B;
                border-color: rgba(255, 255, 255, 0.06);
                color: var(--text-primary);
            }
            .form-group input:focus,
            .form-group select:focus,
            .form-group textarea:focus {
                background: #1E293B;
                border-color: var(--primary);
            }
            .service-item,
            .contact-card,
            .testimonial-item,
            .quick-actions .qa-btn {
                background: #1E293B;
                border-color: rgba(255, 255, 255, 0.04);
            }
            .price-row {
                border-bottom-color: rgba(255, 255, 255, 0.04);
            }
            .hero-image {
                box-shadow: 0 20px 60px rgba(108, 60, 225, 0.2);
            }
        }
    </style>
</head>
<body>

    <!-- ===== TOAST ===== -->
    <div class="toast" id="toast">✅ Pesanan berhasil dikirim!</div>

    <!-- ===== HEADER ===== -->
    <header class="header">
        <div class="container">
            <a href="#" class="header-brand">
                <div class="logo-icon">Z</div>
                <div class="brand-text">Zeevanna <span>Digital</span></div>
            </a>
            <div class="header-actions">
                <a href="tel:083819023700" aria-label="Telepon">
                    <i class="fas fa-phone"></i>
                </a>
                <a href="https://wa.me/6283819023700" target="_blank" aria-label="WhatsApp">
                    <i class="fab fa-whatsapp"></i>
                </a>
            </div>
        </div>
    </header>

    <!-- ===== MAIN ===== -->
    <main>

        <!-- ===== HERO ===== -->
        <section class="hero">
            <div class="container">
                <div class="hero-badge badge anim-fade-up">✨ Layanan Setrika Online</div>
                <h1 class="anim-fade-up anim-delay-1">
                    Setrika <span class="highlight">Rapi</span> &amp; <span class="highlight">Wang</span> Tanpa Ribet
                </h1>
                <p class="anim-fade-up anim-delay-2">
                    Pesan jasa setrika online dari rumah. Kami jemput &amp; antar gratis!
                </p>

                <div class="hero-image anim-fade-up anim-delay-2">
                    <i class="fas fa-iron"></i>
                </div>

                <div class="hero-stats anim-fade-up anim-delay-3">
                    <div class="stat">
                        <div class="num">500+</div>
                        <div class="label">Pelanggan</div>
                    </div>
                    <div class="stat">
                        <div class="num">4.9</div>
                        <div class="label">Rating ⭐</div>
                    </div>
                    <div class="stat">
                        <div class="num">15</div>
                        <div class="label">Kota</div>
                    </div>
                </div>

                <!-- Quick Actions -->
                <div class="quick-actions anim-fade-up anim-delay-4">
                    <a href="https://wa.me/6283819023700?text=Halo%20Zeevanna%2C%20saya%20mau%20pesan%20setrika%20online" target="_blank" class="qa-btn">
                        <i class="fab fa-whatsapp" style="color:#25D366;"></i>
                        <span>Pesan via WA</span>
                    </a>
                    <a href="#order" class="qa-btn">
                        <i class="fas fa-clipboard-list"></i>
                        <span>Pesan Sekarang</span>
                    </a>
                    <a href="#price" class="qa-btn">
                        <i class="fas fa-tags"></i>
                        <span>Lihat Harga</span>
                    </a>
                    <a href="#contact" class="qa-btn">
                        <i class="fas fa-address-card"></i>
                        <span>Kontak</span>
                    </a>
                </div>
            </div>
        </section>

        <!-- ===== SERVICES ===== -->
        <section id="services" class="container" style="padding-top:8px;">
            <div class="section-title anim-fade-up">Layanan Kami</div>
            <div class="section-subtitle anim-fade-up anim-delay-1">Profesional, cepat, dan terpercaya</div>

            <div class="services-grid anim-fade-up anim-delay-2">
                <div class="service-item">
                    <div class="icon"><i class="fas fa-tshirt"></i></div>
                    <h4>Setrika Biasa</h4>
                    <p>Baju, kemeja, celana</p>
                </div>
                <div class="service-item">
                    <div class="icon"><i class="fas fa-user-tie"></i></div>
                    <h4>Setrika Premium</h4>
                    <p>Jas, gaun, bahan halus</p>
                </div>
                <div class="service-item">
                    <div class="icon"><i class="fas fa-bed"></i></div>
                    <h4>Setrika Sprei</h4>
                    <p>Sprei, sarung bantal</p>
                </div>
                <div class="service-item">
                    <div class="icon"><i class="fas fa-truck"></i></div>
                    <h4>Jemput &amp; Antar</h4>
                    <p>Gratis ongkir*</p>
                </div>
            </div>
        </section>

        <!-- ===== PRICE LIST ===== -->
        <section id="price" class="container" style="padding-top:24px;">
            <div class="section-title anim-fade-up">Daftar Harga</div>
            <div class="section-subtitle anim-fade-up anim-delay-1">Harga terjangkau, hasil memuaskan</div>

            <div class="card anim-fade-up anim-delay-2">
                <div class="price-list">
                    <div class="price-row">
                        <div class="item">
                            <span class="emoji">👕</span>
                            <div>
                                <span class="name">Kemeja / Blouse</span>
                                <span class="desc">Bahan katun, linen</span>
                            </div>
                        </div>
                        <span class="price">Rp 8.000</span>
                    </div>
                    <div class="price-row">
                        <div class="item">
                            <span class="emoji">👖</span>
                            <div>
                                <span class="name">Celana Panjang</span>
                                <span class="desc">Jeans, chino, kain</span>
                            </div>
                        </div>
                        <span class="price">Rp 10.000</span>
                    </div>
                    <div class="price-row">
                        <div class="item">
                            <span class="emoji">👗</span>
                            <div>
                                <span class="name">Gaun / Dress</span>
                                <span class="desc">Sutra, satin, katun</span>
                            </div>
                        </div>
                        <span class="price">Rp 15.000</span>
                    </div>
                    <div class="price-row">
                        <div class="item">
                            <span class="emoji">🛏️</span>
                            <div>
                                <span class="name">Sprei (per set)</span>
                                <span class="desc">+ sarung bantal</span>
                            </div>
                        </div>
                        <span class="price">Rp 25.000</span>
                    </div>
                    <div class="price-row">
                        <div class="item">
                            <span class="emoji">🧥</span>
                            <div>
                                <span class="name">Jas / Blazer</span>
                                <span class="desc">Premium handling</span>
                            </div>
                        </div>
                        <span class="price">Rp 20.000</span>
                    </div>
                </div>
                <div style="margin-top:12px;font-size:0.75rem;color:var(--text-muted);text-align:center;">
                    * Minimal pemesanan 5 pcs &nbsp;·&nbsp; Gratis antar untuk area tertentu
                </div>
            </div>
        </section>

        <!-- ===== ORDER FORM ===== -->
        <section id="order" class="container" style="padding-top:24px;">
            <div class="section-title anim-fade-up">Pesan Sekarang</div>
            <div class="section-subtitle anim-fade-up anim-delay-1">Isi form di bawah, kami akan hubungi Anda</div>

            <div class="card anim-fade-up anim-delay-2">
                <form id="orderForm" novalidate>
                    <div class="form-group">
                        <label for="nama">Nama Lengkap</label>
                        <input type="text" id="nama" placeholder="Contoh: Andi Pratama" required />
                    </div>
                    <div class="form-group">
                        <label for="noHp">Nomor HP</label>
                        <input type="tel" id="noHp" placeholder="08xxxxxxxxxx" required />
                    </div>
                    <div class="form-group">
                        <label for="alamat">Alamat Jemput</label>
                        <input type="text" id="alamat" placeholder="Jl. Contoh No. 123, RT/RW..." required />
                    </div>
                    <div class="form-group">
                        <label for="layanan">Jenis Layanan</label>
                        <select id="layanan" required>
                            <option value="">Pilih layanan...</option>
                            <option value="Setrika Biasa">Setrika Biasa</option>
                            <option value="Setrika Premium">Setrika Premium</option>
                            <option value="Setrika Sprei">Setrika Sprei</option>
                            <option value="Paket Hemat (10 pcs)">Paket Hemat (10 pcs)</option>
                            <option value="Paket Keluarga (20 pcs)">Paket Keluarga (20 pcs)</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="jumlah">Jumlah Pakaian</label>
                        <input type="number" id="jumlah" placeholder="Min. 5 pcs" min="1" required />
                    </div>
                    <div class="form-group">
                        <label for="catatan">Catatan Tambahan</label>
                        <textarea id="catatan" placeholder="Misal: bahan rawan, lipatan khusus, dll."></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary">
                        <i class="fas fa-paper-plane"></i> Kirim Pesanan
                    </button>
                </form>
            </div>
        </section>

        <!-- ===== TESTIMONIALS ===== -->
        <section class="container" style="padding-top:24px;">
            <div class="section-title anim-fade-up">Apa Kata Mereka</div>
            <div class="section-subtitle anim-fade-up anim-delay-1">Pelanggan puas dengan layanan kami</div>

            <div class="anim-fade-up anim-delay-2">
                <div class="testimonial-item">
                    <div class="stars">⭐⭐⭐⭐⭐</div>
                    <p>"Setrikaannya rapi banget, wangi, dan diantar tepat waktu. Recomended!"</p>
                    <div class="name">— Rina, Jakarta</div>
                </div>
                <div class="testimonial-item">
                    <div class="stars">⭐⭐⭐⭐⭐</div>
                    <p>"Sudah 3 kali pakai, hasil selalu memuaskan. Harga juga bersahabat."</p>
                    <div class="name">— Budi, Tangerang</div>
                </div>
                <div class="testimonial-item">
                    <div class="stars">⭐⭐⭐⭐⭐</div>
                    <p>"Layanan jemput antar sangat membantu. Gaun pesta saya rapi sempurna!"</p>
                    <div class="name">— Sari, Bekasi</div>
                </div>
            </div>
        </section>

        <!-- ===== CONTACT ===== -->
        <section id="contact" class="container" style="padding-top:24px;">
            <div class="section-title anim-fade-up">Hubungi Kami</div>
            <div class="section-subtitle anim-fade-up anim-delay-1">Siap melayani Anda 24 jam</div>

            <div class="contact-grid anim-fade-up anim-delay-2">
                <a href="https://wa.me/6283819023700" target="_blank" class="contact-card wa">
                    <i class="fab fa-whatsapp"></i>
                    <span class="label">WhatsApp</span>
                    <span class="value">0838-1902-3700</span>
                </a>
                <a href="https://wa.me/6281285526012" target="_blank" class="contact-card wa">
                    <i class="fab fa-whatsapp"></i>
                    <span class="label">WhatsApp</span>
                    <span class="value">0812-8552-6012</span>
                </a>
                <a href="tel:083819023700" class="contact-card telp">
                    <i class="fas fa-phone"></i>
                    <span class="label">Telepon</span>
                    <span class="value">0838-1902-3700</span>
                </a>
                <a href="tel:081285526012" class="contact-card telp">
                    <i class="fas fa-phone"></i>
                    <span class="label">Telepon</span>
                    <span class="value">0812-8552-6012</span>
                </a>
            </div>

            <div class="card card-glass anim-fade-up anim-delay-3" style="margin-top:8px;text-align:center;">
                <i class="fas fa-map-pin" style="color:var(--primary);font-size:1.4rem;"></i>
                <p style="font-size:0.85rem;margin-top:4px;color:var(--text-secondary);">
                    Melayani: Jakarta, Tangerang, Bekasi, Depok, &amp; sekitarnya
                </p>
                <p style="font-size:0.7rem;color:var(--text-muted);margin-top:2px;">
                    📍 Jemput &amp; antar gratis untuk area terpilih
                </p>
            </div>
        </section>

        <!-- ===== FOOTER ===== -->
        <footer class="footer container">
            <p>
                <span class="brand">Zeevanna <span>Digital</span> @ Service</span>
                &nbsp;·&nbsp; Jasa Setrika Online Profesional
            </p>
            <p style="margin-top:4px;font-size:0.65rem;">
                &copy; 2026 Zeevanna Digital. All rights reserved.
            </p>
        </footer>

    </main>

    <!-- ===== BOTTOM NAV ===== -->
    <nav class="bottom-nav" id="bottomNav">
        <a href="#" class="active" data-target="home">
            <i class="fas fa-home"></i>
            <span>Beranda</span>
        </a>
        <a href="#services" data-target="services">
            <i class="fas fa-concierge-bell"></i>
            <span>Layanan</span>
        </a>
        <a href="#order" data-target="order">
            <i class="fas fa-clipboard-list"></i>
            <span>Pesan</span>
        </a>
        <a href="#contact" data-target="contact">
            <i class="fas fa-headset"></i>
            <span>Kontak</span>
        </a>
        <a href="https://wa.me/6283819023700?text=Halo%20Zeevanna%2C%20saya%20mau%20pesan%20setrika%20online" target="_blank" class="nav-wa">
            <i class="fab fa-whatsapp"></i>
            <span>WA</span>
        </a>
    </nav>

    <!-- ===== JAVASCRIPT ===== -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {

            // ----- TOAST -----
            const toast = document.getElementById('toast');
            let toastTimer = null;

            function showToast(msg) {
                toast.textContent = msg || '✅ Pesanan berhasil dikirim!';
                toast.classList.add('show');
                clearTimeout(toastTimer);
                toastTimer = setTimeout(() => {
                    toast.classList.remove('show');
                }, 3500);
            }

            // ----- ORDER FORM -----
            const form = document.getElementById('orderForm');
            form.addEventListener('submit', function(e) {
                e.preventDefault();

                const nama = document.getElementById('nama').value.trim();
                const noHp = document.getElementById('noHp').value.trim();
                const alamat = document.getElementById('alamat').value.trim();
                const layanan = document.getElementById('layanan').value;
                const jumlah = document.getElementById('jumlah').value.trim();
                const catatan = document.getElementById('catatan').value.trim();

                // Validasi sederhana
                if (!nama || !noHp || !alamat || !layanan || !jumlah) {
                    showToast('⚠️ Harap isi semua kolom yang wajib!');
                    return;
                }

                if (parseInt(jumlah) < 1) {
                    showToast('⚠️ Jumlah pakaian minimal 1');
                    return;
                }

                // Build WA message
                const message =
                    `Halo Zeevanna Digital! Saya mau pesan setrika online.%0A%0A` +
                    `📋 *Data Pemesan*%0A` +
                    `Nama: ${nama}%0A` +
                    `No HP: ${noHp}%0A` +
                    `Alamat: ${alamat}%0A%0A` +
                    `👕 *Detail Pesanan*%0A` +
                    `Layanan: ${layanan}%0A` +
                    `Jumlah: ${jumlah} pcs%0A` +
                    `Catatan: ${catatan || 'Tidak ada'}`;

                // Kirim ke WA (nomor utama)
                const waUrl = `https://wa.me/6283819023700?text=${message}`;
                window.open(waUrl, '_blank');

                showToast('✅ Pesanan dikirim! Tunggu konfirmasi dari kami.');

                // Reset form setelah delay
                setTimeout(() => {
                    form.reset();
                }, 2000);
            });

            // ----- BOTTOM NAV ACTIVE STATE -----
            const navLinks = document.querySelectorAll('.bottom-nav a[data-target]');
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    // Hanya untuk link internal (bukan WA)
                    if (this.dataset.target) {
                        navLinks.forEach(l => l.classList.remove('active'));
                        this.classList.add('active');

                        // Jika target adalah 'home', scroll ke atas
                        if (this.dataset.target === 'home') {
                            e.preventDefault();
                            window.scrollTo({ top: 0, behavior: 'smooth' });
                        }
                    }
                });
            });

            // Update active state saat scroll
            const sections = ['home', 'services', 'order', 'contact'];
            const sectionElements = {
                home: document.querySelector('.hero'),
                services: document.getElementById('services'),
                order: document.getElementById('order'),
                contact: document.getElementById('contact')
            };

            let scrollTimeout;
            window.addEventListener('scroll', function() {
                clearTimeout(scrollTimeout);
                scrollTimeout = setTimeout(() => {
                    const scrollPos = window.scrollY + 120;
                    let current = 'home';

                    for (const key of sections) {
                        const el = sectionElements[key];
                        if (el) {
                            const top = el.offsetTop;
                            const height = el.offsetHeight;
                            if (scrollPos >= top && scrollPos < top + height) {
                                current = key;
                            }
                        }
                    }

                    navLinks.forEach(link => {
                        link.classList.toggle('active', link.dataset.target === current);
                    });
                }, 50);
            });

            // ----- PHONE INPUT FORMAT (opsional) -----
            const hpInput = document.getElementById('noHp');
            hpInput.addEventListener('input', function() {
                this.value = this.value.replace(/\D/g, '');
                if (this.value.length > 15) {
                    this.value = this.value.slice(0, 15);
                }
            });

            // ----- NUMBER INPUT MIN -----
            const jumlahInput = document.getElementById('jumlah');
            jumlahInput.addEventListener('input', function() {
                if (this.value < 1) this.value = 1;
            });

            // ----- SWIPE TO CLOSE TOAST (opsional) -----
            toast.addEventListener('click', function() {
                this.classList.remove('show');
                clearTimeout(toastTimer);
            });

            console.log('🚀 Zeevanna Digital @ Service siap!');
            console.log('📞 0838-1902-3700 | 0812-8552-6012');
        });
    </script>

</body>
</html>
