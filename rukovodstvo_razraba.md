Проект: «Пицца кота Стафчика» 

Общая информация



Проект представляет собой frontend-приложение интернет-магазина пиццы, написанное на:



HTML

CSS

Vanilla JavaScript



Архитектура проекта простая и не использует backend или сторонние библиотеки.



&#x20;Структура проекта

pizza

│

├── index.html          # Главная страница

├── order.html          # Страница оформления заказа

├── README.md

│

└── images/             # Изображения проекта

&#x20;   ├── fon.jpg

&#x20;   ├── bg.jpg

&#x20;   ├── pizzamarg.jpg

&#x20;   ├── pizzapeper.jpg

&#x20;   ├── pizzagav.jpg

&#x20;   ├── pizzasir.jpg

&#x20;   ├── pizzamaso.jpg

&#x20;   ├── pizzaveg.jpg

&#x20;   ├── pizzarib.jpg

&#x20;   └── pizzasecret.jpg

Архитектура проекта



Проект состоит из двух основных страниц:



Файл	Назначение

index.html	Каталог пицц и корзина

order.html	Оформление заказа

Работа с меню пицц



Все пиццы хранятся в массиве:



const pizzas = \[

&#x20;   {

&#x20;       id: 1,

&#x20;       name: "Мурчащая Маргарита",

&#x20;       originalName: "Purring Margherita",

&#x20;       description: "Описание",

&#x20;       price: 450,

&#x20;       image: "images/pizzamarg.jpg"

&#x20;   }

];

&#x20;Добавление новой пиццы



Чтобы добавить новую пиццу:



Поместите изображение в папку images/

Добавьте объект в массив pizzas



Пример:



{

&#x20;   id: 9,

&#x20;   name: "Новая пицца",

&#x20;   originalName: "New Pizza",

&#x20;   description: "Описание новой пиццы",

&#x20;   price: 600,

&#x20;   image: "images/newpizza.jpg"

}

🛒 Система корзины



Корзина хранится в:



localStorage



Ключ:



cart



Пример структуры:



\[

&#x20; {

&#x20;   "id": 1,

&#x20;   "name": "Маргарита",

&#x20;   "price": 450,

&#x20;   "quantity": 2

&#x20; }

]

🔧 Основные функции

addToCart(pizzaId)



Добавляет товар в корзину.



addToCart(1);

removeFromCart(pizzaId)



Удаляет товар из корзины.



updateQuantity(pizzaId, change)



Изменяет количество товара.



Пример:



updateQuantity(1, 1);

saveCart()



Сохраняет корзину в localStorage.



displayPizzas()



Генерирует карточки пицц на главной странице.



Система скидок и доставки



Основная логика находится в функции:



calculateDiscount(distance, subtotal)

Логика скидок

if (distance < 3) {

&#x20;   discountPercent = 15;

}

else if (distance >= 3 \&\& distance < 5) {

&#x20;   discountPercent = 5;

}

Бесплатная доставка

if (subtotal >= 1500) {

&#x20;   deliveryCost = 0;

}

&#x20;Стилизация



Все стили находятся внутри <style> в HTML-файлах.



Основные блоки:

Класс	Назначение

.hero	Главный баннер

.pizza-card	Карточка пиццы

.cart-sidebar	Боковая корзина

.order-grid	Сетка оформления заказа

⚠️ Возможные проблемы

Изображения не отображаются



Проверьте:



наличие файлов в папке images

правильность путей

Корзина не работает



Проверьте:



включён ли localStorage

нет ли ошибок в консоли браузера

🔒 Ограничения проекта



Проект не содержит:



backend;

базы данных;

реальной оплаты;

авторизации;

API.



Все данные работают только в браузере пользователя.



Идеи для развития

Backend



Можно подключить:



Node.js + Express

PHP

Django

База данных



Подойдут:



MySQL

PostgreSQL

MongoDB

Дополнительный функционал

Возможные улучшения:

личный кабинет;

история заказов;

фильтр пицц;

поиск;

тёмная тема;

анимации;

онлайн-оплата;

Telegram-бот.

&#x20; Рекомендации по разработке

Использовать:

VS Code

Live Server

Chrome DevTools



