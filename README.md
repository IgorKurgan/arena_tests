# arena_tests

Тестовое окружение:
- Linux Ubuntu 24.04
- Mozila Firefox
- Cypress

Руководствуясь теорией тестирования сначала проведем позитивные тесты

1.Отправка формы с валидными тестовыми данными
- Перейти на сайт https://www.testograf.ru/ru/blog/feedback-form-template
- Обнаружить форму обратной связи
- В поле "Ваше имя" ввести валидное имя "Иван"
- В поле E-mail ввести валидный e-mail "ableton8989@gmail.com"
- В поле Телефон ввести валидный номер телефона 89080015160
- В поле Цель обращения в выпадающем меню выбрать Цель обрашения
- В поле Ваше сообщение ввести сообщение
- Нажать кнопку отправить
  Ожидаемый результат : на странице появится сообщение об успешной отправке "Благодарим за обращение!"

Так-как отсутствуют требования к данной форме, составим чек-лист с возможными проверками, который поможет в дальнейшем тестировщику и аналитику
разработать подробные требования к данной форме, разработать тест- план и составить тест-кейсы
    
Начнем с полей ввода:
  
1.Поле "Ваше имя"
  - Имена содержащие только буквы
  - Имена содержащие спец.символы ("Анна-Мария")
  - Ограничение по количеству вводимых символов
  - Поддержка различных языков ввода (Уточняем на какую аудиторию расчитан наш сервис)
  - Верстка (разрешение экрана,различные устройства)
  - Сообщение о незаполнении полей (валидация)
  - Невалидные данные (!"№;%:?*()_+, пробелы, пустое поле)
  - SQL инъекции
  - Tab
  - Максимальное количество знаков (граничные значения)
    
2.Поле "E-mail"
  - Поле принимает email в стандартном формате (например, "user@example.com").
  - Отображается ошибка при вводе некорректного email (например, "user@", "userexample.com").
  - Ограничение на длину e-mail
  - Пустое поле
  - SQL инъекции
  - Сообщение о незаполнении полей (валидация)
  - Верстка (разрешение экрана,различные устройства)
  - Tab
  - Максимальное количество знаков (граничные значения)

3.Поле "Телефон"
  - Поле принимает стандартные значения
  - Коды стран
  - Пустое поле
  - Максимальное количество знаков (граничные значения)
  - Tab
  - Верстка (разрешение экрана,различные устройства)

4. Поле "Цель обращения"
  - Выпадашка появилась
  - Навигация по выпадашке
  - Выбранное значение в выпадашке корректно отображается в поле после закрытия выпадашки(чекнуть все поля)
  - Верстка (разрешение экрана,различные устройства)
  - Tab

5. Поле "Ваше сообщение"
  - Установить максимальную и минимальную длинну вводимо сообщения (с аналитиком и бизнесом)
  - Ввод символов на граничныx значенияx
  - Пустое поле
  - Верстка (разрешение экрана,различные устройства)
  - Tab
  - SQL инъекции

6. Кнопка "Отправить"
   - Функционал кнопки
   - Верстка (разрешение экрана,различные устройства)
  
7. Тестирование API
   - POST
   - PUT
   - PATCH
   - DELETE
   - GET
   - позитив/негатив

8. Выборка даныых из БД.
9. Нагрузочное тестирование.
    
11. Внештатные ситуации.
- Медленное соеденение.
- Потеря связи.

12. Интеграционное тестирование.
- Смежники.
- Моки.
  
Опираясь на пирамиду тестирования
- Разработчики проводят Unit тесты
- Тестировщики проводят интеграционные тесты (возможно, операторы нашего колцентра получают данные из формы обратной связи посредством веб-хуков, интеграция с социальными сетями,
  либо хранение данных на отдельном ресурсе).
- Проведение end-to-end тестирование с помощью инструментов Postman,Cypress,Figma.

13. Составление отчета по тестированию.  
  
  
