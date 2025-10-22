# Airbnb Clone Backend

## Project Overview
- **Goals**:
1. Learn building scalable server-side applications by building an airbnb clone.
2. Understand how to secure backend systems and server side applications.
3. Impliment a secure system for user registration, authentication and profile management.
4. Impliment features for property management - listings, updates and retrieval.
5. Intergrate payment system to handle transactions and record payment details.
6. Impliment the booking mechanism for users to reserve properties and manage booking details.
7. Impliment allows users to leave reviews and property ratings.
     
## Team Roles
- **Business Analyst (BA)**: Works on analyzing client needs and  translates them into technical requirements.
- **Database Administrator**: Manages database design, indexing, and optimizations.
- **Product Owner (PO)**: Responsible for defining product vision and ensures alignment with client needs.
- **Project Manager (PM)**: Responsible for ensuring timely delivery and also manages the project budget and team.
- **UI/UX Designer**: Responsible for designing intuitive interfaces and optimization of user experience.
- **Software Architect**: Creates scalable architecture, selects tools and enforces code quality.
- **Software Developer**: Responsible for building and stabilizing the backend and resolving any technical issues that arises with the product.
- **QA Engineer**: Tasked with verifying functionality and identifies defects in the products code.
- **Test Automation Engineer**: Responsible for developing automated testing scripts and maintain the testing ecosystem.
- **DevOps Engineer**: Implements CI/CD pipelines and  streamlines development-operations.

## Technology Stack
- **Django**: A web framework for building RESTful APIs and handling the backend logic.
- **Django REST Framework**: Provides tools for creating and managing RESTful APIs.
- **GraphQL**: Allows for flexible and efficient querying of data.
- **Python**: Core programming language for my backend development.
- **Celery**: For handling asynchronous tasks such as sending notifications or processing payments.
- **Redis**: Used for caching and session management.
- **TypeScript**: Used to enhance frontend-backend integration with type-safe APIs.
- **PostgreSQL**: Relational database for storing user, property, and booking data.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

## Database Design
- **Entities and Fields**:
  - **Users**: `id`, `email`, `password_hash`, `name`, `role`.
  - **Properties**: `id`, `owner_id`, `title`, `location`, `price_per_night`.
  - **Bookings**: `id`, `property_id`, `user_id`, `check_in`, `check_out`.
  - **Reviews**: `id`, `property_id`, `user_id`, `rating`, `comment`.
  - **Payments**: `id`, `booking_id`, `amount`, `status`, `payment_date`.
- **Relationships**:
  - One `User` can own multiple `Properties` (one-to-many).
  - One `Property` can have multiple `Bookings` and `Reviews` (one-to-many).
  - One `Booking` links to one `Property` and one `User` (many-to-one).
  - One `Payment` links to one `Booking` (one-to-one).

## Feature Breakdown
- **User Management**:
  Endpoints: /users/, /users/{user_id}/
  Features: Register new users, authenticate, and manage user profiles.
- **Property Management**:
  Endpoints: /properties/, /properties/{property_id}/
  Features: Create, update, retrieve, and delete property listings.
- **Booking System**:
  Endpoints: /bookings/, /bookings/{booking_id}/
  Features: Make, update, and manage bookings, including check-in and check-out details.
- book properties, check availability. Drives core user interaction.
- **Review System**:
- Submit, view ratings and comments. Builds trust and transparency.
  Endpoints: /reviews/, /reviews/{review_id}/
  Features: Post and manage reviews for properties.
- **Payment Processing**:
- Securely handle transactions. Ensures reliable financial operations.
  Indexing: Implement indexes for fast retrieval of frequently accessed data.
  Caching: Use caching strategies to reduce database load and improve performance.

## API Security and documentation overview
- **Authentication**: JWT for user verification, protecting endpoints.
- **Authorization**: Role-based access to restrict actions (e.g., only owners manage listings).
- **Rate Limiting**: Prevent abuse, ensure API stability.
- **Importance**: Secures user data, protects payments, maintains platform trust.#
- **REST API**: Detailed documentation available through the OpenAPI standard, including endpoints for users, properties, bookings, and payments.
- **GraphQL API**: Provides a flexible query language for retrieving and manipulating data.

## CI/CD Pipeline
- **Definition**: Automated processes for code integration (CI) and deployment (CD).
- **Importance**: Ensures fast, reliable delivery with minimal errors.
- **Tools**: GitHub Actions for automation, Docker for containerized deployments.
