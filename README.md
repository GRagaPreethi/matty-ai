🎨 Matty – Online Graphic Design Tool

Matty is a MERN Full-Stack Graphic Design Web Application that enables users to create, edit, and export professional-quality designs directly from the browser.

It acts as a one-stop design platform for creating posters, banners, social media graphics, and marketing creatives with an intuitive drag-and-drop canvas editor.

The application demonstrates modern full-stack development using the MERN stack, cloud storage, authentication, and scalable deployment.

🚀 Features
🔐 Authentication

JWT-based Login & Signup

Secure user session management

Optional Google OAuth integration

🎨 Canvas Design Editor

Drag-and-drop design elements

Add text, shapes, images

Move, resize, rotate elements

Real-time design editing

✏️ Text Styling

Font selection

Size customization

Color picker

Alignment controls

Rotation and transformations

🖼 Image Upload

Upload images directly into the canvas

Cloud storage using Cloudinary / AWS S3

↩️ Undo / Redo

Track editing actions

Navigate backward and forward in design history

💾 Save Designs

Save designs to MongoDB database

Store design metadata and JSON canvas data

Automatically generate preview thumbnails

📂 My Designs Dashboard

View all saved projects

Edit existing designs

Delete unused designs

📥 Export Options

Download designs as:

PNG

PDF

👥 Role Management

Admin role

Registered user role

🔒 Secure Data Handling

JWT authentication

Input validation

Secure CORS configuration

🛠️ Tech Stack
Frontend

React.js

Redux

TailwindCSS

react-konva / fabric.js (Canvas rendering)

Backend

Node.js

Express.js

Mongoose

Database

MongoDB Atlas

Authentication

JWT Authentication

Google OAuth (optional)

File Storage

Cloudinary

AWS S3 (optional alternative)

Deployment

Frontend: Vercel

Backend: Render / Railway

Database: MongoDB Atlas

📂 Project Structure
matty-ai-design-tool/
│
├── client/                     # React frontend
│   ├── src/
│   │   ├── components/         # UI Components (Navbar, Editor, Dashboard)
│   │   ├── pages/              # Auth, Dashboard, Editor pages
│   │   ├── redux/              # State management
│   │   ├── utils/              # Helper functions
│   │   └── App.jsx
│   └── package.json
│
├── server/                     # Node.js backend
│   ├── models/                 # Mongoose schemas
│   │   ├── User.js
│   │   └── Design.js
│   ├── routes/                 # API routes
│   ├── controllers/            # Business logic
│   ├── middleware/             # JWT validation middleware
│   ├── server.js               # Application entry point
│   └── package.json
│
├── uploads/                    # Optional local storage
├── .env.example                # Environment variables example
├── README.md
└── package.json
🗄️ Database Schema
User Model
{
  "username": "string",
  "email": "string",
  "passwordHash": "string",
  "createdAt": "date"
}
Design Model
{
  "userId": "ObjectId",
  "title": "string",
  "jsonData": "object",
  "thumbnailUrl": "string",
  "createdAt": "date"
}

jsonData stores the canvas structure from Konva/Fabric.js.

🔗 API Endpoints
Method	Endpoint	Description
POST	/api/auth/register	Register a new user
POST	/api/auth/login	Login and return JWT
GET	/api/designs	Get user's saved designs
POST	/api/designs	Save new design
PUT	/api/designs/:id	Update existing design
DELETE	/api/designs/:id	Delete design
⚡ Installation & Setup
1️⃣ Clone Repository
git clone https://github.com/your-username/matty-ai-design-tool.git
cd matty-ai-design-tool
2️⃣ Backend Setup
cd server
npm install
cp .env.example .env
npm run dev

Configure environment variables in .env.

3️⃣ Frontend Setup
cd ../client
npm install
npm start
🔑 Environment Variables

Create .env file inside the server folder.

MONGO_URI=your-mongodb-atlas-uri
JWT_SECRET=your-secret-key

CLOUDINARY_CLOUD_NAME=xxxx
CLOUDINARY_API_KEY=xxxx
CLOUDINARY_API_SECRET=xxxx
🧪 Testing
Backend Testing

Jest (Unit testing)

Supertest (API integration testing)

Manual Testing

Postman

Browser UI testing

Run tests:

npm test
🌐 Deployment
Service	Platform
Frontend	Vercel
Backend	Render / Railway
Database	MongoDB Atlas
Storage	Cloudinary
📅 Roadmap

✔ Basic canvas editor

✔ Save and load designs

✔ Export PNG/PDF

⏳ Templates gallery

⏳ Real-time collaboration (Socket.io)

⏳ Premium template marketplace

⏳ Mobile application

🔒 Security

JWT authentication

CORS protection

Input sanitization

Secure cloud file uploads

Environment variable protection

📄 License

This project is licensed under the MIT License.

👨‍💻 Author

Developed by Matty AI Team
