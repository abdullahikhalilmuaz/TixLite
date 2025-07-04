# 🎫 TixLite

<div align="center">
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white" alt="Express.js">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/JSON-5E5C5C?style=for-the-badge&logo=json&logoColor=white" alt="JSON">
  <img src="https://img.shields.io/badge/GitHub%20Pages-222222?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Pages">
</div>

<div align="center">
  <h3>🚀 A Modern, Lightweight Ticketing System Backend</h3>
  <p><em>Built with Express.js, featuring comprehensive event management and ticket booking capabilities</em></p>
</div>

<div align="center">
  
  [![Live Documentation](https://img.shields.io/badge/📖_Live_Documentation-Visit_Now-blue?style=for-the-badge)](https://yourusername.github.io/tixlite)
  [![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?style=for-the-badge)](https://yourusername.github.io/tixlite)
  [![API Status](https://img.shields.io/badge/API-Active-success?style=for-the-badge)](https://your-api-url.com)
  
</div>

---

## 🌟 Overview

**TixLite** is a powerful, lightweight ticketing system backend designed for modern event management. Built with Node.js and Express.js, it provides a complete solution for event organizers to manage events, handle ticket bookings, and process payments with an intuitive admin dashboard.

### ✨ Key Features

- 🔐 **Dual Authentication System** - Separate user and admin authentication
- 🎪 **Event Management** - Create, manage, and organize events with rich media support
- 🎫 **Smart Ticket System** - Advanced booking with payment verification
- 📸 **Image Upload Support** - Event images and payment proof handling
- 🛡️ **Admin Dashboard** - Comprehensive admin controls for approvals
- 🌐 **RESTful API** - Clean, well-documented API endpoints
- 📱 **Mobile Ready** - Responsive design for all devices

---

## 📖 Documentation

### 🎯 Quick Start

**[View Live Documentation →](https://yourusername.github.io/tixlite)**

Our comprehensive documentation includes:
- 📋 Complete API reference
- 🔧 Setup instructions
- 💡 Usage examples
- 🎨 Interactive endpoint explorer
- 📊 Response examples

### 🏗️ Architecture Overview

```
TixLite Backend
├── 👥 User Management
│   ├── Registration & Authentication
│   └── Profile Management
├── 🎪 Event Management
│   ├── Event Creation
│   ├── Image Upload
│   └── Event Listing
├── 🎫 Ticket System
│   ├── Booking Requests
│   ├── Payment Verification
│   └── Approval Workflow
└── 🛡️ Admin Panel
    ├── Event Oversight
    ├── Ticket Approvals
    └── User Management
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Git

### 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/tixlite.git
   cd tixlite
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Start the server**
   ```bash
   npm start
   ```

The server will start on `http://localhost:3000`

---

## 🎯 API Endpoints

### 👤 User Authentication
- `POST /api/signup` - Register new user
- `POST /api/login` - User login

### 🛡️ Admin Authentication
- `POST /admin/signup` - Register new admin
- `POST /admin/login` - Admin login

### 🎪 Event Management
- `POST /api/events` - Create new event
- `GET /api/events` - Get all events
- `GET /api/events/:id` - Get event by ID
- `GET /api/events/admin/:adminId` - Get events by admin

### 🎫 Ticket Management
- `POST /api/events/:eventId/tickets` - Create ticket request
- `POST /api/events/tickets/:ticketId/approve` - Approve ticket
- `POST /api/events/tickets/:ticketId/reject` - Reject ticket
- `GET /api/events/tickets/:ticketId` - Get ticket info
- `GET /api/events/tickets/user/:userId` - Get user tickets
- `GET /api/events/tickets/admin/:adminId` - Get admin tickets

---

## 🛠️ Tech Stack

<div align="center">

| Technology | Purpose | Version |
|------------|---------|---------|
| **Node.js** | Runtime Environment | 16+ |
| **Express.js** | Web Framework | 4.x |
| **Multer** | File Upload Handling | 1.x |
| **UUID** | Unique ID Generation | 9.x |
| **CORS** | Cross-Origin Requests | 2.x |
| **JSON Files** | Data Storage | - |

</div>

---

## 📁 Project Structure

```
tixlite/
├── 📂 controllers/
│   ├── 👤 userController.js
│   ├── 🛡️ adminUserController.js
│   ├── 🎪 eventController.js
│   └── 🎫 ticketController.js
├── 📂 routes/
│   ├── 👤 user.js
│   ├── 🛡️ admin.js
│   ├── 🛡️ adminUser.js
│   └── 🎪 eventRoutes.js
├── 📂 database/
│   ├── 👥 userDB.json
│   ├── 🛡️ admin.json
│   ├── 🎪 events.json
│   └── 🎫 tickets.json
├── 📂 uploads/
│   ├── 🎪 events/
│   └── 💳 payment-proofs/
├── 📂 docs/
│   ├── 📖 documentation.html
│   └── 🎨 documentation.css
└── 🔧 server.js
```

---

## 🎨 Features Deep Dive

### 🔐 Authentication System

- **Dual Role System**: Separate authentication for users and admins
- **Secure Registration**: Validation and duplicate prevention
- **Session Management**: Stateless authentication ready

### 🎪 Event Management

- **Rich Event Creation**: Title, description, date, time, location, and images
- **Payment Integration**: Bank account details for ticket payments
- **Capacity Management**: Automatic ticket availability tracking
- **Admin Ownership**: Events tied to specific admin accounts

### 🎫 Ticket System

- **Smart Booking**: Prevents double-booking and overselling
- **Payment Verification**: Upload and verify payment proofs
- **Approval Workflow**: Admin approval/rejection system
- **Ticket Tracking**: Unique ticket numbers and status tracking

### 📸 File Upload System

- **Image Processing**: Automatic file naming and organization
- **Size Limits**: 5MB maximum for optimal performance
- **Type Validation**: Only image files accepted
- **Secure Storage**: Organized file structure with cleanup

---

## 🔧 Configuration

### Environment Variables

```env
PORT=3000
NODE_ENV=development
CORS_ORIGIN=https://your-frontend-url.com
```

### Directory Setup

The application automatically creates necessary directories:
- `database/` - JSON data files
- `uploads/events/` - Event images
- `uploads/payment-proofs/` - Payment verification files

---

## 🚀 Deployment

### GitHub Pages Documentation

1. **Enable GitHub Pages**
   - Go to repository Settings
   - Scroll to Pages section
   - Select source: Deploy from a branch
   - Choose: main branch / docs folder

2. **Access Documentation**
   - Your docs will be available at: `https://yourusername.github.io/tixlite`

### Backend Deployment Options

- **Render** - Free tier available
- **Heroku** - Easy deployment
- **Vercel** - Serverless functions
- **Railway** - Modern deployment platform

---

## 📊 API Response Examples

### ✅ Success Response

```json
{
  "message": "Event created successfully",
  "event": {
    "_id": "uuid-here",
    "title": "Summer Music Festival",
    "body": "Join us for an amazing summer experience",
    "date": "2024-08-15",
    "time": "18:00",
    "location": "Central Park",
    "tickets": 500,
    "image": "/uploads/events/event-uuid.jpg",
    "adminId": "admin-uuid",
    "paymentInfo": {
      "accountName": "Festival Organizers",
      "accountNumber": "1234567890",
      "bankName": "Example Bank"
    },
    "createdAt": "2024-01-15T10:30:00.000Z"
  }
}
```

### ❌ Error Response

```json
{
  "message": "All fields are required",
  "error": "Missing required field: title"
}
```

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

### 📝 Contribution Guidelines

- Follow the existing code style
- Add tests for new features
- Update documentation
- Ensure all tests pass

---

## 🐛 Known Issues & Roadmap

### Current Limitations
- File-based storage (JSON files)
- No real-time notifications
- Basic payment verification

### 🚧 Upcoming Features
- [ ] Database integration (MongoDB/PostgreSQL)
- [ ] Real-time notifications
- [ ] Payment gateway integration
- [ ] Email notifications
- [ ] Advanced analytics
- [ ] Multi-language support

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Express.js** community for the excellent framework
- **Node.js** team for the powerful runtime
- **GitHub Pages** for free documentation hosting
- **Contributors** who help improve this project

---

## 📞 Support & Contact

<div align="center">

[![GitHub Issues](https://img.shields.io/badge/GitHub-Issues-red?style=for-the-badge&logo=github)](https://github.com/yourusername/tixlite/issues)
[![Documentation](https://img.shields.io/badge/Docs-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://yourusername.github.io/tixlite)
[![Email](https://img.shields.io/badge/Email-Contact-green?style=for-the-badge&logo=gmail)](mailto:your-email@example.com)

</div>

---

<div align="center">
  <h3>🎫 TixLite - Making Event Management Simple</h3>
  <p>Built with ❤️ for the developer community</p>
  
  **[📖 View Documentation](https://yourusername.github.io/tixlite) | [🚀 Get Started](#-getting-started) | [🤝 Contribute](#-contributing)**
</div>

---

<div align="center">
  <sub>⭐ Star this repository if you find it helpful!</sub>
</div>
