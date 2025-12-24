# 🚀 Upstash Redis Setup - Quick Guide

## What is Redis & Why Do We Need It?

**Redis** = Fast in-memory cache for:
- Session management (user login tokens)
- Real-time price data caching
- Rate limiting API calls
- WebSocket connection management

**Upstash** = Free Redis hosting (perfect for our needs!)

---

## Steps to Set Up Upstash (5 minutes)

### 1. Go to Upstash Console
Open: **https://console.upstash.com**

### 2. Sign Up (Free)
- Click "Sign Up"
- Use your **GitHub account** (easiest)
- Or use email

### 3. Create Database
Once logged in:
- Click **"Create Database"** button
- Fill in details:
  - **Name:** `safecapital-redis`
  - **Type:** `Regional` (select this!)
  - **Region:** `ap-south-1 (Mumbai)` ← Choose this (India!)
  - **Primary:** Yes (default)

- Click **"Create"**

### 4. Get Your Credentials

After database is created:
- Click on your database name: `safecapital-redis`
- You'll see the dashboard

**Scroll down to find these sections:**

#### A) REST API Section
You'll see:
```
UPSTASH_REDIS_REST_URL
https://engaged-seahorse-12345.upstash.io

UPSTASH_REDIS_REST_TOKEN
AaaaAAaaAaBbBbCcCcDdDdEeEeFfFf1234567890=
```

**Copy both of these!**

#### B) Connection String (Alternative)
You'll also see:
```
redis://default:[PASSWORD]@engaged-seahorse-12345.upstash.io:6379
```

**Copy this too!**

---

## 5. Update Your .env File

Open: `backend/.env`

Replace these lines:
```bash
# OLD (placeholder):
UPSTASH_REDIS_URL=https://your-redis.upstash.io
UPSTASH_REDIS_TOKEN=your-redis-token

# NEW (your actual credentials):
UPSTASH_REDIS_URL=https://engaged-seahorse-12345.upstash.io
UPSTASH_REDIS_TOKEN=AaaaAAaaAaBbBbCcCcDdDdEeEeFfFf1234567890=
```

**Also update:**
```bash
# OLD:
REDIS_URL=redis://default:password@host:6379

# NEW (paste your connection string):
REDIS_URL=redis://default:[YOUR_PASSWORD]@engaged-seahorse-12345.upstash.io:6379
```

---

## 6. Test Your Setup

**Tell me when done, and I'll help you test the connection!**

You can also test directly in Upstash console:
- Go to "CLI" tab
- Type: `PING`
- Should return: `PONG`

---

## Free Tier Limits (More Than Enough!)

Upstash Free Tier gives you:
- ✅ **10,000 commands per day**
- ✅ **256 MB data storage**
- ✅ **Unlimited databases**
- ✅ **TLS/SSL encryption**
- ✅ **Global replication** (optional)

**For our MVP:** This is perfect! We'll use ~1,000 commands/day max.

---

## What Happens Next?

Once you add your Upstash credentials to `.env`:

1. ✅ Backend can connect to Redis
2. ✅ We can cache user sessions
3. ✅ We can store real-time price data
4. ✅ Rate limiting will work
5. ✅ WebSocket scalability improved

---

## Need Help?

**Having issues?**
- Make sure you selected "Regional" (not "Global")
- Choose Mumbai region (closest to India)
- Copy the FULL token (it's long!)
- Don't include quotes when pasting

**Tell me when you're done!**

Then we'll:
1. Install dependencies
2. Test database connections
3. Start building! 🚀
