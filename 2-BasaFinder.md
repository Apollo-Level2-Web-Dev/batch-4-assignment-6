# BasaFinder 🏡 (Smart Rental & Housing Solution) B4A6V2

# **Project Overview**

## **Purpose:**

BasaFinder is a full-stack web application that provides a smart rental housing solution. The platform connects landlords, tenants, and an admin who oversees both users and house listings. Landlords can post and manage rental property listings, while tenants can search for, view, and request rentals. When a landlord approves a rental request, a payment option becomes available to the tenant, and the landlord can provide their phone number for further contact.

## **Key Components:**

### **Roles:**

-   -   **Admin:** Manages all users(Landlords, Tenants) accounts and rental house posts.
    -   **Landlord:** Posts and manages their rental listings, reviews and responds to rental requests.
    -   **Tenant:** Searches for rental houses and submits requests to rent.

### **Security:**

-   -   Custom authentication using JWT (JSON Web Token).
    -   Password hashing using bcrypt for secure storage.
    -   Role-based access control to ensure only authorized access to private pages.

----------

### Core Functionalities:

-   -   **Rental House Listings:** Landlords can post detailed rental listings with `rental house location`, `details description`, `rent amount`, `number of bedrooms`, `multiple images`, `landlord ID (to link with the users collection)` and any other necessary details.
    -   **Search & Filter:** Tenants can search rentals by `location`, `price` and `number of bedrooms`.
    -   **Rental Requests:** Tenants can submit rental requests. Landlords can approve/reject them.
    -   **Payment:** When a landlord approves a rental request, a payment option (Stripe, ShurjoPay, etc) is made available on the tenant’s end to secure the rental.
    -   **Role-Based Dashboards:** Custom dashboards for **Admin**, **Landlords** and **Tenants**.
    -   **Email Notifications:** Automatic updates for rental requests.

----------

### **Tech Stack:**

-   -   **Frontend**:
        -   **Next.js** (for SSR/SSG)
        -   **TypeScript** for type safety
        -   **React** for building user interfaces
    -   **Backend**:
        -   **Node.js** with **Express** for REST APIs
        -   **MongoDB** for storing data
        -   **JWT** for authentication
        -   **bcrypt** for password hashing
    -   **Deployment**:
        -   **Frontend**: Vercel, Netlify, or similar
        -   **Backend**: Heroku, AWS, or similar

----------

# **Home Page / Landing Page**

## **Header**

**Logo:** Prominently display the BasaFinder logo.

**Navigation Bar:**

-   -   Home
    -   About Us
    -   All Listed Rental Housing Page
    -   Dashboard (Will redirect to a specific user dashboard based on their role)
    -   Login/Register (if the user is not logged in)
    -   My Profile (if logged in)
    -   You can add other nav options if necessary

## **Hero Section**

**Headline:** A catchy statement (e.g., “Find Your Perfect Rental House Today!”).

**Call-to-Action Button:** “Post Rental House Info” that directs Landlords to the listing submission page.

**Search Option:** Allow users to search for rental houses by:

-   -   Location
    -   Price range
    -   Number of bedrooms

**Rental House Cards:** Each card should display:

-   -   Location
    -   Representative images
    -   Brief description
    -   Rent amount
    -   Number of bedrooms
    -   A "View Details" button link to the full Rental House Details page

## **Extra Sections**

-   -   **Testimonials:** Success stories from users who found their ideal rental.
    -   **Tips:** Advice on finding and renting the right house.

## **Footer**

-   -   **Contact Information:** Email, phone, and social media links.
    -   **Copyright:** Standard copyright details.
    -   **Additional Links:** Terms of Use, Privacy Policy, etc.

## **Login & Registration**

### **Login Form**

-   -   **Fields:**
        -   Username or email address
        -   Password

### **Registration Form**

-   -   **Fields:**
        -   Username
        -   Email address
        -   Password (with confirmation)
        -   **User Role:** Choose either **Landlord** or **Tenant** via a radio button or select input

## **Post Rental House Info (Private Route – Landlord Only)**

-   -   **Purpose:** Allow Landlords to submit new rental house listings.
    -   **Form Fields:**
        -   Rental house location
        -   Detailed description
        -   Rent amount
        -   Multiple image
        -   Number of bedrooms
        -   Amenities
    -   **Submit Button:** To post the listing for review and display.

## **Rental House Details Page**

