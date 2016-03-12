# О чём должен помнить веб-дизайнер

От технологов и программистов — веб-дизайнерам. О чём нужно помнить, чтобы называть себя веб-дизайнером.

Сверстать можно всё, что можно придумать и воплотить в макете. Вопрос, однако, во времени, деньгах и удобстве (времени и стоимости) расширения полученного результата и в адекватности перестроения блоков при адаптации страницы под разную ширину окна браузера.



## Общее

**Веб-дизайнер — это инженер**. Веб-дизайнер — это не рисовальщик, он не придумывает «как будет выглядеть», он придумывает «как сделать, чтобы проект лучше всего решал поставленные задачи» и как потом воплотить это визуально. Если Вы совсем не умеете верстать (не представляете как работает страница, как ведут себя блоки), Вы ещё не веб-дизайнер. Отрисовка макета без представления о том, как будет работать сайт, напоминает проектирование автомобиля без представления о его двигателе, системах управления, условиях эксплуатации, количестве и расположение конечностей водителя.

**Технически недоработанный макет осложняет работу технолога**. Для студий — это увеличение сроков разработки. Для фриланса — ухудшение кармы дизайнера в момент, когда технолог описывает клиенту список технических недоработок и/или неучтённых дизайнером ограничений.

**Создавайте компоненты, а не страницы**. Некоторые проекты будут нуждаться в расширении. Гораздо разумнее собирать новые страницы их компонентов, чем создавать дубликаты уже имеющихся (или похожих) элементов.



## Макеты

**Макет нужно делать в sRGB**. Обязательно и критично. Иначе цвета в вёрстке могут отличаться от макетных.

**Макет должен иметь тот размер, в котором его нужно сверстать**. Размер(ы) выбирается, исходя из специфики проекта и целевой аудитории.

