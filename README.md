﻿# Приложение для вычисления математических выражений

[![Build Status](https://api.travis-ci.org/DmitriySidnev/Task_STC.svg?branch=master)](https://travis-ci.org/DmitriySidnev/Task_STC)

## Описание
Приложение выполняет вычисление математических выражений с "длинными" числами.
Ообенности приложения:

- Входной набор выражений задается во входном файле
- Результаты вычислений записываются в выходной файл
- Максимальное количество десятичных разрядов в числе - 1048576
- Допутимые математические операции и символы:
  - сложение '+'
  - вычитание '-'
  - умножение '*'
  - отрывающаяся скобка '('
  - закрывающаяся скобка ')'
  - унарный минус '-'
  - пробельный символ

- Кроме допустимых символов и цифр от 0 до 9 и символа 'пробел' другие символы в выражении не допускаются
- Если выражение является недопустимым или в процессе вычисления какое-либо число содержит больше, чем максимально допустимое число десяичных разрядов, то в качестве результата в выходном файле выводится сообщение "Invalid expression"
- В процессе работы приложения в консоли выводится процент обработки заданного набора выражений
- Выход из приложения осуществляется нажатием клавиши 'q'
- Посде завершения работы приложения в консоли выводится общее время его работы

## Внешние зависимости

Целевая ОС: Ubuntu.

Для корректной работы необходимо выполнить установку библиотеки ncurses:

```
> sudo apt-get install libncurses-dev
```
Для ОС Windows доступна библиотека PDCurses.

## Утановка

```
> git clone https://github.com/DmitriySidnev/Task_STC.git
> cd Task_STC
> git submodule init
> git submodule update
> mkdir build
> cd build
> cmake ..
> make
```

## Запуск

```
> cd bin
> ./task_arithmometer ../../data/in.txt ../../data/out.txt 4
> ./task_arithmometer ../../data/in_big.txt ../../data/out_big.txt
```

Для запуска приложения в качестве аргументов необходимо указать:

- путь к входному файлу с выражениями

- путь к выходному файлу для записи результатов

- количество потоков для обработки, если не указано то создается по одному потоку на ядро

## Пример входных/ выходных файлов

[Входной файл](https://github.com/DmitriySidnev/Task_STC/blob/master/data/in.txt)

[Выходной файл](https://github.com/DmitriySidnev/Task_STC/blob/master/data/out.txt)

## Запуск тестов

```
> cd bin
> ./tests
```
