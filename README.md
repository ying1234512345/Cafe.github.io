# Cafe.github.io
<!DOCTYPE html>
<html>
<head>
<title>W3.CSS Template</title>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Sniglet">
<style>
body, html {
  height: 100%;
  font-family: "Sniglet", sans-serif;
}

.bgimg {
  background-position: center;
  background-size: cover;
  background-image: url("https://mojoboutique.com/cdn/shop/articles/japandi_cafe_ideas_1344x.jpg?v=1712165463");
  min-height: 75%;
}

.menu {
  display: none;
}


/* Move the "MY CAFE" text upwards */
.w3-display-middle {
  position: absolute;
  top: 10%; /* Move it closer to the top */
  left: 50%;
  transform: translateX(-50%);
}


/* Change navbar background to light coffee color */
.w3-bar {
  background-color: #D4A79C !important;  /* Light coffee color */
}

/* Change other black backgrounds to light coffee */
.w3-black {
  background-color: #D4A79C !important;  /* Light coffee color */
}

/* Change menu section background */
#w3-menu {
  background-color: #D4A79C !important;  /* Light coffee color */
}

/* Footer background color change */
footer {
  background-color: #D4A79C !important;  /* Light coffee color */
}

/* Other minor adjustments if needed */
.w3-tag {
  background-color: #D4A79C !important;  /* Light coffee color for tags */
}
</style>
</head>
<body>

<!-- Navbar (sit on top) -->
<div class="w3-top">
  <div class="w3-bar w3-white w3-wide w3-padding w3-card">
    <a href="#home" class="w3-bar-item w3-button"><b>MY</b> Cafe</a>
    <!-- Float links to the right. Hide them on small screens -->
    <div class="w3-right w3-hide-small">
      <a href="#about" class="w3-bar-item w3-button">About</a>
      <a href="#menu" class="w3-bar-item w3-button">Menu</a>
      <a href="#comment" class="w3-bar-item w3-button">Comment</a>

      <!-- Shopping Cart Icon -->
      <a href="javascript:void(0)" class="w3-bar-item w3-button" onclick="showCart()">
        <i class="w3-xlarge fa fa-shopping-cart"></i>
        <span id="cart-badge" class="w3-badge w3-red" style="position: absolute; top: 10px; right: 10px; font-size: 14px;">0</span>
      </a>
    </div>
  </div>
</div>

<!-- Cart Modal -->
<div id="cart-modal" class="w3-modal">
  <div class="w3-modal-content w3-animate-zoom">
    <header class="w3-container w3-teal">
      <span onclick="closeCart()" class="w3-button w3-display-topright">&times;</span>
      <h2>Your Cart</h2>
    </header>
    <div class="w3-container">
      <p id="cart-items-list">No items in cart</p>
      <button onclick="clearCart()" class="w3-button w3-red">Clear Cart</button>
    </div>
  </div>
</div>

<!-- Script for handling the cart -->
<script>
  let cartCount = 0; // Initialize cart count
  let cartItems = []; // To hold items in cart

  // Function to display the cart details in the modal
  function showCart() {
    const cartBadge = document.getElementById('cart-badge');
    const cartModal = document.getElementById('cart-modal');
    const cartItemsList = document.getElementById('cart-items-list');
    
    // Display cart count on badge
    cartBadge.innerText = cartCount;

    // Check if there are items in the cart
    if (cartCount === 0) {
      cartItemsList.innerHTML = 'No items in cart';
    } else {
      cartItemsList.innerHTML = cartItems.join('<br>');
    }

    // Show modal
    cartModal.style.display = 'block';
  }

  // Function to close the cart modal
  function closeCart() {
    const cartModal = document.getElementById('cart-modal');
    cartModal.style.display = 'none';
  }

  // Function to add item to cart (sample item)
  function addToCart(itemName) {
    cartCount++;
    cartItems.push(itemName); // Adds item name to cart
    document.getElementById('cart-badge').innerText = cartCount;
  }

  // Function to clear cart
  function clearCart() {
    cartCount = 0;
    cartItems = [];
    document.getElementById('cart-badge').innerText = cartCount;
    document.getElementById('cart-items-list').innerHTML = 'No items in cart';
  }

  // Close the cart modal if clicked outside the modal
  window.onclick = function(event) {
    const cartModal = document.getElementById('cart-modal');
    if (event.target === cartModal) {
      closeCart();
    }
  }
