## Четвертая домашка


### Шаг 1

Объеденить entity-service Воркеров со скорингом.
#### До объединения
- Instability(entity-service Воркеров) = 1 / 1 + 5 = 0.16
- Instability(расчет и списание средств у клиентов и сотрудников) = 0 / 2 = 0
- Instability(Контроль качества работы сотрудников) = 1 / (2 + 1) = 0.33
- Instability(Сборка необходимых расходников для заказа) = 1 / (2 + 1) = 0.33
- Instability(Система ставок менеджмента happy cat box) = 0 / 2 = 0

#### После объединения
- Instability(entity-service Воркеров) = 0 / 5 = 0
- Instability(расчет и списание средств у клиентов и сотрудников) = 0 / 2 = 0
- Instability(Контроль качества работы сотрудников) = 1 / (2 + 1) = 0.33
- Instability(Сборка необходимых расходников для заказа) = 1 / (1 + 1) = 0.5 (убрал связь потому что воркер попадет транзитивно через Планирование визитов)
- Instability(Система ставок менеджмента happy cat box) = 0 / 2 = 0

[План работ для объединения сервисов](https://github.com/aberkromb/SystemAnalysisHomeWorks/blob/main/Week4/MergeWorkersAndScoring.png)


### Шаг 2
Вынести "интелектуальный Матчинг сотрудников и клиентов" в отдельный сервис. 
Можно воспользоваться паттерном Strangler Fig Application.
[План работ для выноса сервиса](https://github.com/aberkromb/SystemAnalysisHomeWorks/blob/main/Week4/ExtractMatcher.png)
