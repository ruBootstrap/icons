<p align="center">
  <a href="https://getbootstrap.com/">
    <img src="https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png" alt="Bootstrap logo" width="200" height="165">
  </a>
</p>

<h3 align="center">Bootstrap Icons</h3>

<p align="center">
  Официальная библиотека SVG-иконок с открытым исходным кодом для Bootstrap, содержащая более 2000 иконок.
  <br>
  <a href="https://icons.getbootstrap.su/"><strong>[RU] Обзор Иконок Bootstrap »</strong></a> | <a href="https://icons.getbootstrap.com/"><strong>[EN] Explore Bootstrap Icons »</strong></a>
  <br>
  <br>
  <a href="https://getbootstrap.su/">[RU] Bootstrap</a> | <a href="https://getbootstrap.com/">[EN] Bootstrap</a>
  ·
  <a href="https://themes.getbootstrap.com/">Темы</a>
  ·
  <a href="https://blog.getbootstrap.su/">[RU] Блог</a> | <a href="https://blog.getbootstrap.com/">[EN] Blog</a>
  <br>
</p>

[![Bootstrap Icons preview](https://github.com/twbs/icons/blob/main/.github/preview.png)](https://icons.getbootstrap.com/)

## Установка

Иконки Bootstrap упаковываются и публикуются в npm. Мы включаем в этот пакет только обработанные SVG - для Вас и Вашей команды. [Прочтите нашу документацию](https://icons.getbootstrap.su/) для получения инструкций по использованию.

```shell
npm i bootstrap-icons
```

Для тех, кто [использует Packagist](https://packagist.org/packages/twbs/bootstrap-icons), вы также можете установить значки Bootstrap через Composer:

```shell
composer require twbs/bootstrap-icons
```

[Также доступно в Figma](https://www.figma.com/community/file/1042482994486402696/Bootstrap-Icons).

## Использование

В зависимости от Ваших настроек Вы можете включать иконки Bootstrap несколькими способами.

- Копировать и вставлять SVG как встроенный HTML
- Ссылка через элемент `<img>`
- Использовать спрайт SVG
- Включить через CSS

[Смотрите документацию для получения дополнительной информации](https://icons.getbootstrap.com/#usage).

## Разработка

[![Статус сборки](https://img.shields.io/github/actions/workflow/status/twbs/icons/test.yml?branch=main&label=Tests&logo=github)](https://github.com/twbs/icons/actions/workflows/test.yml?query=workflow%3ATests+branch%3Amain)
[![Версия npm](https://img.shields.io/npm/v/bootstrap-icons?logo=npm&logoColor=fff)](https://www.npmjs.com/package/bootstrap-icons)

Клонируйте репозиторий, установите зависимости и запустите сервер Hugo локально.

```shell
git clone https://github.com/twbs/icons/
cd icons
npm i
npm start
```

Затем откройте в браузере `http://localhost:4000`.

### Скрипты npm

Вот несколько ключевых сценариев, которые вы будете использовать во время разработки. Обязательно просмотрите наши выходные данные `package.json` или `npm run`, чтобы получить полный список скриптов.

| Скрипт       | Описание                                                                             |
|--------------|--------------------------------------------------------------------------------------|
| `start`      | Псевдоним для запуска `docs-serve`                                                   |
| `docs-serve` | Запускает локальный сервер Hugo                                                      |
| `pages`      | Создает страницы с постоянными ссылками для каждой иконки с помощью шаблона Markdown |
| `icons`      | Обрабатывает и оптимизирует SVG в каталоге `icons`                                   |

## Добавление SVG

Иконки обычно добавляются только с помощью @mdo, но могут быть сделаны исключения. Новые глифы разрабатываются в Figma сначала в сетке 16x16 пикселей, а затем экспортируются как плоские SVG с заливкой `fill` (без обводки). После того, как новый значок SVG был добавлен в каталог `icons`, мы используем сценарий npm, чтобы:

1. Оптимизируйте наши SVG с помощью SVGO.
2. Измените исходный код SVG, удалив все атрибуты перед установкой новых атрибутов и значений в предпочтительном порядке.

Используйте `npm run icons` для запуска скрипта, запустите `npm run pages` для создания страниц с постоянными ссылками, заполните эти страницы и, наконец, зафиксируйте результаты в новой ветке для обновления.

**Warning**: Please exclude any auto-generated files, like `font/**` and `bootstrap-icons.svg` from your branch because they cause conflicts, and we generally update the dist files before a release.

## Публикация

Документация публикуется автоматически при публикации нового тега Git. Смотрите наши [GitHub Actions](https://github.com/twbs/icons/tree/main/.github/workflows) и [`package.json`](https://github.com/twbs/icons/blob/main/package.json) для получения дополнительной информации.

## Лицензия

MIT

## Автор

[@mdo](https://github.com/mdo)
