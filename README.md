# 📊 Docebo Admin Dashboard

A **custom React + Next.js admin dashboard** for managing and visualizing **Docebo LMS** data in real-time.  
Built with **Tailwind CSS**, **Auth0 authentication**, **Recharts** for visualization, and **SWR** for smooth, real-time data fetching.

---

## 🚀 Features
- **Next.js + TypeScript** for fast, maintainable development.
- **Auth0 Authentication** with Role-Based Access Control (RBAC).
- **Docebo API Integration** for courses, users, and quizzes.
- **Responsive Dashboard Layout** with Sidebar & Navbar.
- **Data Visualization** using **Recharts**.
- **CSV & PDF Export** ready (react-csv + jsPDF).
- **Modular Architecture** for easy scaling and feature additions.

---

## 🛠 Tech Stack
| Tech | Purpose |
|------|---------|
| **Next.js** | Framework with SSR & API routes |
| **TypeScript** | Type safety |
| **Tailwind CSS** | Utility-first styling |
| **@auth0/nextjs-auth0** | Secure authentication & RBAC |
| **SWR** | Client-side data fetching & caching |
| **Recharts** | Charts & visualizations |
| **react-csv** | CSV export |
| **jspdf** & **jspdf-autotable** | PDF export |

---

## 📂 Project Structure
```
src/
│
├── pages/               # Pages & API routes
│   ├── index.tsx        # Dashboard Home
│   ├── courses.tsx      # Course Management
│   ├── api/             # API proxies to Docebo
│
├── components/          # UI components (Layout, Navbar, Sidebar, etc.)
├── hooks/               # Data fetching hooks
├── services/            # Docebo API wrapper functions
├── styles/              # Global styles
└── utils/               # Helper functions
```

---

## 🔑 Environment Variables
Create a `.env.local` file in the project root:

\`\`\`env
# Auth0 Configuration
AUTH0_SECRET=your_auth0_secret
AUTH0_BASE_URL=http://localhost:3000
AUTH0_ISSUER_BASE_URL=https://your-tenant.auth0.com
AUTH0_CLIENT_ID=your_client_id
AUTH0_CLIENT_SECRET=your_client_secret

# Docebo API
DOCEBO_TOKEN=your_docebo_token
\`\`\`

---

## 📦 Installation
\`\`\`bash
# Clone the repo
git clone https://github.com/yourusername/docebo-dashboard.git
cd docebo-dashboard

# Install dependencies
npm install
\`\`\`

---

## ▶️ Running the App
\`\`\`bash
# Start development server
npm run dev

# Build for production
npm run build
npm start
\`\`\`

Visit **http://localhost:3000** in your browser.

---

## 🔐 Authentication & RBAC
- Auth0 handles authentication via \`/api/auth/login\` and \`/api/auth/logout\`.
- API routes are wrapped with \`withApiAuthRequired\` to protect sensitive endpoints.
- Use Auth0 **roles** (\`admin\`, \`manager\`) to restrict access.

---

## 📊 Data Integration
Example API calls are set up in \`/services/docebo.ts\`:
- \`getCourses()\` → Fetches courses from Docebo.
- Extend with \`getUsers()\`, \`getQuizzes()\`, etc.

---

## 📤 Data Export
- **CSV Export** → \`react-csv\`
- **PDF Export** → \`jspdf\` + \`jspdf-autotable\`

---

## 🛣 Roadmap
- [ ] Add Recharts data visualizations
- [ ] Add User Analytics & Quiz Reporting pages
- [ ] Implement CSV/PDF export buttons
- [ ] Integrate React Query for more advanced data caching
- [ ] Dockerize for deployment

---

## 📜 License
MIT License © 2025 Sergio Montecinos
