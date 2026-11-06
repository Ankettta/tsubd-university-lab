# ТСУБД — учебные материалы

Материалы для практических занятий по базам данных и PostgreSQL.


**Репозиторий с материалами:** https://github.com/Ankettta/tsubd-university-lab

## Что понадобится

- PostgreSQL (сервер базы данных) — [официальная страница загрузки](https://www.postgresql.org/download/).
- pgAdmin 4 (графический клиент) — [официальная страница загрузки](https://www.pgadmin.org/download/).
- `psql` (консольный клиент; обычно доступен при установке PostgreSQL с Command Line Tools).
- Git и аккаунт GitHub — для сдачи домашних заданий: [установка Git](https://git-scm.com/downloads).

## Как начать первую практику

1. На этой странице нажмите **Code → Download ZIP** и распакуйте архив.
2. Откройте папку [`data/`](data/) — там находятся пять CSV-файлов учебного университета:
   - `university_departments.csv`
   - `university_instructors.csv`
   - `university_students.csv`
   - `university_courses.csv`
   - `university_enrollments.csv`
3. Откройте pgAdmin и подключитесь к локальному PostgreSQL (обычно `localhost`, порт `5432`, пользователь `postgres`; пароль — тот, что вы задали при установке).
4. Создайте базу `university_lab` либо откройте её, если она уже существует.
5. В Query Tool **для базы `university_lab`** запустите файл [`sql/01_create_tables.sql`](sql/01_create_tables.sql) — он создаёт схему `university` и таблицы, но не решает задания за вас.
6. Импортируйте CSV в созданные таблицы по инструкции [`docs/import_guide.md`](docs/import_guide.md). Порядок: `departments → instructors → students → courses → enrollments`.
7. Проверьте, что данные появились, и приступайте к заданиям, которые выдаются на занятии. **SQL-запросы к данным пишете самостоятельно.**

## Материалы по курсу

- [Как сдавать домашние задания через GitHub](docs/github_homework_flow.pdf) — инструкция с командами, ветками и Pull Request.
- [Итоговый проект / экзамен](docs/exam.md) — предварительная информация; даты и окончательные критерии будут объявлены отдельно.
- [Инструкция по импорту CSV](docs/import_guide.md).

## Как сдавать задания

Каждый студент работает в **своём приватном репозитории**, не отправляет решения в этот общий репозиторий с датасетом! Для каждого домашнего задания используется отдельная ветка (`hw1`, `hw2` и т. д.) и Pull Request на проверку. Подробности — в [инструкции](docs/github_homework_flow.pdf).

> Не публикуйте пароли, персональные данные, конфигурационные секреты и файлы, не относящиеся к заданию.
# tsubd-university-lab
