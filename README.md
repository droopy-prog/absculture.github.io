<html lang="ru">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>АБС Культура - Промышленные теплицы и оборудование для садоводства</title>
  <link href="https://fonts.googleapis.com/css2?family=Commissioner:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <style>
    /* Сброс и базовая типографика */
    *, *::before, *::after { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: "Commissioner", "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
      line-height: 1.6;
      background: #ffffff;
      color: #212E37;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    /* Цветовая схема */
    :root {
      --dark: #212E37;
      --accent: #B5E54E;
      --neutral: #B3B3B3;
      --light-bg: #f8f9fa;
    }

    header {
      background: linear-gradient(135deg, #212E37 0%, #2a3b47 100%);
      color: #ffffff;
      padding: 20px 0;
      box-shadow: 0 4px 12px rgba(33, 46, 55, 0.15);
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 16px;
      margin-bottom: 20px;
    }
    
    .logo {
      width: 70px; /* Немного больше для логотипа */
      height: 70px;
      background: transparent;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 8px rgba(33, 46, 55, 0.2);
      padding: 4px;
      flex-shrink: 0; /* Чтобы логотип не сжимался */
    }
    
    .logo img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      border-radius: 8px;
    }
    
    .brand-text h1 {
      margin: 0;
      font-size: 24px;
      font-weight: 700;
      color: #ffffff;
    }
    
    .brand-text .tagline {
      opacity: 0.9;
      font-weight: 400;
      color: var(--accent);
    }

    /* Навигация */
    nav {
      display: flex;
      flex-wrap: wrap;
      gap: 8px 20px;
      border-top: 1px solid rgba(181, 229, 78, 0.2);
      padding-top: 16px;
    }
    
    nav a {
      color: rgba(255,255,255,0.9);
      text-decoration: none;
      font-weight: 500;
      padding: 8px 0;
      position: relative;
      transition: color 0.3s ease;
    }
    
    nav a:hover {
      color: var(--accent);
    }
    
    nav a::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--accent);
      transition: width 0.3s ease;
    }
    
    nav a:hover::after {
      width: 100%;
    }

    /* Основной контент */
    main {
      padding: 40px 0;
    }

    /* Герой секция */
    .hero {
      background: linear-gradient(135deg, var(--light-bg) 0%, #ffffff 100%);
      padding: 60px 0;
      margin-bottom: 40px;
      border-radius: 0 0 20px 20px;
    }
    
    .hero h2 {
      font-size: 2.5rem;
      font-weight: 700;
      margin: 0 0 20px 0;
      color: var(--dark);
      line-height: 1.2;
    }
    
    .hero p {
      font-size: 1.2rem;
      color: #4a5568;
      margin: 0 0 30px 0;
      max-width: 600px;
    }

    /* Сетка услуг */
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 24px;
      margin: 40px 0;
    }
    
    .service-category {
      background: #ffffff;
      border-radius: 16px;
      padding: 28px;
      box-shadow: 0 4px 20px rgba(33, 46, 55, 0.08);
      border: 1px solid rgba(179, 179, 179, 0.2);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    
    .service-category:hover {
      transform: translateY(-8px);
      box-shadow: 0 12px 40px rgba(33, 46, 55, 0.15);
    }
    
    .service-category h3 {
      color: var(--dark);
      font-size: 1.4rem;
      font-weight: 600;
      margin: 0 0 20px 0;
      padding-bottom: 12px;
      border-bottom: 3px solid var(--accent);
      display: inline-block;
    }
    
    .service-list {
      list-style: none;
      padding: 0;
      margin: 0;
    }
    
    .service-list li {
      padding: 10px 0;
      border-bottom: 1px solid rgba(179, 179, 179, 0.3);
      position: relative;
      padding-left: 24px;
      font-weight: 400;
    }
    
    .service-list li:last-child {
      border-bottom: none;
    }
    
    .service-list li::before {
      content: '✓';
      position: absolute;
      left: 0;
      color: var(--accent);
      font-weight: 700;
    }

    /* Карточки продуктов */
    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 24px;
      margin: 40px 0;
    }
    
    .card {
      background: #ffffff;
      border-radius: 12px;
      padding: 24px;
      box-shadow: 0 4px 16px rgba(33, 46, 55, 0.08);
      border: 1px solid rgba(179, 179, 179, 0.2);
      transition: all 0.3s ease;
      text-align: center;
    }
    
    .card:hover {
      transform: translateY(-6px);
      box-shadow: 0 12px 32px rgba(33, 46, 55, 0.15);
      border-color: var(--accent);
    }
    
    .card-icon {
      width: 80px;
      height: 80px;
      background: linear-gradient(135deg, var(--accent) 0%, #9bcb3a 100%);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 20px;
      font-size: 32px;
      color: var(--dark);
      font-weight: 700;
    }
    
    .card h3 {
      margin: 0 0 12px 0;
      font-size: 1.2rem;
      font-weight: 600;
      color: var(--dark);
    }
    
    .card p {
      margin: 0;
      color: #4a5568;
      font-size: 0.95rem;
      line-height: 1.5;
    }

    /* Кнопки */
    .btn {
      background: var(--accent);
      color: var(--dark);
      border: none;
      padding: 14px 32px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      font-weight: 600;
      text-decoration: none;
      display: inline-block;
      transition: all 0.3s ease;
      box-shadow: 0 4px 12px rgba(181, 229, 78, 0.3);
    }
    
    .btn:hover {
      background: #9bcb3a;
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(181, 229, 78, 0.4);
    }

    /* Футер */
    footer {
      background: var(--dark);
      color: #ffffff;
      padding: 40px 0 20px;
      margin-top: 60px;
    }
    
    .footer-content {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 40px;
      margin-bottom: 30px;
    }
    
    .footer-section h3 {
      color: var(--accent);
      margin: 0 0 20px 0;
      font-size: 1.2rem;
      font-weight: 600;
    }
    
    .footer-section p,
    .footer-section a {
      color: rgba(255,255,255,0.8);
      text-decoration: none;
      line-height: 1.6;
    }
    
    .footer-section a:hover {
      color: var(--accent);
    }
    
    .copyright {
      text-align: center;
      padding-top: 20px;
      border-top: 1px solid rgba(255,255,255,0.1);
      color: rgba(255,255,255,0.6);
      font-size: 0.9rem;
    }

    /* Адаптивность */
    @media (max-width: 768px) {
      .brand {
        flex-direction: column;
        text-align: center;
        gap: 12px;
      }
      
      .logo {
        width: 60px;
        height: 60px;
      }
      
      .hero h2 {
        font-size: 2rem;
      }
      
      .services-grid {
        grid-template-columns: 1fr;
      }
      
      .card-grid {
        grid-template-columns: 1fr;
      }
      
      nav {
        justify-content: center;
      }
    }

    @media (max-width: 480px) {
      .container {
        padding: 0 16px;
      }
      
      .hero {
        padding: 40px 0;
      }
      
      .hero h2 {
        font-size: 1.8rem;
      }
      
      .service-category,
      .card {
        padding: 20px;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <div class="brand">
        <div class="logo">
          <img src="logo.png" alt="АБС Культура">
        </div>
        <div class="brand-text">
          <h1>АБС Культура</h1>
          <div class="tagline">Комплексные решения для сельского хозяйства</div>
        </div>
      </div>
      <nav>
        <a href="#services">Услуги</a>
        <a href="#products">Оборудование</a>
        <a href="#projects">Проекты</a>
        <a href="#consulting">Консультации</a>
        <a href="#contacts">Контакты</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <h2>Профессиональные решения для современного сельского хозяйства</h2>
      <p>Полный цикл услуг: от проектирования тепличных комплексов до агротехнического сопровождения и первых продаж вашей продукции.</p>
      <a href="#contacts" class="btn">Получить консультацию</a>
    </section>

    <section id="services">
      <h2 style="font-size: 2rem; margin-bottom: 20px; color: var(--dark);">Наши услуги</h2>
      <div class="services-grid">
        <div class="service-category">
          <h3>Продажа оборудования</h3>
          <ul class="service-list">
            <li>Промышленные теплицы</li>
            <li>Ягодные туннели</li>
            <li>Оборудование для теплиц</li>
            <li>Системы орошения и комплектующие</li>
            <li>Узлы автоматического внесения удобрений</li>
            <li>Автоматика и насосное оборудование</li>
            <li>Емкости и накопители для воды</li>
            <li>Оборудование для автоматического полива</li>
          </ul>
        </div>

        <div class="service-category">
          <h3>Материалы и расходники</h3>
          <ul class="service-list">
            <li>Посадочный материал и саженцы</li>
            <li>Малообъемные грунты</li>
            <li>Материалы для шпалерных систем</li>
            <li>Комплектующие для систем орошения</li>
          </ul>
        </div>

        <div class="service-category">
          <h3>Проекты и услуги</h3>
          <ul class="service-list">
            <li>Монтаж и шеф-монтаж</li>
            <li>Проекты под ключ (с 0 до первых продаж)</li>
            <li>Агротехническое сопровождение</li>
            <li>Консультационные услуги</li>
            <li>Составление бизнес-моделей</li>
            <li>Подбор техники и оборудования</li>
            <li>Руководство по реализации проекта</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="products" style="margin-top: 60px;">
      <h2 style="font-size: 2rem; margin-bottom: 20px; color: var(--dark);">Ключевые направления</h2>
      <div class="card-grid">
        <div class="card">
          <div class="card-icon">🏭</div>
          <h3>Тепличные комплексы</h3>
          <p>Проектирование и строительство промышленных теплиц любой сложности под ключ</p>
        </div>

        <div class="card">
          <div class="card-icon">💧</div>
          <h3>Системы орошения</h3>
          <p>Комплексные решения полива и автоматического внесения удобрений</p>
        </div>

        <div class="card">
          <div class="card-icon">🌱</div>
          <h3>Агросопровождение</h3>
          <p>Полный цикл агротехнической поддержки от посадки до сбора урожая</p>
        </div>

        <div class="card">
          <div class="card-icon">📊</div>
          <h3>Бизнес-консалтинг</h3>
          <p>Разработка бизнес-моделей и сопровождение проектов до первых продаж</p>
        </div>
      </div>
    </section>

    <section id="contacts" style="margin-top: 60px; text-align: center; background: var(--light-bg); padding: 40px; border-radius: 16px;">
      <h2 style="font-size: 2rem; margin-bottom: 20px; color: var(--dark);">Готовы начать проект?</h2>
      <p style="font-size: 1.1rem; color: #4a5568; margin-bottom: 30px; max-width: 600px; margin-left: auto; margin-right: auto;">
        Свяжитесь с нами для получения подробной консультации и расчета стоимости вашего проекта
      </p>
      <a href="mailto:info@abs-culture.ru" class="btn">Написать нам</a>
    </section>
  </main>

  <footer>
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <h3>АБС Культура</h3>
          <p>Комплексные решения для современного сельского хозяйства и тепличных комплексов</p>
        </div>
        
        <div class="footer-section">
          <h3>Контакты</h3>
          <p>Email: info@abs-culture.ru</p>
          <p>Телефон: +7 (XXX) XXX-XX-XX</p>
        </div>
        
        <div class="footer-section">
          <h3>Услуги</h3>
          <p>Тепличные комплексы</p>
          <p>Системы орошения</p>
          <p>Агросопровождение</p>
        </div>
      </div>
      
      <div class="copyright">
        © 2024 АБС Культура. Все права защищены.
      </div>
    </div>
  </footer>

  <script>
    // Плавная прокрутка для навигации
    document.querySelectorAll('nav a').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const targetId = this.getAttribute('href');
        const targetElement = document.querySelector(targetId);
        
        if (targetElement) {
          targetElement.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });

    // Анимация появления элементов при скролле
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

    // Наблюдаем за карточками и секциями
    document.querySelectorAll('.service-category, .card').forEach(el => {
      el.style.opacity = '0';
      el.style.transform = 'translateY(20px)';
      el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
      observer.observe(el);
    });
  </script>
</body>
</html>
