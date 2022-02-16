# Сегментация изображений
В этом задании вам предстоит решить задачу сегментации медицинских снимков. Часть кода с загрузкой данных написана за вас. Всю содержательную сторону вопроса вам нужно заполнить самостоятельно. Задание оценивается из 15 баллов. 

Обратите внимание, что отчёт по заданию стоит целых 6 баллов. Он вынесен в отдельный пункт в конце тетради. Это сделано для того, чтобы тетрадь была оформлена как законченный документ о проведении экспериментов. Неотъемлемой составляющей отчёта является ответ на следующие вопросы:

* Что было сделано? Что получилось реализовать, что не получилось?
* Какие результаты ожидалось получить?
* Какие результаты были достигнуты?
* Чем результаты различных подходов отличались друг от друга и от бейзлайна (если таковой присутствует)?

В задаче используется датасет [ADDI project](https://www.fc.up.pt/addi/ph2%20database.html).

Это фотографии двух типов **поражений кожи:** меланома и родинки.
В данном задании мы не будем заниматься их классификацией, а будем **сегментировать** их.




---


1. Для начала мы скачаем датасет: [ADDI project](https://www.fc.up.pt/addi/ph2%20database.html).

<table><tr><td><img src="data:image/jpeg;base64,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"></td><td><img src="data:image/jpeg;base64,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"></td></tr></table>

2. Разархивируем .rar файл.
3. Обратите внимание, что папка  `PH2 Dataset images` должна лежать там же где и ipynb notebook.

Это фотографии двух типов **поражений кожи:** меланома и родинки.
В данном задании мы не будем заниматься их классификацией, а будем **сегментировать** их.
