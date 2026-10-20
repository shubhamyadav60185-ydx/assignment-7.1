
## 1. Aim

To create a responsive horizontal navigation bar using CSS Flexbox with a logo, navigation links, and a button.

## 2. Objective

- Create a header containing a logo and navigation links.
- Use `display: flex` to arrange elements horizontally.
- Use `justify-content` to manage spacing between elements.
- Use `align-items` to align elements vertically.
- Style navigation links and a button using CSS.
- Make the navigation bar responsive for different screen sizes.

## 3. Project Structure

Create a folder named `Assignment-7.1` and create these two files inside it:

```text
Assignment-7.1/
├── index.html
└── style.css
```

## 4. HTML Code — `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 7.1 - Responsive Navigation Bar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Website Header -->
    <header class="header">
        <nav class="navbar">

            <!-- Website Logo -->
            <a href="#home" class="logo">
                Code<span>Craft</span>
            </a>

            <!-- Navigation Links -->
            <ul class="nav-links">
                <li><a href="#home" class="active">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

            <!-- Navigation Button -->
            <a href="#contact" class="nav-button">Get Started</a>

        </nav>
    </header>

    <!-- Main Content -->
    <main>
        <section class="hero" id="home">
            <p class="tagline">WELCOME TO CODECRAFT</p>

            <h1>Build Your Future with <span>Code</span></h1>

            <p class="description">
                Explore web development, learn new technologies,
                and turn your creative ideas into reality.
            </p>

            <a href="#about" class="hero-button">Explore More</a>
        </section>

        <section class="content-section" id="about">
            <h2>About Us</h2>
            <p>
                CodeCraft is a sample website created to practice
                HTML, CSS, Flexbox, and responsive web design.
            </p>
        </section>

        <section class="content-section alternate" id="services">
            <h2>Our Services</h2>
            <p>
                We explore web design, frontend development,
                and modern website technologies.
            </p>
        </section>

        <section class="content-section" id="projects">
            <h2>Our Projects</h2>
            <p>
                This section can contain website designs,
                student projects, and development work.
            </p>
        </section>

        <section class="content-section alternate" id="contact">
            <h2>Contact Us</h2>
            <p>
                Thank you for visiting CodeCraft.
                Start learning and building your own projects!
            </p>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2026 CodeCraft. Created for Assignment 7.1.</p>
    </footer>

</body>
</html>
```

## 5. CSS Code — `style.css`

```css
/* Reset Default Browser Spacing */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Smooth Scrolling */
html {
    scroll-behavior: smooth;
}

/* General Page Styling */
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f5f7fb;
    color: #1e293b;
    line-height: 1.6;
}

/* Header Styling */
.header {
    background-color: #ffffff;
    box-shadow: 0 3px 12px rgba(0, 0, 0, 0.08);
    position: sticky;
    top: 0;
    z-index: 1000;
}

/* Flexbox Navigation Container */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    min-height: 76px;
    margin: 0 auto;
    padding: 15px 30px;
    gap: 25px;
}

/* Logo Styling */
.logo {
    color: #172554;
    font-size: 28px;
    font-weight: bold;
    text-decoration: none;
    white-space: nowrap;
}

.logo span {
    color: #2563eb;
}

/* Navigation Links Container */
.nav-links {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 28px;
    list-style: none;
}

/* Navigation Link Styling */
.nav-links a {
    color: #334155;
    text-decoration: none;
    font-size: 15px;
    font-weight: 600;
    transition: color 0.3s ease;
}

/* Hover Effect */
.nav-links a:hover,
.nav-links a.active {
    color: #2563eb;
}

/* Get Started Button */
.nav-button {
    display: inline-block;
    background-color: #2563eb;
    color: #ffffff;
    padding: 11px 20px;
    border-radius: 8px;
    text-decoration: none;
    font-weight: bold;
    font-size: 14px;
    white-space: nowrap;
    transition: background-color 0.3s ease;
}

.nav-button:hover {
    background-color: #1d4ed8;
}

