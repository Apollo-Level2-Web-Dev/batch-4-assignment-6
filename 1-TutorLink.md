# TutorLink 🎓 (Find & Connect with the Best Tutors) B4A6V1

### **Project Overview:**

You are tasked with developing a **Tutor-Student Connection Web Application** where students and tutors can easily connect with each other. The platform should allow students to find and connect with tutors, and tutors to respond to students’ requests, based on the subject needs and available schedules.

### **Key Features:**

1.  **User Authentication**:
    -   Custom login system for **students** and **tutors** using email or phone number and password.
    -   Use of **JWT** (JSON Web Tokens) for authentication, ensuring secure login.
    -   Password hashing using **bcrypt** for added security.
2.  **Student and Tutor Dashboards**:
    -   Students and tutors will have **separate dashboards**.
    -   **Student Dashboard**: For posting requests, viewing responses from tutors, and tracking requests.
    -   **Tutor Dashboard**: For managing profile details, responding to student requests, and managing availability.
3.  **Post a Request**:
    -   Students can post a **request for tutors** specifying subjects and preferred time slots.
    -   Tutors can create and update their **profiles**, listing subjects they teach, available time slots, experience, and hourly rate.
4.  **Search and Match**:
    -   **Students** can search for tutors based on subject expertise, ratings, and availability.
    -   **Tutors** can view student requests and respond if the request matches their profile.
5.  **Role-Based Access Control**:
    -   Different **routes** and **views** for students and tutors, each with access to platform-specific features.
    -   Admin access (if implemented) will be used to manage users and content.
6.  **CRUD Operations**:
    -   Students can **create**, **view**, and **update** their requests.
    -   Tutors can **view**, and **respond** to student requests.

----------

### **Tech Stack:**

-   **Frontend**:
    -   **Next.js** (for SSR/SSG)
    -   **TypeScript** for type safety
    -   **React** for building user interfaces
-   **Backend**:
    -   **Node.js** with **Express** for REST APIs
    -   **MongoDB** for storing data (users, tutor profiles, student requests)
    -   **JWT** for authentication
    -   **bcrypt** for password hashing
-   **Deployment**:
    -   **Frontend**: Vercel, Netlify, or similar
    -   **Backend**: Heroku, AWS, or similar

----------

### **Frontend Requirements:**

#### **Routes for Students:**

1.  **Home Page (**`**/**`**)**:
    -   An overview of the platform and its benefits for students.
    -   Introduction to how students can find tutors.
2.  **Login Page (**`**/login**`**)**:
    -   Students can log in using their **email/phone number** and **password**.
3.  **Student Dashboard (**`**/dashboard/student**`**)**:
    -   **Post a Request**: Students can post tutor requests specifying subjects and preferred times.
    -   **View Tutors**: View available tutors based on the student's request.
    -   **Request History**: View history of all their posted requests and responses from tutors.
4.  **Student Profile (**`**/profile/student**`**)**:
    -   Students can **edit personal details** (name, email, phone number, etc.).
5.  **Find Tutors (**`**/find-tutors**`**)**:
    -   Students can **search for tutors** by subject, rating, availability, or location.
6.  **Post a Request (**`**/request-tutor**`**)**:
    -   Students can **post a tutor request**, including subject, schedule, and any other requirements.

#### **Routes for Tutors:**

1.  **Home Page (**`**/**`**)**:
    -   Overview of the platform, benefits, and how tutors can post profiles and respond to students.
2.  **Login Page (**`**/login**`**)**:
    -   Tutors log in using **email/phone number** and **password**.
3.  **Tutor Dashboard (**`**/dashboard/tutor**`**)**:
    -   **View Student Requests**: Tutors can view a list of requests posted by students.
    -   **Manage Profile**: Tutors can manage their profile and update availability.
    -   **Respond to Requests**: Tutors can respond to student requests by confirming or declining.
4.  **Tutor Profile (**`**/profile/tutor**`**)**:
    -   Tutors can **edit their profile**, specifying subjects they teach, available times, experience, and hourly rates.
5.  **Post Tutor Profile (**`**/post-tutor-profile**`**)**:
    -   Tutors can post a detailed profile for students to view, including subjects taught, experience, rates, etc.
