---
# Front matter
title: "Лабораторная работа 2"
author: "Терентьев Егор Дмитриевич, НФИбд-01-19"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

##### РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ

##### Факультет физико-математических и естественных наук

##### Кафедра прикладной информатики и теории вероятностей

##### ПРЕЗЕНТАЦИЯ ПО ЛАБОРАТОРНОЙ РАБОТЕ №2

дисциплина: Информационная безопасность

Преподователь: Кулябов Дмитрий Сергеевич

Cтудент: Терентьев Егор Дмитриевич

Группа: НФИбд-01-19

МОСКВА

2022 г.

# **Прагматика выполнения лабораторной работы**

- создание нового пользователя
- работа в консоли с атрибутами

# **Цель работы**

Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux.

# **Выполнение лабораторной работы**

# 1. Создание нового пользователя

![новый пользователь](pics/4_id_groups.png "id/groups")

# 2. Заполнение таблицы. Chmod 000 dir1

![Chmod_000_dir1](pics/11_dir000.png "Chmod 000 dir1")

# 3. Заполнение таблицы. Chmod 100 dir1

![Chmod_100_dir1](pics/12_dir100.png "Chmod 100 dir1")

# 4. Заполнение таблицы. Chmod 200 dir1

![Chmod_200_dir1](pics/13_dir200.png "Chmod 200 dir1")

# 5. Заполнение таблицы. Chmod 300 dir1

![Chmod_300_dir1](pics/14_dir300.png "Chmod 300 dir1")

# 6. Заполнение таблицы. Chmod 400 dir1

![Chmod_400_dir1](pics/15_dir400.png "Chmod 400 dir1")

# 7. Заполнение таблицы. Chmod 500 dir1

![Chmod_500_dir1](pics/16_dir500.png "Chmod 500 dir1")

# 8. Заполнение таблицы. Chmod 600 dir1

![Chmod_600_dir1](pics/17_dir600.png "Chmod 600 dir1")

# 9. Заполнение таблицы. Chmod 700 dir1

![Chmod_700_dir1](pics/18_dir700.png "Chmod 700 dir1")

# 10. Заполнение таблицы. Минимально необходимые права для выполнения операций внутри директории dir1

![min_access](pics/19_minaccess.png "Минимальные права для выполнения операций")

# Выводы

Выполнив данную лабораторную работу, я получил практические навыков работы в консоли с атрибутами файлов, закрепил теоретические основы дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux.
