🚀 MERN CRUD App - Backend (Node.js + Express)

This is the backend of the MERN (MongoDB, Express, React, Node.js) CRUD application. It provides RESTful APIs to interact with a MongoDB database and is deployed on an AWS EC2 instance using CI/CD via GitHub Actions.

🌐 API Endpoint

Base URL: http://<your-ec2-public-ip>:5000

🎓 Features

CRUD APIs (Create, Read, Update, Delete)

MongoDB Integration

CORS enabled for frontend interaction

Environment variable configuration

🔧 Technologies Used

Node.js

Express.js

MongoDB Atlas / EC2 Mongo

Mongoose

dotenv

GitHub Actions (CI/CD)

🔄 Folder Structure

backend/
├── models/
│   └── Item.js
├── routes/
│   └── items.js
├── server.js
├── .env
├── package.json
└── README.md

🔧 Getting Started (Local Setup)

Clone the repository

git clone https://github.com/SumangalChhetri/mern-crud-backend.git
cd mern-crud-backend

Install dependencies

npm install

Set environment variablesCreate a .env file with:

MONGO_URI=your-mongodb-connection-uri
PORT=5000

Start the development server

npm run dev

🛠 Available Scripts

npm run dev: Run the server in development using nodemon

npm start: Start server in production mode

🌍 Deployment (AWS EC2)

Backend is deployed to an Ubuntu EC2 instance

Node app runs via PM2 process manager

Optional: Can set up Nginx as a reverse proxy

Required:

Open port 5000 in EC2 Security Groups

SSH access setup

🚧 CI/CD Setup

GitHub Actions Workflow (.github/workflows/deploy-backend.yml)

On every push to master, GitHub connects to EC2 via SSH, deploys the latest code, installs dependencies, and restarts the backend using PM2.

Required Secrets in GitHub Repo:

EC2_HOST: Public IP of EC2

USERNAME: EC2 username (e.g., ubuntu)

EC2_SSH_PRIVATE_KEY: Your PEM private key (add it as a GitHub Secret)

💸 Cost Optimization

Used t2.micro EC2 instance (eligible for AWS Free Tier)

Avoided EBS or large storage allocations

No unnecessary services running

Estimated monthly cost: ~$0.06/month

Budget set using AWS Budgets with $10/month threshold

👤 Author

Sumangal ChhetriGitHub: SumangalChhetri

🔒 License

This project is licensed under the MIT License.

