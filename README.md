# Course API (Express.js + Modular MVC)

**Student:** <Your Name>  |  **Roll No:** <Your Roll Number>

## Setup
1. `npm install`
2. Copy `.env.example` to `.env` and set `MONGO_URI` and `JWT_SECRET`
3. `npm start` (server runs on http://localhost:5000)

## Endpoints
| Module | Method | URL | Auth |
|---|---|---|---|
| Auth | POST | /api/auth/register | No |
| Auth | POST | /api/auth/login | No |
| Auth | GET | /api/auth/me | Yes |
| Category | GET | /api/categories, /api/categories/:id | No |
| Category | POST / PUT / DELETE | /api/categories, /api/categories/:id | Yes |
| Course | GET | /api/courses, /api/courses/:id | No |
| Course | POST / PUT / DELETE | /api/courses, /api/courses/:id | Yes |

Protected routes need header: `Authorization: Bearer <token>`

## Structure
```
server.js
src/
  app.js
  config/db.js
  models/        User, Category, Course
  controllers/   auth, category, course
  routes/        auth, category, course
  middleware/    authMiddleware, errorMiddleware, validateObjectId
```
