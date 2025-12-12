# Real-Time Chat

A private, self-destructing real-time chat application built with Next.js and Upstash.

## Features

- 🔒 **Private Rooms** - Create secure chat rooms with unique IDs
- ⚡ **Real-Time Messaging** - Instant message delivery using Upstash Realtime
- ⏱️ **Self-Destructing** - Rooms automatically expire after 10 minutes
- 👤 **Anonymous Users** - Auto-generated anonymous usernames
- 🚫 **Room Limits** - Maximum 2 users per room
- 💣 **Manual Destruction** - Destroy rooms instantly at any time

## Tech Stack

- **Frontend**: Next.js 16, React 19, TypeScript
- **Backend**: Elysia (Bun runtime)
- **Database**: Upstash Redis
- **Real-Time**: Upstash Realtime
- **Styling**: Tailwind CSS
- **State Management**: TanStack Query

## Prerequisites

- Node.js 18+ or Bun
- Upstash Redis account
- Upstash Realtime account

## Environment Variables

Create a `.env.local` file in the root directory:

```env
UPSTASH_REDIS_REST_URL=your_redis_url
UPSTASH_REDIS_REST_TOKEN=your_redis_token
UPSTASH_REALTIME_URL=your_realtime_url
UPSTASH_REALTIME_TOKEN=your_realtime_token
```

## Getting Started

1. Install dependencies:

```bash
bun install
# or
npm install
```

2. Set up your environment variables (see above)

3. Run the development server:

```bash
bun dev
# or
npm run dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## Usage

1. **Create a Room**: Click "CREATE SECURE ROOM" to generate a new chat room
2. **Share the Link**: Copy the room URL and share it with one other person
3. **Chat**: Start sending messages in real-time
4. **Destroy**: Click "DESTROY NOW" to immediately delete the room and all messages

## Project Structure

```
src/
├── app/
│   ├── api/              # API routes (Elysia backend)
│   ├── room/[roomId]/    # Chat room page
│   └── page.tsx          # Home/lobby page
├── components/           # React components
├── hooks/                # Custom React hooks
└── lib/                  # Utilities and clients
```

## License

MIT
