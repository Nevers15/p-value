# Анализ значимости переходов по онлайн-объявлениям



***СТАТУС:*** **Завершён**


## Цели проекта:

Фред запустил рекламную кампанию, где на протяжении 20-ти дней проверяет число переходов по ссылкам разных цветов. Всего фред имеет 30 цветов, ему важно знать существует ли такой цвет, который обеспечит больше
переходов, чем синий. Все не так просто, Фред не умеет правильно интерпретировать результаты и не не уверен в том, какие переходы были целенаправленными, а какие произошли случайно.

## Бизнес-Задачи: 

1. Обработка и анализ данных по онлайн переходам.
2. Определение среднего колличества переходов по каждому из цветов.
3. Определение нулевой и альтернативной гиппотезы.
4. Поиск вероятности случайных переходов.

## Вывод исследования:

Анализ выявил, что есть два претендента на место самого популярного цвета среди пользователей. Ими оказались Ультрамариновый и цвет Нави. Однако, как указывает Фред, есть вероятность того, что могут существовать случайные переходы. Отталкиваясь от этого была определена следующая нулевая гипотеза, Ультрамариновый цвет не отличается от цвета Нави по количеству переходов из-за случайности таких переходов, которая по результатам p-value через хи-квадрат (Коэффициент Пирсона) превзошла установленный уровень значимости в 0.05. 

<img src="https://i.imgur.com/FnCy1LP.png" alt="p-value"/>

Как итог, есть 25% вероятности того, что большое число переходов случайно и 95% вероятности того, что результат является следствием созданных условий. Фред может считать, что Ультрамариновый цвет и цвет Нави могуть быть в равной степени достаточно хороши, чтобы превзойти Синий цвет.

## Использование результатов исследования:

Результатом исследования стало понимание концепта p-value, который помог определить корректны ли поставленные мною гипотезы. Величина p-value часто встречается на практике и служит хорошим инструментом для определения  вероятности получения наблюдаемых результатов при условии, что нулевая гипотеза верна, или вероятность ошибки в случае отклонения нулевой гипотезы.

## Технические особенности проекта:

Распределение данных количества переходов не было нормальным, по этим причинам пришлось отбросить алгоритм подсчета через z-оценку и прибегнуть к критерию хи-квадрат, он же коэффициент Пирсона, который измеряет разницу между ожидаемыми и наблюдаемыми значениями эксперимента, следовательно от распределения мы не зависим.

## Инструменты проекта

- Python
- Pandas
- Numpy
- scipy.stats
