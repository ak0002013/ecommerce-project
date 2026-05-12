# Ecommerce Project

A modern, full-stack ecommerce application built with React and Express.js. This project demonstrates a complete shopping experience with product browsing, cart management, checkout, and order tracking.

## Features

- 🛍️ **Product Browsing** - Browse and explore products with detailed information
- 🛒 **Shopping Cart** - Add/remove items, manage quantities with persistent state
- 💳 **Checkout** - Multi-step checkout process with delivery options and payment summary
- 📦 **Order Tracking** - View order history and track order details
- 🔄 **Real-time Sync** - Cart synchronizes with backend in real-time using API calls
- 📱 **Responsive Design** - Works seamlessly across desktop and mobile devices

## Tech Stack

### Frontend (This Project)
- **React 19** - UI framework
- **Vite** - Fast build tool and dev server
- **React Router 7** - Client-side routing
- **Axios** - HTTP client for API requests
- **Day.js** - Date manipulation and formatting
- **CSS** - Styling

### Backend
- **Express.js** - Web server framework
- **Sequelize** - ORM for database operations
- **Node.js** - JavaScript runtime

## Installation

### Prerequisites
- Node.js (version 18+)
- npm or yarn

### Setup

1. **Clone or download the repository**
   ```bash
   git clone <repository-url>
   cd react-course
   ```

2. **Install frontend dependencies**
   ```bash
   cd ecommerce-project
   npm install
   ```

3. **Install backend dependencies** (in a separate terminal)
   ```bash
   cd ecommerce-backend
   npm install
   ```

## Getting Started

### Run the Backend Server
```bash
cd ecommerce-backend
npm run dev
```
The backend will start on `http://localhost:3000` (or your configured port)

### Run the Frontend Development Server
```bash
cd ecommerce-project
npm run dev
```
The frontend will start on `http://localhost:5173` (or the next available port)

Visit `http://localhost:5173` in your browser to access the application.

## Project Structure

```
ecommerce-project/
├── src/
│   ├── components/          # Reusable UI components
│   │   └── header.jsx       # Navigation header
│   ├── pages/               # Page components
│   │   ├── home/            # Home/products page
│   │   ├── checkout/        # Checkout flow page
│   │   └── orders/          # Order history page
│   ├── utils/               # Utility functions
│   │   └── money.js         # Currency formatting
│   ├── App.jsx              # Main application component
│   ├── App.css              # Global styles
│   └── main.jsx             # Application entry point
├── public/                  # Static assets (images, icons)
├── package.json             # Dependencies and scripts
└── vite.config.js           # Vite configuration

ecommerce-backend/
├── models/                  # Database models
├── routes/                  # API endpoints
├── backend/                 # Data storage (JSON files)
├── defaultData/             # Default data for models
├── server.js                # Express server setup
└── package.json             # Dependencies and scripts
```

## Available Scripts

### Frontend
- `npm run dev` - Start development server with hot module replacement
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint to check code quality

### Backend
- `npm run dev` - Start backend with nodemon (auto-restart on changes)
- `npm start` - Start backend server
- `npm run zip` - Create a zip file of the project

## API Endpoints

The frontend communicates with the backend via REST API:

- `GET /api/products` - Fetch all products
- `GET /api/cart-items` - Fetch cart items
- `POST /api/cart-items` - Add item to cart
- `DELETE /api/cart-items/:id` - Remove item from cart
- `GET /api/delivery-options` - Fetch delivery options
- `GET /api/orders` - Fetch user orders
- `POST /api/orders` - Create new order

## Usage

### Home Page
- Browse all available products
- Click "Add to Cart" to add items to your shopping cart
- See total cart count in the header

### Checkout Page
- Review items in your cart
- Choose a delivery option
- View order summary with costs
- Proceed to payment

### Orders Page
- View all your orders
- See order details including items and delivery information
- Track order status

## Development Tips

- Use the browser DevTools to inspect network requests to the backend
- Check the Console for any errors or API-related issues
- The cart state is managed in the App component and passed down via props
- Each page is a separate route component

## Troubleshooting

- **Backend not connecting?** Ensure the backend server is running on the correct port
- **Port already in use?** Check for other processes using the same port
- **CORS errors?** Ensure the backend CORS configuration allows frontend origin
- **Page not loading?** Check browser console for errors and network tab for failed requests

For more backend-specific issues, see the [Backend README](../ecommerce-backend/README.md).

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Future Enhancements

- User authentication and profiles
- Payment gateway integration
- Product search and filters
- Product reviews and ratings
- Wishlist functionality
- Admin dashboard