</script>

<!-- Include Font Awesome for cart icon -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

  <!-- Header with image -->
<header class="bgimg w3-display-container w3-grayscale-min" id="home">
  <div class="w3-display-bottomleft w3-center w3-padding-large w3-hide-small">
    <span class="w3-tag">Open from 8am to 11pm</span>
  </div>
  <div class="w3-display-middle w3-center">
    <span class="w3-text-white" style="font-size:100px; font-family: 'Cooper Black', serif;"><br>MY CAFE</span>
  </div>
  <div class="w3-display-bottomright w3-center w3-padding-large w3-hide-small">
    <span class="w3-tag">No. 28, Jalan Sultan Iskandar,
30300 Ipoh, Perak, Malaysia.</span>
  </div>
</header>

<!-- Add a background color and large text to the whole page -->
<div class="w3-sand w3-grayscale w3-large">

<!-- About Container -->
<div class="w3-container" id="about">
  <div class="w3-content" style="max-width:700px">
    <h5 class="w3-center w3-padding-64"><span class="w3-tag w3-wide">ABOUT THE CAFE</span></h5>
<p><strong>Welcome to MY CAFE, A Cozy spot in Ipoh!</strong></p>
    <p>Located in the heart of Ipoh, MY CAFE has been delighting customers with memorable dishes and attentive service for over five years. Our menu offers a variety of options, from wholesome mains and refreshing light bites to exquisite desserts. Every dish is crafted with fresh ingredients and care, bringing the warmth of home and the essence of nature to your table.</P>
<p>Whether you're looking for a quick, relaxed lunch or a cheerful afternoon with friends, MY CAFE is the perfect choice. After five years of growth and innovation, we�ve created a cozy space where you can enjoy your own peaceful moments. Every visit feels like reconnecting with an old friend�warm and comforting.</p>
<p><strong>Come visit MY CAFE and enjoy the perfect blend of flavor, comfort, and hospitality!</strong></p>
<div class="w3-panel w3-leftbar w3-light-grey">
      <p><i>"Make the most of nature gifts, but always at the right time. Freshness is the true sweetness.</i></p>
      <p>Chef, Coffeeist and Owner: Julia Claire</p>
    </div>
    <img src="https://dynamic-media-cdn.tripadvisor.com/media/photo-o/10/e5/73/92/photo1jpg.jpg?w=1200&h=-1&s=1" style="width:100%;max-width:1000px" class="w3-margin-top">
    <p><strong>Opening hours:</strong> Everyday from 8am to 11pm.</p>
    <p><strong>Address:</strong> No. 28, Jalan Sultan Iskandar,
30300 Ipoh, Perak, Malaysia.</p>
  </div>
</div>

<style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f9f9f9;
    }

    .container {
      width: 90%;
      max-width: 1200px;
      margin: 20px auto;
      padding: 10px;
    }

    .card {
      display: flex;
      background: #fff;
      border: 1px solid #ddd;
      border-radius: 8px;
      margin: 10px 0;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      overflow: hidden;
    }

    .card img {
      width: 150px;
      height: 150px;
      object-fit: cover;
    }

    .card-content {
      padding: 15px;
      flex: 1;
    }

    .card-content h3 {
      margin: 0;
      font-size: 18px;
      color: #333;
    }

    .card-content p {
      margin: 5px 0;
      color: #666;
    }

    .card-content .price {
      font-weight: bold;
      color: #28a745;
      margin-bottom: 10px;
    }

    .card-content .description {
      font-size: 14px;
      color: #777;
    }

    .add-button {
      display: flex;
      align-items: center;
      justify-content: center;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 50%;
      width: 40px;
      height: 40px;
      font-size: 18px;
      cursor: pointer;
      margin: 15px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    }

    .add-button:hover {
      background: #0056b3;
    }
  </style>
</head>

