# JavaScript Best Practice Guide
### 1. Избегайте глобальных переменных
*Сведите к минимуму использование глобальных переменных.*
Вместо этого используйте локальные переменные и узнайте, как использовать замыкания.

### 2. Используйте camelCase для названий переменных, объектов и функций.
😃
   
    lastName
    numberOne
    
😠

    lastname
    numberone
    
### 3. Объявление переменной
*Объявляйте все переменные с помощью const или let.*

😃 let hello = 'Hello';

😠 var hello = 'Hello';

### 4. Точка с запятой
😃 

    let hello = 'Hello';
    let a = 10;

😠 

    let hello = 'Hello'
    let a = 10

### 5. При использовании конструкции if .. else else следует располагать на одной строке со скобкой закрывающей блок if.
😃

    if (a === 10) {
      console.log('true');
    } else {
      console.log('false');
    }
    
😠

    if (a === 10) {
      console.log('true');
    } 
    else {
      console.log('false');
    }
    
### 6. Строгое сравнение
*Оператор сравнения == всегда преобразуется (в соответствующие типы) перед сравнением.

Оператор === принудительно сравнивает значения и тип*

😃

    0 === "";       // false
    1 === "1";      // false
    1 === true;     // false

😠

    0 == "";        // true
    1 == "1";       // true
    1 == true;      // true

### 7. Завершайте Switches настройками по умолчанию
    switch (new Date().getDay()) {
      case 0:
        day = "Sunday";
        break;
      case 1:
        day = "Monday";
        break;
      case 2:
        day = "Tuesday";
        break;
      case 3:
        day = "Wednesday";
        break;
      case 4:
        day = "Thursday";
        break;
      case 5:
        day = "Friday";
        break;
      case 6:
        day = "Saturday";
        break;
      default:
        day = "Unknown";
    }
    
### 8. Остерегайтесь автоматических преобразований типов
*Помните, что числа могут быть случайно преобразованы в строки или NaN*
       
    var x = "Hello";     // typeof x строка
    x = 5;               // смена typeof x на число
    
### 9. Никогда не объявляйте числовые, строковые или логические объекты
*Всегда относитесь к числам, строкам или логическим значениям как к примитивным значениям. Не как к объектам.*

    var x = "John";             
    var y = new String("John");
    (x === y) // это ложь так как x это строка and y это объект.
    
### 10. Объявления сверху
*Хорошей практикой написания кода является размещение всех объявлений в начале каждого скрипта или функции.*

    // Объявите в начале
    var firstName, lastName, price, discount, fullPrice;
    
    // Запишите затем
    firstName = "John";
    lastName = "Doe";

    price = 19.90;
    discount = 0.10;

    fullPrice = price - discount;
