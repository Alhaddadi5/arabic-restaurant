<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>مطعمنا العربي</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f9f5f0;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        header {
            background: linear-gradient(to right, #8B4513, #A0522D);
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-left: 10px;
            font-size: 32px;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80') no-repeat center center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            text-align: center;
            color: white;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
        }
        
        .hero-content {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 20px;
            margin-bottom: 30px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
        }
        
        .btn {
            display: inline-block;
            background-color: #8B4513;
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: all 0.3s ease;
            border: 2px solid #8B4513;
        }
        
        .btn:hover {
            background-color: transparent;
            color: #8B4513;
        }
        
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: #8B4513;
            font-size: 36px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: #8B4513;
            margin: 15px auto;
            border-radius: 2px;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .menu-item {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .menu-item:hover {
            transform: translateY(-10px);
        }
        
        .menu-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .menu-item-content {
            padding: 20px;
        }
        
        .menu-item h3 {
            color: #8B4513;
            margin-bottom: 10px;
            font-size: 22px;
        }
        
        .menu-item p {
            color: #666;
            margin-bottom: 15px;
        }
        
        .price {
            display: block;
            font-weight: bold;
            color: #8B4513;
            font-size: 20px;
            margin-top: 10px;
        }
        
        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }
        
        .contact-info {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .contact-info h3 {
            color: #8B4513;
            margin-bottom: 20px;
            font-size: 24px;
        }
        
        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-left: 10px;
            color: #8B4513;
            font-size: 20px;
            width: 24px;
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 16px;
        }
        
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 30px 0;
            margin-top: 60px;
        }
        
        .social-links {
            margin-bottom: 20px;
        }
        
        .social-links a {
            color: white;
            font-size: 24px;
            margin: 0 15px;
            transition: color 0.3s ease;
        }
        
        .social-links a:hover {
            color: #8B4513;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
    <!-- الهيدر -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-utensils"></i>
                    <span>مطعمنا العربي</span>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">الرئيسية</a></li>
                        <li><a href="#about">عن المطعم</a></li>
                        <li><a href="#menu">قائمة الطعام</a></li>
                        <li><a href="#contact">اتصل بنا</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- قسم الهيرو -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>أطيب المأكولات العربية الأصيلة</h1>
            <p>استمتع بتجربة فريدة من النكهات الشرقية الأصيلة في أجواء عربية مميزة</p>
            <a href="#menu" class="btn">استعرض قائمة الطعام</a>
        </div>
    </section>

    <!-- قسم عن المطعم -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">عن مطعمنا</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>مطعمنا العربي يقدم أشهى المأكولات العربية الأصيلة منذ عام 1995. نفتخر بتقديم أطباقنا التقليدية المعدة بأيدٍ خبيرة باستخدام أفضل المكونات الطازجة.</p>
                    <p>يتميز مطعمنا بالأجواء العائلية الدافئة والتصميم العربي الأصيل الذي ينقلك إلى عالم من التراث والعراقة. لدينا فريق عمل محترف يسعى دائمًا لتقديم أفضل خدمة لتجربة طعام لا تُنسى.</p>
                    <p>نقدم في مطعمنا مجموعة متنوعة من المأكولات العربية من مختلف البلدان، بما في ذلك المأكولات السعودية، اللبنانية، السورية، والمصرية.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80" alt="صالة المطعم">
                </div>
            </div>
        </div>
    </section>

    <!-- قائمة الطعام -->
    <section id="menu">
        <div class="container">
            <h2 class="section-title">قائمة الطعام</h2>
            <div class="menu-items">
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1598214886806-c87b84b7078b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1025&q=80" alt="منسف">
                    <div class="menu-item-content">
                        <h3>المنسف الأردني</h3>
                        <p>لحم ضأن مطبوخ مع الأرز واللبن العربي، يقدم مع الخبز والصنوبر.</p>
                        <span class="price">45 ريال</span>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1619840606585-e92ecc35443f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80" alt="كباب">
                    <div class="menu-item-content">
                        <h3>كباب مشاوي</h3>
                        <p>لحم ضأن مشوي على الفحم مع خلطة خاصة من البهارات العربية.</p>
                        <span class="price">38 ريال</span>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1633321702518-7feccafb94d5?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80" alt="حمص">
                    <div class="menu-item-content">
                        <h3>حمص بالطحينة</h3>
                        <p>حمص مهروس مع الطحينة وعصير الليمون وزيت الزيتون والبهارات.</p>
                        <span class="price">18 ريال</span>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1589302168068-964664d93dc0?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80" alt="فتة">
                    <div class="menu-item-content">
                        <h3>فتة</h3>
                        <p>خبز محمص مع اللبن والحمص والصنوبر وزيت الزيتون.</p>
                        <span class="price">25 ريال</span>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1613896520356-0c2a350dde2c?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80" alt="شاورما">
                    <div class="menu-item-content">
                        <h3>شاورما</h3>
                        <p>لحم دجاج أو لحم ضأن مشوي بطريقة خاصة، يقدم مع الخبز والثومية.</p>
                        <span class="price">22 ريال</span>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1512058564366-18510be2db19?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1172&q=80" alt="كنافة">
                    <div class="menu-item-content">
                        <h3>كنافة نابلسية</h3>
                        <p>حلويات عربية تقليدية محشوة بالجبنة ومرشوة بالق syrup.</p>
                        <span class="price">20 ريال</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم الاتصال -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">اتصل بنا</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>معلومات التواصل</h3>
                    <p><i class="fas fa-map-marker-alt"></i> العنوان: شارع الملك فهد، الرياض، السعودية</p>
                    <p><i class="fas fa-phone"></i> الهاتف: 0112345678</p>
                    <p><i class="fas fa-envelope"></i> البريد الإلكتروني: info@arabic-restaurant.com</p>
                    <p><i class="fas fa-clock"></i> أوقات العمل: من 12 ظهراً حتى 12 منتصف الليل</p>
                    <p><i class="fas fa-car"></i> خدمة التوصيل متاحة من الساعة 5 مساءً حتى 11 مساءً</p>
                </div>
                <div class="contact-form">
                    <h3>احجز طاولة</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">الاسم</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">رقم الهاتف</label>
                            <input type="tel" id="phone" required>
                        </div>
                        <div class="form-group">
                            <label for="date">التاريخ</label>
                            <input type="date" id="date" required>
                        </div>
                        <div class="form-group">
                            <label for="time">الوقت</label>
                            <input type="time" id="time" required>
                        </div>
                        <div class="form-group">
                            <label for="guests">عدد الأشخاص</label>
                            <input type="number" id="guests" min="1" max="20" required>
                        </div>
                        <button type="submit" class="btn">احجز الآن</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- الفوتر -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-snapchat"></i></a>
            </div>
            <p>جميع الحقوق محفوظة &copy; 2023 مطعمنا العربي</p>
        </div>
    </footer>

    <script>
        // دالة للتنقل السلس بين الأقسام
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetSection = document.querySelector(targetId);
                window.scrollTo({
                    top: targetSection.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });

        // دالة لحجز الطاولة
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('شكراً لك! تم استلام طلب حجز الطاولة وسنتصل بك خلال دقائق لتأكيد الحجز.');
            this.reset();
        });

        // دالة لإضافة تأثيرات عند التمرير
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = '#8B4513';
                header.style.boxShadow = '0 4px 12px rgba(0, 0, 0, 0.15)';
            } else {
                header.style.background = 'linear-gradient(to right, #8B4513, #A0522D)';
                header.style.boxShadow = '0 4px 12px rgba(0, 0, 0, 0.1)';
            }
        });
    </script>
</body>
</html>
