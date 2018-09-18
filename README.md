# [@scrapy_python](https://t.me/scrapy_python) FAQ #

В этом репозитории находится полезная информация, собранная участниками чата.

### С чего начать? ###

* [Прочитать документацию](https://docs.scrapy.org/en/latest/)

### Как ограничить количество реквестов? ###

* CLOSESPIDER_PAGECOUNT = 10

### Как спарсить JS? ###

* ставится Splash(удобно в Docker) и плагин [scrapy_splash](https://github.com/scrapy-plugins/scrapy-splash)
* смотреть откуда идут данные в Chrome -> devtools -> network -> XHR

### Лучшие практики ###

* Использовать css селекторы чтобы избежать пробелов в названии .class
* Использовать xpath для поиска сложных значений, например в таблицах
* Использовать [inline-requests](https://github.com/rmax/scrapy-inline-requests) для синхронных запросов в функции 

### Нельзя мешать yield и return? ###
После return жизни нет. Нужно возвращать список или что-то итерируемое.

### Как вытащить узел по тексту внутри него используя css-селектор ###
Через CSS - никак. Использовать xpath contains.

### Как поставить на windows ###
Простой способ - поставить в anaconda

### Как достать items из последного job-а в scrapinghub?###
https://app.scrapinghub.com/api/items.json?project=PROJECT&spider=SPIDERNAME&apikey=KEY
там где SPIDERNAME нужно вставить именно название, а не номер паука.
дополнительно можно почитать тут: https://support.scrapinghub.com/support/discussions/topics/22000009481
