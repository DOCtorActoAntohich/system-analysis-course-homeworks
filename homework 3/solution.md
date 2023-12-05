# Решение: Домашка №3

## Стейкхолдеры

Выделим таких держателей стейков с их консёрнами:

- **Топ-менеджмент** - родительская компания
  - Тестирование большего количества гипотез по отсеву потенциальных работников.
    Планируется продавать это решение другим (сильно возросла сложность).
    Требуется релизный цикл в неделю как максимум.
  - Для остальной системы хотят релизный цикл в 1 месяц.
- **Разработчики**
  - Стабильная система, которую легко фиксить в случае сбоев.
- **Клиенты**
  - Ожидаемое поведение системы.
- **Воркеры** [new]
  - Ожидаемое поведение системы, в том числе своевременные уведомления о заказах.
    (На месте воркера, не хотелось бы напороться на штраф когда
    не успел на заказ из-за хреновых уведомлений).
- **Менеджеры**
  - Скрыть систему ставок от посторонних глаз типа всех остальных отделов
    и разработчиков, которые системой не занимаются.
  - Рост нагрузки с 10 заказов в день до 10 заказов в минуту.
- **Работники склада** - сборщики расходников [new]
  - Ожидаемое поведение системы.
- **Админы**
  - Простота мониторинга системы.
- **Юристы**
  - Соблюдение правовых норм.
- **Финотдел**
  - Списание денег с клиентов не раз в неделю, а раз в месяц.
    Выплаты воркерам раз в месяц.
  - Надежность хранения финансовой информации.
  - Внедрение новых способов списания денег для клиентов.

Раскидаем стейкхолдеров по матрице Влияние-Интерес:

| Стейкхолдер      | Влияние | Интерес |       Приоритет и группа        |
|:---------------- |:-------:|:-------:|:-------------------------------:|
| Топ-менеджмент   | Высоко  | Высоко  |       1 - Плотная работа        |
| Разработчики     | Высоко  | Высоко  |       1 - Плотная работа        |
| Админы           | Высоко  |  Низко  | 2 - Удовлетворение потребностей |
| Клиенты          |  Низко  | Высоко  |       3 - Информирование        |
| Воркеры          |  Низко  | Высоко  |       3 - Информирование        |
| Менеджеры        |  Низко  | Высоко  |       3 - Информирование        |
| Работники склада |  Низко  |  Низко  |         4 - Мониторинг          |
| Юристы           |  Низко  |  Низко  |         4 - Мониторинг          |
| Финотдел         |  Низко  |  Низко  |         4 - Мониторинг          |

Визуализируем важность консёрнов стейкхолдеров

![stakeholder_concerns.svg](./materials/stakeholder_concerns.svg)