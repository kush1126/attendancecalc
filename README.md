# Bunk Calculator - Smart Attendance Tracking System

A comprehensive web application for students to track attendance, calculate bunkable classes, and collaborate in groups for better academic planning.

## 🚀 Features

### Core Features
- **User Authentication**: Secure login/registration with JWT tokens
- **Student Profiles**: Auto-generated student IDs with comprehensive profile management
- **Multi-step Registration**: College, course, semester, and subject selection
- **Attendance Tracking**: Real-time attendance monitoring for individual subjects
- **Bunk Calculator**: Smart calculation of safely bunkable classes while maintaining required attendance
- **Group Collaboration**: Create and join groups for collaborative attendance tracking

### Advanced Features
- **Subject-wise Calculations**: Calculate bunkable classes for specific subjects or overall course
- **Attendance Analytics**: Detailed analytics with visual indicators and status alerts
- **Group Management**: Public/private groups with invite codes
- **Real-time Updates**: Live attendance tracking and calculations
- **Responsive Design**: Modern, mobile-friendly UI with smooth animations

## 🛠️ Technology Stack

### Backend
- **Node.js** with Express.js
- **MongoDB** with Mongoose ODM
- **JWT** for authentication
- **bcryptjs** for password hashing
- **Express Validator** for input validation

### Frontend
- **React.js** with Hooks
- **React Router** for navigation
- **Axios** for API communication
- **Framer Motion** for animations
- **React Icons** for UI icons
- **React Toastify** for notifications

## 📋 Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd bunk-calculator
   ```

2. **Install backend dependencies**
   ```bash
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd client
   npm install
   cd ..
   ```

4. **Environment Setup**
   Create a `.env` file in the root directory:
   ```env
   MONGODB_URI=mongodb://localhost:27017/bunk-calculator
   JWT_SECRET=your-secret-key-here
   NODE_ENV=development
   PORT=5000
   ```

5. **Start the application**

   **Development mode:**
   ```bash
   # Terminal 1 - Start backend
   npm run dev
   
   # Terminal 2 - Start frontend
   npm run client
   ```

   **Production mode:**
   ```bash
   npm run build
   npm start
   ```

## 📱 Usage

### For Students

1. **Registration**
   - Visit the application and click "Sign Up"
   - Fill in personal information (name, email, password)
   - Select your college, course, and semester
   - Choose your subjects from the available list

2. **Dashboard**
   - View overall attendance statistics
   - See subject-wise attendance breakdown
   - Access quick actions for calculator and groups

3. **Bunk Calculator**
   - Choose between subject-specific or overall calculations
   - Enter total classes, classes held, and classes attended
   - Set required attendance percentage (default: 75%)
   - Get instant results showing bunkable classes

4. **Groups**
   - Create groups for collaborative attendance tracking
   - Join existing groups using invite codes
   - View group attendance summaries
   - Share invite codes with classmates

### For Administrators

- Monitor student attendance patterns
- View group analytics and collaboration metrics
- Manage system-wide attendance requirements

## 🏗️ Project Structure

```
bunk-calculator/
├── client/                 # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── contexts/       # React contexts
│   │   └── App.js
│   └── package.json
├── models/                 # MongoDB models
│   ├── Student.js
│   └── Group.js
├── routes/                 # API routes
│   ├── auth.js
│   ├── students.js
│   ├── groups.js
│   ├── subjects.js
│   └── attendance.js
├── server.js              # Express server
├── package.json
└── README.md
```

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/register` - Student registration
- `POST /api/auth/login` - Student login
- `GET /api/auth/me` - Get current user

### Students
- `GET /api/students/profile` - Get student profile
- `PUT /api/students/profile` - Update profile
- `POST /api/students/subjects` - Add subjects
- `PUT /api/students/subjects/:name` - Update subject data
- `GET /api/students/attendance` - Get attendance summary
- `GET /api/students/bunkable` - Calculate bunkable classes

### Groups
- `POST /api/groups` - Create group
- `GET /api/groups` - Get all groups
- `GET /api/groups/:id` - Get group details
- `POST /api/groups/:id/join` - Join group
- `POST /api/groups/:id/attendance` - Mark group attendance
- `DELETE /api/groups/:id/leave` - Leave group

### Subjects
- `GET /api/subjects/colleges` - Get colleges list
- `GET /api/subjects/courses` - Get courses list
- `GET /api/subjects/semester/:semester` - Get subjects for semester

## 🎨 Features in Detail

### Smart Bunk Calculator
- Calculates how many classes you can safely miss
- Considers remaining classes in the semester
- Provides both subject-specific and overall calculations
- Shows attendance status with color-coded indicators

### Group Collaboration
- Create study groups with classmates
- Track group attendance collectively
- Share invite codes for easy joining
- View group analytics and member progress

### Student Profiles
- Auto-generated unique student IDs
- Comprehensive academic information
- Editable personal details
- Visual attendance overview

### Real-time Analytics
- Live attendance percentage calculations
- Subject-wise breakdown
- Status indicators (Safe/At Risk)
- Progress tracking over time

## 🔒 Security Features

- JWT-based authentication
- Password hashing with bcrypt
- Input validation and sanitization
- Protected API routes
- Secure session management

## 📱 Responsive Design

- Mobile-first approach
- Cross-browser compatibility
- Smooth animations and transitions
- Intuitive user interface
- Accessibility considerations

## 🚀 Deployment

### Heroku Deployment
1. Create a Heroku account
2. Install Heroku CLI
3. Create a new Heroku app
4. Set environment variables
5. Deploy using Git

### Vercel Deployment (Frontend)
1. Connect your GitHub repository
2. Configure build settings
3. Set environment variables
4. Deploy automatically

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## 🎯 Future Enhancements

- [ ] Push notifications for attendance alerts
- [ ] Integration with college LMS systems
- [ ] Advanced analytics and reporting
- [ ] Mobile app development
- [ ] AI-powered attendance predictions
- [ ] Social features and leaderboards

---

**Built with ❤️ for students by students** 