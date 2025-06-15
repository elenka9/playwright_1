# [My first playwright test](https://github.com/elenka9/playwright_1/blob/main/tests/mainPage.spec.ts)

*☝️ клик, чтобы посмотреть*


## Test Automation Project


**Language:** Type Script


**About project**: Учусь писать тесты на Playwright+Type Script.


*Объект тестирования*: [HEADER главной страницы Playwright](https://playwright.dev/)


*Инструмент:*  Playwright - это библиотека Node.js для автоматизации Chromium, Firefox и WebKit с помощью одного API


1. [Первые шаги в тестах с помощью Playwright](https://github.com/elenka9/playwright_1/blob/main/tests/mainPage.spec.ts)


- применила мэтчеры:
  - toBeVisible() проверка отображения элемента
  - toContainText('Docs') проверка элемент содержит текст
  - toHaveAttribute('href', '/'); поверка атрибута href элемента
- использовала Soft Assertions в проверке кнопки "GET STARTED", которые не прерывают выполнение теста, а собирают ошибки и показывают их все сразу.
- оформила тесты в связанную группу с помощью метода describe()  ('тесты главной страницы')
- применила хук beforeEach для выполнения определенного кода (переход на страницу перед каждым тестом) перед каждым тестом в блоке describe, чтобы убрать повторяющиеся действия

2. [Модифицируем этот код, делаем его масштабируемым](https://github.com/elenka9/playwright_2/blob/main/tests/mainPage.spec.ts)

- создала интерфейс, чтобы затипизировать список элементов
- создала переменную элементы (const = elements), чтобы сделать код расширяемым и добавлять новые элементы при необходимости
- убрала повторяющиеся действия за счет метода forEach, который последовательно перебирает все элементы массива, что сокращает код
- добавила title для каждого шага с пмощью функции test.step. Она разбивает сложные тесты на более понятные шаги, улучшая читабельность и отчетность.
