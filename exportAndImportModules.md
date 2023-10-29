<h1>Exporting and Importing in ES6 Modules</h1>

To create a new module, we simply need to create a new file.

<h2>Importing a module without importing a value</h2>

Suppose you have a module named ```myModule.js``` that contains some code with side effects but doesn't export anything:

```js
// myModule.js
console.log("This is a side effect in myModule.js");

// No exports in this module
```

Now, if you want to import this module without importing any specific values, you can do it like this:

```js
import "./myModule.js";

// This will execute the code in myModule.js without importing any values.
```

In the above code, we use ```import ./myModule.js```; to import ```myModule.js```. This will execute the code in myModule.js, which is the side effect, without importing any specific values or variables from it.

***

<h2>Importing in ES6 Modules</h2>

When you want to use code from another module in your JavaScript program, you import it using the import statement. Here's how it works:

Example 1:
```js
// Import a named export from another module
import { functionName } from './moduleName';

// Import multiple named exports from another module
import { function1, function2 } from './moduleName';

// Import a default export from another module
import defaultName from './moduleName';
```

Example 2:
```js
const totalPrice = 237;
const totalQuantity = 23;

export { totalPrice, totalQuantity };
```

1) ```Named imports``` - simplest way of importing something from a module because all we have to do is to put ```import``` in front of anything that we might want to import.

2) We can also import multiple things from a module using Named imports. That is the main use case of Named imports. When we want to import multiple things. We can import multiple things at the same time using Named imports.

3) When we import a default export, we can basically give it a name that we want.

We can also import all the exports of a module at the same time. We importing everything into an object for example, in this case is "ShoppingCart" ```ShoppingCart``` will create an object containing everything that is exported from the module that we specified:

```js
import * as ShoppingCart from "./shoppingCart.js";
```

**Changing the import name**:

```js
import { totalPrice as price} from "./shoppingCart.js";
``` 
- You now use totalPrice as price after import.

We can mix default export and named export in the same import statement:

```js
import add, { addToCart, totalPrice as price, tq } from "./shoppingCart.js";
```

***

<h2>Exporting in ES6 Modules</h2>

You can export values, functions, or objects from your module to make them accessible to other modules. Here's how to do it:

```js
// Export a named function or variable
export function myFunction() {
  // Your function code here
}

// Export a constant
export const myConstant = 42;

// Export a default value (you can only export one default per module)
export default myDefaultFunction;

// Export multiple items at once
export { item1, item2 };
```

**Changing the export name**:

```js
const totalQuantity = 23;

export { totalQuantity as tq};
```
- You now use totalQuantity as tq after export.

















