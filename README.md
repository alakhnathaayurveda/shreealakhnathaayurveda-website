<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Shree Alakhnath Aayurveda - Premium Ayurvedic Products, Raw Herbs, Food Grains, Puja Items. GMP, ISO, FSSAI Certified.">
    <meta name="keywords" content="Ayurveda, Ayurvedic Products, Raw Herbs, Herbal Medicine, Natural Wellness">
    <meta name="author" content="Shree Alakhnath Aayurveda OPC Private Limited">
    <title>Shree Alakhnath Aayurveda - Certified Ayurvedic Products</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-green: #2d5016;
            --gold: #d4af37;
            --white: #ffffff;
            --light-gray: #f5f5f5;
            --dark-gray: #333333;
            --text-light: #666666;
            --border-light: #e0e0e0;
            --danger: #e74c3c;
            --transition: all 0.3s ease;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: var(--dark-gray);
            background-color: var(--white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        body.dark-mode {
            background-color: #0f0f0f;
            color: #e0e0e0;
        }

        header {
            background: linear-gradient(135deg, var(--primary-green) 0%, #1f3a0f 100%);
            color: var(--white);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
        }

        body.dark-mode header {
            background: linear-gradient(135deg, #1a1a1a 0%, #0d0d0d 100%);
        }

        .header-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 2rem;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 1rem;
            flex: 1;
            min-width: 0;
        }

        .logo {
            width: 55px;
            height: 55px;
            background: linear-gradient(135deg, var(--gold) 0%, #c9a227 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: var(--primary-green);
            font-size: 28px;
            flex-shrink: 0;
            box-shadow: 0 4px 12px rgba(212, 175, 55, 0.3);
        }

        .company-info {
            display: flex;
            flex-direction: column;
            gap: 0.2rem;
            min-width: 0;
        }

        .company-name {
            font-size: 20px;
            font-weight: 800;
            color: var(--white);
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            letter-spacing: 0.5px;
        }

        .tagline {
            font-size: 12px;
            color: #e8c547;
            font-style: italic;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .search-box {
            position: relative;
            width: 220px;
            display: none;
        }

        .search-box input {
            width: 100%;
            padding: 0.65rem 1.2rem;
            border: none;
            border-radius: 25px;
            background: rgba(255, 255, 255, 0.15);
            color: var(--white);
            font-size: 14px;
            outline: none;
            transition: var(--transition);
        }

        .search-box input::placeholder {
            color: rgba(255, 255, 255, 0.5);
        }

        .search-box input:focus {
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.2);
        }

        .icon-button {
            background: none;
            border: none;
            color: var(--white);
            cursor: pointer;
            font-size: 22px;
            padding: 0.6rem;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }

        .icon-button:hover {
            color: #e8c547;
            transform: scale(1.15);
            background: rgba(255, 255, 255, 0.1);
        }

        .hamburger {
            display: none;
            flex-direction: column;
            gap: 6px;
            cursor: pointer;
        }

        .hamburger span {
            width: 26px;
            height: 3px;
            background: var(--white);
            border-radius: 3px;
            transition: var(--transition);
        }

        .hamburger.active span:nth-child(1) {
            transform: rotate(45deg) translate(10px, 10px);
        }

        .hamburger.active span:nth-child(2) {
            opacity: 0;
        }

        .hamburger.active span:nth-child(3) {
            transform: rotate(-45deg) translate(7px, -7px);
        }

        nav {
            display: flex;
            align-items: center;
            flex: 2;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 0;
            width: 100%;
        }

        nav li {
            position: relative;
            display: flex;
            align-items: center;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            padding: 1rem 0.9rem;
            font-size: 14px;
            font-weight: 500;
            display: block;
            white-space: nowrap;
            transition: var(--transition);
            border-bottom: 3px solid transparent;
        }

        nav a:hover {
            color: #e8c547;
            border-bottom-color: #e8c547;
            background: rgba(255, 255, 255, 0.05);
        }

        .mobile-drawer {
            position: fixed;
            left: -400px;
            top: 0;
            width: 400px;
            height: 100vh;
            background: var(--primary-green);
            color: var(--white);
            overflow-y: auto;
            z-index: 999;
            transition: var(--transition);
            padding-top: 60px;
            box-shadow: 4px 0 20px rgba(0, 0, 0, 0.2);
        }

        body.dark-mode .mobile-drawer {
            background: #1a1a1a;
        }

        .mobile-drawer.active {
            left: 0;
        }

        .mobile-drawer ul {
            list-style: none;
            display: flex;
            flex-direction: column;
        }

        .mobile-drawer a {
            padding: 1rem 1.5rem;
            color: var(--white);
            text-decoration: none;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
        }

        .mobile-drawer a:hover {
            background: rgba(212, 175, 55, 0.15);
            color: #e8c547;
        }

        .drawer-overlay {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.5);
            z-index: 998;
            display: none;
            backdrop-filter: blur(4px);
        }

        .drawer-overlay.active {
            display: block;
        }

        .hero {
            background: linear-gradient(135deg, rgba(45, 80, 22, 0.85) 0%, rgba(31, 58, 15, 0.85) 100%);
            color: var(--white);
            padding: 6rem 1rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: radial-gradient(ellipse at center, transparent 0%, rgba(0, 0, 0, 0.3) 100%);
            pointer-events: none;
        }

        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
            animation: slideUpFade 0.8s ease-out;
        }

        @keyframes slideUpFade {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-logo {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, var(--gold) 0%, #c9a227 100%);
            border-radius: 50%;
            margin: 0 auto 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            box-shadow: 0 10px 40px rgba(212, 175, 55, 0.4);
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        .hero h1 {
            font-size: 48px;
            font-weight: 900;
            margin-bottom: 1rem;
            letter-spacing: -1px;
            text-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
        }

        .hero-subtitle {
            font-size: 18px;
            color: #e8c547;
            margin-bottom: 2rem;
            font-weight: 500;
            letter-spacing: 1px;
        }

        .hero-tagline {
            font-size: 28px;
            font-weight: 700;
            margin-bottom: 2.5rem;
            background: linear-gradient(135deg, #e8c547 0%, #fff 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border: none;
            border-radius: 50px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--gold) 0%, #c9a227 100%);
            color: var(--primary-green);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(212, 175, 55, 0.4);
        }

        .btn-secondary {
            background: transparent;
            color: var(--white);
            border: 2px solid #e8c547;
        }

        .btn-secondary:hover {
            background: #e8c547;
            color: var(--primary-green);
            transform: translateY(-3px);
        }

        main {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .page-section {
            display: none;
            animation: fadeIn 0.3s ease-in;
        }

        .page-section.active {
            display: block;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        section {
            padding: 4rem 1rem;
            border-bottom: 1px solid var(--border-light);
        }

        body.dark-mode section {
            border-bottom-color: #333;
        }

        .section-container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title {
            font-size: 42px;
            font-weight: 900;
            margin-bottom: 1rem;
            color: var(--primary-green);
            position: relative;
            padding-bottom: 1.5rem;
        }

        body.dark-mode .section-title {
            color: #e8c547;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, var(--gold) 0%, #c9a227 100%);
            border-radius: 2px;
        }

        .section-subtitle {
            font-size: 16px;
            color: var(--text-light);
            max-width: 600px;
            margin: 1rem auto;
            line-height: 1.8;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
            margin-top: 3rem;
        }

        .about-content h3 {
            font-size: 28px;
            color: var(--primary-green);
            margin-bottom: 1rem;
            font-weight: 700;
        }

        body.dark-mode .about-content h3 {
            color: #e8c547;
        }

        .about-content p {
            margin-bottom: 1rem;
            color: var(--text-light);
            line-height: 1.8;
        }

        .about-image {
            width: 100%;
            height: 400px;
            background: linear-gradient(135deg, var(--light-gray) 0%, #e8e8e8 100%);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 100px;
            color: var(--gold);
        }

        body.dark-mode .about-image {
            background: linear-gradient(135deg, #2a2a2a 0%, #1a1a1a 100%);
        }

        .founder-card {
            background: var(--white);
            border-radius: 20px;
            padding: 3rem 2rem;
            text-align: center;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
            max-width: 600px;
            margin: 2rem auto;
        }

        body.dark-mode .founder-card {
            background: #1a1a1a;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
        }

        .founder-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(212, 175, 55, 0.2);
        }

        .founder-image {
            width: 200px;
            height: 200px;
            background: linear-gradient(135deg, var(--light-gray) 0%, #e8e8e8 100%);
            border-radius: 50%;
            margin: 0 auto 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.2);
            border: 4px solid var(--gold);
        }

        body.dark-mode .founder-image {
            background: linear-gradient(135deg, #2a2a2a 0%, #1a1a1a 100%);
        }

        .founder-card h3 {
            font-size: 32px;
            color: var(--primary-green);
            margin-bottom: 0.5rem;
            font-weight: 800;
        }

        body.dark-mode .founder-card h3 {
            color: #e8c547;
        }

        .founder-title {
            font-size: 18px;
            color: var(--gold);
            margin-bottom: 1.5rem;
            font-weight: 600;
        }

        .founder-card p {
            color: var(--text-light);
            line-height: 1.8;
        }

        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .cert-item {
            background: var(--light-gray);
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            transition: var(--transition);
            border: 2px solid transparent;
        }

        body.dark-mode .cert-item {
            background: #1a1a1a;
            border-color: #333;
        }

        .cert-item:hover {
            border-color: var(--gold);
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.15);
        }

        .cert-icon {
            font-size: 60px;
            margin-bottom: 1rem;
        }

        .cert-item h4 {
            font-size: 18px;
            color: var(--primary-green);
            font-weight: 700;
        }

        body.dark-mode .cert-item h4 {
            color: #e8c547;
        }

        .cert-item p {
            font-size: 13px;
            color: var(--text-light);
            margin-top: 0.5rem;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .product-card {
            background: var(--white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: var(--transition);
        }

        body.dark-mode .product-card {
            background: #1a1a1a;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.4);
        }

        .product-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 15px 40px rgba(212, 175, 55, 0.2);
        }

        .product-image {
            width: 100%;
            height: 220px;
            background: linear-gradient(135deg, var(--light-gray) 0%, #e8e8e8 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 80px;
            position: relative;
            overflow: hidden;
        }

        body.dark-mode .product-image {
            background: linear-gradient(135deg, #2a2a2a 0%, #1a1a1a 100%);
        }

        .product-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(212, 175, 55, 0.1);
            transition: var(--transition);
            opacity: 0;
        }

        .product-card:hover .product-image::after {
            opacity: 1;
        }

        .product-content {
            padding: 2rem 1.5rem;
        }

        .product-content h3 {
            font-size: 22px;
            color: var(--primary-green);
            margin-bottom: 0.5rem;
            font-weight: 700;
        }

        body.dark-mode .product-content h3 {
            color: #e8c547;
        }

        .product-content p {
            color: var(--text-light);
            font-size: 14px;
            line-height: 1.6;
            margin-bottom: 1.5rem;
        }

        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .review-card {
            background: var(--light-gray);
            border-radius: 15px;
            padding: 2rem;
            border-left: 5px solid var(--gold);
            transition: var(--transition);
        }

        body.dark-mode .review-card {
            background: #1a1a1a;
        }

        .review-card:hover {
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }

        .review-stars {
            color: var(--gold);
            font-size: 18px;
            margin-bottom: 1rem;
        }

        .review-card p {
            color: var(--text-light);
            font-size: 15px;
            line-height: 1.8;
            margin-bottom: 1rem;
            font-style: italic;
        }

        .review-author {
            font-weight: 700;
            color: var(--primary-green);
            font-size: 16px;
        }

        body.dark-mode .review-author {
            color: #e8c547;
        }

        .review-position {
            font-size: 13px;
            color: var(--text-light);
        }

        .form-container {
            max-width: 700px;
            margin: 3rem auto;
            background: var(--light-gray);
            border-radius: 20px;
            padding: 3rem;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
        }

        body.dark-mode .form-container {
            background: #1a1a1a;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.4);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--primary-green);
            font-size: 15px;
        }

        body.dark-mode .form-group label {
            color: #e8c547;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 0.85rem 1rem;
            border: 2px solid var(--border-light);
            border-radius: 10px;
            font-family: inherit;
            font-size: 15px;
            transition: var(--transition);
            background: var(--white);
            color: var(--dark-gray);
        }

        body.dark-mode .form-group input,
        body.dark-mode .form-group select,
        body.dark-mode .form-group textarea {
            background: #2a2a2a;
            color: #e0e0e0;
            border-color: #444;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--gold);
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.1);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
        }

        .form-group.full {
            grid-column: 1 / -1;
        }

        .btn-submit {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(135deg, var(--gold) 0%, #c9a227 100%);
            color: var(--primary-green);
            border: none;
            border-radius: 10px;
            font-size: 16px;
            font-weight: 700;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(212, 175, 55, 0.3);
        }

        .btn-submit:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(212, 175, 55, 0.4);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 3rem;
            align-items: start;
        }

        .footer-contact {
            display: flex;
            gap: 1rem;
            align-items: flex-start;
            margin-bottom: 1rem;
            font-size: 15px;
        }

        .footer-contact-icon {
            font-size: 20px;
            color: var(--gold);
            flex-shrink: 0;
        }

        footer {
            background: var(--primary-green);
            color: var(--white);
            padding: 3rem 1rem 1rem;
            margin-top: 3rem;
        }

        body.dark-mode footer {
            background: #0d0d0d;
            border-top: 2px solid var(--gold);
        }

        .footer-container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2.5rem;
            margin-bottom: 2rem;
        }

        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 1.5rem;
            color: #e8c547;
            font-weight: 700;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 0.8rem;
        }

        .footer-column ul li a {
            color: rgba(255, 255, 255, 0.85);
            text-decoration: none;
            transition: var(--transition);
            font-size: 15px;
        }

        .footer-column ul li a:hover {
            color: #e8c547;
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 45px;
            height: 45px;
            background: rgba(255, 255, 255, 0.1);
            color: var(--white);
            border-radius: 50%;
            font-size: 20px;
            transition: var(--transition);
            text-decoration: none;
        }

        .social-links a:hover {
            background: var(--gold);
            color: var(--primary-green);
            transform: translateY(-5px);
        }

        .footer-divider {
            height: 1px;
            background: rgba(255, 255, 255, 0.1);
            margin: 2rem 0;
        }

        .footer-bottom {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 14px;
        }

        .footer-bottom a {
            color: rgba(255, 255, 255, 0.85);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-bottom a:hover {
            color: #e8c547;
        }

        .floating-button {
            position: fixed;
            width: 65px;
            height: 65px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            cursor: pointer;
            z-index: 500;
            transition: var(--transition);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.25);
            bottom: 100px;
            right: 20px;
            border: none;
            text-decoration: none;
        }

        .whatsapp-button {
            background: linear-gradient(135deg, #25d366 0%, #20ba5a 100%);
            color: var(--white);
        }

        .whatsapp-button:hover {
            transform: scale(1.12);
            box-shadow: 0 6px 30px rgba(37, 211, 102, 0.4);
        }

        .call-button {
            background: linear-gradient(135deg, var(--danger) 0%, #c0392b 100%);
            color: var(--white);
            bottom: 175px;
        }

        .call-button:hover {
            transform: scale(1.12);
            box-shadow: 0 6px 30px rgba(231, 76, 60, 0.4);
        }

        .scroll-top-button {
            background: linear-gradient(135deg, var(--primary-green) 0%, #1f3a0f 100%);
            color: var(--white);
            bottom: 20px;
            display: none;
        }

        .scroll-top-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 30px rgba(45, 80, 22, 0.4);
        }

        .scroll-top-button.show {
            display: flex;
        }

        .language-selector {
            position: relative;
        }

        .language-dropdown {
            position: absolute;
            top: 100%;
            right: 0;
            background: var(--primary-green);
            border: 1px solid var(--gold);
            border-radius: 5px;
            min-width: 150px;
            display: none;
            z-index: 1001;
            margin-top: 0.5rem;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
        }

        .language-dropdown.show {
            display: block;
        }

        .language-dropdown a {
            display: block;
            padding: 0.75rem 1rem;
            color: var(--white);
            text-decoration: none;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            transition: var(--transition);
        }

        .language-dropdown a:last-child {
            border-bottom: none;
        }

        .language-dropdown a:hover {
            background: rgba(212, 175, 55, 0.1);
            color: #e8c547;
        }

        @media (max-width: 1024px) {
            nav a {
                padding: 1rem 0.5rem;
                font-size: 13px;
            }

            .hero h1 {
                font-size: 40px;
            }

            .hero-tagline {
                font-size: 22px;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            nav {
                display: none;
            }

            .search-box {
                display: none !important;
            }

            .header-container {
                gap: 1rem;
            }

            .company-name {
                font-size: 16px;
            }

            .tagline {
                font-size: 10px;
            }

            .mobile-drawer {
                width: 300px;
                left: -300px;
            }

            .hero {
                padding: 4rem 1rem;
            }

            .hero h1 {
                font-size: 32px;
            }

            .hero-tagline {
                font-size: 18px;
            }

            .hero-buttons {
                gap: 1rem;
            }

            .btn {
                padding: 0.85rem 1.5rem;
                font-size: 15px;
            }

            section {
                padding: 3rem 1rem;
            }

            .section-title {
                font-size: 32px;
            }

            .certifications-grid {
                grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            }

            .products-grid {
                grid-template-columns: 1fr;
            }

            .form-container {
                padding: 2rem;
            }
        }

        @media (max-width: 480px) {
            .header-container {
                gap: 0.5rem;
            }

            .logo {
                width: 45px;
                height: 45px;
                font-size: 22px;
            }

            .company-name {
                font-size: 13px;
            }

            .icon-button {
                font-size: 18px;
                padding: 0.4rem;
            }

            .hero {
                padding: 3rem 1rem;
            }

            .hero-logo {
                width: 80px;
                height: 80px;
                font-size: 48px;
            }

            .hero h1 {
                font-size: 24px;
            }

            .hero-tagline {
                font-size: 16px;
            }

            .btn {
                padding: 0.75rem 1.2rem;
                font-size: 14px;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }

            .section-title {
                font-size: 26px;
            }

            .certifications-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .footer-grid {
                grid-template-columns: 1fr;
            }

            .footer-bottom {
                flex-direction: column;
                text-align: center;
            }

            .floating-button {
                width: 55px;
                height: 55px;
                font-size: 24px;
                bottom: 80px;
                right: 12px;
            }

            .call-button {
                bottom: 140px;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-container">
            <div class="logo-section">
                <div class="logo">🌿</div>
                <div class="company-info">
                    <div class="company-name">ALAKHNATH AAYURVEDA</div>
                    <div class="tagline">Ancient • Modern • Global</div>
                </div>
            </div>

            <div class="search-box">
                <input type="text" id="searchInput" placeholder="Search products...">
            </div>

            <nav>
                <ul id="mainMenu"></ul>
            </nav>

            <div class="header-actions">
                <button class="icon-button" id="searchToggle" title="Search">🔍</button>
                <button class="icon-button" id="darkModeToggle" title="Dark Mode">🌙</button>
                <button class="icon-button" id="languageToggle" title="Language">🌐</button>
                <a href="tel:+919713327109" class="icon-button" title="Call">📞</a>
                <a href="https://wa.me/919713327109" target="_blank" class="icon-button" title="WhatsApp">💬</a>
                <button class="icon-button hamburger" id="hamburger" title="Menu">
                    <span></span>
                    <span></span>
                    <span></span>
                </button>
            </div>

            <div class="language-selector">
                <div class="language-dropdown" id="languageDropdown">
                    <a href="#" onclick="changeLanguage('en'); return false;">English</a>
                    <a href="#" onclick="changeLanguage('hi'); return false;">हिन्दी</a>
                    <a href="#" onclick="changeLanguage('gu'); return false;">ગુજરાતી</a>
                    <a href="#" onclick="changeLanguage('mr'); return false;">मराठी</a>
                </div>
            </div>
        </div>
    </header>

    <div class="drawer-overlay" id="drawerOverlay"></div>
    <div class="mobile-drawer" id="mobileDrawer">
        <ul id="mobileMenu"></ul>
    </div>

    <main id="mainContent">
        <section class="hero page-section" id="page-home">
            <div class="hero-content">
                <div class="hero-logo">🌿</div>
                <h1>SHREE ALAKHNATH AAYURVEDA</h1>
                <p class="hero-subtitle">Certified Ayurvedic Products & Natural Wellness Solutions</p>
                <p class="hero-tagline">Ancient Ayurveda • Modern Trust • Global Reach</p>
                <div class="hero-buttons">
                    <button class="btn btn-primary" onclick="navigateTo('contact')">📞 Contact Now</button>
                    <a href="https://wa.me/919713327109" target="_blank" class="btn btn-secondary">💬 WhatsApp</a>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-company">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">About Company</h2>
                    <p class="section-subtitle">Your Trusted Source for Premium Ayurvedic Products</p>
                </div>
                <div class="about-grid">
                    <div class="about-image">🏢</div>
                    <div class="about-content">
                        <h3>Our Mission & Vision</h3>
                        <p>Shree Alakhnath Aayurveda OPC Private Limited is dedicated to preserving and promoting authentic Ayurvedic knowledge and products. With decades of expertise in traditional medicine, we bring the wisdom of ancient Ayurveda to modern consumers across the globe.</p>
                        <p>We are committed to sourcing the highest quality raw herbs, maintaining strict quality standards, and ensuring complete transparency in our supply chain. Our GMP-certified facilities, ISO certifications, and FSSAI approval ensure that every product meets international standards.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-founder">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Our Founder</h2>
                    <p class="section-subtitle">Guided by Wisdom and Passion for Traditional Ayurveda</p>
                </div>
                <div class="founder-card">
                    <div class="founder-image">🧘</div>
                    <h3>Yogi Alakhnath</h3>
                    <p class="founder-title">Founder & Managing Director</p>
                    <p>Yogi Alakhnath brings decades of experience in Ayurvedic science and traditional wellness practices. With a deep understanding of ancient Ayurvedic principles combined with modern business acumen, he has built Shree Alakhnath Aayurveda into a trusted brand.</p>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-certificate">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Certifications & Standards</h2>
                    <p class="section-subtitle">Quality Assurance and International Compliance</p>
                </div>
                <div class="certifications-grid">
                    <div class="cert-item">
                        <div class="cert-icon">✓</div>
                        <h4>GMP Certified</h4>
                        <p>Good Manufacturing Practice</p>
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon">✓</div>
                        <h4>ISO 9001:2015</h4>
                        <p>Quality Management</p>
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon">✓</div>
                        <h4>FSSAI Approved</h4>
                        <p>Food Safety License</p>
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon">✓</div>
                        <h4>MSME Registered</h4>
                        <p>Government Recognition</p>
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon">✓</div>
                        <h4>Startup India</h4>
                        <p>Recognized Startup</p>
                    </div>
                    <div class="cert-item">
                        <div class="cert-icon">✓</div>
                        <h4>Trademark</h4>
                        <p>Protected Brand</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-products">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Product Categories</h2>
                    <p class="section-subtitle">Premium Quality Products for Wellness</p>
                </div>
                <div class="products-grid">
                    <div class="product-card">
                        <div class="product-image">🌿</div>
                        <div class="product-content">
                            <h3>Ayurveda Products</h3>
                            <p>Premium ayurvedic formulations crafted from traditional recipes using pure natural ingredients.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🌾</div>
                        <div class="product-content">
                            <h3>Raw Herbs</h3>
                            <p>Authentic dried herbs sourced from trusted suppliers maintaining traditional quality standards.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🌾</div>
                        <div class="product-content">
                            <h3>Food Grains</h3>
                            <p>Organic natural food grains selected for nutritional value and purity.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🙏</div>
                        <div class="product-content">
                            <h3>Puja Items</h3>
                            <p>Sacred ceremonial items for spiritual practices and religious rituals.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🔥</div>
                        <div class="product-content">
                            <h3>Havan Items</h3>
                            <p>Ceremonial materials for Havan and Yagna rituals with traditional ingredients.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🏠</div>
                        <div class="product-content">
                            <h3>House Items</h3>
                            <p>Natural household products and eco-friendly alternatives for daily living.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🔱</div>
                        <div class="product-content">
                            <h3>Dharmic Items</h3>
                            <p>Traditional spiritual items for religious observances and practices.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-importexport">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Import & Export</h2>
                    <p class="section-subtitle">Global Distribution Network</p>
                </div>
                <div class="about-grid">
                    <div class="about-content">
                        <h3>International Trade Excellence</h3>
                        <p>We proudly serve customers across multiple continents, ensuring authentic Ayurvedic products reach wellness enthusiasts worldwide. Our efficient logistics network facilitates seamless international shipping.</p>
                        <p>With experience in navigating international regulations, quality certifications, and compliance requirements, we enable businesses globally to access premium Indian Ayurvedic products with confidence.</p>
                    </div>
                    <div class="about-image">🌍</div>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-globalpartners">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Global Partners</h2>
                    <p class="section-subtitle">Collaborative Network of Trusted Partners</p>
                </div>
                <div class="products-grid">
                    <div class="product-card">
                        <div class="product-image">🤝</div>
                        <div class="product-content">
                            <h3>International Distributors</h3>
                            <p>Strategic partnerships with distributors across countries ensuring reliable availability.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🏪</div>
                        <div class="product-content">
                            <h3>Retail Partners</h3>
                            <p>Collaborating with health stores and wellness centers worldwide.</p>
                        </div>
                    </div>
                    <div class="product-card">
                        <div class="product-image">🏢</div>
                        <div class="product-content">
                            <h3>Corporate Clients</h3>
                            <p>Serving wellness programs and health institutions globally.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-reviews">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Customer Reviews</h2>
                    <p class="section-subtitle">Trusted by Customers Worldwide</p>
                </div>
                <div class="reviews-grid">
                    <div class="review-card">
                        <div class="review-stars">⭐⭐⭐⭐⭐</div>
                        <p>"Exceptional quality products. The raw herbs are absolutely pure and customer service is outstanding."</p>
                        <div class="review-author">Rajesh Kumar</div>
                        <div class="review-position">Wellness Entrepreneur</div>
                    </div>
                    <div class="review-card">
                        <div class="review-stars">⭐⭐⭐⭐⭐</div>
                        <p>"As a retailer, I appreciate the reliable supply chain and consistent product quality."</p>
                        <div class="review-author">Priya Sharma</div>
                        <div class="review-position">Health Store Owner</div>
                    </div>
                    <div class="review-card">
                        <div class="review-stars">⭐⭐⭐⭐⭐</div>
                        <p>"The certifications and quality standards are impressive. Highly recommended."</p>
                        <div class="review-author">Dr. Anuj Patel</div>
                        <div class="review-position">Wellness Center Director</div>
                    </div>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-contact">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Get In Touch</h2>
                    <p class="section-subtitle">Contact Us for Inquiries and Partnerships</p>
                </div>
                <div class="contact-grid">
                    <div>
                        <h3 style="color: var(--primary-green); margin-bottom: 2rem; font-size: 24px; font-weight: 700;">Contact Information</h3>
                        <div class="footer-contact">
                            <span class="footer-contact-icon">📞</span>
                            <div>
                                <strong style="color: var(--primary-green);">Phone</strong>
                                <p style="color: var(--text-light); margin-top: 0.3rem;">+91 99999 99999</p>
                            </div>
                        </div>
                        <div class="footer-contact">
                            <span class="footer-contact-icon">📧</span>
                            <div>
                                <strong style="color: var(--primary-green);">Email</strong>
                                <p style="color: var(--text-light); margin-top: 0.3rem;">info@alakhnath.com</p>
                            </div>
                        </div>
                        <div class="footer-contact">
                            <span class="footer-contact-icon">📍</span>
                            <div>
                                <strong style="color: var(--primary-green);">Address</strong>
                                <p style="color: var(--text-light); margin-top: 0.3rem;">India</p>
                            </div>
                        </div>
                        <div class="footer-contact">
                            <span class="footer-contact-icon">⏰</span>
                            <div>
                                <strong style="color: var(--primary-green);">Business Hours</strong>
                                <p style="color: var(--text-light); margin-top: 0.3rem;">Mon - Sat: 9:00 AM - 6:00 PM</p>
                            </div>
                        </div>
                    </div>

                    <div class="form-container">
                        <h3 style="color: var(--primary-green); margin-bottom: 2rem; font-size: 24px; font-weight: 700;">Business Inquiry Form</h3>
                        <form id="inquiryForm">
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="name">Full Name *</label>
                                    <input type="text" id="name" name="name" required>
                                </div>
                                <div class="form-group">
                                    <label for="mobile">Mobile Number *</label>
                                    <input type="tel" id="mobile" name="mobile" required>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="email">Email Address *</label>
                                    <input type="email" id="email" name="email" required>
                                </div>
                                <div class="form-group">
                                    <label for="city">City *</label>
                                    <input type="text" id="city" name="city" required>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="form-group">
                                    <label for="state">State/Province *</label>
                                    <input type="text" id="state" name="state" required>
                                </div>
                                <div class="form-group">
                                    <label for="business">Business Type *</label>
                                    <select id="business" name="business" required>
                                        <option value="">Select Type</option>
                                        <option value="retailer">Retailer</option>
                                        <option value="wholesaler">Wholesaler</option>
                                        <option value="distributor">Distributor</option>
                                        <option value="manufacturer">Manufacturer</option>
                                        <option value="other">Other</option>
                                    </select>
                                </div>
                            </div>
                            <div class="form-group full">
                                <label for="message">Message *</label>
                                <textarea id="message" name="message" required></textarea>
                            </div>
                            <button type="submit" class="btn-submit">Submit Inquiry</button>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <section class="page-section" id="page-help">
            <div class="section-container">
                <div class="section-header">
                    <h2 class="section-title">Help Center</h2>
                    <p class="section-subtitle">We're Here to Assist You</p>
                </div>
                <div class="reviews-grid">
                    <div class="review-card">
                        <div style="font-size: 36px; margin-bottom: 1rem;">📦</div>
                        <h3 style="color: var(--primary-green); margin-bottom: 1rem;">Order Support</h3>
                        <p>Questions about orders, delivery, or tracking? Our team is ready to assist with any inquiries.</p>
                    </div>
                    <div class="review-card">
                        <div style="font-size: 36px; margin-bottom: 1rem;">🏢</div>
                        <h3 style="color: var(--primary-green); margin-bottom: 1rem;">Business Partnerships</h3>
                        <p>Interested in becoming a distributor or retailer? We welcome partnership opportunities.</p>
                    </div>
                    <div class="review-card">
                        <div style="font-size: 36px; margin-bottom: 1rem;">💬</div>
                        <h3 style="color: var(--primary-green); margin-bottom: 1rem;">WhatsApp Support</h3>
                        <p>Connect with us on WhatsApp for quick responses and immediate assistance.</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <a href="https://wa.me/919999999999" target="_blank" class="floating-button whatsapp-button" title="WhatsApp">💬</a>
    <a href="tel:+919999999999" class="floating-button call-button" title="Call">📞</a>
    <button class="floating-button scroll-top-button" id="scrollTopButton" title="Scroll to top">⬆️</button>

    <footer>
        <div class="footer-container">
            <div class="footer-grid">
                <div class="footer-column">
                    <h3>About Us</h3>
                    <p style="font-size: 15px; line-height: 1.8; color: rgba(255,255,255,0.85);">Shree Alakhnath Aayurveda OPC Private Limited - Your trusted source for authentic, GMP and ISO certified ayurvedic products with global reach.</p>
                </div>
                <div class="footer-column">
                    <h3>Products</h3>
                    <ul>
                        <li><a href="#" onclick="navigateTo('products'); return false;">Ayurveda Products</a></li>
                        <li><a href="#" onclick="navigateTo('products'); return false;">Raw Herbs</a></li>
                        <li><a href="#" onclick="navigateTo('products'); return false;">Food Grains</a></li>
                        <li><a href="#" onclick="navigateTo('products'); return false;">Puja Items</a></li>
                        <li><a href="#" onclick="navigateTo('products'); return false;">Havan Items</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Business</h3>
                    <ul>
                        <li><a href="#" onclick="navigateTo('company'); return false;">Company</a></li>
                        <li><a href="#" onclick="navigateTo('founder'); return false;">Founder</a></li>
                        <li><a href="#" onclick="navigateTo('globalpartners'); return false;">Global Partners</a></li>
                        <li><a href="#" onclick="navigateTo('importexport'); return false;">Import & Export</a></li>
                        <li><a href="#" onclick="navigateTo('certificate'); return false;">Certifications</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact & Support</h3>
                    <div class="footer-contact">
                        <span class="footer-contact-icon">📞</span>
                        <span>+91 97133 27109</span>
                    </div>
                    <div class="footer-contact">
                        <span class="footer-contact-icon">📧</span>
                        <span>info@alakhnath.com</span>
                    </div>
                    <div class="footer-contact">
                        <span class="footer-contact-icon">📍</span>
                        <span>India</span>
                    </div>
                    <h3 style="margin-top: 2rem;">Follow Us</h3>
                    <div class="social-links">
                        <a href="https://facebook.com" target="_blank" title="Facebook">f</a>
                        <a href="https://twitter.com" target="_blank" title="Twitter">𝕏</a>
                        <a href="https://instagram.com" target="_blank" title="Instagram">📷</a>
                        <a href="https://youtube.com" target="_blank" title="YouTube">▶️</a>
                    </div>
                </div>
            </div>
            <div class="footer-divider"></div>
            <div class="footer-bottom">
                <div>&copy; 2024 Shree Alakhnath Aayurveda OPC Private Limited. All Rights Reserved.</div>
                <div>
                    <a href="#" onclick="return false;">Privacy Policy</a>
                    &nbsp;|&nbsp;
                    <a href="#" onclick="return false;">Terms & Conditions</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        const menuItems = [
            { icon: '🏠', label: 'Home', route: 'home' },
            { icon: '🏢', label: 'Company', route: 'company' },
            { icon: '👤', label: 'Founder', route: 'founder' },
            { icon: '📜', label: 'Certifications', route: 'certificate' },
            { icon: '🛍️', label: 'Products', route: 'products' },
            { icon: '🚢', label: 'Import & Export', route: 'importexport' },
            { icon: '🌍', label: 'Global Partners', route: 'globalpartners' },
            { icon: '⭐', label: 'Reviews', route: 'reviews' },
            { icon: '📞', label: 'Contact', route: 'contact' },
            { icon: '🆘', label: 'Help', route: 'help' }
        ];

        document.addEventListener('DOMContentLoaded', function() {
            initializeMenu();
            loadDarkModePreference();
            setupEventListeners();
            navigateTo('home');
        });

        function initializeMenu() {
            const mainMenu = document.getElementById('mainMenu');
            const mobileMenu = document.getElementById('mobileMenu');

            menuItems.forEach(function(item) {
                const li = document.createElement('li');
                const a = document.createElement('a');
                a.href = '#';
                a.textContent = item.icon + ' ' + item.label;
                a.onclick = function(e) {
                    e.preventDefault();
                    navigateTo(item.route);
                    closeMobileMenu();
                };
                li.appendChild(a);
                mainMenu.appendChild(li);
                
                const mobileItem = li.cloneNode(true);
                mobileItem.querySelector('a').onclick = function(e) {
                    e.preventDefault();
                    navigateTo(item.route);
                    closeMobileMenu();
                };
                mobileMenu.appendChild(mobileItem);
            });
        }

        function navigateTo(route) {
            document.querySelectorAll('.page-section').forEach(function(section) {
                section.classList.remove('active');
            });
            const targetSection = document.getElementById('page-' + route);
            if (targetSection) {
                targetSection.classList.add('active');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
        }

        function setupEventListeners() {
            document.getElementById('hamburger').addEventListener('click', toggleMobileMenu);
            document.getElementById('drawerOverlay').addEventListener('click', closeMobileMenu);
            document.getElementById('darkModeToggle').addEventListener('click', toggleDarkMode);
            document.getElementById('searchToggle').addEventListener('click', toggleSearchBox);
            document.getElementById('scrollTopButton').addEventListener('click', scrollToTop);
            document.getElementById('languageToggle').addEventListener('click', toggleLanguageDropdown);
            
            window.addEventListener('scroll', updateScrollButton);
            
            const form = document.getElementById('inquiryForm');
            if (form) {
                form.addEventListener('submit', handleFormSubmit);
            }

            document.addEventListener('click', function(e) {
                const drawer = document.getElementById('mobileDrawer');
                if (drawer.classList.contains('active') && !e.target.closest('#mobileDrawer') && !e.target.closest('#hamburger')) {
                    closeMobileMenu();
                }
            });
        }

        function toggleMobileMenu() {
            document.getElementById('mobileDrawer').classList.toggle('active');
            document.getElementById('drawerOverlay').classList.toggle('active');
            document.getElementById('hamburger').classList.toggle('active');
        }

        function closeMobileMenu() {
            document.getElementById('mobileDrawer').classList.remove('active');
            document.getElementById('drawerOverlay').classList.remove('active');
            document.getElementById('hamburger').classList.remove('active');
        }

        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
            localStorage.setItem('darkMode', document.body.classList.contains('dark-mode'));
        }

        function loadDarkModePreference() {
            if (localStorage.getItem('darkMode') === 'true') {
                document.body.classList.add('dark-mode');
            }
        }

        function toggleSearchBox() {
            const searchBox = document.querySelector('.search-box');
            searchBox.style.display = searchBox.style.display === 'block' ? 'none' : 'block';
            if (searchBox.style.display === 'block') {
                document.getElementById('searchInput').focus();
            }
        }

        function toggleLanguageDropdown() {
            document.getElementById('languageDropdown').classList.toggle('show');
        }

        function changeLanguage(lang) {
            localStorage.setItem('language', lang);
            document.getElementById('languageDropdown').classList.remove('show');
            alert('Language changed to: ' + lang.toUpperCase());
        }

        function scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function updateScrollButton() {
            const button = document.getElementById('scrollTopButton');
            if (window.scrollY > 300) {
                button.classList.add('show');
            } else {
                button.classList.remove('show');
            }
        }

        function handleFormSubmit(e) {
            e.preventDefault();
            const formData = {
                name: document.getElementById('name').value,
                mobile: document.getElementById('mobile').value,
                email: document.getElementById('email').value,
                city: document.getElementById('city').value,
                state: document.getElementById('state').value,
                business: document.getElementById('business').value,
                message: document.getElementById('message').value
            };
            
            console.log('Form Data:', formData);
            alert('Thank you for your inquiry! We will contact you soon at ' + formData.mobile);
            e.target.reset();
        }

        document.addEventListener('click', function(e) {
            if (!e.target.closest('.language-selector')) {
                document.getElementById('languageDropdown').classList.remove('show');
            }
        });
    </script>
</body>
</html>
