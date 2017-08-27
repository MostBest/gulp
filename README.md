# Gulp - быстрый старт
Сборка gulp от компании mostbest.ru. Автор: Чернов Алексей

# Используемые технологии
_Для работы требуется установка [Node.js](https://nodejs.org/en/), [Git](https://git-scm.com/)_

# Подготовка рабочей области
Создаем репозиторий проекта на локальном сервере.  
1. Открываем окно команд **shift + левая кнопка мыши** из папки проекта.
1. В открывшемся окне пишим команду **npm i gulp -g** - установка gulp (глобально). Данная операция выполняется однократно так как при этом gulp будет установлен глобально.  
1. **npm init -f** - стартовая команда для создание файла **package.json**. В него будет записаваться информация об установленных пакетах. Ключ **-f** означает "тихую" установку.  
1. **npm i gulp -D** - устанавливаем пакет gulp локально.
1. **Копируем/создаем структуру каталогов** - основными делаем дериктивы **src** и **build**.  
5.1 **src** - дериктива разработки.  
5.1.1 **src -> fonts** - папка шрифтов проекта. Шрифты желательно подгружать из [google репозитория](https://fonts.google.com/).  Если есть необходимость разместить шрифты локально, то они переносяться в папку рабочего проекта без изменений.  
5.1.2 **src -> sass** - стилевая папка проекта. Использовать scss синтаксис.  
5.1.3 **src -> sass -> index.scss** - родительский файл описывающий связи.  
5.1.4 **src -> sass -> includes** - общая директория scss файлов.  
5.1.5 **src -> sass -> includes -> system** - директория системных scss файлов.  
5.1.6 **src -> sass -> includes -> system -> variables.sass** - файл системных переменых.  
5.1.7 **src -> sass -> includes -> system -> fonts.sass** - файл подключения шрифтов.
5.1.8 **src -> js** - javascript директория. Использовать ECMAScript 6.  
5.1.9 **src -> img** - директория визуального оформления.  
5.1.10 **src -> pug** - директория html разметки. Использовать html предпроцессор pug.  
5.2 **build** - дериктива скомпелированных файлов. 
1. **Создаем файл gulpfile.js** - файл с инструкциями для gulp.


## Сборка CSS
**gulp-sass** - CSS препроцессор/шаблонизатор. Возможная альтернатива [gulp-stylus](http://stylus-lang.com/). 
**gulp-cssnano** - CSS компрессор. [Официальный сайт](http://cssnano.co/).
**gulp-autoprefixer** - автоматическое добавление вендорных префиксов. 

## Сборка JS
**gulp-uglify** - JavaScript компрессор. 
**gulp-concat** - объединение JavaScript файлов. 

## Оптимизация изображений
**gulp-imagemin** - компрессор изображений. 
**imagemin-pngquant** - PNG плагин для gulp-imagemin.
**gulp.spritesmith** - объединяет изображения в спрайты, формирует вызов из CSS.
**gulp-cache** - формирует кэш из временных файлов. Необходим для оптимизации работы с изображениями. 

## Оптимизация SVG изображений
**gulp-svgmin** - минификация SVG/SVGO.
**gulp-svg-spritesheet** - объединяет SVG изображения в спрайты, формирует вызов из CSS.

## Автоматическая перезагрузка страницы браузера
**browser-sync** - сервер, перезагрузка страницы при внесении изменений. Возможная альтернатива [gulp-livereload](https://www.npmjs.com/package/livereload).

## Вспомогательные плагины
**gulp-rename** - переименование файлов.
**del** - очистка выбранной директории. 
**gulp-rigger** - подключает содержимое одного файла в тело другого. 
