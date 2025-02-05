# План автоматизации тестирования сценария перехода к форме записи и заполнения формы на сайте Нетологии

## 1. Перечень автоматизируемых сценариев

### Сценарии перехода к форме записи:

**Сценарий 1**: Переход через меню «Каталог курсов»
1. Открытие главной страницы сайта
2. Навигация через меню «Каталог курсов»
3. Переход на страницу профессии «Инженер по тестированию»
4. Прокрутка страницы до формы записи
   
_**Ожидаемый результат**_: Страница профессии «Инженер по тестированию» открыта, форма записи отображается.

**Сценарий 2**: Переход через контент на главной странице
1. Открытие главной страницы сайта.
2. Поиск и использование ссылки или баннера, ведущего на страницу профессии «Инженер по тестированию».
3. Прокрутка страницы до формы записи.
   
_**Ожидаемый результат**_: Страница профессии «Инженер по тестированию» открыта, форма записи отображается.

**Сценарий 3**: Переход через кнопку «Записаться»
1. Открытие страницы профессии «Инженер по тестированию».
2. Нажатие кнопки «Записаться» для перехода к форме записи.

_**Ожидаемый результат**_: Страница профессии «Инженер по тестированию» открыта, форма записи отображается.

### Сценарии заполнения формы:

**Сценарий 4**: Заполнение всех обязательных полей валидными данными

**Шаги**:
1. Ввод имени (например, «Иван»).
2. Ввод телефона (например, «+79012345678»).
4. Ввод электронной почты (например, «ivanov@mail.ru»).

_**Ожидаемый результат**_: Форма успешно заполняется, все поля проходят валидацию, кнопка «Записаться» активируется.

  **Сценарий 5**: Заполнение формы с невалидным именем

**Шаги**:
1. Ввод имени с недопустимым форматом(например, «????»).
2. Ввод телефона (например, «+79012345678»).     
3. Ввод электронной почты (например, «ivanov@mail.ru»).

_**Ожидаемый результат**_: Кнопка «Записаться» остаётся неактивной, выводятся ошибки валидации для полей с неверным форматом.

 **Сценарий 6**: Заполнение формы с невалидным номером телефона

**Шаги**:
1. Ввод имени (например, «Иван»).
2. Ввод телефона с недопустимым форматом (например, «123456»).
3. Ввод электронной почты (например, «ivanov@mail.ru»).

_**Ожидаемый результат**_: Кнопка «Записаться» остаётся неактивной, выводятся ошибки валидации для полей с неверным форматом.

 **Сценарий 7**: Заполнение формы с невалидной электронной почтой

**Шаги**:
1. Ввод имени (например, «Иван»).
2. Ввод телефона (например, «+79012345678»). 
3. Ввод электронной почты с недопустимым форматом(например, «ivanov»).

_**Ожидаемый результат**_: Кнопка «Записаться» остаётся неактивной, выводятся ошибки валидации для полей с неверным форматом.

**Сценарий 8**: Оставление поля имени пустым

**Шаги**:
1. Оставить поле имени пустым.
2. Ввод телефона (например, «+79012345678»).  
3. Ввод электронной почты (например, «ivanov@mail.ru»).

_**Ожидаемый результат**_: Кнопка «Записаться» неактивна, появляется сообщение об ошибке с просьбой заполнить обязательные поля.

**Сценарий 9**: Оставление поля телефон пустым

**Шаги**:
1. Ввод имени (например, «Иван»).
2. Оставить поле телефона пустым.
3. Ввод электронной почты (например, «ivanov@mail.ru»).

_**Ожидаемый результат**_: Кнопка «Записаться» неактивна, появляется сообщение об ошибке с просьбой заполнить обязательные поля.

**Сценарий 10**: Оставление поля электронной почты пустым

**Шаги**:
1. Ввод имени (например, «Иван»).
2. Ввод телефона (например, «+79012345678»).  
3. Оставить поле электронной почты пустым.

_**Ожидаемый результат**_: Кнопка «Записаться» неактивна, появляется сообщение об ошибке с просьбой заполнить обязательные поля.

## 2. Перечень используемых инструментов с обоснованием выбора
- **Язык программирования**: Java.
    - Применим на основе опыта, полученного в рамках курса. Хорошо подходит для автоматизации тестирования веб-приложений.

- **Selenide**:
  - Используется для автоматизации взаимодействия с веб-страницами. Обеспечивает лаконичный API для написания тестов.
  - Преимущества: Автоматическое управление браузером, простота в использовании.

- **JUnit**:
  - Фреймворк для написания и выполнения тестов, организации структуры тестов и отчётов.
  - Преимущества: Хорошая интеграция с другими инструментами, простота в настройке.

- **Maven/Gradle**:
  - Используются для управления зависимостями и сборки проекта. Maven обеспечит управление зависимостями и интеграцию с CI/CD, Gradle — гибкость в настройке.

- **Allure**:
  - Для генерации наглядных отчетов о выполнении тестов.
  - Преимущества: Создаёт отчёты с подробными шагами выполнения тестов, с возможностью добавления скриншотов.

- **CI (например, Appveyor)**:
  - Для автоматического выполнения тестов при каждом обновлении проекта. Поддержка параллельного выполнения тестов и отчетности.

## 3. Перечень необходимых разрешений, данных и доступов

- **Доступ к публичным страницам сайта Нетологии**: Необходим для выполнения тестов без авторизации.
- **Технические данные о форме записи**: Необходимы для точного заполнения полей формы (список обязательных полей, допустимые форматы для каждого поля).

## 4. Перечень и описание возможных рисков при автоматизации

- **Изменения на сайте**:
  - Изменения в структуре или элементах страницы могут привести к сбоям в тестах.
  - Меры: Регулярные проверки актуальности элементов и обновлений на сайте.

- **Нестабильность окружения**:
  - Проблемы с доступом к сайту или сетевыми задержками могут привести к ошибкам выполнения тестов.
  - Меры: Настройка повторных попыток выполнения тестов и мониторинг доступности сервера.

- **Ошибки в тестах**:
  - Неверная логика тестов может привести к ложным срабатываниям (например, пропущены проверяемые поля).
  - Меры: Регулярная проверка тестов, включая их прохождение вручную перед автоматизацией.

- **Зависимость от внешних инструментов**:
  - Проблемы с настройкой или устареванием используемых инструментов.
  - Меры: Регулярное обновление инструментов и зависимостей проекта.

## 5. Перечень необходимых специалистов для автоматизации

- **Инженер по автоматизации тестирования**:
  - Разработка и поддержка автоматизированных тестов.
  - Необходимые компетенции: опыт работы с Java, Selenide, JUnit, Maven/Gradle, Allure, CI.

## 6. Интервальная оценка с учётом рисков в часах

- **Анализ требований и планирование**: 1 ч
- **Разработка тестов для сценариев перехода** (включая настройку инструментов и окружения): 3-5 ч
- **Разработка тестов для сценариев заполнения формы** (включая описание данных): 2-4 ч
- **Тестирование и отладка автоматизированных тестов**: 2-4 ч
- **Документация и отчетность**: 1-2 ч

**Общая оценка**: 9-16 часов