<body>
  <!-- Menu Container -->
  <div class="w3-container w3-black w3-padding-64 w3-xxlarge" id="menu">
    <div class="w3-content">
      <h1 class="w3-center w3-jumbo" style="margin-bottom:64px; font-family: 'Cooper Black', sans-serif;">THE MENU</h1>

      <!-- Tabs -->
      <div class="w3-row w3-center w3-border w3-border-dark-grey">
        <a href="javascript:void(0)" onclick="openMenu(event, 'Beverages');" id="defaultOpen">
          <div class="w3-col s4 tablink w3-padding-large w3-hover-red">Beverages</div>
        </a>
        <a href="javascript:void(0)" onclick="openMenu(event, 'Dishes');">
          <div class="w3-col s4 tablink w3-padding-large w3-hover-red">Dishes</div>
        </a>
        <a href="javascript:void(0)" onclick="openMenu(event, 'Snacks');">
          <div class="w3-col s4 tablink w3-padding-large w3-hover-red">Snacks</div>
        </a>
      </div>

      <!-- Beverages Section -->
      <div id="Beverages" class="w3-container menu w3-padding-32 w3-white">
        <div class="card">
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYP1HvsoRhlTrN-JNyx2rNszwxIykYlC9dSw&s" alt="Espresso">
          <div class="card-content">
            <h3>Espresso</h3>
            <p class="price">RM 9.90</p>
            <p class="description">A strong, concentrated coffee.</p>
          </div>
          <button class="w3-button w3-green" onclick="addToCart('Espresso', 9.90)">+</button>
        </div>
        <div class="card">
    <img src="https://cdn.apartmenttherapy.info/image/upload/f_jpg,q_auto:eco,c_fill,g_auto,w_1500,ar_1:1/k%2FPhoto%2FRecipe%20Ramp%20Up%2F2022-07-Cappuccino%2FCappuccino" alt="Cappocino">
    <div class="card-content">
        <h3>Cappuccino</h3>
        <p class="price">RM 10.90</p>
        <p class="description">Espresso with steamed milk and foam.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Cappuccino', 10.90)">+</button>
</div>
<div class="card">
    <img src="https://www.cuisinart.com/dw/image/v2/ABAF_PRD/on/demandware.static/-/Sites-us-cuisinart-sfra-Library/default/dwae845f23/images/recipe-Images/cafe-latte1-recipe.jpg?sw=1200&sh=1200&sm=fit" alt="latte">
    <div class="card-content">
        <h3>Latte</h3>
        <p class="price">RM 10.90</p>
        <p class="description">Espresso with steamed milk.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Latte', 10.90)">+</button>
</div>
<div class="card">
    <img src="https://img.buzzfeed.com/thumbnailer-prod-us-east-1/8f1e6c865e5b4ef0a1f8d15b3f676202/BFV69042_HowToMakeBobaFromScratch_JP_Final_YT.jpg">
    <div class="card-content">
        <h3>Bubble Milk Tea</h3>
        <p class="price">RM 11.90</p>
        <p class="description">Sweet milk tea with chewy tapioca pearls, served cold.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Bubble Milk Tea', 11.90)">+</button>
</div>
<div class="card">
    <img src="https://amandascookin.com/wp-content/uploads/2023/11/Crockpot-Hot-Chocolate-RCSQ-U-500x500.jpg">
    <div class="card-content">
        <h3>Chocolate</h3>
        <p class="price">RM 9.90</p>
        <p class="description">Creamy chocolate.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Chocolate', 9.90)">+</button>
</div>
<div class="card">
    <img src="https://i0.wp.com/thejoyfilledkitchen.com/wp-content/uploads/2021/04/Lemonade-2-2.jpg?resize=740%2C792&ssl=1">
    <div class="card-content">
        <h3>Lemonade</h3>
        <p class="price">RM 7.90</p>
        <p class="description">Sweet and tangy lemon drink.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Lemonade', 7.90)">+</button>
</div>

      </div>

      <!-- Dishes Section -->
      <div id="Dishes" class="w3-container menu w3-padding-32 w3-white" style="display: none;">
        <div class="card">
          <img src="https://supervalu.ie/thumbnail/800x600/var/files/real-food/recipes/Uploaded-2020/spaghetti-bolognese-recipe.jpg">
          <div class="card-content">
            <h3>Spaghetti Bolognese</h3>
            <p class="price">RM 15.90</p>
            <p class="description">Pasta with rich tomato meat sauce.</p>
          </div>
          <button class="w3-button w3-green" onclick="addToCart('Spaghetti Bolognese', 15.90)">+</button>
        </div>
        <div class="card">
    <img src="https://zhangvillage.com/image/smartacc/image/cache/data/all_product_images/product-821/pP3mp6Bl1660968818-1024x1024.jpg">
    <div class="card-content">
        <h3>Tom Yum Mee</h3>
        <p class="price">RM 14.90</p>
        <p class="description">Spicy and sour noodle soup with shrimp.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Tom Yum Mee', 14.90)">+</button>
