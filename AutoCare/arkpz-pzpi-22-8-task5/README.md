# AutoCare System

## Опис проекту
AutoCare - це система моніторингу стану автомобіля, яка використовує IoT пристрої для збору даних про критичні параметри автомобіля в реальному часі.

## Функціональність
- Моніторинг тиску в шинах
- Контроль напруги акумулятора
- Відстеження товщини гальмівних колодок
- Система сповіщень про критичні показники
- Управління обслуговуванням автомобіля
- Адміністративна панель для керування системою

## Технічний стек
### Серверна частина
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT для автентифікації
- MQTT для IoT комунікації
- Swagger для API документації

### IoT пристрій
- ESP32
- PubSubClient для MQTT
- WiFi підключення

## Встановлення та налаштування

### Попередні вимоги
- Node.js (v14 або вище)
- MongoDB
- Arduino IDE (для IoT пристрою)

### Встановлення серверної частини
1. Клонуйте репозиторій:
```bash
git clone https://github.com/NureHurovIvan/arkpz-pzpi-22-8-hurov-ivan.git
```

2. Встановіть залежності:
```bash
cd Task5/arkpz-pzpi-22-8-hurov-ivan-task5
npm install
```

3. Створіть файл .env з наступними змінними:
```env
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
PORT=5000
```

4. Запустіть сервер:
```bash
npm start
```

### Налаштування IoT пристрою
1. Відкрийте файл `sketch.ino` в Arduino IDE
2. Встановіть необхідні бібліотеки:
   - WiFi
   - PubSubClient
3. Налаштуйте параметри Wi-Fi та MQTT в коді
4. Завантажте скетч на ESP32

## API Документація
API документація доступна за адресою `http://localhost:5000/api-docs` після запуску сервера.

### Основні ендпоінти
- POST `/api/register` - Реєстрація нового користувача
- POST `/api/login` - Авторизація користувача
- GET `/api/vehicles` - Отримання списку автомобілів
- POST `/api/maintenance` - Додавання запису про обслуговування

## Безпека
- JWT автентифікація
- Хешування паролів
- Розмежування прав доступу (користувач/адмін)
- HTTPS для API запитів
- Безпечне зберігання конфіденційних даних

## Тестування
Для запуску тестів використовуйте команду:
```bash
npm test
```

## Ліцензія
MIT License

