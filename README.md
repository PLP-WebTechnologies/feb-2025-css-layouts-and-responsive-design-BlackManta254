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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }

        nav {
            background-color: #444;
            padding: 10px;
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style-type: none;
            margin: 0;
            padding: 0;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            padding: 20px;
        }

        .content, .sidebar {
            background-color: #f4f4f4;
            padding: 20px;
            margin: 10px;
            border-radius: 8px;
            flex: 1;
        }

        .sidebar {
            flex: 0 0 25%;
        }

        .content {
            flex: 0 0 70%;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
        }

        /* Media Queries for Responsiveness */
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
                align-items: center;
            }

            .sidebar {
                flex: 0 0 100%;
            }

            .content {
                flex: 0 0 100%;
            }

            nav ul {
                flex-direction: column;
            }
        }

        @media (max-width: 480px) {
            header {
                font-size: 18px;
            }

            nav ul li {
                margin: 5px 0;
            }
        }
    </style>
</head>
<body>

<header>
    <h1>Responsive Website</h1>
</header>

<nav>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>

<div class="container">
    <div class="content">
        <h2>Main Content</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut purus orci. Integer placerat magna vel bibendum tincidunt.</p>
    </div>
    <div class="sidebar">
        <h3>Sidebar</h3>
        <p>Sidebar content goes here.</p>
    </div>
</div>

<footer>
    <p>© 2025 Responsive Website</p>
</footer>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with CSS Grid</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }

        nav {
            background-color: #444;
            padding: 10px;
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style-type: none;
            margin: 0;
            padding: 0;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
        }

        .container {
            display: grid;
            grid-template-columns: 70% 25%;
            gap: 20px;
            padding: 20px;
        }

        .content, .sidebar {
            background-color: #f4f4f4;
            padding: 20px;
            margin: 10px;
            border-radius: 8px;
        }

        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
        }

        /* Media Queries for Responsiveness */
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }

            nav ul {
                flex-direction: column;
            }
        }

        @media (max-width: 480px) {
            header {
                font-size: 18px;
            }

            nav ul li {
                margin: 5px 0;
            }
        }
    </style>
</head>
<body>

<header>
    <h1>Responsive Website</h1>
</header>

<nav>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>

<div class="container">
    <div class="content">
        <h2>Main Content</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent ut purus orci. Integer placerat magna vel bibendum tincidunt.</p>
    </div>
    <div class="sidebar">
        <h3>Sidebar</h3>
        <p>Sidebar content goes here.</p>
    </div>
</div>

<footer>
    <p>© 2025 Responsive Website</p>
</footer>

</body>
</html>

Happy Coding! 💻✨
