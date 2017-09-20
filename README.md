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
Following these steps will help you include this script.
##### Prepare your cart
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
This cart only allows you to include several aspects
* product titles
* product price
* quantity
* subtotal
* image

This is where your cart is actually going to go
Firstly create a template version of what you want your cart to look like. 
```sh
    <div id="cart">
        <div id="CartContainer">
            <div id="template" class="product">
                <h2 class="product_title"></h2>
                <p>$<span class="product_price"></span></p>
                <p class="product_quantity"></p>
                <p class="sub_price"></p>
                <button class="add">Add</button>
                <button class="remove">Remove</button>
            </div>
        </div>
    </div>
```


