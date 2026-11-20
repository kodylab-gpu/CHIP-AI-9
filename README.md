# Chip AI — Vercel repaired

This project uses one FastAPI entrypoint (`chat:app`) to serve the interface and API.

## Deploy
1. Remove old files from your GitHub repository, then upload the **contents** of this folder (not the enclosing folder).
2. Keep `chat.py`, `index.html`, `pyproject.toml`, `requirements.txt`, and `vercel.json` at the repository root.
3. Deploy on Vercel (Framework: FastAPI / auto-detected).
4. Visit `/` to view the UI and `/api/health` to check backend status.
5. Configure `AI_API_KEY`, `AI_MODEL`, and optionally `AI_BASE_URL` in Vercel environment variables, then redeploy.

## Notes
The HTML is embedded in `chat.py` to ensure it is included in the serverless function. If you edit `index.html`, you must also update the embedded `INDEX_HTML` in `chat.py` (or regenerate the bundle). Never commit API keys.
