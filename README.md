# Job search project
# Технічне завдання (ТЗ)  

### 1. Загальний опис проєкту  
Мета проєкту — створення веб-додатку, який інтегрується з API Robota.ua (https://api.robota.ua/swagger/ui/index#/) для відображення списку компаній та їхніх вакансій. Користувач зможе переглядати компанії на головній сторінці, обирати конкретну компанію та отримувати детальну інформацію про неї разом із переліком доступних вакансій.

---

### 2. Функціональні вимоги  

#### 2.1. Головна сторінка  
- **Перелік компаній**:  
  - Відображення у вигляді карток або таблиці.  
  - Кожна картка/рядок містить:  
    - Назва компанії.  
    - Логотип (якщо доступний через API).  
    - Короткий опис (якщо є).  
  - Клік на картку/рядок перенаправляє на сторінку компанії.  
- **Пошук та фільтрація**:  
  - Поле пошуку за назвою компанії (текстове введення).  
  - Фільтр за галуззю (якщо API надає категорії).  
- **Пагінація**:  
  - Відображення 10-20 компаній на сторінку.  
  - Кнопки "Попередня" та "Наступна" для навігації.  

#### 2.2. Сторінка компанії  
- **Інформація про компанію**:  
  - Назва компанії (заголовок).  
  - Логотип (зображення, якщо є).  
  - Опис компанії (текстовий блок).  
  - Контактні дані (сайт, email, якщо доступно).  
- **Перелік вакансій**:  
  - Список у вигляді карток або таблиці.  
  - Кожна вакансія містить:  
    - Назва вакансії.  
    - Локація (якщо є).  
    - Тип зайнятості (повна/часткова, якщо є).  
    - Короткий опис.  
    - Посилання на деталі (якщо API повертає URL).  
- **Сортування**:  
  - Випадаючий список із опціями: "За датою" / "За назвою".  

#### 2.3. Інтеграція з API  
- Використання ендпоінтів API Robota.ua для отримання даних.  
- Обробка відповідей і відображення у відповідних компонентах.   

---

### 3. Нефункціональні вимоги  
- **Інтерфейс**:  
  - Чистий, мінімалістичний дизайн.  
  - Адаптивність для десктопів (мін. 1024px) та мобільних пристроїв (макс. 768px).    
- **Безпека**:   
  - Обробка помилок (повідомлення типу "Сервіс тимчасово недоступний").  
- **Технології**:  
  - Frontend: Vanila JS, CSS.   

---

### 4. Структура проєкту  
1. **Головна сторінка**:  
   - URL: `/`.  
   - Компоненти: список компаній, пошук, фільтри, пагінація.  
2. **Сторінка компанії**:  
   - URL: `/company/:id`.  
   - Компоненти: інформація про компанію, список вакансій, сортування.  

---

### 5. Очікуваний результат  
- Головна сторінка з інтерактивним списком компаній.  
- Сторінка компанії з детальною інформацією та вакансіями.  
- Зручний пошук, фільтрація та сортування.  

---

### 6. Мокапи інтерфейсу  

#### 6.1. Головна сторінка  
**Опис мокапу**:  
- **Шапка**: Логотип додатку зліва, поле пошуку посередині (ширина ~300px), кнопка "Фільтри" праворуч.  
- **Основний контент**:  
  - Сітка карток (3 у рядку для десктопу, 1 для мобільного).  
  - Картка компанії:  
    - Логотип (100x100px).  
    - Назва (жирний шрифт, 16px).  
    - Короткий опис (12px, до 50 символів).  
- **Футер**: Пагінація (кнопки "1, 2, 3..." та "Наступна").  

#### 6.2. Сторінка компанії  
**Опис мокапу**:  
- **Шапка**: Назва компанії (24px, жирний), кнопка "Назад" зліва.  
- **Ліва колонка (30%)**:  
  - Логотип (150x150px).  
  - Опис (текстовий блок, до 500 символів).  
  - Посилання на сайт (якщо є).  
- **Права колонка (70%)**:  
  - Заголовок "Вакансії" (20px).  
  - Випадаючий список "Сортувати: За датою / За назвою".  
  - Список вакансій (картки):  
    - Назва (16px).  
    - Локація та тип (12px).  
    - Короткий опис (до 100 символів).  
    - Кнопка "Деталі" (посилання).  
- **Мобільна версія**: Колонки стають вертикальними.  

### 8. Додаткові зауваження  
- Якщо API потребує авторизації, додати поле для API-ключа в конфігурацію.  
- У разі відсутності даних про компанії, використати мокові дані для тестування.  

---

