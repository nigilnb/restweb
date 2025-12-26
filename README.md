# Ex.07 Restaurant Website
## Date: 26/12/2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LOCATION MULTI CUISINE RESTAURENT</title>
    <style>
        body {
            background-color: #FFF8F0;
            margin: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
            color: #4B1D0F;
        }
        header {
            background-color: #B23A48;
            color: #FFF8F0;
            text-align: center;
            padding: 30px 10px 20px 10px;
        }
        nav {
            background-color: #F39237;
            overflow: hidden;
        }
        nav a {
            float: left;
            display: block;
            color: #4B1D0F;
            text-align: center;
            padding: 16px 36px;
            text-decoration: none;
            font-weight: bold;
        }
        nav a:hover {
            background-color: #FFD166;
            color: #B23A48;
        }
        .banner {
            width: 100%;
            height: 360px;
            background-image: url(restaurent.avif);
            background-size: cover;
            background-position: center;
        }
        .container {
            max-width: 1000px;
            margin: 40px auto;
            padding: 24px;
            background-color: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 24px rgba(180,58,72,0.07);
        }
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 22px;
        }
        .menu-item {
            background: #FFF8F0;
            border: 1px solid #FFD166;
            border-radius: 8px;
            padding: 20px 12px;
            text-align: center;
        }
        .menu-item img {
            width: 90px;
            height: 70px;
            object-fit: cover;
            border-radius: 8px;
        }
        .admin-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 28px;
            margin-top: 18px;
        }
        .admin-card {
            background: #FFF8F0;
            border: 1px solid #FFD166;
            border-radius: 8px;
            text-align: center;
            padding: 24px 12px;
        }
        .admin-card img {
            width: 78px;
            height: 78px;
            border-radius: 50%;
            object-fit: cover;
        }
        footer {
            background: #B23A48;
            color: #FFF8F0;
            text-align: center;
            padding: 18px 0 8px 0;
            position: relative;
        }
        .active {
            background-color: #FFD166;
            color: #B23A48 !important;
        }
        @media (max-width: 800px) {
            .menu-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            .admin-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        @media (max-width: 500px) {
            .menu-grid, .admin-grid {
                grid-template-columns: 1fr;
            }
            nav a {
                float: none;
                display: block;
            }
        }
    </style>
    <script>
        function showPage(pageId) {
            document.querySelectorAll('.container').forEach(c=>c.style.display='none');
            document.getElementById(pageId).style.display = 'block';
            document.querySelectorAll('nav a').forEach(a=>a.classList.remove('active'));
            document.getElementById('nav-' + pageId).classList.add('active');
        }
        window.onload = function() {
            showPage('home');
        }
    </script>
</head>
<body>
    <header>
        <div class="banner"></div>
        <h1>LOCATION MULTI CUISINE RESTAURENT</h1>
        <p>Nourish Your Body, Feed Your Soul!</p>
    </header>
    <nav>
        <a id="nav-home" href="#" onclick="showPage('home');return false;">Home</a>
        <a id="nav-menu" href="#" onclick="showPage('menu');return false;">Menu</a>
        <a id="nav-admin" href="#" onclick="showPage('admin');return false;">Administration</a>
        <a id="nav-contact" href="#" onclick="showPage('contact');return false;">Contact Us</a>
    </nav>
    <div id="home" class="container">
        <h2>Welcome. Discover the art of multi cuisine!</h2>
        <p>Welcome to our restaurent, where every dish is a celebration of fresh, flavorful ingredients. We invite you to experience a culinary journey that delights the senses with our traditional recipes and innovative creations, all crafted with passion and care.We promise a wholesome and satisfying dining experience that will leave you feeling nourished and refreshed. </p>
    </div>
    <div id="menu" class="container" style="display:none;">
        <h2>Our Menu</h2>
        <div class="menu-grid">
            <div class="menu-item"><img src="CHICKEN LOLI.webp"><br>CHICKEN LOLIPOP<br>₹190</div>
            <div class="menu-item"><img src="CHICken manchhorien.jpg"><br>CHICKEN MANCHURIEN<br>₹210</div>
            <div class="menu-item"><img src="Dragon-Chicken.jpg"><br>DRAGON CHICKEN<br>₹260</div>
            <div class="menu-item"><img src="broasted chicken.webp"><br>BROASTED CHICKEN FULL 8PC/KHUBOOS,FRENCH FRIES<br>₹660</div>
            <div class="menu-item"><img src="Vegetable-Dum-Biryani.jpg"><br>VEG BIRIYANI<br>₹145</div>
            <div class="menu-item"><img src="chilli paroota.jpg"><br>CHILLI PAROTTA<br>₹100</div>
            <div class="menu-item"><img src="chicken mandhi.avif"><br>CHICKEN MANDHI<br>₹800</div>
            <div class="menu-item"><img src="mutton mandhi.webp"><br>MUTTON MANDHI<br>₹1500</div>
            <div class="menu-item"><img src="chicken biriyani.jpg"><br>CHICKEN BIRIYANI<br>₹220</div>
            <div class="menu-item"><img src="Mutton-Biryani.webp"><br>MUTTON BIRIYANI<br>₹440</div>
            <div class="menu-item"><img src="french fries.avif"><br>MUTTON BIRIYANI<br>₹150</div>
            
        </div>
    </div>
    <div id="admin" class="container" style="display:none;">
        <h2>Administration</h2>
        <div class="admin-grid">
            <div class="admin-card">
                <img src="MANAGER.jpg">
                <b>RICHARD</b><br>
                Manager
            </div>
            <div class="admin-card">
                <img src="Chef_Dhamu.avif">
                <b>K.DAMODHARAN</b><br>
                Head Chef
            </div>
            <div class="admin-card">
                <img src="KOUSHIK.jpg">
                <b>KOUSHIK SHANKAR</b><br>
                Lead Cook
            </div>
            <div class="admin-card">
                <img src="MARKETTING HEAD.avif">
                <b>Anjali</b><br>
                Marketing Head
            </div>
            <div class="admin-card">
                <img src="FINANCE.webp">
                <b>ROBERT</b><br>
                Finance Manager
            </div>
            <div class="admin-card">
                <img src="SARAH.webp">
                <b>SARAH</b><br>
                Customer Relations
            </div>
        </div>
    </div>
    <div id="contact" class="container" style="display:none;">
        <h2>Contact Us</h2>
        <p><b>Address:</b> AZHAGIYAMANDABAM JN,THUCKALAY,KANYAKUAMRI</p>
        <p><b>Phone:</b>+91 XXXXXXXXXX</p>
        <p><b>Email:</b> info@LOCATION MULTI CUISINE RESTAURENT.com</p>
        <p>We welcome all your feedback and enquiries!</p>
    </div>
    <footer>
        &copy; 2025 LOCATION MULTI CUISINE RESTAURENT.
    </footer>
</body>
</html>
```


## OUTPUT:
![alt text](<Screenshot 2025-12-26 214250-2.png>) ![alt text](<Screenshot 2025-12-26 214316-2.png>) ![alt text](<Screenshot 2025-12-26 214345-2.png>) ![alt text](<Screenshot 2025-12-26 214410-2.png>) 





## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
