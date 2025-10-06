Аналог Open Movie Database API.

Поддерживаемые операции:

| Метод | URL |Handler| Действие |
|---------|----------|--------|-------|
| **GET** | /v1/healthcheck | healthcheckHandler | Получение информации о состоянии и версии приложения |
| **GET**| /v1/movies      | listMoviesHandler | Получение информации о всех фильмах |
| **POST**| /v1/movies      | createMovieHandler | Добавление нового фильма |
| **GET**| /v1/movies/:id      | showMovieHandler | Получение информации о конкретном фильме |
| **PATCH**| /v1/movies/:id      | updateMovieHandler | Измениние информации о конкретном фильме по id |
| **DELETE**| /v1/movies/:id      | deleteMovieHandler | Удаление фильма по id  |
| **POST**| /v1/users    | registerUserHandler | Регистрация нового пользователя, уведомление по email |
| **PUT**| /v1/users/activated    | activateUserHandler | Подтверждение учетной записи, "активация" пользователя |
| **...**| .....      |....| Авторизация в процессе... |

База данных - PostgreSQL.

Данные принимаются / возвращаются в формате JSON.

"Особенности": rate limiting, graceful shutdown, SQL migrations.