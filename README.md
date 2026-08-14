# Kasir Online (POS System)

A modern, high-performance web-based Cashier/POS (Point of Sale) system built with **Laravel**, **Filament PHP**, and **React (TypeScript) with Inertia.js**.

## 🚀 Tech Stack

- **Backend Framework:** [Laravel 11](https://laravel.com)
- **Admin Panel & Resource Management:** [Filament PHP v3](https://filamentphp.com) (Livewire-powered)
- **Frontend Framework:** [React](https://react.dev) (TypeScript) via [Inertia.js](https://inertiajs.com)
- **Styling:** Tailwind CSS & Shadcn UI
- **Database:** MySQL / MariaDB

---

## ✨ Features

- **Authentication & Security:**
  - Standard Email/Password Sign-in & Registration
  - Multi-factor Authentication (2FA) & Recovery Codes
  - Passkeys (Biometric / Hardware key logins)
- **Multi-tenant / Team Management:**
  - Create and switch teams
  - Invite members with role-based permissions
- **Inventory & Category Management (Filament Admin):**
  - **Categories:** Add, edit, list, and delete product categories
  - **Products:** Track stock, prices, descriptions, and assign categories with automatic redirection after creation.
- **Modern Responsive Design:** Sleek, user-friendly layout with support for Dark Mode/Light Mode.

---

## 🛠️ Installation & Setup

Follow these steps to run the project locally:

### 1. Prerequisites
Ensure you have the following installed on your machine:
- PHP >= 8.2
- Composer
- Node.js & NPM
- MySQL / MariaDB

### 2. Clone the Repository
```bash
git clone git@github.com:AldioYaspindoDev/kasir-online.git
cd kasir-online
```

### 3. Install Dependencies
**Backend Dependencies:**
```bash
composer install
```

**Frontend Dependencies:**
```bash
npm install
```

### 4. Configuration
Duplicate the environment template file and configure your database settings:
```bash
cp .env.example .env
```

Generate application key:
```bash
php artisan key:generate
```

Open `.env` and set your database connection:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=kasir_online
DB_USERNAME=root
DB_PASSWORD=your_password
```

### 5. Database Migration & Seeding
Run migrations to set up database tables:
```bash
php artisan migrate:fresh
```

### 6. Create Filament Admin User
To access the admin panel, create a superuser:
```bash
php artisan make:filament-user
```
Follow the prompts to enter your Name, Email, and Password.

### 7. Run the Application
Start the local Laravel development server:
```bash
php artisan serve
```

In a separate terminal, compile the frontend assets:
```bash
npm run dev
```

Visit the application at:
- **Client App:** `http://localhost:8000`
- **Filament Admin Dashboard:** `http://localhost:8000/admin`

---

## 📂 Project Structure

- `app/Filament/Resources/` — Filament resource definitions (Categories, Products) and their page actions.
- `app/Models/` — Eloquent models containing relations & database logic.
- `resources/js/` — React components, layouts, hooks, and pages managed by Inertia.js.
- `database/migrations/` — Database schema blueprints.
- `routes/` — Application web, console, and settings route configurations.
