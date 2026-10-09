# Проверка CI
## Событие, ветка и SHA
https://github.com/buster16788/pm03-day07/pull/1
## Красный запуск
URL: https://github.com/buster16788/pm03-day07/pull/1/changes/50d408746a4dce8bb6df1583439122c27bd381d2 Job: tests (3.11/3.12), упавший step: Run tests.
Упали test_at_limit, test_high_priority, test_low_priority: ожидалось False, получено True (>= вместо >).
## Исправление
Вернул оператор > коммитом "Restore strict SLA boundary". PR: https://github.com/buster16788/pm03-day07/pull/1/commits/80b570f1a04ed68842b2768e1972269540cbbf0e
## Зелёный запуск на Python 3.11 и 3.12
https://github.com/buster16788/pm03-day07/pull/1/changes/c152e8400d33d2f06e05913620d773ad40437e09
## Два новых сценария
test_negative_elapsed: -1 даёт ValueError.
test_unknown_priority: "urgent" даёт ValueError. Всего 8 тестов.
## Что автоматическая проверка пока не покрывает
Не проверяются типы входа, кроме числа и строки; Python вне 3.11 и 3.12; нет проверки стиля кода.
