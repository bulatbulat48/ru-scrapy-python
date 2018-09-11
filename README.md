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
после return жизни нет. Нужно возвращать список или что-то итерируемое.

### Как вытащить узел по тексту внутри него используя css-селектор ###
Через CSS - никак. Использовать xpath contains.
