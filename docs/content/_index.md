---
---

## Установка

Иконки Bootstrap публикуются в npm, но при необходимости их также можно загрузить вручную.

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### npm
Установите [Bootstrap Icons](https://www.npmjs.com/package/bootstrap-icons), включая SVG, спрайты иконок и шрифты иконок, с помощью npm. Затем выберите, кому Вы хотите добавить иконки в [инструкции по использованию](#использование).

{{< highlight sh >}}
npm i bootstrap-icons
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

Иконки Bootstrap - это SVG-файлы, поэтому Вы можете включать их в свой HTML несколькими способами в зависимости от того, как настроен Ваш проект. Иконки Bootstrap по умолчанию включают в себя `width` и `height` равную `1em`, чтобы можно было легко изменять размер с помощью `font-size`.

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### Встраивание
Встраивайте свои значки в HTML-код своей страницы (а не во внешний файл изображения). Здесь мы использовали нестандартные `width` и `height`.
{{< /md >}}
  </div>
  <div class="col-md-8">
    {{< example >}}<svg class="bi bi-chevron-right" width="32" height="32" viewBox="0 0 20 20" fill="currentColor" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M6.646 3.646a.5.5 0 01.708 0l6 6a.5.5 0 010 .708l-6 6a.5.5 0 01-.708-.708L12.293 10 6.646 4.354a.5.5 0 010-.708z"/></svg>{{< /example >}}
  </div>
</div>

<div class="row my-4">
  <div class="col-md-4">
{{< md >}}
### Спрайт
Используйте спрайт SVG для вставки любого иконки через элемент `<use>`. Используйте имя файла иконки в качестве идентификатора фрагмента (например, `toggles` это `#toggles`). Спрайты SVG позволяют ссылаться на внешний файл, аналогичный элементу `<img>`, но с мощью `currentColor` для упрощения тем.
{{< /md >}}
  </div>
  <div class="col-md-8">
{{< example >}}
<svg class="bi" width="32" height="32" fill="currentColor">
  <use xlink:href="bootstrap-icons.svg#heart-fill"/>
</svg>
<svg class="bi" width="32" height="32" fill="currentColor">
  <use xlink:href="bootstrap-icons.svg#toggles"/>
</svg>
<svg class="bi" width="32" height="32" fill="currentColor">
  <use xlink:href="bootstrap-icons.svg#shop"/>
</svg>
{{< /example >}}
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
    {{< example >}}<img src="/assets/img/bootstrap.svg" alt="Bootstrap" width="32" height="32">{{< /example >}}
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
      <svg class="bi bi-alert-triangle text-success" width="32" height="32" viewBox="0 0 20 20" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
        <path fill-rule="evenodd" d="M9.938 4.016a.146.146 0 00-.054.057L3.027 15.74a.176.176 0 00-.002.183c.016.03.037.05.054.06.015.01.034.017.066.017h13.713a.12.12 0 00.066-.017.163.163 0 00.055-.06.176.176 0 00-.003-.183L10.12 4.073a.146.146 0 00-.054-.057.13.13 0 00-.063-.016.13.13 0 00-.064.016zm1.043-.45a1.13 1.13 0 00-1.96 0L2.166 15.233c-.457.778.091 1.767.98 1.767h13.713c.889 0 1.438-.99.98-1.767L10.982 3.566z"/>
        <rect width="2" height="2" x="9.002" y="13" rx="1"/>
        <path d="M9.1 7.995a.905.905 0 111.8 0l-.35 3.507a.553.553 0 01-1.1 0L9.1 7.995z"/>
      </svg>
    </div>
{{< highlight html >}}
<svg class="bi bi-alert-triangle text-success" width="32" height="32" viewBox="0 0 20 20" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
  ...
</svg>
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