</div>
<div class="card">
    <img src="https://s.wendyweekendgourmet.com/media/20241017160228/Deluxe-Seafood-and-Steak-Fried-Rice_-done-768x482.jpg">
    <div class="card-content">
        <h3>Seafood Fried Rice</h3>
        <p class="price">RM 13.90</p>
        <p class="description">Fried rice with shrimp and other seafood.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Seafood Fried Rice', 13.90)">+</button>
</div>
<div class="card">
    <img src="https://s23209.pcdn.co/wp-content/uploads/2018/04/Thai-Red-Curry-Noodle-SoupIMG_4787.jpg">
    <div class="card-content">
        <h3>Curry Noodles</h3>
        <p class="price">RM 13.90</p>
        <p class="description">Noodles in a rich curry broth with meat.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Curry Noodles', 13.90)">+</button>
</div>
<div class="card">
    <img src="https://www.unileverfoodsolutions.com.my/dam/global-ufs/mcos/SEA/calcmenu/recipes/MY-recipes/general/chicken-chop-kegemaran-malaysia/main-header.jpg">
    <div class="card-content">
        <h3>Chicken Chop</h3>
        <p class="price">RM 18.90</p>
        <p class="description">Grilled or fried chicken served with sauce and sides.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Chicken Chop', 18.90)">+</button>
</div>
<div class="card">
    <img src="https://shutterandmint.com/wp-content/uploads/2023/08/lamb-chop-hero-shot.jpg">
    <div class="card-content">
        <h3>Lamb Chop</h3>
        <p class="price">RM 26.90</p>
        <p class="description">Grilled lamb served with sauce and sides.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Lamb Chop', 26.90)">+</button>
</div>
<div class="card">
    <img src="https://simplyhomecooked.com/wp-content/uploads/2024/03/tuna-sandwich-recipe-2.jpg">
    <div class="card-content">
        <h3>Tuna Sandwich</h3>
        <p class="price">RM9.90</p>
        <p class="description">Tuna salad with mayo, lettuce, and cucumber.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Tuna Sandwich', 9.90)">+</button>
</div>
<div class="card">
    <img src="https://www.recipetineats.com/tachyon/2023/09/Crispy-fried-chicken-burgers_5.jpg">
    <div class="card-content">
        <h3>Chicken Burger</h3>
        <p class="price">RM 10.90</p>
        <p class="description">Grilled or fried chicken patty with lettuce, tomato, and mayo.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Chicken Burger', 10.90)">+</button>
</div>

      </div>
<!-- Snacks Section -->
      <div id="Snacks" class="w3-container menu w3-padding-32 w3-white" style="display: none;">
        <div class="card">
          <img src="https://rainbowplantlife.com/wp-content/uploads/2022/11/Mushroom-soup-cover-image-1-of-1.jpg">
          <div class="card-content">
            <h3>Mushroom Soup</h3>
            <p class="price">RM 6.90</p>
            <p class="description">Creamy and rich mushroom soup.</p>
          </div>
          <button class="w3-button w3-green" onclick="addToCart('Mushroom Soup', 6.90)">+</button>
        </div>
        <div class="card">
    <img src="https://images.themodernproper.com/billowy-turkey/production/posts/2022/Homemade-French-Fries_8.jpg?w=1200&q=82&auto=format&fit=crop&dm=1662474181&s=577d686ad285c29c256e35d3ce9e437b">
    <div class="card-content">
        <h3>French Fries</h3>
        <p class="price">RM 7.90</p>
        <p class="description">Crispy fried fries served with ketchup.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('French Fries', 7.90)">+</button>
