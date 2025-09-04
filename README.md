# 💰 Expense Tracker Backend API

A robust, secure, and scalable backend service built for a mobile **Expense Tracker Application**.  
This RESTful API manages **user authentication, financial data, and automated tasks**, providing a strong foundation for the frontend client.

---

## 🛠 Tech Stack
- **Framework**: [Node.js](https://nodejs.org/) with [Express.js](https://expressjs.com/)  
- **Database**: [PostgreSQL](https://www.postgresql.org/) (Relational storage for users, expenses, categories)  
- **Caching & Rate Limiting**: [Redis](https://redis.io/)  
- **Job Scheduling**: [Node Cron](https://www.npmjs.com/package/node-cron)  
- **Deployment**: [Render](https://render.com/)  

---

## 📚 API Endpoints

| Method | Endpoint                        | Description                                                | Auth Required | Parameters / Body                                                                 |
|--------|---------------------------------|------------------------------------------------------------|---------------|----------------------------------------------------------------------------------|
| GET    | `/api/transactions`             | Get paginated & filtered transactions for the user         | ✅            | `page`, `limit`, `category`, `startDate`, `endDate`                              |
| POST   | `/api/transactions`             | Create a new transaction                                   | ✅            | `{ title: string, amount: number, category: string }`                             |
| PUT    | `/api/transactions/:id`         | Update a specific transaction                              | ✅            | `{ title?: string, amount?: number, category?: string }`                          |
| DELETE | `/api/transactions/:id`         | Delete a specific transaction                              | ✅            | `id` (URL Parameter)                                                             |
| GET    | `/api/transactions/summary`     | Get financial summary (balance, income, expenses)          | ✅            | -                                                                                |
| GET    | `/api/transactions/categories`  | Get spending breakdown by category                         | ✅            | -                                                                                |

---

## 🚀 Features
- 🔐 Secure user authentication with JWT  
- 📊 Transaction tracking with categories  
- ⚡ Redis-based caching & request rate limiting  
- ⏰ Scheduled jobs with Node Cron  
- 🌐 Ready for deployment on Render  

---

## 🏗️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Vinaykumarkajjapu2311/ExpenseTrackerReactNativeApp.git
   cd src
