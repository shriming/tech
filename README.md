# Технологии, которые можно использовать для приложения на полном БЭМ-стеке

## Содержание

* [На клиенте](#frontend)
* [На сервере](#backend)
* [Хостинг и облака](#hosting)

<a name="frontend"></a>
### Клиент

* [БЭМ](https://ru.bem.info/) — главный ресурс с исчерпывающей информацией по БЭМ (рекомендую использовать кнопку ["Быстрый старт"](https://ru.bem.info/tutorials/quick-start-static)). А также прогулятся по всем разделам ресурса (начать лучше с [методологии](https://ru.bem.info/method/) и [FAQ](https://ru.bem.info/faq/)).
  * [БЭМ-компоненты](https://github.com/bem/bem-components/blob/v2.3.0/README.ru.md) — тут кратко собрано все из чего состоит БЭМ. Собрано большое количество ссылок на внешние ресурсы об инструментах, которые упоминиаются в лекциях ([ссылка](https://github.com/bem/bem-components/blob/v2.3.0/README.ru.md#Инструменты)).
  * [Мастер-класс по БЭМ](https://github.com/yuriMalakhov/do-it-yourself-workshop) — удобный способ выполнения заданий по БЭМ, необходимых для начального усвоения методологии. Стоит также посмотреть [лекцию](https://events.yandex.ru/lib/talks/2185/). Кроме того, есть [инструкции](https://github.com/dab/bemup-workshop-vagrant/blob/master/README.ru.md) для пользователей windows.
  * Список очень полезных лекций стоит посмотреть [тут](https://events.yandex.ru/lib/talks/?audience=frontenderyi&tech=bem). Например, про полный стек [БЭМ-технологий](https://events.yandex.ru/lib/talks/1922/).
* [ENB-сборщик](https://ru.bem.info/tools/bem/enb-bem/) — писать можно на любых технологиях с любыми препроцессорами, а потом все собирать с ENB.

<a name="backend"></a>
### Сервер

* [Sails](http://sailsjs.org/) и [EXPRESS](http://expressjs.com/) — 2 основых nodejs-фреймворка, которые используются во всех примерах для full-stack БЭМ.
  * Sails базируется на Express и предлагает более удобную реализацию в рамках MVC подхода и организацию файлов внутри проекта (по личному опыту).
  * Sails предлагает удобное подключение всевозможных адаптеров для баз данных:
    описание модели в JSON (+ автоматические миграции)
      -> подключение адаптера
      -> использование любой БД
      -> [REST API](http://sailsjs.org/documentation/reference/blueprint-api?q=blueprint-routes) из коробки без доп. настроек.
  * [Генератор для связки БЭМ и Sails](https://ru.bem.info/built-with-b/#sails-bem-project-stub)
  * [Фреймворк для одностраничных приложений](https://ru.bem.info/built-with-b/#bnsf)
* [Passport](http://passportjs.org/) — для  реализации авторизации на сайте.

<a name="hosting"></a>
### Хостинг и облака

* [Node-hosting](https://github.com/nodejs/node-v0.x-archive/wiki/Node-Hosting) — сводная таблица с кратким описанием хостингов, поддерживающих nodejs и websockets из коробки. Из бесплатных стоит выделить:
  * [Heroku](http://heroku.com/)
    * Плюсы: интеграция с GitHub, большое количество add-ons (базы данных, мониторинг, и тд.), удобный deploy и доступ к приложению из командной строки.
    * Минусы: если приложение не используется, то "засыпает" через 30 минут и достаточно долго просыпается потом. Можно обойти с помощью [HostTracker](http://www.host-tracker.com/), если настроить проверку приложения чаще чем в 30 минут. Кроме того, если выходить за рамки бесплатных услуг, то все стоит достаточно дорого.
  * [Qt Cloud Services](http://qtcloudservices.com/) — есть интеграция с GitHub, приятный интерфейс. Приложение не засыпает, поддержка MongoDB.
  * [OpenShift](https://www.openshift.com/)
