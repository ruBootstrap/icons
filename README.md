<p align="center">
  <a href="https://v5.getbootstrap.com/">
    <img src="https://v5.getbootstrap.com/docs/5.0/assets/brand/bootstrap-logo-shadow.png" alt="Bootstrap logo" width="200" height="165">
  </a>
</p>

<h3 align="center">Bootstrap Icons</h3>

<p align="center">
  Официальная библиотека иконок SVG с открытым исходным кодом для Bootstrap с более чем 1300 иконок.
  <br>
  <a href="https://icons.getbootstrap.su/"><strong>[RU] Обзор Иконок Bootstrap »</strong></a> | <a href="https://icons.getbootstrap.su/"><strong>[EN] Explore Bootstrap Icons »</strong></a>
  <br>
  <br>
  <a href="https://getbootstrap.su/">Bootstrap</a>
  ·
  <a href="https://themes.getbootstrap.com/">Темы</a>
  ·
  <a href="https://blog.getbootstrap.com/">Блог</a>
  <br>
</p>

[![Bootstrap Icons preview](https://github.com/twbs/icons/blob/main/.github/preview.png)](https://icons.getbootstrap.com)

## Установка

Иконки Bootstrap упаковываются и публикуются в npm. Мы включаем в этот пакет только обработанные SVG - для Вас и Вашей команды. [Прочтите нашу документацию](https://icons.getbootstrap.su/) для получения инструкций по использованию.

```shell
npm i bootstrap-icons
```

[Также доступно в Figma.](https://www.figma.com/community/file/972989644486753519/Bootstrap-Icons-v1.5.0)

## Использование

В зависимости от Ваших настроек Вы можете включать иконки Bootstrap несколькими способами.

- Копировать и вставлять SVG как встроенный HTML
- Ссылка через элемент `<img>`
- Использовать спрайт SVG
- Включить через CSS

[См. документацию для получения дополнительной информации.](https://icons.getbootstrap.su/#использование)

## Разработка

[![Статус сборки](https://github.com/twbs/icons/workflows/Tests/badge.svg)](https://github.com/twbs/icons/actions?workflow=Tests)

Клонируйте репозиторий, установите зависимости и запустите сервер Hugo локально.

```shell
git clone https://github.com/twbs/icons/
cd icons
npm i
npm start
```

Затем откройте в браузере `http://localhost:4000`.

### Скрипты npm

Вот несколько ключевых сценариев, которые Вы будете использовать во время разработки. Не забудьте заглянуть в наш `package.json` для получения полного списка скриптов.

| Скрипт       | Описание |
| ------------ | --- |
| `start`      | Псевдоним для запуска `docs-serve` |
| `docs-serve` | Запускает локальный сервер Hugo |
| `pages`      | Создает страницы с постоянными ссылками для каждой иконки с помощью шаблона Markdown |
| `icons`      | Обрабатывает и оптимизирует SVG в каталоге `icons` |

## Добавление SVG

Иконки обычно добавляются только с помощью @mdo, но могут быть сделаны исключения. Новые глифы разрабатываются в Figma сначала в сетке 16x16 пикселей, а затем экспортируются как плоские SVG с заливкой `fill` (без обводки). После того, как новый значок SVG был добавлен в каталог `icons`, мы используем сценарий npm, чтобы:

1. Оптимизируйте наши SVG с помощью SVGO.
2. Измените исходный HTML-код SVG, удалив все атрибуты перед установкой новых атрибутов и значений в нашем предпочтительном порядке.

Используйте `npm run icons` для запуска скрипта, запустите `npm run pages` для создания страниц с постоянными ссылками, заполните эти страницы и, наконец, зафиксируйте результаты в новой ветке для обновления.

## Публикация

Документация публикуется автоматически при публикации нового тега Git. Смотрите наши [GitHub Actions](https://github.com/twbs/icons/tree/main/.github/workflows) и [`package.json`](https://github.com/twbs/icons/blob/main/package.json) для получения дополнительной информации.

## Лицензия

MIT

## Автор

[@mdo](https://github.com/mdo)
