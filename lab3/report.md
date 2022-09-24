---
# Front matter
title: "Информационная безопасность. Отчет по лабораторной работе №3"
subtitle: "Дискреционное разграничение прав в Linux. Два пользователя"
author: "Терентьев Егор Дмитриевич 1032192875"
group: "НФИбд-01-19"
institute: RUDN University, Moscow, Russian Federation

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
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

# Цель работы

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей.

# Выполнение лабораторной работы

Добавляю второго пользователя и задаю ему пароль [@fig:1].

![guest2](pics/1_useradd_guest2.png){#fig:1 width=100%}

Добавил пользователя guest2 в группу guest

![Добавление guest2 в группу guest](pics/2_gpasswd_guest2.png){#fig:2 width=100%}

Осуществил вход в систему от двух пользователей на двух разных консолях: guest на первой консоли и guest2 на второй консоли.. [@fig:3].

![2 пользователя в консоли](pics/3_guests_console.png){#fig:3 width=100%}

Для первого пользователя определил директорию, группы, id [@fig:4]

![guest1 pwd groups id](pics/4_info_guest1.png){#fig:4 width=100%}

Для второго пользователя определил директорию, группы, id [@fig:5]

![guest2 pwd groups id](pics/5_info_guest2.png){#fig:5 width=100%}

Проверил содержимое файла group командой cat /etc/group вторым пользователем [@fig:6].

![cat /etc/group](pics/6_etc_group.png){#fig:6 width=100%}

От имени пользователя guest2 выполнил регистрацию пользователя guest2 в группе guest [@fig:7].

![регистрация пользователя guest2 в группе guest](pics/7_newgrp.png){#fig:7 width=100%}

От имени пользователя guest измените права директории /home/guest, разрешив все действия для пользователей группы
От имени пользователя guest снимите с директории /home/guest/dir1 все атрибуты [@fig:8]

![изменения атрибутов домашний директории и dir1](pics/8_chmod_homedir_dir1.png){#fig:8 width=100%}

Операции при установки директории атрибутов на chmod 000 [@fig:9].

![chmod 000 dir1](pics/9_table_000.png){#fig:9 width=100%}

Операции при установки директории атрибутов на chmod 100 [@fig:10].

![chmod 010 dir1](pics/10_table_010.png){#fig:10 width=100%}

Операции при установки директории атрибутов на chmod 200 [@fig:11].

![chmod 020 dir1](pics/11_table_020.png){#fig:11 width=100%}

Операции при установки директории атрибутов на chmod 300 [@fig:12]

![chmod 030 dir1](pics/12_table_030.png){#fig:12 width=100%}

Операции при установки директории атрибутов на chmod 400 [@fig:13]

![chmod 040 dir1](pics/13_table_040.png){#fig:13 width=100%}

Операции при установки директории атрибутов на chmod 500 [@fig:14].

![chmod 050 dir1](pics/14_table_050.png){#fig:14 width=100%}

Операции при установки директории атрибутов на chmod 600 [@fig:15].

![chmod 060 dir1](pics/15_table_060.png){#fig:15 width=100%}

Операции при установки директории атрибутов на chmod 700 [@fig:16].

![chmod 070 dir1](pics/16_table_070.png){#fig:16 width=100%}

На основании заполненной таблицы определите те или иные минимально необходимые права для выполнения операций внутри директории dir1 [@fig:17].

![min_access](pics/17_table_3_2.png){#fig:17 width=100%}

# Выводы

Приобретены практические навыки работы в консоли с атрибутами файлов для групп пользователей.

# Список литературы

1. Методические материалы курса
