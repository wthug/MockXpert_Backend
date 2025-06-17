# **🔥 MockXpert 🔥**  

## 🌍 Overview  
Welcome to **Dev Heat Backend** – the powerhouse behind our interview management system! This backend is responsible for **user authentication, interview data handling, and email notifications**, ensuring a smooth experience for all users.  

Built with **Node.js, Express, MongoDB, and JWT authentication**, this project efficiently manages interview-related data while maintaining security and scalability.  

---

## 📁 **Project Structure**  

```
Interview_Whiz_Backend/
│── cache/             # Caching mechanisms
│   ├── mailcache.js   # Cache for email operations
│
│── controllers/       # Handles request logic  
│   ├── analysisController.js  # Analysis operations
│   ├── feedbackController.js  # User feedback handling
│   ├── interviewController.js # Interview-related operations
│   ├── mailController.js      # Manages email operations  
│   ├── questionController.js  # Question management
│   ├── resetPass.js           # Password reset operations
│   ├── resourceController.js  # Resource management
│   ├── userController.js      # Handles user-related operations  
│  
│── db/                # Database connection setup  
│   ├── connect.js     # Database connection logic
│  
│── lib/               # External library integrations
│   ├── cloudinary.js  # Cloudinary integration for media
│
│── middleware/        # Middleware functions  
│   ├── auth.middleware.js    # Auth middleware (JWT)  
│  
│── models/            # Database models  
│   ├── interview.js   # Schema for interview data  
│   ├── resources.js   # Schema for resources
│   ├── userModel.js   # Schema for user data  
│  
│── routes/            # API routes  
│   ├── forgetPassRoute.js    # Password reset routes
│   ├── interviewRoutes.js    # Interview-related routes
│   ├── portal.js             # Portal access routes
│   ├── resourceRoutes.js     # Resource management routes
│   ├── userRoute.js          # User-related routes  
│   ├── verify.js             # User verification logic  
│  
│── utils/             # Helper functions  
│   ├── cleanMarkdown.js      # Markdown processing
│   ├── generateOtp.js        # OTP generation
│   ├── generateToken.js      # JWT token generation
│   ├── openaiClient.js       # OpenAI API integration
│   ├── pdfGenerator.js       # PDF creation utility
│   ├── randString.js         # Generates random strings  
│   ├── sendEmail.js          # Email sending logic  
│  
│── .env               # Environment variables (ignored in Git)  
│── .gitignore         # Files to exclude from version control  
│── package-lock.json  # Dependency lock file
│── package.json       # Project metadata & dependencies  
│── server.js          # Main server file (entry point)  
│── README.md          # Documentation
```

---

## Backend Flow
![Image](https://github.com/user-attachments/assets/92ad4d5c-0609-4d2f-b7b4-5d99d31f45ea)

## 🚀 **Getting Started**  

### **🔹 Prerequisites**  
Before you begin, ensure you have:  
✅ **Node.js** installed (v14+ recommended)  
✅ **MongoDB** installed (or use MongoDB Atlas)  
✅ A `.env` file with the necessary credentials  

### **🔹 Installation**  
Clone this repository and install dependencies:  
```sh
git clone https://github.com/your-repo/dev_heat_backend.git
cd Dev_Heat_Backend
npm install
```

### **🔹 Environment Variables**  
Create a `.env` file in the root directory and configure your environment:  
```env
PORT=5000  
MONGO_URI=your_mongodb_connection_string  
JWT_SECRET=your_secret_key  
EMAIL_SERVICE=your_email_service  
EMAIL_USER=your_email  
EMAIL_PASS=your_email_password  
CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
OPENAI_API_KEY=your_openai_api_key 
```

### **🔹 Running the Server**  
Start the development server:  
```sh
npm run dev
```  
For production:  
```sh
npm start
```

---

## 🎯 **API Endpoints**  

### **🔑 Authentication & User Management**  
| Method | Endpoint                | Description                 |
|--------|-------------------------|-----------------------------|
| **POST** | `/api/user/register`   | Register new user           |
| **POST** | `/api/user/login`      | User login                  |
| **GET**  | `/api/user/profile`    | Get user profile            |
| **PUT**  | `/api/user/profile`    | Update user profile         |
| **GET**  | `/api/verify`          | Verify user account         |
| **POST** | `/api/reset/request`   | Request password reset      |
| **POST** | `/api/reset/verify`    | Verify reset OTP            |
| **POST** | `/api/reset/password`  | Set new password            |

### **📋 Interview Management**  
| Method | Endpoint                      | Description                      |
|--------|-------------------------------|----------------------------------|
| **GET**  | `/api/interview/questions`   | Get interview questions          |
| **POST** | `/api/interview/submit`      | Submit interview responses       |
| **GET**  | `/api/interview/results`     | Get interview results            |
| **GET**  | `/api/interview/history`     | Get past interview history       |
| **POST** | `/api/interview/feedback`    | Submit feedback on interview     |

### **📚 Resource Management**  
| Method | Endpoint                      | Description                      |
|--------|-------------------------------|----------------------------------|
| **GET**  | `/api/resources/all`         | Get all learning resources       |
| **GET**  | `/api/resources/category/:id`| Get resources by category        |
| **GET**  | `/api/resources/:id`         | Get specific resource            |
| **POST** | `/api/resources/download`    | Generate and download resource   |

### **🖥️ Portal Access**  
| Method | Endpoint                      | Description                      |
|--------|-------------------------------|----------------------------------|
| **GET**  | `/api/portal/dashboard`      | Access user dashboard            |
| **GET**  | `/api/portal/analytics`      | Get user analytics               |
| **GET**  | `/api/portal/recommendations`| Get recommended resources        |
---

## 🛠 **Built With**  

🚀 **Node.js & Express.js** - Backend Framework  
📦 **MongoDB & Mongoose** - Database & ORM  
🔐 **JWT** - Secure authentication  
📩 **Nodemailer** - Email service  
☁️ Cloudinary - Media management
🤖 OpenAI - AI-powered analysis
📄 PDF Generation - Resource creation
🛠 dotenv - Environment variable management
🛠 **dotenv** - Environment variable management  

---

## 👥 **Contributing**  
We welcome contributions! 💡 If you have ideas for improvement, feel free to:  
✅ Fork the repo  
✅ Create a new branch  
✅ Submit a pull request  
---

## 📜 **License**  
This project is open-source and available under the **MIT License**.  

---

💡 **Made with ❤️ for Dev Heat!** 🚀 Let’s build something awesome together!  
