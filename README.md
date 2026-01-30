# 🛍️ ShopShakti – Full‑Stack E‑Commerce Platform



📌 **Status:** Active Development — Stable Core Features

ShopShakti is a modern, full‑stack, responsive **e‑commerce web application** built using **Angular** (frontend) and **ASP.NET Core Web API** (backend). The project focuses on **clean architecture, scalability, performance, and secure user experience**.

---

## 📽️ Project Demo

🎥 **YouTube Walkthrough:**
🔗 [https://youtu.be/rlYTUn8ONFk?si=KnZtb-_hHt2Op6vs](https://youtu.be/rlYTUn8ONFk?si=KnZtb-_hHt2Op6vs)

🚧 *Note: This project is actively evolving, but core features and flows are stable and production‑ready.*

---

## 🚀 Frontend (Angular)

### ✨ Key Features

* 🏠 Homepage with hero banners, trending products, deals & featured categories
* 🛒 Product listing & product detail pages with filtering & dynamic routing
* 👤 Authentication: Register, Login & Profile Management
* 🧺 Cart system with quantity control & persistence
* 💳 Checkout flow with order summary & confirmation
* 📦 Order management for users & admin
* 🧑‍💼 Admin dashboard with analytics & protected routes
* 🍞 Toast notifications for real‑time feedback
* 📱 Fully responsive (desktop, tablet & mobile)

---

### 🧱 Frontend Folder Structure

```
ShopShakti_frontend/
└── src/
    ├── app/
    │   ├── components/
    │   │   ├── admin/
    │   │   ├── auth_user_pages/
    │   │   ├── core_pages/
    │   │   ├── orders/
    │   │   ├── staff/
    │   │   ├── home/
    │   │   └── ui_ux/
    │   ├── models/
    │   └── services/
    ├── assets/
    │   └── images/
    └── index.html
```

---

### 🛠️ Frontend Tech Stack

* Angular 19 (Standalone Components)
* TypeScript
* Angular Router & Route Guards
* Material Icons & FontAwesome

---

### 🔒 Admin Access Logic

Admin routes are protected using route guards:

```ts
if (auth.isLoggedIn() && auth.isAdmin()) {
  return true;
}
```

---

### ▶️ Run Frontend Locally

```bash
npm install
ng serve
```

🌐 App URL: [http://localhost:4200](http://localhost:4200)

---

## 🔧 Backend (ASP.NET Core Web API)

### 🧱 Backend Structure

```
ShopShakti_backend/
├── Controllers/
├── Data/
├── Models/
├── Migrations/
├── Program.cs
├── appsettings.json
└── ShopShakti_backend.csproj
```

---

### 🧰 Backend Tech Stack

* ASP.NET Core 7 Web API
* Entity Framework Core
* SQL Server / SQLite
* JWT Authentication
* Swagger (OpenAPI 3.0)
* CORS Configuration

---

## 📘 API Endpoints

### 🛒 CartItems

* GET /api/CartItems
* GET /api/CartItems/{id}
* POST /api/CartItems
* PUT /api/CartItems/{id}
* DELETE /api/CartItems/{id}

### 📦 Orders

* GET /api/Orders
* GET /api/Orders/{id}
* POST /api/Orders
* PUT /api/Orders/{id}
* DELETE /api/Orders/{id}

### 🛍️ Products

* GET /api/Products
* GET /api/Products/{id}
* POST /api/Products
* PUT /api/Products/{id}
* DELETE /api/Products/{id}

### 👤 Users

* GET /api/Users
* GET /api/Users/{id}
* POST /api/Users
* PUT /api/Users/{id}
* DELETE /api/Users/{id}
* POST /api/Users/login

### 📊 Admin Metrics

* GET /api/Admin/metrics

---

## 🔐 Security Architecture

### ✅ Authentication & Authorization

* JWT‑based authentication (Issuer, Audience, HMAC SHA256)
* Token expiration & validation (ClockSkew = 0)
* Role‑based access control (Admin / User)
* Password hashing using `PasswordHasher<T>`

### ✅ API Security

* `[Authorize]` & `[AllowAnonymous]`
* Restricted CORS policy
* Blocked user detection with 403 response

### ✅ Frontend Security

* JWT HTTP Interceptor
* Secure token storage (no passwords stored client‑side)
* Route guards for protected pages

✔ All critical flows (login, logout, admin access, token validation) are securely implemented.

---

## 🧪 Run Backend Locally

```bash
cd ShopShakti_backend
dotnet restore
dotnet ef database update
dotnet run
```

🔗 API Base URL: [https://localhost:7171/api](https://localhost:7171/api)
📘 Swagger UI: [https://localhost:7171/swagger](https://localhost:7171/swagger)

---

## 🚀 Future Enhancements

* Wishlist & payment gateway integration
* Advanced search, filters & pagination
* Product ratings & reviews
* Order tracking & invoice downloads

---

## 🤝 Contribution

Contributions are welcome!
Fork the repository and submit a PR with meaningful commit messages.

---

## 📄 License

Licensed under the **MIT License**.
You are free to use, modify, and distribute this project with attribution.

---

## 👨‍💻 Developer Note

This project is crafted with a strong focus on **clean architecture, intuitive UI/UX, and scalability**, following modern full‑stack development best practices.

---

## 🧑‍🎓 Developed & Maintained By


© 2025 Chetan Patil. All rights reserved.

⚠️ Please do not reproduce without proper attribution.
