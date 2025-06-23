# Requirement Analysis in Software Development

<p>This repo will be for requirements gathering and analysis for the Airbnb clone app.</p>

# What is Requirement Analysis?

<p>Requirement Analysis is the critical process in the Software Development Lifecycle (SDLC) that involves defining, documenting, and validating the expectations and needs of stakeholders for a new or modified software product. It serves as the foundational blueprint for the entire project, ensuring that the final product aligns with user needs and business objectives. A thorough and well-executed Requirement Analysis phase is paramount to a project's success, directly impacting its timeline, budget, and overall quality.</p>

# Why is Requirement Analysis Important?

A thorough Requirement Analysis phase is critical to the success of any project in the Software Development Lifecycle (SDLC). It acts as the project's foundation, directly influencing budget, timeline, and final product quality.

Here are three key reasons why it is indispensable:

### 1. Reduces Development Costs and Prevents Rework
- **Finding errors early is cheap.** An error in the requirements phase is significantly easier and less expensive to fix than the same error found during development or after the product has been deployed.
- **Prevents "Scope Creep".** A clearly defined and agreed-upon set of requirements establishes a solid baseline, protecting the project from uncontrolled changes and additions that lead to budget overruns and missed deadlines.

### 2. Ensures the Final Product Meets User Needs
- **Builds the *right* product.** Requirement Analysis focuses on understanding the problems and goals of the end-users. This ensures the development team's effort is directed at building a product that provides real value, leading to higher user satisfaction and adoption.
- **Aligns Stakeholder Expectations.** It forces all stakeholders—customers, developers, and managers—to agree on a shared vision for the final product, eliminating misunderstandings from the start.

### 3. Provides a Clear Foundation for Design, Development, and Testing
- **Acts as a "Single Source of Truth".** The formal requirements document (like an SRS) becomes the definitive guide for the entire team. Designers know what to design, developers know what to build, and testers know what to test against.
- **Minimises Ambiguity.** Clear, detailed, and validated requirements remove guesswork and misinterpretation, leading to a smoother workflow and a higher-quality end product.

# Key Activities in Requirement Analysis.

At its heart, Requirement Analysis is a process of discovery and communication. It seeks to answer fundamental questions such as:

> - What is the problem the software is intended to solve?
> - Who are the users, and what are their goals?
> - What functionalities must the software possess?
> - What are the performance, security, and usability expectations?
> - What are the constraints and limitations of the project?

To answer these questions, the process is typically broken down into several key activities:

### Key Activities in Requirement Analysis

1.  **Elicitation**: This is the initial step of gathering requirements from all relevant stakeholders, including customers, users, business managers, and technical staff. Common techniques for elicitation include interviews, surveys, workshops, brainstorming sessions, and analysis of existing systems and documents.

2.  **Analysis**: Once gathered, the raw requirements are analysed for clarity, completeness, consistency, and feasibility. Analysts identify and resolve any conflicts or ambiguities in the stated needs. This stage often involves prioritising requirements based on business value and technical complexity.

3.  **Modelling**: To better understand and communicate the requirements, analysts often create visual models. These can include diagrams such as Use Case diagrams, Data Flow Diagrams (DFDs), and Unified Modelling Language (UML) diagrams, which help to illustrate the system's behaviour, data flows, and structure.

4.  **Specification**: The analysed and modelled requirements are then formally documented in a Software Requirements Specification (SRS) document. This document serves as a single source of truth for all stakeholders, detailing both functional and non-functional requirements.
    -   **Functional Requirements** describe what the system should *do*. For example:
        > `The system shall allow users to register for an account.`
    -   **Non-Functional Requirements** define the *qualities* of the system. For example:
        > -   **Performance:** `The system shall load the dashboard within 2 seconds.`
        > -   **Security:** `All user data must be encrypted.`
        > -   **Usability:** `The user interface should be intuitive for a novice user.`

5.  **Validation and Verification**: Before moving to the design phase, the documented requirements are reviewed and validated by the stakeholders to ensure they accurately reflect their needs. Verification ensures that the requirements are well-formed, complete, and consistent.

# Types of Requirements

Based on the architecture for a hotel booking app like Airbnb or Oyo, we can categorise requirements into two main types: Functional and Non-functional.

---

## Functional Requirements

**Definition:** These describe what the system *must do*. They are the specific features and functions that allow a user to accomplish their tasks on the platform.

### Examples:

-   **User Management:**
    -   The system shall allow users to register for an account using an email address and password, or via OAuth providers like Google and Facebook.
    -   The system shall allow users to log in and log out.
    -   Users must be able to create and update their user profiles with information like name, profile picture, and contact details.
    -   The system shall differentiate between "Guest" and "Host" user roles, each with different permissions.

-   **Property & Search:**
    -   A Host shall be able to create, update, and delete a property listing (e.g., hotel room, apartment).
    -   Listings must include details such as name, address, description, photos, price per night, and available amenities.
    -   A Guest shall be able to search for properties based on location (city, zip code), check-in/check-out dates, and the number of guests.
    -   The search results must be filterable by price range, property type (e.g., `apartment`, `house`), and specific amenities (e.g., `Wi-Fi`, `pool`).

-   **Booking & Payment:**
    -   The system shall allow a Guest to select a property and book it for available dates.
    -   The system must display a total price, including nightly rates, cleaning fees, and service charges, before confirming a booking.
    -   The system shall integrate with a payment gateway (e.g., Stripe, PayPal) to process credit/debit card payments securely.
    -   Upon successful payment, the system must confirm the booking and update the property's calendar to show it is unavailable for the booked dates.

-   **Notifications & Reviews:**
    -   The system shall send an automated email and/or push notification to both the Guest and Host upon booking confirmation.
    -   After a stay is complete, the system shall prompt both the Guest and Host to leave a review and a rating (e.g., 1-5 stars) for each other.
    -   The system shall display average ratings and all public reviews on a property's listing page.

---

## Non-functional Requirements

**Definition:** These define the *qualities* of the system and describe *how* it should perform its functions. They are often called "quality attributes" and set constraints on the system's operation.

### Examples:

-   **Performance & Scalability:**
    -   The property search results page must load in under **3 seconds**, even with thousands of listings.
    -   The payment processing gateway must respond (success or failure) within **5 seconds**.
    -   The system must be able to handle **10,000 concurrent users** during peak holiday seasons without significant degradation in performance.

-   **Availability & Reliability:**
    -   The booking and payment services must have an uptime of **99.9%** (less than 45 minutes of downtime per month).
    -   User data, such as bookings and profiles, must be backed up daily to prevent data loss.

-   **Security:**
    -   All user passwords must be securely hashed and salted before being stored in the database.
    -   All communication between the client (browser/app) and the server must be encrypted using **TLS 1.2** or higher.
    -   The system must be **PCI DSS compliant** to handle credit card information securely.

-   **Usability:**
    -   The user interface must be responsive and provide a seamless experience on desktop, tablet, and mobile devices.
    -   A new user should be able to complete the booking process (from search to payment confirmation) in **5 steps or fewer**.

-   **Localisation:**
    -   The platform's user interface must be available in multiple languages, starting with English and Spanish.
    -   The system must support and display prices in multiple currencies (e.g., `USD`, `EUR`, `INR`), with clear conversion rates.
