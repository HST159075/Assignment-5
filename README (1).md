# 🎬 CineTube — Movie & Series Rating Portal

A full-stack Movie and Series Rating Portal where users can explore, rate, and review movies and TV series. Admins manage the media library and moderate user-generated content.

![CineTube](https://tube-client.vercel.app/og-image.png)

---

## 🔗 Live Links

| Service | URL |
|---|---|
| 🌐 Frontend | [https://tube-client.vercel.app](https://tube-client.vercel.app/) |
| ⚙️ Backend API | [https://tube-server.onrender.com](https://tube-server.onrender.com) |
| 📁 Frontend Repo | [https://github.com/HST159075/Tube-client](https://github.com/HST159075/Tube-client) |
| 📁 Backend Repo | [https://github.com/HST159075/Tube-server](https://github.com/HST159075/Tube-server) |
| 🎥 Demo Video | https://drive.google.com/file/d/18VTk2ig0E7nOjSoFXfZHPL5hvbcOTWOl/view?usp=sharing|

---

## 🔐 Admin Credentials

```
Email:    alam18@gmail.com
Password: (123456789)
```

---

## ✨ Features

### 👤 User
- Register & login with email/password or Google OAuth
- Browse movies & series by genre, rating, year
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

---

## 🛠️ Tech Stack

### Frontend
- **Next.js 14**
- **TypeScript**
- **Better Auth** (Authentication)

### Backend
- **Node.js** + **Express.js**
- **Prisma ORM**
- **PostgreSQL**
- **Better Auth**
- **SSLCommerz**

### Deployment
- Frontend → **Vercel**
- Backend → **Render**
- Database → **PostgreSQL** 

---

## ⚙️ Local Setup

### Prerequisites
- Node.js v18+
- PostgreSQL database
- SSLCommerz sandbox account

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

**Tasin**
- GitHub: [@HST159075](https://github.com/HST159075)

---

