🛒 Order & Checkout Functionality Explanation

The checkout system in your online bookstore works through the function checkout().

1. When User Clicks Checkout

The function checkout() is triggered when the Checkout button is pressed.

<button onclick="checkout()">Checkout</button>

2. Check if Cart is Empty

First, the program checks if the cart has any books.

If the cart is empty, it shows an alert message:


if (cart.length === 0) {
  alert("Your cart is empty. Please add some books!");
  return;
}

👉 This prevents placing an order without books.

3. Calculate Total Price

If the cart has books, the total price is calculated using:


let total = cart.reduce((sum, item) => sum + item.price, 0);

reduce() goes through every item in the cart and adds up all the prices.

Example:

Cart = [₹200, ₹300, ₹150]

Total = ₹650

4. Show Order Confirmation

After calculating, it shows a confirmation message with the total amount:


alert("✅ Order placed successfully!\nTotal amount: ₹" + total);

Example message:

✅ Order placed successfully!
Total amount: ₹650

5. Clear the Cart

After placing the order, the cart is emptied so that the user can start fresh for the next order:


cart = [];
localStorage.setItem("cart", JSON.stringify(cart));
displayCart();

localStorage is updated to make sure old items are removed.

displayCart() updates the cart display to show nothing.

🔑 In Simple Words

1. User clicks Checkout


2. If no books → show warning


3. If books are in cart → add up prices


4. Show total amount with success message


5. Empty the cart after order

Technologies Used

HTML5 – Structure of the webpage.

CSS3 – Styling and layout.

JavaScript (Vanilla) – Cart functionality and storage.





