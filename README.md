# Meal Buddy - Food Delivery Application

A full-stack Django-based food delivery application that connects customers with restaurants. Built with Django, Tailwind CSS, and integrated with Razorpay for payment processing.

## Features

- **User Authentication**: Sign up and sign in functionality for customers and admins
- **Restaurant Management**: Add, update, and manage restaurant details
- **Menu Management**: Add and update menu items for restaurants
- **Shopping Cart**: Add items to cart and manage quantities
- **Checkout**: Secure checkout process with order summary
- **Payment Integration**: Razorpay payment gateway integration
- **Order Tracking**: View order history and status
- **Admin Dashboard**: Manage restaurants and menu items
- **Responsive Design**: Beautiful UI with Tailwind CSS

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/meal-buddy.git
cd meal-buddy
```

### 2. Create Virtual Environment
```bash
# On Windows
python -m venv myenv
myenv\Scripts\activate

# On macOS/Linux
python3 -m venv myenv
source myenv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Database Setup
```bash
python manage.py migrate
```

### 5. Create Superuser (Admin Account)
```bash
python manage.py createsuperuser
```

### 6. Run Development Server
```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`

## Project Structure

```
meal-buddy/
├── delivery/               # Main Django app
│   ├── models.py          # Database models
│   ├── views.py           # View logic
│   ├── urls.py            # URL routing
│   ├── admin.py           # Django admin configuration
│   ├── templates/         # HTML templates
│   │   └── delivery/
│   │       ├── index.html
│   │       ├── signin.html
│   │       ├── signup.html
│   │       ├── customer_home.html
│   │       ├── customer_menu.html
│   │       ├── cart.html
│   │       ├── checkout.html
│   │       ├── orders.html
│   │       ├── admin_home.html
│   │       ├── add_restaurant.html
│   │       ├── update_restaurant.html
│   │       ├── update_menu.html
│   │       ├── show_restaurants.html
│   │       ├── success.html
│   │       └── fail.html
│   └── migrations/        # Database migrations
├── meal_buddy/            # Django project settings
│   ├── settings.py        # Project settings
│   ├── urls.py            # Main URL configuration
│   ├── wsgi.py            # WSGI configuration
│   └── asgi.py            # ASGI configuration
├── myenv/                 # Virtual environment
├── manage.py              # Django management script
├── db.sqlite3             # SQLite database
├── requirements.txt       # Project dependencies
└── README.md              # This file
```

## Dependencies

- **Django** (5.2.6) - Web framework
- **django-tailwind** (4.2.0) - Tailwind CSS integration
- **razorpay** (2.0.0) - Payment gateway
- **requests** (2.32.5) - HTTP library
- **sqlparse** (0.5.3) - SQL parser
- And other supporting libraries

See `requirements.txt` for complete list.

## Usage

### For Customers
1. Visit the homepage
2. Sign up or sign in
3. Browse restaurants
4. Select a restaurant and view menu
5. Add items to cart
6. Proceed to checkout
7. Complete payment
8. View order status

### For Admins
1. Log in to admin dashboard
2. Add or manage restaurants
3. Update restaurant details
4. Manage menu items
5. View and process orders

## Environment Variables

Create a `.env` file in the project root for sensitive configuration:
```
SECRET_KEY=your_django_secret_key
DEBUG=False
RAZORPAY_KEY_ID=your_razorpay_key
RAZORPAY_KEY_SECRET=your_razorpay_secret
```

## API Integration

### Razorpay Payment Gateway
- Payment processing for orders
- Webhook support for payment confirmation
- PCI-DSS compliant

## Database Models

### Restaurant
- Name, location, contact information
- Operating hours

### Item (Menu Item)
- Name, description, price
- Vegetarian/Non-vegetarian category
- Associated restaurant

### Cart
- User/session tracking
- Items and quantities
- Order total calculation

### Orders
- Order details and history
- Payment status
- Delivery status

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For issues and questions, please open an issue on GitHub.

## Author

Meal Buddy Development Team

---

**Happy coding! 🚀**
