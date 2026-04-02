# 🎬 CineTube — Movie & Series Rating Portal

A full-stack Movie and Series Rating Portal where users can explore, rate, and review movies and TV series. Admins manage the media library and moderate user-generated content.

![CineTube](https://tube-client.vercel.app/og-image.png)

---

## 🔗 Live Links

| Service | URL |
|---|---|
| 🌐 Frontend | [https://project-frontend.vercel.app](https://project-frontend.vercel.app) |
| ⚙️ Backend API | [https://tube-server.onrender.com](https://tube-server.onrender.com) |
| 📁 Frontend Repo | [https://github.com/HST159075/Tube-client](https://github.com/HST159075/Tube-client) |
| 📁 Backend Repo | [https://github.com/HST159075/Tube-server](https://github.com/HST159075/Tube-server) |
| 🎥 Demo Video | _Coming soon_ |

---

## 🔐 Admin Credentials

```
Email:    alam18@gmail.com
Password: (add your password here)
```

---

## ✨ Features

### 👤 User
- Register & login with email/password or Google OAuth
- Browse movies & series by genre, platform, rating, year
- Rate titles on a **1–10 scale** and write reviews
- Add **spoiler warnings** and **tags** to reviews
- Like/unlike reviews and comment on them
- Save titles to a personal **Watchlist**
- Edit/delete own unpublished reviews
- **Subscribe** for premium content via SSLCommerz

### ⚡ Admin
- Add, edit, delete movies/series in the media library
- Approve or unpublish user reviews
- View all users and manage their accounts
- View aggregated stats (total users, titles, subscribers)
- Access pending reviews and moderate content

---

## 📄 Pages

| Page | Route |
|---|---|
| Home | `/` |
| Browse Movies | `/movies` |
| Movie Details | `/movies/[id]` |
| Login | `/login` |
| Register | `/register` |
| Profile | `/profile` |
| Subscription | `/subscription` |
| Admin Dashboard | `/admin/dashboard` |
| Payment Success | `/payment/success` |
| Payment Failed | `/payment/failed` |
| About | `/about` |
| Contact | `/contact` |
| FAQ | `/faq` |
| Privacy Policy | `/privacy` |

---

## 🛠️ Tech Stack

### Frontend
- **Next.js 14** (App Router)
- **TypeScript**
- **Better Auth** (Authentication)

### Backend
- **Node.js** + **Express.js**
- **Prisma ORM**
- **PostgreSQL**
- **JWT Authentication**
- **SSLCommerz** (Payment Gateway)

### Deployment
- Frontend → **Vercel**
- Backend → **Render**
- Database → **PostgreSQL** (Render / Supabase)

---

## ⚙️ Local Setup

### Prerequisites
- Node.js v18+
- PostgreSQL database
- SSLCommerz sandbox account

---

### 1. Clone Repositories

```bash
# Frontend
git clone https://github.com/HST159075/Tube-client.git
cd Tube-client

# Backend
git clone https://github.com/HST159075/Tube-server.git
cd Tube-server
```

---

### 2. Backend Setup

```bash
cd Tube-server
npm install
```

Create `.env` file:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/cinetube
JWT_SECRET=your_jwt_secret

BETTER_AUTH_SECRET=your_better_auth_secret
BETTER_AUTH_URL=http://localhost:5000

FRONTEND_URL=http://localhost:3000
BACKEND_URL=http://localhost:5000

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret

SSL_STORE_ID=your_sslcommerz_store_id
SSL_STORE_PASSWORD=your_sslcommerz_store_password
```

Run migrations and start:

```bash
npx prisma migrate dev
npx prisma db seed   # optional: seed sample data
npm run dev
```

Backend runs on → `http://localhost:5000`

---

### 3. Frontend Setup

```bash
cd Tube-client
npm install
```

Create `.env.local` file:

```env
NEXT_PUBLIC_API_URL=http://localhost:5000/api/v1
BETTER_AUTH_SECRET=your_better_auth_secret
BETTER_AUTH_URL=http://localhost:3000
```

Start:

```bash
npm run dev
```

Frontend runs on → `http://localhost:3000`

---

## 💳 Payment Integration

Payments are handled via **SSLCommerz** (Bangladesh's #1 payment gateway).

Supported methods:
- bKash, Nagad, Rocket
- Credit / Debit Cards
- All major mobile banking

### Subscription Plans
| Plan | Price | Duration |
|---|---|---|
| Free | ৳0 | Forever |
| Monthly | ৳299 | 1 Month |
| Yearly | ৳2,499 | 1 Year (2 months free) |

---

## 📡 API Endpoints

### Auth
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/v1/auth/register` | Register user |
| POST | `/api/v1/auth/login` | Login user |

### Media
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/v1/media` | Get all media |
| GET | `/api/v1/media/:id` | Get single media |
| POST | `/api/v1/media` | Add media (Admin) |
| PUT | `/api/v1/media/:id` | Update media (Admin) |
| DELETE | `/api/v1/media/:id` | Delete media (Admin) |

### Reviews
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/v1/reviews?mediaId=` | Get reviews by media |
| POST | `/api/v1/reviews` | Submit review |
| PATCH | `/api/v1/reviews/approve/:id` | Approve review (Admin) |
| DELETE | `/api/v1/reviews/:id` | Delete review |

### Users
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/v1/users/admin/all-users` | All users (Admin) |
| GET | `/api/v1/users/admin/stats` | Dashboard stats (Admin) |
| DELETE | `/api/v1/users/:id` | Delete user (Admin) |

### Payment
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/v1/payment/create-checkout` | Initiate SSLCommerz payment |
| POST | `/api/v1/payment/success` | Payment success callback |
| POST | `/api/v1/payment/fail` | Payment fail callback |

### Watchlist
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/v1/watchlist` | Get user watchlist |
| POST | `/api/v1/watchlist` | Add to watchlist |
| DELETE | `/api/v1/watchlist/:mediaId` | Remove from watchlist |

---

## 👨‍💻 Developer

**Alam**
- GitHub: [@HST159075](https://github.com/HST159075)

---

## 📝 License

This project is built for educational purposes as part of a full-stack web development assignment.
