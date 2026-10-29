# Launchpad — Next.js + MongoDB

A responsive website starter using Next.js App Router, React, route handlers, and the official MongoDB Node.js driver.

## Included
- Responsive landing page
- Next.js App Router
- API route handlers for reading and saving messages
- MongoDB persistence
- Input validation and basic error handling

## Requirements
- Node.js LTS: https://nodejs.org/
- A MongoDB database: local Community Server or MongoDB Atlas: https://www.mongodb.com/atlas

## Setup

1. Extract the ZIP and open the folder in VS Code.
2. Install dependencies:

   ```bash
   npm install
   ```

3. Copy `.env.example` to `.env.local`.
4. Configure `MONGODB_URI` in `.env.local`.
   - Local MongoDB example: `mongodb://127.0.0.1:27017`
   - For Atlas, use the connection string from your cluster and replace the placeholders.
5. Optionally set `MONGODB_DB=launchpad`.
6. Start the development server:

   ```bash
   npm run dev
   ```

7. Visit `http://localhost:3000`.

For a production build, run `npm run build` then `npm start`.

## API
- `GET /api/messages` — returns the latest 50 messages
- `POST /api/messages` — accepts JSON such as `{"name":"Alex","message":"Hello!"}`

## Important security notes
- Never commit `.env.local` or expose MongoDB credentials in client-side code.
- Configure Atlas network access and database users carefully.
- This starter has no user accounts or authentication and is not a production-ready guestbook. Add rate limiting, moderation, authentication, and deployment configuration before exposing it publicly.
