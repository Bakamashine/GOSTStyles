# GOSTStyles

Шаблон для оформления документов по ГОСТ с использованием XeLaTeX.

## Структура проекта

- `gost.sty` — основной пакет стилей: шрифты (Times New Roman, Consolas), геометрия страницы, заголовки, изображения, вёрстка кода
- `table.sty` — пакет для таблицы-штампа (основная надпись по ГОСТ) и рамки вокруг текста
- `border.sty` — альтернативный пакет для рамки вокруг страницы
- `main.tex` — пример основного документа

## Использование

```latex
\documentclass[a4paper, 14pt]{extarticle}
\usepackage{gost}
\usepackage{table}
\begin{document}
...
\end{document}
```

## Команды

- `\titleOne{...}` — заголовок уровня 1 (22pt, полужирный, верхний регистр)
- `\titleTwo{...}` — заголовок уровня 2 (22pt, полужирный)
- `\titleThree{...}` — заголовок уровня 3 (обычный размер, полужирный)
- `\image{path}{caption}` — вставка изображения с подписью
- `\smallImage{path}{caption}` — вставка изображения (0.5 ширины) с подписью
- `\imageWithoutCaption{path}` — вставка изображения без подписи
- `\MyVerbatim{file}` — вставка кода из файла в две колонки (7pt)
- `\MyVerbatimLarge{file}` — вставка кода из файла в две колонки (5pt)

## Сборка

```bash
xelatex -interaction=nonstopmode main.tex
```