/* Hero Section */
.hero {
    min-height: 430px;
    padding: 100px 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    background: linear-gradient(135deg, #eff6ff, #dbeafe);
}

.tagline {
    color: #2563eb;
    font-size: 13px;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 15px;
}

.hero h1 {
    font-size: 42px;
    line-height: 1.2;
    margin-bottom: 20px;
}

.hero h1 span {
    color: #2563eb;
}

.description {
    max-width: 600px;
    color: #475569;
    margin-bottom: 28px;
}

.hero-button {
    display: inline-block;
    background-color: #172554;
    color: #ffffff;
    text-decoration: none;
    padding: 12px 24px;
    border-radius: 8px;
    font-weight: bold;
}

.hero-button:hover {
    background-color: #334155;
}

/* Content Sections */
.content-section {
    padding: 65px 20px;
    text-align: center;
    background-color: #ffffff;
}

.content-section h2 {
    color: #172554;
    font-size: 28px;
    margin-bottom: 15px;
}

.content-section p {
    max-width: 650px;
    margin: 0 auto;
    color: #475569;
}

.alternate {
    background-color: #f1f5f9;
}

/* Footer */
.footer {
    padding: 22px 15px;
    background-color: #172554;
    color: #ffffff;
    text-align: center;
    font-size: 14px;
}

/* Responsive Design for Tablets and Smaller Screens */
@media (max-width: 900px) {
    .navbar {
        flex-wrap: wrap;
        justify-content: space-between;
        gap: 18px;
    }

    .nav-links {
        gap: 18px;
    }

    .nav-links a {
        font-size: 14px;
    }

    .hero h1 {
        font-size: 34px;
    }
}

/* Responsive Design for Mobile Phones */
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 18px 15px;
        gap: 18px;
    }

    .nav-links {
        width: 100%;
        flex-wrap: wrap;
        justify-content: center;
        gap: 12px 20px;
    }

    .nav-links a {
        font-size: 14px;
    }

    .nav-button {
        padding: 10px 18px;
    }

    .hero {
        min-height: 350px;
        padding: 70px 18px;
    }

    .hero h1 {
        font-size: 30px;
    }

    .description {
        font-size: 14px;
    }

    .content-section {
        padding: 45px 18px;
    }
}
```

## 6. Explanation of CSS Flexbox Properties

### `display: flex`

It arranges the direct child elements of a container in a row by default.

```css
.navbar {
    display: flex;
}
```

### `justify-content: space-between`

It distributes available horizontal space between the logo, navigation links, and button.

```css
.navbar {
    justify-content: space-between;
}
```

### `align-items: center`

It aligns the elements vertically in the center of the navigation bar.

```css
.navbar {
    align-items: center;
}
```

### `gap`

It creates space between navigation links without adding margins to individual links.

```css
.nav-links {
    display: flex;
    gap: 28px;
}
```

### Media Queries

Media queries change the layout according to the screen width. On smaller screens, the navigation items wrap onto additional lines and the navbar changes to a vertical layout.

```css
@media (max-width: 600px) {
    .navbar {
        flex-direction: column;
    }
}
```

## 7. How to Run the Project

1. Create a folder named `Assignment-7.1`.
2. Open the folder in Visual Studio Code.
3. Create `index.html` and `style.css`.
4. Copy the complete HTML code into `index.html`.
5. Copy the complete CSS code into `style.css`.
6. Save both files using `Ctrl + S`.
7. Open `index.html` in a browser, or use the Live Server extension in VS Code.
8. Resize the browser window to inspect the responsive layout.

## 8. Testing and Observation

Test the website at different browser widths:

| Screen | Expected Result |
|---|---|
| Desktop — 1200px or wider | Logo, links, and button appear in a horizontal navigation bar. |
| Tablet — around 768px | Navigation items adjust their spacing and can wrap if required. |
| Mobile — 600px or narrower | Logo, navigation links, and button are arranged vertically. |
| Hover over links | Link text changes to blue. |
| Click navigation links | The page scrolls to the matching section. |

## 9. Expected Output

The website displays a clean horizontal navigation bar with:

- A **CodeCraft** logo on the left.
- Home, About, Services, Projects, and Contact links.
- A blue **Get Started** button.
- A hero section and supporting content sections.
- Responsive styling for desktop, tablet, and mobile screens.

## 10. Submission Checklist

- [ ] `index.html` created successfully.
- [ ] `style.css` created successfully.
- [ ] Logo and navigation links displayed correctly.
- [ ] `display: flex` applied to the navigation container.
- [ ] `justify-content` used for spacing.
- [ ] `align-items` used for vertical alignment.
- [ ] Navigation links and button styled properly.
- [ ] Website tested at different browser widths.
- [ ] Screenshot of desktop view captured.
- [ ] Screenshot of mobile view captured.

## 11. Conclusion

In this assignment, I created a responsive navigation bar using HTML and CSS Flexbox. I learned how to arrange a logo, navigation links, and a button using `display: flex`, `justify-content`, `align-items`, and `gap`. I also used CSS media queries to make the navigation bar suitable for desktop, tablet, and mobile screens.
