# Cryptocurrency Tracker with React JS, Material UI and Chart JS

🚀 Cryptocurrency Tracker – Full Stack (MERN) Project

This is a full-stack cryptocurrency tracker built with the MERN stack. It displays real-time data for the top 10 cryptocurrencies, fetched from the CoinGecko API. Historical price data is stored hourly using a cron job and displayed via a React dashboard.


## 📦 Tech Stack Used

### 🧩 Frontend
- **React.js**
- **Material-UI** (UI components)
- **Axios** (API calls)
- **Chart.js + react-chartjs-2** (Optional: charts for price history)
- **React Router DOM**
- **React HTML Parser**
- **React Alice Carousel** (for UI animation)

### ⚙️ Backend
- **Node.js + Express**
- **Axios** (for fetching data from CoinGecko)
- **dotenv** (for environment configuration)
- **node-cron** (for hourly automation)

### 🗃️ Database
- **MongoDB** (via **MongoDB Atlas**)
- **Mongoose** ODM for schema/model creation

### 🌍 External API
- [CoinGecko API](https://www.coingecko.com/en/api)

### 🚀 Deployment
- **Frontend**: 1. Web Hosting & Deployment: Static Site Hosting:-Netlify
- **Backend**: Render
- **Database**: MongoDB Atlas

---

## 🛠️ Setup and Installation

### 1. Clone the Repository

```bash
git clone https://github.com/pritammukati/crypto-tracker.git
cd crypto-tracker
2. Backend Setup
bash
Copy
Edit
cd server
npm install
Create a .env file in /server with:

ini
Copy
Edit
PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
Run the server:

bash
Copy
Edit
node server.js
3. Frontend Setup
bash
Copy
Edit
cd ../client
npm install
npm start
The frontend will start on http://localhost:3000.

⏱ How the Cron Job Works
The project uses node-cron to automatically fetch and store crypto data every hour.

The cron job is defined in /server/cron/fetchHistory.js.

It uses fetchTopCoins() from the CoinGecko API and saves the response into the History collection in MongoDB.

Schedule: 0 * * * * (runs every hour at minute 0)

Logs are printed to the console whenever the job runs successfully or fails.

🌐 Live Demo
https://crypto-hunter.netlify.app/

Replace these URLs with your actual deployment links

📂 Folder Structure
bash
Copy
Edit
crypto-tracker/
├── client/      # React frontend
├── server/      # Express backend + MongoDB
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   ├── cron/
│   ├── services/
│   └── server.js
└── README.md

🏁 Final Notes
This project was built as a full-stack developer test for VR Automations, mimicking real-world requirements including API integration, cron automation, database modeling, and deployment. Let me know if you need the GitHub .gitignore file or bonus features like search, sort, or charting.








