Аналог Open Movie Database API.

Поддерживаемые операции:

| Метод | URL | Необходимое разрешение |Handler| Действие |
|---------|----------|--------|--------|-------|
| **GET** | /v1/healthcheck | - | healthcheckHandler | Получение информации о состоянии и версии приложения |
| **GET**| /v1/movies      | movies:read | listMoviesHandler | Получение информации о всех фильмах |
| **POST**| /v1/movies      | movies:write | createMovieHandler | Добавление нового фильма |
| **GET**| /v1/movies/:id      | movies:read | showMovieHandler | Получение информации о конкретном фильме |
| **PATCH**| /v1/movies/:id      | movies:write | updateMovieHandler | Измениние информации о конкретном фильме по id |
| **DELETE**| /v1/movies/:id      | movies:write | deleteMovieHandler | Удаление фильма по id  |
| **POST**| /v1/users    | - | registerUserHandler | Регистрация нового пользователя, уведомление по email |
| **PUT**| /v1/users/activated    | - | activateUserHandler | Подтверждение учетной записи, "активация" пользователя |
| **POST**| /v1/tokens/authentication    | - | createAuthenticationTokenHandler | Генерация нового токена аутентификации |


База данных - PostgreSQL.

Данные принимаются / возвращаются в формате JSON.

"Особенности": rate limiting, graceful shutdown, SQL migrations, permission-based authorization.