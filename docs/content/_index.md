---
aliases:
  - /font/
---

## Установка

Иконки Bootstrap публикуются в npm, но при необходимости их также можно загрузить вручную.

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### Менеджер пакетов
Установите [Bootstrap Icons](https://www.npmjs.com/package/bootstrap-icons), включая SVG, спрайты иконок и шрифты иконок, с помощью npm или Composer. Затем выберите, кому Вы хотите добавить иконки в [инструкции по использованию](#использование).

{{< highlight sh >}}
npm i bootstrap-icons
{{< /highlight >}}
{{< highlight sh >}}
composer require twbs/bootstrap-icons
{{< /highlight >}}
{{< /md >}}

  </div>
  <div class="col-md-4">
{{< md >}}
### Скачать
[Релизы публикуются на GitHub](https://github.com/twbs/icons/releases/) и включают иконки SVG, шрифты, лицензию и файл readme. Наш `package.json` также включен, хотя наши сценарии npm в основном доступны для наших рабочих процессов разработки.

{{< highlight css >}}
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@{{< param version >}}/font/bootstrap-icons.css");
{{< /highlight >}}
{{< /md >}}

  </div>
  <div class="col-md-4">
{{< md >}}
### CDN
Включите таблицу стилей шрифтов иконок - на свой веб-сайт `<head>` или через `@import` в CSS - из нашей CDN и приступайте к работе за секунды. [Смотрите документацию по шрифтам иконок](#шрифт-иконки) для примеров.

{{< highlight html >}}

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@{{< param version >}}/font/bootstrap-icons.css">
{{< /highlight >}}

{{< highlight css >}}
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@{{< param version >}}/font/bootstrap-icons.css");
{{< /highlight >}}
{{< /md >}}

  </div>
</div>

## Использование

Иконки Bootstrap - это SVG, поэтому вы можете включить их в свой HTML несколькими способами в зависимости от того, как настроен ваш проект. Мы рекомендуем использовать `width: 1em` (и, возможно, `height: 1em`) для легкого изменения размера с помощью `font-size`.

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### Встраивание
Встраивайте свои значки в HTML-код своей страницы (а не во внешний файл изображения). Здесь мы использовали нестандартные `width` и `height`.
{{< /md >}}
  </div>
  <div class="col-md-8">
    {{< example >}}<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-emoji-heart-eyes" viewBox="0 0 16 16"><path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z"/><path d="M11.315 10.014a.5.5 0 0 1 .548.736A4.498 4.498 0 0 1 7.965 13a4.498 4.498 0 0 1-3.898-2.25.5.5 0 0 1 .548-.736h.005l.017.005.067.015.252.055c.215.046.515.108.857.169.693.124 1.522.242 2.152.242.63 0 1.46-.118 2.152-.242a26.58 26.58 0 0 0 1.109-.224l.067-.015.017-.004.005-.002zM4.756 4.566c.763-1.424 4.02-.12.952 3.434-4.496-1.596-2.35-4.298-.952-3.434zm6.488 0c1.398-.864 3.544 1.838-.952 3.434-3.067-3.554.19-4.858.952-3.434z"/></svg>{{< /example >}}
  </div>
</div>

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### Спрайт
Используйте спрайт SVG для вставки любого иконки через элемент `<use>`. Используйте имя файла иконки в качестве идентификатора фрагмента (например, `toggles` это `#toggles`). Спрайты SVG позволяют ссылаться на внешний файл, аналогичный элементу `<img>`, но с мощью `currentColor` для упрощения тем.

**Внимание!** В Chrome проблема, из-за которой [`<use>` не работает в разных доменах](https://bugs.chromium.org/p/chromium/issues/detail?id=470601).
{{< /md >}}

  </div>
  <div class="col-md-8">

<div class="bd-example" style="font-size: 32px;">
  <i class="bi bi-heart-fill"></i>
  <i class="bi bi-toggles"></i>
  <i class="bi bi-shop"></i>
</div>
{{< highlight html >}}
<svg class="bi" width="32" height="32" fill="currentColor">
  <use xlink:href="bootstrap-icons.svg#heart-fill"/>
</svg>
<svg class="bi" width="32" height="32" fill="currentColor">
  <use xlink:href="bootstrap-icons.svg#toggles"/>
</svg>
<svg class="bi" width="32" height="32" fill="currentColor">
  <use xlink:href="bootstrap-icons.svg#shop"/>
</svg>
{{< /highlight >}}
  </div>
</div>

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### Внешнее изображение
Скопируйте SVG-файлы Bootstrap Icons в выбранный Вами каталог и укажите на них ссылки, как на обычные изображения, с помощью элемента `<img>`.
{{< /md >}}
  </div>
  <div class="col-md-8">
    {{< example >}}<img src="/assets/icons/bootstrap.svg" alt="Bootstrap" width="32" height="32">{{< /example >}}
  </div>
</div>

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### Шрифт иконки
Иконочные шрифты с классами для каждой иконки также включены в Bootstrap Icons. Включите веб-шрифты иконок на свою страницу с помощью CSS, затем укажите имена классов, если это необходимо в Вашем HTML (например, `<i class="bi-alarm-clock"></i>`).

Используйте `font-size` и `color`, чтобы изменить внешний вид иконки.
{{< /md >}}

  </div>
  <div class="col-md-8">
    {{< example >}}<i class="bi-alarm"></i>{{< /example >}}
    {{< example >}}<i class="bi-alarm" style="font-size: 2rem; color: cornflowerblue;"></i>{{< /example >}}
  </div>
</div>

<div class="row">
  <div class="col-md-4">
{{< md >}}
### CSS
Вы также можете использовать SVG в своем CSS (** обязательно экранируйте любые символы **, например, от `#` до `%23` при указании шестнадцатеричных значений цвета). Когда никакие размеры не указаны через `width` и `height` в `<svg>`, иконка заполнит доступное пространство.

Атрибут `viewBox` необходим, если Вы хотите изменить размер иконок с помощью `background-size`. Обратите внимание, что атрибут `xmlns` является обязательным.
{{< /md >}}

  </div>
  <div class="col-md-8">
{{< highlight css >}}
.bi::before {
  display: inline-block;
  content: "";
  vertical-align: -.125em;
  background-image: url("data:image/svg+xml,<svg viewBox='0 0 16 16' fill='%23333' xmlns='http://www.w3.org/2000/svg'><path fill-rule='evenodd' d='M8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z' clip-rule='evenodd'/></svg>");
  background-repeat: no-repeat;
  background-size: 1rem 1rem;
}

{{< /highlight >}}

  </div>
</div>

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
## Стилизация
Цвет можно изменить, установив класс `.text- *` или собственный CSS:
{{< /md >}}
  </div>
  <div class="col-md-8">
    <div class="bd-example">
      <svg class="bi bi-exclamation-triangle text-success" width="32" height="32" fill="currentColor" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg">
        <path d="M7.938 2.016A.13.13 0 0 1 8.002 2a.13.13 0 0 1 .063.016.146.146 0 0 1 .054.057l6.857 11.667c.036.06.035.124.002.183a.163.163 0 0 1-.054.06.116.116 0 0 1-.066.017H1.146a.115.115 0 0 1-.066-.017.163.163 0 0 1-.054-.06.176.176 0 0 1 .002-.183L7.884 2.073a.147.147 0 0 1 .054-.057zm1.044-.45a1.13 1.13 0 0 0-1.96 0L.165 13.233c-.457.778.091 1.767.98 1.767h13.713c.889 0 1.438-.99.98-1.767L8.982 1.566z"/>
        <path d="M7.002 12a1 1 0 1 1 2 0 1 1 0 0 1-2 0zM7.1 5.995a.905.905 0 1 1 1.8 0l-.35 3.507a.552.552 0 0 1-1.1 0L7.1 5.995z"/>
      </svg>
    </div>
{{< highlight html >}}
<svg class="bi bi-exclamation-triangle text-success" width="32" height="32" fill="currentColor" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg">
  ...
</svg>
{{< /highlight >}}
  </div>
</div>

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
## Доступность
Для чисто декоративных иконок добавьте `aria-hidden="true"`. В противном случае укажите соответствующую текстовую альтернативу. В зависимости от того, какой метод вы используете для добавления значков и где вы их используете (например, как отдельные изображения или как единственное содержимое кнопки или аналогичного элемента управления), возможны различные подходы. Вот несколько примеров:
{{< /md >}}
  </div>
  <div class="col-md-8">
    <div class="bd-example">
      <img src="/assets/icons/bootstrap.svg" alt="Bootstrap" width="32" height="32">
    </div>
{{< highlight html >}}
<!-- alt="..." на элементе <img> -->
<img src="/assets/icons/bootstrap.svg" alt="Bootstrap" ...>
{{< /highlight >}}
    <div class="bd-example">
      <i class="bi-github" role="img" style="font-size: 2em" aria-label="GitHub"></i>
      <i class="bi-tools" role="img" style="font-size: 2em" aria-label="Tools"></i>
    </div>
{{< highlight html >}}
<svg class="bi" ... role="img" aria-label="Tools">
  <use xlink:href="bootstrap-icons.svg#tools"/>
</svg>
{{< /highlight >}}
    <div class="bd-example">
      <button type="button" class="btn btn-primary" aria-label="Mute">
        <svg class="bi bi-volume-mute-fill" width="32" height="32" viewBox="0 0 16 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg" aria-hidden="true"><path d="M6.717 3.55A.5.5 0 017 4v8a.5.5 0 01-.812.39L3.825 10.5H1.5A.5.5 0 011 10V6a.5.5 0 01.5-.5h2.325l2.363-1.89a.5.5 0 01.529-.06zm7.137 2.096a.5.5 0 010 .708L12.207 8l1.647 1.646a.5.5 0 01-.708.708L11.5 8.707l-1.646 1.647a.5.5 0 01-.708-.708L10.793 8 9.146 6.354a.5.5 0 11.708-.708L11.5 7.293l1.646-1.647a.5.5 0 01.708 0z"></path></svg>
      </button>
    </div>
{{< highlight html >}}
<!-- aria-label="..." на контроле -->
<button ... aria-label="Mute">
  <svg class="bi bi-volume-mute-fill" aria-hidden="true" ...>
  ...
  </svg>
</button>
{{< /highlight >}}
  </div>
</div>

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
## Работа с SVG
С SVG приятно работать, но у них есть некоторые известные особенности, которые нужно обойти. Учитывая множество способов использования SVG, мы не включили эти атрибуты и обходные пути в наш код.
{{< /md >}}
  </div>
  <div class="col-md-8">
{{< md >}}
К известным проблемам относятся:

- **SVG получают фокус по умолчанию в Internet Explorer и Edge Legacy.** При встраивании SVG добавьте `focusable="false"` в элемент `<svg>`. [Подробнее на Stack Overflow.](https://stackoverflow.com/questions/18646111/disable-onfocus-event-for-svg-element)

- **При использовании SVG с элементами `<img>` программы чтения с экрана могут не объявлять их как изображения или полностью пропускать изображение.** Включите дополнительный `role="img"` в элемент `<img>`, чтобы избегать любых проблем. [Подробнее смотрите в этой статье.](https://simplyaccessible.com/article/7-solutions-svgs/#acc-heading-2)

- **Внешние спрайты SVG могут некорректно работать в Internet Explorer.** При необходимости используйте полифилл [svg4everybody](https://github.com/jonathantneal/svg4everybody).

Нашли еще одну проблему с SVG, которую следует отметить? Пожалуйста, откройте [вопрос]({{< param repo >}}/issues), чтобы поделиться подробностями.
{{< /md >}}

  </div>
</div>
