BlueLeafBooks - Production Deploy Notes (Render)

Backend (Render Web Service):
- Root Directory: backend
- Build Command: npm install
- Start Command: npm start
- Environment variables (set in Render, NOT in code):
  MONGODB_URI=...
  JWT_SECRET=...
  CLOUDINARY_CLOUD_NAME=...
  CLOUDINARY_API_KEY=...
  CLOUDINARY_API_SECRET=...
  PAYPAL_CLIENT_ID=...
  PAYPAL_CLIENT_SECRET=...
  PAYPAL_MODE=live   (or sandbox for testing)
  PLATFORM_FEE_PERCENTAGE=10
  ADMIN_EMAIL=blueleafbooks@hotmail.com
  ADMIN_PASSWORD=...

Frontend:
- This is a static HTML/CSS/JS frontend in /frontend
- Update API_BASE_URL in frontend/js/api.js to your Render backend URL:
  https://<your-backend>.onrender.com/api

Recommended:
- Use Render Static Site (or Netlify) for /frontend
- Or host /frontend on GitHub Pages (if CORS is configured on backend)

Security:
- Do NOT upload .env to GitHub.
- Keep keys only in Render Environment settings.
