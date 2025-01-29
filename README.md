<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bookstore</title>
  <link rel="stylesheet" href="style.css">

  <style>
    /* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    background-image: linear-gradient(to right, #8E2DE2, #4A00E0); /* Attractive gradient background */
    color: white;
}

ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
}

a {
    text-decoration: none;
    color: inherit;
}

header, footer {
    background-color: #333;
    color: white;
}

footer {
    padding: 10px;
    text-align: center;
}

footer ul {
    display: flex;
    justify-content: center;
}

footer ul li {
    margin: 0 15px;
}

/* Navbar */
.navbar {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    background-color: #333;
}

.navbar ul {
    display: flex;
}

.navbar ul li {
    margin-right: 20px;
}

.navbar a {
    color: white;
    padding: 10px;
    font-size: 16px;
}

/* Dropdown Styles */
.dropdown {
    position: relative;
}

.dropbtn {
    background-color: #333;
    color: white;
    padding: 10px;
    border: none;
    cursor: pointer;
    font-size: 16px;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
    z-index: 1;
    top: 100%; /* Position the dropdown below the button */
    left: 0;
    border-radius: 4px;
}

.dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    font-size: 14px;
    background-color: white;
    border-bottom: 1px solid #ddd;
}

.dropdown-content a:hover {
    background-color: #ddd;
    color: #333;
}

.dropdown:hover .dropdown-content {
    display: block;
}

.dropdown:hover .dropbtn {
    background-color: #444; /* Change background color on hover */
}

/* Bookstore Title Section */
.title-section {
    text-align: center;
    padding: 50px;
    color: #fff;
    background-color: rgba(0, 0, 0, 0.5); /* Semi-transparent background */
    margin-bottom: 40px;
}

.title-section h1 {
    font-size: 48px;
}

.title-section p {
    font-size: 18px;
    margin-top: 10px;
}

/* Main Section */
.book-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr); /* Four items in one row */
    gap: 20px;
    padding: 20px;
}

.book-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 15px;
    text-align: center;
    background-color: white;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: box-shadow 0.3s ease, transform 0.3s ease, background-color 0.3s ease;
}

/* Hover Effect on Book Card */
.book-card:hover {
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    transform: translateY(-5px); /* Slight lift effect */
    background-color: #f1f1f1;
}

/* Different button colors for each card */
.book-card .wishlist {
    background-color: #e60000;
}

.book-card .read-more {
    background-color: #0066cc;
}

.book-card .buy-now {
    background-color: #28a745;
}

/* Hover Effects on Buttons Inside the Card */
.book-card:hover button {
    background-color: #444; /* Darker button background on hover */
}

.book-card img {
    width: 200px;
    height: auto;
    border-radius: 8px;
    margin-bottom: 10px;
}

