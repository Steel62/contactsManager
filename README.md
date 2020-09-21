## Contacts Manager (Менеджер контактов)
### Описание
Небольшой менеджер контактов, позволяющий хранить, добавлять, редактировать список Ваших контактов.
Приложение написано в рамках тестового задания на позицию frontend разработчика, поэтому
backend реализован минимально необходимым.

Frontend реализован на стеке React+Redux. 

В качестве backend использован фреймворк Express, на котором реализован минимальный REST API,
необходимый для работы приложения. Express запускается на порте 3001.

Для пользования приложением требуется авторизация пользователя. Так как backend выполнен минимальным
и служит заглушкой полноценного API, то на стороне backend создана единственная валидная учетная запись
```
userName: admin
password: 111
```
После авторизации frontend получает токен и записывает его в Local Storage. Дальнейшие
запросы к backend происходят с использованием секретного токена. Хранение токена
в Local Storage позволяет пользователю оставаться авторизованным при повтороном заходе
на страницу приложения. Сброс токена происходит после нажатия на кнопку _Выход_ в личном кабинете.

Установка приложения выполняется стандартной командой 

`npm install`

Запуск приложения прозводится командой

`npm start`

Эта команда, используя библиотеку concurrently, запускает одновременно и frontend и 
backend.