# Spotify music to Telegram Bio

Автоматически обновляет биографию в Telegram, показывая текущий трек из Spotify. (Оригинал скрипта https://github.com/deadcxde/spotify-to-telegram-bio-go)

## Первый запуск

1. Уставновите [Go](https://go.dev/)
2. После скачивания скрипта, запустите терминал в этой папке и введите команду `go run main.go` 
3. Дождитесь установки нужных библиотек

### Обязательно включить VPN перед первым запуском, после авторизации он не потребуется

1. Создайте приложение в [Spotify Developer Dashboard](https://developer.spotify.com/dashboard):
   - Получите Client ID и Client Secret
   - В настройках приложения добавьте Redirect URI: `http://localhost:8080/callback`

2. Создайте приложение в [Telegram API](https://my.telegram.org/apps):
   - Получите API ID (числовой) и API Hash

3. Запустите программу. При первом запуске она попросит ввести:
   - Spotify Client ID
   - Spotify Client Secret
   - Telegram API ID
   - Telegram API Hash
   - Номер телефона в международном формате (например: +79001234567)

4. После ввода данных:
   - В консоли появится запрос кода подтверждения от Telegram (придет в приложение)
   - После потребуеться открыть ссылку в браузере для авторизации в Spotify


## Использование

- Для остановки программы нажмите Ctrl+C - оригинальная биография будет восстановлена
- Биография обновляется каждые 45 секунд (можно изменить в config/config)

## Требования

- Для работы программы необходим VPN в стране, где доступен Spotify
- Аккаунт Spotify должен быть зарегистрирован в стране, где сервис доступен
- Telegram аккаунт должен быть активен и иметь доступ к API

## Устранение неполадок

1. Если Spotify не авторизуется:
   - Убедитесь, что VPN включен
   - Проверьте правильность Client ID и Client Secret
   - Проверьте, что добавлен правильный Redirect URI

2. Если Telegram не авторизуется:
   - Проверьте правильность API ID и API Hash
   - Убедитесь, что номер телефона введен в правильном формате
   - Проверьте, что код подтверждения вводится правильно

3. Если биография не обновляется:
   - Проверьте, что в Spotify играет музыка
   - Проверьте логи на наличие ошибок


   ## Помощь
   Можно обратиться ко мне в телеграмме @b1nt1n
