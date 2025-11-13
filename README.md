# Ex.07 Restuarant Website
## Date:30-10-25

## AIM:
To develop a static Resturant website to display the menu and services provided by the resturant.

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
index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Taste Haven Restaurant</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Taste Haven Restaurant</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="gallery.html">Gallery</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <h2>Delicious Food, Cozy Ambience</h2>
    <p>Experience the best dishes made with love and fresh ingredients.</p>
    <a href="menu.html" class="btn">Explore Menu</a>
  </section>

  <footer>
    <p>© 2025 Taste Haven Restaurant | Designed by Mithun Rono</p>
  </footer>
</body>
</html>

menu.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menu - Taste Haven</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Our Menu</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="gallery.html">Gallery</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="menu">
    <div class="menu-item">
      <h3>Grilled Chicken</h3>
      <p>Served with garlic sauce and fries — ₹250</p>
    </div>
    <div class="menu-item">
      <h3>Paneer Butter Masala</h3>
      <p>Creamy tomato-based curry with soft paneer cubes — ₹200</p>
    </div>
    <div class="menu-item">
      <h3>Veg Fried Rice</h3>
      <p>Spicy and flavorful rice loaded with veggies — ₹150</p>
    </div>
    <div class="menu-item">
      <h3>Chocolate Lava Cake</h3>
      <p>Warm and gooey chocolate delight — ₹180</p>
    </div>
  </section>

  <footer>
    <p>© 2025 Taste Haven Restaurant</p>
  </footer>
</body>
</html>

gallery.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gallery - Taste Haven</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Our Gallery</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="gallery.html">Gallery</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="gallery">
    <h2>Delicious Moments Captured</h2>
    <div class="gallery-grid">
      <img src="https://images.unsplash.com/photo-1600891964599-f61ba0e24092?w=800" alt="Pasta Dish">
      <img src="https://images.unsplash.com/photo-1546069901-ba9599a7e63c?w=800" alt="Fresh Salad">
      <img src="https://images.unsplash.com/photo-1594007654729-407eedc4be65?w=800" alt="Pizza">
      <img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836?w=800" alt="Burger">
      <img src="https://images.unsplash.com/photo-1551024601-bec78aea704b?w=800" alt="Dessert">
      <img src="https://images.unsplash.com/photo-1551782450-a2132b4ba21d?w=800" alt="Grilled Chicken">
    </div>
  </section>

  <footer>
    <p>© 2025 Taste Haven Restaurant</p>
  </footer>
</body>
</html>

conact.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contact - Taste Haven</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Contact Us</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="gallery.html">Gallery</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="contact">
    <h2>Get in Touch</h2>
    <p>📍 Location: 123 Food Street, Sivakasi</p>
    <p>📞 Phone: +91 98765 43210</p>
    <p>✉️ Email: info@tastehaven.com</p>

    <h3>Reserve a Table</h3>
    <form class="reservation-form">
      <input type="text" placeholder="Your Name" required>
      <input type="email" placeholder="Email Address" required>
      <input type="tel" placeholder="Phone Number" required>
      <input type="date" required>
      <input type="time" required>
      <textarea placeholder="Special Requests"></textarea>
      <button type="submit">Book Now</button>
    </form>
  </section>

  <footer>
    <p>© 2025 Taste Haven Restaurant</p>
  </footer>
</body>
</html>

about.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>About - Taste Haven</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>About Us</h1>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="menu.html">Menu</a></li>
        <li><a href="gallery.html">Gallery</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="about">
    <h2>Welcome to Taste Haven</h2>
    <p>We are passionate about serving delicious and freshly prepared meals that bring people together. 
    Our chefs use only the finest ingredients to create mouth-watering dishes that satisfy every craving.</p>

    <p>From Indian classics to continental delights, we believe every plate tells a story. 
    Come, experience food made with love and served with warmth.</p>
  </section>

  <footer>
    <p>© 2025 Taste Haven Restaurant</p>
  </footer>
</body>
</html>

style.css

/* ====== General Styles ====== */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background-color: #fff8f0;
  color: #333;
}

header {
  background-color: #c0392b;
  color: white;
  padding: 15px 0;
  text-align: center;
}

nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

nav ul li {
  display: inline;
  margin: 0 15px;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

nav ul li a:hover {
  text-decoration: underline;
}

/* ====== Hero Section ====== */
.hero {
  text-align: center;
  padding: 70px 20px;
  background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)),
    url('https://images.unsplash.com/photo-1551782450-17144efb9c50');
  background-size: cover;
  background-position: center;
  color: white;
}

.hero h2 {
  font-size: 2.5em;
  margin-bottom: 10px;
}

.hero p {
  font-size: 1.2em;
  margin-bottom: 20px;
}

.btn {
  background-color: #e67e22;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
}

.btn:hover {
  background-color: #d35400;
}

/* ====== Menu Section ====== */
.menu {
  padding: 30px;
  text-align: center;
}

.menu-item {
  background: #ffe6e6;
  margin: 15px auto;
  padding: 15px;
  width: 60%;
  border-radius: 10px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.2);
}

/* ====== Gallery Section ====== */
.gallery {
  padding: 30px;
  text-align: center;
}

.gallery h2 {
  margin-bottom: 20px;
  color: #c0392b;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 15px;
  margin: 0 auto;
  max-width: 1000px;
}

.gallery-grid img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border-radius: 10px;
  transition: transform 0.3s, box-shadow 0.3s;
}

.gallery-grid img:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 10px rgba(0,0,0,0.3);
}

/* ====== About Section ====== */
.about {
  padding: 30px;
  text-align: center;
  width: 80%;
  margin: auto;
}

/* ====== Contact Section ====== */
.contact {
  padding: 30px;
  text-align: center;
}

.reservation-form {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 60%;
  margin: 20px auto;
}

.reservation-form input,
.reservation-form textarea {
  width: 100%;
  padding: 10px;
  margin: 8px 0;
  border-radius: 5px;
  border: 1px solid #ccc;
}

.reservation-form button {
  background-color: #c0392b;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

.reservation-form button:hover {
  background-color: #a93226;
}

/* ====== Footer ====== */
footer {
  background-color: #c0392b;
  color: white;
  text-align: center;
  padding: 10px;
  position: relative;
  bottom: 0;
  width: 100%;
}
```

## OUTPUT:
<img width="1918" height="1137" alt="1" src="https://github.com/user-attachments/assets/690d3989-085a-4928-94c4-728a32168b3e" />
<img width="1918" height="1117" alt="2" src="https://github.com/user-attachments/assets/4e588c3b-073e-4f00-b7c7-72c9d6675517" />
<img width="1918" height="1123" alt="3" src="https://github.com/user-attachments/assets/3e3e0113-3f1b-4fd1-be41-84853189e1b6" />
<img width="1918" height="1068" alt="4" src="https://github.com/user-attachments/assets/10cc0397-2ba0-4373-b5f4-8b7bb4170bdd" />
<img width="1916" height="1118" alt="5" src="https://github.com/user-attachments/assets/3a201d9e-2d1b-47a1-987b-19ef81dfb9d6" />





## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
