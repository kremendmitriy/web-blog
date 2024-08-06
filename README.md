Области хранения данных:

- база данных на json-server
- BFF
- redux store

Сущности приложения:

- пользователь: БД (список пользователей), BFF (сессия текущего), redux store
- роль пользователя: БД(список ролей), BFF ( сессия пользователя с ролью), redux store (использовать роль пользователя)
- статья: БД (список статей), redux store (отображение в браузере)
- комментарии: БД(список комментариев), redux store (отображение в браузере)

Таблицы БД:

- пользователи - users: id/ login / password / registred_at / role_id / name / secondName / sex
- роли - roles: id / name
- статьи - posts: id / title / image_url / content / published_at
- комментарии - comments: id / author_id / post_id / content

Схема состояния на BFF:

- сессия текущего пользователя: login / password / role

Схема redux store:

- user: id / login / roleId
- posts: массив post: id / title / imageUrl / published_at / commentsCount
- post: id / title / imageUrl / content / published_at / comments: array comment: id / author / content / published_at
- users: array user: id / login / registeredAt / role
