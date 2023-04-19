jmeter
Нагрузочное тестирование с jmeter

В файле aksioma_bd.jmx нагрузочный тест запросами к базе данных.


запуск тестов из консоли jmeter -n -t .jmx -l _result.jtl

Настройка тестов для API

Добавь Thread Group (ПКМ (правая кнопка мышки) → add → Threads (users) → Thread Group)

Чтобы указать количество нагрузки в RPS, нужно добавить Constant Throughput Timer Значение задаётся в количестве запросов в минуту (ПКМ → add → Timer → Constant Throughput Timer)

Добавить запрос, который надо нагрузить ПКМ → add → Sampler → HTTP Request

Добавить HTTP Header Manager (ПКМ → add → Config Element → HTTP Header Manager)

Вытащить из ответа в переменные значение - добавляем Json Extractor (ПКМ → add → POST Processors → JSON Extractor)

Результы View Results Tree (ПКМ → Listener → View Results Tree) Summary Report (ПКМ → Listener → Summary Report)