</div>
<div class="card">
    <img src="https://blog.worldgymtaiwan.com/hs-fs/hubfs/%E6%96%87%E7%AB%A0%E5%B0%88%E7%94%A8%E5%9C%96%E7%89%87/%E7%94%B0%E5%9C%92%E6%B2%99%E6%8B%89.jpg?width=700&name=%E7%94%B0%E5%9C%92%E6%B2%99%E6%8B%89.jpg">
    <div class="card-content">
        <h3>Salad</h3>
        <p class="price">RM 6.90</p>
        <p class="description">Fresh vegetable salad with homemade dressing.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Salad', 6.90)">+</button>
</div>
 <div class="card">
    <img src="https://topcreamery-com.s3.ap-southeast-1.amazonaws.com/wp-content/uploads/2023/01/15221924/Frozen-Desserts.jpg">
    <div class="card-content">
        <h3>Ice Cream</h3>
        <p class="price">RM 5.90</p>
        <p class="description">Smooth ice cream available in various flavors</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Ice Cream', 5.90)">+</button>
</div>
   <div class="card">
    <img src="https://www.wholesomeyum.com/wp-content/uploads/2017/03/wholesomeyum-Low-Carb-Keto-Pancakes-Recipe-21.jpg">
    <div class="card-content">
        <h3>Pancakes</h3>
        <p class="price">RM 7.90</p>
        <p class="description">Soft and fluffy pancakes, served with jam or honey</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Pancakes', 6.90)">+</button>
</div>
   <div class="card">
    <img src="https://funcakes.com/content/uploads/2022/05/Fun-Cakes-20201119-Glutenvrije-Macarons-02-1000x667.jpg">
    <div class="card-content">
        <h3>Macarons</h3>
        <p class="price">RM 8.90</p>
        <p class="description">Delicate French macarons, sweet and flavorful, available in various flavors.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Macarons', 8.90)">+</button>
</div>
   <div class="card">
    <img src="https://assets.epicurious.com/photos/628d02aef79b073d2fe4e130/1:1/w_2488,h_2488,c_limit/Japanese%20Cheesecake%E2%80%94RECIPE.jpg">
    <div class="card-content">
        <h3>Cheesecake</h3>
        <p class="price">RM 11.90</p>
        <p class="description">Creamy cheesecake with a rich flavor.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Cheesecake', 11.90)">+</button>
</div>
   <div class="card">
    <img src="https://sugarpursuit.com/wp-content/uploads/2023/03/Easy-tiramisu-recipe-thumbnail.jpg">
    <div class="card-content">
        <h3>Tiramisu</h3>
        <p class="price">RM 11.90</p>
        <p class="description">Classic Italian dessert with layers of coffee and chocolate flavor.</p>
    </div>
    <button class="w3-button w3-green" onclick="addToCart('Tiramisu', 11.90)">+</button>
</div>

      </div>
    </div>
  </div>

  <!-- JavaScript -->
  <script>
    function openMenu(evt, menuName) {
      // Hide all menu sections
      var i, menuItems;
      menuItems = document.getElementsByClassName("menu");
      for (i = 0; i < menuItems.length; i++) {
        menuItems[i].style.display = "none";
      }

      // Remove "w3-red" class from all tabs
      var tablinks = document.getElementsByClassName("tablink");
      for (i = 0; i < tablinks.length; i++) {
        tablinks[i].className = tablinks[i].className.replace(" w3-red", "");
      }

      // Show the selected menu section and highlight the tab
      document.getElementById(menuName).style.display = "block";
      evt.currentTarget.className += " w3-red";
    }

    // Open the default tab
    document.getElementById("defaultOpen").click();
  </script>

