# MediMart💊 B4A6V4

# Medicine E-Commerce Shop - Project Overview

## Overview:

The **Medicine E-Commerce Shop** is an online platform where users can browse, search, and purchase medicines. The platform will have user authentication, an intuitive shopping experience, secure payment integration, and an order-tracking system. The shop will sell medicines only and will comply with necessary regulations regarding prescription-based purchases.

## Key Features:

### **User Authentication:**

-   Custom login system for users and admins using email/phone number and password.
-   Use of JWT (JSON Web Tokens) for authentication, ensuring secure login.
-   Password hashing using bcrypt for added security.

### **User Roles:**

-   **Customers**: Can browse, add medicines to the cart, and place orders.
-   **Admin**: Manages products, orders, and user queries.

### **Medicine Listings & Search:**

-   Users can search for medicines by name, category, or symptoms.
-   Medicines should have a detailed page including:
    -   Name
    -   Description
    -   Price
    -   Stock availability
    -   Required Prescription (Yes/No)
    -   Manufacturer Details
    -   Expiry date

### **Shopping Cart & Checkout:**

-   Users can add medicines to the cart.
-   Users can modify the cart (increase quantity, remove items).
-   Users can place an order and select delivery options.
-   **Prescription Upload:** If a medicine requires a prescription, users must upload a valid prescription before checkout.
-   Secure checkout with payment integration (Stripe, ShurjoPay, etc.).

### **Order Management & Tracking:**

-   Users can track their orders (Pending, Processing, Shipped, Delivered).
-   Admins can manage orders and update their status.
-   Users receive email notifications on order updates.

### **Admin Dashboard:**

-   -   **Manage Medicines:** Add, update, or remove medicines.
    -   Monitor stock levels and update inventory.
    -   **Manage Orders:** View and process user orders.
    -   Verify uploaded prescriptions before approving orders.
    -   **Manage Users:** View customer details and order history.
    -   **Manage Payments:** Track successful transactions.

### **Security & Compliance:**

-   Ensure prescription medicines require verification before purchase.
-   Implement role-based access control (Admin vs. Customer).

## **Tech Stack:**

### **Frontend:**

-   Next.js
-   TypeScript for type safety
-   React for building user interfaces
-   Tailwind or any other CSS library or framework

### **Backend:**

-   Node.js with Express for REST APIs
-   MongoDB (Mongoose) for storing user data, medicine inventory, and orders
-   JWT for authentication
-   bcryptjs for password hashing

## **Frontend Requirements:**

### **Routes for Customers:**

#### **Home Page (**`**/**`**)**

-   Navbar with necessary menu items and logo
-   Branding section
-   Search bar for finding medicines by name or category.
-   Overview of the shop with featured medicines.
-   Customer reviews (show latest 6)
-   Footer with necessary links

### Register Page(`/register`)

-   Customer will register using their data.

#### **Login Page (**`**/login**`**)**

-   Customers log in using their email and password.

#### **Shop (**`**/shop**`**)**

-   Displays all available medicines.
-   Filtering and sorting options (category, price, required prescription, etc.).
-   Infinite scrolling on this page.

#### **Medicine Details (**`**/medicine/:id**`**)**

-   Displays detailed information about the medicine.
-   Add to cart button.

#### **Cart Page (**`**/cart**`**)**

-   Users can view, edit, and proceed to checkout.

#### **Checkout Page (**`**/checkout**`**)**

-   Users enter their shipping details.
-   Users upload a prescription if required.
-   Users select a payment method and confirm the order.

#### **Order History (**`**/orders**`**)**

-   Users can view past orders and track current orders.

#### **Profile Page (**`**/profile**`**)**

-   Users can update personal details (name, email, phone number, address, etc.).

### **Routes for Admin:**

#### **Admin Dashboard (**`**/admin**`**)**

-   Overview of total orders, stock levels, and pending prescriptions.

#### **Manage Medicines (**`**/admin/medicines**`**)**

-   Add, update, and remove medicines from the inventory.

#### **Manage Orders (**`**/admin/orders**`**)**

-   Approve or reject prescription-based orders.
-   Update order statuses.

#### **Manage Users (**`**/admin/users**`**)**

-   View customer details and order history.

## **UI/UX Design:**

-   **Responsive Design:** Optimized for mobile and desktop.
-   **Modern UI/UX:** Clean, minimal, and easy navigation.
-   **User-friendly Interface:** Simple forms for login, ordering, and profile management.

## **Additional Features:**

-   **Live Chat Support:** Customers can chat with a support agent.
    -   **Email Notifications:** Order confirmation and status updates.
    -   Admin notifications for low stock.
-   **Discounts & Coupons:** Admin can create discount codes for promotions.

## **Deployment:**

-   **Frontend:** Vercel, Netlify, or similar
-   **Backend:** Vercel, Render, or similar

## **Submission Guidelines:**

### **Codebase:**

-   Clean, well-documented code.
-   Follow best practices for security and optimization.

### **GitHub Repositories:**

-   Separate repositories for frontend and backend.
-   Meaningful commit messages.

### **Live Deployment:**

-   Provide working live URLs for both frontend and backend.

### Admin Credentials:

-   Admin credentials like: Email and password.

### **Demo Video:**

-   A short video showcasing:
    -   User registration/login.
    -   Browsing and searching medicines.
    -   Adding to cart and placing an order.
    -   Admin managing medicines and orders.

### **Timeline & Marks:**

-   **Full Submission (60 Marks)**: Due by **March 06, 2025, 11:59 PM**.
-   **Late Submission (50 Marks)**: Due by **March07, 2025, 11:59 PM**.
-   **Late Submission with Penalty (30 Marks)**: Due by **March 07, 2025, 11:59 PM**.

### **Important Notes:**

-   **Plagiarism:** This will result in 0 marks.
-   **Focus on Functionality:** Keep it simple but complete.