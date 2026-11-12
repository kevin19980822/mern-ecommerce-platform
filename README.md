# MERN E-commerce Platform

A TypeScript MERN storefront with product discovery, search, authenticated shopping cart, Stripe Checkout, order history, stock tracking and admin catalog tools.

## Stack
React + TypeScript + Vite; Express + TypeScript; MongoDB/Mongoose; JWT; Zod; Stripe-hosted Checkout.

## Run locally
1. Install Node.js 20+ and MongoDB.
2. Copy `.env.example` to `.env`; use a JWT secret of 32+ characters.
3. Run `npm install`.
4. Run `npm run dev`.
5. Open http://localhost:5174 (API http://localhost:4001).

## Stripe test checkout
Add Stripe test keys to `.env`. Configure a webhook for `checkout.session.completed` at `/api/checkout/webhook` and set `STRIPE_WEBHOOK_SECRET`. For local testing use Stripe CLI forwarding to http://localhost:4001/api/checkout/webhook. Never use live payment keys in development. Card details are handled by Stripe, not stored here.

## Admin access
Set `ADMIN_EMAILS` to a comma-separated list of registered user emails. Admins can create, update and deactivate products.

## API
- POST /api/auth/register, POST /api/auth/login, GET /api/auth/me
- GET /api/products?q=...&category=..., GET /api/products/:id
- POST/PATCH/DELETE /api/products (admin)
- GET /api/cart, POST /api/cart/items, PATCH/DELETE /api/cart/items/:productId
- POST /api/checkout/session, POST /api/checkout/webhook
- GET /api/orders

This is a portfolio implementation. Before real commerce use, add payment/order reconciliation, transactional stock reservation, rate limiting, shipping/tax rules, monitoring, backups, HTTPS, CI and a security review.
