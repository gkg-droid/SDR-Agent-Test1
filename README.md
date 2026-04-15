# SDR Proxy

A minimal Express server that proxies requests to the Anthropic API, allowing the SDR browser app to work without CORS issues.

## Deploy to Render (free, ~5 min)

1. Push this folder to a GitHub repo
2. Go to render.com → New → Web Service
3. Connect your GitHub repo
4. Render auto-detects the config from render.yaml
5. Add environment variable: `ANTHROPIC_API_KEY` = your key
6. Click Deploy

Your proxy URL will be: `https://sdr-proxy.onrender.com` (or similar)

## Deploy to Railway (alternative)

1. Push to GitHub
2. Go to railway.app → New Project → Deploy from GitHub
3. Add environment variable: `ANTHROPIC_API_KEY` = your key
4. Deploy — Railway gives you a URL automatically

## Run locally

```bash
npm install
export ANTHROPIC_API_KEY=sk-ant-...
npm start
# Proxy runs at http://localhost:3001
```

## Using with the browser app

Once deployed, paste your proxy URL into the browser app's "Proxy URL" field in Step 1.
The app will route all Claude API calls through your proxy instead of directly to Anthropic.
