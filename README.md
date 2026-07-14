# Jupyter Notebook Extensions — Миграция на JupyterLab / Notebook 7

## Описание

Репозиторий содержит 58 расширений для классического Jupyter Notebook (v4.x–5.x) и таблицу совместимости с современными версиями JupyterLab 4.x и Notebook 7.6.x.

Исходные коды всех расширений сохранены в папке `backup_extensions/` для дальнейшей переработки.

---

## Таблица совместимости: все 58 расширений

| <span style="color:#2196F3">#</span> | <span style="color:#2196F3">Расширение</span> | <span style="color:#2196F3">Что делает</span> | <span style="color:#2196F3">NB7</span> | <span style="color:#2196F3">JupyterLab</span> |
|---|-----------|-----------|-----|------------|
| 1 | **Table of Contents (2)** | Оглавление ноутбука из заголовков | Встроено: View → Table of Contents | Встроено: View → Table of Contents |
| 2 | **Collapsible Headings** | Сворачивание секций по markdown-заголовкам | Встроено: клик по ▶ в ToC | Встроено: клик по ▶ в ToC |
| 3 | **Code Folding** | Сворачивание кода по отступам/скобкам | Можно доработать 🟢 (CodeMirror API) | Встроено: Settings → Settings Editor → Notebook → Code Cell Configuration → Code Folding |
| 4 | **Code Folding (Editor)** | Сворачивание в редакторе файлов | Можно доработать 🟢 (CodeMirror API) | Встроено: Settings → Settings Editor → Text Editor → Editor configuration → Code Folding |
| 5 | **Variable Inspector** | Окно переменных ядра (имя, тип, значение) | Можно поставить: pip install lckr-jupyterlab-variableinspector | Можно поставить: pip install lckr-jupyterlab-variableinspector |
| 6 | **ExecuteTime** | Время выполнения ячейки | Можно поставить: pip install jupyterlab-execute-time | Можно поставить: pip install jupyterlab-execute-time |
| 7 | **Hinterland** | Автодополнение кода при вводе | Можно поставить: pip install jupyterlab-lsp python-lsp-server | Можно поставить: pip install jupyterlab-lsp python-lsp-server |
| 8 | **Snippets** | Вставка сниппетов из выпадающего меню | Можно доработать 🟡 (нужен UI-компонент) | Можно поставить: pip install elyra |
| 9 | **Snippets Menu** | Меню сниппетов для Python/NumPy/Matplotlib | Можно доработать 🟡 (нужен UI-компонент) | Можно поставить: pip install jupyterlab-code-snippets |
| 10 | **Freeze** | Блокировка ячеек (только чтение/полная заморозка) | Можно поставить: pip install jupyterlab-freeze | Можно поставить: pip install jupyterlab-freeze |
| 11 | **Comment/Uncomment** | Горячая клавиша комментирования строк | Можно доработать 🟡 (шорткат + CodeMirror) | Встроено: настраивается в Keyboard Shortcuts |
| 12 | **Navigation Hotkeys** | Расширенные шорткаты навигации | Можно доработать 🟡 (шорткаты) | Встроено: настраивается в Keyboard Shortcuts |
| 13 | **Zen Mode** | Минималистичный режим без лишних элементов | Можно доработать 🟡 (скрытие UI) | Встроено: View → Simple Interface |
| 14 | **Limit Output** | Ограничение вывода ячейки | Можно поставить: pip install jupyterlab-limit-output | Можно поставить: pip install jupyterlab-limit-output |
| 15 | **Hide Header** | Скрытие шапки (меню, тулбар) | Можно доработать 🟢 (только CSS) | Встроено: View → Simple Interface |
| 16 | **Hide Input** | Скрытие кода отдельной ячейки | Можно доработать 🟡 (metadata + CSS) | Встроено: View → Collapse Selected Code |
| 17 | **Hide Input All** | Скрытие кода всех ячеек | Можно доработать 🟡 (metadata + CSS) | Встроено: View → Collapse All Code |
| 18 | **Scratchpad** | Песочница для кода (отдельная область) | Встроено: Run → Create Console for Notebook | Встроено: Code Console |
| 19 | **Ruler** | Вертикальная линия-ориентир (80 символов) | Можно доработать 🟡 (CodeMirror API) | Встроено: Settings → codeCellConfig.rulers |
| 20 | **Python Markdown** | Вставка переменных Python в Markdown | Можно доработать 🔴 (kernel + renderer) | Можно доработать 🔴 (kernel + renderer) |
| 21 | **Gist-it** | Публикация ноутбука как GitHub Gist | Можно доработать 🟡 (GitHub API) | Можно доработать 🟡 (GitHub API) |
| 22 | **Printview** | Конвертация в HTML/PDF в новой вкладке | Можно доработать 🟡 (nbconvert API) | Встроено: File → Export Notebook As |
| 23 | **Runtools** | Продвинутое выполнение (диапазон, помеченные) | Встроено частично: Run → Run All Above/Below | Встроено: Run → Run All Above/Below |
| 24 | **Keyboard Shortcut Editor** | Редактирование шорткатов через диалог | Можно доработать 🔴 (settings API) | Встроено: Settings → Keyboard Shortcuts |
| 25 | **Highlighter** | Подсветка текста в Markdown цветами | Можно доработать 🟡 (markdown extension) | Можно доработать 🟡 (markdown extension) |
| 26 | **Spellchecker** | Проверка орфографии в Markdown | Можно поставить: pip install jupyterlab-spellchecker | Можно поставить: pip install jupyterlab-spellchecker |
| 27 | **Split Cells** | Разделение ячейки на две части | Можно поставить: pip install jupyterlab-gridwidth | Можно поставить: pip install jupyterlab-gridwidth |
| 28 | **Table Beautifier** | Стилизация таблиц Bootstrap-ом | Можно доработать 🟢 (только CSS) | Можно доработать 🟢 (только CSS) |
| 29 | **Select Keymap** | Выбор раскладки CodeMirror (vim/emacs) | Можно поставить: pip install jupyterlab-vim | Можно поставить: pip install jupyterlab-vim |
| 30 | **Toggle Line Numbers** | Показ/скрытие номеров строк | Встроено: View → Show Line Numbers | Встроено: View → Show Line Numbers |
| 31 | **AddBefore** | Вставка ячейки перед текущей | Встроено: Escape → A | Встроено: A в command mode |
| 32 | **AutoSave Time** | Интервал автосохранения | Можно доработать 🟢 (settings) | Встроено: Settings → Autosave interval |
| 33 | **Autoscroll** | Порог автопрокрутки вывода | Можно доработать 🟡 (observer) | Можно доработать 🟡 (observer) |
| 34 | **Cell Filter** | Фильтрация ячеек по тегам | Можно доработать 🟡 (metadata API) | Частично встроено в ToC |
| 35 | **Code Font Size** | Размер шрифта кода (кнопки +/−) | Можно доработать 🟢 (CSS) | Встроено: Settings → Theme |
| 36 | **CodeMirror Mode Extensions** | Расширения Octave/MATLAB | Можно доработать 🟢 (CodeMirror modes) | Можно доработать 🟢 (установить modes отдельно) |
| 37 | **CSS Selector** | Выбор темы из выпадающего списка | Можно доработать 🟢 (CSS) | Встроено: Settings → Theme |
| 38 | **Datestamper** | Вставка текущей даты/времени | Можно доработать 🟢 (кнопка + kernel) | Можно доработать 🟢 (кнопка + kernel) |
| 39 | **Equation Numbering** | Автонумерация формул MathJax | Можно доработать 🟡 (MathJax config) | Можно доработать 🟡 (MathJax config) |
| 40 | **Exercise** | Скрытие решений (виджет +/−) | Можно доработать 🔴 (cell grouping UI) | Можно доработать 🔴 (cell grouping UI) |
| 41 | **Exercise2** | Скрытие решений (чекбокс) | Можно доработать 🔴 (cell grouping UI) | Можно доработать 🔴 (cell grouping UI) |
| 42 | **Export Embedded HTML** | Экспорт с встроенными картинками | Можно доработать 🟡 (nbconvert) | Встроено: File → Export Notebook As |
| 43 | **Go to Running Cell** | Навигация к выполняемой ячейке (Alt-I) | Можно доработать 🟡 (kernel status) | Можно доработать 🟡 (kernel status) |
| 44 | **Help Panel** | Панель со справкой по шорткатам | Можно доработать 🟢 (simple panel) | Встроено: Help → Keyboard Shortcuts |
| 45 | **Load TeX Macros** | Загрузка LaTeX-макросов из файла | Можно доработать 🟡 (file loader) | Можно доработать 🟡 (file loader) |
| 46 | **Move Selected Cells** | Перемещение ячеек вверх/вниз | Встроено: Edit → Move Cells Up/Down | Встроено: Edit → Move Cells Up/Down |
| 47 | **nbTranslate** | Перевод ноутбуков / многоязычный режим | Можно доработать 🔴 (UI + translation API) | Можно доработать 🔴 (UI + translation API) |
| 48 | **Notify** | Браузерное уведомление при свободном ядре | Можно поставить: pip install jupyterlab-notifications | Можно поставить: pip install jupyterlab-notifications |
| 49 | **QTConsole** | Запуск QtConsole из интерфейса | Можно доработать 🟡 (external app) | Можно доработать 🟡 (external app) |
| 50 | **Rubberband** | Множественный выбор мышью | Встроено: Shift + клик | Встроено: Shift + клик |
| 51 | **Scroll Down** | Автопрокрутка вывода вниз | Можно доработать 🟢 (observer) | Можно доработать 🟢 (observer) |
| 52 | **SKILL Syntax** | Подсветка SKILL (Cadence EDA) | Можно доработать 🟢 (CodeMirror mode) | Можно доработать 🟢 (CodeMirror mode) |
| 53 | **Skip-Traceback** | Сворачивание трассировок ошибок | Можно поставить: pip install jupyterlab-skip-traceback | Можно поставить: pip install jupyterlab-skip-traceback |
| 54 | **Tree Filter** | Фильтр файлов в дашборде | Можно доработать 🟡 (file browser API) | Встроено: Settings → fileNameSearcher |
| 55 | **Execution Dependencies** | Зависимости выполнения ячеек | Можно доработать 🔴 (DAG solver + kernel) | Можно доработать 🔴 (DAG solver + kernel) |
| 56 | **Live Markdown Preview** | Превью Markdown в реальном времени | Можно доработать 🟡 (split view) | Можно доработать 🟡 (split view) |
| 57 | **Init Cell** | Автовыполнение ячеек при запуске ядра | Можно доработать 🟡 (notebook API) | Можно поставить: pip install jupyterlab-autorun-cells |
| 58 | **Code Prettify** | Форматирование кода (autopep8/black) | Можно поставить: pip install jupyterlab-code-formatter black isort | Можно поставить: pip install jupyterlab-code-formatter black isort |

