Prestashop module
=================

Модуль интеграции CMS Prestashop c [RetailCRM](http://www.retailcrm.com)

#### Модуль позволяет:

* Экспортировать в CRM данные о заказах и клиентах и получать обратно изменения по этим данным
* Синхронизировать справочники (способы доставки и оплаты, статусы заказов и т.п.)
* Выгружать каталог товаров в формате [ICML](http://retailcrm.ru/docs/Разработчики/ФорматICML) (IntaroCRM Markup Language)

#### Настройка

На странице настроек модуля введите API url и API ключ, после этого установите соответствие справочников

#### Выгрузка каталога

Добавьте в крон запись вида

```
* */4 * * * /usr/bin/php /path/to/your/site/modules/retailcrm/job/icml.php
```

#### Получение изменение из RetailCRM

Добавьте в крон запись вида

```
*/7 * * * * /usr/bin/php /path/to/your/site/modules/retailcrm/job/sync.php
```

#### Единоразовая выгрузка архива клиентов и заказов в RetailCRM

```
/usr/bin/php /path/to/your/site/modules/retailcrm/job/export.php
```