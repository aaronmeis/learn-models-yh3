# Tencent Hy3 on OpenRouter — POC

A self-contained static HTML page documenting the Tencent Hy3 model family (295B MoE) as exposed through OpenRouter in July 2026.

## What this is

- Single-file landing page (`index.html`) with:
  - Hero + key metrics
  - Side-by-side model route cards (free vs standard)
  - Detailed comparison table
  - Ready-to-copy OpenRouter configuration
  - Full attribute ledger (raw catalog data)
- Data captured from OpenRouter catalog + model pages for `tencent/hy3:free` and `tencent/hy3`.
- Includes reasoning support, tool calling, structured outputs, and 256K-class context.

## Quick start

1. Open `index.html` directly in a browser (no build step).
2. For local development with live reload you can use any simple static server:

   ```bash
   # Python
   python -m http.server 8000

   # Node (http-server or serve)
   npx serve .
   ```

3. To use the model:

   ```bash
   # .env (never commit the real one)
   OPENROUTER_API_KEY=sk-or-v1-...
   OPENAI_BASE_URL=https://openrouter.ai/api/v1
   MODEL=tencent/hy3:free
   ```

   The page itself is informational; point any OpenAI-compatible client at the OpenRouter base URL with the desired model slug.

## Files

- `index.html` — the complete POC page (HTML + CSS + JS)
- `.env.example` — safe template for environment variables
- `README.md` — this file

## Notes

- The free route (`tencent/hy3:free`) has $0 pricing for prompt and completion.
- The standard route (`tencent/hy3`) has paid capacity and slightly different provider limits.
- Both target the same underlying model weights (`tencent/Hy3` on Hugging Face).

## Data source

OpenRouter model catalog snapshot dated around July 6–7, 2026.

---

Built as a quick POC in `C:\projects\codex\yh3_poc`.
