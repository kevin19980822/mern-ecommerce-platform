# Full-Stack E-commerce Platform

A TypeScript MERN commerce application foundation covering product discovery, cart and checkout, inventory, order lifecycle, and administration.

## Stack
- React + TypeScript storefront (planned)
- Node.js + Express + TypeScript API
- MongoDB + Mongoose
- Zod request validation
- Stripe checkout integration (planned; use test keys only)

## Getting started
1. Install Node.js 20+ and MongoDB.
2. Copy `.env.example` to `.env`.
3. Run `npm install`, then `npm run dev`.

## Current implementation
Initial API foundation with health endpoint and centralized error handling. Catalog, inventory transactions, checkout, webhook verification, and frontend are staged for follow-up commits.

## Security notes
Never trust client-supplied prices or inventory counts. Checkout totals must be calculated server-side and payment webhooks must be signature-verified.
