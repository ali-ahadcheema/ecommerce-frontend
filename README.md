Fashion Store: Frontend

React frontend for a full stack e-commerce store with Stripe payments, Google sign-in and an AI shopping assistant.

Backend repo: link to your backend repo

Home page

Features
Product listing with category and price filters, and pagination
Product detail page with quantity selector
Login and sign up with email and password, and Google sign-in
Cart: add, edit and remove items
Checkout with Stripe card payments (test mode)
Order history with filters for payment and status
Admin dashboard
AI shopping assistant in a slide-in side panel: search products, check order status and manage the cart. Before it changes anything, it asks the user to confirm.
Responsive layout
Tech stack
React (Vite)
Tailwind CSS
React Router
Axios
Stripe (@stripe/react-stripe-js)
lucide-react and react-icons
react-markdown for AI replies
Getting started
1. Install
bash
git clone https://github.com/YOUR-USERNAME/YOUR-FRONTEND-REPO.git
cd YOUR-FRONTEND-REPO
npm install
2. Environment variables

Create a .env file in the project root (see .env.example):

VITE_API_URL=http://localhost:3000/link
VITE_STRIPE_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxx

Only the Stripe publishable key goes in the frontend. Never put a secret key here.

3. Run
bash
npm run dev

The app runs on http://localhost:5173. The backend must be running on port 3000, with CORS allowing this origin.

Test payments

Stripe runs in test mode. Use this card:

Field	Value
Card number	4242 4242 4242 4242
Expiry	any future date
CVC	any 3 digits
Project structure
src/
  frontpage.jsx      Home page
  shop.jsx           Product list, filters, pagination
  product.jsx        Product detail, add to cart, buy now
  allcart.jsx        Cart page
  orderprofile.jsx   Order history
  ai.jsx             AI assistant side panel
  dashboard.jsx      Admin dashboard
  login.jsx          Login
  signup.jsx         Sign up
  context.jsx        Auth context
  App.jsx            Routes and Stripe provider
How the AI assistant works

The panel sends the user's message to the backend. If the AI wants to change something (for example remove an item from the cart), the backend returns a confirmation request and the panel shows Yes and No buttons. Nothing changes until the user clicks Yes.

Screenshots
Shop	Product	AI assistant
Shop	Product	AI
Author

Ali Cheema. Open to freelance work. LinkedIn
