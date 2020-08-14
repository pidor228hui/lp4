### IDM multi - LP module
LP модуль позволяет работать приемнику сигналов «IDM multi» работать в любых чатах.
Так же он добавляет игнор, глоигнор, мут и алиасы.

## Аргументы запуска 
- `--config_path CONFIG_PATH` - Путь до файла с конфингом
- `--use_app_data` - Использовать папку AppData/IDM (Windows). При использовании этой настройки AppData/IDM и config_path складываются

## Структура кофигурационного файла config.json

- `tokens`            - Токены вк в количестве 3х штук. Получить можно [здесь](https://oauth.vk.com/authorize?client_id=2685278&scope=1073737727&redirect_uri=https://oauth.vk.com/blank.html&display=page&response_type=token&revoke=1)
- `secret_code`       - Секретный код дежурного. Можно получить на странице настроек дежурного в графе `секретный код`
- `service_prefixes`  - Префиксы для выполнения команд модуля ЛП (добаление в мутлист, создание алиасов и тд.)
- `self_prefixes`     - Префиксы для высылки команд для себя (аналог !с .с ...)
- `duty_prefixes`     - Префиксы для высылки команд для дежурного (аналог !д .д ...)

**! Остальные поля заполняются программно**

![](https://sun1-86.userapi.com/10hU2v5Z8sV0ZBeDGWtOn4alEdiYZy2qY4_Ajw/_BeWOFmtcdw.jpg "Пример заполнения config.json")

## Команды модуля ЛП
- `{сервисный префикс}` пинг/кинг/пиу - пинг
***
- `{сервисный префикс}` префиксы свои - просмотр своих префиксов
- `{сервисный префикс}` префиксы дежурный - просмотр префиксов для дежурного
- `{сервисный префикс}` +префикс `[свой/дежурный]` - создание префикса
- `{сервисный префикс}` -префикс `[свой/дежурный]` - удаление префикса
***
- `{сервисный префикс}` алиасы - просмотр алиасов
- `{сервисный префикс}` +алиас `{имя}` {enter} `{команда которую получает модуль ЛП}` {enter} `{команда которую отсылает модуль ЛП}`  - создание алиаса
- `{сервисный префикс}` -алиас `{имя}` - удаление алиаса
***
- `{сервисный префикс}` игнорлист - просмотр игнорлиста
- `{сервисный префикс}` +игнор `[{ссылка}/{упоминание}/{реплай}]` - добавить в игнорлист
- `{сервисный префикс}` -игнор `[{ссылка}/{упоминание}/{реплай}]` - удалить из игнорлиста
***
- `{сервисный префикс}` глоигнорлист - просмотр глоигнорлиста
- `{сервисный префикс}` +глоигнор `[{ссылка}/{упоминание}/{реплай}]` - добавить в глоигнорлист
- `{сервисный префикс}` -глоигнор `[{ссылка}/{упоминание}/{реплай}]` - удалить из глоигнорлиста
***
- `{сервисный префикс}` мутлист - просмотр мутлиста
- `{сервисный префикс}` +мут `[{ссылка}/{упоминание}/{реплай}]` - добавить в мутлист
- `{сервисный префикс}` -мут `[{ссылка}/{упоминание}/{реплай}]` - удалить из мутлиста






