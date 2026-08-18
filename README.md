# Online Clothing Store

A responsive React storefront for men's and women's clothing with a cart, checkout form, WhatsApp contact, and an Express order API.

## Project structure

- `frontend/` - Create React App storefront
- `backend/` - Express API with JSON-file persistence for orders and products

## Run locally

### Frontend

```bash
cd frontend
npm install
npm start
```

### Backend

```bash
cd backend
npm install
npm run dev
```

The API runs on `http://localhost:5000`. Create `frontend/.env` with `REACT_APP_API_URL=http://localhost:5000/api` if you want checkout orders sent to the API. Without it, the demo checkout still works in the browser.

## Admin API

Set `ADMIN_KEY` in `backend/.env`. Use `GET /api/products` to read products, `POST /api/products` with header `x-admin-key` to add a product, and `GET /api/orders` with the same header to view orders. Add authentication and a payment provider before using this in production.
