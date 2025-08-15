# Organ-Donation-System
🫀 OrganLink – Organ Donation Management System
A humane, secure, and scalable platform connecting donors, recipients, and hospitals.



Mission: Streamline the organ donation process—register donors, match recipients, and coordinate hospitals with privacy, transparency, and trust.
✨ Features at a Glance
🪪 Role-based access: Donor, Recipient, Hospital, Admin
🧬 Smart matching engine: Blood group, organ type, HLA tags (optional), urgency & location
📝 Secure registrations: Donor pledges, recipient requests, consent workflows
🏥 Hospital dashboard: Verify cases, update organ availability, manage waitlists
🔍 Powerful search: Filter by organ type, city, blood group, status
🔔 Email notifications: Status changes, verifications, matched availability (via Nodemailer)
🔐 Security first: Hashed passwords, JWT auth, input validation, rate limiting
📊 Audit & logs: Actions tracked for compliance (admin-only view)
🌗 Modern UI: Clean HTML/CSS with responsive layout & dark mode toggle
🗂️ Project Structure
organlink/
├─ client/
│  ├─ assets/
│  │  ├─ css/      # base.css, theme.css, components.css
│  │  └─ js/       # app.js, auth.js, donate.js, request.js
│  ├─ images/
│  └─ views/       # HTML pages (no framework): index.html, login.html, ...
├─ server/
│  ├─ src/
│  │  ├─ config/   # db.js, mailer.js, logger.js
│  │  ├─ middleware/ # auth.js, roles.js, limiter.js, validator.js
│  │  ├─ models/   # User.js, Donor.js, Recipient.js, Hospital.js, Match.js
│  │  ├─ routes/   # auth.routes.js, donor.routes.js, recipient.routes.js, ...
│  │  ├─ services/ # match.service.js, mail.service.js
│  │  └─ app.js
│  └─ tests/       # supertest routes, unit tests
├─ .env.example
├─ package.json
├─ README.md
└─ Dockerfile (optional)
🧰 Tech Stack
Frontend: HTML, CSS (custom), Vanilla JS
Backend: Node.js, Express
Database: MongoDB (Mongoose)
Auth: JWT + Bcrypt
Mail: Nodemailer (SMTP)
Dev Tools: ESLint, Prettier, Jest/Supertest (optional), Nodemon
🚀 Quick Start
1) Clone & Install
git clone https://github.com/your-username/organlink.git
cd organlink
npm install
2) Configure Environment
Create .env (copy from .env.example):
PORT=8080
MONGO_URI=mongodb://localhost:27017/organlink
JWT_SECRET=supersecretlongrandomstring
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@example.com
SMTP_PASS=app_password
BASE_URL=http://localhost:8080
3) Run Dev Server
npm run dev
# or
node server/src/app.js
Open: http://localhost:8080
🌐 Frontend Pages (HTML/CSS/JS)
index.html – Landing page with CTAs (Become a Donor / Request Organ / Hospital Login)
register-donor.html – Donor pledge form (organ type, blood group, city, consent)
request-recipient.html – Recipient request form (organ needed, urgency, blood group, hospital)
hospital-dashboard.html – Manage waitlists, verify donors/recipients, mark availability
login.html / signup.html – Auth with role selection
search.html – Explore donors & organs with filters and pagination
All pages are static HTML consuming REST APIs via fetch(). Clean CSS with responsive grid, cards, and dark mode.
