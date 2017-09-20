# CartFunctionality

Add to cart functionality using Session Storage.
You can use this JS file for your Summative 1.
This script doesnt do everything needed to create a fully functioning shopping cart. This just simulates the process. DO NOT user this for actual websites

You will have to do some changes to the JavaScript code for it to be able to fully work with your project. When you are ready to add this to your project then let me know and I will help you out to get it working.
To get this working you need to follow several steps.

### Installation
On each page which uses the cart you have to include this line at the bottom of your html page
This includes jQuery as well as the required javascript file

```sh
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script src="js/cartFunction.min.js"></script>
```

### Setup
This cart only allows you to include several aspects
To use these they need to have the exact classnames which are listed bellow
* product titles = product_title
* product price = product_price
* product description  = product_description
* quantity = product_quantity
* subtotal = sub_price
* image = product_image

Following these steps will help you include this script.

#### Prepare your Products
You can include as many products as you want, but they all have to be formatted in the same way. They also all need to have a unique name which distinguishes them all from each other.
Each product must be wrapped in their own div with a class of product. In there you will include the information about the product.
```sh
<div class="product">
    <h3 class="product_title">Apples</h3>
    <img class="product_image" src="images/apples.jpg">
    <p class="product_description">This is an Apple</p>
	<p>$<span class="product_price">5.00</span></p>
	<button class="add">+</button>
	<button class="remove">-</button>
</div>
```
To successfully add this to your site you must give it the classnames in the example above. If you do not then it isn't going to work.
When adding prices you need to make sure you dont include the $ in the class. This is why you should include a <span> around the number itself

#### Prepare your cart
Create a container of where your cart is going to be. Give this cart an ID of Cart
```sh
    <div id="cart"></div>
```
In that cart you can prepare it how you want, it could be divs, tables or how ever you want. Divs would be the easiest way.
Inside that element with the ID of cart create another element with an ID of CartContainer
```sh
    <div id="cart">
        <div id="CartContainer"></div>
    </div>
```

This is where your cart is actually going to go
Firstly create a template version of what you want your cart to look like. 
```sh
    <div id="cart">
        <div id="CartContainer">
            <div id="template" class="product" style="display:none;">
                <h2 class="product_title"></h2>
                <p class="product_description"></p>
                <p>$<span class="product_price"></span></p>
                <p class="product_quantity"></p>
                <p class="sub_price"></p>
                <button class="add">Add</button>
                <button class="remove">Remove</button>
                <img class="product_image" src="">
            </div>
        </div>
    </div>
```
You dont need to include everything shown above as it will work with some of the elements.
As long as you have followed these instructions and named all the classes and ID's correctly, the cart should take a copy of your template and insert the appropriate data.

#### Clear Cart
If you want to include a clear cart button. Then add an ID of clear to that element
```sh
    <button id="clear">Clear Cart</button>
```
#### Total Price
If you want to include the total price of every item in your cart then add the class priceCount to a <span> element.
This will only include the number and not the dollar sign so you need to include that outside of the span
```sh
    <p>Total Price of cart is $<span class="priceCount"></span></p>
```
#### Cart Count
To include the count of how many items are in your cart, add the class cartCount to a <span> element.
```sh
    <p>Number of items in cart = <span class="cartCount"></span></p>
```
