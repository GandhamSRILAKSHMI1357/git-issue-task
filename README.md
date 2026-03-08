# MEDPlat - Healthcare Platform

## 📋 Overview

**MEDPlat** is a comprehensive healthcare platform that brings the simplicity and power of low-code technologies to healthcare implementations. It is a point-of-care application that provides a seamless interface for healthcare providers through both mobile and web applications. The platform completely digitizes care delivery and management across all stakeholders including doctors, healthcare workers, patients, and administrators.

MEDPlat enables healthcare organizations to:
- Manage patient records digitally
- Track healthcare services and delivery points
- Manage announcements and notifications
- Generate comprehensive reports
- Access services through mobile and web interfaces

---

## ✨ Key Features

### 📱 Mobile Application (Android)
- Responsive point-of-care mobile interface
- Offline functionality for low-connectivity scenarios
- Real-time synchronization with the backend
- User-friendly navigation
- Push notifications support

### 🌐 Web Interface
- Comprehensive dashboard for healthcare administrators
- Patient record management
- Role-based access control (RBAC)
- Advanced reporting and analytics
- Announcement and messaging system
- Multi-language support (i18n)

### 🎯 Core Functionalities
- **Patient Management**: Create, read, update, and delete patient records
- **Healthcare Services**: Manage various healthcare delivery services
- **Administration**: User, role, and permission management
- **Reporting**: Generate detailed healthcare reports
- **Notifications**: Push notifications and in-app messaging
- **Multi-language Support**: Internationalization (i18n) ready

---

## 📁 Project Structure

```
medplat/
├── medplat-android/          # Android mobile application
│   ├── sewa-android/         # Main Android app module
│   ├── build.gradle          # Gradle build configuration
│   └── gradle/               # Gradle wrapper
│
├── medplat-ui/               # Web UI (AngularJS frontend)
│   ├── app/                  # Application code
│   │   ├── admin/            # Admin module
│   │   │   ├── applicationmanagement/
│   │   │   ├── drtecho/
│   │   │   ├── labelstranslation/
│   │   │   ├── pushnotification/
│   │   │   └── report/
│   │   ├── login/            # Authentication module
│   │   ├── manage/           # Manage module
│   │   ├── common/           # Shared components
│   │   │   ├── components/
│   │   │   ├── services/
│   │   │   ├── controllers/
│   │   │   ├── directives/
│   │   │   └── filters/
│   │   └── [other modules]
│   ├── styles/               # CSS styles
│   ├── img/                  # Images and icons
│   ├── index.html            # Main HTML file
│   ├── package.json          # NPM dependencies
│   └── Gruntfile.js          # Grunt build configuration
│
├── medplat-web/              # Backend API (Java)
│   ├── src/main/             # Java source code
│   ├── pom.xml               # Maven build configuration
│   └── Dockerfile.back       # Docker configuration
│
├── Documents/                # Documentation files
│   ├── Architecture Diagram/
│   └── medplat-documentation.html
│
├── docker-compose.yml        # Docker compose for local development
├── Dockerfile                # Main Docker image
├── entrypoint.sh             # Application entry point
└── README.md                 # This file
```

---

## 🛠 Technologies Used

### Frontend (Web UI)
- **Framework**: AngularJS
- **Build Tool**: Grunt
- **Package Manager**: npm, bower
- **Languages**: JavaScript, HTML5, CSS3
- **HTTP Client**: Custom HTTP interceptors
- **Routing**: Custom AngularJS router

### Mobile (Android)
- **Platform**: Android
- **Build Tool**: Gradle
- **Language**: Java/Kotlin
- **UI Framework**: Android native

### Backend (Web API)
- **Framework**: Java (likely Spring-based)
- **Build Tool**: Maven
- **Database**: SQL (based on migration files)

### DevOps
- **Containerization**: Docker
- **Orchestration**: Docker Compose
- **Version Control**: Git

---

## 🚀 Getting Started

### Prerequisites
- Git
- Docker & Docker Compose (for containerized setup)
- Node.js 12+ (for frontend development)
- Java 8+ (for backend development)
- Android SDK (for mobile development)
- Maven 3.6+ (for backend)
- Gradle 6.0+ (for Android)

