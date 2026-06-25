# Advanced E-Commerce App

A React e-commerce application built for the advanced module project. The app uses FakeStoreAPI for product/category data, React Query for asynchronous API fetching, Redux Toolkit for shopping cart state, and sessionStorage for cart persistence.

## Features

- Product catalog loaded from FakeStoreAPI
- Product cards showing title, price, category, description, rating, and image
- Graceful fallback placeholder for broken product image URLs
- Dynamic category dropdown loaded from FakeStoreAPI
- Category-specific product filtering using FakeStoreAPI category endpoints
- Add products to shopping cart directly from the home page
- Shopping cart powered by Redux Toolkit
- Update cart item quantity
- Remove products from cart
- Total product count and total price calculation
- sessionStorage persistence during the browser session
- Simulated checkout that clears Redux state and sessionStorage
- Clean responsive UI

## Technologies Used

- React
- Vite
- React Router DOM
- Redux Toolkit
- React Redux
- React Query / TanStack Query
- FakeStoreAPI
- sessionStorage
- CSS

## API Endpoints Used

```txt
GET https://fakestoreapi.com/products
GET https://fakestoreapi.com/products/categories
GET https://fakestoreapi.com/products/category/{category}
```

## How to Run the Project

1. Download or clone this project.
2. Open the project folder in VS Code.
3. Open a terminal in the project folder.
4. Install dependencies:

```bash
npm install
```

5. Start the development server:

```bash
npm run dev
```

6. Open the local URL shown in the terminal. It will usually be:

```txt
http://localhost:5173/
```

## How the Cart Works

The cart is managed in `src/features/cart/cartSlice.js` using Redux Toolkit.

Cart actions include:

- `addToCart`
- `removeFromCart`
- `updateQuantity`
- `clearCart`

The cart is stored as an array of product objects in `sessionStorage` using this key:

```txt
cart
```

Each cart item uses this structure:

```js
{
  id: 1,
  title: "Product Name",
  price: 19.99,
  image: "image-url",
  count: 2
}
```

## Checkout

FakeStoreAPI does not process real orders, so this project simulates checkout by:

1. Clearing the Redux cart state
2. Removing the cart from sessionStorage
3. Showing a checkout success message

## Project Structure

```txt
src/
  api/
    fakestore.js
  app/
    store.js
  components/
    CategorySelect.jsx
    ProductCard.jsx
    ShoppingCart.jsx
  features/
    cart/
      cartSlice.js
  pages/
    Home.jsx
  App.jsx
  main.jsx
  styles.css
```

## Video Presentation Reminder

The project video must be under 5 minutes. You must be visible on camera. Upload the video directly to Disco. Do not use Google Drive or external video links.

Submit:

- GitHub repository URL
- Uploaded video attached directly in Disco
