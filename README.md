<p align="center">
  <a href="https://v5.getbootstrap.com/">
    <img src="https://v5.getbootstrap.com/docs/5.0/assets/brand/bootstrap-logo-shadow.png" alt="Bootstrap logo" width="200" height="165">
  </a>
</p>

<h3 align="center">Bootstrap Icons</h3>

<p align="center">
  Официальная библиотека иконок SVG с открытым исходным кодом для Bootstrap.
  <br>
  <a href="https://icons.getbootstrap.su/"><strong>[RU] Обзор Иконок Bootstrap »</strong></a> | <a href="https://icons.getbootstrap.su/"><strong>[EN] Explore Bootstrap Icons »</strong></a>
  <br>
  <br>
  <a href="https://getbootstrap.su/docs/5.0/">Bootstrap</a>
  ·
  <a href="https://themes.getbootstrap.com/">Темы</a>
  ·
  <a href="https://blog.getbootstrap.com/">Блог</a>
</p>

## 1,100+ icons

[![Полный набор иконок Bootstrap](https://github.com/twbs/icons/blob/main/.github/preview.png)](https://icons.getbootstrap.com)

[Также доступно в Figma.](https://www.figma.com/file/6jIgJymnRpMjGSMG2BKNRe/Bootstrap-Icons-v1.1.0?node-id=0%3A1)

## Установка

Иконки Bootstrap упаковываются и публикуются в npm. Мы включаем в этот пакет только обработанные SVG - для Вас и Вашей команды. [Прочтите нашу документацию](https://icons.getbootstrap.su/) для получения инструкций по использованию.

```shell
npm i bootstrap-icons --save
```

## Использование

В зависимости от Ваших настроек Вы можете включать иконки Bootstrap несколькими способами.

- Копировать и вставлять SVG как встроенный HTML
- Ссылка через элемент `<img>`
- Использовать спрайт SVG
- Включить через CSS

[См. документацию для получения дополнительной информации.](https://icons.getbootstrap.su/#использование)

## Development

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

После того, как новая иконка SVG была добавлена в каталог `icons`, Вам нужно будет их оптимизировать. Сценарий npm используется для:

1. Оптимизируйте наши SVG с помощью SVGO.
2. Измените исходный HTML-код SVG, удалив все атрибуты перед установкой новых атрибутов и значений в нашем предпочтительном порядке.

Используйте `npm run icons` для запуска скрипта, запустите `npm run pages` для создания страниц с постоянными ссылками, заполните эти страницы и, наконец, зафиксируйте результаты в новой ветке для обновления.

## Публикация

Документация публикуется автоматически при публикации нового тега Git. Смотрите наши [GitHub Actions](https://github.com/twbs/icons/tree/main/.github/workflows) и [`package.json`](https://github.com/twbs/icons/blob/main/package.json) для получения дополнительной информации.

## Лицензия

MIT

## Автор

[@mdo](https://github.com/mdo)
