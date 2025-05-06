# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


HTML CODES
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout with Flexbox</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Navigation Bar -->
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <!-- Main Content -->
  <div class="container">
    <section class="sidebar">
      <h2>Sidebar</h2>
      <p>Content for sidebar...</p>
    </section>

    <section class="main-content">
      <h2>Main Content</h2>
      <p>This is where the main content goes...</p>
    </section>
  </div>

  <footer>
    <p>&copy; 2025 Your Website</p>
  </footer>
</body>
</html>


CSS CODES
/* Basic Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Global Styles */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
  padding: 0 20px;
}

/* Navigation Bar */
nav {
  background-color: #333;
  padding: 10px;
}

nav ul {
  display: flex;
  justify-content: center;
  list-style-type: none;
}

nav ul li {
  margin: 0 15px;
}

nav ul li a {
  color: white;
  text-decoration: none;
  font-size: 18px;
}

/* Main Layout */
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 20px;
}

.sidebar {
  flex: 1;
  background-color: #ddd;
  padding: 20px;
  margin-right: 20px;
}

.main-content {
  flex: 2;
  background-color: #fff;
  padding: 20px;
  margin-left: 20px;
}

/* Footer */
footer {
  text-align: center;
  margin-top: 20px;
  background-color: #333;
  color: white;
  padding: 10px;
}

/* Media Queries */
@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    align-items: center;
  }

  .container {
    flex-direction: column;
  }

  .sidebar, .main-content {
    margin: 0;
    width: 100%;
  }
}

@media (max-width: 480px) {
  nav ul {
    font-size: 16px;
  }

  .sidebar, .main-content {
    padding: 10px;
  }
}

