### В данном репозитории размещен возможный вариант решения следующей задачи:

## Домашнее задание к лекции 9.«Работа с библиотекой requests, http-запросы»
## Задача №2
У Яндекс.Диска есть очень удобное и простое API. Для описания всех его методов существует [Полигон](https://yandex.ru/dev/disk/poligon/). Нужно написать программу, которая принимает на вход путь до файла на компьютере и сохраняет на Яндекс.Диск с таким же именем.

1. Все ответы приходят в формате json;
1. Загрузка файла по ссылке происходит с помощью метода put и передачи туда данных;
1. Токен можно получить кликнув на полигоне на кнопку "Получить OAuth-токен".

HOST: [https://cloud-api.yandex.net:443/](https://cloud-api.yandex.net:443/)

*Важно*: Токен публиковать в github не нужно, переменную для токена нужно оставить пустой!

Шаблон для программы

```python
class YaUploader:
    def __init__(self, token: str):
        self.token = token

    def upload(self, file_path: str):
        """Метод загружает файлы по списку file_list на яндекс диск"""
        # Тут ваша логика
        # Функция может ничего не возвращать


if __name__ == '__main__':
    # Получить путь к загружаемому файлу и токен от пользователя
    path_to_file = ...
    token = ...
    uploader = YaUploader(token)
    result = uploader.upload(path_to_file)
```
