---

# **Airbnb Clone System Interactions: Use Case Diagram and User Stories**

---

## **Task 1 — Use Case Diagram**

### **Objective**

To visualize how different users (actors) interact with the Airbnb Clone system for major functionalities such as registration, property management, booking, payments, and reviews.

---

### **1.1 Actors**

| Actor               | Description                                                              |
| ------------------- | ------------------------------------------------------------------------ |
| **Guest**           | A user who browses, books, and reviews properties.                       |
| **Host**            | A user who lists and manages properties.                                 |
| **Admin**           | A system administrator who oversees users, properties, and transactions. |
| **Payment Gateway** | An external system responsible for processing payments securely.         |

---

### **1.2 Key Use Cases**

| Use Case                                   | Description                                                        | Primary Actor          |
| ------------------------------------------ | ------------------------------------------------------------------ | ---------------------- |
| **Register Account**                       | Create a new user account (guest or host).                         | Guest / Host           |
| **Login and Authenticate**                 | Access the platform securely using email/password or OAuth.        | Guest / Host / Admin   |
| **Manage Profile**                         | Update personal information, contact details, or profile image.    | Guest / Host           |
| **List Property**                          | Create a property listing with details and images.                 | Host                   |
| **Edit/Delete Property**                   | Update or remove an existing property listing.                     | Host                   |
| **Search Properties**                      | Find properties based on filters (location, price, amenities).     | Guest                  |
| **Book Property**                          | Reserve an available property for specific dates.                  | Guest                  |
| **Cancel Booking**                         | Cancel an existing booking within the cancellation policy.         | Guest / Host           |
| **Make Payment**                           | Complete payment for a booking via Stripe/PayPal.                  | Guest                  |
| **Receive Payout**                         | Host receives payment after successful booking completion.         | Host / Payment Gateway |
| **Leave Review**                           | Submit a review and rating for a completed booking.                | Guest                  |
| **Respond to Review**                      | Reply to guest reviews on hosted properties.                       | Host                   |
| **Send Message**                           | Communicate between guest and host about bookings.                 | Guest / Host           |
| **Receive Notification**                   | Get in-app or email notifications for booking and payment updates. | All Users              |
| **Manage Users, Properties, and Payments** | Administrative oversight and issue resolution.                     | Admin                  |

---

### **1.3 Use Case Diagram Logic (Text Representation)**

```
                          [Payment Gateway]
                                  │
                                  │ (process payments)
                                  │
                                (Make Payment)
                                   ▲
                                   │
        ┌────────────────────────────────────────────────────┐
        │                                                    │
        │                Airbnb Clone System                 │
        │                                                    │
        │  (Register Account)       (Login and Authenticate) │
        │  (Manage Profile)         (Search Properties)      │
        │  (Book Property)          (Cancel Booking)         │
        │  (Make Payment)           (Leave Review)           │
        │  (Respond to Review)      (Send Message)           │
        │  (Receive Notification)   (List/Edit/Delete Property) │
        │  (Manage Users, Bookings, Payments)                 │
        │                                                    │
        └────────────────────────────────────────────────────┘
           ▲                 ▲                 ▲
           │                 │                 │
         [Guest]           [Host]           [Admin]
```

---

### **1.4 Description**

* **Guest** interacts with the system to register, search, book, pay, review, and communicate.
* **Host** interacts to register, list, manage, and monitor property bookings and messages.
* **Admin** manages overall system data, ensuring compliance, moderation, and security.
* **Payment Gateway** connects externally to process transactions securely.

---

## **Task 2 — User Stories**

### **Objective**

To translate the use case interactions into clear, actionable user stories that reflect end-user goals and motivations.
Each story follows the standard Agile format:

> **As a [role], I want to [action] so that I can [benefit].**

---

### **2.1 Core User Stories**

1. **User Registration**

   > As a new user, I want to be able to register an account as a guest or host so that I can use the Airbnb Clone platform.

2. **Property Management**

   > As a host, I want to create and manage property listings so that I can rent out my accommodations to guests.

3. **Search and Booking**

   > As a guest, I want to search for available properties and make bookings so that I can easily find suitable accommodations for my travel dates.

4. **Payment Processing**

   > As a guest, I want to make secure payments using online methods like Stripe or PayPal so that my bookings are confirmed instantly.

5. **Review System**

   > As a guest, I want to leave reviews and ratings for properties I’ve stayed in so that other users can make informed decisions.

6. **Communication**

   > As a guest or host, I want to send and receive messages within the platform so that I can coordinate bookings directly.

7. **Notifications**

   > As a user, I want to receive notifications for booking updates, payment confirmations, and messages so that I stay informed of important activities.

8. **Administrative Oversight**

   > As an admin, I want to manage all users, bookings, payments, and reviews so that the platform remains secure and efficient.

---

### **2.2 Summary Table**

| Actor               | Key Use Cases                                        | Example User Story                                                                          |
| ------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **Guest**           | Register, Search, Book, Pay, Review                  | “As a guest, I want to search and book properties so I can find a place to stay.”           |
| **Host**            | List Properties, Manage Listings, Respond to Reviews | “As a host, I want to create and manage listings so I can rent out my properties.”          |
| **Admin**           | Monitor Users, Bookings, and Payments                | “As an admin, I want to oversee users and payments to maintain trust and safety.”           |
| **Payment Gateway** | Process Payments                                     | “As a system, I want to securely process payments so bookings are confirmed automatically.” |

---