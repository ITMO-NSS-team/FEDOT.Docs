# Автоматическое машинное обучение
## Что такое автоматическое машинное обучение?
Автоматическое машинное обучение (AutoML) – интеллектуальные технологии автоматизации процессов работы с данными и моделями машинного обучения для решения задач реального мира. Автоматическое МО решает задачи оптимизации параметров, отбора признаков, выбора типа модели и т.д.

Две основных проблемы автоматизации обучения моделей МО при решении прикладных задач:

* Невозможность получения приемлемого качества;
* Неинтерпретируемая структура модели;

## Популярные конкурирующие решения AutoML
Примеры существующих решений:

* Autosklearn
* AutoKeras
* H2O
* Google Colud HyperTune
* Microsoft Automated ML
* TPOP
* Hyperopt
* PyBrain

<img src="img_automl/automl_conc.png" alt="drawing" width="700"/>

Актуальность задач AutoML в настоящее время весьма высока:

<img src="img_automl/68747470733a2f2f626c6f67732e666f726265732e636f6d2f6c6f756973636f6c756d6275732f66696c65732f323031392f30392f476172746e65722d487970652d4379636c652d466f722d4172746966696369616c2d496e74656c6c6967656e63652d323031392e6a7.jfif" alt="drawing" width="700"/>

## Что такое генеративное машинное обучение?
Генеративное автоматическое МО решает задачи выращивания новых data-driven моделей, новых цепочек, ансамблей или других композиций из уже существующих моделей и т.п. В настоящее время, идеи низкоуровневой «сборки» модели под конкретную постановку проблемы реализованы только в контексте NAS (Neural Architecture Search) направления и в основном для задач распознавания образов. Однако, для всех остальных классов задач и классов моделей (применение которых может быть более эффективным, чем нейронных сетей) эти подходы не реализованы.

Основые проблемы, решаемые с помощью ГАМО, таковы:

* Отсутствие готовых решений для автоматизации процесса моделирования для решения предметных задач (АвтоМО должно быть более всеядным);
* Сложность применения новых методов моделирования без переизобретения существующих решений по управлению ими (МО должно быть более простым и гибким в управлении);
* Отсутствие устоявшихся подходов к улучшению воспроизводимости результата МО (МО должно быть воспроизводимым)
* Цель реализации ГАМО - повысить качество анализа различных природных, технических и социальных процессов с помощью идентификации композитных моделей на основе доступных массивов данных

## Основные понятия ГАМО
* Атомарная модель – модель целевого процесса, отображающая данные в результат моделирования Y=A(X) или преобразующие результаты моделирования Yn+1= O(Y1…Yn) и считающаяся не-декомпозируемой в ходе решения конкретной задачи идентификации композитной моделей. При этом модель может воспроизводить как все масштабы изменчивости Y, так и только часть из них;

* Операция – преобразование одного или нескольких наборов данных (результатов моделирования) в производные наборы.

* Композитная модель – составная модель, представляющая собой цепочку всех атомарных моделей и операций, идентифицированных в ходе применения эволюционного алгоритма.

* Атомизация – преобразование композитной модели в атомарную для использования в последующих запусках фреймворка.

## Основные методы ГАМО
* Метод композирования. Решаемая задача: создание или модификация цепочки.
* Метод порождения. Решаемая задача: создание атомарной модели (или операции).
