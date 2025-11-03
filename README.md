<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lucklyy - 精致珠宝品牌</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #D4AF37; /* 金色 */
            --secondary-color: #000000; /* 黑色 */
            --accent-color: #FFFFFF; /* 白色 */
            --light-bg: #F8F8F8;
            --text-dark: #333333;
            --text-light: #777777;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            color: var(--text-dark);
            line-height: 1.6;
            background-color: var(--accent-color);
        }
        
        /* 导航栏 */
        header {
            background-color: var(--secondary-color);
            color: var(--accent-color);
            padding: 1rem 2rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            align-items: center;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: var(--accent-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary-color);
        }
        
        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        .lang-switch {
            background: transparent;
            color: var(--accent-color);
            border: 1px solid var(--primary-color);
            padding: 0.4rem 0.8rem;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: all 0.3s;
        }
        
        .lang-switch:hover {
            background-color: var(--primary-color);
            color: var(--secondary-color);
        }
        
        /* 英雄区域 */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--accent-color);
            padding: 0 1rem;
        }
        
        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        
        .hero-content p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary-color);
            color: var(--secondary-color);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 4px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
        }
        
        .btn:hover {
            background-color: var(--accent-color);
            transform: translateY(-3px);
        }
        
        /* 公司简介 */
        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary-color);
            display: inline-block;
        }
        
        .section-title h2:after {
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            background-color: var(--primary-color);
            margin: 0.5rem auto;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* 产品展示 */
        .products {
            background-color: var(--light-bg);
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background-color: var(--accent-color);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
        }
        
        .product-image {
            height: 250px;
            overflow: hidden;
        }
        
        .product-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-image img {
            transform: scale(1.1);
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-info h3 {
            margin-bottom: 0.5rem;
            color: var(--secondary-color);
        }
        
        .product-info p {
            color: var(--text-light);
            margin-bottom: 1rem;
        }
        
        .price {
            font-weight: bold;
            color: var(--primary-color);
            font-size: 1.2rem;
        }
        
        /* 未来展望 */
        .vision-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .vision-content p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }
        
        /* 留言系统 */
        .contact {
            background-color: var(--light-bg);
        }
        
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--accent-color);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .form-submit {
            text-align: center;
        }
        
        /* 页脚 */
        footer {
            background-color: var(--secondary-color);
            color: var(--accent-color);
            padding: 3rem 2rem;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .footer-column h3 {
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }
        
        .footer-column p, .footer-column a {
            color: #ccc;
            margin-bottom: 0.8rem;
            display: block;
            text-decoration: none;
        }
        
        .footer-column a:hover {
            color: var(--primary-color);
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            margin-top: 3rem;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #999;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--secondary-color);
                flex-direction: column;
                padding: 1rem 0;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 0;
                text-align: center;
                padding: 0.8rem 0;
            }
            
            .mobile-menu {
                display: block;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .section {
                padding: 3rem 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- 导航栏 -->
    <header>
        <nav class="navbar">
            <div class="logo">Lucklyy</div>
            <ul class="nav-links">
                <li><a href="#home" data-lang="home">首页</a></li>
                <li><a href="#about" data-lang="about">关于我们</a></li>
                <li><a href="#products" data-lang="products">产品展示</a></li>
                <li><a href="#vision" data-lang="vision">未来展望</a></li>
                <li><a href="#contact" data-lang="contact">留言咨询</a></li>
                <li>
                    <button class="lang-switch" id="langSwitch">EN</button>
                </li>
            </ul>
            <div class="mobile-menu">
                <i class="fas fa-bars"></i>
            </div>
        </nav>
    </header>

    <!-- 英雄区域 -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1 data-lang="heroTitle">Lucklyy 珠宝</h1>
            <p data-lang="heroDesc">精致工艺与永恒设计的完美融合，为您打造独一无二的奢华体验</p>
            <a href="#products" class="btn" data-lang="exploreBtn">探索产品</a>
        </div>
    </section>

    <!-- 公司简介 -->
    <section class="section" id="about">
        <div class="section-title">
            <h2 data-lang="aboutTitle">关于我们</h2>
        </div>
        <div class="about-content">
            <div class="about-text">
                <h3 data-lang="brandStory">Lucklyy 品牌故事</h3>
                <p data-lang="aboutText1">Lucklyy 成立于2010年，是一家专注于高端珠宝设计与制造的品牌。我们秉承"精致工艺与永恒设计"的理念，致力于为每一位客户打造独特而珍贵的珠宝作品。</p>
                <p data-lang="aboutText2">我们的设计师团队来自世界各地，拥有丰富的创意和精湛的工艺，每一件作品都经过精心设计和严格的质量控制，确保达到最高标准。</p>
                <p data-lang="aboutText3">多年来，Lucklyy 已经成为高端珠宝市场的领导者之一，我们的产品远销全球30多个国家和地区，深受各界名流和珠宝爱好者的喜爱。</p>
            </div>
            <div class="about-image">
                <img src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Lucklyy珠宝工作室">
            </div>
        </div>
    </section>

    <!-- 产品展示 -->
    <section class="section products" id="products">
        <div class="section-title">
            <h2 data-lang="productsTitle">产品展示</h2>
        </div>
        <div class="product-grid">
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="永恒之恋戒指">
                </div>
                <div class="product-info">
                    <h3 data-lang="product1Title">永恒之恋戒指</h3>
                    <p data-lang="product1Desc">采用顶级钻石与铂金打造，象征永恒不变的爱情。</p>
                    <div class="price">¥9.9</div>
                </div>
            </div>
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="璀璨星辰项链">
                </div>
                <div class="product-info">
                    <h3 data-lang="product2Title">璀璨星辰项链</h3>
                    <p data-lang="product2Desc">灵感来自夜空中的繁星，展现优雅与神秘的气质。</p>
                    <div class="price">¥3.7</div>
                </div>
            </div>
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="皇家荣耀手链">
                </div>
                <div class="product-info">
                    <h3 data-lang="product3Title">皇家荣耀手链</h3>
                    <p data-lang="product3Desc">融合古典与现代设计元素，彰显尊贵与品味。</p>
                    <div class="price">¥19.8</div>
                </div>
            </div>
            <div class="product-card">
                <div class="product-image">
                    <img src="https://images.unsplash.com/photo-1594576722512-582d321f7a2a?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="海洋之心耳环">
                </div>
                <div class="product-info">
                    <h3 data-lang="product4Title">海洋之心耳环</h3>
                    <p data-lang="product4Desc">蓝宝石与钻石的完美结合，如同海洋深处的珍宝。</p>
                    <div class="price">¥7,200,000</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 未来展望 -->
    <section class="section" id="vision">
        <div class="section-title">
            <h2 data-lang="visionTitle">未来展望</h2>
        </div>
        <div class="vision-content">
            <p data-lang="visionText1">在未来的发展中，Lucklyy 将继续秉承"精致工艺与永恒设计"的品牌理念，不断探索创新，将传统工艺与现代科技完美结合。</p>
            <p data-lang="visionText2">我们计划在未来三年内，在全球开设50家精品店，将Lucklyy的独特设计带给更多珠宝爱好者。同时，我们将加大对可持续发展和环保材料的研发投入，致力于成为珠宝行业的环保先锋。</p>
            <p data-lang="visionText3">我们相信，通过不懈的努力和创新，Lucklyy将成为全球领先的珠宝品牌，为世界各地的客户带来更多精美绝伦的珠宝作品。</p>
        </div>
    </section>

    <!-- 留言系统 -->
    <section class="section contact" id="contact">
        <div class="section-title">
            <h2 data-lang="contactTitle">留言咨询</h2>
        </div>
        <div class="contact-form">
            <form id="contactForm">
                <div class="form-group">
                    <label for="name" data-lang="nameLabel">姓名</label>
                    <input type="text" id="name" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="email" data-lang="emailLabel">邮箱</label>
                    <input type="email" id="email" class="form-control" required>
                </div>
                <div class="form-group">
                    <label for="phone" data-lang="phoneLabel">电话</label>
                    <input type="tel" id="phone" class="form-control">
                </div>
                <div class="form-group">
                    <label for="message" data-lang="messageLabel">留言内容</label>
                    <textarea id="message" class="form-control" required></textarea>
                </div>
                <div class="form-submit">
                    <button type="submit" class="btn" data-lang="submitBtn">提交留言</button>
                </div>
            </form>
            <div id="formMessage" style="display:none; margin-top:1rem; padding:1rem; background:#e8f5e9; border-radius:4px; text-align:center;">
                感谢您的留言，我们会尽快与您联系！
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="footer-content">
            <div class="footer-column">
                <h3 data-lang="footerBrand">Lucklyy 珠宝</h3>
                <p data-lang="footerDesc">精致工艺与永恒设计的完美融合，为您打造独一无二的奢华体验。</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-weixin"></i></a>
                    <a href="#"><i class="fab fa-weibo"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                </div>
            </div>
            <div class="footer-column">
                <h3 data-lang="contactUs">联系我们</h3>
                <p><i class="fas fa-map-marker-alt"></i> <span data-lang="address">广州职业技术大学西区学生宿舍区</span></p>
                <p><i class="fas fa-phone"></i> 110-119-120</p>
                <p><i class="fas fa-envelope"></i> <span data-lang="email">四个入@lucklyy.com</span></p>
            </div>
            <div class="footer-column">
                <h3 data-lang="quickLinks">快速链接</h3>
                <a href="#home" data-lang="home">首页</a>
                <a href="#about" data-lang="about">关于我们</a>
                <a href="#products" data-lang="products">产品展示</a>
                <a href="#vision" data-lang="vision">未来展望</a>
                <a href="#contact" data-lang="contact">留言咨询</a>
            </div>
        </div>
        <div class="copyright">
            <p data-lang="copyright">&copy; 2023 Lucklyy 珠宝品牌. 保留所有权利.</p>
        </div>
    </footer>

    <script>
        // 语言数据
        const translations = {
            zh: {
                home: "首页",
                about: "关于我们",
                products: "产品展示",
                vision: "未来展望",
                contact: "留言咨询",
                heroTitle: "Lucklyy 珠宝",
                heroDesc: "精致工艺与永恒设计的完美融合，为您打造独一无二的奢华体验",
                exploreBtn: "探索产品",
                aboutTitle: "关于我们",
                brandStory: "Lucklyy 品牌故事",
                aboutText1: "Lucklyy 成立于2010年，是一家专注于高端珠宝设计与制造的品牌。我们秉承'精致工艺与永恒设计'的理念，致力于为每一位客户打造独特而珍贵的珠宝作品。",
                aboutText2: "我们的设计师团队来自世界各地，拥有丰富的创意和精湛的工艺，每一件作品都经过精心设计和严格的质量控制，确保达到最高标准。",
                aboutText3: "多年来，Lucklyy 已经成为高端珠宝市场的领导者之一，我们的产品远销全球30多个国家和地区，深受各界名流和珠宝爱好者的喜爱。",
                productsTitle: "产品展示",
                product1Title: "永恒之恋戒指",
                product1Desc: "采用顶级钻石与铂金打造，象征永恒不变的爱情。",
                product2Title: "璀璨星辰项链",
                product2Desc: "灵感来自夜空中的繁星，展现优雅与神秘的气质。",
                product3Title: "皇家荣耀手链",
                product3Desc: "融合古典与现代设计元素，彰显尊贵与品味。",
                product4Title: "海洋之心耳环",
                product4Desc: "蓝宝石与钻石的完美结合，如同海洋深处的珍宝。",
                visionTitle: "未来展望",
                visionText1: "在未来的发展中，Lucklyy 将继续秉承'精致工艺与永恒设计'的品牌理念，不断探索创新，将传统工艺与现代科技完美结合。",
                visionText2: "我们计划在未来三年内，在全球开设50家精品店，将Lucklyy的独特设计带给更多珠宝爱好者。同时，我们将加大对可持续发展和环保材料的研发投入，致力于成为珠宝行业的环保先锋。",
                visionText3: "我们相信，通过不懈的努力和创新，Lucklyy将成为全球领先的珠宝品牌，为世界各地的客户带来更多精美绝伦的珠宝作品。",
                contactTitle: "留言咨询",
                nameLabel: "姓名",
                emailLabel: "邮箱",
                phoneLabel: "电话",
                messageLabel: "留言内容",
                submitBtn: "提交留言",
                footerBrand: "Lucklyy 珠宝",
                footerDesc: "精致工艺与永恒设计的完美融合，为您打造独一无二的奢华体验。",
                contactUs: "联系我们",
                address: "广州职业技术大学西区学生宿舍区",
                email: "四个入@lucklyy.com",
                quickLinks: "快速链接",
                copyright: "&copy; 2023 Lucklyy 珠宝品牌. 保留所有权利."
            },
            en: {
                home: "Home",
                about: "About Us",
                products: "Products",
                vision: "Vision",
                contact: "Contact",
                heroTitle: "Lucklyy Jewelry",
                heroDesc: "Perfect fusion of exquisite craftsmanship and timeless design, creating unique luxury experiences for you",
                exploreBtn: "Explore Products",
                aboutTitle: "About Us",
                brandStory: "Lucklyy Brand Story",
                aboutText1: "Founded in 2010, Lucklyy is a brand specializing in high-end jewelry design and manufacturing. We adhere to the philosophy of 'Exquisite Craftsmanship and Timeless Design', committed to creating unique and precious jewelry pieces for every customer.",
                aboutText2: "Our design team comes from around the world, with rich creativity and superb craftsmanship. Each piece is carefully designed and undergoes strict quality control to ensure the highest standards.",
                aboutText3: "Over the years, Lucklyy has become one of the leaders in the high-end jewelry market. Our products are exported to more than 30 countries and regions worldwide, loved by celebrities and jewelry enthusiasts from all walks of life.",
                productsTitle: "Our Products",
                product1Title: "Eternal Love Ring",
                product1Desc: "Crafted with top-grade diamonds and platinum, symbolizing eternal and unchanging love.",
                product2Title: "Starry Night Necklace",
                product2Desc: "Inspired by the stars in the night sky, showcasing elegant and mysterious temperament.",
                product3Title: "Royal Glory Bracelet",
                product3Desc: "Blending classical and modern design elements, highlighting nobility and taste.",
                product4Title: "Ocean Heart Earrings",
                product4Desc: "Perfect combination of sapphire and diamond, like treasures from the deep ocean.",
                visionTitle: "Future Vision",
                visionText1: "In future development, Lucklyy will continue to adhere to the brand philosophy of 'Exquisite Craftsmanship and Timeless Design', constantly exploring innovation and perfectly combining traditional craftsmanship with modern technology.",
                visionText2: "We plan to open 50 boutiques worldwide in the next three years, bringing Lucklyy's unique designs to more jewelry enthusiasts. At the same time, we will increase investment in sustainable development and eco-friendly materials, striving to become an environmental pioneer in the jewelry industry.",
                visionText3: "We believe that through unremitting efforts and innovation, Lucklyy will become a globally leading jewelry brand, bringing more exquisite jewelry pieces to customers around the world.",
                contactTitle: "Contact Us",
                nameLabel: "Name",
                emailLabel: "Email",
                phoneLabel: "Phone",
                messageLabel: "Message",
                submitBtn: "Submit Message",
                footerBrand: "Lucklyy Jewelry",
                footerDesc: "Perfect fusion of exquisite craftsmanship and timeless design, creating unique luxury experiences for you.",
                contactUs: "Contact Us",
                address: "West Campus Student Dormitory Area, Guangzhou Vocational and Technical University",
                email: "contact@lucklyy.com",
                quickLinks: "Quick Links",
                copyright: "&copy; 2023 Lucklyy Jewelry Brand. All rights reserved."
            }
        };

        // 当前语言
        let currentLang = 'zh';

        // 语言切换功能
        document.getElementById('langSwitch').addEventListener('click', function() {
            currentLang = currentLang === 'zh' ? 'en' : 'zh';
            updateLanguage();
            this.textContent = currentLang === 'zh' ? 'EN' : '中文';
        });

        // 更新页面语言
        function updateLanguage() {
            const elements = document.querySelectorAll('[data-lang]');
            elements.forEach(element => {
                const key = element.getAttribute('data-lang');
                if (translations[currentLang][key]) {
                    if (element.tagName === 'INPUT' || element.tagName === 'TEXTAREA') {
                        element.setAttribute('placeholder', translations[currentLang][key]);
                    } else {
                        element.innerHTML = translations[currentLang][key];
                    }
                }
            });
        }

        // 移动端菜单切换
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('.nav-links').classList.toggle('active');
        });
        
        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // 关闭移动端菜单
                document.querySelector('.nav-links').classList.remove('active');
            });
        });
        
        // 表单提交处理
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // 这里可以添加表单验证
            
            // 模拟表单提交成功
            document.getElementById('contactForm').style.display = 'none';
            document.getElementById('formMessage').style.display = 'block';
            
            // 更新成功消息语言
            const successMsg = document.getElementById('formMessage');
            successMsg.textContent = currentLang === 'zh' 
                ? '感谢您的留言，我们会尽快与您联系！' 
                : 'Thank you for your message. We will contact you soon!';
            
            // 在实际应用中，这里可以使用第三方服务如Formspree来提交表单
            // 例如: fetch('https://formspree.io/f/your-form-id', {
            //     method: 'POST',
            //     headers: {
            //         'Content-Type': 'application/json'
            //     },
            //     body: JSON.stringify({
            //         name: document.getElementById('name').value,
            //         email: document.getElementById('email').value,
            //         phone: document.getElementById('phone').value,
            //         message: document.getElementById('message').value
            //     })
            // })
        });
        
        // 导航栏滚动效果
        window.addEventListener('scroll', function() {
            if (window.scrollY > 100) {
                document.querySelector('header').style.padding = '0.5rem 2rem';
            } else {
                document.querySelector('header').style.padding = '1rem 2rem';
            }
        });
    </script>
</body>
</html>