<style>
        /* Container styles */
        .container {
            display: grid;
            grid-template-columns: repeat(4, 1fr); /* Four-column layout */
            gap: 20px; /* Space between grid items */
            padding: 20px;
        }

        .box {
            border: 1px solid #ddd;
            background-color: #654321; /* Dark brown background */
            color: #fff; /* White text */
            padding: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
            border-radius: 10px; /* Rounded corners */
        }

        .circle {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-bottom: 10px;
            background-color: #fff; /* Default avatar background */
        }

        .circle img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .name {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .stars {
            color: gold;
            font-size: 16px;
            margin-bottom: 5px;
        }

        .review {
            font-size: 14px;
            text-align: center;
        }

        /* Button styles */
        .add-review-btn {
            margin: 20px auto;
            display: block;
            padding: 10px 20px;
            background-color: #DAA520; /* Warm color for contrast with brown */
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        .add-review-btn:hover {
            background-color: #B8860B; /* Darker gold */
        }

        /* Modal styles */
        .modal {
            display: none; /* Hidden modal by default */
            position: fixed; /* Fix the position in the viewport */
            top: 90%; /* Move the modal down to 90% of the screen height */
            left: 50%; /* Center horizontally */
            transform: translate(-50%, -50%); /* Adjust for exact centering */
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            background-color: rgba(0, 0, 0, 0.5); /* Dark semi-transparent background */
            justify-content: center;
            align-items: center;
            z-index: 1000; /* Ensure the modal appears on top of other content */
        }

        /* Modal content */
        .modal-content {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            width: 300px; /* Set a specific width */
            text-align: center;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Optional shadow effect */
        }

        .modal-content input, .modal-content textarea, .modal-content select {
            width: 100%;
            margin: 10px 0;
            padding: 8px;
            font-size: 14px;
        }

        .modal-content button {
            padding: 10px 20px;
            background-color: #28a745;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .modal-content button:hover {
            background-color: #218838;
        }

.modal-content {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    width: 300px;
    text-align: center;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    color: #333; /* Ensures all text in the modal is a dark gray or appropriate color */
}

.modal-content h3 {
    color: #000; /* Set the specific color for the heading */
    margin-bottom: 20px;
}
    </style>
</head>
<body>
<!-- Comment/Area Container -->
<div class="w3-container" id="comment" style="padding-bottom:32px;">
    <div class="w3-content" style="max-width:700px; max-height:70px;">
        <h1 class="w3-center w3-jumbo" style="margin-bottom:64px; font-family: 'Cooper Black', sans-serif;">COMMENT</h1>
    </div>
</div>


    <!-- Grid layout -->
    <div class="container" id="reviewContainer">
        <div class="box">
            <div class="circle">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcShe7fsVIyExYqcIsSFAG9b6kMpDm0quQYQoA&s" alt="User 1">
            </div>
            <div class="name">Alex</div>
            <div class="stars">?????</div>
            <div class="review">This is a great cafe I love it so much will come back again.</div>
        </div>
        <div class="box">
            <div class="circle">
                <img src="https://s1.aigei.com/src/img/jpg/18/18f6db8f29004415a7d881a2863a5943.jpg?imageMogr2/auto-orient/thumbnail/!282x282r/gravity/Center/crop/282x282/quality/85/%7CimageView2/2/w/282&e=1735488000&token=P7S2Xpzfz11vAkASLTkfHN7Fw-oOZBecqeJaxypL:8RFf7zPPLGz6XcZN6W5dzKSHrxk=" alt="User 2">
            </div>
            <div class="name">John </div>
            <div class="stars">?????</div>
            <div class="review">Very satisfied, highly recommended!</div>
        </div>
        <div class="box">
            <div class="circle">
                <img src="https://p3-pc-sign.douyinpic.com/tos-cn-i-0813c001/ootlml9AAJzOV4vhO3feZEAzAgAiIgCKNdAD4A~tplv-dy-aweme-images:q75.webp?biz_tag=aweme_images&from=327834062&s=PackSourceEnum_SEARCH&sc=image&se=false&x-expires=1734994800&x-signature=UqjjzUkt0PEkH9Ys526nmZpRrJc%3D" alt="User 3">
            </div>
            <div class="name">May</div>
            <div class="stars">?????</div>
            <div class="review">Great value for money and excellent service!</div>
        </div>
        <div class="box">
            <div class="circle">
                <img src="https://img.k2r2.com/uploads/frombd/0/253/2182420150/2665057502.jpg!190pic" alt="User 4">
            </div>
            <div class="name">Jane</div>
            <div class="stars">?????</div>
            <div class="review">Perfect!</div>
        </div>
    </div>

    
       <!-- Add review button -->
    <button class="add-review-btn" onclick="openModal()">Add Review</button>

    <!-- Modal -->
    <div class="modal" id="reviewModal" onclick="closeModal(event)">
        <div class="modal-content">
            <h3>Add Review</h3>
            <input type="text" id="username" placeholder="Enter your name">
            <textarea id="reviewText" placeholder="Enter your review"></textarea>
            <select id="stars">
                <option value="?????">?????</option>
                <option value="?????">?????</option>
                <option value="?????">?????</option>
                <option value="?????">?????</option>
                <option value="?????">?????</option>
            </select>
            <button onclick="submitReview()">Submit</button>
        </div>
</div>


    <script>
        // Open the modal
        function openModal() {
            document.getElementById('reviewModal').style.display = 'flex';
        }

        // Close the modal when clicking outside
        function closeModal(event) {
            if (event.target === document.getElementById('reviewModal')) {
                document.getElementById('reviewModal').style.display = 'none';
            }
        }

        // Submit review
        function submitReview() {
            const username = document.getElementById('username').value;
            const reviewText = document.getElementById('reviewText').value;
            const stars = document.getElementById('stars').value;

            if (username && reviewText && stars) {
                // Create new review HTML
                const newBox = document.createElement('div');
                newBox.className = 'box';
                newBox.innerHTML = `
                    <div class="circle">
                        <img src="https://cilisos.my/wp-content/uploads/2016/07/unknown-person-icon-Image-from.png" alt="${username}">
                    </div>
                    <div class="name">${username}</div>
                    <div class="stars">${stars}</div>
                    <div class="review">${reviewText}</div>
                `;
                // Append to container
                document.getElementById('reviewContainer').appendChild(newBox);

                // Clear form and close modal
                document.getElementById('username').value = '';
                document.getElementById('reviewText').value = '';
                document.getElementById('stars').value = '?????';
                document.getElementById('reviewModal').style.display = 'none';
            } else {
                alert('Please fill out all fields!');
            }
        }
    </script>

<!-- End page content -->
</div>

    <footer class="w3-container w3-black">
      <button onclick="checkout()" class="w3-button w3-green">Checkout</button>
    </footer>
  </div>
</div>
<!-- Footer -->
<footer class="w3-center w3-light-grey w3-padding-48 w3-large">
  <p>Powered by <a href="https://www.w3schools.com/w3css/default.asp" title="W3.CSS" target="_blank" class="w3-hover-text-green">w3.css</a></p>
</footer>
<style>
        /* Modal Styling */
        .w3-modal-content {
            width: 50%;
            margin: auto;
        }
        .total-price {
            font-size: 18px;
            font-weight: bold;
            margin-top: 10px;
        }

        /* Colorful Thank You Box */
        .thank-you-box {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #FFDDC1; /* Light pink */
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            text-align: center;
            width: 60%;
            max-width: 400px;
            font-size: 18px;
            color: #333;
        }

        .thank-you-box h3 {
            color: #006400; /* Green color for heading */
        }

        .thank-you-box p {
            font-size: 16px;
        }

        .thank-you-box button {
            background-color: #28a745; /* Green button */
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .thank-you-box button:hover {
            background-color: #218838; /* Darker green on hover */
        }
    </style>
</head>
<body>

<!-- Cart Modal -->
<div id="cartModal" class="w3-modal">
    <div class="w3-modal-content w3-animate-top">
        <header class="w3-container w3-black">
            <span onclick="closeCart()" class="w3-button w3-large w3-display-topright">&times;</span>
            <h2>Your Cart</h2>
        </header>
        
        <div class="w3-container" id="cartContent">
            <div id="cartItems"></div>
            <div class="total-price">Total: RM<span id="totalPrice">0.00</span></div>
            <button class="w3-button w3-red" onclick="clearCart()">Clear Cart</button>

            <div>
                <label for="phoneNumber">Enter your phone number:</label>
                <input id="phoneNumber" type="text" class="w3-input" placeholder="Enter phone number here...">
            </div>

            <div>
                <label for="address">Enter your delivery address:</label>
                <textarea id="address" rows="4" class="w3-input" placeholder="Enter address here..."></textarea>
            </div>

            <!-- Payment method selection -->
            <div>
                <label for="paymentMethod">How would you like to pay?</label>
                <div>
                    <label><input type="radio" name="paymentMethod" value="cash" id="paymentCash" class="w3-radio"> Cash on Delivery</label>
                </div>
                <div>
                    <label><input type="radio" name="paymentMethod" value="card" id="paymentCard" class="w3-radio"> Credit Card</label>
                </div>
            </div>

            <button class="w3-button w3-green" onclick="checkout()">Checkout</button>
        </div>
    </div>
</div>

<!-- Cart Button with Badge -->
<button onclick="showCart()">Cart <span id="cart-badge">0</span></button>

<!-- Colorful Thank You Box -->
<div id="thankYouBox" class="thank-you-box">
    <h3>Thank You!</h3>
    <p id="thankYouMessage">Your order has been placed successfully.</p>
    <button onclick="closeThankYou()">Close</button>
</div>

<!-- Footer -->
<footer class="w3-center w3-light-grey w3-padding-48 w3-large">
    <p>Powered by <a href="https://www.w3schools.com/w3css/default.asp" title="W3.CSS" target="_blank" class="w3-hover-text-green">w3.css</a></p>
</footer>

<script>
// Cart initialization
let cart = [];

// Add item to cart
function addToCart(itemName, price) {
  cart.push({ itemName, price });
  updateCartBadge();
  updateCartContent();
}

// Update cart badge
function updateCartBadge() {
  const cartBadge = document.getElementById('cart-badge');
  cartBadge.textContent = cart.length;
}

// Update cart content
function updateCartContent() {
  const cartItemsContainer = document.getElementById('cartItems');
  const totalPriceElement = document.getElementById('totalPrice');
  
  cartItemsContainer.innerHTML = ''; // Clear current cart items
  let totalPrice = 0;

  cart.forEach((item, index) => {
    totalPrice += item.price;
    const cartItem = document.createElement('div');
    cartItem.classList.add('cart-item');
    cartItem.innerHTML = 
      `<span>${index + 1}. ${item.itemName}</span><span>RM${item.price.toFixed(2)}</span>
      <button class="w3-button w3-red w3-small" onclick="removeFromCart(${index})">Remove</button>`;
    cartItemsContainer.appendChild(cartItem);
  });

  totalPriceElement.textContent = totalPrice.toFixed(2); // Display the total price
}

// Remove item from cart
function removeFromCart(index) {
  cart.splice(index, 1);
  updateCartBadge();
  updateCartContent();
}

// Show cart modal
function showCart() {
  const modal = document.getElementById('cartModal');
  modal.style.display = 'block';
}

// Close cart modal
function closeCart() {
  const modal = document.getElementById('cartModal');
  modal.style.display = 'none';
}

// Clear cart
function clearCart() {
  cart = [];
  updateCartBadge();
  updateCartContent();
}

// Checkout function
function checkout() {
  const phoneNumber = document.getElementById('phoneNumber').value;
  const address = document.getElementById('address').value;
  const paymentMethod = document.querySelector('input[name="paymentMethod"]:checked');

  if (!phoneNumber || !address || !paymentMethod) {
    alert("Please enter your phone number, address, and select a payment method.");
    return;
  }

  // Close Cart Modal
  closeCart();

  // Show Colorful Thank You Box
  const thankYouBox = document.getElementById('thankYouBox');
  const thankYouMessage = document.getElementById('thankYouMessage');

  const payment = paymentMethod.value === 'cash' ? 'Cash on Delivery' : 'Credit card';
  thankYouMessage.innerHTML = `Thank you for your order!<br>We will deliver to: ${address}<br>Payment method: ${payment}`;

  // Display the Thank You Box
  thankYouBox.style.display = 'block';

  // Clear the cart
  clearCart(); 
}

// Close Thank You box
function closeThankYou() {
  const thankYouBox = document.getElementById('thankYouBox');
  thankYouBox.style.display = 'none';
}
</script>

<!-- Include Font Awesome for cart icon -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<script>
// Tabbed Menu
function openMenu(evt, menuName) {
  var i, x, tablinks;
  x = document.getElementsByClassName("menu");
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
  tablinks = document.getElementsByClassName("tablink");
  for (i = 0; i < x.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" w3-dark-grey", "");
  }
  document.getElementById(menuName).style.display = "block";
  evt.currentTarget.firstElementChild.className += " w3-dark-grey";
}
document.getElementById("myLink").click();
</script>

</body>
</html>
