# lab28-ponomarencko

# Games API

Простой REST API для управления коллекцией видеоигр, разработанный на ASP.NET Core. Позволяет добавлять, просматривать, обновлять и удалять игры, а также отмечать избранные titles.

## 🚀 Запуск проекта

Для запуска приложения выполните следующую команду в терминале из корневой директории проекта:

```bash
dotnet run
```

## Таблица всех маршрутов

| Метод | | Маршрут | | Описание | |Cтатус|
| Get | |`/api/games`| |Получить все игры| |200|
| Get | |`/api/games/{id}`| |Получить игру по id| |200 / 404|
| Get | |`/api/games`| |Добавить игру| |201|
| Get | |`/api/games/{id}`| |Удалить игру| |204 / 404|

## Примеры curl-команд для каждого маршрута

# Получить все игры

```
curl -X GET http://localhost:5000/api/games
```

## Получить игру по ID (например, ID = 1)

```
curl -X GET http://localhost:5000/api/games/1
```

## Добавить новую игру

```
curl -X POST http://localhost:5000/api/games \
     -H "Content-Type: application/json" \
     -d '{"name": "The Witcher 3", "genre": "RPG", "price": 29.99}'
```

## Удалить игру по ID (например, ID = 1)

```
curl -X DELETE http://localhost:5000/api/games/1
```
