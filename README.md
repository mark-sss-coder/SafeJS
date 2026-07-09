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
# Node.js needed
Please download [Node.js](https://nodejs.org/) because it needed for a transpiler.
# How to use transpiler?
Run the following command in your terminal (Works on macOS, Linux, and Windows):
```bash
node "path/to/the/file/transpiler.js" "path/to/your/.sjs/file" "path/where/you/want/to/make/.js/file"
```
*Note: Make sure you have **Node.js** installed on your system before running.*
# File extension
.sjs
# VS Code extension
If you are using VS Code then you can use the extension.
Download the .vsix archive from .vscode folder (safejs-syntax-1.0.0.vsix).
Open VS Code, press Ctrl (Cmd on MacOS) + Shift + X or open the extensions tab.
Press *...* button in top-right, select **Install from VSIX...**,
select the downloaded safejs-syntax-1.0.0.vsix file and press **OK**, **Install** or **Done** button.

Create any .sjs file... Hooray! You will get the beautiful syntax
highlighting.
# Coming soon: Online SafeJS Transpiler
