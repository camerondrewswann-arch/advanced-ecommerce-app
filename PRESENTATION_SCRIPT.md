# Presentation Script - Under 5 Minutes

Hi, my name is Cameron, and this is my advanced e-commerce application built with React, Redux Toolkit, React Query, and the FakeStoreAPI.

The purpose of this project is to simulate a real online shopping experience. Users can browse products, filter them by category, add items to a shopping cart, remove items from the cart, view the total number of products, see the total price, and complete a simulated checkout.

On the home page, the application uses React Query to fetch product data from the FakeStoreAPI. Each product displays important information, including the title, price, category, description, rating, and product image. Since some FakeStoreAPI images may not load correctly, I added a fallback placeholder image so the layout still looks clean if an image fails.

The category dropdown is also dynamic. Instead of hard coding categories, the app uses React Query to request the categories directly from the FakeStoreAPI. When a user selects a category, the app sends a request to the category-specific endpoint and only displays products from that selected category.

For the shopping cart, I used Redux Toolkit to manage the cart state. The cart slice includes actions for adding products, removing products, updating quantities, and clearing the cart during checkout. If a user adds the same product more than once, the cart updates the count instead of creating duplicate items.

I also used sessionStorage to save the cart. This means the cart data can stay available while the browser session is active, even if the user moves between components or refreshes the page.

Now I’ll demonstrate the project.

Here on the home page, you can see all the products being loaded from the API. I can use the category dropdown to filter products. For example, when I select a category, the product list updates and only shows items from that category.

Next, I can click the Add to Cart button on a product. The item is added to the shopping cart. In the cart section, I can see the product title, image, quantity, and price. The app also shows the total number of products and the total price. If I remove an item, the totals update automatically.

Finally, when I click checkout, the application simulates completing the purchase. Since FakeStoreAPI does not process real orders, the checkout clears the Redux cart state and also removes the cart from sessionStorage. A success message is displayed to let the user know the checkout was completed.

Overall, this project demonstrates asynchronous data fetching with React Query, global state management with Redux Toolkit, cart persistence with sessionStorage, dynamic category filtering, and a complete front-end shopping cart workflow.

Thank you for watching my presentation.
