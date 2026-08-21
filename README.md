Prep-Mate 🚀

Prep-Mate is an AI-powered interview preparation web application that helps candidates prepare for job interviews based on their resume, self-description, and target job description.

The application analyzes the candidate's profile against the job description and generates a personalized interview preparation strategy, including a match score, skill gaps, technical questions, behavioral questions, model answers, and a day-by-day preparation roadmap.

It can also generate an ATS-friendly resume PDF tailored to the target job.

✨ Features
🔐 User Authentication
User registration
User login and logout
Password hashing using bcrypt
JWT-based authentication
HTTP-only authentication cookies
Protected API routes
Token blacklist support for logout
🤖 AI-Powered Interview Analysis
Analyze candidate resume
Accept candidate self-description
Analyze target job description
Generate a personalized interview report using Google Gemini
Calculate a candidate-job match score
Identify important skill gaps
Classify skill gaps by severity
💻 Technical Interview Preparation
Generate role-specific technical interview questions
Provide the intention behind each question
Provide model answers and important points to cover
🗣️ Behavioral Interview Preparation
Generate personalized behavioral questions
Explain the interviewer's intention
Provide suggested/model answers
🗺️ Preparation Roadmap
Generate a day-by-day interview preparation plan
Define the focus for each day
Provide tasks for each preparation day
📄 AI Resume Generation
Generate a tailored resume based on the candidate's profile and job description
Generate ATS-friendly resume content
Convert generated HTML resume content into PDF
Download the generated resume as a PDF
📊 Interview Reports
Save generated interview reports
View previous interview plans
Display match scores
Open individual interview reports
View technical questions, behavioral questions, skill gaps, and preparation roadmap
📎 Resume Upload
Upload resume in PDF format
Extract resume text using pdf-parse
Resume files are processed in memory
Maximum upload size is 3 MB

🛠️ Technologies Used
Frontend
React
Vite
JavaScript
React Router
Axios
SCSS / Sass
HTML
CSS

Backend
Node.js
Express.js
JavaScript (ES Modules)
JWT
bcryptjs
Multer
PDF Parse
Puppeteer
Database
MongoDB
Mongoose
AI
Google Gemini API
@google/genai
Zod for structured AI response validation
Development Tools
Git
GitHub
Nodemon
ESLint


🏗️ Project Architecture

Prep-Mate is divided into two main applications:

Prep-Mate/
│
├── Backend/
│   ├── src/
│   │   ├── config/
│   │   │   └── db.js
│   │   │
│   │   ├── controllers/
│   │   │   ├── auth.controller.js
│   │   │   └── interview.controller.js
│   │   │
│   │   ├── middlewares/
│   │   │   ├── auth.middleware.js
│   │   │   └── file.middleware.js
│   │   │
│   │   ├── models/
│   │   │   ├── blacklist.model.js
│   │   │   ├── interviewReport.model.js
│   │   │   └── user.model.js
│   │   │
│   │   ├── routes/
│   │   │   ├── auth.routes.js
│   │   │   └── interview.routes.js
│   │   │
│   │   └── services/
│   │       └── ai.service.js
│   │
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── Frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── featues/
│   │   │   ├── auth/
│   │   │   ├── interview/
│   │   │   └── landing/
│   │   ├── App.jsx
│   │   ├── app.routes.jsx
│   │   ├── main.jsx
│   │   └── style.scss
│   │
│   ├── public/
│   ├── package.json
│   └── .env
│
└── README.md

🔄 How Prep-Mate Works
Candidate
   │
   ├── Resume PDF
   ├── Self Description
   └── Job Description
          │
          ▼
     Prep-Mate
          │
          ▼
     Resume Text Extraction
          │
          ▼
      Google Gemini AI
          │
          ├── Match Score
          ├── Skill Gaps
          ├── Technical Questions
          ├── Behavioral Questions
          └── Preparation Roadmap
          │
          ▼
    Interview Report
          │
          ├── View Report
          └── Generate Resume PDF