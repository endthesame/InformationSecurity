---
# Front matter
title: "Лабораторная работа 5"
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

##### ПРЕЗЕНТАЦИЯ ПО ЛАБОРАТОРНОЙ РАБОТЕ №5

дисциплина: Информационная безопасность

Преподователь: Кулябов Дмитрий Сергеевич

Cтудент: Терентьев Егор Дмитриевич

Группа: НФИбд-01-19

МОСКВА

2022 г.

# **Прагматика выполнения лабораторной работы**

- Изучение механизмов изменения идентификаторов:
  1. Применения SetUID и SetGID
  2. Применения Sticky-битов.

# **Цель работы**

Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов.
Получение практических навыков работы в консоли с дополнительными атрибутами.
Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# **Выполнение лабораторной работы**

# 1. Создали программу simpleid

![simpleid](pics/2_simpleid.png "листинг simpleid")

# 2. Сравниваем id и simpleid

![id_simpleid](pics/3_id_simpleid.png "id simpleid")

# 3. Создаем simpleid2

![simpleid2](pics/4_simpleid2.png "simpleid2")

# 4. Запускаем simpleid2

![chown_chmod](pics/5_simpleid2_launch.png "simpleid2 launch")

# 5. Меняем chown и chmod

![chown_chmod_simpleid2](pics/6_su_chown_chmod.png "Меня права доступа и владельца файла")

# 6. Сравниваем id и simpleid2

![id_simpleid2](pics/7_ls_id_su.png "id simpleid2")

# 7. Создаем readfile

![readfile](pics/9_readfile.png "Создаем readfile")

# 8. Проверяем перезапись, удаление, переименование

Затем меняем владельца файла чтобы только суперпользователь мог прочитать его
и проверяем может ли пользователь прочитать readfile с помощью readfile.o

![readfile_readfile](pics/12_readfile_readfile.png "Читаем файл с помощью readfile")

# 9. Создаем файл test1 от guest и работаем с guest2

От пользователя guest2 (не являющегося владельцем) попробуйте прочитать файл /tmp/file01.txt
От пользователя guest2 попробуйте дозаписать в файл /tmp/file01.txt слово test2
Проверьте содержимое файла
От пользователя guest2 попробуйте записать в файл /tmp/file01.txt
Проверьте содержимое файла
От пользователя guest2 попробуйте удалить файл /tmp/file01.txt

##

![file1_guest2](pics/14_file1_guest2.png "Работа с файлом от guest2")

# 10. Снимаем sticky-bit

![guest2_without_stickybit](pics/15_guest2_without_stickybit.png "Снимаем sticky-bit  и работаем с файлом")

# Выводы

В результате выполнения работы я изученил механизмы изменения идентификаторов, применения SetUID- и Sticky-битов,
получил практические навыки работы в консоли с дополнительными атрибутами, а также
рассмотрел работы механизма смены идентификатора процессов пользователей и влияние бита Sticky на запись и удаление файлов.
