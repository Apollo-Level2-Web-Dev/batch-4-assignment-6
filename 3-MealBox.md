# Meal Box -  🍱 (Personalized Meal Planning & Delivery) B4A6V3

### Project Overview:

You are tasked with developing a **Meal Planning & Delivery Web Application** where users can personalize their meal plans and have meals delivered based on their dietary preferences and schedules. The platform should allow customers to choose meal options, set dietary preferences, and schedule deliveries, while meal providers can manage menus and respond to customer requests.

### Key Features:

#### 1. User Authentication:

-   Custom login system for customers and meal providers using email or phone number and password.
-   Use of **JWT (JSON Web Tokens)** for authentication, ensuring secure login.
-   Password hashing using **bcrypt** for added security.

#### 2. Customer and Meal Provider Dashboards:

-   **Customer Dashboard:** For selecting meal plans, tracking orders, and managing preferences.
-   **Meal Provider Dashboard:** For managing meal menus, responding to customer orders, and tracking deliveries.

#### 3. Meal Selection & Preferences:

-   Customers can select meal plans and customize meals based on dietary preferences (vegan, keto, gluten-free, etc.).
-   Meal providers can create and update meal options, specifying ingredients, portion sizes, and pricing.

#### 4. Search and Match:

-   Customers can search for meals based on cuisine, dietary preferences, ratings, and availability.
-   Meal providers can view customer meal preferences and prepare orders accordingly.

#### 5. Role-Based Access Control:

-   Different routes and views for customers and meal providers, each with access to platform-specific features.
-   **Admin access** (if implemented) will be used to manage users and content.

#### 6. CRUD Operations:

-   Customers can **create, view, and update** their meal plans and preferences.
-   Meal providers can **view and respond** to customer meal requests.

### Tech Stack:

#### Frontend:

-   **Next.js** (for SSR/SSG)
-   **TypeScript** for type safety
-   **React** for building user interfaces

#### Backend:

-   **Node.js with Express** for REST APIs
-   **MongoDB** for storing data (users, meal menus, orders)
-   **JWT** for authentication
-   **bcrypt** for password hashing

#### Deployment:

-   **Frontend:** Vercel, Netlify, or similar
-   **Backend:** Heroku, AWS, or similar

### Frontend Requirements:

#### Routes for Customers:

-   **Home Page (/):** Overview of the platform and its benefits for customers.
-   **Login Page (/login):** Customers can log in using their email/phone number and password.
    -   **Customer Dashboard (/dashboard/customer):Select Meals:** Customers can browse available meal options and customize their orders.
    -   **Track Orders:** View past and ongoing meal deliveries.
    -   **Manage Preferences:** Set dietary restrictions, preferred cuisines, and portion sizes.
-   **Customer Profile (/profile/customer):** Customers can edit personal details (name, email, phone number, delivery address, etc.).
-   **Find Meals (/find-meals):** Customers can search for meals based on preferences, ratings, and meal providers.
-   **Order Meal (/order-meal):** Customers can place meal orders, including schedule and customization options.

#### Routes for Meal Providers:

1.  **Home Page (/):** Overview of the platform, benefits, and how meal providers can manage menus and respond to orders.
2.  **Login Page (/login):** Meal providers log in using email/phone number and password.
3.  **Meal Provider Dashboard (/dashboard/provider):Manage Menus:** Meal providers can create and update their meal offerings.
    -   **View Orders:** List of customer orders and their preferences.
    -   **Respond to Orders:** Accept, modify, or decline meal requests.
4.  **Meal Provider Profile (/profile/provider):**Edit meal provider profile, including cuisine specialties, pricing, and availability.
5.  **Post Meal Menu (/post-meal-menu):**Meal providers can post detailed meal menus for customers to browse.
6.  **Order Responses (/responses):**Meal providers can confirm or decline customer orders.

### Backend Requirements:

#### Database Collections (MongoDB):

-   -   **Users Collection:**Fields: Name, email, phone number, password (hashed), role (customer or meal provider), and any other necessary details.
    -   Stores user credentials and roles for authentication and authorization.
    -   **Orders Collection:**Fields: Meal selection, dietary preferences, customer ID, status (pending, in progress, delivered).
    -   Tracks all meal orders placed by customers.
    -   **Meal Providers Collection:**Fields: Cuisine specialties, available meal options, pricing, experience, customer reviews, etc.
    -   Stores meal provider profiles that customers can browse.

#### Authentication:

-   Use **JWT** for handling user sessions securely.
-   Implement **bcrypt** for password hashing.
-   Custom **middleware for protected routes** to ensure that only authorized users (customers and meal providers) can access their respective dashboards.

#### CRUD Operations:

-   -   **Customers:**`POST /customers/order`: Create a new meal order.
    -   `GET /customers/orders`: Retrieve all orders placed by the customer.
    -   `PUT /customers/profile`: Update customer profile.
    -   **Meal Providers:**`POST /providers/menu`: Create or update meal menu.
    -   `GET /providers/orders`: Retrieve all customer orders.
    -   `PUT /providers/response`: Respond to customer orders.

### UI/UX Design:

-   **Responsive Design:** Mobile-friendly, optimized for all devices.
-   **Modern UI/UX:** Simple navigation, clear calls to action, and easily accessible features.
-   **User-friendly Interface:** Easy-to-use forms for placing orders, managing preferences, and search filters.

### Additional Features:

#### Meal Ordering:

-   Customers can place meal orders with detailed dietary preferences and delivery schedules.

#### Meal Provider Profiles:

-   Meal providers can create detailed profiles, including cuisines, pricing, and availability.

#### Search and Match:

-   Customers can search meals based on dietary preferences, ratings, and provider availability.
-   Meal providers can view customer preferences and prepare meals accordingly.

#### Email Notifications:

-   **For Customers:** Email updates when meals are prepared and out for delivery.
-   **For Meal Providers:** Email when a new order is placed.

#### Role-Based Access:

-   Customers and meal providers have different access roles.

### Deployment:

-   **Frontend:** Deploy using Vercel or similar platforms.
-   **Backend:** Deploy using Heroku or similar platforms.

### Submission Guidelines:

#### Codebase:

-   Clean, well-organized, and well-documented codebase following best practices.

#### GitHub Repositories:

-   Separate repositories for frontend and backend.
-   Ensure a commit history reflecting your development process.

#### Live Deployment:

-   Provide live URLs for both frontend and backend.

#### Demo Video:

A short video demonstrating:

-   User registration/login.
-   Placing a meal order (customer).
-   Managing menus (meal provider).
-   Searching for meals (customer).
-   Responding to orders (meal provider).

### **Timeline & Marks:**

-   **Full Submission (60 Marks)**: Due by **March 06, 2025, 11:59 PM**.
-   **Late Submission (50 Marks)**: Due by **March07, 2025, 11:59 PM**.
-   **Late Submission with Penalty (30 Marks)**: Due by **March 07, 2025, 11:59 PM**.

**Important Notes:**

-   **Plagiarism:** Must be original work. Any plagiarism detected will result in 0 Marks.
-   **Simplicity:** Focus on building a functional platform with specified features.

Good luck! Let me know if you need any further clarification!