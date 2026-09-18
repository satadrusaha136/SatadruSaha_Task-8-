# Task 8 - CSS Hamburger Menu and Responsive Design

## Project Overview

This project demonstrates a responsive Laundry Services webpage using HTML and CSS.

The webpage is designed to work across:

- Desktop
- Tablet
- Mobile
- Extra Small Mobile

The responsive navigation changes into a hamburger menu on tablet, mobile, and extra small mobile screen sizes.

---

## Technologies Used

- HTML5
- CSS3
- CSS Media Queries
- CSS Variables
- CSS Pseudo-classes
- CSS Pseudo-elements
- Flexbox

No JavaScript or Bootstrap is used for the hamburger menu.

---

## Responsive Breakpoints

### Desktop

**Screen width: 1025px and above**

The desktop layout displays:

- Logo
- Navigation links
- Username button
- Hero text
- Call-to-action button
- Laundry image

The navigation links are displayed horizontally.

The hamburger menu is hidden on desktop.

---

### Tablet

**Screen width: 601px to 1024px**

The normal navigation links are hidden.

A hamburger menu is displayed instead.

When the hamburger button receives focus, the menu opens.

The hamburger menu:

- Has a black background
- Has white text
- Has centered navigation links
- Covers the full height of the screen
- Occupies 50% of the screen width
- Is positioned on the right side of the screen

The hero section changes to a vertical layout using:

```css
flex-direction: column;

Mobile

Screen width: 381px to 600px

The normal navigation links are hidden.

The hamburger menu is displayed.

The hamburger menu:

Has a black background
Has white text
Has centered navigation links
Covers the full height of the screen
Occupies 50% of the screen width
Opens from the right side

The hero section is displayed vertically.

Font sizes and image sizes are reduced to fit the smaller screen.

Extra Small Mobile

Screen width: 380px and below

The normal navigation links are hidden.

The hamburger menu is displayed.

The hamburger menu:

Has a black background
Has white text
Has centered navigation links
Covers the full height of the screen
Occupies 50% of the screen width
Opens from the right side

The font sizes, button sizes and image sizes are further reduced for smaller devices.

Hamburger Menu

The hamburger icon is created using a CSS pseudo-element:
.menu-button::before {
    content: "☰";
}

Hamburger Menu

The hamburger icon is created using a CSS pseudo-element:

.menu-button::before {
    content: "☰";
}

The menu is initially hidden:

.menu-list {
    display: none;
}

The menu is displayed when the hamburger button receives focus:

.menu-button:focus + .menu-list {
    display: block;
}

Therefore, JavaScript is not required to open the menu.

Hamburger Menu Styling

The menu uses:

position: fixed;
top: 0;
right: 0;
width: 50vw;
height: 100vh;

This makes the menu:

Fixed to the right side
Half the width of the viewport
Full screen height

The menu background and text are:

background-color: black;
color: white;

The navigation text is centered using:

text-align: center;
CSS Variables

The project uses CSS variables for commonly used values:

:root {
    --primary-color: #09a9f5;
    --dark-text: #4f5f6d;
    --light-text: #8d9aa5;
    --button-radius: 10px;
    --page-width: 1100px;
}

These variables make the CSS easier to maintain and modify.

Project Structure
Task8/
│
├── index.html
├── style.css
├── Readme.md
│
└── images/
    └── laundry.png
How to Run
Open the project folder.
Make sure index.html and style.css are present.
Make sure the laundry image is inside the images folder.
Open index.html in a web browser.
Resize the browser window to test the different responsive layouts.

Responsive Testing

Test the webpage at the following screen widths:

Device	Screen Width
Desktop	1025px and above
Tablet	601px - 1024px
Mobile	381px - 600px
Extra Small Mobile	380px and below

On tablet, mobile and extra small mobile:

Click or focus on the hamburger icon.
The navigation menu should appear.
The menu should occupy 50% of the screen width.
The menu should cover the complete screen height.
The menu background should be black.
The navigation text should be white and centered.
Important Notes
The project uses CSS only for responsive behavior.
No Bootstrap is used.
No JavaScript is used for the hamburger menu.
CSS media queries are used to create different layouts for different screen sizes.
CSS :focus is used to display the hamburger menu.
CSS ::before is used to create the hamburger icon.