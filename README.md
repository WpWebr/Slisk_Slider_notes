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

Option | Type | Default | Description
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

