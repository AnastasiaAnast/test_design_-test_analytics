# Исследовательское тестирование

- Как тестировать без требований?
- Исследовательское vs. сценарное тестирование.
- Концепция исследовательских туров Дж. Уиттакера.
- Эвристики в тестировании.

# Как тестировать без требований

Ожидание
Вся документация в наличии: полная, доступная, непротиворечивая.

Реальность

- Документации нет.
- Есть, но неполная/ непонятная, возможно есть макеты.
- Разработчики уже что-то сделали.
- Тестировать надо срочно

# Тестирование без требований

- Работать с приложением, будто вы его пользователь.
- Опираться на бизнес-процессы.
- Декомпозировать функциональность.
- Уточнить информацию у других участников разработки (разработчика).
- Использовать оракулы (прим. по методике FEW HICCUPS).

1. Familiar (известность) — ПО не воспроизводит известные проблемы других программных продуктов.
2. Explainability (объяснимость) — работа ПО понятна, пользователь может её объяснить.
3. World (мир) — ПО соответствует знаниям и фактам окружающей действительности.
4. History (история) — новая версия ПО не противоречит предыдущей.
5. Image (имидж) — ПО соответствует имиджу компании, которая его разрабатывает.
6. Comparable product (конкуренты) — ПО не хуже, чем аналогичные продукты конкурентов.
7. Claims (заявления) — ПО выполняет то, что заявляется в рекламе, пресс-релизах и так далее.
8. User Expectations (ожидания пользователя) — ПО отвечает ожиданиям людей, которые его используют.
9. Product (продукт) — все элементы ПО работают как единое целое.
10. Purpose (цель) — ПО решает ту задачу, ради которой оно создавалось.
11. Standards (стандарты) — ПО соответствует стандартам, установленным в отрасли.

- Проводить мозговой штурм.
- Применять исследовательское тестирование.

# Исследовательское VS сценарное тестирование

Исследовательское тестирование (не методика, а подход, требующий подготовки) — одновременное изучение программы, проектирование, выполнение тестов (тесты не определены заранее, не выполняются по какому-то плану).

Когда применять исследовательское тестирование?

1. Нужна быстрая обратная связь о новом продукте.
2. Нужно быстро изучить продукт.
3. Сценарное тестирование не находит баги, требует разнообразия.
4. Следует принять решение о необходимости покрытия области сценарными тестами.
5. Требований нет, они неполные / устарели.
6. Продукт маленький, и разработка тестовых сценариев займёт больше времени, чем сам процесс тестирования.

**Исследовательское**

- Нестандартные ходы выявляют нестандартные дефекты.
- Не тратится время на описание всех сценариев.
- Не нужна поддержка тестовых сценариев.
- Не наступает «эффект пестицида» (тесты перестают выявлять баги).
- Можно тестировать без требований.
- Тесты могут стать интереснее, креативнее.

**Сценарное**

- Тестирование можно планировать: тесткейсы можно распределить между тестировщиками.
- Важные кейсы гарантированно будут пройдены.
- Возможно оценить процент покрытия требований тестами.
- Тестовые сценарии можно использовать для обучения новых сотрудников.
- Тестовые сценарии помогают проводить приёмочные испытания и определять критерии готовности.

# Исследовательское тестирование — НЕ лучший вариант, если:

1. Приложение стандартизованное — банковские продукты, сложные системы CRM, ERP, любые программы с высокими рисками.
2. Интеграционное тестирование — хорошо покрыто документацией, часто автоматизируется.
3. Тестовые сценарии на аутсорсе.
4. Длительный проект — если долго не тестировать, специфика забывается, поэтому нужны тесты.

# Концепция исследовательских туров Дж. Уиттакера (книга)

Исследовательское тестирование

- Туры в бизнес-районах.
- Туры в исторических районах.
- Развлекательные туры.
- Туристические достопримечательности.
- Тур по отелям.
- Туры по злачным местам.

_Тур по путеводителю_
Цель — тестирование пользовательской документации.
Тестировщик берёт руководство пользователя, последовательно выполняет всё, что там написано. Подход вскрывает ошибки в функциональности, пользовательской документации.

_Денежный тур_
Цель — протестировать то, за что клиенты готовы заплатить, платные возможности программы.
В денежном туре проверяют маркетинговые артефакты:

- демо-режим;
- рекламные ролики;
- соответствие маркетинговой документации реальности.

_Интеллектуальный тур_
Цель — «озадачить» приложение, заставить его работать по максимуму.

- Сформировать очень сложный отчёт.
- Оформить очень большой заказ.
- Допустить максимальное количество ошибок при выполнении операции и т.д.

# Эвристики/оракулы/модели

— быстрые когнитивные способы решения проблемы / принятия решения.

Эвристики тестирования:

- чек-листы;
- чит-листы;
- мнемоники.

**Эвристика «Маша и медведь»**: Слишком много, слишком мало, в самый раз.
Применение: тестирование поля ввода.

1. Слишком много — очень длинная строка / большое число: имя из 100 букв, возраст человека — 1000 лет.
2. Слишком мало — очень короткая / пустая строки, ноль.
3. В самый раз — типичная для параметра длина строки / число: имя из 4–10 букв, возраст — 35 лет.

**Эвристика RCRCRC** релиз кандидат. Поддерживает регрессионное тестирование.

1. Recent — недавнее: новый инструментарий / починка багов.
2. Core — ключевое: главные функции, дымовое тестирование.
3. Risky — рискованное: сложная логика / недостаточность требований.
4. Configuration — конфигурационное: изменения в файлах настроек.
5. Repaired — исправленное: починка багов.
6. Chronic — хроническое: места, где баги возникают постоянно

**Эвристика FEW HICCUPS**
FEW HICCUPS — мнемоника, позволяющая запомнить ключевые слова для источников ожидаемого результата тестирования. Иногда их называют оракулами.
Оракулы особенно полезны, если спецификации нет / содержит неадекватную/неактуальную информацию.

**Личные эвристики**

1. Определить процесс, в котором используются эвристики.
2. Обдумать устойчивые шаблоны поведения.
3. Вербализовать свои действия.
4. Применять эвристики на практике. Пример изученной эвристики — правило «Что? Где? Когда?».
