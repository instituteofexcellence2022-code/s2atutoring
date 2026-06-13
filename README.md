# S2A Tutoring – Premium Home Tuition Website

S2A Tutoring is a premium, modern, mobile-first home tuition agency website offering personalized one-to-one tuition services in the Delhi NCR region. Built with the latest React and Next.js technology, the platform is designed to convert visitors into students and attract elite tutors.

---

## 🌟 Features

- **Ultra-Premium Visuals**: Sleek dark/light theme, modern typography (Outfit/Inter), glassmorphism cards, and fluid Framer Motion animations.
- **Production-Ready Serverless Architecture**: Fully compatible with Vercel and serverless database systems (no disk writes, zero CORS issues).
- **Free-Tier Friendly**: Uses free resources for database (Neon/Supabase) and transaction emails (Resend).
- **Serverless Resume Upload**: Client-side Base64 resume file encoding, stored securely in PostgreSQL and attached directly to admin email notifications.
- **SEO Optimized**: Dynamic `sitemap.xml`, `robots.txt`, schema markup (`LocalBusiness`, `EducationalOrganization`, `FAQPage`), and strict semantic HTML.
- **Secure Lead Capture**: Spam protection using Honeypots and in-memory rate limiting.

---

## 🛠️ Tech Stack

- **Framework**: Next.js 16 (App Router, Server Actions, Dynamic API Routes)
- **Styling**: Tailwind CSS v4, Lucide Icons, next-themes
- **Animations**: Framer Motion
- **Database**: Prisma ORM, PostgreSQL
- **Email Delivery**: Resend SDK
- **Forms & Validation**: React Hook Form, Zod Validation

---

## 🚀 Quick Start (Local Setup)

### 1. Clone the repository
```bash
git clone https://github.com/instituteofexcellence2022-code/s2atutoring.git
cd s2atutoring
```

### 2. Install dependencies
```bash
npm install
```

### 3. Setup environment variables
Copy `.env.example` to `.env` and fill in your credentials:
```bash
cp .env.example .env
```

Ensure you have your PostgreSQL Database URL and Resend API Key inside `.env`.

### 4. Setup the database schema
Prisma will sync the models directly to your PostgreSQL database:
```bash
npx prisma db push
```

### 5. Start the development server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) to view the application.

---

## 🔑 Environment Variables Configuration

| Variable | Description | Provider / Value |
| :--- | :--- | :--- |
| `DATABASE_URL` | PostgreSQL connection string | Neon, Supabase, Railway (Free tier database) |
| `RESEND_API_KEY` | Transactional email API key | [Resend](https://resend.com) (100 free emails/day) |
| `NEXT_PUBLIC_APP_URL` | The production URL of your website | e.g. `https://s2atutoring.com` |
| `ADMIN_EMAIL` | Destination email for leads and tutor applications | e.g. `support@s2atutoring.com` |

---

## 📦 Production Deployment (Vercel)

1. **Deploy Repository**: Push your code to GitHub.
2. **Create Vercel Project**: Link your GitHub repository to [Vercel](https://vercel.com).
3. **Configure Environment Variables**: Add `DATABASE_URL`, `RESEND_API_KEY`, `NEXT_PUBLIC_APP_URL`, and `ADMIN_EMAIL` in the Vercel project settings.
4. **Deploy**: Click **Deploy**. Vercel will build and host the application.
5. **Database Initialization**: Run `npx prisma db push` locally pointed to your production `DATABASE_URL` (or configure a GitHub action) to ensure the table schema is provisioned.

---

## 📁 Project Structure

```
s2a-tutoring/
├── prisma/
│   └── schema.prisma                # Database Schema Definitions
├── public/                          # Static Assets
└── src/
    ├── actions/                     # Next.js Server Actions (Leads, Tutors)
    ├── app/
    │   ├── api/
    │   │   └── resumes/[id]/        # Decodes & downloads resumes from database
    │   ├── layout.tsx               # Root Layout, global metadata & providers
    │   ├── globals.css              # Custom Tailwind configuration
    │   └── page.tsx                 # Main entry point rendering all sections
    ├── components/
    │   ├── layout/                  # Navbar, Footer, ScrollProgress
    │   ├── sections/                # Modular landing page sections
    │   └── shared/                  # Common icons and buttons
    └── lib/                         # Helpers (Prisma client, rate-limit, resend client)
```

---

## 📧 Contact & Support

- **Email**: [support@s2atutoring.com](mailto:support@s2atutoring.com)
- **Phone**: +91 8287549367
- **Coverage**: Delhi NCR, India
