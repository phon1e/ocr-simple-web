# ocr-api-simple web app (for thai/en lang.)

# using Typhoon OCR

A single-file browser tool to extract raw text from images and PDFs using **Typhoon OCR**.


No install. No server. Just open `index.html`.

---

## Setup

1. Get a **Typhoon API key** → [opentyphoon.ai](https://opentyphoon.ai)
2. Open `index.html` in your browser
3. Paste your API key into the input field

> Keys are never stored — session memory only.

---

## Usage

1. Enter your API key
2. Upload an image (PNG, JPG, WEBP) or PDF
3. Click **Extract Text**
4. Copy the result

---

## OCR Parameters

Tweak these inside `extractTextFromImage()` in `index.html`:

| Parameter | Default | Description |
|---|---|---|
| `model` | `typhoon-ocr` | OCR model |
| `task_type` | `default` | Extraction mode |
| `max_tokens` | `16384` | Max output tokens |
| `temperature` | `0.1` | Lower = more deterministic |
| `top_p` | `0.6` | Nucleus sampling threshold |
| `repetition_penalty` | `1.0` | Penalises repeated tokens |
| `pages` | `null` | Specific pages to process (PDF), `null` = all |

---

## Rate Limits (typhoon-ocr)

| Limit | Value |
|---|---|
| Requests/second | 2 |
| Requests/minute | 20 |

Need higher limits? Email `contact@opentyphoon.ai`.
