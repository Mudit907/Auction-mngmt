**Auction‑Management System**

An Auction‑Management web app built with PHP and MySQL to facilitate item listings, bidding, and user management.

**Table of Contents**

1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Setup & Installation](#setup--installation)
4. [Configuration](#configuration)
5. [Usage](#usage)
6. [Database Schema](#database-schema)
7. [Directory Structure](#directory-structure)
8. [Contributors](#contributors)
9. [License](#license)

---

**Features**

* ✅ User registration and authentication
* ✅ Admin dashboard for creating/managing auctions
* ✅ Item listing with categories
* ✅ Real-time bidding and bid history
* ✅ Bank integration (if applicable)
* ✅ Search and filter by category or city
* ✅ Contact form, About, Advertise, etc.

---

**Tech Stack**

* **Backend**: PHP (≈ 98%)
* **Database**: MySQL
* **Frontend**: HTML, CSS, JavaScript
* **Web Server**: Apache or Nginx

---

**Setup & Installation**

**Prerequisites**

* PHP ≥ 7.x
* MySQL
* A web server (Apache, Nginx)
* Composer (if dependency management is used)

**Installation Steps**

1. Clone the repo:

   ```bash
   git clone https://github.com/Mudit907/Auction-mngmt.git
   cd Auction-mngmt
   ```
2. Create a MySQL database, e.g. `auction_db`.
3. Import the provided SQL dump:

   ```sql
   mysql -u root -p auction_db < db/schema.sql
   ```
4. Copy config template and set your credentials:

   ```bash
   cp config.example.php config.php
   # Edit config.php with your DB credentials
   ```
5. Place your files under document root (e.g., `htdocs/auction/`).
6. Visit `http://localhost/auction/index.php` to run.

---

**Configuration**

Create/edit `config.php` with:

```php
<?php
define('DB_HOST', 'localhost');
define('DB_USER', 'your_user');
define('DB_PASS', 'your_password');
define('DB_NAME', 'auction_db');
define('BASE_URL', 'http://localhost/auction/');
```
---

**Usage**

* **Homepage**: Lists open auctions with filters and search.
* **Register/Login**: Users must sign up to bid.
* **Auctions Page**: View item details, bid, see history.
* **Admin Interface**: Manage auctions, categories, banks, and cities.
* **Info Pages**: About Us, Contact Us, Advertise with Us.

---

**Database Schema**

Key tables:

| Table      | Description                   |
| ---------- | ----------------------------- |
| users      | User credentials & profiles   |
| auctions   | Auction listings & status     |
| bids       | Bid records                   |
| categories | Item categories               |
| cities     | Available cities for auctions |
| banks      | Bank details/configuration    |


---

**Directory Structure**

```
/
├── auctions.php        # Main auction list
├── auctions1.php       # Single‑auction detail page
├── category.php        # Category filter views
├── banks.php           # Bank management
├── cities.php          # City management
├── contact-us.php      # Contact form page
├── about-us.php
├── advertise-with-us.php
├── include/            # Shared headers, footers
├── config.php          # DB & app config (exclude from git)
└── db/                 # SQL scripts and seed data
```

**Contributors**

* **Mudit** – Initial development ([@Mudit907](https://github.com/Mudit907))

Contributions welcome! Feel free to open issues or pull requests 😊

---

## License

Distributed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

**Final Notes**

* Don’t commit sensitive files (like `Server-Credentials.txt`) – add them to `.gitignore`.
* Consider migrating to [Composer](https://getcomposer.org/) for dependencies.
* Add unit/integration tests to `tests/`.
* Enhance UX: email notifications, timers, responsive layout.


