# string
String

Загальні вимоги:

Аутентифікація та авторизація: API повинен мати механізми для аутентифікації користувачів та авторизації їх доступу до ресурсів.
Кешування: API повинен використовувати кешування для покращення продуктивності.
Ведення журналів: API повинен записувати всі запити та відповіді для налагодження та аудиту.
Обробка помилок: API повинен чітко й зрозуміло повідомляти про помилки.
Вимоги до ресурсів:

Студенти:
GET /students: Отримати список усіх студентів.
GET /students/{id}: Отримати інформацію про студента з ідентифікатором {id}.
POST /students: Створити нового студента.
PUT /students/{id}: Оновити інформацію про студента з ідентифікатором {id}.
DELETE /students/{id}: Видалити студента з ідентифікатором {id}.
Предмети:
GET /subjects: Отримати список усіх предметів.
GET /subjects/{id}: Отримати інформацію про предмет з ідентифікатором {id}.
Викладачі:
GET /teachers: Отримати список усіх викладачів.
GET /teachers/{id}: Отримати інформацію про викладача з ідентифікатором {id}.
Заняття:
GET /lessons: Отримати список усіх занять.
GET /lessons/{id}: Отримати інформацію про заняття з ідентифікатором {id}.
Відвідування:
GET /attendances: Отримати список усіх відвідувань.
GET /attendances/{id}: Отримати інформацію про відвідування з ідентифікатором {id}.
Оцінювання:
GET /assessments: Отримати список усіх оцінок.
GET /assessments/{id}: Отримати інформацію про оцінку з ідентифікатором {id}.
Додаткові вимоги:

API повинен підтримувати фільтрацію та сортування ресурсів.
API повинен дозволяти завантажувати та вивантажувати файли.
API повинен мати документацію, що описує всі його кінцеві точки та формати даних.
Рекомендації щодо дизайну REST API
Використовую RESTful архітектурний стиль.
Назвав свої кінцеві точки ресурсів чітко й зрозуміло.
Використовую відповідні коди HTTP-статусу.
Повертаю дані в JSON-форматі.
Використовую HATEOAS для полегшення навігації по API.
Тестуйю свій API ретельно.
Приклад кінцевої точки API
Ось приклад кінцевої точки API для отримання списку всіх студентів:

GET /students

HTTP/1.1 200 OK
Content-Type: application/json

[
  {
    "id": 1,
    "name": "John Doe",
    "surname": "Doe",
    "year_of_admission": "2023",
    "course": "1",
    "speciality": "Computer Science"
  },
  {
    "id": 2,
    "name": "Jane Doe",
    "surname": "Doe",
    "year_of_admission": "2022",
    "course": "2",
    "speciality": "Mathematics"
  }
]   

Вимоги до REST API з точки зору користувача
Формат User Story:

Актор: [Роль користувача]

Хочу: [Опис того, що користувач хоче зробити]

Щоб: [Очікуваний результат]

Приклади:

Актор: Студент

Хочу: Отримати список усіх курсів

Щоб: Я міг вибрати курс, який хочу пройти.

Актор: Викладач

Хочу: Додати оцінку для студента

Щоб: Я міг відстежувати успішність студента.

Актор: Адміністратор

Хочу: Створити нового користувача

Щоб: Я міг додати нового користувача до системи.

Ролі та можливості:

Студент:

Може переглядати список усіх курсів.
Може переглядати інформацію про курс.
Може реєструватися на курси.
Може переглядати свої оцінки.
Може завантажувати навчальні матеріали.
Викладач:

Може переглядати список усіх курсів.
Може переглядати інформацію про курс.
Може створювати та редагувати курси.
Може додавати та редагувати оцінки для studentів.
Може завантажувати навчальні матеріали.
Адміністратор:

Може переглядати список усіх користувачів.
Може переглядати інформацію про користувача.
Може створювати, редагувати та видаляти користувачів.
Може скидати паролі користувачів.
REST API ресурси
На основі вимог, викладених у форматі User Story, можна сформувати REST API ресурси:

Студенти:

GET /students: Отримати список усіх studentів.
GET /students/{id}: Отримати інформацію про studentа з ідентифікатором {id}.
POST /students: Створити нового studentа.
PUT /students/{id}: Оновити інформацію про studentа з ідентифікатором {id}.
DELETE /students/{id}: Видалити studentа з ідентифікатором {id}.
Предмети:

GET /subjects: Отримати список усіх предметів.
GET /subjects/{id}: Отримати інформацію про предмет з ідентифікатором {id}.
Викладачі:

GET /teachers: Отримати список усіх викладачів.
GET /teachers/{id}: Отримати інформацію про викладача з ідентифікатором {id}.
Заняття:

GET /lessons: Отримати список усіх занять.
GET /lessons/{id}: Отримати інформацію про заняття з ідентифікатором {id}.
Відвідування:

GET /attendances: Отримати список усіх відвідувань.
GET /attendances/{id}: Отримати інформацію про відвідування з ідентифікатором {id}.
Оцінювання:

GET /assessments: Отримати список усіх оцінок.
GET /assessments/{id}: Отримати інформацію про оцінку з ідентифікатором {id}.
Додаткові ресурси:

GET /courses: Отримати список усіх курсів.
GET /courses/{id}: Отримати інформацію про курс з ідентифікатором {id}.
POST /courses: Створити новий курс.
PUT /courses/{id}: Оновити інформацію про курс з ідентифікатором {id}.
DELETE /courses/{id}: Видалити курс з ідентифікатором {id}.
Фільтрація та сортування:

API повинен підтримувати фільтрацію та сортування ресурсів за допомогою параметрів запиту.

Завантаження та вивантаження файлів:

API повинен дозволяти користувачам завантажувати та вивантажувати файли, наприклад, навчальні матеріали.

Документація:

API повинен мати документацію, що описує всі його кінцеві точки, формати даних, коди HTTP-статусу та інші важливі деталі.

Приклад опису кінцевої точки API 
openapi: 3.0.0
info:
  title: "Система управління освітою

![Схема](scheme.png)
