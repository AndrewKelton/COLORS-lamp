# COLORS-lamp
COLORS LAB for COP4331C-0003


## Description
  The COLORS Lab is a small web app that allows user's to login, add colors to the database, and search for those colors 
  in the database. This lab focused more on integrating existing code into the Digital Ocean deployment architecture. I 
  learned to set up and deploy a web app with a custom URL on Digital Ocean's servers.

## Technologies
  This lab uses the following technologies:
  - LAMP Stack
    - L - Linux
    - A - Apache HTTP Server
    - M - MySQL
    - P - PHP
  - JavaScript front end

## High-Level Setup Instructions 
To set up this program:

1. **Server Environment Setup**
   - Set up a Linux server (Ubuntu recommended) with Apache, MySQL, and PHP installed
   - Ensure Apache is configured and running
   - Verify PHP and MySQL are properly installed and configured

2. **Database Configuration**
   - Create a MySQL database for the application
   - Create a `Users` table with fields: `ID`, `firstName`, `lastName`, `Login`, `Password`
   - Create a `Colors` table with fields: `UserId`, `Name`
   - Update database credentials in all PHP files in the `LAMPAPI/` directory:
     - Replace `DB_USER`, `DB_PASSWORD`, and `DB_NAME` with your actual database credentials

3. **Web Server Deployment**
   - Clone or upload the repository to your web server's document root (e.g., `/var/www/html/`)
   - Ensure proper file permissions are set for Apache to read the files
   - Configure Apache to serve the application from your desired domain or subdomain

4. **DNS Configuration (for custom URL)**
   - Point your domain/subdomain to your server's IP address
   - Configure Apache virtual hosts if using a custom domain

5. **Testing**
   - Create test user accounts in the `Users` table
   - Access the application through your web browser
   - Test login, color addition, and color search functionality

## How to run and access the application
To run and access the application:

1. **Access the Application**
   - Open a web browser and navigate to your deployed URL (e.g., `http://yourdomain.com` or `http://your-server-ip/`)
   - The login page (`index.html`) will be displayed

2. **Login**
   - Enter your username and password
   - Click the "Do It" button to authenticate
   - Upon successful login, you'll be redirected to the color management page (`color.html`)

3. **Add Colors**
   - On the color management page, enter a color name in the "Color To Add" field
   - Click "Add Color" to save the color to the database
   - The color will be associated with your user account

4. **Search Colors**
   - Enter a search term in the "Color To Search For" field
   - Click "Search Color" to find matching colors
   - Results will display all colors matching your search that belong to your account

5. **Logout**
   - Click the "Log Out" button to end your session and return to the login page

## Any assumptions, limitations, or AI usage (as per class policy).
This lab was limited to using the LAMP stack, as stated earlier. It was assumed that
the code written worked as intended.