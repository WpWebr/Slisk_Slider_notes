#  Slisk Slider - шпаргалка

- [Официальный сайт](https://kenwheeler.github.io/slick/)
- [GitHub](https://github.com/kenwheeler/slick/)

## УСТАНОВКА

[Скачать](https://github.com/kenwheeler/slick/archive/v1.8.1.zip)

### NPM
>npm install slick-carousel

### CSS
```html
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
```
### JS
```html
<script type="text/javascript" src="//cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.min.js"></script>
```
### HTML

- Начиная с версии 1.5 можно добавлять настройки, используя атрибут data-slick. 
- Вам все равно нужно вызвать $(element).slick() для инициализации слайдера.

```html
<div data-slick='{"slidesToShow": 4, "slidesToScroll": 4}'>
  <div><h3>1</h3></div>
  <div><h3>2</h3></div>
  <div><h3>3</h3></div>
  <div><h3>4</h3></div>
  <div><h3>5</h3></div>
  <div><h3>6</h3></div>
</div>
```

### JS

##### Пример адаптивного варианта

```javascript
$(".slider").slick({

  // обычный
  infinite: false,

  // адаптивный вариант
  responsive: [{

      breakpoint: 1024,
      settings: {
        slidesToShow: 3,
        infinite: true
      }

    }, {

      breakpoint: 600,
      settings: {
        slidesToShow: 2,
        dots: true
      }

    }, {

      breakpoint: 300,
      settings: "unslick" // отключает слайдер

    }]
});
```

### Settings

Вариант | Тип | По умолчанию | Описание
------ | ---- | ------- | -----------
accessibility | boolean | true | Включает навигацию с помощью табуляции и клавиш со стрелками. Если `autoplay: true`, фокус браузера устанавливается на текущий слайд (или первый из текущего набора слайдов, если несколько `slidesToShow`) после смены слайдов. Для полного соответствия требованиям в дополнение к этому включите focusOnChange.
adaptiveHeight | boolean | false | Адаптирует высоту слайдера к текущему слайду
appendArrows | string | $(element) | Измените место прикрепления стрелок навигации (Селектор, htmlString, Массив, Элемент, объект jQuery)
appendDots | string | $(element) | Измените место прикрепления точек навигации (Селектор, htmlString, Массив, Элемент, объект jQuery)
arrows | boolean | true | Включить стрелки «Следующий/Предыдущий»
asNavFor | string | $(element) | Включает синхронизацию нескольких слайдеров
autoplay | boolean | false | Включает автоматическое воспроизведение слайдов.
autoplaySpeed | int  | 3000 | Интервал изменения автоматического воспроизведения
centerMode | boolean | false | Включает центрированный просмотр с частичными предыдущими и следующими слайдами. Используйте с нечетными номерами слайдовToShow.
centerPadding | string | '50px' | Padding в центральном режиме. (px или %)
cssEase | string |  'ease' | CSS3 анимация
customPaging | function | n/a | Пользовательские шаблоны страниц. См. источник для примера использования.
dots | boolean | false | Включить точки индикатора слайда
dotsClass | string | 'slick-dots' | Класс для контейнера точек 
draggable | boolean | true | Включает перетаскивание рабочего стола
easing | string |  'linear' | animate() резервное замедление
edgeFriction | integer | 0.15 | Сопротивление при смахивании по краям не бесконечной карусели
fade | boolean | false | Включает затухание
focusOnSelect | boolean | false | Включить фокус на выбранном элементе (нажмите)
focusOnChange | boolean | false | Перемещает фокус на слайд после изменения
infinite | boolean | true | Бесконечный цикл
initialSlide | integer | 0 | Слайд, чтобы начать
lazyLoad | string | 'ondemand' | Принимает режим «по требованию» или «прогрессивный» для техники отложенной загрузки. «ondemand» загрузит изображение, как только вы к нему подведете, «прогрессивный» загружает одно изображение за другим при загрузке страницы.
mobileFirst | boolean | false | В адаптивных настройках используется расчет «сначала для мобильных устройств».
nextArrow | string (html \| jQuery selector) \| object (DOM node \| jQuery object) | `<button type="button" class="slick-next">Далее</button>` | Позволяет выбрать узел или настроить HTML для стрелки «Далее».
pauseOnDotsHover | boolean | false | Приостанавливает автозапуск при наведении курсора на точку
pauseOnFocus | boolean | true | Приостанавливает автовоспроизведение, когда ползунок находится в фокусе
pauseOnHover | boolean | true | Приостанавливает автозапуск при наведении
prevArrow | string (html \| jQuery selector) \| object (DOM node \| jQuery object) | `<button type="button" class="slick-prev">Назад</button>` | Позволяет выбрать узел или настроить HTML для стрелки «Назад».
respondTo | string | 'window' | Ширина, на которую реагирует адаптивный объект. Может быть 'window', 'slider' или 'min' (меньшее из двух).
responsive | array | null | Массив объектов [содержащий точки останова и объекты настроек (см. пример)](#Пример-адаптивного-варианта). Включает настройки в данной «точке останова». Установите для `settings` значение "unslick" вместо объекта, чтобы отключить слайдер в заданной точке останова.
rows | int | 1 | Установка значения более 1 инициализирует режим сетки. ИспользуйтеlidesPerRow, чтобы указать, сколько слайдов должно быть в каждой строке.
rtl | boolean | false | Измените направление ползунка, чтобы оно двигалось справа налево.
slide | string | '' | Запрос элемента слайда
slidesPerRow | int | 1 | Если режим сетки инициализирован с помощью параметра строк, он устанавливает количество слайдов в каждой строке сетки.
slidesToScroll | int | 1 | Количество слайдов для одновременной прокрутки
slidesToShow | int | 1 | Количество слайдов для одновременного показа
speed | int | 300 | Скорость перехода
swipe | boolean | true | Включает сенсорное пролистывание
swipeToSlide | boolean | false | Проведите пальцем по слайду независимо от слайдовToScroll
touchMove | boolean | true | Позволяет перемещать слайды касанием
touchThreshold | int | 5 | Для перемещения по слайдам пользователь должен провести длину (1/touchThreshold) * от ширины слайдера.
useCSS | boolean | true | Включить/отключить переходы CSS
useTransform | boolean | true | Включить/отключить преобразования CSS
variableWidth | boolean | false | Отключает автоматический расчет ширины слайда.
vertical | boolean | false | Вертикальное направление слайда
verticalSwiping | boolean | false | Меняет направление свайпа на вертикальное
waitForAnimate | boolean | true | Игнорирует запросы на продвижение слайда во время анимации.
zIndex | number | 1000 | Установите значения zIndex для слайдов, что полезно для IE9 и более ранних версий.

### События ( Events )

В версии 1.4 методы обратного вызова устарели и были заменены событиями. Используйте их перед инициализацией слика, как показано ниже:

```javascript
// При событии смахивания
$('.your-element').on('swipe', function(event, slick, direction){
  console.log(direction);
  // left
});

// На грани удара
$('.your-element').on('edge', function(event, slick, direction){
  console.log('edge was hit')
});

// Включается перед сменой слайдов
$('.your-element').on('beforeChange', function(event, slick, currentSlide, nextSlide){
  console.log(nextSlide);
});
```

Событие | Параметры | Описание
------ | -------- | -----------
afterChange | event, slick, currentSlide | Обратный вызов после смены слайда
beforeChange | event, slick, currentSlide, nextSlide | Обратный вызов перед сменой слайда
breakpoint | event, slick, breakpoint | Срабатывает после достижения точки останова
destroy | event, slick | Когда слайдер разрушен или снят с места.
edge | event, slick, direction | Срабатывает, когда край прокручивается в небесконечном режиме.
init | event, slick | Когда Slick впервые инициализирует обратный вызов. Обратите внимание, что это событие должно быть определено до инициализации ползунка.
reInit | event, slick | Каждый раз, когда Slick (повторно) инициализирует обратный вызов
setPosition | event, slick | Каждый раз, когда Slick пересчитывает позицию
swipe | event, slick, direction | Срабатывает после смахивания/перетаскивания
lazyLoaded | event, slick, image, imageSource | Срабатывает после ленивой загрузки изображения
lazyLoadError | event, slick, image, imageSource | Срабатывает после того, как изображение не загружается

#### Методы ( Methods )

Методы вызываются в экземплярах slick через сам метод slick в версии 1.4, см. ниже:

```javascript
// Добавить слайд
$('.your-element').slick('slickAdd',"<div></div>");

// Получить текущий слайд
var currentSlide = $('.your-element').slick('slickCurrentSlide');
```

Этот новый синтаксис позволяет вам также вызывать любой внутренний метод:

```javascript
// Обновить положение слайдера вручную
$('.your-element').slick('setPosition');
```


Метод | Аргумент | Описание
------ | -------- | -----------
`slick` | options : object | Initializes Slick
`unslick` |  | Destroys Slick
`slickNext` |  |  Triggers next slide
`slickPrev` | | Triggers previous slide
`slickPause` | | Pause Autoplay
`slickPlay` | | Start Autoplay (_will also set `autoplay` option to `true`_)
`slickGoTo` | index : int, dontAnimate : bool | Goes to slide by index, skipping animation if second parameter is set to true
`slickCurrentSlide` |  |  Returns the current slide index
`slickAdd` | element : html or DOM object, index: int, addBefore: bool | Add a slide. If an index is provided, will add at that index, or before if addBefore is set. If no index is provided, add to the end or to the beginning if addBefore is set. Accepts HTML String || Object
`slickRemove` | index: int, removeBefore: bool | Remove slide by index. If removeBefore is set true, remove slide preceding index, or the first slide if no index is specified. If removeBefore is set to false, remove the slide following index, or the last slide if no index is set.
`slickFilter` | filter : selector or function | Filters slides using jQuery .filter syntax
`slickUnfilter` | | Removes applied filter
`slickGetOption` | option : string(option name) | Gets an option value.
`slickSetOption` | change an option, `refresh` is always `boolean` and will update UI changes...
 | `option, value, refresh` | change a [single `option`](https://github.com/kenwheeler/slick#settings) to given `value`; `refresh` is optional.
 | `"responsive", [{ breakpoint: n, settings: {} }, ... ], refresh` | change or add [whole sets of responsive options](#responsive-option-example)
 | `{ option: value, option: value, ... }, refresh` | change  [multiple `option`s](https://github.com/kenwheeler/slick#settings) to corresponding `value`s.


#### Примеры

Инициализируйте с помощью:

```javascript
$(element).slick({
  dots: true,
  speed: 500
});
 ```

Измените скорость с помощью:

```javascript
$(element).slick('slickSetOption', 'speed', 5000, true);
```

Уничтожить с помощью:

```javascript
$(element).slick('unslick');
```

#### Переменные Sass

Variable | Type | Default | Description
------ | ---- | ------- | -----------
$slick-font-path | string | "./fonts/" | Путь к каталогу для иконочного шрифта
$slick-font-family | string | "slick" | Семейство шрифтов для иконочного шрифта
$slick-loader-path | string | "./" | Путь к каталогу для образа загрузчика
$slick-arrow-color | color | white | Цвет значков стрелок влево/вправо
$slick-dot-color | color | black | Цвет навигационных точек
$slick-dot-color-active | color | $slick-dot-color | Цвет активной навигационной точки
$slick-prev-character | string | '\2190' | Код символа Юникода для значка предыдущей стрелки
$slick-next-character | string | '\2192' | Код символа Юникода для значка следующей стрелки
$slick-dot-character | string | '\2022' | Код символов Юникода для значка навигационной точки
$slick-dot-size | pixels | 6px | Размер навигационных точек

#### Поддержка в браузерах

Slick работает в IE8+, а также в других современных браузерах, таких как Chrome, Firefox и Safari.

#### Зависимости

jQuery 1.7