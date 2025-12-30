# EWU Car Rental Portal

A comprehensive web-based car rental management system that enables users to browse, search, and book vehicles. This application includes both customer-facing and administrative interfaces for complete car rental business management.

## Overview

EWU Car Rental Portal is a full-featured car rental platform built with PHP, MySQL, and Bootstrap. It provides an intuitive interface for customers to search and book vehicles while offering administrators powerful tools to manage inventory, bookings, and customer inquiries.

## Features

### Customer Features
- **Vehicle Browsing**: View all available cars with detailed information including specifications, pricing, and images
- **Advanced Search**: Filter vehicles by brand and fuel type to find the perfect car
- **Vehicle Details**: Comprehensive vehicle information including:
  - Multiple high-resolution images
  - Specifications (seating capacity, model year, fuel type)
  - Pricing per day
  - Vehicle overview and features
  - Amenities checklist (AC, power steering, etc.)
- **Booking System**: Easy-to-use booking interface with availability checks
- **User Accounts**: 
  - Registration with email verification
  - Login/Logout functionality
  - Password management
  - Profile management (personal information, address, contact details)
- **Booking Management**: View and manage all active and past bookings
- **Testimonials**: Share experiences and read other customer testimonials
- **Contact Us**: Send queries and feedback to the management team
- **Theme Switcher**: Choose from multiple color themes (Red, Orange, Blue, Pink, Green, Purple)

### Admin Features
- **Secure Admin Dashboard**: Role-based access control
- **Vehicle Management**:
  - Add new vehicles to inventory
  - Edit vehicle details and specifications
  - Upload and manage multiple vehicle images
  - Change individual vehicle images
  - Delete vehicles
- **Brand Management**:
  - Create and manage car brands
  - Edit brand information
  - Delete brands
- **Booking Management**: View and manage all customer bookings
- **User Management**: View registered users and their profiles
- **Testimonial Management**: View and moderate customer testimonials
- **Contact Query Management**: View and respond to customer inquiries
- **Subscriber Management**: Manage newsletter subscribers
- **Page Management**: Create and manage static pages (About Us, Terms & Conditions, etc.)
- **Contact Information**: Update business contact information
- **Password Management**: Secure admin password change

## Project Structure

```
EWU-CAR-RENTAL/
├── index.php                          # Homepage with featured vehicles
├── car-listing.php                    # All available vehicles listing
├── vehical-details.php                # Detailed vehicle information
├── search-carresult.php               # Search results page
├── my-booking.php                     # User's bookings
├── my-testimonials.php                # User's testimonials
├── post-testimonial.php               # Submit new testimonial
├── profile.php                        # User profile management
├── update-password.php                # Change password
├── contact-us.php                     # Contact form
├── logout.php                         # Logout functionality
├── check_availability.php             # AJAX email availability checker
├── page.php                           # Static pages display
│
├── admin/                             # Admin panel directory
│   ├── index.php                      # Admin login page
│   ├── dashboard.php                  # Admin dashboard
│   ├── manage-vehicles.php            # Vehicle inventory management
│   ├── post-avehical.php              # Add new vehicle
│   ├── edit-vehicle.php               # Edit vehicle details
│   ├── changeimage1.php to changeimage5.php  # Change vehicle images
│   ├── manage-brands.php              # Brand management
│   ├── create-brand.php               # Add new brand
│   ├── edit-brand.php                 # Edit brand
│   ├── manage-bookings.php            # Booking management
│   ├── manage-contactusquery.php      # Customer inquiries
│   ├── manage-subscribers.php         # Newsletter subscribers
│   ├── manage-pages.php               # Static pages management
│   ├── reg-users.php                  # Registered users list
│   ├── testimonials.php               # Testimonials management
│   ├── update-contactinfo.php         # Update business contact info
│   ├── change-password.php            # Admin password change
│   ├── logout.php                     # Admin logout
│   ├── nicEdit.js                     # Rich text editor
│   ├── includes/                      # Admin shared files
│   │   ├── config.php                 # Database configuration
│   │   ├── header.php                 # Admin header
│   │   └── leftbar.php                # Admin sidebar navigation
│   ├── css/                           # Admin stylesheets
│   ├── js/                            # Admin JavaScript
│   └── fonts/                         # Font files
│
├── includes/                          # Shared files
│   ├── config.php                     # Database configuration
│   ├── header.php                     # Main header navigation
│   ├── footer.php                     # Footer component
│   ├── sidebar.php                    # Sidebar navigation
│   ├── colorswitcher.php              # Theme switcher
│   ├── login.php                      # Login form modal
│   ├── registration.php               # Registration form modal
│   └── forgotpassword.php             # Forgot password form
│
├── assets/                            # Frontend resources
│   ├── css/                           # Stylesheets
│   │   ├── bootstrap.min.css
│   │   ├── style.css                  # Custom styles
│   │   ├── owl.carousel.css
│   │   ├── slick.css
│   │   ├── bootstrap-slider.min.css
│   │   └── font-awesome.min.css
│   ├── js/                            # JavaScript files
│   │   ├── jquery.min.js
│   │   ├── bootstrap.min.js
│   │   ├── owl.carousel.min.js
│   │   ├── slick.min.js
│   │   ├── interface.js
│   │   └── countdown_date.js
│   ├── images/                        # Static images
│   │   └── favicon-icon/
│   ├── fonts/                         # Font files
│   └── switcher/                      # Color theme files
│       ├── css/                       # Theme stylesheets
│       └── js/                        # Theme switcher script
│
└── index2.html                        # Default InfinityFree page

```

