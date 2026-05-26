# Lumina Learn

A full-stack learning portal for students and teachers — deployed as a single `index.html` on Vercel, powered by Supabase.

-----

## Files in this repo

|File        |Purpose                                               |
|------------|------------------------------------------------------|
|`index.html`|The entire frontend app (HTML + CSS + JS)             |
|`schema.sql`|Supabase database schema — run this once in SQL Editor|
|`README.md` |This file                                             |

-----

## Setup in 3 steps

### Step 1 — Supabase

1. Go to [supabase.com](https://supabase.com) → create a free project
1. Open **SQL Editor → New Query**
1. Paste the full contents of `schema.sql` → click **Run**
1. Go to **Project Settings → API**
1. Copy your **Project URL** and **anon public key**
1. Open `index.html`, find these two lines near the top and replace the values:

```js
const SUPABASE_URL  = 'YOUR_PROJECT_URL';
const SUPABASE_ANON = 'YOUR_ANON_KEY';
```

### Step 2 — Supabase Auth Settings

1. Go to **Authentication → Providers → Email**
1. Turn **Confirm email OFF** (so users can log in immediately)
1. Go to **Authentication → URL Configuration**
1. Set **Site URL** to your Vercel URL (e.g. `https://lumina-learn.vercel.app`)

### Step 3 — Deploy on Vercel

1. Push `index.html` to a GitHub repo
1. Go to [vercel.com](https://vercel.com) → New Project → import the repo
1. Leave all settings as default → click **Deploy**

-----

## How to register

- Open your Vercel URL
- Choose **Student** or **Teacher**
- Click **New here? Create Account**
- Enter your **real email** and a **6-digit numeric PIN** (e.g. `123456`)

-----

## Features

**Student**

- Browse and enroll in courses
- Track progress with continue / drop actions
- Access video lectures, reading materials, and Q&A per course
- View analytics — enrollment charts, faculty rankings
- Receive teacher announcements

**Teacher**

- Create and manage courses
- Schedule exams with status tracking
- Grade students via the Grade Book (saved to Supabase)
- View class roster with progress per student
- Send announcements to students
- View teaching schedule and student feedback charts