<h1>The Module Pattern</h1>

The main goal of the module pattern is to encapsulate functionality to have private data, and to expose a Public API. The best way of achieving all that is by simply using a function because functions give us private data by default and allow us to return values which can become our Public API.

**How is Module Pattern Implemented?**

- Usually, we write an **IIFE**, the reason for that is because this way, we don't have to call it separately and we can also ensure that it's only called once. It is important that the function is only created once because the goal of this function is not to reuse code by running it multiple times, the only purpose of this function is to create a new scope and return data just once. The data that we return in this function will become the Public API.

```js
const ShoppingCart2 = (function () {
  const cart = [];
  const shippingCost = 10;
  const totalPrice = 237;
  const totalQuantity = 23;

  const addToCart = (product, quantity) => {
    cart.push({ product, quantity });
    console.log(
      `${quantity} ${product} added to cart (shipping cost is ${shippingCost})`
    );
  };

  const orderStock = (product, quantity) => {
    console.log(`${quantity} ${product} ordered from supplier`);
  };

  return {
    addToCart,
    cart,
    totalPrice,
    totalQuantity,
  };
})();
```

The code above;

1) **IIFE (Immediately Invoked Function Expression)**:
```js
const ShoppingCart2 = (function () {
  // ...
})();
```
The code starts by defining a constant variable named **ShoppingCart2**. This variable is assigned the result of invoking an anonymous function immediately. This pattern is often used to create private scopes and encapsulate variables.

2) **Private Variables**:

Inside the IIFE, there are several private variables:
- cart: An array that represents the shopping cart. It stores objects containing product and quantity.
- shippingCost: A constant set to 10, representing the fixed cost of shipping.
- totalPrice: A constant set to 237, representing the total price of items in the cart.
- totalQuantity: A constant set to 23, representing the total quantity of items in the cart.

3) **addToCart Function**:

```js
const addToCart = (product, quantity) => {
  cart.push({ product, quantity });
  console.log(
    `${quantity} ${product} added to cart (shipping cost is ${shippingCost})`
  );
};
```
- addToCart is a function that takes two parameters: product and quantity.
- It pushes an object into the cart array, which contains the product and its quantity.
- It also logs a message indicating that a product has been added to the cart, including the product name and the shipping cost.

4) **orderStock Function**:

```js
const orderStock = (product, quantity) => {
  console.log(`${quantity} ${product} ordered from supplier`);
};
```
- orderStock is another function that takes two parameters: product and quantity.
- It logs a message indicating that a certain quantity of a product has been ordered from a supplier.

5) **Module Exports**:

```js
return {
  addToCart,
  cart,
  totalPrice,
  totalQuantity,
};
```
The IIFE returns an object that exposes the following properties and functions:
- addToCart: The function for adding products to the shopping cart.
- cart: The array representing the shopping cart.
- totalPrice: The total price of items in the cart.
- totalQuantity: The total quantity of items in the cart.

This structure allows you to manage a shopping cart and its related data in a modular and encapsulated way. You can use the addToCart function to add items to the cart, and access the cart contents, total price, and total quantity through the exported properties. The IIFE ensures that the internal variables are hidden from the global scope, making this module a good example of encapsulation in JavaScript.







