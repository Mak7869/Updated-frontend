# NexEvent - Event Management System

A beautiful, modern event management platform built with Node.js, Express, MySQL, and EJS. Manage events, attendees, and venues with an intuitive dashboard and stunning rainbow-themed UI.

![NexEvent](https://img.shields.io/badge/NexEvent-Event%20Management-blue?style=for-the-badge&logo=eventbrite)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=flat&logo=mysql&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=flat&logo=bootstrap&logoColor=white)

## ✨ Features

### 🎯 Core Functionality
- **Event Management**: Create, edit, publish, and manage events
- **Attendee Registration**: Seamless registration system with user management
- **Venue Scheduling**: Assign and manage event venues
- **Role-based Access**: Different permissions for attendees, organizers, and admins
- **Search & Filter**: Advanced filtering by date, category, and search terms

### 🎨 User Experience
- **Rainbow Theme**: Beautiful gradient backgrounds throughout the application
- **Responsive Design**: Perfect experience on desktop, tablet, and mobile
- **Interactive UI**: Smooth animations, hover effects, and transitions
- **Glass Morphism**: Modern translucent design elements
- **Toast Notifications**: Real-time feedback for user actions

### 👥 User Roles
- **Attendee**: Browse and register for events
- **Organizer**: Create and manage their own events
- **Admin**: Full system administration and user management

## 🚀 Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MySQL
- **Frontend**: EJS, Bootstrap 5, Custom CSS
- **Authentication**: Passport.js with bcrypt
- **Session Management**: Express Session
- **Security**: Helmet, Rate Limiting, Input Validation
- **Icons**: Font Awesome

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v14 or higher)
- **MySQL** (v8.0 or higher)
- **npm** or **yarn** package manager

## 🛠️ Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/nexevent.git
cd nexevent
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Setup
Create a `.env` file in the root directory with the following variables:

```env
# Database Configuration
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=nexevent_db

# Session Configuration
SESSION_SECRET=your_super_secret_session_key_here

# Server Configuration
PORT=8080
NODE_ENV=development
```

### 4. Database Setup

#### Create Database
```sql
CREATE DATABASE nexevent_db;
```

#### Run Schema
Execute the SQL commands from `schema.sql` in your MySQL database:

```bash
mysql -u your_username -p nexevent_db < schema.sql
```

#### Sample Data (Optional)
The schema includes sample categories and initial data structure.

## 🚀 Running the Application

### Development Mode
```bash
npm start
```

### Production Mode
```bash
npm run prod
```

The application will be available at `http://localhost:8080`

## 📖 Usage Guide

### 🔐 User Registration & Login

1. **Visit the homepage** at `http://localhost:8080`
2. **Register** a new account or **login** with existing credentials
3. **Choose your role**: Attendee, Organizer, or Administrator

### 👤 For Attendees

1. **Browse Events**: View all published events on the events page
2. **Search & Filter**: Use the search bar and filters to find specific events
3. **Register**: Click "Join Event" on events you're interested in
4. **View Registrations**: Check your registered events in your profile

### 🎭 For Organizers

1. **Dashboard**: Access your organizer dashboard with statistics
2. **Create Events**: Use "Add New Event" to create events
3. **Manage Events**: Edit, publish, or cancel your events
4. **Track Attendance**: View attendee lists and manage registrations

### 👑 For Administrators

1. **Admin Dashboard**: Full system overview and analytics
2. **User Management**: View and manage all users
3. **Event Oversight**: Monitor all events in the system
4. **System Health**: Check database statistics and performance

## 🎨 UI Features

### 🌈 Rainbow Theme
- **Dynamic Background**: Flowing rainbow gradient on all pages
- **Glass Effects**: Translucent elements with backdrop blur
- **Gradient Accents**: Multi-color overlays and shimmer effects

### 📱 Responsive Design
- **Mobile-First**: Optimized for all screen sizes
- **Touch-Friendly**: Interactive elements work perfectly on touch devices
- **Flexible Layouts**: Bootstrap grid system with custom enhancements

### ✨ Animations & Effects
- **Hover Animations**: Smooth transitions and scaling effects
- **Loading States**: Visual feedback during form submissions
- **Toast Notifications**: Non-intrusive status messages
- **Ripple Effects**: Interactive button feedback

## 🔌 API Endpoints

### Authentication
- `GET /login` - Login page
- `POST /login` - Process login
- `GET /register` - Registration page
- `POST /register` - Process registration
- `GET /logout` - Logout user

### Events
- `GET /events` - List all events (with search/filter)
- `GET /events/new` - Create new event form
- `POST /events` - Create event
- `GET /events/:id/edit` - Edit event form
- `PUT /events/:id` - Update event
- `DELETE /events/:id` - Delete event

### Event Management
- `POST /events/:id/publish` - Publish draft event
- `POST /events/:id/unpublish` - Unpublish event
- `POST /events/:id/cancel` - Cancel event
- `POST /events/:id/join` - Register for event
- `POST /events/:id/leave` - Unregister from event

### Dashboard & Admin
- `GET /dashboard` - Organizer dashboard
- `GET /admin` - Admin dashboard
- `GET /admin/users` - User management
- `GET /admin/events` - Event management

## 📁 Project Structure

```
nexevent/
├── views/                 # EJS templates
│   ├── layouts/          # Layout templates
│   ├── index.ejs         # Home page
│   ├── login.ejs         # Login page
│   ├── register.ejs      # Registration page
│   ├── dashboard.ejs     # Organizer dashboard
│   ├── admin.ejs         # Admin dashboard
│   └── events.ejs        # Events listing
├── public/               # Static assets
│   └── style.css         # Additional styles
├── config/               # Configuration files
│   └── passport.js       # Authentication setup
├── server.js             # Main application file
├── schema.sql            # Database schema
├── package.json          # Dependencies and scripts
└── README.md            # This file
```

## 🔒 Security Features

- **Password Hashing**: bcrypt for secure password storage
- **Session Management**: Secure session handling with expiration
- **Rate Limiting**: Protection against brute force attacks
- **Input Validation**: Sanitization of user inputs
- **Helmet**: Security headers and protections
- **CSRF Protection**: Session-based protection

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines
- Follow the existing code style
- Write clear, concise commit messages
- Test your changes thoroughly
- Update documentation as needed

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙋‍♂️ Support

If you have any questions or need help:

- **Issues**: Open an issue on GitHub
- **Discussions**: Use GitHub Discussions for questions
- **Email**: Contact the maintainers

## 🎉 Acknowledgments

- **Bootstrap** for the responsive framework
- **Font Awesome** for beautiful icons
- **Express.js** community for excellent documentation
- **MySQL** for reliable database management

---

**Happy Event Managing! 🎊**

Built with ❤️ using Node.js, Express, and modern web technologies.
