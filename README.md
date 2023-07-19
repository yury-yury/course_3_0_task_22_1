Условия домашки

Контекст: зачем решать подобные задачи
‍Данные, которые передает пользователь для сохранения, а также данные, которые пользователь хочет получать в ответ на обращение к веб-приложению, должны быть динамически изменяемые, поэтому для работы с ними используются базы данных.

В любом веб-приложении разработчик должен уметь подключить базу данных и создать модели для тех данных, с которыми будет работать пользователь.

Наше приложение не будет исключением. Пришло время создать структуру БД для хранения данных.

Критерии выполнения заданий
Результат выполнения проекта залейте в GitHub и сдайте в виде ссылки на репозиторий.
Результаты работы по первому пункту в задании 6 прикрепите в виде скриншотов терминала.

Задание 1
Подключите СУБД PostgreSQL для работы в проекте. Для этого:

Создайте базу данных в ручном режиме.
Внесите изменения в настройки подключения.

Задание 2
В приложении каталога создайте модели:

Product,
Category.
Опишите для них начальные настройки.

Задание 3
Для каждой модели опишите следующие поля:

Product:
наименование,
описание,
изображение (превью),
категория,
цена за покупку,
дата создания,
дата последнего изменения.

Category:
наименование,
описание.

Для поля с изображением необходимо добавить соответствующие настройки в проект, а также установить библиотеку для работы с изображениями
Pillow
.

Задание 4
Перенесите отображение моделей в базу данных с помощью инструмента миграций. Для этого:
- Создайте миграции для новых моделей.
- Примените миграции.
- 
Внесите изменения в модель категорий, добавьте поле 
created_at

, примените обновление структуры с помощью миграций.
Откатите миграцию до состояния, когда поле 
created_at
 для модели категории еще не существовало, и удалите лишнюю миграцию.

Задание 5
Для моделей категории и продукта настройте отображение в административной панели. Для категорий выведите id 
и наименование в список отображения, а для продуктов выведите в список id, название, цену и категорию.

При этом интерфейс вывода продуктов настройте так, чтобы можно было результат отображения фильтровать по категории, 
а также осуществлять поиск по названию и полю описания.

Задание 6
Через инструмент shell заполните список категорий, а также выберите список категорий, применив произвольные 
рассмотренные фильтры. В качестве решения приложите скриншот.

Сформируйте фикстуры для заполнения базы данных.

Напишите кастомную команду, которая умеет заполнять данные в базу данных, при этом предварительно зачищать ее от старых данных.
Последний пункт можно реализовать в связке с инструментом работы с фикстурами, можно описать вставку данных отдельными запросами.

* Дополнительное задание
В контроллер отображения главной страницы добавьте выборку последних 5 товаров и вывод их в консоль.
Создайте модель для хранения контактных данных и попробуйте вывести данные, заполненные через админку, на страницу с контактами.
* 
Дополнительное задание, помеченное звездочкой, желательно, но не обязательно выполнять.