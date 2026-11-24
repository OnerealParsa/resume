# Resume REST API

A small Node.js REST API that stores and serves resume data — the backend of my personal resume website.

## API Endpoints

| Method | Route | Description |
|---|---|---|
| `GET` | `/api/resume` | Return the full resume |
| `GET` | `/api/resume/:section` | Return a single section (e.g. `personal_info`, `skills`) |
| `POST` | `/api/resume` | Add new keys to the stored resume |
| `PUT` | `/api/resume` | Replace the whole resume (requires `personal_info` and `skills`) |
| `PATCH` | `/api/resume` | Deep-merge a partial update |

## Stack

- Node.js + Express
- `helmet`, `cors`, `morgan` (security, CORS, request logging)

## Project Structure

| File | Purpose |
|---|---|
| `server.js` | Express app and REST routes |
| `resume-data.json` | Resume data store |
| `index.html` / `style.css` / `script.js` | Minimal client for testing the API |

## Run

```bash
npm install
node server.js
```

The server listens on `PORT` (default `3001`).

## Related

Frontend: [resume-front](https://github.com/OnerealParsa/resume-front) — the deployed resume site.
