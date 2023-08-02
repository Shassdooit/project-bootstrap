##  Gulp сборка (под вёрстку)


### npm run dev (режим разработки):

1. Запускает локальный сервер.

2. Добавляет sourcemaps в css и js файлы.

3. Переименовывает файлы в (min.*) не минифицируя их, минифицирует в build режиме.

4. Все изображения из папки src/img сжимает и преобразует в формат webp (кроме svg).

5. Все шрифты с папки src/fonts преобразует в формат woff и woff2, в папке src/scss/base создается файл fonts.scss(с кодом подключения шрифтов) который подключается в style.scss через импорт @import "./base/fonts", плагин автоматически считывает font weight.

6. Создается svg sprite,берет svg файлы из  src/svgicons и создает спрайт в папке dist/img/icons/icons.svg.

7. Выгрузка на FTP сервер, в config/ftp.js указываем данные, подключение командой npm run ftp.

8. Отдельное создание svg sprite командой npm run sprite.

9. Архивация Build проекта в формат Zip с названием папки проекта, команда npm run zip .



### npm run build (продакшен проекта) "отличия от dev" :



1. Локальный сервер не запускается.

2. sourcemaps не добавляется.

3. читать п.3 dev.

4. По мимо webp выгружаются изначальные форматы изображений(но сжатые) настройки можно менять в images.js optimizationLevel  от 0 до 7 .
