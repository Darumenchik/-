<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Помощь с компьютерами и ноутбуками</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(120deg, #89f7fe, #66a6ff);
            color: #333;
            animation: backgroundAnimation 10s infinite alternate;
        }

        @keyframes backgroundAnimation {
            0% {
                background: linear-gradient(120deg, #89f7fe, #66a6ff);
            }
            50% {
                background: linear-gradient(120deg, #ff9a9e, #fad0c4);
            }
            100% {
                background: linear-gradient(120deg, #ffecd2, #fcb69f);
            }
        }

        header {
            background-color: rgba(0, 0, 0, 0.6);
            color: white;
            padding: 20px 10px;
            text-align: center;
            border-radius: 0 0 15px 15px;
        }

        header h1 {
            margin: 0;
            font-size: 32px;
            animation: fadeIn 2s;
        }

        @keyframes fadeIn {
            0% {
                opacity: 0;
                transform: translateY(-20px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .container {
            padding: 20px;
            max-width: 1200px;
            margin: auto;
        }

        .services {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .service {
            background-color: white;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            width: 300px;
            transition: transform 0.3s, box-shadow 0.3s;
            animation: float 4s infinite;
        }

        .service:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
        }

        .service img {
            width: 50px;
            height: 50px;
            margin-bottom: 15px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
            100% {
                transform: scale(1);
            }
        }

        .service h3 {
            font-size: 22px;
            margin-bottom: 10px;
            color: #4CAF50;
        }

        .service p {
            font-size: 16px;
            color: #666;
        }

        .service button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px;
            width: 100%;
            cursor: pointer;
            border-radius: 10px;
            transition: background-color 0.3s;
        }

        .service button:hover {
            background-color: #45a049;
        }

        .reviews {
            margin-top: 40px;
            text-align: center;
        }

        .review {
            display: inline-block;
            width: 30%;
            padding: 10px;
            margin: 20px;
            background-color: #f9f9f9;
            border-radius: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .review img {
            border-radius: 50%;
            width: 60px;
            height: 60px;
        }

        .reviewer {
            font-weight: bold;
        }

        .cart {
            background-color: #fff;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            margin-top: 40px;
        }

        .cart .total {
            font-size: 20px;
            margin-top: 20px;
            font-weight: bold;
        }

        .checkout {
            margin-top: 20px;
        }

        #notification, #notification-success, #address-notification {
            display: none;
            padding: 10px;
            background-color: #f44336;
            color: white;
            margin-top: 20px;
            text-align: center;
            border-radius: 5px;
        }

        #notification-success {
            background-color: #4CAF50;
        }

        .specialists p {
            font-size: 18px;
            color: #333;
            margin: 10px 0;
        }

        .footer {
            background-color: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .footer a {
            color: #ff0;
        }

        .whatsapp-button {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #25d366;
            color: white;
            padding: 15px;
            border-radius: 50%;
            font-size: 30px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            transition: transform 0.3s;
        }

        .whatsapp-button:hover {
            transform: scale(1.1);
        }

        .captcha {
            text-align: center;
            margin-top: 20px;
        }

        .captcha input {
            font-size: 20px;
            padding: 5px;
            margin: 10px;
            width: 100px;
            text-align: center;
        }

        .captcha button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            margin-top: 10px;
            border-radius: 5px;
        }

        .captcha button:hover {
            background-color: #45a049;
        }

    </style>
</head>
<body>
    <header>
        <h1>Помощь с компьютерами и ноутбуками</h1>
    </header>

    <div class="container">
        <section class="services">
            <!-- Список программ -->
            <h2>Программы для установки</h2>
            <div class="service">
                <h3>Антивирус Kaspersky</h3>
                <p>Надежная защита вашего ПК.</p>
                <button onclick="addToCart('Антивирус Kaspersky', 3000)">Добавить в корзину (3000₸)</button>
            </div>
            <div class="service">
                <h3>Google Chrome</h3>
                <p>Быстрый и безопасный браузер.</p>
                <button onclick="addToCart('Google Chrome', 0)">Добавить в корзину (бесплатно)</button>
            </div>
            <div class="service">
                <h3>Microsoft Office</h3>
                <p>Полный офисный пакет.</p>
                <button onclick="addToCart('Microsoft Office', 12000)">Добавить в корзину (12000₸)</button>
            </div>
            <div class="service">
                <h3>Adobe Photoshop</h3>
                <p>Лучший графический редактор.</p>
                <button onclick="addToCart('Adobe Photoshop', 15000)">Добавить в корзину (15000₸)</button>
            </div>
        </section>

        <!-- Услуги: чистка и диагностика -->
        <section class="services">
            <div class="service">
                <h3>Чистка ноутбука</h3>
                <img src="https://images.app.goo.gl/ypy2kSc3UNhqjL4L6" alt="Чистка" />
                <p>Полная чистка от пыли, улучшение охлаждения.</p>
                <button onclick="addToCart('Чистка ноутбука', 5000)">Добавить в корзину (5000₸)</button>
            </div>
            <div class="service">
                <h3>Диагностика</h3>
                <img src="https://images.app.goo.gl/4feNdppmv5aK8GJj8" alt="Диагностика" />
                <p>Диагностика проблем с производительностью и железом.</p>
                <button onclick="addToCart('Диагностика', 3000)">Добавить в корзину (3000₸)</button>
            </div>
        </section>

        <!-- Корзина -->
        <div class="cart">
            <h2>Ваша корзина</h2>
            <div id="cart-items"></div>
            <div class="total">Итого: 0₸</div>
            <div class="checkout">
                <input type="text" id="card-number" placeholder="Номер карты" />
                <button onclick="checkout()">Оплатить</button>
            </div>

            <div class="captcha">
                <p>Введите цифры с экрана для подтверждения оплаты:</p>
                <input type="text" id="captcha-input" placeholder="55648" />
                <button onclick="verifyCaptcha()">Подтвердить</button>
            </div>
        </div>

        <div class="specialists">
            <h2>Наши специалисты</h2>
            <p>Арсен - Ваш лучший помощник по настройке ПК.</p>
            <p>Даурен - Специалист по улучшению производительности.</p>
            <p>Касым - Мастер по настройке и установке программ.</p>
            <p>Димаш - Профессионал по установке антивирусов и защите данных.</p>
        </div>

        <!-- Уведомления -->
        <div id="notification">Ошибка: Неправильный номер карты или недостаточно средств.</div>
        <div id="notification-success">Оплата прошла успешно! Спасибо за покупку!</div>
        <div id="address-notification">
            Райымбек батыр 283, мастер скоро приедет. Подтвердите, если готовы.
            <button onclick="confirmAddress(true)">Да</button>
            <button onclick="confirmAddress(false)">Нет</button>
        </div>
    </div>

    <footer class="footer">
        <p>&copy; 2024 Помощь с компьютерами и ноутбуками. Все права защищены.</p>
        <a href="#about">О нас</a> | <a href="mailto:dglsayra@mail.ru">Написать нам</a> | <a href="tel:+8777820110">Позвонить</a>
    </footer>

    <!-- Кнопка WhatsApp -->
    <a href="https://wa.me/8777820110" class="whatsapp-button">🟢</a>

    <script>
        const cart = [];
        let total = 0;

        function addToCart(service, price) {
            cart.push({ service, price });
            total += price;
            updateCart();
        }

        function updateCart() {
            const cartItems = document.getElementById("cart-items");
            const totalPrice = document.querySelector(".total");
            cartItems.innerHTML = cart.map(item => `<p>${item.service}: ${item.price}₸</p>`).join("");
            totalPrice.innerHTML = `Итого: ${total}₸`;

            if (total > 15000) {
                document.getElementById("notification").style.display = 'block';
                total = 0;
                cart.length = 0;
                updateCart();
            }
        }

        function checkout() {
            const cardNumber = document.getElementById("card-number").value;
            if (cardNumber === '4400556577445566' && total <= 15000) {
                document.getElementById("notification-success").style.display = 'block';
                document.getElementById("notification").style.display = 'none';
                setTimeout(() => {
                    document.getElementById("address-notification").style.display = 'block';
                }, 2000);
            } else {
                document.getElementById("notification").style.display = 'block';
                document.getElementById("notification-success").style.display = 'none';
            }
        }

        function verifyCaptcha() {
            const captchaInput = document.getElementById("captcha-input").value;
            if (captchaInput === "55648") {
                alert("Captcha подтверждена!");
            } else {
                alert("Неверный код. Попробуйте снова.");
            }
        }

        function confirmAddress(confirm) {
            if (confirm) {
                alert("Ждите 1 час, мастер приедет.");
            } else {
                alert("Оплата отменена.");
            }
        }
    </script>
</body>
</html>

