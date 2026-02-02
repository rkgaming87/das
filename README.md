# PetZio - Complete E-Commerce Platform

A full-stack, FAANG-level e-commerce platform for pet supplies with multi-role support (Customer, Vendor, Admin).

## 🎨 Theme: Playful Professionalism

- **Primary Color**: `#FF8C42` (Warm Orange) - Energy, happiness, pet friendliness
- **Secondary Color**: `#4A90E2` (Soft Blue) - Trust, professional care
- **Background**: `#F9FAFB` (Off-white) - Clean, high-conversion

## ✨ Features

### 🏠 **Landing/Home Page** (Public)
- Hero section with high-quality pet imagery
- Pet category grid (Dog, Cat, Bird, Fish, Small Pets)
- Featured products carousel
- Vendor spotlight
- Trust badges (Verified Vendors, Fast Delivery, Pet Care Guaranteed)

### 🛍️ **Product Discovery (Shop) Page**
- Advanced faceted search with filters:
  - Category filter
  - Price range slider
  - Brand filter
  - Vendor filter
- Active filters bar with clear chips
- Responsive 4-column product grid
- Real-time search functionality

### 📦 **Product Details Page**
- Breadcrumb navigation
- Image gallery with thumbnail strip
- Product specifications (SKU, brand, stock)
- Quantity selector
- "Add to Cart" and "Buy Now" options
- Vendor information card
- Related products section
- Trust indicators

### 🛒 **Shopping Cart & Checkout**
- Cart item management (add, remove, update quantity)
- Order summary with tax calculation
- Promo code support (Try: PET10 for 10% off)
- Free shipping threshold ($50+)
- Multi-step checkout:
  1. Shipping information
  2. Payment details (mock UI)
  3. Order confirmation
- Secure checkout badges

### 👤 **Customer Dashboard**
- Order history with status tracking
- Profile management
- Order details view
- Account information

### 🏪 **Vendor Business Suite**
- Sales analytics with charts (Recharts)
- Inventory management table with CRUD operations
- Order fulfillment tracking
- Product stock alerts
- Revenue overview

### ⚙️ **Admin Command Center**
- Platform analytics dashboard
- User management with search
- Vendor moderation
- Orders overview
- Security audit logs
- Revenue trends (Bar chart)
- Product distribution (Pie chart)

### 🔐 **Authentication Suite**
- Sign in / Sign up with role selection
- NextAuth.js integration
- Password strength meter
- Demo accounts provided
- Role-based access control

## 🔑 Demo Accounts

```
Customer Account:
Email: customer@test.com
Password: customer123

Vendor Account:
Email: vendor@test.com
Password: vendor123

Admin Account:
Email: admin@test.com
Password: admin123
```

## 🛠️ Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Styling**: Tailwind CSS + shadcn/ui components
- **Authentication**: NextAuth.js
- **State Management**: React Context API (Cart)
- **Form Handling**: React Hook Form + Zod validation
- **Charts**: Recharts
- **Icons**: Lucide React
- **Notifications**: Sonner
- **Data**: Mock data (no backend required)

## 📁 Project Structure

```
/app
├── app/
│   ├── api/auth/[...nextauth]/     # NextAuth configuration
│   ├── auth/signin/                # Authentication page
│   ├── shop/                       # Product discovery
│   ├── product/[id]/               # Product details
│   ├── cart/                       # Shopping cart
│   ├── checkout/                   # Checkout flow
│   ├── dashboard/                  # Customer dashboard
│   ├── vendor/                     # Vendor dashboard
│   ├── admin/                      # Admin panel
│   ├── order-confirmation/         # Order success page
│   ├── page.js                     # Home page
│   ├── layout.js                   # Root layout
│   └── globals.css                 # Global styles
├── components/
│   ├── Navbar.js                   # Navigation component
│   ├── ProductCard.js              # Product display card
│   └── ui/                         # shadcn/ui components
├── lib/
│   ├── mockData.js                 # Mock data (products, users, orders)
│   └── CartContext.js              # Cart state management
└── package.json
```

## 🚀 Getting Started

### Installation

```bash
# Install dependencies
yarn install

# Run development server
yarn dev
```

Visit `http://localhost:3000` to see the application.

## 🎯 Key Pages & Routes

| Route | Description | Access |
|-------|-------------|--------|
| `/` | Home page | Public |
| `/shop` | Product discovery | Public |
| `/product/[id]` | Product details | Public |
| `/auth/signin` | Authentication | Public |
| `/cart` | Shopping cart | Public |
| `/checkout` | Checkout flow | Public |
| `/dashboard` | Customer dashboard | Customers only |
| `/vendor` | Vendor dashboard | Vendors only |
| `/admin` | Admin panel | Admins only |

## 🎨 Design Patterns

### Atomic Design
- **Atoms**: Buttons, Inputs, Labels, Badges
- **Molecules**: ProductCards, SearchBars, FilterComponents
- **Organisms**: Navbar, Dashboard layouts, Product grids

### Component Architecture
- Server components by default for optimal performance
- Client components (`'use client'`) only when needed:
  - State management (useState, useEffect)
  - Event handlers
  - Browser APIs
  - Authentication hooks

## 💾 Mock Data Structure

### Products
- 14 sample products across 5 categories
- Realistic pricing, ratings, and stock levels
- Associated with vendors

### Vendors
- 3 verified pet stores
- Location, rating, and sales data
- Linked to products

### Orders
- Sample order history
- Multiple statuses (processing, shipped, delivered)
- Tied to customers and vendors

### Users
- Demo accounts for all roles
- Avatar images from pravatar.cc

## 🔒 Security Features

- Role-based authentication
- Protected routes with middleware checks
- Session management via NextAuth.js
- Secure password handling (mock implementation)

## 🎨 UI/UX Features

- **Responsive Design**: Mobile-first approach
- **Loading States**: Skeleton screens and spinners
- **Error Handling**: Toast notifications for user feedback
- **Accessibility**: Semantic HTML and ARIA labels
- **Animations**: Framer Motion for micro-interactions
- **Dark Mode Ready**: CSS variables for theming

## 🧪 Testing Tips

1. **Customer Flow**:
   - Browse products → Add to cart → Checkout → View order in dashboard

2. **Vendor Flow**:
   - Sign in as vendor → View inventory → Check orders → Update stock

3. **Admin Flow**:
   - Sign in as admin → View analytics → Manage users → Monitor orders

## 📝 Notes

- All data is mock data stored in memory
- Cart persists in localStorage
- Payment is simulated (no actual transactions)
- No MongoDB required for this frontend-focused build
- All images from Unsplash (placeholder)

## 🎯 Performance Optimizations

- Lazy loading for routes
- Image optimization with Next.js Image component
- Memoization for product filtering
- Efficient state updates
- Code splitting by route

## 🐛 Known Limitations

- Mock data only (no real backend)
- No actual payment processing
- Search is client-side only
- No real-time updates
- Single-session shopping cart

## 🤝 Contributing

This is a demonstration project. Feel free to extend with:
- Real API integration
- Database connection
- Payment gateway (Stripe/PayPal)
- Email notifications
- Advanced search (Algolia/Elasticsearch)

## 📄 License

MIT License - Feel free to use this project for learning and development.

---

Built with ❤️ for pet lovers everywhere 🐾
