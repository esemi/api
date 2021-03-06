# Персональный токен

Персональный токен служит для упрощения интеграции с Хантфлоу API и не требует дополнительного процесса авторизации. Наиболее частым применением может служить интеграция серверных скриптов или приложений (например, сбор откликов с корпоративного сайта) с Хантфлоу.

Для получения персонального токена вам необходимо отправив заявку на [hello@huntflow.ru](mailto:hello@huntflow.ru) с указанием пользователя Хантфлоу, для которого необходимо получить токен.

Внимание! Использование персонального токена требует более высокого уровня безопасности в вопросах его хранения и несанкционированного доступа.

### Использование персонального токена

Использование персонального токена происходит аналогично `access_token`, полученному при [OAuth 2.0 авторизации](authorization.md). 
Приложение должно использовать полученный токен при запросах, 
передавая его в заголовке в формате:

```Authorization: Bearer <personal_token>```

Для тестирования токена, удобно использовать метод [/me](user.md#me).

```http
GET /me HTTP/1.1
User-Agent: App/1.0 (incaseoffire@example.com)
Host: api.huntflow.ru
Accept: */*
Authorization: Bearer <personal_token>
```
