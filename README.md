# 🍳 NalBheema — Complete Full-Stack Recipe App

## What is inside?
- **120 recipes exactly:** 100 Indian + 8 Italian + 5 Japanese + 7 American
- Ingredient-based recipe discovery and match scores
- Premium responsive dark UI
- Cuisine filters + Surprise Me
- Favorites using localStorage
- Detailed ingredients and cooking steps
- **Cook With Me** mode
- Animated CSS cooking visuals
- Per-step cooking timers
- Express REST API
- MongoDB/Mongoose-ready backend
- Bundled dataset fallback: MongoDB is not required to demo the app

## Start
Install Node.js 18+.

```bash
npm install
npm run dev
```

Frontend: http://localhost:5173  
API: http://localhost:5000/api/health

## Production
```bash
npm run build
npm start
```

## MongoDB
Copy `.env.example` to `.env` and set `MONGODB_URI`. The current version deliberately works without MongoDB; the bundled JSON dataset makes the demo immediately runnable.

## Main API endpoints
- `GET /api/health`
- `GET /api/recipes`
- `GET /api/recipes/:id`
- `POST /api/match` with `{ "ingredients": ["rice","tomato"] }`

## Architecture
React + Vite frontend → Express API → bundled JSON / optional MongoDB.

The food photos use remote Unsplash image URLs. Cooking animations are lightweight CSS animations so the ZIP stays fast; the recipe model is ready to swap them for Lottie/WebM/MP4 assets later.
