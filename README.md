# Airbnb Clone Project

The **Airbnb Clone Project** is a full-stack web application inspired by Airbnb. It simulates the real-world development of a robust, scalable booking platform. The project emphasizes backend development, database design, API security, and CI/CD integration.

## 1. 👥 Team Roles

| **Role**                     | **Responsibilities**                                                                                             |
| ---------------------------- | -----------------------------------------------------------------------------------------------------------------|
| **Project Manager**          | Manages and motivates the software development team.                                                             |
| **DevOps Engineer**          | Builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery.                     |
| **QA Engineer**              | Makes sure an application performs according to requirements.                                                    |
| **Product Owner**            | Holds responsibility for a product vision, evolution & makes sure the final product meets customer requirements. |
| **Business Analyst**         | Understands customer’s business processes & translates customer business needs into requirements.                |
| **Software Architect**       | Designs a high-level software architecture.                                                                      |
| **Software Developer**       | Engineers and stabilizes the product.                                                                            |
| **Test Automation Engineer** | Designs a test automation ecosystem.                                                                             |
| **UI/UX Designer**           | Transforms a product vision into user-friendly designs.                                                          |

## 2. 🧰 Technology Stack

### 🔧 **Django**
 + A high-level Python web framework used for building the backend, authentication logic, views, and managing models.

### 🔗 **GraphQL**
 + A query language that allows clients to request the data they need, reducing over-fetching and improving performance.

### 🗄️ **MySQL**
 + A powerful relational database management system used to store user data.

### 🐳 **Docker**
 + Used for creating isolated and replicable development environments for both production and local setups.

### ⚙️ **GitHub Actions**
 + Automates testing, deployment processes and linting through workflows that trigger on repository events.

## 3. 🗃️ Database Design

### Key Entities

1. **Users**
   - `id`
   - `username`
   - `email`
   - `password`
   - `role` (host or guest)

2. **Properties**
   - `id`
   - `user_id`
   - `title`
   - `description`
   - `location`

3. **Bookings**
   - `id`
   - `property_id`
   - `user_id`
   - `check_in`
   - `check_out`

4. **Reviews**
   - `id`
   - `booking_id`
   - `rating`
   - `feedback`

5. **Payments**
   - `id`
   - `booking_id`
   - `amount`
   - `payment_mode`
   - `status`

   ### Entity Relationships

- A **User** can create multiple **Properties**.
- A **Booking** belongs to one **Property** and one **User**.
- A **Review** is linked to a **Booking**.
- A **Payment** is associated with a **Booking**.

## 4. 🧩 Feature Breakdown

### 👤 User management
  + This allows users to sign up, log in, and manage their profiles. Authentication is secured using JWT or OAuth2.

### 🏠 Property management
  + The hosts can create, update, and delete property listings. Includes support for pricing, and location.

### 📅 Booking system
  + Users can search for properties by date and location, then book them. Booking dates are validated to prevent conflicts.

### ⭐ Reviews
  + Users can leave comments and ratings after completing a booking. This will help improve trust in the platform and system.

### 💳 Payment services
  + Securely handles transactions for bookings which may include payment tracking, method and status.

  ## 5. 🔐 API Security

  ### Key security measures

- **Authentication:** Use JWT or OAuth2 to verify, manage user identity sessions.
- **Rate limiting:** Protect APIs from denial-of-service attacks and abuse.
- **Authorization:** Ensure only authorized users can perform certain actions.
- **Data encryption:** Encrypt sensitive data at rest where necessary and in transit (HTTPS).

### Why security is crucial

- **User protection:** Prevent unauthorized access to personal data and accounts.
- **System reliability:** Prevent malicious attacks that could disrupt service and functionalities.
- **Financial integrity:** Secure booking processes and payment transactions.