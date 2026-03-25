# Foot Rush Backend

This backend provides a local API for the Foot Rush frontend (pro1.html).

## install and run

```bash
cd d:\html\server
npm install
npm start
```

## endpoints

- GET `/api/products` - list of products
- GET `/api/cart` - current cart items
- POST `/api/cart` - add cart item { name, price }
- DELETE `/api/cart/:name` - remove from cart
- GET `/api/wishlist` - current wishlist
- POST `/api/wishlist` - add wishlist item { name, price, rating, category }
- DELETE `/api/wishlist/:name` - remove from wishlist
- POST `/api/login` - login/create user { username, password }
- GET `/api/users` - user list
- POST `/api/reset` - clear cart + wishlist

## frontend integration

In `d:\html\pro1.html`:
- `handleLogin` calls `/api/login`
- `initializeStore` calls `/api/products`
- `addToCart` posts to `/api/cart`
- `addToWishlist` posts to `/api/wishlist`
- `removeFromWishlist` deletes via `/api/wishlist/:name`

Use CORS-enabled endpoint at `http://localhost:3000`.
