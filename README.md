1. Smart Bookmark App
A full-stack bookmark management application built with Next.js (App Router) and Supabase.
Users can log in using Google OAuth, create private bookmarks, delete them, and see updates in real-time.

2. Live Demo
https://smart-bookmark-app-hq5p.vercel.app

3. Tech Stack
Frontend: Next.js (App Router)
Authentication: Supabase Auth (Google OAuth)
Database: Supabase PostgreSQL
Realtime: Supabase Realtime Subscriptions
Styling: Tailwind CSS / CSS
Deployment: Vercel

4. Features
Google OAuth login
Private bookmarks per user (Row Level Security)
Add bookmark
Delete bookmark
Real-time updates across tabs
Deployed on Vercel

5. Security
Row Level Security (RLS) enabled
Policies ensure:
Users can only view their own bookmarks
Users can only insert their own bookmarks
Users can only delete their own bookmarks
Policy condition used:
auth.uid() = user_id

6. Project Structure
app/
  page.tsx
  dashboard/page.tsx
lib/
  supabase.ts

7. Environment Variables
Create .env.local:
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_publishable_key

8. Challenges Faced
OAuth redirect mismatch between localhost and production
Module path alias issues during Vercel deployment
Case sensitivity differences between Windows and Linux
Supabase Site URL misconfiguration
All were resolved by:
Removing hardcoded redirectTo
Using relative imports
Updating Supabase URL configuration

9. How To Run Locally
npm install
npm run dev
