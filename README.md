# SafeJS
SafeJS is the simple language based on JavaScript. The SafeJS transpiles to JavaScript.
# Function, method, constructor or destroy cache
- *cache function* - caches the function
- *weak cache function* - caches the function in a WeakMap
- *cache /\* arrow function \*/* - caches the arrow function
- *weak cache /\* arrow function \*/* - caches the arrow function in a WeakMap
Dependence on arguments. If you have changed the arguments, result will re-count.
# *destroy* method in classes
This method calls when other code tries to delete the instance. In destroy, like in a constructor, *this* is an instance.
When destroy method returns *false*, instance doesn't removes.
# *delete \<obj\>* operator
You can delete a variable or a class, let, instance... What can you do? You can use *delete* operator!
How to test that a variable were removed? Use *variable == removed* or *variable instanceof removed*.
**Example:**
```js
var variable = 5;
delete variable;
console.log(variable); // removed (value)
```
# *&&&* operator
This operator combines objects.
**Example:**
```js
let numberArray = Number &&& Array;
```
# Types that added to SafeJS and not created in JavaScript
- *never* - value that is not possible
- *empty* - absolute blank value. You can use it in your code
- *removed* - value of var, let, class or instance after delete operator
# How to get *destroy* method from classes?
Use this:
```js
// get
yourClass.deleteThis
// set
yourClass.deleteThis = /* function */;
```
# *Function.useCache*
Every instance of Function class has the useCache property.
Values of this property:
- *false* - don't use cache
- *true* - use cache
- *1* - use cache in a WeakMap
# *delete this* operator warning
You can't use *delete this*.
# *isStrict* variable
This variable controls the SafeJS strict mode.