-   -   **Features:**
        -   Display detailed information about the rental house, including:
            -   Multiple image
            -   Detailed description
            -   Rent amount
            -   Number of bedrooms
            -   Amenities
            -   Exact location
        -   **Request Rental Button:** A button opens a modal with a text input for tenants to add move-in dates, rental duration, and special requirements to the Rental House Request.

## **Rental House Request Page (Private Route – Tenant Only)**

-   -   **Form Fields:**
        -   User’s contact information (auto-populated from profile)
        -   Text message field
        -   Checkbox for agreement to terms and conditions
    -   **Submit Button:** To send a rental house request.
    -   **Owner Response Workflow:**
        -   Once submitted, the Landlord can reviews the request.
        -   They can **Approve** or **Reject** the request.
            -   If **approved**, a payment option becomes visible to the tenant, and a phone number field is available for the landlord to provide further contact.
            -   If **rejected** the request status is updated to “Rejected".

## **Dashboard**

### **Dashboard Views by Role**

-   -   **Admin Dashboard:**
        -   Full control over user accounts and rental listings.
        -   **User Management:**
            -   View all user accounts.
            -   Activate/deactivate users.
            -   Edit user roles as necessary.
        -   **Rental House Management:**
            -   View, edit, or remove any rental house listing.
            -   Oversee listings posted by Landlords for quality and compliance.

-   -   **Landlord Dashboard:**
        -   Manage rental house posts:
            -   View a list of your posted listings.
            -   Edit or delete existing posts.
        -   View and respond to rental requests.
        -   Once the landloard approves the rental request, they will initiate a payment request that appears on the tenant's dashboard. The landlord also has the option to provide a phone number for further contact.

-   -   **Tenant Dashboard:**
        -   View submitted rental requests with custom text(move-in dates, rental duration etc), along with their status (pending, approved, rejected).
        -   When a rental request is approved, the tenant sees a payment option to finalize the rental and also receives the landlord's phone number for further contact.

### **Common Profile Features**

-   -   **Edit Profile:** Options to update username, email, and other details.
    -   **Change Password:** Link to a dedicated change password page.

## **Change Password Page**

-   -   **Fields:**
        -   Current password
        -   New password (with confirmation)
    -   **Functionality:** Securely update the user’s password after proper validation.

## **About Us**

-   -   **Content Sections:**
        -   **Mission Statement:** Explain the purpose and vision behind BasaFinder.
        -   **Team Information:** Introduce the team behind the platform.
        -   **Contact Information:** Provide email, phone, and social media details.

----------

## **Frontend Requirements**

### **User Registration & Authentication**

-   -   **Custom Authentication:**
        -   Use JWT for secure Registration and Login.
        -   Validate inputs (e.g. proper email format, strong password criteria).

### **Routing and Public/Private Pages**

#### **Public Routes:**

-   -   Home Page (Landing)
    -   About Us
    -   FAQ, Terms & Conditions, Privacy Policy, and News pages

#### **Private Routes:**

-   -   **Admin Dashboard:** For administrative tasks.
    -   **Landlord Dashboard:** For managing rental posts and requests.
    -   **Tenant Dashboard:** For tracking rental requests.
    -   **Add Rental House:** Accessible only to Landlords.
    -   **Rental House Request Page:** Accessible Only to Tenants **(**Only logged-in users can request a rental property).

## **User Roles & Access Control**

-   -   **Admin:**
        -   Full control over user accounts and rental listings.
        -   Can edit or remove any listing or user.
    -   **Landlord:**
        -   Can post, edit, and delete their own rental listings.
        -   Can review and act upon rental requests (approve or reject).
    -   **Tenant:**
        -   Can search for rental houses.
        -   Can submit rental requests.
        -   Can track the status of their requests.

----------

### **UI/UX Design:**

-   -   Create a responsive, mobile-friendly UI using Next.js, ensuring a smooth experience across all devices.
    -   The design should be visually appealing and user-friendly.
    -   Follow design guidelines and best practices to maintain consistency.

----------

## **Backend Requirements:**

**The provided collections are examples only. You may add new collections or remove/edit existing ones as necessary to best suit your project's requirements.**

#### **Database Collections (MongoDB):**

