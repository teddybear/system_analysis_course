# Заметки

Авторизация не прорабатывается?
Админка:
    - Справочник типов услуг
    - Конфигуратор тестов под каждого кота-соискателя/вакансию
    - список выполненных заказов с контактными данными клиента (контроль качества)
    - список проваленных заказов с теми же данными
    - форма для результатов проверки качества
    - система ставок на выполнение заказа (выигрыш делят сами, проигрыш — банк разработчикам) (это лучше отдельно сделать от всего)
Клиент/Заказы:
    - Дашборд клиентов
    - Форма выбора типа услуги с примерной стоимостью
    - Система матчинга so far — рандомный матчинг ()
    - Расчет скидок, за каждые 10к: первые 10к 5%, дальше по 1% до достижения 12% ()
    - Стоимость услуги фиксированная, но расчет нужно предусмотреть, стоимость 100 за любую услугу ()
    - Оплата всегда, независимо от результата
    - Если воркер не пришел, заказ отменяется, предлагается сделать заказ (копию) заново на другую дату, назначается новый воркер
    - Сумма списывается с клиента каждое воскресенье согласно затратам на запрошенные задачи, списание
    - видит все свои списания и начисления
Воркер:
    - Дашборд воркера
    - Список активных заказов назначенных на воркера
    - Перед выездом должен получить необходимые расходники (бланк приема работы) (флоу заказа в отдел сборки расходников)
    - перед стартом отмечается в приложении, присылает фотку
    - отмечается перед стартом заказа (фотка и кнопка приступил)
    - В конце заказа фото (отчет с подписью клиента)
    - Каждый последний день месяца начисляется равная сумме выплат минус штрафы, зачисление через внешний сервис (инвойс)
    - штрафы начисляются за проваленные задачи (-40), отмененные не оплачиваются, за задачу выплачивается 60% (т.е. 60 =)
    - видит все свои списания и начисления
    - менеджер может зачислить рандомное количество денег воркеру, тоже нужно отражать (кто и за что)
Онбординг воркера:
    - заявка на сайт
    - выполнение назначенных менеджером за каждые 10к: первые 10к 5%, дальше по 1% до достижения 12% тестов для оценки уровня
    - ожидается высокий RPS на прием заказов
    - онбординг заканчивается либо попаданием в пул воркеров, либо отказ (уведомляется как-то, наверн по имейлу)
Отдел расходников:
    - уведомить сотрудника о новом заказе
    - дождаться печенья под клиента (под заказ), положить в заказ
    - ткнуть выдано после сбора
Нотификации:
    - approve/decline для новых воркеров
    - новые заявки на тестирование
    - уведомления по изменению статуса заказа, подтверждению от клиента и воркера
    - уведомления о готовности расходников
    - генерация инвойса (клиенту и воркеру)
    - уведомления о контроле качества (клиенту и воркеру)
    - уведомления о новом заказе воркеру (что и когда надо сделать)