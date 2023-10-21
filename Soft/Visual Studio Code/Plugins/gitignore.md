# Расширение gitignore для кода Visual Studio

Расширение для Visual Studio Code, которое помогает вам в работе с `.gitignore` файлами.

## Характеристики

-   Добавьте локальный `.gitignore` файл, извлекая шаблоны .gitignore из репозитория [github / gitignore](https://github.com/github/gitignore)
-   Языковая поддержка `.gitignore` файлов

## Использование

Запустите палитру команд (с помощью Ctrl + Shift + P или F1) и начните вводить текст `Add gitignore`

## Настройки

### Настройки кода Visual Studio

```JavaScript
{
    // Number of seconds the list of `.gitignore` files retrieved from github will be cached
    "gitignore.cacheExpirationInterval": 3600
}
```

### Аутентифицированные запросы API GitHub

Это расширение выполняет вызовы API к [GitHub REST API](https://docs.github.com/en/rest), на которые распространяются [ограничения скорости](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#rate-limiting).

По умолчанию запросы, отправляемые в REST API GitHub, не проходят проверку подлинности. Хотя ограничение скорости для запросов, не прошедших проверку подлинности, низкое, обычно это не должно быть проблемой из-за кэширования и, скорее всего, нечастого использования этого расширения.

Если вы достигнете предела скорости (например, из-за того, что работаете внутри корпоративной сети), вы можете переключиться на [аутентифицированные запросы](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#authentication), установив `GITHUB_AUTHORIZATION` переменную среды.

#### Примеры

Использование [токена личного доступа](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#oauth2-token-sent-in-a-header):

```
export GITHUB_AUTHORIZATION='Token <oauth2-token>'
code
```

Использование [ключа OAuth2 / секретного](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#oauth2-keysecret)

```
export GITHUB_AUTHORIZATION='Basic <base65-encoded-key-secret>'
code
```