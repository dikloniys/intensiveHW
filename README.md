OPTIONS
HTTP-метод OPTIONS используется для описания параметров соединения с целевым ресурсом. Клиент может указать особый URL для обработки метода OPTIONS, или * (звёздочку) чтобы указать весь сервер целиком.

 new AbortController();
 Он имеет единственный метод abort() и единственное свойство signal.
При вызове abort():
генерируется событие с именем abort на объекте и прерывает метод fetch

это новый синтаксис HTTP, который работает на IETF QUIC, мультиплексированном и безопасном транспорте на основе UDP

Написать по 2 примера создания примитивных значений
let sum = 5

Почему, если обратиться к переменным созданным через let, const до их объявления - мы получаем ReferenceError?
Потому что они не всплывают (hoisting)

let str = 'строка'

const res = "B" + "a" + (1 - "hello");
console.log(res)
BaNaN

const res2 = (true && 3) + "d";
console.log(res2); 
3d

const res3 = Boolean(true && 3) + "d";
console.log(res3);
trued


ДЗ 3
задача 1
let user = new Object(); 
let user2 = {};
let user3 = Object.create({})

задача 2
let a = user

Задание 3 – 

let makeCounter = function (){}
function makeCounter (){}
(function makeCounter (){})()
