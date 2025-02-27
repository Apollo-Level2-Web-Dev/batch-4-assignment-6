# SecondHand 🛒 (Marketplace for Buying & Selling Used Items) B4A6V5

## **Project Overview**

You are tasked with developing a **SecondHand Marketplace Web Application**, where users can buy and sell used items easily. The platform should allow users to post listings for used items, browse available products, and communicate securely with sellers. The system must provide a seamless and secure experience for all users.

----------

## **Roles**

-   -   **User (Single Role)**A unified role where users can both **buy and sell** items.
    -   **Admin (Optional)**Can manage users and listings.

----------

## **Key Features**

### **User Authentication**

-   Custom login system using **email/phone number** and password.
-   **JWT (JSON Web Token)** for secure authentication.
-   **Password hashing** using bcrypt for security.

### **User Dashboard**

-   **Post an Item for Sale:** Users can list used items with descriptions, images, pricing, and categories.
-   **Manage Listings:** Update, and remove item listings.
-   **Track Sales & Purchases:** View purchase history and sales history.
-   **Profile Management:** Edit personal details.
-   **Wishlist Feature:** Save items for later.

### **Listings and Search**

-   Users can **list items** for sale with details like price, condition, images, and category.
-   **Search & Filter:** Powerful filtering system based on category, price, condition, and location.
-   **Mark as Sold:** Sellers can update item status after a sale.

### **Communication & Transactions (Optional)**

-   **Messaging System:** Users can chat with sellers before making a purchase.
-   **Order Management:** Users can track sold/purchased items.

### **Admin Features (Optional)**

-   **User Management:** Ban/unban users.
-   **Listing Management:** Delete inappropriate listings.

----------

## **Tech Stack**

### **Frontend:**

-   **Next.js** (for SSR/SSG)
-   **TypeScript** (for type safety)

### **Backend:**

-   **Express.js** (REST API)
-   **MongoDB** (for user and product data storage)
-   **JWT** (authentication)
-   **bcrypt** (password hashing)

### **Deployment:**

-   **Frontend:** Vercel, Netlify
-   **Backend:** Vercel, Railway

----------

## **Frontend Requirements**

### **User Routes:**

1.  **Home Page (**`**/**`**)** – Overview of available items.
2.  **Login Page (**`**/login**`**)** – Authenticate users.
3.  **Products Page (**`**/products**`**)** – Browse all listings.
    -   **User Dashboard (**`**/dashboard**`**)Track Purchases (**`**/dashboard/purchase-history**`**)** – View order history.
    -   **Manage Listings (**`**/dashboard/listing**`**)** – Create, update, delete listings.
    -   **Track Sales (**`**/dashboard/sales-history**`**)** – View sales inquiries.
    -   **Profile (**`**/dashboard/profile**`**)** – Edit personal details.
4.  **Messages (**`**/messages**`**)** – Direct communication between buyers and sellers (optional).

### **Admin Routes (Optional):**

1.  **Admin Dashboard (**`**/dashboard/admin**`**)** – Admin panel.
2.  **User Management (**`**/dashboard/admin/user-management**`**)** – Ban/unban users.
3.  **Listings Management (**`**/dashboard/admin/listings**`**)** – Delete or review listings.

----------

## **Backend Requirements**

### **Database Collections (MongoDB):**

-   -   **Users Collection**Fields: `name`, `email`, `phone number`, `password (hashed)`, `role`.
    -   **Listings Collection**Fields: `title`, `description`, `price`, `condition`, `images`, `userID (seller)`, `status (available/sold)`.
    -   **Transactions Collection**Fields: `buyerID`, `sellerID`, `itemID`, `status (pending/completed)`.
    -   **Messages Collection (Optional)**Fields: `senderID`, `receiverID`, `message`, `timestamp`.

### **API Endpoints (CRUD Operations)**

#### **Authentication**

-   `POST /auth/register` – Register a new user.
-   `POST /auth/login` – User login.
-   `POST /auth/logout` – Logout user.

#### **Listings**

-   `GET /listings` – Retrieve all available listings.
-   `GET /listings/:id` – Retrieve details of a specific listing.
-   `POST /listings` – Create a new product listing.
-   `PUT /listings/:id` – Update listing details.
-   `DELETE /listings/:id` – Remove a listing.

#### **User Management**

-   `GET /users/:id` – Retrieve user details.
-   `PUT /users/:id` – Update user profile.
-   `DELETE /users/:id` – Delete user account.

#### **Transactions & Purchases**

-   `GET /purchases/:userId` – Fetch purchase history.
-   `GET /sales/:userId` – Fetch sales history.
-   `POST /transactions` – Create a new transaction.
-   `PUT /transactions/:id` – Update transaction status.

#### **Admin (Optional)**

-   `PUT /users/:id/ban` – Ban/unban a user.
-   `DELETE /listings/:id` – Delete a listing.

#### **Messages (Optional)**

-   `POST /messages` – Send a message.
-   `GET /messages/:userId` – Retrieve user messages.

----------

## **UI/UX Design Considerations**

-   **Responsive Design:** Mobile-friendly.
-   **Modern UI/UX:** Simple navigation, clear CTAs, and intuitive interface.
-   **User-friendly Forms:** Easy to post listings, search, and communicate.

----------

## **Additional Features**

-   -   **Email Notifications**
        -   **For Buyers:** When a seller responds to their inquiry.
        -   **For Sellers:** When they receive a new inquiry.
    -   **Role-Based Access Control:** Buyers & sellers have equal access; optional admin role for moderation.

----------

## **Submission Guidelines**

### **Codebase**

-   Well-structured, documented, and follows best practices.
-   **GitHub Repositories:** Separate repos for **frontend** and **backend**.
-   Commit history must reflect the development process.

### **Live Deployment**

-   Provide working **frontend** and **backend** URLs.
-   Ensure a seamless user experience.

### **Demo Video**

A short video demonstrating:

-   User registration/login.
-   Posting a listing (seller).
-   Searching for items (buyer).
-   Sending an inquiry (buyer).
-   Responding to inquiries (seller).

----------

### **Timeline & Marks:**

-   **Full Submission (60 Marks)**: Due by **March 06, 2025, 11:59 PM**.
-   **Late Submission (50 Marks)**: Due by **March07, 2025, 11:59 PM**.
-   **Late Submission with Penalty (30 Marks)**: Due by **March 07, 2025, 11:59 PM**.

### **Important Notes:**

-   **Plagiarism:** Must be original work. Any plagiarism detected will result in **0 Marks**.
-   **Simplicity:** Focus on **functionality over unnecessary complexity**.

----------

🚀 **Good luck! Let me know if you need any further clarifications!**