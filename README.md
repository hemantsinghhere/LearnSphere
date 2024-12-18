# LearnSphere Ed-Tech Platform

LearnSphere is a versatile and intuitive ed-tech platform that enables users to create, consume, and rate educational content. It provides a seamless and interactive learning experience for students while offering a platform for instructors to showcase their expertise and connect with learners worldwide. The platform is built using the MERN stack, which includes ReactJS, NodeJS, MongoDB, and ExpressJS.

![My Image](https://drive.google.com/uc?export=view&id=1z1YDgOqtNjhrQntvEn-YRFrBx8lY5ct5 "My Image from Google Drive")

## System Architecture
The LearnSphere ed-tech platform follows a client-server architecture with the following main components:
- **Front-end:** Built with ReactJS, it communicates with the back end using RESTful API calls.
- **Back-end:** Developed with NodeJS and ExpressJS, it handles user authentication, course management, and more.
- **Database:** Utilizes MongoDB as a NoSQL database to store course content, user data, and other relevant information.

### Architecture Diagram
![My Image](https://drive.google.com/uc?export=view&id=1jZkgLWHo5b8xD4AwMQ1Q3NrQHzkXSLIj "My Image from Google Drive")

## Frontend

The front end of LearnSphere is built with ReactJS, offering a dynamic and responsive user interface for students and instructors. Here are some key pages and functionalities:

For Students:

- Homepage: Introduction to the platform.
- Course List: List of available courses with descriptions and ratings.
- Wishlist: Display added courses.
- Cart Checkout: Complete course purchase using Razorpay.
- Course Content: Access course material, including videos.
- Enrolled Courses: Progress and list of enrolled courses.
- User Details: Account information.
- User Edit Details: Edit account information.

For Instructors:

- Dashboard: Overview of instructor's courses and ratings.
- Insights: Detailed course including the number of views, clicks, and other relevant metrics.
- Course Management Pages: Create, update, delete courses.
- View and Edit Profile Details: Account management.

Front-end tools and technologies include ReactJS, CSS, Tailwind CSS, Redux for state management, and VSCode for development. Additionally, we use some npm packages to add extra functionality to the front end.

## Backend

The back end of LearnSphere is built with NodeJS and ExpressJS and uses MongoDB as its primary database. Key features and functionalities include:

- User Authentication and Authorization: Secure login, OTP verification, and forgot password functionality.
- Course Management: Instructors can create, update, delete courses, and students can view and rate them.
- Payment Integration: Razorpay integration for course purchases.
- Cloud-based Media Management: Cloudinary for storing and managing media content.
- Markdown Formatting: Course content is stored in Markdown format for rendering.
Frameworks, libraries, and tools used: Node.js, MongoDB, Express.js, JWT for authentication and authorization, Bcrypt for password hashing, and Mongoose for database interaction.

### Data Models and Database Schema
![My Image](https://drive.google.com/uc?export=view&id=19X0SDmnwye4GXZ8JnkBom4QbPMGGhKy6 "My Image from Google Drive")


- Student Schema: Includes name, email, password, and course details.
- Instructor Schema: Includes name, email, password, and course details.
- Course Schema: Includes course name, description, instructor details, and media content.

## API Design

The LearnSphere platform's API is designed following the REST architectural style. The API is implemented using Node.js and Express.js. It uses JSON for data exchange and follows standard HTTP request methods such as GET, POST, PUT, and DELETE.

**Here is list of API endpoints:**

- POST /api/auth/signup: Create a new user account.
- POST /api/auth/login: Log in and generate a JWT token.
- POST /api/auth/verify-otp: Verify OTP sent to the user's email.
- POST /api/auth/forgot-password: Send a password reset link.
- GET /api/courses: Get a list of all available courses.
- GET /api/courses/:id: Get details of a specific course.
- POST /api/courses: Create a new course.
- PUT /api/courses/:id: Update an existing course.
- DELETE /api/courses/:id: Delete a course.
- POST /api/courses/:id/rate: Add a course rating (out of 5).

Sample API requests and responses:

- GET /api/courses: Get all courses
- Response: A list of all courses in the database
- GET /api/courses/:id: Get a single course by ID
- Response: The course with the specified ID
- POST /api/courses: Create a new course
- Request: The course details in the request body
- Response: The newly created course
- PUT /api/courses/:id: Update an existing course by ID
- Request: The updated course details in the request body
- Response: The updated course
- DELETE /api/courses/:id: Delete a course by ID
- Response: A success message indicating that the course has been deleted.

#### This infrastructure ensures scalability, security, and reliability.

### Installation

1. Clone the repository: `git clone https://github.com/username/repo.git`
2. Navigate to the project directory: `cd LearnSphere`
3. Install dependencies: `npm install`

### Configuration
1. Set up a MongoDB database and obtain the connection URL.
2. Create a `.env` file in the root directory with the following environment variables

```
# Nodemailer Credentials
MAIL_HOST = "smtp.gmail.com"
MAIL_USER = "Your_Gmail_Account"
MAIL_PASS = "Your_Gmail_Pass"


JWT_SECRET = "your_secret_key"
FOLDER_NAME = "LearnSphere"

#  Razorpay
RAZORPAY_KEY = your_razorpay_key
RAZORPAY_SECRET = your_razorpay_secret

# MongoDB 
MONGODB_URL = "your_connection_string"
PORT = 4000  // Backend is running on port 4000 


#  Cloudinary 
CLOUD_NAME = cloudinary's_cloud_name
API_KEY = your cloudinary_API_Key
API_SECRET = your_cloudinary_API_Secret

```

### Usage
1. Start the server: `npm start`
2. Open a new terminal and navigate to the client directory: `cd client`
3. Start the React development server: `npm start`

Access the application in your browser at `http://localhost:3000`.

