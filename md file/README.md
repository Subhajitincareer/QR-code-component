### Documentation for QR Code Component

This documentation provides an overview of the QR code component, its structure, and the styling applied using HTML and CSS.

---

### **1. Project Overview**

The QR code component is designed as a simple yet visually appealing card displaying a QR code along with a heading and description. The component is fully responsive and adjusts itself for both mobile and desktop screens.

---

### **2. Project Structure**

The project consists of two main files:

1. **HTML File** (`index.html`): Contains the structure of the QR code component.
2. **CSS File** (`style.css`): Contains all the styling for the component.

---

### **3. HTML Structure**

The HTML file defines the structure of the QR code component, which consists of:

#### **a. Container for the QR Code**
The `div` with class `.container` contains the QR code image and accompanying text.

```html
<div class="container">
    <img src="image-qr-code.png" alt="">
    <div>
        <p class="bold-font">Improve your front-end skills by building projects</p>
        <p class="paragraph">Scan the QR code to visit Frontend Mentor and take your coding skills to the next level</p>
    </div>
</div>
```

- **`<img src="image-qr-code.png" alt="">`**: The QR code image displayed in the component.
- **`<p class="bold-font">`**: The heading text styled as bold.
- **`<p class="paragraph">`**: The paragraph with a brief description.

#### **b. Attribution Section**
The attribution section is placed at the bottom of the page.

```html
<div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
    Coded by <a href="#">Subhajit pal</a>.
</div>
```

- **`<a href="#">Subhajit pal</a>`**: Links to the coder’s profile or a placeholder for the coder’s name.
- **`<a href="https://www.frontendmentor.io?ref=challenge"`**: Links to Frontend Mentor's website for challenge details.

---

### **4. CSS Styling**

#### **a. Variables**
The `:root` selector defines a set of CSS variables to make color and font customization easier.

```css
:root {
    --white-color: hsl(0, 0%, 100%);
    --slate-300: hsl(212, 45%, 89%);
    --Slate-500: hsl(216, 15%, 48%);
    --Slate-900: hsl(218, 44%, 22%);
    --Mobile: 375px;
    --Desktop: 1440px;
    --Font-size-p: 15px;
    --font-bold-size: 1.25rem;
    --Weights-font: 400;
    --Weights-font2: 700;
    --font-family: "Outfit";
}
```

These variables allow for consistent color and font usage across the project.

#### **b. Body Styling**
The `body` tag is styled to center the QR code component both vertically and horizontally using Flexbox.

```css
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    font-family: var(--font-family);
    background-color: var(--slate-300);
    color: var(--Slate-900);
    padding: 20px;
}
```

#### **c. Container Styling**
The `.container` is the main section of the card, where the QR code image and text are displayed.

```css
.container {
    width: 100%;
    max-width: 320px;
    padding: 20px;
    background-color: var(--white-color);
    border-radius: 15px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    text-align: center;
}
```

- **Max width** ensures it does not stretch too wide on large screens.
- **Box shadow** gives the card a subtle elevation effect.

#### **d. Image Styling**
The `img` tag is styled to maintain a responsive layout with a rounded border.

```css
img {
    width: 100%;
    height: auto;
    border-radius: 10px;
    margin-bottom: 20px;
}
```

#### **e. Typography Styling**
The typography for the heading and paragraph is styled as follows:

```css
.bold-font {
    font-size: var(--font-bold-size);
    font-weight: bold;
    color: var(--Slate-900);
    margin-bottom: 10px;
}

.paragraph {
    font-size: var(--Font-size-p);
    color: var(--Slate-500);
    line-height: 1.6;
}
```

- **Heading** (`.bold-font`): Styled with a larger font size and bold weight.
- **Paragraph** (`.paragraph`): Styled with a smaller font size for easy reading.

#### **f. Attribution Section Styling**
The attribution section is styled with a smaller font size, placed below the main component.

```css
.attribution {
    font-size: 12px;
    text-align: center;
    color: var(--Slate-500);
    margin-top: 20px;
}

.attribution a {
    color: var(--Slate-500);
    text-decoration: none;
}

.attribution a:hover {
    text-decoration: underline;
}
```

---

### **5. Media Queries (Responsiveness)**

The project includes two media queries for responsiveness:

1. **For screens smaller than 768px (Mobile):**
   - The `.container` is centered with padding, and the image adjusts its width and height.
   - Text is centered with adjusted margins.

```css
@media (max-width: 768px) {
    .container {
        width: 62%;
        height: 50%;
        border-radius: 10px;
        background-color: var(--white-color);
        position: relative;
        left: 20%;
        top: 40px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    img {
        width: 92%;
        height: 92%;
        border-radius: 10px;
        margin: 10px 5% 0 5%;
    }
}
```

2. **For screens larger than 768px (Desktop):**
   - The layout uses a grid with specific column and row settings to place the component centrally.
   - The `.container` has increased width and padding for larger screens.

```css
@media (min-width: 768px) {
    body {
        display: grid;
        grid-template-columns: 39% 22% 39%;
        grid-template-rows: repeat(3, 1fr);
        width: 100%;
        height: 100vh;
        align-items: center;
        justify-items: center;
    }

    .container {
        grid-column: 2/3;
        grid-row: 2/3;
        width: 100%;
        max-width: 400px;
        height: auto;
        padding: 20px;
        border-radius: 10px;
        background-color: var(--white-color);
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
    }
}
```

---

### **6. Conclusion**

This QR code component is designed to be responsive and visually appealing. The use of CSS variables allows for easy customization of colors and fonts. The media queries ensure the component looks good on both mobile and desktop devices.