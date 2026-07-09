# Tencent Hy3 on OpenRouter

> **Tencent Hy3 on OpenRouter - free vs standard routes, specs, and config**

<p align="center">
  <a href="https://aaronmeis.github.io/learn-models-yh3/">
    <strong>View live demo</strong>
  </a>
</p>

> **Repo description (copy for GitHub):**
> `Tencent Hy3 on OpenRouter - free vs standard routes, specs, and config`

A self-contained static HTML page documenting the Tencent Hy3 model family (295B MoE) as exposed through OpenRouter.

## What this is

- Single-file landing page (`index.html`) with:
  - Hero + key metrics
  - Side-by-side model route cards (free vs standard)
  - Detailed comparison table
  - Ready-to-copy OpenRouter configuration
  - Full attribute ledger (raw catalog data)
- Data captured from the OpenRouter catalog for `tencent/hy3:free` and `tencent/hy3`.
- Includes reasoning support, tool calling, structured outputs, and 256K-class context.

## Quick start

1. Open `index.html` directly in a browser. There is no build step.
2. For local development with live reload, use any simple static server:

   ```bash
   # Python
   python -m http.server 8000

   # Node
   npx serve .
   ```

3. To use the model:

   ```bash
   # .env - never commit the real one
   OPENROUTER_API_KEY=sk-or-v1-...
   OPENAI_BASE_URL=https://openrouter.ai/api/v1
   MODEL=tencent/hy3:free
   ```

   The page itself is informational; point any OpenAI-compatible client at the OpenRouter base URL with the desired model slug.

## Files

- `index.html` - the complete POC page (HTML + CSS + JS)
- `.env.example` - safe template for environment variables
- `README.md` - this file

## Notes

- The free route (`tencent/hy3:free`) has $0 pricing for prompt and completion.
- The standard route (`tencent/hy3`) has paid capacity and slightly different provider limits.
- Both target the same underlying model weights (`tencent/Hy3` on Hugging Face).

## Data Source

OpenRouter model catalog snapshot dated July 8, 2026.

## GitHub Pages

This repo is designed to be hosted with GitHub Pages. Once Pages is enabled with `main` / root, the `index.html` becomes the live landing page at:

```text
https://aaronmeis.github.io/learn-models-yh3/
```

After enabling Pages, go to Settings -> General and set the same URL as the Website in the About section on the right sidebar.

---

**Tip:** To make the live site more discoverable, add the GitHub Pages URL as the "Website" link in the repo's About section.
