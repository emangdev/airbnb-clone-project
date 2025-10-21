# Airbnb Clone Backend

## Project Overview
- **Goals**: Build a scalable, secure backend for a vacation rental platform with user management, property listings, bookings, and payments.
- **Tech Stack**: Python, Django, TypeScript, PostgreSQL.

## Team Roles
- **Business Analyst (BA)**: Analyzes client needs, translates them into technical requirements.
- **Product Owner (PO)**: Defines product vision, ensures alignment with client needs.
- **Project Manager (PM)**: Oversees timely delivery, manages budget and team.
- **UI/UX Designer**: Designs intuitive interfaces, optimizes user experience.
- **Software Architect**: Creates scalable architecture, selects tools, enforces code quality.
- **Software Developer**: Builds and stabilizes backend, resolves technical issues.
- **QA Engineer**: Verifies functionality, identifies defects.
- **Test Automation Engineer**: Develops automated testing scripts, maintains test ecosystem.
- **DevOps Engineer**: Implements CI/CD pipelines, streamlines development-operations.

## Technology Stack
- **Django**: Web framework for building RESTful APIs and handling backend logic.
- **Python**: Core programming language for backend development.
- **TypeScript**: Enhances frontend-backend integration with type-safe APIs.
- **PostgreSQL**: Relational database for storing user, property, and booking data.

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
- **User Management**: Register, login, manage profiles. Enables secure access and personalization.
- **Property Management**: Create, update, delete listings. Core to platform’s rental functionality.
- **Booking System**: Book properties, check availability. Drives core user interaction.
- **Review System**: Submit, view ratings and comments. Builds trust and transparency.
- **Payment Processing**: Securely handle transactions. Ensures reliable financial operations.

## API Security
- **Authentication**: JWT for user verification, protecting endpoints.
- **Authorization**: Role-based access to restrict actions (e.g., only owners manage listings).
- **Rate Limiting**: Prevent abuse, ensure API stability.
- **Importance**: Secures user data, protects payments, maintains platform trust.

## CI/CD Pipeline
- **Definition**: Automated processes for code integration (CI) and deployment (CD).
- **Importance**: Ensures fast, reliable delivery with minimal errors.
- **Tools**: GitHub Actions for automation, Docker for containerized deployments.
