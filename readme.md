
/app - проект для разработки

/dist - сборка с минификацией css/js и пр. для выгрузки на сервер


--- > Для установки сборщика используем команды (в корне проекта):

npm install
bower install

--- > Для работы над проектом команда gulp (локальнй сервер, автообновление страницы бразуера, компиляция less, и т.д.):

gulp

Проект работает с файлами из папки app, в папке dist будет находиться только финальная сборка.

--- > Для сборки проекта

gulp dist


------------------------------------------------------------------------------------------------------------------------

В html файлах есть следующие комментарии в теге <head></head>

	<!-- build:css css/vendor.css --> // сборка всех внешних css файлов в 1 под названием vendor.css
    <!-- bower:css --> // получение необходимых css файлов от пакетного менеджера bower из bower_components
	....
    <!-- endbower -->
    <!-- endbuild -->
	
    <!-- build:css css/main.css --> // сборка стилей разработчика в 1 файл main.css
	....
    <!-- endbuild -->
	
    <!-- build:js js/vendor.js --> // сборка внешних подключаемых скриптов в 1 файл
    <!-- bower:js -->// получение необходимых js файлов от пакетного менеджера bower
    ....
    <!-- endbower -->
    <!-- endbuild -->
	
    <!-- build:js js/main.js --> // сборка скриптов разработчика в 1 файл
    ....
    <!-- endbuild -->
