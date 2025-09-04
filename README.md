Expense Tracker Backend API
A robust, secure, and scalable backend service built for a mobile expense tracker application. This RESTful API handles user authentication, financial data management, and automated tasks, providing a solid foundation for the frontend client.

🛠 Tech Stack
Framework: Node.js with Express.js

Database: PostgreSQL (Relational data storage for users, expenses, categories)

Caching & Rate Limiting: Redis

Job Scheduling: Node Cron (for cron jobs)

Deployment: Render (PaaS)

📚 API Endpoints
Method	Endpoint	Description	Auth Required	Parameters/Body
GET	/api/transactions	Get paginated & filtered transactions for the authenticated user.	✅	page, limit, category, startDate, endDate
POST	/api/transactions	Create a new transaction.	✅	{ title: string, amount: number, category: string }
PUT	/api/transactions/:id	Update a specific transaction.	✅	{ title?: string, amount?: number, category?: string }
DELETE	/api/transactions/:id	Delete a specific transaction.	✅	id (URL Parameter)
GET	/api/transactions/summary	Get financial summary (balance, income, expenses) for the user.	✅	-
GET	/api/transactions/categories	Get spending breakdown by category.	✅