### Installation

#### Option 1: Using Docker (Recommended)

```bash
# Clone the repository
git clone https://github.com/GandhamSRILAKSHMI1357/git-issue-task.git
cd medplat

# Start the application using docker-compose
docker-compose up -d

# Application will be available at:
# Web UI: http://localhost:8080
# API: http://localhost:8080/api
```

#### Option 2: Local Development Setup

**Backend Setup:**
```bash
cd medplat-web
mvn clean install
mvn spring-boot:run
```

**Frontend Setup:**
```bash
cd medplat-ui
npm install
bower install
grunt serve
```

**Android Setup:**
```bash
cd medplat-android
gradle build
# Open in Android Studio for development
```

---

## 📖 Usage Guide

### Web Application

1. **Login**: Access the application at `http://localhost:8080`
   - Enter your credentials
   - Multi-role login supported

2. **Dashboard**: View key metrics and statistics
   - Patient counts
   - Service delivery status
   - Recent activities

3. **Patient Management**:
   - Navigate to Manage → Patient
   - Create new patient records
   - View and update patient information
   - Track patient history

4. **Administration**:
   - User management
   - Role-based access control
   - System configuration
   - Report generation

### Mobile Application

1. **Install APK**: Build or install from release
2. **Login**: Use same credentials as web app
3. **Point-of-Care**: Use mobile app for on-field healthcare delivery
4. **Offline Mode**: Works without internet connection
5. **Sync**: Automatically syncs when connection is restored

---

## 🔧 Configuration

### Environment Variables
Create a `.env` file or configure via Docker environment:

```
DATABASE_URL=jdbc:mysql://localhost:3306/medplat
DATABASE_USER=root
DATABASE_PASSWORD=password
APP_NAME=MEDPlat
PORT=8080
```

### Database Setup
SQL migration scripts are provided in `medplat-web/src/main/resources/`:
- V1__init.sql - Initial schema
- V2__query_master.sql - Query templates
- And more...

Run migrations via Maven or manually execute SQL scripts.

---

## 🧪 Testing

### Frontend Tests
```bash
cd medplat-ui
npm test
```

### Backend Tests
```bash
cd medplat-web
mvn test
```

### AndroidTests
```bash
cd medplat-android
gradle test
```

---

## 📝 Common Modules

### Admin Module
- Application Management
- Dr. Echo (telemedicine features)
- Label Translation
- Menu Feature Management
- My Techo
- Push Notifications
- Report Generation
- Role Management
- SOH (State of Health)
- Values and Multimedia

### Manage Module
- Administration settings
- Anganwadi (nutrition programs)
- Announcements
- Healthcare services
- And more...

### Common Module
- Shared components
- Reusable services
- HTTP interceptors
- Utility filters
- Directives

---

## 🌍 Multi-Language Support

The platform supports internationalization (i18n) for multiple languages. Labels and text can be translated via the Admin → Label Translation interface.

---

## 🤝 Contributing

Contributions are welcome! Follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit changes: `git commit -am 'Add new feature'`
4. Push to branch: `git push origin feature/your-feature`
5. Submit a Pull Request

### Coding Standards
- Follow existing code style
- Write clear commit messages
- Add tests for new features
- Update documentation

---

## 🐛 Known Issues

- Some Android features require specific device capabilities
- Web interface works best on desktop browsers
- Offline sync may have delays with large datasets

---

## 📄 License

This project is licensed under the terms specified in the LICENSE file.

---

## 📞 Support & Documentation

- Full documentation available in `Documents/medplat-documentation.html`
- Architecture diagrams in `Documents/Architecture Diagram/`
- User guides available in `medplat-ui/MOCK_DATA.json`

---

## 🙏 Acknowledgments

MEDPlat is maintained by the open-source community and healthcare technology contributors. Special thanks to all contributors and organizations supporting this project.

---

**Last Updated**: March 2026
**Repository**: https://github.com/GandhamSRILAKSHMI1357/git-issue-task
