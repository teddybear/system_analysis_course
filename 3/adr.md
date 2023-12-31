# Решение по сервису скоринга HCB-MCF-1

## Status
Proposed

## Context

В рамках реализации MCF необходимо сделать скоринг (тестирования и определения характеристик котов-воркеров)
Почему?
 - Для бизнеса критично проверять новые гипотезы по отсеву котов и изменять уже существующие с максимальной скоростью и надёжностью.

Из требований к сервису, выделяется следующее:
 - скоринг потенциальных работников уникален в своём роде, и логика его работы сильно выше, чем планировалось. Бизнес в будущем хочет продавать его другим компаниям и тестировать больше гипотез;
 - релизный цикл для всей системы — месяц, для скоринга работников — неделя максимум.
 - Мы ожидаем 1к заявок в день от рандомных котов, также, судя по отзывам, наши конкуренты могут попытаться нас заддосить в этом месте.

Исходя из требований, можно выделить 
- performance
- modifiability
- evolvability
- scalability
- maintainability
- agility, testability и deployability — общие требования к системе

## Decision

Очевидно, что исходя из требований к скорингу, это должен быть:
- отдельный сервис
- выполенный в стиле microkernel
- база данных RDBMS
- коммуникации: асинхронные (общий стиль проекта EDA)
Это позволит управлять нагрузкой и развертыванием, не затрагивая остальную систему, кроме того, microkernel позволит контролировать логику, подключая не только требования HCB, но и других потенциальных клиентов.

## Consequences
- Потребуется инфрастурктурное расширение под отдельный сервис, включая deployment и observability
- Для реализации выбранного стиля (microkernel) нужно выделить команду сениор-разработчиков, что логично, т.к. сервис является частью core-domain компании

## Compliance
- Необходимо контролировать coverage и другие метрики качества кода, сервис очень критичен
- Нагрузочное тестирование
- Coupling/cohesion
- Проверка, что команда строго следует выбранному архитектурному стилю (нужно уточнить варианты контроля)
- Контроль релиз-цикла
- Контроль schema-registry

![ADR Meme](figures/adr-meme.png)