1.  1.  **Users Collection**:
        -   **Fields**: `name`, `email`, `phone number`, `password (hashed)`, `role (admin, landlord, tenant)`, and any other necessary details.
        -   Store user credentials and roles for **authentication** and **authorization**.
    2.  **Listings Collection (Rental Houses):**
        -   **Fields**: `rental house location`, `details description`, `rent amount`, `number of bedrooms`, `multiple images`, `landlord ID (to link with the users collection)` , and any other necessary details.
        -   Store details of each rental house listing submitted by Landlords.
    3.  **Requests Collection (Rental Requests):**
        -   **Fields**: `rental house (listing) ID`, `tenant ID (to identify the requesting user)`, `status(pending, approve, reject)`, `(Upon approval) landlord’s phone number for direct contact`, `payment status (for approved requests)`, additional message or information provided by the tenant
        -   Track all rental requests submitted by Tenants and the corresponding responses by Landlords.

#### **Authentication:**

-   -   Use **JWT** for handling user sessions securely.
    -   Implement **bcrypt** for password hashing to store passwords securely.
    -   **Custom middleware** for protected routes to ensure that only authorized users (admins, landlords, and tenants) can access their respective dashboards and endpoints.

#### **CRUD Operations:**

**The provided routes are examples only. You may add new routes or remove/edit existing ones as necessary to best suit your project's requirements.**

-   -   **For Tenants:**
        -   `**POST** /tenants/requests:` Create a new rental request for a house.
        -   `**GET** /tenants/requests:` Retrieve all rental requests submitted by the tenant.
        -   `**PUT** /tenants/profile:` Update tenant profile.

-   -   **For Landlords:**
        -   `**POST** /landlords/listings:` Create a new rental house listing.
        -   `**GET** /landlords/listings:` Retrieve all rental listings posted by the landlord.
        -   `**PUT** /landlords/listings/:id:` Update a specific rental listing.
        -   `**DELETE** /landlords/listings/:id:` Remove a rental listing.
        -   `**GET** /landlords/requests:` Retrieve all rental requests for the listings posted by the landlord.
        -   `**PUT** /landlords/requests/:id:`
            -   Respond to a rental request by approving or rejecting it.
            -   **If approved:** The payment process initiate and a simple input field appears for the landlord to enter their phone number. This number is saved and made available to the tenant.

-   -   **For Admin:**
        -   `**GET** /admin/users:` Retrieve all user(tenants, landlords) accounts.
        -   `**PUT** /admin/users/:id:` Update user roles.
        -   `**DELETE** /admin/user/:id:` Delete user.
        -   `**GET** /admin/listings:` Retrieve all rental house listings.
        -   `**PUT** /admin/listings/:id:` Update or moderate a rental listing.
        -   `**DELETE** /admin/listings/:id:` Remove a rental listing if necessary.

----------

### **Additional Features:**

1.  1.  **Tenant Rental Request Text:**
        -   Tenants can write a text detailed while ask for rental request including move-in dates, rental duration, and any special requirements
    2.  **Search and Filter:**
        -   Tenants can **search for rental houses** based on location, rent range, number of bedrooms.
    3.  **Email Notifications**:
        -   **For Tenants: Email notifications** when rental requests are updated
        -   **For Landlords: Email notifications** when a new rental request is submitted.
    4.  **Role-Based Access**:
        -   Tenants and Landlords will have different roles, with access to their relevant sections (listings, requests, dashboard).

----------

### **Submission Guidelines:**

1.  1.  **Codebase**:
        -   Submit a well-structured, clean, and documented codebase.
        -   Ensure that the code follows best practices (modular backend, clean components, and reusable code).
        -   Include a **README** file with detailed setup instructions, project overview, technology stack, live URL, and any other relevant information.
    2.  **GitHub Repository**:
        -   Provide separate GitHub repositories for the front end and back end.
        -   Ensure there’s a **commit history** that demonstrates your development process.
    3.  **Live Deployment**:
        -   Provide live deployment URLs for both frontend and backend.
    4.  **Demo Video**:
        -   Create a short demo video highlighting the main features, including user registration, login, CRUD operations, and the admin dashboard.
    5.  **Admin Credentials**:
        -   Provide admin credentials (email and password) to access the admin dashboard.

----------

### **Timeline & Marks:**

-   **Full Submission (60 Marks)**: Due by **March 06, 2025, 11:59 PM**.
-   **Late Submission (50 Marks)**: Due by **March07, 2025, 11:59 PM**.
-   **Late Submission with Penalty (30 Marks)**: Due by **March 07, 2025, 11:59 PM**.

----------

### **Important Note:**

-   -   Plagiarism will not be tolerated. Your work must be original.
    -   Any plagiarism detected will result in **0 Marks**.

Good luck with your assignment! Let me know if you need further assistance!