<script setup>
  import { onUnmounted, ref } from 'vue'
  import useAuth from '../composable/useAuth';
  import useChat from '../composable/useChat';
  

 

  const { messages, unsubscribe, sendMessage } = useChat()
  const { user } = useAuth()

  const newMessage = ref('')

  const send = () => {
    sendMessage(newMessage.value)
    newMessage.value = ''
  }

  onUnmounted(() => {
    unsubscribe()
  })
</script>

<template>
   <title>The Generics | Store</title>
        <meta name="description" content="This is the description">

       
  
    <body>
        <header class="main-header">
            <nav class="main-nav nav">
                <ul>
                    
                    <li><a href="index.html">Pants</a></li> 
                    <li><a href="store.html">Shoes</a></li> 
                    <li><a href="../store.html">Shirts</a></li> 
                    
                </ul>
            </nav>
            <h1 class="name name-large">Reyes Clothing Store</h1>
        </header>
        <section class="container content-section">
            <h2 class="section-header">Pants</h2>
            <div class="shop-items">
                <div class="shop-item">
                    <span class="shop-item-title">Item 1</span>
                    <img class="shop-item-image" src="../Images3/Pants1.jpg">
                    <div class="shop-item-details">
                        <span class="shop-item-price">$49.99</span>
                        <button class="btn btn-primary shop-item-button" type="button">ADD TO CART</button>
                    </div>
                </div>
                <div class="shop-item">
                    <span class="shop-item-title">Item 2</span>
                    <img class="shop-item-image" src="../Images3/Pants2.jpg">
                    <div class="shop-item-details">
                        <span class="shop-item-price">$20.99</span>
                        <button class="btn btn-primary shop-item-button" type="button">ADD TO CART</button>
                    </div>
                </div>
                <div class="shop-item">
                    <span class="shop-item-title">Item 3</span>
                    <img class="shop-item-image" src="../Images3/Pants3.webp">
                    <div class="shop-item-details">
                        <span class="shop-item-price">$53.99</span>
                        <button class="btn btn-primary shop-item-button" type="button">ADD TO CART</button>
                    </div>
                </div>
                <div class="shop-item">
                    <span class="shop-item-title">Item 4</span>
                    <img class="shop-item-image" src="../Images3/Pants4.jpg">
                    <div class="shop-item-details">
                        <span class="shop-item-price">$37.99</span>
                        <button class="btn btn-primary shop-item-button" type="button">ADD TO CART</button>
                    </div>
                </div>
            </div>
        </section>
        <section class="container content-section">
            <h2 class="section-header">Popular</h2>
            <div class="shop-items">
                <div class="shop-item">
                    <span class="shop-item-title">Pants</span>
                    <img class="shop-item-image" src="../Images3/Pants5.jpg">
                    <div class="shop-item-details">
                        <span class="shop-item-price">$75.99</span>
                        <button class="btn btn-primary shop-item-button" type="button">ADD TO CART</button>
                    </div>
                </div>
                <div class="shop-item">
                    <span class="shop-item-title">Pants</span>
                    <img class="shop-item-image" src="../Images3/Pants6.jpg">
                    <div class="shop-item-details">
                        <span class="shop-item-price">$69.99</span>
                        <button class="btn btn-primary shop-item-button" type="button">ADD TO CART</button>
                    </div>
                </div>
            </div>
        </section>
        <section class="container content-section">
            <h2 class="section-header">CART</h2>
            <div class="cart-row">
                <span class="cart-item cart-header cart-column">ITEM</span>
                <span class="cart-price cart-header cart-column">PRICE</span>
                <span class="cart-quantity cart-header cart-column">QUANTITY</span>
            </div>
            <div class="cart-items">
            </div>
            <div class="cart-total">
                <strong class="cart-total-title">Total</strong>
                <span class="cart-total-price">$0</span>
            </div>
            <button class="btn btn-primary btn-purchase" type="button">PURCHASE</button>
        </section>
        <footer class="main-footer">
            <div class="container main-footer-container">
                <h3 class="band-name">Contact Us</h3>
                <ul class="nav footer-nav">
                    <li>
                        <a href="https://www.facebook.com" target="_blank">
                            <img src="../Images/facebook.png">
                        </a>
                    </li>
                    <li>
                        <a href="https://twitter.com" target="_blank">
                            <img src="../Images/twitter.webp">
                        </a>
                    </li>
                    <li>
                        <a href="https://www.instagram.com/" target="_blank">
                            <img src="../Images/intagram.jpg">
                        </a>
                    </li>
                </ul>
            </div>
        </footer>
    </body>
</template>