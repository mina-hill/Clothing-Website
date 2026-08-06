# 🧥 RAVEN ATTIRE — Clothing Store Website

*"Where style meets innovation."*

A static, no-JavaScript, no-backend website for a gothic/vintage-inspired clothing store — product pages, per-item cart pages, a checkout flow, and a payment form, all built with plain **HTML5** and **CSS3**.

**🌐 Live demo: [mina-hill.github.io/Clothing-Website](https://mina-hill.github.io/Clothing-Website/index.html)**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![Static Site](https://img.shields.io/badge/Static%20Site-No%20Backend-81613B?style=flat)
![No JavaScript](https://img.shields.io/badge/JavaScript-None-lightgrey?style=flat)
![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-222?style=flat&logo=github&logoColor=white)

---

## 📊 Project at a Glance

The site is 16 static HTML pages in total: 5 product pages, 6 cart pages (one combined view + one per product), a checkout/payment pair, the category/home pages, and a login screen.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/charts/pages-by-type-dark.png">
  <img src="docs/charts/pages-by-type.png" alt="Bar chart of RAVEN ATTIRE pages by type: 6 cart pages, 5 product pages, 2 checkout/payment pages, 2 category/home pages, 1 login page" width="600">
</picture>

---

## 🖼️ Gallery

Real product photography used across the category and product pages:

<table>
  <tr>
    <td align="center"><img src="clothes/p1.png" width="140"><br><sub>Cozy Sweater</sub></td>
    <td align="center"><img src="clothes/p2.png" width="140"><br><sub>Raven-Hued Trousers</sub></td>
    <td align="center"><img src="clothes/p3.png" width="140"><br><sub>Scholarly Corduroys</sub></td>
    <td align="center"><img src="clothes/p4.png" width="140"><br><sub>Autumny Sweater</sub></td>
    <td align="center"><img src="clothes/p5.png" width="140"><br><sub>Mystic Frock</sub></td>
  </tr>
</table>

> Live screenshots of the deployed site weren't captured in this pass (browser preview tooling was unavailable) — the images above are the site's actual product photos from `clothes/`, not placeholders. You can browse the live pages directly at the [demo link](https://mina-hill.github.io/Clothing-Website/index.html) above.

---

## 🧭 Site Flow

Navigation is consistent across every page (Home / Categories / Payment / Login / Shopping Cart in the header). The real user journey through the pages looks like this:

```mermaid
flowchart LR
    Home["🏠 index.html<br/>Home"]:::a --> Categories["📂 categories.html<br/>Categories"]:::a
    Categories --> P1["products/p1.html<br/>Cozy Sweater"]:::b
    Categories --> P2["products/p2.html<br/>Raven-Hued Trousers"]:::b
    Categories --> P3["products/p3.html<br/>Scholarly Corduroys"]:::b
    Categories --> P4["products/p4.html<br/>Autumny Sweater"]:::b
    Categories --> P5["products/p5.html<br/>Mystic Frock"]:::b

    P1 --> Cart1["cart1.html"]:::c
    P2 --> Cart2["cart2.html"]:::c
    P3 --> Cart3["cart3.html"]:::c
    P4 --> Cart4["cart4.html"]:::c
    P5 --> Cart5["cart5.html"]:::c
    Categories -.->|"Add To Cart"| Cart["cart.html<br/>Combined Cart"]:::c

    Cart1 --> Cart
    Cart2 --> Cart
    Cart3 --> Cart
    Cart4 --> Cart
    Cart5 --> Cart

    Cart --> Checkout["checkout.html"]:::d
    Checkout --> Payment["payment.html"]:::d

    Home --> Login["login.html<br/>Login / SignUp"]:::e

    classDef a fill:#4C72B0,stroke:#2E4670,stroke-width:2px,color:#ffffff
    classDef b fill:#DD8452,stroke:#854F31,stroke-width:2px,color:#ffffff
    classDef c fill:#4C9F8A,stroke:#2F6455,stroke-width:2px,color:#ffffff
    classDef d fill:#C9A227,stroke:#7A6418,stroke-width:2px,color:#ffffff
    classDef e fill:#8172B2,stroke:#574F7A,stroke-width:2px,color:#ffffff
```

- 🔵 **Browsing** — Home and Categories, the entry points into the catalog
- 🟠 **Product pages** — one static page per item, each showing related products
- 🟢 **Cart pages** — a dedicated cart page per product plus a combined cart view
- 🟡 **Checkout / Payment** — the two-step purchase flow
- 🟣 **Auth** — the login/sign-up screen, linked from the header on every page

---

## 📁 Project Structure

```
.
├── index.html               # Homepage
├── categories.html          # Lists clothing categories
├── login.html                # Login / sign-up page
├── cart.html                 # Combined cart view
├── cart1.html - cart5.html   # Cart pages for individual products
├── checkout.html              # Checkout interface
├── payment.html                # Payment interface
├── style.css                    # Main CSS file (theme accent: #81613b)
├── logo.png                      # Store logo
├── favicon.ico                    # Favicon
├── clothes/                        # Product photos, p1.png - p5.png
├── products/                        # Product detail pages, p1.html - p5.html
└── docs/charts/                      # README chart assets
```

---

## ✨ Features

- Clean homepage hero and "Why Choose Us" section
- Category page listing all 5 products with pricing
- 5 individual product pages (`products/p1.html`–`p5.html`) with size selectors and related-product suggestions
- Per-product cart pages (`cart1.html`–`cart5.html`) plus a combined cart (`cart.html`)
- Checkout and payment UI with a styled form
- Login/sign-up screen
- Consistent gothic/vintage styling driven by a single warm brown accent color (`#81613b`) across headers, buttons, cards, and the footer
- Fully responsive layout with breakpoints at 1400px, 1220px, 900px, 768px, and 570px

---

## 🚀 How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/mina-hill/Clothing-Website.git
   cd Clothing-Website
   ```

2. Open `index.html` in your browser:
   - Double-click it, or
   - Right-click → *Open with* → your preferred browser

No build step, package manager, or server is required.

---

## 🛠️ Built With

- HTML5
- CSS3

> No frameworks, JavaScript, or backend logic included — every page here is plain markup and CSS.
