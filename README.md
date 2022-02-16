# Сегментация изображений
В этом задании вам предстоит решить задачу сегментации медицинских снимков. Часть кода с загрузкой данных написана за вас. Всю содержательную сторону вопроса вам нужно заполнить самостоятельно. Задание оценивается из 15 баллов. 

Обратите внимание, что отчёт по заданию стоит целых 6 баллов. Он вынесен в отдельный пункт в конце тетради. Это сделано для того, чтобы тетрадь была оформлена как законченный документ о проведении экспериментов. Неотъемлемой составляющей отчёта является ответ на следующие вопросы:

* Что было сделано? Что получилось реализовать, что не получилось?
* Какие результаты ожидалось получить?
* Какие результаты были достигнуты?
* Чем результаты различных подходов отличались друг от друга и от бейзлайна (если таковой присутствует)?

В задаче используется датасет [PH2Dataset](https://www.fc.up.pt/addi/ph2%20database.html) ADDI project.

Это фотографии двух типов **поражений кожи:** меланома и родинки.

<table><tr><td><img src="https://github.com/kkruglik/semantic_segmetation/blob/main/mask.jpg"></td><td><img src="https://github.com/kkruglik/semantic_segmetation/blob/main/melanoma.jpg"></td></tr></table>

В данном задании мы не будем заниматься их классификацией, а будем **сегментировать** их.
