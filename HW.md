Написать ответ - почему массивы в JS являются "неправильными" и совмещают в себе несколько структур данных? Какие ?
Массивы совмещают в себе следующие структуры данных:

Стэк
Очередь
Двустроннюю очередь
Упорядоченный список
Массив в JS гетерогенный (может хранить в себе данные разных типов) и динамический (позволяет изменять длину массива). Реализован как частный случай хэш-таблиц.

Привязать контекст объекта к функции logger, чтобы при вызове this.item выводило - some value (Привязать через bind, call, apply)

function logger() {
 console.log('I output only external context: ' + this.item);
}

const obj = { item: "some value" };

logger.call(obj);

logger.apply(obj);

const boundLogger = logger.bind(obj);
boundLogger();

Бонус задание: Реализовать полифил (собственную функцию реализующую встроенную в js) метода bind()

declare global {
  interface Function {
    customBind(ctx: any, args?: any[]): Function;
  }
}

Function.prototype.customBind = function(ctx) {
  const targetFunc = this;
  const args = Array.from(arguments).slice(1);
 
  return function() {
    return targetFunc.apply(ctx, args);
  }
}

Function.prototype.customBind2 = function(ctx, ...args) { 
  return () => this.apply(ctx, args || []);
}