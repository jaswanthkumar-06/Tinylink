# Tinylink
A Modern , Full-stack URL shortener build with Next.js ,Typescript ,and Prisma
TinyLink

TinyLink is a URL shortening service built with modern web technologies. It allows users to shorten long URLs into concise, easy-to-share links, track clicks, and manage their links efficiently.

Features

Shorten long URLs with a custom or auto-generated alias.

Redirect users from short URLs to original URLs seamlessly.

View analytics: track number of clicks per link.

Simple and clean UI for easy link management.

Built with scalability in mind for handling multiple requests efficiently.


Tech Stack

Backend: Node.js, Express.js, Prisma ORM

Database: PostgreSQL / MySQL / SQLite (depending on your configuration)

Frontend: React.js (or Next.js if using SSR)

Authentication: JWT / Optional login for link management

Logging: Query logging enabled for development


Installation

1. Clone the repository:



git clone https://github.com/yourusername/tinylink.git
cd tinylink

2. Install dependencies:



npm install

3. Configure environment variables:
Create a .env file in the root directory with the following:



DATABASE_URL="your_database_connection_string"
PORT=5000
JWT_SECRET="your_secret_key"

4. Run database migrations (for Prisma):



npx prisma migrate dev --name init

5. Start the development server:



npm run dev

6. Open http://localhost:5000 in your browser.



API Endpoints

POST /api/shorten – Shorten a long URL.

GET /:shortId – Redirect to the original URL.

GET /api/links – Get all shortened links (requires auth).

GET /api/analytics/:shortId – Get click stats for a link.


Project Structure

tinylink/
├── prisma/          # Database schema and migrations
├── src/
│   ├── controllers/ # API request handlers
│   ├── routes/      # Express routes
│   ├── models/      # Database models
│   ├── utils/       # Helper functions
│   ├── middleware/  # Auth, error handling, etc.
├── client/          # Frontend code
├── .env
├── package.json
└── README.md

Contribution

Contributions are welcome! Feel free to open issues or submit pull requests.

License

This project is licensed under the MIT License.
