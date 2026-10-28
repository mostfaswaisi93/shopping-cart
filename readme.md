# Shopping Cart with Stripe

An online store built with **Laravel 7**: browse products, manage a session-based shopping cart, pay with **Stripe**, and review past orders. Store content is managed through a **Voyager** admin panel.

![Laravel](https://img.shields.io/badge/Laravel-7-FF2D20?logo=laravel&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?logo=stripe&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-7.2%2B-777BB4?logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?logo=bootstrap&logoColor=white)

## Features

- Product store page
- **Session-based cart**: add products, update quantities, remove items, with running total quantity and price
- **Checkout with Stripe** (`cartalyst/stripe-laravel`) for logged-in users
- Orders saved after a successful payment, with an **order history** page
- **Voyager** admin panel under `/admin` for products, users, pages, posts and categories
- SweetAlert messages for user feedback
- Database seeders for Voyager and sample data

## Routes

| Route | Description |
|---|---|
| `/store` | Product catalogue |
| `/addToCart/{product}` | Add a product to the cart |
| `/shopping-cart` | View and edit the cart |
| `/checkout/{amount}` | Payment page (auth) |
| `POST /charge` | Charge the card with Stripe |
| `/orders` | Order history |
| `/admin` | Voyager admin panel |

## Getting Started

**Prerequisites:** PHP 7.2.5+, Composer, Node.js, MySQL, a Stripe test account

```bash
git clone https://github.com/mostfaswaisi93/shopping-cart.git
cd shopping-cart
composer install
npm install && npm run dev

cp .env.example .env
php artisan key:generate
# set DB_* values and STRIPE_KEY / STRIPE_SECRET (test keys) in .env
php artisan migrate --seed
php artisan storage:link
php artisan serve      # http://localhost:8000
```

Use Stripe's test card `4242 4242 4242 4242` with any future date and CVC.

## Author

**Mustafa T. Al-Swaisi** · [LinkedIn](https://www.linkedin.com/in/mostfaswaisi93/) · [GitHub](https://github.com/mostfaswaisi93)
