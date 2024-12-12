# EzyLearn-LearingPlatform

**EzyLearn is an innovative online learning platform designed to empower learners and educators. It allows users to register, enroll in courses, and manage their learning journey, while publishers and admins can create and manage courses, track enrollments, and manage user accounts. Built using modern web technologies, EzyLearn offers a seamless and secure learning experience for everyone.**

## **Author: Badal Kumar Behera**

## Backend

**The Backend of the EzyLearn platform is built using Node.js, Express, and follows the MVC architecture pattern with Repository and Service layers. It handles all operations related to users, courses, and enrollments.**

---

### Model

#### userModel

- Represents user data (name, email, role, etc.).
- Used for authentication and authorization.

#### courseModel

- Represents course data (title, description, lessons, etc.).
- Allows course creation, updates, and deletion.

#### enrolledCourseModel

- Manages the relationship between users and courses (enrollment status).

---

### Routes and Operations

#### User Routes

- GET /getallusers: Get details of all users (protected route, requires authentication).
- POST /refresh: Refresh the user's session token (protected route, requires authentication).
- POST /register: Register a new user (public route).
- POST /login: Login for a user (public route).
- POST /logout: Log out the user (public route).
- GET /deleteuser/:id: Delete a user by ID (protected route, requires authentication).
- POST /updateuser/:id: Update user details (protected route, requires authentication).
- POST /getuser/:email: Get details of a user by email (public route).

#### Course Routes

- POST /create-course: Create a new course (protected route, requires authentication).
- POST /create-enrolled-course: Enroll a user in a course.
- GET /getallcourses: Get all courses (public route).
- GET /deletecourse/:id: Delete a course by ID (protected route, requires authentication).
- POST /getcourse/:id: Get course details by ID (public route).
- GET /getmycourse/:id: Get course information for a specific user.
- GET /getenrolledcourses/:id: Get all courses a user is enrolled in.

---

### Authentication & Authorization

- JWT Authentication: Tokens are used for securing routes.
- Protected Routes: Certain routes like course creation, updates, and deletions are protected and can only be accessed by authorized users, typically admins.

---

## Frontend

**The Frontend of EzyLearn is built using React.js. It provides user-friendly interfaces for both normal users and admin users to manage their courses, enrollments, and account details.**

---

### Pages

#### User and Publisher Pages

- Register Page: Allows new users to sign up.
- Login Page: Allows users to log in and authenticate.
- Create Course Page: Allows publishers to create and publish courses.
- Enrolled Courses Page: Displays courses the user is enrolled in.

#### Admin Pages

- Admin Dashboard: Allows admins to view all users and courses.
- User Management: Admins can delete or update user details.
- Course Management: Admins can delete or update courses, and add other admins.

---

### Protected Routes

**Certain pages like creating, updating, or deleting courses, and managing users, are protected and accessible only to admins.**