6.  **Responses (**`**/responses**`**)**:
    -   Tutors can **respond to student requests**, either confirming availability or explaining why they can’t assist.

----------

### **Backend Requirements:**

#### **Database Collections (MongoDB)**:

1.  **Users Collection**:
    -   **Fields**: Name, email, phone number, password (hashed), role (student or tutor), and any other necessary details.
    -   Store user credentials and roles for **authentication** and **authorization**.
2.  **Requests Collection**:
    -   **Fields**: Subject, preferred times, student ID, status (open, closed, in-progress).
    -   Track all **student requests** for tutors.
3.  **Tutors Collection**:
    -   **Fields**: subjects, availability, hourly rate, experience, student reviews, etc.
    -   Store **tutor profiles** that students can view.

#### **Authentication**:

-   Use **JWT** for handling user sessions securely.
-   Implement **bcrypt** for password hashing to store passwords securely.
-   **Custom middleware** for protected routes to ensure that only authorized users (students and tutors) can access their respective dashboards.

#### **CRUD Operations**:

-   **Students**:
    -   **POST** `/students/request`: Create a new student request for a tutor.
    -   **GET** `/students/requests`: Retrieve all requests posted by the student.
    -   **PUT** `/students/profile`: Update student profile.
-   **Tutors**:
    -   **POST** `/tutors/profile`: Tutors can create or update their profile.
    -   **GET** `/tutors/requests`: Retrieve all requests posted by students.
    -   **PUT** `/tutors/response`: Tutors can respond to student requests.

----------

### **UI/UX Design**:

-   **Responsive Design**: The platform should be mobile-friendly, providing an optimized experience for all device sizes.
-   **Modern UI/UX**: Focus on simple navigation, clear calls to action, and easily accessible features.
-   **User-friendly Interface**: Easy-to-use forms for posting requests and profiles, search filters, and notifications.

----------

### **Additional Features:**

1.  **Student Request Posting**:
    -   Students can post a **detailed request** including the subject, preferred tutor rating, and time availability.
2.  **Tutor Profile Posting**:
    -   Tutors can **create and update profiles**, which include information on subjects taught, experience, hourly rates, and availability.
3.  **Search and Match**:
    -   Students can **search tutors** based on subjects, ratings, and availability. Tutors can also search for student requests to respond to.
4.  **Email Notifications**:
    -   **For Students**: **Email** when tutors respond to their requests.
    -   **For Tutors**: **Email** when a new request matches their profile.
5.  **Role-Based Access**:
    -   Students and tutors will have different roles, with access to their relevant sections (requests, profiles, dashboard).

----------

### **Deployment:**

-   **Frontend**: Deploy using **Vercel** or similar platforms.
-   **Backend**: Deploy using **Vercel**, or similar platforms.

----------

### **Submission Guidelines:**

1.  **Codebase**:
    -   A clean, well-organized, and well-documented codebase following best practices.
2.  **GitHub Repositories**:
    -   Separate repositories for **frontend** and **backend**.
    -   Ensure a **commit history** that reflects your development process.
3.  **Live Deployment**:
    -   Provide **live URLs** for both frontend and backend.
    -   Make sure that everything works seamlessly in the deployed version.
4.  **Demo Video**:
    -   A short video demonstrating:
        -   User registration/login.
        -   Posting a request (student).
        -   Posting a profile (tutor).
        -   Searching for tutors (student).
        -   Responding to requests (tutor).

----------

### **Timeline & Marks:**

-   **Full Submission (60 Marks)**: Due by **March 06, 2025, 11:59 PM**.
-   **Late Submission (50 Marks)**: Due by **March07, 2025, 11:59 PM**.
-   **Late Submission with Penalty (30 Marks)**: Due by **March 07, 2025, 11:59 PM**.

----------

### **Important Notes**:

-   **Plagiarism**: Must be original work. Any plagiarism detected will result in 0 Marks.
-   **Simplicity**: The project should focus on building a **functional** platform with specified features, not be overly complex or too simple.

Good luck! Let me know if you need any further clarification!