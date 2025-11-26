# NavigationPage – React Router Navigation Project

A modern and clean navigation page built using **React**, **React Router DOM**, and organized folder structure. This README guides you step‑by‑step from project setup to running the final application.

---

## **1. Create the React App Project**

Open your terminal and run:

```sh
npx create-react-app NavigationPage
```

---

## **2. Go Inside the Project Folder**

```sh
cd NavigationPage
```

---

## **3. Install React Router DOM**

```sh
npm install react-router-dom
```

---

## **4. Open the Project in VS Code**

```sh
code .
```

---

## **5. Create Project Folders Inside `src/`**

Create the following folders:

```
src/
 ├── components/
 └── pages/
```

---

## **6. Create Required Files**

Inside **components** folder:

```
Navbar.jsx
```

Inside **pages** folder:

```
Home.jsx
Products.jsx
Contact.jsx
```

---

## **7. Add Code to Files**

### **`src/components/Navbar.jsx`**

```jsx
import React from "react";
import { Link } from "react-router-dom";

export default function Navbar() {
  return (
    <nav className="navbar">
      <div className="logo">ShopX</div>
      <ul>
        <li><Link to="/">Home</Link></li>
        <li><Link to="/products">Products</Link></li>
        <li><Link to="/contact">Contact</Link></li>
      </ul>
    </nav>
  );
}
```

---

### **`src/pages/Home.jsx`**

```jsx
import React from "react";

export default function Home() {
  return (
    <div className="page">
      <h1>Welcome to ShopX</h1>
      <p>Discover the latest gadgets in style.</p>
    </div>
  );
}
```

---

### **`src/pages/Products.jsx`**

```jsx
import React from "react";

export default function Products() {
  return (
    <div className="page">
      <h1>Our Products</h1>
      <p>High-quality tech items for modern users.</p>
    </div>
  );
}
```

---

### **`src/pages/Contact.jsx`**

```jsx
import React from "react";

export default function Contact() {
  return (
    <div className="page">
      <h1>Contact Us</h1>
      <p>Email: info@shopX.com</p>
    </div>
  );
}
```

---

## **8. Update `src/App.js`**

```jsx
import React from "react";
import { BrowserRouter as Router, Routes, Route } from "react-router-dom";
import Navbar from "./components/Navbar";
import Home from "./pages/Home";
import Products from "./pages/Products";
import Contact from "./pages/Contact";
import "./App.css";

export default function App() {
  return (
    <Router>
      <Navbar />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/products" element={<Products />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
}
```

---

## **9. Add Styling (`src/index.css`)**

```css
body {
  margin: 0;
  font-family: "Poppins", sans-serif;
  background-color: #000;
  color: #fff;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 40px;
  background: #111;
  position: sticky;
  top: 0;
  z-index: 10;
}

.navbar .logo {
  font-size: 24px;
  font-weight: bold;
  color: #fff;
}

.navbar ul {
  list-style: none;
  display: flex;
  gap: 20px;
  margin: 0;
}

.navbar a {
  text-decoration: none;
  color: #fff;
  font-weight: 500;
  transition: 0.3s;
}

.navbar a:hover {
  color: #888;
}

.page {
  padding: 100px 20px;
  text-align: center;
}

.page h1 {
  font-size: 36px;
  margin-bottom: 20px;
}

.page p {
  font-size: 18px;
  color: #ccc;
}
```

---

## **10. Run the Project**

```sh
npm start
```

Your app will open at:

```
http://localhost:3000
```

---

## 🎉 **Your Navigation Page is Ready!**