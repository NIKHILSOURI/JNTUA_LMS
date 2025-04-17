# JNTUA Faculty Leave Management System - Installation Guide

## Prerequisites
- XAMPP (PHP 7.4+ recommended)
- MySQL 5.7+
- Web Browser (Chrome, Firefox, Edge)

## Installation Steps

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/jntua-lms.git
cd jntua-lms
```

### 2. XAMPP Configuration
1. Start XAMPP Control Panel
2. Start Apache and MySQL services
3. Open phpMyAdmin (http://localhost/phpmyadmin)

### 3. Database Setup
#### Option 1: Using phpMyAdmin
1. Create a new database named `jntua_lms`
2. Import `database/jntua_lms_setup.sql`
3. Import `database/jntua_lms_sample_data.sql`

#### Option 2: Using MySQL Command Line
```bash
mysql -u root
CREATE DATABASE jntua_lms;
USE jntua_lms;
SOURCE database/jntua_lms_setup.sql;
SOURCE database/jntua_lms_sample_data.sql;
```

### 4. Configuration
1. Update `config/database.php` with your MySQL credentials if different from default
```php
<?php
$host = 'localhost';
$username = 'root';
$password = '';
$database = 'jntua_lms';
```

### 5. Project Placement
- Move the project folder to `htdocs` directory
- Typical path: `C:\xampp\htdocs\jntua_lms`

### 6. Access the Application
- Open browser
- Navigate to `http://localhost/jntua_lms`

## Default Login Credentials

### Admin
- Username: `admin`
- Password: `Admin@2024`
- Role: Admin

### Faculty Users
- Usernames: `fac1`, `fac2`, `fac3`, `fac4`, `fac5`
- Password for all: `Test@123`

## Troubleshooting
- Ensure PHP extensions are enabled in `php.ini`
- Check MySQL service is running
- Verify file permissions
- Review error logs in `logs/` directory

## Security Recommendations
- Change default passwords immediately
- Configure proper file and directory permissions
- Enable HTTPS for production

## System Requirements
- PHP 7.4+
- MySQL 5.7+
- 512MB RAM
- 100MB Disk Space
