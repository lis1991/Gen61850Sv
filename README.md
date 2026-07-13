# О проекте / About This Project

**🇷🇺 Русский**  
Этот репозиторий является активным форком оригинального проекта генератора/анализатора потоков IEC 61850-9-2 LE (Sampled Values). Оригинальный код, написанный несколько лет назад, устарел и имел критические проблемы с совместимостью на современных операционных системах (Windows 10/11, Visual Studio 2022, новые версии драйверов Npcap). 

**Цель этого форка** — доработать, модернизировать и сделать проект стабильным для повседневного использования, исправив архитектурные ошибки (например, привязку к IP-адресам вместо GUID сетевых адаптеров, устаревшие библиотеки WinPcap) и сохранив весь полезный функционал оригинала.

---

**🇬🇧 English**  
This repository is an active fork of the original IEC 61850-9-2 LE (Sampled Values) generator/capture project. The original code, written several years ago, is outdated and suffers from critical compatibility issues on modern operating systems (Windows 10/11, Visual Studio 2022, newer Npcap driver versions).

**The goal of this fork** is to refine, modernize, and stabilize the project for daily use by fixing architectural flaws (e.g., binding to IP addresses instead of network adapter GUIDs, outdated WinPcap libraries) while preserving all the useful functionality of the original tool.

> **Уважение к оригиналу / Respect to the original:**  
> Спасибо оригинальному автору за создание этого полезного инструмента. Данный форк создан исключительно с целью сохранить его актуальность и полезность для инженерного сообщества.  
> *We are grateful to the original author for creating this useful tool. This fork is created solely to keep it relevant and useful for the engineering community.*

---

### ⚠️Warning: seriously outdated⚠️
_Kept because some people still getting use of it_

This is IEC61850-9.2LE Software Generator.

Software can generate different shapes of voltages and currents, with bunch of editable parameters - amplitude, frequency, phase. Moreover, it can generate arbitrary waveform by defining harmonics amplitudes and phases.

Additionaly this software can be used to control sampled values stream on any network port. It has decoding module (it's not so efficient, but works well).

# Recent information interlude

This code is well-outdated, but I am getting requests from people want to run it on modern OSes. So I spent a little time to make it compile and work for Win7/10/11 with Qt 5.12.12.

The code itself is ugly AF (I was a student), so I just made necessary changes for network adapters to power on and work.

sln files were updated to be working with VS 2022 and 141 toolchain.

If you just want to play around - get latest release archive.

# Continue


Software ready to be launched on devices with sensor screens as it has virtual keyboard.

This tool also has some network-controlled parameters to remote control generation and signal params.

Additional information can be found in _documents folder.

Code have been being developed with Qt and Visual Studio (not needed to build). Using libpcap and qwt libs (included).
Note that it is not production-grade code, it's kinda handy tool for various manipulations with IEC61850-9.2. There is much C-like code in this masterpiece.

Works under Windows and Linux.

Distributed under Apache 2.0 license

**Please note** this is an embedded software, so some settings looks weird. To use generator/capture you must tweak settings.ini - `macFront` and `macRear`. Also I am not sure whether it works on newer Windows versions.

### ⚠️Предупреждение: крайне устарело⚠️
_Сохранено, так как некоторые люди всё ещё находят ему применение_

Это программный генератор IEC61850-9.2LE.

Программа может генерировать различные формы напряжений и токов с множеством редактируемых параметров: амплитудой, частотой и фазой. Более того, она может генерировать произвольную форму волны путем задания амплитуд и фаз гармоник.

Кроме того, это ПО можно использовать для контроля потока дискретизированных значений (Sampled Values) на любом сетевом порту. В нём присутствует модуль декодирования (не самый эффективный, но работает исправно).

# Небольшое отступление о свежих обновлениях

Этот код изрядно устарел, но я продолжаю получать запросы от людей, которые хотят запустить его на современных ОС. Поэтому я потратил немного времени, чтобы заставить его компилироваться и работать на Win7/10/11 с Qt 5.12.12.

Сам по себе код написан просто отвратительно (я был студентом), поэтому я внёс лишь минимально необходимые изменения, чтобы сетевые адаптеры инициализировались и работали.

Файлы `.sln` были обновлены для работы с Visual Studio 2022 и набором инструментов (toolchain) v141.

Если вы просто хотите поэкспериментировать — скачайте архив с последним релизом.

# Продолжение

Программа готова к запуску на устройствах с сенсорными экранами, так как в неё встроена виртуальная клавиатура.

Этот инструмент также поддерживает некоторые параметры, управляемые по сети, для удаленного контроля генерации и параметров сигнала.

Дополнительную информацию можно найти в папке `_documents`.

Код разрабатывался с использованием Qt и Visual Studio (хотя для сборки сам VS не обязателен). Используются библиотеки `libpcap` и `qwt` (включены в комплект).
Обратите внимание, что это не код промышленного уровня (production-grade), а скорее удобный инструмент для различных манипуляций с IEC61850-9.2. В этом «шедевре» очень много кода в стиле C.

Работает под Windows и Linux.

Распространяется по лицензии Apache 2.0.

**Обратите внимание:** это ПО изначально задумывалось как встраиваемое (embedded software), поэтому некоторые настройки выглядят странно. Чтобы использовать генератор/захват, вам обязательно нужно будет подправить файл `settings.ini`, а именно параметры `macFront` и `macRear`. Также я не уверен, работает ли это на более новых версиях Windows.
