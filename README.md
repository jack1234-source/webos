<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# AetherOS

The API is FastAPI. For local production mode, FastAPI also serves the built React frontend. Vite uses Node.js for frontend development and builds; Vercel serves the built frontend as static assets and routes API requests to FastAPI.

## Run Locally

**Prerequisites:** Python 3.10+, Node.js, and npm


1. Install Python dependencies: `python -m pip install -r requirements.txt`
2. Install frontend dependencies and build the UI: `npm install && npm run build`
3. Start the application, with FastAPI serving both the API and built UI: `uvicorn api.index:app --host 0.0.0.0 --port 8000`
4. Open `http://localhost:8000`.

For frontend development with hot reload, run `uvicorn api.index:app --reload --port 8000` and `npm run dev` in separate terminals, then open `http://localhost:3000`. Vite forwards `/api` requests to FastAPI.
