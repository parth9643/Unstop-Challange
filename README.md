# Train Seat Booking System

## Problem Statement

The train seat booking system is designed for a single coach train with the following configuration:

- The coach contains **80 seats**, arranged in **7 seats per row**, with the **last row containing 3 seats**.
- A person can reserve up to **7 seats at a time**.
- **Priority:**
  - Seats should be booked in the **same row** whenever possible.
  - If seats are not available in the same row, the system will book **nearby seats**.

The seating status is represented by a string of length 80, where:

- `0` indicates an **empty seat**.
- `1` indicates a **booked seat**.

The system ensures the seating status is **persistent** by storing this string in a database. This allows the program to maintain the latest seat status across different sessions.

---

## Features

- **Seat Availability Check:**
  - Determines if a row has enough consecutive empty seats for a booking.
- **Reservation Logic:**
  - Books seats in a single row if possible.
  - Ensures nearby seats are booked when a single-row reservation isn't feasible.
- **Database Integration:**
  - The seat status is stored in a database for persistence.
  - The application fetches and updates the seat status dynamically.

---

## Project Setup

Follow these steps to set up and run the application:

### Prerequisites

- PHP 8.0 or later
- Composer
- MySQL
- XAMPP (or any local server environment)

### Installation

1. **Clone the Repository:**

   ```bash
   git clone
   https://github.com/parth9643/Unstop-Challange.git
   cd Unstop-Challenge-Files
   ```

2. **Install Dependencies:**

   ```bash
   composer install
   ```

3. **Set Up Environment File:**

   - Copy the `.env.example` file to `.env`:
     ```bash
     cp .env.example .env
     ```
   - Update the `.env` file with your local environment details (database configuration, etc.).

4. **Generate Application Key:**

   ```bash
   php artisan key:generate
   ```

5. **Start the MySQL Server:**

   - Use XAMPP or your preferred MySQL server.

6. **Run Database Migrations:**

   ```bash
   php artisan migrate:fresh
   ```

7. **Seed the Database:**

   - Insert the initial seating status (a string of 80 characters):
     ```bash
     php artisan db:seed
     ```

8. **Run the Application:**

   ```bash
   php artisan serve
   ```

   The application will be available at `http://localhost:8000`.

---

## Project Structure

### Key Files

- **Controllers:**

  - `app/Http/Controllers/TicketBookingController`
    - Contains the core logic for seat availability checks and reservation.

- **Database:**

  - `database/migrations/`
    - Defines the structure of the database tables.
  - `database/seeders/TicketbookingSeeder`
    - Seeds the database with the initial seat status.

- **Views:**

  - `resources/views/welcome.blade.php`
    - Landing page of the application.
  - `resources/views/ticket-info.blade.php`
    - Displays ticket reservation details.

- **Routes:**

  - `routes/web.php`
    - Defines the application’s web routes.

---

## Usage

1. Access the application through the browser at `http://localhost:8000`.
2. Use the interface to reserve seats in the train coach.
3. View the seat status and booking information dynamically.

---

## About Me

I am a Full Stack Web Developer with experience in designing, developing, and deploying web applications tailored to client requirements. I am passionate about solving complex problems and creating efficient solutions.

---

## Connect with Me

- [LinkedIn](#)

[https://www.linkedin.com/in/parthshukla9643/](https://www.linkedin.com/in/parthshukla9643/)



