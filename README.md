Темою курсового проєкту є «Облік продажу квитків на концерти».
Розробити програму мовою програмування С/С++ для ведення файлу даних для обліку продажу квитків на концерти.
Файл повинен містити наступні дані: 
1	Назву гурту (обирається зі списку: Rammstein, Skillet, Альона-Альона, Віскі, AC/DC);
2	Місто виступу (вводиться з клавіатури);
3	Дату виступу (вводиться з клавіатури);
4	Вартість одного квитка (вводиться з клавіатури);
5	Кількість квитків (вводиться з клавіатури);
6	ПІБ покупця (вводиться з клавіатури);
7	Вартість покупки (вираховується автоматично).
Наприклад, файл може бути таким, як вказано в таблиці 1.1.

Таблиця 1.1 – Приклад файлу 
Назва гурту	Місто виступу	Дата виступу	Вартість  квитка	Кількість квитків	ПІБ покупця	Вартість покупки 
(грн.)
АС/DС	Київ	12.12.2019	2000	3	Іванов А.І.	6000
Віскі	Харків	01.09.2020	1500	2	Петров Е.С.	3000

Для обслуговування цього файлу програма повинна мати головне меню з наступними обов’язковими пунктами:
–	перегляд існуючих даних про продаж квитків;
–	додавання нових даних;
–	видалення даних (за двома ознаками: за номером та за уведеною ПІБ покупця);
–	сортування записів (за двома ознаками: за вартістю квитка та містом виступу гурту);
–	обслуговування запитів (5 запитів).
Програма повинна виконувати запити та виводити наступну інформацію:
–	ПІБ покупців, що придбали квитків на найбільшу суму;
–	відсоткове співвідношення кількості проданих квитків за гуртами від загальної кількості усіх продаж;
–	середня вартість одного квитка за усіма гуртами;
–	загальна сума продаж квитків у місті, що введено з клавіатури;
–	пошук найдешевших білетів обраної групи.
Файл даних виконати у вигляді файлу структур.
Кожний з пунктів головного меню оформити у вигляді окремої підпрограми (функції). 
Перегляд існуючої БД виконати у вигляді таблиці (україномовнї).
При виконанні пошуку у файлі де-якого рядкового значення, наприклад, ПІБ, надати користувачу можливість пошуку:
	за введенням ПІБ повністю (наприклад, Іванов К.Е.);
	за частковим введенням початкових літер (наприклад, Іва);
	за частковим введенням частини рядка (наприклад, ов К).
При створенні нового файлу даних, при редагуванні, при додаванні будь-яких записів усі дані, що мають вводитися з клавіатури, повинні бути максимально перевірені на коректність. Наприклад, дати «30 лютого» не існує, кількість товарів не може дорівнювати «мінус 5» тощо. 
Ще приклад перевірки даних на коректність. При спробі додати ідентифікаційний код, наприклад,  платівника до файлу, спочатку треба перевірити, чи є такий самий код вже у файлі даних? Та чи співпадає ПІБ платівника, якого додаємо з тим, що вже існує?
Рядкові дані (наприклад, ПІБ, назва товару тощо) після уведення з клавіатури зберігати у файлі так, щоб, як би користувач не увів би його з клавіатури, воно завжди повинно бути знайдене. Наприклад, ПІБ може бути уведено з пробілами спочатку, наприкінці, з декількома пробілами між прізвищем та по-батькові, великими чи малими літерами, чи по-батькові без крапок:
         _ _ _ІвАНов_ _к_ _Е._ _ (тут символом «_» позначений символ «пробіл»)
Таким чином  уведене ПІБ треба перетворити у формат: 
Прізвище  Ініціал.Ініціал.
і тоді записати у файл. Тобто для нашого прикладу так:
 Іванов  К.Е.
При введенні даних з клавіатури  у разі помилки після виведення повідомлення про помилку також треба  вивести подробиці – як уводити ці дані правильно. Наприклад, якщо на запит введення назви виробу, користувач увів
                 Торт-8      Киї)вський
то вивести, наприклад, таке повідомлення:
              Помилка!
У назві  виробу   неможна   використовувати 
цифри та  спеціальні символи, а тільки букви 
та пробіли. 
Чи, наприклад, таке  повідомлення:              
              Помилка!
У назві  тільки букви та пробіли.
Зберігти назву  Торт  Київський ?(1-так, 0-ні):
Для виділення певних частин інформації, що виводиться на екран монітору, використати різні кольори.
