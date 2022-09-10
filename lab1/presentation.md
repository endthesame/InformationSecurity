---
# Front matter
title: "Лабораторная работа 1"
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

##### ПРЕЗЕНТАЦИЯ ПО ЛАБОРАТОРНОЙ РАБОТЕ №1

дисциплина: Информационная безопасность

Преподователь: Кулябов Дмитрий Сергеевич

Cтудент: Терентьев Егор Дмитриевич

Группа: НФИбд-01-19

МОСКВА

2022 г.

# **Прагматика выполнения лабораторной работы**

- установка операционной системы Rocky
- анализ загрузки системы

# **Цель работы**

Установить операционную систему на виртуальную машину.
Проанализировать последовательность загрузки системы.

# **Выполнение лабораторной работы**

# 1. Успешная установка Rocky, вход в систему и подключение образа диска гостевой OC

![Rocky Linux](pics/18.png "Rocky Linux")

# 2. Проверка hostnamectl

![hostnamectl](pics/20_hostname.png "hostnamectl")

# 3. Добавление пользователя

![adduser](pics/21_adduser.png "add user")

# 1. Версия ядра Linux (Linux version)

Версия линукса: Linux 5.14.0-70.22.1.el9_0.x86_64

![Linux Version](pics/23_linuxver.png "Linux Version")

# 2. Частота процессора (Detected Mhz processor)

Примерно 3600 Мега герц.

![Detected Mhz processor](pics/24_mhzproc.png "Detected Mhz processor")

# 3. Модель процессора (CPU0)

Процессор - Ryzen 5 3600

![CPU0](pics/25_cpumodel.png "CPU0")

# 4. Объем доступной оперативной памяти (Memory available)

Свободной памяти 3.5 Гб из 4Гб.

![Memory available](pics/26_memoryav.png "Memory available")

# 5. Тип обнаруженного гипервизора (Hypervisor detected)

Hypervisor detected: KVM

![Hypervisor detected](pics/27_hypervisor.png "Hypervisor detected")

# 6. Тип файловой системы корневого раздела

Для sda1 - тип файловой системы XFS.

![XFS](pics/28_filesystem.png "XFS")

# 7. Последовательность монтирования файловых систем

Сначала монтируется Huge Pages FS, POSIX Message Queue FS, Kernel Debug FS, Kernel Trace FS и наконец Root and Kernel FS

![Mount FileSystem](pics/29_mounting.png "Mount FileSystem")

# Выводы

Выполнив данную лабораторную работу, я установил Rocky на виртуальную машину, а также изучил последовательность загрузки операционной системы.
