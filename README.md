# 🚀 SMM Panel - Professional Social Media Marketing Platform

<div align="center">

![SMM Panel](https://img.shields.io/badge/SMM-Panel-blue?style=for-the-badge)
![Laravel](https://img.shields.io/badge/Laravel-11.x-red?style=for-the-badge&logo=laravel)
![PHP](https://img.shields.io/badge/PHP-8.2+-purple?style=for-the-badge&logo=php)
![MySQL](https://img.shields.io/badge/MySQL-8.0+-blue?style=for-the-badge&logo=mysql)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**Production-ready SMM Panel with Multi-Role System, Automatic Profit Margins, and Provider Integration**

[Features](#-features) • [Demo](#-demo) • [Installation](#-installation) • [Documentation](#-documentation) • [Support](#-support)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [System Requirements](#-system-requirements)
- [Quick Start](#-quick-start)
- [Project Structure](#-project-structure)
- [Configuration](#-configuration)
- [Documentation](#-documentation)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)
- [Support](#-support)

---

## 🎯 Overview

SMM Panel is a comprehensive Social Media Marketing platform that allows users to purchase social media services (followers, likes, views, etc.) with an automated order processing system. Built with security, scalability, and user experience in mind.

### Why Choose This SMM Panel?

- ✅ **Production Ready** - Battle-tested code with proper error handling
- ✅ **Multi-Role System** - Admin, Reseller, User with hierarchical profit margins
- ✅ **Automatic Profit** - Smart profit calculation and distribution
- ✅ **API Integration** - Seamless connection with SMM providers
- ✅ **Modern UI/UX** - Beautiful, responsive interface with dark/light mode
- ✅ **Secure** - Built with security best practices (CSRF, XSS, SQL Injection protection)
- ✅ **Scalable** - Queue system, caching, and optimized database queries
- ✅ **Well Documented** - Extensive documentation for setup and customization

---

## ⭐ Key Features

### 👥 User Management
- User registration and authentication
- Email verification
- Password reset functionality
- Profile management with avatar upload
- Multi-role system (Admin, Reseller, User)
- Hierarchical user structure (Admin → Reseller → User)

### 💰 Profit System
- Automatic profit margin calculation
- Role-based pricing:
  - **Admin**: Base price + admin margin
  - **Reseller**: Admin price + reseller margin
  - **User**: Full retail price
- Customizable margins per service or globally
- Real-time profit tracking and reporting
- Commission distribution for resellers

### 🛍️ Order Management
- Create orders for 100+ services
- Real-time order status tracking
- Automatic order processing via API
- Order history with detailed information
- Bulk order support
- Order cancellation and refund system
- Progress tracking with completion percentage

### 💳 Payment System
- Multiple payment methods:
  - Manual bank transfer
  - Midtrans (automatic)
  - Tripay (automatic)
  - PayPal (automatic)
- Deposit approval system for manual payments
- Automatic balance crediting for gateway payments
- Transaction history and receipts
- Payment proof upload

### 📊 Admin Dashboard
- Real-time statistics and analytics
- User management (create, edit, ban, adjust balance)
- Service management (add, edit, activate/deactivate)
- Order management and manual updates
- Deposit approval system
- Provider management
- Settings configuration
- Sales and profit reports

### 🔌 API Integration
- RESTful API for external integrations
- API key authentication
- Comprehensive API documentation
- Rate limiting for security
- Webhook support for payment callbacks
- Multiple SMM provider support

### 🎫 Support System
- Ticket-based support system
- Real-time messaging
- File attachment support
- Ticket priority levels
- Admin and user ticket management
- Email notifications

### 🔔 Notification System
- In-app notifications
- Email notifications
- Push notifications (optional)
- Notification preferences
- Real-time updates

### 📱 Responsive Design
- Mobile-first approach
- Works on all devices (desktop, tablet, mobile)
- Dark and light mode
- Modern UI with Tailwind CSS
- Smooth animations and transitions

---

## 🛠️ Technology Stack

### Backend
- **Framework**: Laravel 11.x
- **Language**: PHP 8.2+
- **Database**: MySQL 8.0+ / PostgreSQL 14+
- **Cache**: Redis 6.0+
- **Queue**: Redis Queue
- **Authentication**: Laravel Sanctum

### Frontend
- **HTML5** - Semantic markup
- **CSS**: Tailwind CSS 3.x
- **JavaScript**: Alpine.js / Vue.js 3
- **Icons**: Font Awesome 6
- **Charts**: Chart.js

### DevOps
- **Version Control**: Git
- **Package Manager**: Composer, NPM
- **Task Runner**: Laravel Mix / Vite
- **Process Manager**: Supervisor
- **Web Server**: Nginx / Apache
- **SSL**: Let's Encrypt

---

## 💻 System Requirements

### Minimum Requirements
- **OS**: Ubuntu 20.04+ / CentOS 7+ / Debian 10+
- **CPU**: 2 cores
- **RAM**: 2GB (4GB recommended)
- **Storage**: 20GB SSD
- **PHP**: 8.2 or higher
- **MySQL**: 8.0+ or PostgreSQL 14+
- **Redis**: 6.0+
- **Node.js**: 18+

### Required PHP Extensions
```
php8.2-cli, php8.2-fpm, php8.2-mysql, php8.2-mbstring, 
php8.2-xml, php8.2-curl, php8.2-zip, php8.2-gd, 
php8.2-redis, php8.2-bcmath, php8.2-intl
```

---

## 🚀 Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/yourrepo/smm-panel.git
cd smm-panel
```

### 2. Install Dependencies
```bash
composer install
npm install
```

### 3. Environment Setup
```bash
cp .env.example .env
php artisan key:generate
```

Edit `.env` file with your database and other credentials.

### 4. Database Setup
```bash
php artisan migrate
php artisan db:seed
```

### 5. Build Assets
```bash
npm run build
```

### 6. Start Development Server
```bash
php artisan serve
```

Visit `http://localhost:8000`

**Default Admin Credentials:**
- Email: `admin@smmpanel.com`
- Password: `Admin123!@#`

> ⚠️ **Important**: Change default credentials immediately after first login!

---

## 📁 Project Structure

```
smm-panel/
├── app/
│   ├── Console/          # Artisan commands
│   ├── Http/
│   │   ├── Controllers/  # Route controllers
│   │   ├── Middleware/   # Custom middleware
│   │   └── Requests/     # Form requests
│   ├── Models/           # Eloquent models
│   ├── Services/         # Business logic
│   └── Jobs/             # Queue jobs
├── config/               # Configuration files
├── database/
│   ├── migrations/       # Database migrations
│   └── seeders/          # Database seeders
├── public/               # Public assets
├── resources/
│   ├── views/            # Blade templates
│   ├── css/              # Stylesheets
│   └── js/               # JavaScript
├── routes/               # Application routes
├── storage/              # App storage
└── tests/                # Test files
```

---

## ⚙️ Configuration

### Environment Variables

#### Application
```env
APP_NAME="SMM Panel Pro"
APP_ENV=production
APP_DEBUG=false
APP_URL=https://yoursmmpanel.com
```

#### Database
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=smm_panel
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

#### Queue
```env
QUEUE_CONNECTION=redis
REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379
```

#### SMM Provider
```env
SMM_PROVIDER_URL=https://provider.com/api/v2
SMM_PROVIDER_KEY=your-api-key
```

#### Payment Gateway (Optional)
```env
MIDTRANS_SERVER_KEY=your-key
TRIPAY_API_KEY=your-key
PAYPAL_CLIENT_ID=your-id
```

---

## 📚 Documentation

Comprehensive documentation is available in the `docs/` directory:

- **[Architecture](docs/00_ARSITEKTUR_SISTEM.md)** - System architecture overview
- **[Database Schema](docs/01_DATABASE_SCHEMA.md)** - Complete database structure and ERD
- **[Folder Structure](docs/02_FOLDER_STRUCTURE.md)** - Project folder organization
- **[API Documentation](docs/03_API_DOCUMENTATION.md)** - RESTful API reference
- **[Installation Guide](docs/04_INSTALLATION_GUIDE.md)** - Step-by-step installation
- **[Deployment Guide](docs/05_DEPLOYMENT_GUIDE.md)** - Production deployment
- **[Profit System](docs/06_PROFIT_SYSTEM.md)** - How profit calculation works
- **[Provider Integration](docs/07_PROVIDER_INTEGRATION.md)** - SMM provider setup

---

## 📸 Screenshots

### User Dashboard
![Dashboard](screenshots/dashboard.png)

### Create New Order
![New Order](screenshots/new-order.png)

### Admin Panel
![Admin](screenshots/admin-panel.png)

### Services List
![Services](screenshots/services.png)

---

## 🎨 Features In-Depth

### Profit Margin System

The profit system works hierarchically:

```
Provider Price: $1.00 per 1000
│
├─ Admin Margin (20%) → $1.20
│  └─ Admin earns: $0.20
│
├─ Reseller Margin (15%) → $1.38
│  ├─ Admin earns: $0.20
│  └─ Reseller earns: $0.18
│
└─ User Price → $1.38
   Total platform profit: $0.38
```

### Order Processing Flow

```
1. User places order
2. System validates balance
3. Balance deducted
4. Order sent to provider API
5. Provider returns order ID
6. Background job checks status (every 5 min)
7. Order completed → User notified
8. Commission distributed (if reseller)
```

### Security Features

- ✅ **Authentication**: Laravel Sanctum with token-based auth
- ✅ **Authorization**: Role-based access control (RBAC)
- ✅ **CSRF Protection**: Built-in Laravel CSRF tokens
- ✅ **XSS Prevention**: Output escaping and Content Security Policy
- ✅ **SQL Injection**: Eloquent ORM with prepared statements
- ✅ **Password Security**: Bcrypt hashing (cost factor 12)
- ✅ **Rate Limiting**: Throttling for API endpoints
- ✅ **API Security**: API key authentication and validation
- ✅ **Input Validation**: Server-side validation for all inputs
- ✅ **Encryption**: Sensitive data encryption (API keys, etc.)

---

## 🧪 Testing

```bash
# Run all tests
php artisan test

# Run specific test suite
php artisan test --testsuite=Feature

# Run with coverage
php artisan test --coverage
```

---

## 🔄 Updating

```bash
# Put in maintenance mode
php artisan down

# Pull latest changes
git pull origin main

# Update dependencies
composer install --no-dev
npm install && npm run build

# Run migrations
php artisan migrate --force

# Clear and cache
php artisan optimize

# Restart queue workers
php artisan queue:restart

# Exit maintenance mode
php artisan up
```

---

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

### Development Setup

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 💬 Support

### Get Help

- 📧 **Email**: support@smmpanel.com
- 💬 **Discord**: [Join our community](https://discord.gg/smmpanel)
- 📖 **Documentation**: [docs.smmpanel.com](https://docs.smmpanel.com)
- 🐛 **Issues**: [GitHub Issues](https://github.com/yourrepo/smm-panel/issues)

### Professional Support

Need professional support, customization, or consulting?
Contact us at: business@smmpanel.com

---

## 🙏 Acknowledgments

- Laravel Framework
- Tailwind CSS
- Font Awesome
- All open-source contributors

---

## 📊 Project Status

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Maintenance](https://img.shields.io/badge/maintained-yes-green)

**Current Version**: 1.0.0  
**Last Updated**: January 2024  
**Status**: Production Ready ✅

---

<div align="center">

**Made with ❤️ for the SMM community**

[⬆ Back to Top](#-smm-panel---professional-social-media-marketing-platform)

</div>
