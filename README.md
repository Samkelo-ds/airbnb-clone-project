# airbnb-clone-project
A scalable Django-based backend that replicates core Airbnb functionalities — including user authentication, property listings, bookings, payments, and reviews. Features REST &amp; GraphQL APIs, PostgreSQL, Redis caching, Celery tasks, and Dockerized deployment.
## 👥 Team Roles

This project is a team effort! Here are the important roles and what they do:

### 🧠 Backend Developer
Builds the brains of the app — the APIs that let users sign up, list properties, book, pay, and more.

### 🗄️ Database Administrator (DBA)
Takes care of the data — they design, organize, and make sure everything saves safely and loads fast.

### 🔧 DevOps Engineer
Makes sure the app runs smoothly online. They handle deployments, updates, and monitoring.

### 🧪 QA Engineer (Quality Assurance)
Checks everything — they test the system to catch bugs and make sure everything works as expected.
Technology Stack
## 🛠️ Technology Stack

Here are the main tools and technologies used to build the Airbnb Clone backend, along with what they do:

### ⚙️ Django
A Python web framework used to build and manage the backend logic and API routes.

### 🌐 Django REST Framework (DRF)
Helps create RESTful APIs that allow users to interact with the backend (e.g., sign up, list properties).

### 🗃️ PostgreSQL
A powerful and reliable database used to store all the data — like user profiles, bookings, and payments.

### 🔎 GraphQL
A query language used for asking the backend only for the data you need — more flexible than traditional REST.

### ⏳ Celery
Used to handle background tasks like sending emails, notifications, or processing long-running jobs.

### ⚡ Redis
An in-memory data store used for caching (making things faster) and session management.

### 📦 Docker
Used to package the app into containers so it runs the same on every computer or server.

### 🚀 CI/CD Pipelines
Automated tools that help test, build, and deploy the app faster and safer.
## 🗄️ Database Design

The project uses a relational database (PostgreSQL) to store all important information. Here are the key entities and their relationships:

### 👤 Users
Stores information about people using the platform.
- `id`: Unique identifier for the user
- `name`: Full name of the user
- `email`: Email address (used for login)
- `password`: Encrypted password
- `role`: Indicates if the user is a guest or host

### 🏡 Properties
Holds details about places listed for rent.
- `id`: Unique property ID
- `owner_id`: References the user who owns the property
- `title`: Name of the property
- `location`: Address or area of the property
- `price_per_night`: Rental cost per night

### 📆 Bookings
Stores reservations made by users.
- `id`: Booking ID
- `user_id`: The guest who made the booking
- `property_id`: The property being booked
- `check_in_date`: Start of the stay
- `check_out_date`: End of the stay

### 💳 Payments
Stores payment details for bookings.
- `id`: Payment ID
- `booking_id`: The booking being paid for
- `amount`: Total payment amount
- `status`: Payment status (e.g., completed, pending)
- `payment_date`: When the payment was made

### ⭐ Reviews
Stores feedback left by users after a stay.
- `id`: Review ID
- `user_id`: User who wrote the review
- `property_id`: Property being reviewed
- `rating`: Score out of 5
- `comment`: Written feedback

---

### 🔗 Entity Relationships

- A **User** can own multiple **Properties**
- A **User** can make multiple **Bookings**
- A **Booking** belongs to one **User** and one **Property**
- A **Booking** can have one **Payment**
- A **Property** can have many **Reviews**
- A **User** can write many **Reviews**

  ## 🧩 Feature Breakdown

Here are the main features of the Airbnb Clone backend and what each one does:

### 👤 User Management
Users can register, log in, and manage their profiles securely. This feature ensures that users have personalized access and control over their data.

### 🏠 Property Management
Hosts can list their properties, including details like location, pricing, and availability. This enables users to browse and book places to stay.

### 📅 Booking System
Guests can make bookings for available properties by selecting check-in and check-out dates. The system manages reservation details and prevents double bookings.

### 💳 Payment Processing
Payments can be made securely for each booking. This feature records transactions and helps ensure both guests and hosts are protected.

### ⭐ Review System
After a stay, guests can leave reviews and ratings for the properties. This builds trust in the community and helps users make informed decisions.

### ⚡ API Access (REST & GraphQL)
The project supports both REST and GraphQL APIs for flexibility and efficiency. This allows developers to interact with the backend in different ways depending on their needs.

### 🚀 Performance Optimization
Indexing and caching are used to make the backend faster and more responsive. These optimizations improve the user experience by speeding up data access.
