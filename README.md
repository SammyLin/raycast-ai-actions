# AI Actions - Raycast Extension

[![Lint](https://github.com/SammyLin/raycast-ai-actions/actions/workflows/lint.yml/badge.svg)](https://github.com/SammyLin/raycast-ai-actions/actions/workflows/lint.yml)
[![CI](https://github.com/SammyLin/raycast-ai-actions/actions/workflows/ci.yml/badge.svg)](https://github.com/SammyLin/raycast-ai-actions/actions/workflows/ci.yml)
[![Build](https://github.com/SammyLin/raycast-ai-actions/actions/workflows/build.yml/badge.svg)](https://github.com/SammyLin/raycast-ai-actions/actions/workflows/build.yml)

Quick AI text processing tool - Process selected text with custom AI prompts.

Supports multiple AI endpoints:
- ✅ Google Gemini (Official)
- ✅ [Gemini Balance](https://github.com/snailyp/gemini-balance)
- ✅ OpenRouter
- ✅ Any Gemini API compatible endpoint

## Features

- 🎯 **Process Selected Text** - Select text and run directly, no copy-paste needed
- 🔧 **Fully Customizable** - Create custom prompt templates for your needs
- 🌐 **Multiple Endpoint Support** - Official Gemini, gemini-balance, OpenRouter, etc.
- ⚡ **Fast & Convenient** - Results displayed instantly, one-click copy or paste

## Installation

```bash
cd ai-quick-actions
npm install
npm run dev
```

## Configuration

### Global Settings (Shared by all commands)

Configure in Raycast Extension Preferences:

1. **API Format** - Select API format (Gemini API or OpenAI API)
2. **API Key** - Your API Key
3. **Model** - Model name
4. **Custom Endpoint** (Optional) - Custom API endpoint URL

### Using Official Gemini API

```
API Format: Gemini API (Official / gemini-balance)
API Key: your_gemini_api_key
Model: gemini-2.5-flash
Custom Endpoint: (leave empty for official API)
```

### Using Gemini Balance

If you're using [gemini-balance](https://github.com/snailyp/gemini-balance):

```
API Format: Gemini API (Official / gemini-balance)
API Key: your_api_key
Model: gemini-2.5-flash
Custom Endpoint: http://127.0.0.1:8000
```

### Using OpenRouter

```
API Format: OpenAI API (OpenRouter)
API Key: sk-or-v1-xxxxx
Model: google/gemini-2.0-flash-exp
Custom Endpoint: https://openrouter.ai/api/v1
```

## Usage

1. **Select text** - Select text in any application
2. **Open Raycast** - Press hotkey (usually `⌥ Space`)
3. **Run command** - Search and run "Run AI Prompt"
4. **Choose prompt** - Select from your custom prompts
5. **View result** - Result displayed in window, can copy or paste

## Prompt Examples

### Translate to Chinese

```
Title: Translate to Chinese
Prompt: Translate to Traditional Chinese. Output ONLY the translated text:

{selection}
```

### Summarize

```
Title: Summarize
Prompt: Summarize the following content in Traditional Chinese, maximum 500 words:

{selection}
```

### Improve Writing

```
Title: Improve Writing
Prompt: Improve the following text to make it clearer and more fluent. Output only the improved text:

{selection}
```

### Explain Code

```
Title: Explain Code
Prompt: Explain the following code in Traditional Chinese:

{selection}
```

### Translate to English

```
Title: Translate to English
Prompt: Translate to English. Output ONLY the translated text:

{selection}
```

### Fix Grammar

```
Title: Fix Grammar
Prompt: Fix grammar and spelling errors in the following text:

{selection}
```

## Advanced Tips

### Using Variables

Use `{selection}` in your prompt as placeholder for selected text:

```
Translate the following to Japanese:

{selection}

Please maintain the original tone and style.
```

## Project Structure

```
ai-quick-actions/
├── src/
│   ├── manage-prompts.tsx  # Manage prompts interface
│   └── run-prompt.tsx      # Run prompts interface
├── assets/
│   └── extension-icon.png
└── package.json
```

## Development

```bash
# Development mode (hot reload)
npm run dev

# Build
npm run build

# Publish to Raycast Store
npm run publish
```

## Related Links

- [Raycast Extensions Documentation](https://developers.raycast.com)
- [Gemini Balance](https://github.com/snailyp/gemini-balance)
- [Google AI Studio](https://makersuite.google.com/app/apikey) - Get API Key

## License

MIT