---

## Итого: что уже работает

| Платформа | Встроено + поставить | доработать 🟢 | доработать 🟡 | доработать 🔴 |
|-----------|---------------------|---------------|---------------|---------------|
| **NB7** | 18 | 12 | 17 | 6 |
| **JupyterLab** | 32 | 6 | 10 | 5 |

**JupyterLab покрывает 32 из 58 расширений без доработки (55%).**
**NB7 покрывает 18 из 58 расширений без доработки (31%).**

---

## Установка расширений для JupyterLab

```bash
pip install \
  jupyterlab-execute-time \
  jupyterlab-limit-output \
  jupyterlab-skip-traceback \
  jupyterlab-notifications \
  jupyterlab-spellchecker \
  jupyterlab-vim \
  jupyterlab-freeze \
  lckr-jupyterlab-variableinspector \
  jupyterlab-rise \
  jupyterlab-code-formatter \
  black isort \
  python-lsp-server \
  jupyterlab-gridwidth
```

---

## Папка backup_extensions/

Содержит исходные коды всех 58 расширений для классического Jupyter Notebook. Используйте их как справочник при переработке расширений под JupyterLab / Notebook 7.

---

## Легенда

| Маркер | Значение |
|--------|----------|
| Встроено | Расширение уже есть в платформе |
| Можно поставить | Доступно через `pip install` |
| Можно доработать 🟢 | Низкая сложность (только CSS/UI) |
| Можно доработать 🟡 | Средняя сложность (нужен API/kernel) |
| Можно доработать 🔴 | Высокая сложность (сложная логика) |
