# Up-Study

# Оглавление
1. [Цель проекта](https://github.com/up-study/docs#1-%D1%86%D0%B5%D0%BB%D1%8C-%D0%BF%D1%80%D0%BE%D0%B5%D0%BA%D1%82%D0%B0)
2. [Описание системы](https://github.com/up-study/docs#2-%D0%BE%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B)
3. [Технологии](https://github.com/up-study/docs#3-%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%B0%D0%B3%D0%B0%D0%B5%D0%BC%D1%8B%D0%B9-%D1%81%D1%82%D1%8D%D0%BA-%D1%82%D0%B5%D1%85%D0%BD%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D0%B9)
4. [Требования к дизайну](https://github.com/up-study/docs#4-%D1%82%D1%80%D0%B5%D0%B1%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F-%D0%BA-%D0%B4%D0%B8%D0%B7%D0%B0%D0%B9%D0%BD%D1%83)

# 1. Цель проекта
Цель проекта – разработать систему образования с фриланс биржей для авторов курсов, учителей и учеников. Автор курсов, имеет доступ к конструктору курса, Создание и управление платными подписками на курсы, может нанимать учителей, при этом имеет все права учителя. Ученик оплачивая подписку попадает на платформу обучения в группу курса, подписку которого приобрел.

# 2. Описание системы
Система состоит из следующих основных функциональных блоков:

1. [Пользователи](https://github.com/up-study/docs/blob/master/content/users/)
2. [Рекрутмент](https://github.com/up-study/docs/blob/master/content/recruitment/)
3. [Система Управления Обучением](https://github.com/up-study/docs/blob/master/content/lms/)
4. [Telegram](https://github.com/up-study/docs/blob/master/content/telegram/)
5. [Мессенджер](https://github.com/up-study/docs/blob/master/content/messenger/)
6. [Уведомления](https://github.com/up-study/docs/blob/master/content/notifications/)
7. [Подписки](https://github.com/up-study/docs/blob/master/content/subscriptions/)
8. [Платежи](https://github.com/up-study/docs/blob/master/content/payments/)
9. [Скидки](https://github.com/up-study/docs/blob/master/content/discounts/)
10. [Публикации](https://github.com/up-study/docs/blob/master/content/publications/)
11. [Дорожные карты](https://github.com/up-study/docs/blob/master/content/roadmaps/)
12. [Календарь](https://github.com/up-study/docs/blob/master/content/calendar/)

# 3. Предлагаемый стэк технологий
## Бэкенд
- Python 3.11 ≥
- Django 4.1 ≥
- Django REST Framework
- Django Post Office
- PostgreSQL
- Redis
- Celery
- Aiogram

## Фронтенд
- Typescript
- React
- Tailwind

# 4. Требования к дизайну
Немного скругленные компоненты (но не круглые). Темный фон. Боковое раскрывающеесе меню справа на всех страницах.
Страница регистрации и авторизации - всплывающий компонент внутри другой страницы.
