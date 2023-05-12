Задачата да се реализира на езика C++. За успешно преминаване на тази част от изпита, решението ви трябва коректно да изпълнява всичко, което се изисква в условието на задачата. Разглеждаме система за работа с двуизмерни фигури. Тя трябва да поддържа поне следните фигури: 

* Триъгълник (triangle), който има три страни a, b, и c. 

* Кръг (circle), който има радиус (radius). 

* Квадрат (square), който има страна (a). 

За всяка фигура трябва да може да се намери нейният периметър (реално число). 

Да се реализира подходяща йерархия от класове за фигурите. Тя да включва поне 4 класа – един абстрактен за фигура и три за конкретните фигури. 

Всички член-данни трябва да са константни, т.е. да се задават при създаването на обектите и след това да не може да се променят. 

Класовете да се реализират според правилата на ООП с подходящо използване на полиморфизъм. Помислете за коректния начин това да бъде направено в C++. Помислете какъв трябва да бъде деструкторът в абстрактния клас. 

Да се реализира функция sumOfPerimeters, която получава аргумент от подходящ тип, задаващ хетерогенен масив от фигури от произволен вид и връща сумата от техните периметри. Масивът може да съдържа фигури от произволен вид. 

Работата на функцията sumOfPerimeters да се демонстрира в примерна програма. Програмата трябва да подава на функцията примерни данни съдържащи поне по една от всеки вид фигура и да извежда на екрана сумата от периметрите. 
-------------------------------------------------------------------------------------------------

Да се реализира система за управление на събития. За всички събития в системата се предполага, че са в един и същ ден (в рамките на 24 часа) и че всички моменти от време се задават с точност до минута. 
А) Да се реализират 3 класа, които поддържат следните 3 типа събития: 

* събитие от тип SimpleEvent – събитието се определя от начален и краен час.  
Максимална продължителност на този тип събития трябва да бъде не повече от 2 часа. 

* събитие от тип EventWithFixedIntermission – събитието се определя от начален час, начало на антракт с фиксирано време от 20 минути и краен час.  
Максималната продължителността на събитието (без времето за антракта) е не повече от 4 часа. 

* събитие от тип EventWithIntermission – събитието се определя от начален час, начало и край на антракта и край на събитието. Продължителността на събитието (без времето за антракта) трябва да е не повече от 6 часа, а антрактът трябва да е с продължителност между 30 минути и 1 час. 

Представянето на часовете за събитията е по ваш избор. Ако се подадат неправилни данни при създаването на съответните събития, програмата да извежда съобщение за грешка и да инициализира събитието със стойности по подразбиране.  

Б) Да се реализира контейнер EventManager, в който се пази колекция от произволен тип събития с фиксиран максимален капацитет, т.е. контейнерът не може да се преоразмерява след първоначалното си създаване. Да се дефинира операция добавяне на събитие в контейнера със следната сигнатура: 
bool addEvent (<подходящ_тип>* event). Добавянето се извършва чрез записване на указателя в контейнера (т.е. контейнерът “открадва” паметта, заделена за събитието) и само ако има достатъчно място.   
Бонус: Да се реализира клониране на събитието в контейнера вместо паметта да се “краде”. 

В) Да се реализира метод ongoingEvents, който по подаден час намира броя на всички събития, които се провеждат в дадения час. Ако едно събитие е в антракт, то не се провежда в настоящия момент. 
