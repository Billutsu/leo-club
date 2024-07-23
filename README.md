<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canaan City Leo Club</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="logo-container">
                <img src="leo-club-logo.png" alt="LEO Club Logo" class="logo">
                <img src="lions-club-logo.png" alt="Lions Club Logo" class="logo">
            </div>
            <h1>Welcome to Canaan City Leo Club</h1>
            <button class="toggle-menu">Menu</button>
            <nav>
                <ul>
                    <li><a href="#about">About Us</a></li>
                    <li><a href="#events">Events</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#register">Register</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <main>
        <section id="about">
            <div class="container">
                <h2>About Us</h2>
                <p>The Canaan City Leo Club is a youth organization dedicated to community service and leadership development. We are part of the international Leo Club Program, which provides young people with an opportunity to grow personally and professionally.</p>
            </div>
        </section>
        
        <section id="events">
            <div class="container">
                <h2>Upcoming Events</h2>
                <ul>
                    <li><strong>Event 1:</strong> CLUB GENERAL MEETING - Date: July 30, 2024</li>
                    <li><strong>Event 2:</strong> Fundraising Marathon - Date: August 15, 2024</li>
                    <li><strong>Event 3:</strong> Youth Leadership Workshop - Date: September 10, 2024</li>
                </ul>
            </div>
        </section>
        
        <section id="contact">
            <div class="container">
                <h2>Contact Us</h2>
                <p>If you have any questions or want to join our club, feel free to reach out!</p>
                <address>
                    Email: <a href="mailto:info@canaanleoclub.org">info@canaanleoclub.org</a><br>
                    Phone: +234 9024334822<br>
                    Address: BIG MUNCH EDIBA ROAD, Calabar, Nigeria
                </address>
            </div>
        </section>

        <section id="register">
            <div class="container">
                <h2>Event Registration</h2>
                <form id="registrationForm">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name" required>
                    
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>
                    
                    <button type="submit">Register</button>
                </form>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2024 Canaan City Leo Club. All Rights Reserved.</p>
        </div>
    </footer>

    <script src="scripts.js"></script>
</body>
</html>
<div class="logo-container">
    <a href="https://www.lionsclubs.org/en" target="_blank">
        <img src="leo-club-logo.png" alt="LEO Club Logo" class="logo">
    </a>
    <a href="https://www.lionsclubs.org/en" target="_blank">
        <img src="lions-club-logo.png" alt="Lions Club Logo" class="logo">
    </a>
</div>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

.container {
    width: 80%;
    margin: 0 auto;
    max-width: 1200px;
}

header {
    background: #003366;
    color: #fff;
    padding: 1rem 0;
    position: relative;
}

.logo-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 1rem;
}

.logo {
    max-width: 100px;  /* Adjust size as needed */
    margin: 0 10px;
}

header h1 {
    text-align: center;
    margin: 0;
}

nav ul {
    list-style: none;
    padding: 0;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

nav ul li {
    margin: 0 15px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
    font-weight: bold;
}

.toggle-menu {
    display: none;
    background: #003366;
    color: #fff;
    border: none;
    font-size: 1.2rem;
    padding: 0.5rem 1rem;
    position: absolute;
    right: 10px;
    top: 10px;
    cursor: pointer;
}

main {
    padding: 2rem 0;
}

section {
    margin-bottom: 2rem;
}

h2 {
    color: #003366;
    margin-bottom: 1rem;
}

footer {
    background: #003366;
    color: #fff;
    text-align: center;
    padding: 1rem 0;
    position: fixed;
    width: 100%;
    bottom: 0;
}

address {
    font-style: normal;
}

form {
    max-width: 500px;
    margin: 0 auto;
    background: #f4f4f4;
    padding: 1rem;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
}

form input {
    width: 100%;
    padding: 0.5rem;
    margin-bottom: 1rem;
    border: 1px solid #ccc;
    border-radius: 5px;
}

form button {
    display: block;
    width: 100%;
    padding: 0.5rem;
    background: #003366;
    color: #fff;
    border: none;
    border-radius: 5px;
    font-size: 1rem;
    cursor: pointer;
}

form button:hover {
    background: #0055a5;
}

@media (max-width: 768px) {
    .toggle-menu {
        display: block;
    }
    
    nav ul {
        display: none;
        flex-direction: column;
        align-items: center;
        background: #003366;
        padding: 1rem 0;
    }
    
    nav ul.active {
        display: flex;
    }
    
    nav ul li {
        margin: 10px 0;
    }
}
// Smooth scrolling for navigation links
document.querySelectorAll('nav a').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const targetId = this.getAttribute('href').substring(1);
        const targetElement = document.getElementById(targetId);
        
        if (targetElement) {
            window.scrollTo({
                top: targetElement.offsetTop,
                behavior: 'smooth'
            });
        }
    });
});

// Toggle menu for mobile view
const toggleButton = document.querySelector('.toggle-menu');
const navMenu = document.querySelector('nav ul');

toggleButton.addEventListener('click', () => {
    navMenu.classList.toggle('active');
});

// Form submission
const registrationForm = document.getElementById('registrationForm');

registrationForm.addEventListener('submit', function (e) {
    e.preventDefault();
    
    // Example: Get the form data
    const formData = new FormData(this);
    const name = formData.get('name');
    const email = formData.get('email');
    
    // Example: Simple validation
   