.book-card h3 {
    font-size: 20px;
    margin-top: 15px;
    background: linear-gradient(to left, #ff7e5f, #feb47b); /* Gradient color for title */
    -webkit-background-clip: text;
    color: transparent;
    text-transform: uppercase; /* Uppercase for a bolder look */
}

.book-card .author {
    font-size: 14px;
    color: #d8b1ff; /* Subtle light lavender for author */
    margin-top: 5px;
}

/* Author Styling Hover Effect */
.book-card .author:hover {
    color: #fff; /* Make it white when hovered */
}

.book-card .description {
    font-size: 14px;
    margin-top: 10px;
    color: #333;
}

.book-card .price {
    font-size: 16px;
    margin-top: 15px;
    color: #e60000;
}

button {
    color: white;
    padding: 10px;
    margin-top: 10px;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #555;
}

/* Footer */
footer a {
    color: white;
}

footer a:hover {
    text-decoration: underline;
}

  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <nav class="navbar">
      <ul>
        <li><a href="#">Home</a></li>
        <li class="dropdown">
          <a href="#" class="dropbtn">Categories</a>
          <div class="dropdown-content">
            <a href="#">Fiction</a>
            <a href="#">Non-fiction</a>
            <a href="#">Finance</a>
            <a href="#">Thriller</a>
          </div>
        </li>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Bookstore Title -->
  <section class="title-section">
    <h1>Welcome to The Book Heaven</h1>
    <p>Your one-stop shop for the best books across all genres!</p>
  </section>

  <!-- Main Section -->
  <main>
    <section class="book-grid">
      <!-- Example Book Card -->
      <div class="book-card">
        <img src="images5/psy.jpg" alt="Psychology of Money">
        <h3>Psychology of Money</h3>
        <p class="author">Morgan Housel</p>
        <p class="description">Doing well with money isn't necessarily about what you know. It's about how you behave. And behavior is hard to teach, even to really smart people...</p>
        <p class="price">$26.15</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

      <div class="book-card">
        <img src="images5/pap.jpg" alt="Pride and Prejudice">
        <h3>Pride and Prejudice</h3>
        <p class="author">Jane Austen</p>
        <p class="description">Elizabeth Bennet's journey of overcoming initial prejudice against the wealthy Mr. Darcy, leading to a transformative love story despite their social differences.</p>
        <p class="price">$24.65</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

      <div class="book-card">
        <img src="images5/ge.jpg" alt="Great Expectations">
        <h3>Great Expectations</h3>
        <p class="author"> Charles Dickens</p>
        <p class="description">Great Expectations is one of Charles Dickens's finest and well-received novels, a coming-of-age story about social ambition, love, crime, and the disappointment of expectations.</p>
        <p class="price">$9.56</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

      <div class="book-card">
        <img src="images5/2tl.jpg" alt="To the Lighthouse">
        <h3>To the Lighthouse</h3>
        <p class="author">Virginia Woolf</p>
        <p class="description">Explores the complex dynamics of a family, particularly the matriarchal Mrs. Ramsay, through the lens of a planned but ultimately postponed trip to a nearby lighthouse.</p>
        <p class="price">$17.89</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

      <div class="book-card">
        <img src="images5/wap.jpg" alt="War and Peace">
        <h3>War and Peace</h3>
        <p class="author">Leo Tolstoy</p>
        <p class="description">A man on a thousand mile walk has to forget his goal and say to himself every morning, 'Today I'm going to cover twenty-five miles and then rest up and sleep.</p>
        <p class="price">$10.54</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

      <div class="book-card">
        <img src="images5/asb.jpg" alt="A Suitable Boy">
        <h3>A Suitable Boy</h3>
        <p class="author">Vikram Seth</p>
        <p class="description">A sprawling novel about a young Indian woman, Lata, navigating the complexities of love and family in post-partition India.</p>
        <p class="price">$12.34</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

      <div class="book-card">
        <img src="images5/tgp.jpg" alt="The Glass Palace">
        <h3>The Glass Palace</h3>
        <p class="author">Amitav Ghosh</p>
        <p class="description">Follows the life of a young Indian boy, Rajkumar, caught up in the turbulent political landscape of Burma during the British colonial era.</p>
        <p class="price">$22.79</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

      <div class="book-card">
        <img src="images5/afotc.jpg" alt="A Tale of Two Cities">
        <h3>A Tale of Two Cities</h3>
        <p class="author">Charles Dickens</p>
        <p class="description">“It was the best of times, it was the worst of times…” This line famously opens Charles Dickens' historical novel, A Tale of Two Cities.</p>
        <p class="price">$20.25</p>
        <button class="wishlist">Add to wish list</button>
        <button class="read-more">Read More</button>
        <button class="buy-now">Buy Now</button>
      </div>

    </section>
  </main>

  <!-- Footer -->
  <footer>
    <ul>
      <li><a href="#">Privacy Policy</a></li>
      <li><a href="#">Terms & Conditions</a></li>
    </ul>
  </footer>

</body>
</html>