## Technology Stack

- **Backend**: PHP 7.x
- **Database**: MySQL
- **Frontend Framework**: Bootstrap 3
- **Frontend Libraries**:
  - jQuery
  - OWL Carousel (image slider)
  - Slick Slider
  - Bootstrap Slider
  - Font Awesome Icons
- **Data Access**: PDO (PHP Data Objects)
- **Rich Text Editor**: NicEdit
- **Charting**: Chart.js (for admin dashboard)

## Database

The application uses MySQL database with the following main tables:
- **tblusers**: User account information
- **tblvehicles**: Vehicle inventory and details
- **tblbrands**: Car brands
- **tblbooking**: Booking records
- **tbltestimonial**: Customer testimonials
- **tblcontactusquery**: Contact form submissions
- **tblpages**: Static page content
- **tblsubscribers**: Newsletter subscribers

**Database Credentials** (from includes/config.php):
- Host: sql111.infinityfree.com
- User: if0_37786310
- Database: if0_37786310_survey

## Installation & Setup

### Requirements
- PHP 7.0 or higher
- MySQL 5.6 or higher
- Web Server (Apache, Nginx, etc.)
- Modern web browser

### Installation Steps

1. **Clone or download the project**
   ```bash
   git clone https://github.com/azizulabedinazmi/EWU-CAR-RENTAL.git
   cd EWU-CAR-RENTAL
   ```

2. **Database Setup**
   - Create a MySQL database
   - Import the database schema (ensure all tables are created)
   - Update database credentials in `includes/config.php` and `admin/includes/config.php`

3. **Configure Database Connection**
   
   Edit `includes/config.php`:
   ```php
   define('DB_HOST', 'your_host');
   define('DB_USER', 'your_user');
   define('DB_PASS', 'your_password');
   define('DB_NAME', 'your_database');
   ```

4. **Upload to Server**
   - Upload all files to your web server root directory
   - Ensure proper file permissions (644 for files, 755 for directories)

5. **Access the Application**
   - Frontend: `http://yourserver.com/`
   - Admin Panel: `http://yourserver.com/admin/`

## Usage Guide

### For Customers

1. **Browse Vehicles**
   - Visit the homepage to see featured vehicles
   - Click "Car Listing" to view all available cars
   - Use search functionality to filter by brand and fuel type

2. **View Vehicle Details**
   - Click on any vehicle to see complete details
   - View multiple images, specifications, and amenities
   - Check availability and pricing

3. **Book a Vehicle**
   - Select your booking dates
   - Provide necessary information
   - Complete the booking process

