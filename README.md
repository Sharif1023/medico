# ShasthoCare — Full-Stack Pharmacy & Healthcare Commerce

## Live Demo

The project is deployed and available online.

🌐 Live Website:

https://medico.sharuu.com

Admin login-
http://localhost:5173/admin/login

Email & Password:

admin@shasthocare.local
Admin@12345

You can visit the above link to check the complete working application, including the customer storefront and administration control center.

---

ShasthoCare is an original JavaScript-only pharmacy and healthcare ecommerce project with a customer storefront and a full administration control center. The UI follows a clean teal/healthcare visual direction while using original branding and assets.

## Stack

- Client: React 18, Vite, Tailwind CSS, JavaScript, React Router, TanStack Query, Zustand, Axios, Lucide React.
- Server: Node.js, Express, JavaScript, MySQL 8+, mysql2/promise, JWT access tokens, rotating refresh cookies, bcrypt, Multer, Sharp.
- Database: MySQL migrations/schema plus development seed data.
- Security: Helmet, CORS, rate limiting, prepared SQL, RBAC, private prescription files, audit logging.

## What is included

The public site is database/admin driven: brand, logo, favicon, four switchable themes, announcement, header/footer navigation, hero/promo banners, homepage section order/visibility/titles, categories, brands, manufacturers, products, product cover and gallery images, pricing, stock, prescription flags, healthcare services, CMS pages, contact/social information, shipping zones, coupons and payment-method visibility can all be managed from the admin panel.

Administration includes dashboard analytics; products and JSON product import; rich-text editing; categories/brands/manufacturers; FEFO batches, stock movement and adjustments; suppliers and purchase orders; orders, payments and refunds; prescriptions; customers; reviews and returns; coupons, banners and newsletter; services and bookings; homepage, navigation/footer, CMS and contact messages; reports; staff, roles/permissions and audit logs; website/admin settings.

## Admin login

Two admin login routes are available:

- Recovery route:
  `http://localhost:5173/admin/login`

- Configurable alias:
  `http://localhost:5173/control-center/login`

The server hydrates the signed-in user's roles and exposes the admin flag only after role verification. Changing the alias never removes the recovery route.

## Development Super Admin

Email:

```
admin@shasthocare.local
```

Password:

```
Admin@12345
```

## Development Customer

Email:

```
customer@example.com
```

Password:

```
Customer@12345
```

## Quick Start

Requirements:

- Node.js 20+
- npm 10+
- MySQL 8+

Create environment files:

```powershell
Copy-Item server\.env.example server\.env
Copy-Item client\.env.example client\.env
```

Configure `server/.env` with your MySQL credentials.

Install dependencies:

```powershell
npm run install:all
```

Run database migration:

```powershell
npm run db:migrate
```

Load development data:

```powershell
npm run db:seed
```

Start the project:

```powershell
npm run dev
```

## Application URLs

Storefront:

```
http://localhost:5173
```

Admin:

```
http://localhost:5173/admin/login
```

API:

```
http://localhost:5000/api/v1
```

Health Check:

```
http://localhost:5000/health
```

## Product JSON Import

Go to:

```
Admin → Catalog → Products → Add Product → JSON
```

JSON import supports:

- Product information
- Pricing
- Product flags
- Remote or existing `/uploads/...` image URLs
- Initial FEFO batches

See:

```
docs/product-import-example.json
```

for examples.

## Verification

After dependencies are installed:

```bash
npm run verify
npm run build
npm test
```

`npm run verify` checks required admin files, routes, themes, rich-text controls and key database tables.

## Main Features

### Customer Features

- User registration and login
- Product browsing and searching
- Shopping cart
- Wishlist
- Product reviews
- Address management
- Prescription upload
- Order tracking
- Invoice generation
- Coupon support
- Multiple payment methods

### Admin Features

- Dashboard analytics
- Product management
- Category and brand management
- Manufacturer management
- Inventory and FEFO batch management
- Supplier management
- Purchase orders
- Order management
- Payment and refund management
- Prescription review
- Customer management
- CMS management
- Banner management
- Homepage customization
- Navigation management
- Staff roles and permissions
- Audit logs

## Database Modules

The database includes:

- Users
- Roles and Permissions
- Products
- Categories
- Brands
- Manufacturers
- Inventory
- Orders
- Payments
- Prescriptions
- Reviews
- Returns
- Services
- CMS Pages
- Settings
- Audit Logs

## Project Structure

```
ShasthoCare

├── client
│   ├── React Application
│   ├── Components
│   ├── Pages
│   └── State Management
│
├── server
│   ├── Express API
│   ├── Controllers
│   ├── Authentication
│   ├── Database
│   └── Upload Services
│
└── database
    ├── Schema
    └── Seed Data
```

## Security Features

- JWT based authentication
- Refresh token rotation
- Password hashing with bcrypt
- Role Based Access Control (RBAC)
- SQL prepared statements
- Secure file upload handling
- Private prescription file access
- Audit logging

## Production Notes

Before production deployment:

- Change development accounts and secrets
- Enable HTTPS
- Configure production database credentials
- Use persistent storage for uploads
- Configure real payment credentials
- Configure email services
- Setup backups and monitoring
