🛍️ Full-Stack E-Commerce Solution
A complete, production-ready e-commerce platform featuring a cross-platform mobile app, a powerful backend API, and a comprehensive admin dashboard.

✨ Key Features
📱 Mobile Application (React Native + Expo)
Authentication: Secure sign-in with Clerk (Google & Apple support).

Shopping Experience: Full cart management, favorites list, address management, and order history.

Payments: Integrated Stripe checkout flow.

Performance: Optimized data fetching and caching using TanStack Query.

UI: Product image sliders and responsive design.

🏪 Admin Dashboard (React + Vite)
Management: CRUD operations for Products, Orders, and Customers.

Analytics: Live dashboard with statistics and charts.

Security: Admin-only protected routes and role-based access.

Monitoring: Sentry integration for error tracking.

⚙️ Backend API (Node.js + Express)
Architecture: robust REST API with Authentication & Role management.

Background Jobs: Asynchronous tasks handled by Inngest.

Deployment: Configured for deployment on Sevalla.

DevOps: End-to-End workflow with CodeRabbit PR analysis and Git branching.

🛠️ Environment Setup
To run this project, you must configure the environment variables for each module. Create a .env file in the respective directories using the templates below.

1. Backend Configuration (/backend/.env)
Code snippet

NODE_ENV=development
PORT=3000

# Database
DB_URL=<YOUR_DB_URL>

# Authentication (Clerk)
CLERK_PUBLISHABLE_KEY=<YOUR_CLERK_PUBLISHABLE_KEY>
CLERK_SECRET_KEY=<YOUR_CLERK_SECRET_KEY>

# Background Jobs (Inngest)
INNGEST_SIGNING_KEY=<YOUR_INNGEST_SIGNING_KEY>

# Image Storage (Cloudinary)
CLOUDINARY_API_KEY=<YOUR_CLOUDINARY_API_KEY>
CLOUDINARY_API_SECRET=<YOUR_CLOUDINARY_API_SECRET>
CLOUDINARY_CLOUD_NAME=<YOUR_CLOUDINARY_CLOUD_NAME>

# Admin & Client Config
ADMIN_EMAIL=<YOUR_ADMIN_EMAIL>
CLIENT_URL=http://localhost:5173

# Payments (Stripe)
STRIPE_PUBLISHABLE_KEY=<YOUR_STRIPE_PUBLISHABLE_KEY>
STRIPE_SECRET_KEY=<YOUR_STRIPE_SECRET_KEY>
STRIPE_WEBHOOK_SECRET=<YOUR_STRIPE_WEBHOOK_SECRET>
2. Admin Dashboard Configuration (/admin/.env)
Code snippet

VITE_CLERK_PUBLISHABLE_KEY=<YOUR_CLERK_PUBLISHABLE_KEY>
VITE_API_URL=http://localhost:3000/api
VITE_SENTRY_DSN=<YOUR_SENTRY_DSN>
3. Mobile App Configuration (/mobile/.env)
Code snippet

EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=<YOUR_CLERK_PUBLISHABLE_KEY>
EXPO_PUBLIC_STRIPE_PUBLISHABLE_KEY=<YOUR_STRIPE_PUBLISHABLE_KEY>
SENTRY_AUTH_TOKEN=<YOUR_SENTRY_DSN>
🚀 Installation & Running
Follow these steps to get the entire stack running locally.

Step 1: Run the Backend
Start the server to handle API requests and database connections.

Bash

cd backend
npm install
npm run dev
Step 2: Run the Admin Dashboard
Launch the web-based dashboard to manage store data.

Bash

cd admin
npm install
npm run dev
Step 3: Run the Mobile App
Launch the Expo development server. You can run this on an emulator or a physical device.

Bash

cd mobile
npm install
npx expo start
After running the command, scan the generated QR Code with your phone using the Expo Go app.
