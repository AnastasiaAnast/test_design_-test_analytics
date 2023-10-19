# Классы эквивалентности

- Тест-дизайн
- Классы эквивалентности, их основные принципы
- Виды классов эквивалентности
- Алгоритм определения классов эквивалентности
- Примеры

**Тест-дизайн** — этап тестирования ПО, на котором проектируются и создаются тест-кейсы (тестовые сценарии, разработка проверок).

_Техники тест-дизайна помогают обеспечить оптимальное тестовое покрытие при ограниченном кол-ве проверок_.

    Задача: протестировать форму регистрации с двумя полями: логин, пароль.
    Сколько тестов нужно, чтобы установить уровень качества?

    Интуитивно предположим:

    - позитивный сценарий (логин test, пароль test1!);
    - негативный сценарий (логин и пароль не заполнены).

    Но что, если:

    - логин уже занят;
    - в логине есть спецсимволы \*/%;
    - логин с пробелами;
    - пароль из одного символа.
      А сколько ещё внештатных ситуаций может быть? И как покрыть их все тест-кейсами? Техники тест-дизайна обеспечивают оптимальное тестовое покрытие при ограниченном количестве проверок.

## Популярные техники/методы тест-дизайна

- Классы эквивалентности (эквивалентное разделение) - _тестирование методом черного ящика_
- Граничные значения (анализ граничных значений, метод граничных значений).
- Попарное тестирование (тестовая комбинаторика, Pairwise).
- Тестирование состояний и переходов.
- Таблицы принятия решений.
- Исследовательское тестирование.
- Предугадывание ошибок.

## Классы эквивалентности и их основные принципы (тестирование методом черного ящика)

**Класс эквивалентности** — набор _входных значений_, каждое из которых _обрабатывается одинаково и приводит систему к одному результату_. Значения внутри класса обладают общими признаками, что и приводит к идентичной обработке всех данных.

Если известно, что есть группа данных, использование которых приводит систему в одно и то же состояние, то нет необходимости проверять каждое значение из этой группы отдельно.
Исключения возможны, но мы не можем проверять все данные, так что приходится прибегать к подобным допущениям.

## Виды классов эквивалентности

**Линейные (упорядоченные)** (возраст, суммы, расстояния, р-ры/объем памяти, передаваемых данных)

- значения можно упорядочить и расположить на шкале (числовой прямой);
- есть границы, где заканчивается один класс и начинается другой.

**Нелинейные (неупорядоченные)** (наборы данных: буквы, символы, названия)

- значения нельзя упорядочить на числовой прямой;
- граничных значений нет.

1. Если одно значение из класса выявит ошибку, остальные, скорее всего, тоже это сделают.
2. Если одно значение из класса не выявит ошибку, остальные, скорее всего, тоже этого не сделают.

Мы не можем знать, будет баг/нет - метод тестирования черного ящика

На классы эквивалентности можно разбить

- символы,
- длину строки,
- объём памяти,
- разрешение экрана (нелинейный КЭ),
- версии ОС, библиотек (зависит от формата),
- объём передаваемых данных.

## Алгоритм определения классов эквивалентности

1. На основе анализа _выбрать параметры_, которые влияют на результат.
2. Для каждого параметра _выделить классы эквивалентности_ (длина строки, тип вводимых символов, способ ввода, язык ввода и тп).
3. Из _каждого класса_ эквивалентности _выбрать одно значение_.
4. Обработать выбранные значение в соответствии с pairwise (при необходимости).