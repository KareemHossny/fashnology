# Fashnology – FullStack E-commerce Platform

![React](https://img.shields.io/badge/Frontend-React_19-blue)
![Express](https://img.shields.io/badge/Backend-Express_5-yellow)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-green)
![Vercel](https://img.shields.io/badge/Deployment-Vercel-black)
![Stripe](https://img.shields.io/badge/Payment-Stripe-purple)
![Production](https://img.shields.io/badge/Status-Production-green)

**Fashnology** is a **production-ready full-stack MERN e-commerce platform** providing a **customer storefront**, **admin dashboard**, and a **Node.js/Express backend** with JWT authentication and Stripe checkout.  
It delivers a complete shopping workflow: product discovery → cart → checkout → order tracking.

---

## 🚀 Live Demo

- **Storefront:** [https://frontende-commerce.vercel.app](https://frontende-commerce.vercel.app)  
- **Admin Panel:** [https://admin-e-commerce-peach.vercel.app](https://admin-e-commerce-peach.vercel.app)  
- **Backend API:** [https://backende-commerce-kappa.vercel.app](https://backende-commerce-kappa.vercel.app)

> Fully functional: Users can browse products, manage cart, checkout via Stripe or COD, while admin manages products and orders.

---
## 🧠 Architecture

```
User
  ↓
Frontend (React CRA + Tailwind + Context API)
  ↓
Backend (Node.js + Express + MongoDB)
  ↓
Stripe Payment API
```

- Frontend: React 19 (CRA), Tailwind, React Router, Axios, React Toastify  
- Admin: React 19 (CRA), Tailwind, Axios  
- Backend: Node.js, Express 5, MongoDB via Mongoose, JWT Auth, Multer + Cloudinary, Stripe SDK  
- Deployment: Vercel (Frontend + Admin + Backend)  

---

## ✨ Core Features (Fully Working)

### 🛒 Storefront

- Product listing and detailed pages  
- Category/subcategory filtering, search, and price sorting  
- Bestsellers and latest arrivals  
- Related products display  

### 🛍 Cart

- Add/update/remove items with size-awareness  
- LocalStorage persistence  
- Local-to-backend cart sync on login  

### 💳 Checkout & Orders

- Delivery form and order summary  
- Cash on Delivery  
- Stripe checkout session + payment verification  
- User order history  

### 👨‍💻 Admin Dashboard

- Dashboard metrics: products, orders, revenue  
- Create/edit/delete products (up to 4 images)  
- Update order status workflow  
- View all orders  

### 🔐 Authentication & Security

- JWT-based session  
- Role-based access control (user vs admin)  
- Password hashing with bcrypt  
- Protected routes for user actions and admin operations  
- Basic input validation  

---

## 📡 API Documentation

### User
| Endpoint | Description |
|----------|-------------|
| POST /api/user/register | Register new customer |
| POST /api/user/login | Customer login |
| POST /api/user/admin | Admin login |

### Product
| Endpoint | Description |
|----------|-------------|
| POST /api/product/create | Create product (admin) |
| GET /api/product/all | Get all products |
| GET /api/product/:id | Get product by ID |
| PUT /api/product/:id | Update product (admin) |
| DELETE /api/product/:id | Delete product (admin) |
| GET /api/product/category/:category | Products by category |
| GET /api/product/bestsellers/all | Bestseller products |

### Cart
| Endpoint | Description |
|----------|-------------|
| POST /api/cart/add | Add item to cart |
| POST /api/cart/update | Update item quantity |
| POST /api/cart/get | Get current cart |
| POST /api/cart/removefromcart | Remove item |
| POST /api/cart/removeall | Clear cart |

### Order
| Endpoint | Description |
|----------|-------------|
| POST /api/order/place | Place COD order |
| POST /api/order/stripe | Create Stripe checkout order |
| POST /api/order/verifystripe | Verify Stripe payment |
| POST /api/order/userorders | Get user orders |
| GET /api/order/all | Get all orders (admin) |
| PUT /api/order/status | Update order status (admin) |

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repositories

```bash
git clone https://github.com/KareemHossny/fashnology/tree/main/frontend
git clone https://github.com/KareemHossny/fashnology/tree/main/backend
git clone https://github.com/KareemHossny/fashnology/tree/main/admin
```

### 2️⃣ Backend Setup

```bash
cd backend
npm install
```

**.env**
```
PORT=5777
NODE_ENV=development
JWT_SECRET=your_jwt_secret
ADMIN_EMAIL=admin@example.com
ADMIN_PASSWORD=your_admin_password
MONGO_URI=your_mongodb_connection_string
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_key
CLOUDINARY_API_SECRET=your_cloudinary_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
```

```bash
npm run server
```

### 3️⃣ Frontend Setup

```bash
cd frontend
npm install
npm start
```

### 4️⃣ Admin Setup

```bash
cd admin
npm install
npm start
```

### Production Build

```bash
cd frontend
npm run build
cd ../admin
npm run build
cd ../backend
npm start
```

---

## 📈 Performance Optimizations

- Cart persisted in localStorage  
- Backend cart normalization prevents data loss  
- Client-side filtering/sorting for fast rendering  
- Multer memory storage for serverless deployment  
- Lean API responses and minimal payloads  

---

## 🧪 Future Improvements

- Move hardcoded API URLs to environment variables  
- Add route guards consistently for admin endpoints  
- Automated tests (unit/integration/e2e)  
- Pagination for products/orders  
- Improved logging and production cleanup  
- Refresh-token strategy + token expiration handling  
- Complete Stripe/Razorpay integration  

---

## 👨‍💻 Author

**Kareem Hossny** – Full Stack MERN Developer  
Open to freelance & junior full-stack opportunities
