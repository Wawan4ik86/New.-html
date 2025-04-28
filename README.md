<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Студия красоты волос Наталии Сазоновой - профессиональный уход с помощью кератина и ботокса">
    <title>Студия красоты волос Наталии Сазоновой</title>
    <style>
        :root {
            --primary-color: #c23030;
            --secondary-color: #de8f6d;
            --background-image: url('https://images.unsplash.com/photo-1522337360788-8b13dee7a37e');
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Arial', sans-serif;
            color: #16171a;
            line-height: 1.6;
            background: var(--background-image) fixed;
            background-size: cover;
            background-position: center;
            min-height: 100vh;
        }

        .overlay {
            background-color: rgba(0, 0, 0, 0.5);
            min-height: 100vh;
        }

        header {
            background: linear-gradient(135deg, #9a9c9c, var(--primary-color));
            color: white;
            padding: 2rem 0;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
        }

        .container {
            width: 85%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        h1 {
            font-size: 2.8rem;
            margin: 0;
            text-align: center;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
        }

        .tagline {
            font-style: italic;
            font-size: 1.1rem;
            text-align: center;
            margin: 0.5rem 0;
        }

        .nav-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin: 2.5rem 0;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 30px;
            background: var(--secondary-color);
            color: white;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            font-size: 1rem;
            position: relative;
            overflow: hidden;
        }

        .btn:hover {
            background: #c5f5f8;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .active-btn {
            background: var(--primary-color);
            font-weight: bold;
        }

        .content-section {
            padding: 2.5rem;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 15px;
            margin: 2rem 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            display: none;
        }

        .active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .booking-calendar {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .day-slot {
            background: white;
            padding: 1.2rem;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.1);
        }

        .day-name {
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .time-slot {
            display: block;
            padding: 0.8rem;
            margin: 0.5rem 0;
            background: #a89698;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.2s ease;
            color: white;
        }

        .time-slot:hover {
            background: #e5c5c5;
            transform: scale(1.02);
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .gallery img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.3s ease;
            box-shadow: 0 3px 15px rgba(0, 0, 0, 0.1);
        }

        .gallery img:hover {
            transform: scale(1.03);
        }

        .review {
            background: #f5f5f5;
            padding: 1.5rem;
            border-left: 4px solid #5a5c5c;
            margin: 1.5rem 0;
            border-radius: 0 8px 8px 0;
        }

        .review-author {
            font-style: italic;
            color: #666;
            margin-top: 0.5rem;
        }

        .contacts-section {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-top: 2rem;
        }

        footer {
            background: #5a5c5c;
            color: white;
            padding: 2rem 0;
            margin-top: 4rem;
            text-align: center;
        }

        @media (max-width: 768px) {
            .container {
                width: 95%;
            }

            h1 {
                font-size: 2rem;
            }

            .contacts-section {
                grid-template-columns: 1fr;
            }

            .gallery img {
                height: 250px;
            }
        }
    </style>
</head>
<body>
    <div class="overlay">
        <header>
            <div class="container">
                <h1>Студия красоты волос Наталии Сазоновой</h1>
                <p class="tagline">Профессиональный уход с помощью кератина и ботокса</p>
            </div>
        </header>

        <div class="container">
            <nav class="nav-buttons">
                <a href="#" class="btn active-btn" onclick="showSection('booking')">Запись</a>
                <a href="#" class="btn" onclick="showSection('reviews')">Отзывы</a>
                <a href="#" class="btn" onclick="showSection('gallery')">Галерея</a>
                <a href="#" class="btn" onclick="showSection('contacts')">Контакты</a>
            </nav>

            <!-- Секция записи -->
            <section id="booking" class="content-section active">
                <h2>Запись на процедуру</h2>
                <div class="booking-calendar">
                    <div class="day-slot">
                        <div class="day-name">Понедельник</div>
                        <div class="time-slots">
                            <span class="time-slot">10:00</span>
                            <span class="time-slot">12:30</span>
                            <span class="time-slot">15:00</span>
                        </div>
                    </div>
                    <div class="day-slot">
                        <div class="day-name">Вторник</div>
                        <div class="time-slots">
                            <span class="time-slot">10:00</span>
                            <span class="time-slot">12:30</span>
                            <span class="time-slot">15:00</span>
                        </div>
                    </div>
                    <div class="day-slot">
                        <div class="day-name">Среда</div>
                        <div class="time-slots">
                            <span class="time-slot">10:00</span>
                            <span class="time-slot">12:30</span>
                            <span class="time-slot">15:00</span>
                        </div>
                    </div>
                    <div class="day-slot">
                        <div class="day-name">Четверг</div>
                        <div class="time-slots">
                            <span class="time-slot">10:00</span>
                            <span class="time-slot">12:30</span>
                            <span class="time-slot">15:00</span>
                        </div>
                    </div>
                    <div class="day-slot">
                        <div class="day-name">Пятница</div>
                        <div class="time-slots">
                            <span class="time-slot">10:00</span>
                            <span class="time-slot">12:30</span>
                            <span class="time-slot">15:00</span>
                        </div>
                    </div>
                    <div class="day-slot">
                        <div class="day-name">Суббота</div>
                        <div class="time-slots">
                            <span class="time-slot">10:00</span>
                            <span class="time-slot">12:30</span>
                            <span class="time-slot">15:00</span>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Секция отзывов -->
            <section id="reviews" class="content-section">
                <h2>Отзывы клиентов</h2>
                <div class="review">
                    <p>"Лучшая процедура для волос! Результат превзошел все ожидания..."</p>
                    <p class="review-author">- Анна, 29 лет</p>
                </div>
                <div class="review">
                    <p>"После процедуры волосы стали шелковистыми и гладкими!"</p>
                    <p class="review-author">- Мария, 32 года</p>
                </div>
            </section>

            <!-- Галерея работ -->
            <section id="gallery" class="content-section">
                <h2>Наши работы</h2>
                <div class="gallery">
                    <img src="images/keratin-treatment.jpg" alt="Результат кератинового восстановления">
                    <img src="images/botox-hair.jpg" alt="Результат ботокса для волос">
                    <img src="images/hair-care.jpg" alt="Процедура ухода">
                    <img src="images/keratin-result-1.jpg" alt="Кератиновое выпрямление волос">
                    
                </div>
            </section>

            <!-- Контакты -->
            <section id="contacts" class="content-section">
                <h2>Контакты</h2>
                <div class="contacts-section">
                    <div>
                        <h3>Адрес салона</h3>
                        <p>г. Ижевск, ул. Николая Шишкина, д. 11/1, кв. 1</p>
                        <h3>Телефон</h3>
                        <p>+7 (950) 153-62-38</p>
                    </div>
                    <div>
                        <h3>Часы работы</h3>
                        <p>Пн-Пт: 10:00 - 17:00</p>
                        <p>Сб: 11:00 - 16:00</p>
                        <p>Вс: выходной</p>
                    </div>
                </div>
            </section>
        </div>

        <footer>
            <div class="container">
                <p>© 2023 Студия восстановления волос Наталии Сазоновой. Все права защищены.</p>
                <p>ИП Сазонова Н. С. ОГРНИП 1234567890123</p>
            </div>
        </footer>
    </div>

    <script>
        function showSection(sectionId) {
            // Убираем активный класс со всех кнопок
            document.querySelectorAll('.btn').forEach(btn => {
                btn.classList.remove('active-btn');
            });
            
            // Добавляем активный класс текущей кнопке
            event.currentTarget.classList.add('active-btn');

            // Скрываем все секции
            document.querySelectorAll('.content-section').forEach(section => {
                section.classList.remove('active');
            });

            // Показываем выбранную секцию
            const section = document.getElementById(sectionId);
            section.classList.add('active');
            section.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }

        // Обработчики для слотов времени
        document.querySelectorAll('.time-slot').forEach(slot => {
            slot.addEventListener('click', function() {
                alert(`Выбрано время: ${this.textContent}\n\nДля подтверждения записи мы свяжемся с вами в течение 15 минут.`);
            });
        });
    </script>
</body>
</html>
