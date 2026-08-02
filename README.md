# Short URL Service

A simple URL shortener API built with Node.js, Express, and MongoDB. Create short links, redirect visitors, and track click analytics.

## Features

- Generate a short URL for any long URL
- Redirect short URL to the original URL
- Track total clicks and visit timestamps

## Tech Stack

Node.js · Express · MongoDB (Mongoose) · nanoid · dotenv

## Project Structure

```
.
├── connect.js              # MongoDB connection
├── index.js                # App entry point
├── models/
│   └── url.js               # URL schema
├── controllers/
│   └── url.js                # Route handler logic
├── routes/
│   └── url.js                 # /url router
├── .env                          # Environment variables
└── package.json
```

## Setup

```bash
git clone https://github.com/yasirrajput4/short-url-service
cd short-url-service
npm install
```

Create a `.env` file:

```
MONGODB_URL=your_mongodb_connection_string
PORT=your_port_number
```

Run the server:

```bash
npm start
```

## API Endpoints

**Create a short URL**

```
POST /url
Body: { "url": "https://example.com" }
Response: { "id": "aZ3xK9pQ" }
```

**Redirect to original URL**

```
GET /:shortId
```

**Get analytics**

```
GET /url/analytics/:shortId
Response: { "totalClicks": 3, "analytics": [...] }
```

## License

ISC
