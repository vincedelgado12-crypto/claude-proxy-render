# Claude API Proxy for Render

Simple Express.js proxy server to handle Claude API requests and bypass CORS restrictions.

## Setup

1. Clone this repository
2. Deploy to Render.com (free tier)
3. Use the deployed URL in your frontend application

## API Endpoint

POST `/claude`

**Request Body:**
```json
{
  "prompt": "Your question here"
}
```

**Response:**
Returns Claude API response directly.

## Deploy to Render

1. Connect this GitHub repository to Render
2. Create a new Web Service
3. Use these settings:
   - Build Command: `npm install`
   - Start Command: `npm start`
   - Environment: Node.js

## Usage in Frontend

```javascript
const response = await fetch('YOUR_RENDER_URL/claude', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    prompt: 'Your question'
  })
});

const data = await response.json();
```