# TutorLink 🎓: Assignment Brief  
**Find & Connect with the Best Tutors**  

---

## **Project Overview**  
Build a platform where students can discover tutors, book sessions, and manage their learning journey. Tutors can create profiles, list subjects, and manage availability. Admins (if implemented) oversee users, tutor approvals, and platform content.  

---

## **Core Features**  
### **Frontend Requirements**  
#### **User Roles**  
1. **Student**: Browse tutors, book sessions, view history.  
2. **Tutor**: Create profiles, set availability, manage bookings.   

#### **Public Routes**  
- Here’s a brief description for each of the **Public Routes** pages in your project, **TutorLink 🎓 (Find & Connect with the Best Tutors)**:

**1. Home Page**
- **Overview**: The landing page introduces users to the platform and its core services.
- **Features**:
  - A **hero section** with a prominent search bar allowing users to search for tutors by subject, grade, or tutor name.
  - Highlight key features like "Find Tutors Fast," "Secure Payments," and "Verified Profiles."
  - Include testimonials or success stories from students and tutors.
  - Call-to-action buttons like "Sign Up as a Student" or "Register as a Tutor."

**2. Browse Tutors**
- **Overview**: A dynamic page where users can explore available tutors based on filters.
- **Features**:
  - **Filter Options**: Users can filter tutors by subject, rating, hourly rate, availability, and location.
  - **Sort Options**: Sort tutors by relevance, rating, price (low to high or high to low), or newest profiles.
  - Display tutor cards with key details: profile picture, name, subjects taught, hourly rate, and average rating.

**3. Tutor Profile**
- **Overview**: A detailed page showcasing an individual tutor's information.
- **Features**:
  - **Bio**: A short introduction about the tutor, including qualifications and teaching philosophy.
  - **Subjects Taught**: List of subjects and grades the tutor specializes in.
  - **Rates**: Hourly rate and any discounts for bulk hours.
  - **Reviews**: Ratings and feedback from previous students.
  - **Booking Calendar**: Availability calendar for scheduling sessions.
  - **Call-to-Action**: Button to request tutoring or contact the tutor.

**4. About Us**
- **Overview**: Provides insight into the platform's mission, values, and team.
- **Features**:
  - **Mission Statement**: Explain the platform's goal to connect students with qualified tutors.
  - **Team**: Introduce the founders or core team behind the platform.
  - **Success Stories**: Share real-life examples of how the platform has helped students and tutors succeed.
  - **Vision**: Outline future plans for the platform (e.g., expanding subjects, global reach).

**5. FAQ**
- **Overview**: Answers frequently asked questions about the platform and its services.
- **Features**:
  - **Categories**: Organize FAQs into sections like "Tutoring," "Payments," "Account Management," etc.
  - **Common Questions**:
    - How do I find a tutor?
    - How are payments processed?
    - Can I cancel a session?
    - What if I’m not satisfied with my tutor?

**6. News/Blog (You can use any open source blog/news API)**
- **Overview**: A resource hub for educational tips, industry news, and platform updates.
- **Features**:
  - **Educational Tips**: Articles on study techniques, exam preparation, and learning strategies.
  - **Platform Updates**: Announcements about new features or improvements.
  - **Industry News**: Insights into trends in education and tutoring.
  - **Search Bar**: Allow users to search for specific topics or articles.

#### **Private Routes**  
- **Student Dashboard**:
  - Manage profile.
  - Past bookings, payment history.  
  - Review tutors.  
- **Tutor Dashboard**:  
  - Manage profile, booking requests, earnings.  
  - Subject management, Availability slots.  
- **Checkout Page**: Secure payment for booking tutor.
- **Step-by-Step Payment Process**:
   1. **Tutor Confirms Request**: Once a tutor accepts a student’s request, the student is notified.
   2. **Student Chooses Payment Duration**: The student selects the number of months and hours they wish to hire the tutor.
   3. **Calculate Total Payment**: The backend calculates the total cost based on the tutor’s hourly rate and selected hours.
   4. **Payment Processing**: The frontend securely handles the payment through **SSLCommerz, Stripe, or PayPal**.
   5. **Tutor's Earnings Updated**: Once the payment is processed, the tutor’s earnings are updated on their dashboard. 

#### **UI/UX**  
- **Responsive Design**: Optimized for all devices.  
- **Interactive Elements**: Interactive design, color combination, typography, etc.  
- **Theming**: Education-focused (icons, colors, illustrations).  

---

## **Backend Requirements**  
### **Database Collections (You can modify as you want)**  
1. **Users**  
   - Roles: `student`, `tutor`.  
   - Fields: Bio, subjects, availability (tutors), ratings, etc.  
2. **Subjects**  
   - Fields: Name (e.g., "Algebra"), grade level, category, etc.  
3. **Bookings**  
   - Linked to `user` (student) and `tutor`.  
   - Fields: Date/time, duration, price, status (`pending`, `completed`, `canceled`), etc.  
4. **Reviews**  
   - Linked to `tutor` and `student`.  
   - Fields: Rating, comment, timestamp, etc.  

### **Key Modules**  
1. **Auth**: JWT-based login/registration, role checks.  
2. **Tutor**: CRUD for profile, availability, and subjects.  
3. **Booking**: Booking creation, payment handling, status updates.  
4. **Review**: Posting ratings, calculating tutor averages.  

### **Payment Integration**  
- **SSLCommerz/Stripe**: Handle payments using any popular payment method.  

### **Advanced Features (Optional)**  
- **Tutor Application Form**: Users apply to become tutors (admin approval required).  
- **Calendar Sync**: Integrate Google Calendar for tutor availability.  
- **Live Chat**: Socket.io for student-tutor messaging.  

---

## **Tech Stack**  
### **Frontend**  
- **Next.js 15** (SSR/SSG for SEO-friendly pages like blog).  
- **TypeScript** + **Tailwind CSS** (styling).    

### **Backend**  
- **Node.js/Express** (REST API with modular routes).  
- **MongoDB/Mongoose** (data modeling).  
- **JWT** + **bcrypt** (secure auth).  

---

## **Submission Requirements**  
1. **Codebase**:  
   - Modular backend (split into `auth`, `tutor`, `booking`, `review`).  
   - Clean, reusable React components (e.g., `RatingStars`, `BookingCard`).  
2. **Deployment**:  
   - Frontend: Vercel.  
   - Backend: Render/Vercel.  
   - MongoDB: Atlas.  
3. **Demo Video**:  
   - Show student/tutor registration, booking flow, tutor and student dashboard.  

