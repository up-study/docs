# Content
1. [Цель проекта](https://github.com/up-study/docs#1-%D1%86%D0%B5%D0%BB%D1%8C-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)
2. [Описание системы](https://github.com/up-study/docs#2-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B)
3. [Технологии](https://github.com/up-study/docs#3-%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%B0%D0%B3%D0%B0%D0%B5%D0%BC%D1%8B%D0%B9-%D1%81%D1%82%D1%8D%D0%BA-%D1%82%D0%B5%D1%85%D0%BD%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D0%B9)
4. [Требования к дизайну](https://github.com/up-study/docs#4-%D1%82%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F-%D0%BA-%D0%B4%D0%B8%D0%B7%D0%B0%D0%B9%D0%BD%D1%83)

# 1. Цель проекта
Цель проекта – разработать систему образования с фриланс биржей для авторов курсов, учителей и учеников. Автор курсов, имеет доступ к конструктору курса, Создание и управление платными подписками на курсы, может нанимать учителей, при этом имеет все права учителя. Ученик оплачивая подписку попадает на платформу обучения в группу курса, подписку которого приобрел.

# 2. Описание системы
Система состоит из следующих основных функциональных блоков:

1. Типы пользователей
2. Регистрация, аутентификация и авторизация
3. Страница редактирования
4. Домашняя страница, поиск курсов
5. Функционал для автора (LMS)
6. Функционал оплаты подписки или разового платежа
7. Функционал выплаты зп учителю автором
8. Функционал подписчика (ученика)
9. Уведомления, Календарь занятий - для учителей и учеников
10. Roadmap по курсу для ученика, с тестами
11. Телеграм бот, контролирует группы в телеграме по подписке, удаляет-добавляет пользователей.
12. Мессенджер
13. Платформа проведения лекций
14. Up-Study задачник
15. Панель Администрирования
16. Система скидок

# 2.1 Типы пользователей
Система предусматривает четыре типа пользователей системы: админ(менеджер), автор, учитель и подписчик(ученик). Автор создаёт курсы, подписки и выкладывает контент, подписчики в соответствии со своим уровнем подписки получают доступ к разрешённому для них контенту и возможно Telegram чату. Учитель может откликаться на вакансию, пройти собеседование если требуется и получить право преподавать на курсе автора.

# 2.2 Регистрация и Аутентификация
## 2.2.1 Регистрация
### 2.2.1.1 На платформе
Два обязательных поля: `email`, `username` отправляется сообщение на email с временным сгенерированным паролем. пользователь создается в бд как неактивный, ссылка на создание пароля (`password`, `repeated_password`), после которого пользователь становится активным и попадает на страницу редактирования профиля

### 2.2.1.2 Приглашение через панель администрации
Все тоже самое, что и в [2.2.2.1](), но пользователь получает права администратора

### 2.2.1.3 Приглашение от другого пользователя по ссылке
создается ссылка, связанная с пользователем который приглашает. Оба пользователя получают бенефиты, рассмотрим это позже. Ссылку нельзя менять, можно создать только одну ссылку, если ее не существует.

### 2.2.1.4 Приглашение от другого пользователя по email
Приглашая пользователя по email, происходит тоже, что в [2.2.1.3]() только ссылка отправляется по email, ссылка та же, что получаешь в пункте [2.2.1.3]()

## 2.2.2 Аутентификация
- jwt истекает через 5 минут
- jwt refresh каждые 4 минуты
- jwt refresh истекает после 7 дней оффлайн
### 2.2.2.1 С паролем
- получить jwt(json web token) при вводе username/email и пароля
### 2.2.2.1 Через соц. сеть
получить json web token при аутентификации через соц сеть (github, gmail, telegram)
# 2.3 Страница редактирования профиля
| field | type |
|-------|------|
|first name|string|
|last name|string|
|phone|string|
|birth date|date|
|sex|string-choices|

Возможные соц. сети для связки аккаунта:
- telegram (button to bind telegram account -> link to telegram bot which going to bind user)
- instagram
- github
- linkedin
- gmail
Для смены пароля – надо подтвердить старый

# 2.9 Мессенджер
- личные сообщения, группы, каналы
- папки с группами/каналами/личными сообщениями
- django-channels

# 3. Предлагаемый стэк технологий
## 3.1 Бэкенд
- Python 3.11 ≥
- Django 4.1 ≥
- Django REST Framework
- Django Post Office
- PostgreSQL
- Aiogram
- Celery
## 3.2 Фронтенд
- React
- Typescript

# 4. Требования к дизайну
Немного скругленные компоненты (но не круглые). Темный фон. Боковое раскрывающеесе меню справа на всех страницах.
Страница регистрации и авторизации - всплывающий компонент внутри другой страницы.
