# Cria Marketplace Technical Architecture

## Core Tech Stack
- **Framework**: Next.js 15 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS + Shadcn/UI + Framer Motion
- **Backend/Auth**: Supabase (PostgreSQL, Auth, Storage)
- **Payments**: Stripe Connect (Marketplace)
- **State Management**: Zustand
- **Forms/Validation**: React Hook Form + Zod

## Folder Structure
```text
/
├── app/                  # Route groups & pages
│   ├── (auth)/           # login, signup, forgot-password
│   ├── (shop)/           # products, artists, collections
│   ├── (dashboard)/      # Protected seller routes
│   ├── (admin)/          # Protected admin routes
│   └── layout.tsx        # Global layout with providers
├── components/
│   ├── ui/               # Shadcn components
│   ├── shared/           # Header, Footer, LiquidGlassCard
│   ├── product/          # Gallery, PriceTag, VariantPicker
│   └── dashboard/        # Charts, StatCards, OrderTable
├── lib/
│   ├── supabase/         # Client/Server configs
│   ├── stripe/           # Stripe Connect logic
│   └── utils.ts          # Tailwind merge & helpers
├── hooks/                # useAuth, useCart, useWishlist
├── store/                # Zustand stores
├── actions/              # Server Actions for mutations
└── types/                # TypeScript interfaces
```

## Database Schema (PostgreSQL)

### Users & Profiles
- `users`: (Internal Supabase Auth)
- `profiles`: id, full_name, email, avatar_url, role (buyer, seller, admin)
- `seller_profiles`: id, bio, craft_type, city, state, stripe_account_id, rating

### Products
- `categories`: id, name, slug, description, image_url
- `products`: id, seller_id, title, description, price, stock, category_id, materials, dimensions, production_time, status (draft, active)
- `product_images`: id, product_id, url, position

### Orders & Transactions
- `orders`: id, buyer_id, total_amount, status, shipping_address, created_at
- `order_items`: id, order_id, product_id, quantity, unit_price
- `transactions`: id, order_id, stripe_payment_id, amount, fee_amount, seller_amount

### Interactions
- `reviews`: id, product_id, user_id, rating, comment
- `wishlist`: id, user_id, product_id
- `cart_items`: id, user_id, product_id, quantity