4. **Manage Account**
   - Register or login
   - Update profile information
   - Change password
   - View booking history

5. **Share Feedback**
   - Write testimonials about your experience
   - View other customers' testimonials
   - Contact support via contact form

### For Administrators

1. **Admin Login**
   - Access `http://yourserver.com/admin/`
   - Enter admin credentials

2. **Manage Vehicles**
   - Add new vehicles with details and images
   - Edit existing vehicle information
   - Change vehicle images
   - Delete vehicles from inventory

3. **Manage Brands**
   - Create new car brands
   - Edit brand information
   - Delete brands

4. **Process Bookings**
   - View all booking requests
   - Confirm or cancel bookings
   - Track booking status

5. **User Management**
   - View registered users
   - Manage user accounts

6. **Customer Support**
   - View testimonials and approve them
   - View and respond to contact inquiries
   - Manage newsletter subscribers

7. **Settings**
   - Update business contact information
   - Manage static pages (About, Terms, etc.)
   - Change admin password

## Key Features Explained

### Email Verification
The registration system includes real-time email verification to prevent duplicate accounts. When registering, the system checks if the email already exists in the database.

### Booking System
Customers can check vehicle availability for specific dates and complete bookings. The system validates dates and availability before confirming bookings.

### Theme Customization
Users can switch between 6 different color themes:
- Red
- Orange
- Blue
- Pink
- Green
- Purple

### Security Features
- Password encryption using MD5
- Session-based authentication
- SQL injection prevention using PDO prepared statements
- HTML entity encoding for output sanitization

### Image Management
Admin can upload up to 5 different images for each vehicle, with individual image change functionality for easy updates.

## File Naming Conventions

- **vehical-details.php**: Note: Uses "vehical" spelling (appears to be intentional or legacy naming)
- **post-avehical.php**: Admin file for adding vehicles (legacy naming: "avehical")
- **nicEdit.js**: Rich text editor for admin content management

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- IE 9+

## Performance Features

- CSS and JavaScript minification
- Image optimization with responsive sizing
- Lazy loading of images
- Carousel and slider optimization
- Database query optimization with prepared statements

## Security Considerations

⚠️ **Important Security Notes**:
- Database credentials should be stored in environment variables, not hardcoded
- Password encryption should be upgraded from MD5 to bcrypt or similar
- HTTPS should be enabled in production
- Implement CSRF tokens for form submissions
- Add rate limiting for login attempts
- Regularly update dependencies

## Future Enhancement Suggestions

- [ ] Payment gateway integration
- [ ] Email notifications for bookings
- [ ] SMS notifications
- [ ] Advanced reporting and analytics
- [ ] API development for mobile apps
- [ ] User reviews with ratings
- [ ] Loyalty program
- [ ] Insurance options
- [ ] Advanced search with date/location filtering
- [ ] Google Maps integration
- [ ] Real-time booking status updates

## Troubleshooting

### Database Connection Issues
- Verify database credentials in `config.php`
- Ensure MySQL server is running
- Check database user permissions

### Upload Issues
- Ensure `admin/img/vehicleimages/` directory exists and is writable
- Check PHP upload size limits in php.ini
- Verify file permissions (755 for directories)

### Login Problems
- Clear browser cache and cookies
- Verify user exists in database
- Check password is correct (case-sensitive)

### Display Issues
- Clear browser cache
- Check CSS file paths
- Verify JavaScript is enabled

## Author

**Azizul Abedin Azmi**
- GitHub: [azizulabedinazmi](https://github.com/azizulabedinazmi)

## License

This project is provided as-is for educational and commercial use.

## Support & Contact

For issues, questions, or suggestions:
- Open an issue on GitHub
- Contact via the application's contact form
- Visit: https://github.com/azizulabedinazmi

## Changelog

### Version 1.0
- Initial release
- Complete car rental management system
- User authentication and profiles
- Vehicle browsing and booking
- Admin dashboard
- Testimonial system
- Contact management
- Theme customization

---



For the latest updates and information, visit the [GitHub Repository](https://github.com/azizulabedinazmi/EWU-CAR-RENTAL)
