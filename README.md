# Dev Share Server 🚀

> **The high-performance technical engine behind DevShare.**  
> Where technical intuition meets collective wisdom. This server powers a growing collective of engineers distilling complex concepts into readable insights through an advanced block-based editing experience.

---

## 🏛 Architecture & Philosophy

The DevShare backend is architected using the **Modular Pattern** (Feature-based structure). Unlike traditional monolithic structures, this approach isolates logic for Users, Blogs, and Auth into independent modules, ensuring high scalability, strict type-safety, and professional-grade maintainability.

### Key Architectural Standards:

- **Zero-Magic Numbers:** Standardized API status codes using `http-status`.
- **Strict Type-Safety:** 100% TypeScript coverage for interfaces and database models.
- **Fail-Safe Processing:** Centralized global error handling and asynchronous wrapper utilities.
- **Request Sanitization:** Schema-based validation via `Zod` before hitting controllers.

---

## 🛠 Tech Stack

| Layer          | Technology                                                                  |
| :------------- | :-------------------------------------------------------------------------- |
| **Runtime**    | [Node.js](https://nodejs.org/) (LTS)                                        |
| **Framework**  | [Express.js](https://expressjs.com/)                                        |
| **Language**   | [TypeScript](https://www.typescriptlang.org/) (Strict Mode)                 |
| **Database**   | [MongoDB](https://www.mongodb.com/) via [Mongoose](https://mongoosejs.com/) |
| **Validation** | [Zod](https://zod.dev/)                                                     |
| **Security**   | JWT, Bcrypt, CORS, Cookie-Parser                                            |

---

## 📂 System Structure

```text
devshare-server/
├── src/
│   ├── server.ts             # Entry point & DB synchronization
│   ├── app.ts                # Express application configuration
│   ├── config/               # Environment & Global variables
│   ├── app/
│   │   ├── modules/          # Feature-based logic (Modular Pattern)
│   │   │   ├── user/         # Identity & Profile management
│   │   │   └── blog/         # Content Engine (Block Editor & Deep Dives)
│   │   ├── middlewares/      # Global guards (Auth, Error Handlers)
│   │   ├── routes/           # Centralized API Router
│   │   ├── utils/            # Helpers (sendResponse, catchAsync)
│   │   └── errors/           # Custom Exception classes
│   └── shared/               # Global TypeScript interfaces
├── .env                      # Sensitive configuration (Excluded from Git)
└── tsconfig.json             # TypeScript compiler settings
```
## 🚀 Getting Started

### 1. Prerequisites
* **Node.js**: v20.x or higher
* **MongoDB**: A URI from MongoDB Atlas or a local instance.

### 2. Installation
```bash
# Clone the repository
git clone https://github.com/SafiaJotey/devshare-server.git

# Navigate to directory
cd devshare-server

# Install dependencies
npm install

```

### 3. Environment Configuration
Create a .env file in the root directory:
```bash
NODE_ENV=development
PORT=5000
DATABASE_URL=mongodb+srv://<username>:<password>@cluster.mongodb.net/devshare
```
### 4. Running the Engine
```bash

# Start development server with hot-reload
npm run dev

# Build for production
npm run build

# Start production build
npm start
```
## 🛠 Roadmap

-  **Core System:** Initial setup with Express, TypeScript, and MongoDB.
-  **Auth Node:** JWT-based Auth (Google, LinkedIn, Facebook integration).
- **Content Engine:** Advanced block-editor persistence for engineering insights.
- **Signal Check:** Technical verification middleware for code-accuracy.
-  **Analytics API:** Real-time engagement monitoring and traffic visualization.

## 🔐 Security & Validation
-  **Request Validation:** Every incoming request is validated against a Zod schema to ensure data integrity.
-  **Resilient Errors:** The server uses a centralized error handling mechanism to provide clear, technical feedback without leaking sensitive stack traces.
-  **CORS Policy:** Strict cross-origin resource sharing to protect the API from unauthorized domains.
## 🤝 Contributing
We believe the best way to master a technology is to master it together.
-  Fork the Project.
-  Create your Feature Branch (git checkout -b feature/AmazingFeature).
-  Commit your Changes (git commit -m 'Add: AmazingFeature').
-  Push to the Branch (git push origin feature/AmazingFeature).
-  Open a Pull Request.
## 📄 License
Distributed under the MIT License. See LICENSE for more information.
<p align="center">
Built with ☕ and 💻 by the <strong>Dev Share</strong> 
</p>