**В макетах допустим только режим наложения normal**. Критично, обязательно. И так будет, пока не [появится кроссбраузерная поддержка](http://caniuse.com/#feat=css-mixblendmode) режимов наложения. И даже когда появится, использование режимов наложения нужно будет применять осторожно, с огладкой на особенности реализации в вебе. Это правило не касается состоящих из множества слоёв иллюстраций, которые планируется соединять в одно изображение.

**Одна страница = один макет**. Обычно, это довольно объёмные файлы, если хранить все на артбордах в едином файле, он может подтормаживать. Особенно актуально для PSD-макетов, для простых AI-макетов может быть допустимо разместить все макеты на артбордах в одном файле.

**Скрытые слои не будут свёрстаны, если в техническом задании не указано иное**. Хотите показать, что в макете есть необходимые блоки, скрытые по умолчанию — приложите скриншоты, на которых эти слои видны. Обязательно складывайте нужные скрытые слои в отдельные папки и скрывайте такие папки.

**Оставляйте эффекты слоёв**. Эффекты, преобразованные в слои, ощутимо дольше верстать.

**Про корректирующие слои лучше забыть**. Любые «пост-модификации» могут всерьёз осложнить работу технолога.

**Делаете макет в Adobe Illustrator — прикладывайте все линкованные ресурсы (картинки, шрифты...) и скриншоты макета**. Если в макете использована растровая картинка, не записанная в файл (линкованная), технолог её не увидит, если она не приложена к макету.



### Стайлгайд

**Должен быть стайлгайд**, в котором видны все необходимые состояния меняющихся элементов (интерактивных и просто изменяющихся) и типографическое оформление.

**Создали стайлгайд — используйте его**. Нет ничего хуже, чем обнаружить «новую» кнопку, атипичную модульную сетку или «уникальный» размер шрифта. Хотите создать новый блок (который нельзя собрать из уже имеющихся) — начните со стайлгайда. «Думайте компонентами», не плодите сущности (размеры шрифтов и отступов, цвета, типы обводки и пр.) без надобности.

**Стайлгайд — это отдельный макет**. Это не текстовая инструкция как включать/выключать видимость слоёв, варианты композиции слоёв. Это не артборд, включённый в какой-либо макет.

**Для ссылок нужны состояния: «покой», «наведение», «клик» (последние два могут совпадать)**. Для навигационных ссылок нужно состояние «находимся на этой странице». Для контентных ссылок желательно состояние «ссылка посещалась».

**Для кнопок нужны состояния: «покой», «наведение», «клик», «блокирована»**. Иногда ещё нужно состояние «идёт процесс».

**Для текстовых полей форм нужны состояния: «покой», «курсор в поле», «блокировано»**. Нет смысла прорисовывать состояние «клик». Нет смысла прорисовывать состояние «наведение».

**Для флажков (чекбоксов) и радиокнопок нужны состояния: «отмечено», «не отмечено», «блокировано»**. Нет смысла прорисовывать состояние «клик». Нет смысла прорисовывать состояние «наведение».

**Для типографики нужно показать, как минимум, следующее**: заголовок 1, параграф, заголовок 2, параграф, заголовок 3, параграф, заголовок 4, параграф, параграф, маркированный список, параграф, нумерованный список, блочная цитата, параграф, таблица, параграф. Верстальщику важно увидеть все вертикальные расстояния (для этого и нужно чередование параграфами и два параграфа подряд).



## Модульные сетки

**Используйте модульные сетки**. Это сделает результат аккуратнее и, если не допускать глупых ошибок, ускорит реализацию макета в вёрстке. Самая глупая ошибка: создать модульную сетку, но не следовать ей.

**Модульные сетки — резиновые**. «Строку» с блоками модульной сетки можно вставить в блок любой ширины с сохранением параметров сетки. [Пример](http://getbootstrap.com/css/#grid-nesting).

**Граница ячеек модульной сетки — это середина промежутка между ячейками**. Блок не может выступать за середину этого промежутка — левая граница блока не может проходить по правой границе предыдущей ячейки модульной сетки.

**Идеал модульной сетки — 12 колонок**. Ибо 12 делится на 2, 3, 4 и 6. Чтобы придумывать свои (пяти- и восьми-колоночные) сетки нужно иметь действительно серьезные причины, ибо восьми-колоночная сетка не позволит выстроить блоки по 3 в ряд.

**Между колонками может быть пустое место, пропорциональное ширине колонки**. К примеру, блоки в 12-колоночном ряду могут распределяться так: 2-колоночный блок, 1 колонка «пустоты», 9-колоночный блок.



## Текст, Шрифты

**Используйте легальные шрифты**. Есть множество хороших бесплатных. Например, на [Google Fonts](https://www.google.com/fonts).

**Используйте проверенные шрифты**. Перед использованием редкого шрифта или особого начертания, обязательно проверяйте, как они отображаются во всех браузерах из технического задания на всех операционных системах. Особенно в Windows и Linux, особенно кириллица. Самые «удачные» браузеры — IE (и Edge) и Firefox. За этим можно обратиться к технологу.

**Размеры шрифтов и интерлиньяж указывайте целыми числами в пикселях**. Браузер всё равно приведёт их к пиксельным размерам, пересчёт в другие единицы удобнее всего из пикселей.

**Выберите несколько размеров шрифта и придерживайтесь их**. Пример размеров: для заголовков 1, 2, 3 и 4 уровней, контентный, акцентированный (если не совпадает с каким-либо заголовочным), уменьшенный. Не плодите сущности без надобности.

**Вертикальные границы текстового блока проходят по границам «высоты линии», а не по границам букв первой и последней строк**.

**Избегайте менять кернинг и трекинг**. На подавляющем большинстве дисплеев очень мало «пикселей на дюйм», такое изменение нередко приводит к грустным эффектам: размытие символов, изменение их визуальной плотности.

**Интерлиньяж не должен быть меньше размера шрифта**. Всегда помните: если в текстовом блоке более одного слова, количество строк непредсказуемо. Не избегайте знакомства с «электрогардиографической одиннадцатиклассницей, псевдореволюцонизирующей циклопентанпергидрофенантрены».

**В вебе нет кроссбраузерных переносов**. Лучше не использовать переносы слов вообще. Расстановка символов мягкого переноса в тексте возможна (никто не будет делать это вручную, а автоматическое ещё нужно внедрить в проект), автоматический перенос в браузерах имеет [скромную поддержку](http://caniuse.com/#feat=css-hyphens).

**Символ «рубль» есть во многих шрифтах**. При желании использовать символ рубля в указании цен, не стоит использовать комбинацию «Р-», в которой дефис сильно сдвинут (отрицательным кёрнингом). Во многих шрифтах есть символ рубля, а если подходящий его вид найти не удалось, нарисуйте векторную картинку и отдайте ее технологу в формате svg.

**Не используйте [маркерное выделение текста](/img/marker-text.png)**, если предполагается перенос строк (это случится обязательно, если строка длиннее одного слова и проект подразумевает адаптивность). Правый и левый внутренние отступы возможны только в начале и в конце какого-либо элемента, при переносе они будут нулевыми. [Оборачивание](http://codepen.io/nicothin/pen/xZoOWV) же каждого слова в отдельный тег добавит много боли контент-менеджеру.



## Блоки

**Думайте о блоках и потоках блоков**. Крайне важно понимать как ведут себя блоки на странице и как они могут взаимодействовать в потоке. Это помогает избежать наложения блоков друг на друга.

**Всегда думайте о переполнении блока текстом или другими блоками. Всегда**. Почти для всех блоков нужно предусматривать возможность переполнения. Это самое важное с точки зрения технической реализации макета в вёрстке.

**У блоков есть внутренние и внешние отступы**. Внешние отступы пересекаются, а не суммируются.

**Однотипные блоки должны иметь однотипные свойства**. То есть, одинаковую ширину, высоту, цвет бордюра и пр.



## Векторная графика

**Используйте векторную графику**. Везде, где это возможно. При соблюдении некоторых условий, векторная графика технологичнее растровой, меньше размер файлов, поддерживает «эффекты внутри картинки», не требует ретинизации или ускоряет её.

**Создавайте векторную графику в векторных редакторах**. Для любых форм (сложнее прямоугольника со сглаженными краями или простых библиотечных форм) используйте [Adobe Illustrator](http://www.adobe.com/ru/products/illustrator.html) или [Inkscape](https://inkscape.org/ru/download/).

**Создавайте векторную графику в отдельных файлах**. Любые иконки и иллюстрации создавайте в отдельных файлах (лучше всего — сразу в SVG-файлах, одна иконка = один файл). Если Вы предоставите такие небольшие файлы технологу, его работа будет существенно быстрее. Часто иконки берутся с [icomoon.io](https://icomoon.io/app/), [flaticon.com](http://www.flaticon.com/) и подобных — если Вы скачиваете их оттуда в виде архива с SVG-файлами, приложите используемые к макету.

**Рисуйте векторные формы вместо работы кистью**. Заливки и формы, созданные кистью получаются «грязными» — имеют множество лишних ключевых точек, что крайне негативно сказывается на размере файла (иногда, оптимизировав количество точек, удавалось сжать SVG-изображение в 12 (!!!) раз — прим. Н.Г.).

**Предоставляйте векторную графику в том её размере, в котором она использована в макете**. Обязательно!

**Не накладывайте на векторные изображения в PSD-макетах корректирующие слои, маски, эффекты**. C высокой вероятностью это приведёт к невозможности использования такой векторной графики.

**Выравнивайте точки в кривых по пиксельной сетке** если возможно. Тогда иконки не будут мыльными на экранах с низким разрешением, к тому же будут лучше сжиматься. В редакторах настройка обычно называется «snap to pixel».

**Артборд должен быть подогнан по габаритам фигуры**. Для нескольких иконок одинакового размера допустимо, чтобы атрборды были одинаковых размеров (больше габарита фигур).

**Недопустимы режимы наложения, отличные от normal**. Кроссбраузерно это не сверстать.

**Всё, что может быть слито в единую форму, должно быть слито**. Это позволяет уменьшить размер файла (нередко, существенно).

**Удаляйте всё лишнее из векторных картинок**. Если какие-либо формы не видны, их нужно удалить, иначе они будут бессмысленно увеличивать размер файла.

**Избегайте наложения эффектов и трансформаций**. Переводите всё в кривые, применяйте трансформации.

**Избегайте градиентов и теней**. В некоторых случаях это может наложить ограничения на использование векторной графики.

**Для форм с заливкой не используйте обводку того же цвета, что и заливка**.

**Не комбинируйте в макете слои со вставленной векторной графикой с элементами, нарисованными в макете**. Если Вы вставили в макет векторную картинку и потом «дополнили» её какими-то слоями макета, использовать такую картинку без растеризации в вёрстке, как правило, не получится.



## Адаптивность, адаптивная графика

**Выберите 2-3 брейкпоинта и создавайте макеты для них**. Обычно, брейкпоинты следующие: 768, 992, 1200 пикселей (изредка добавляется ещё 480 пикселей). Традиционно, мы принимаем некую минимальную ширину (320 или 240), преобразования блоков происходят по достижении брейкпонта. Важно понимать: сделав макет в ширине 768, Вы показали то, как макет выглядит от 768 до следующего брекпоинта в большую сторону (скажем, 992).

**Уточняйте в техническом задании как ведет себя дизайн на разных брейкпоинтах**. По умолчанию, всё, что уже чем ≈1000 пикс. будет «резиновым».

**Ретинизируемые растровые изображения в оригинале должны быть в 2-3 раза крупнее, чем видно в макете**. Лучше всего, чтобы они не лежали в режиме подрезающей маски, а были масштабированными смарт-объектами.



## Разное

**Реализация нестандартных элементов форм увеличивает сроки проекта**. Особенно это касается нестандартных выпадающих списков (если не планируется использовать какое-либо готовое решение).

**Не рисуйте векторные иконки в [Sketch](http://www.sketchapp.com)**. Такие иконки в 90% случаев технологически непригодны к использованию в векторном виде.



## Неприятные для технолога мелочи

**Отсутствие структуры слоёв**. Если слои не разложены по правильно именованным папкам, это несколько замедляет работу.

**Большие части макета в смарт-объектах**. «Шапка» и «подвал» в смарт-объектах не имеют смысла для экономии места, но увеличивают время доступа к своим составляющим. Это не относится к **связанным** смарт-объектам, в случае, когда макетов много.

**Изменение цвета объектов или текста при помощи прозрачности**. Плохо, так как технологически мы стараемся избегать прозрачности — много полупрозрачных объектов могут вызвать проблемы быстродействия страницы.

**Изменения вида векторных объектов эффектами Photoshop**. Это может привести к невозможности использования векторной графики.

**Набор текстовых блоков КАПСОМ вместо использования «All Caps»**. Приводит к необходимости нажимать несколько лишних кнопок при копировании текста слоя. Когда таких слоёв много — потеря времени.

**Заголовок текстового блока и его контентный текст в одном текстовом слое**. Несколько лишних кликов.



# Об авторах

- [Николай Громов](http://nicothin.pro/contact). Технолог. Фрилансер. Преподаватель [EpicSkills](http://epixx.ru/) и [HTML Academy](https://htmlacademy.ru). Первый сайт сделал в 2000 г.
- [Андрей Алексеев](https://github.com/aalexeev239). Технолог. Фрилансер.
