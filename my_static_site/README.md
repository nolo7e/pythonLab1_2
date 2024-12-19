# Мой кастомный статичный сайт на MkDocs

## Описание проекта

Этот проект представляет собой статичный сайт, созданный с помощью **MkDocs** с кастомной темой на основе **HTML**, **CSS** и **JavaScript**. Сайт включает автоматизированный процесс сборки и деплоя на **GitHub Pages** с использованием **GitHub Actions**.

### Основные возможности

- Кастомная тема с собственным `base.html`, `header.html` и `footer.html`.
- Стилизация на чистом CSS с минификацией через **PostCSS**.
- Интерактивность на JavaScript с минификацией через **Terser**.
- Автоматическая валидация и минификация HTML через **html-minifier-terser**.
- CI/CD пайплайн для сборки и деплоя на **GitHub Pages**.

---

## Структура проекта

```
python-static-site/
├── .github/
│   └── workflows/
│       └── gh-pages.yml       # GitHub Actions workflow для сборки и деплоя
├── custom_theme/
│   ├── base.html              # Основной шаблон
│   ├── static/
│   │   ├── main.min.css       # Минифицированный CSS
│   │   ├── main.min.js        # Минифицированный JS
│   │   ├── main.css           # Исходный CSS
│   │   └── main.js            # Исходный JS
│   └── overrides/
│       ├── header.html        # Кастомный header
│       └── footer.html        # Кастомный footer
├── my_static_site/
│   ├── index.md               # Главная страница
│   ├── about/
│   │   └── index.md           # Страница "Обо мне"
│   ├── projects/
│   │   └── index.md           # Страница "Проекты"
│   ├── blog/
│   │   └── index.md           # Страница "Блог"
│   └── contact/
│       └── index.md           # Страница "Контакты"
├── .gitignore                 # Игнор файлов
├── mkdocs.yml                 # Конфигурация MkDocs
├── package-lock.json          # Lock-файл для Node
├── package.json               # Скрипты для сборки и минификации
└── postcss.config.js          # Конфиг для плагина Post-CSS
```

---

## Инструкции по сборке и деплою

### Установка зависимостей

1. **Установка Python-зависимостей**:

   ```bash
   pip install mkdocs
   ```

2. **Установка Node.js-зависимостей**:

   ```bash
   npm install
   ```

### Сборка проекта

Выполните команду для сборки CSS, JS и сайта:

```bash
npm run build
```

### Запуск локального сервера

Для запуска локального сервера MkDocs:

```bash
mkdocs serve
```

Сайт будет доступен по адресу: [http://localhost:8000](http://localhost:8000)

---

## Описание GitHub Actions Workflow

### Файл `.github/workflows/gh-pages.yml`

Этот workflow автоматически выполняет следующие шаги:

1. **Устанавливает зависимости** для Python и Node.js.
2. **Собирает и минифицирует CSS и JS**.
3. **Собирает сайт с MkDocs**.
4. **Валидирует и минифицирует HTML**.
5. **Деплоит сайт на GitHub Pages**.

---

## Валидация и минификация

- **CSS**: Минифицируется с помощью **PostCSS** (`cssnano`).
- **JavaScript**: Минифицируется с помощью **Terser**.
- **HTML**: Валидируется и минифицируется с помощью **html-minifier-terser**.

---

## Результат

Сайт доступен по ссылке: [GitHub Pages](https://artcherenkov.github.io/python-static-site/)

Репозиторий: [GitHub Repository](https://github.com/artcherenkov/python-static-site)
