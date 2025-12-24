# 🚀 Quick Start Guide
## SafeCapital Pro - Get Up and Running in 30 Minutes

---

## Prerequisites Checklist

✅ Node.js v20+ installed (you have v24 - perfect!)
✅ Git installed (you have v2.52 - perfect!)
✅ npm v11+ installed (you have v11.6 - perfect!)
⏳ Supabase account (we'll set up next)
⏳ Upstash account (we'll set up next)
⏳ Claude API key (optional for now)

---

## Step 1: Install Dependencies (5 minutes)

### Backend Setup
```bash
cd backend
npm install
```

This will install:
- Express (API framework)
- TypeScript (type safety)
- PostgreSQL client (database)
- Redis client (caching)
- Socket.io (real-time)
- Claude AI SDK
- JWT (authentication)
- And more...

### Frontend Setup
```bash
cd frontend
npm install
```

This will install:
- Next.js 14 (React framework)
- TypeScript
- Tailwind CSS (styling)
- Framer Motion (animations)
- Socket.io client
- React Query (data fetching)
- And more...

---

## Step 2: Set Up Cloud Databases (10 minutes)

### A) Supabase (PostgreSQL Database)

1. **Go to:** https://supabase.com
2. **Sign up** with GitHub or email (FREE)
3. **Create new project:**
   - Project name: `safecapital-pro`
   - Database password: (create strong password, SAVE IT!)
   - Region: `Southeast Asia (Singapore)` (closest to India)
   - Plan: Free tier (perfect for development)

4. **Get your credentials:**
   - Go to Project Settings → Database
   - Copy "Connection String" (URI format)
   - Go to Project Settings → API
   - Copy "Project URL" and "anon public" key

5. **Save credentials** in `backend/.env` file (we'll create it next)

### B) Upstash (Redis Cache)

1. **Go to:** https://upstash.com
2. **Sign up** with GitHub or email (FREE)
3. **Create new database:**
   - Name: `safecapital-redis`
   - Region: `ap-south-1 (Mumbai)` (India region!)
   - Type: `Regional`
   - Plan: Free tier

4. **Get your credentials:**
   - Click on your database
   - Copy "UPSTASH_REDIS_REST_URL"
   - Copy "UPSTASH_REDIS_REST_TOKEN"

5. **Save credentials** (we'll add to .env next)

---

## Step 3: Configure Environment Variables (5 minutes)

### Backend Environment

```bash
cd backend
cp .env.example .env
```

Now edit `backend/.env` and add your credentials:

```bash
# Database (from Supabase)
DATABASE_URL=postgresql://postgres:[YOUR-PASSWORD]@db.[PROJECT-REF].supabase.co:5432/postgres
SUPABASE_URL=https://[PROJECT-REF].supabase.co
SUPABASE_ANON_KEY=your-anon-key-from-supabase

# Redis (from Upstash)
UPSTASH_REDIS_URL=https://[YOUR-REDIS-URL].upstash.io
UPSTASH_REDIS_TOKEN=your-redis-token

# JWT (generate random string for now)
JWT_SECRET=change-this-to-random-string-later

# For now, leave others as default
```

### Frontend Environment

```bash
cd frontend
cp .env.example .env.local
```

The defaults are fine for now!

---

## Step 4: Create Database Tables (5 minutes)

We'll create a simple SQL script to set up our initial database:

```bash
cd database/migrations
```

I'll create the initial migration file for you in the next step.

---

## Step 5: Run the Application (5 minutes)

### Terminal 1: Start Backend
```bash
cd backend
npm run dev
```

You should see:
```
🚀 Server running on http://localhost:5000
✅ Database connected
✅ Redis connected
```

### Terminal 2: Start Frontend
```bash
cd frontend
npm run dev
```

You should see:
```
▲ Next.js 14.0.4
- Local: http://localhost:3000
✓ Ready in 2.5s
```

### Open Your Browser
Go to: **http://localhost:3000**

You should see the SafeCapital Pro homepage!

---

## Troubleshooting

### "Cannot connect to database"
- Check your `DATABASE_URL` in `.env`
- Make sure Supabase project is running
- Verify password is correct

### "Redis connection failed"
- Check `UPSTASH_REDIS_URL` in `.env`
- Verify token is correct
- Make sure Upstash database is active

### "npm install" fails
- Delete `node_modules` folder
- Delete `package-lock.json`
- Run `npm install` again

### Port already in use
- Backend: Change `PORT=5000` to `PORT=5001` in `.env`
- Frontend: Run with `npm run dev -- -p 3001`

---

## What's Next?

1. ✅ You have a working development environment
2. ✅ Databases are connected (Supabase + Upstash)
3. ✅ Both frontend and backend running

**Next steps:**
- Create database schema (Week 1, Day 3)
- Build authentication system
- Create first API endpoints
- Design dashboard UI

**Follow the MASTER_DEVELOPMENT_PLAN.md for Week 1 tasks!**

---

## Need Help?

- Check the main README.md
- Review MASTER_DEVELOPMENT_PLAN.md
- Ask me (Claude) for help anytime!

**You're doing great! Let's build something amazing! 🚀**
