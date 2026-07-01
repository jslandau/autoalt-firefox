# Firefox Add-ons (AMO) listing copy

This file contains the text to paste into the Mozilla Add-ons Developer Hub when creating the AutoAlt listing for Firefox.

---

## Name

```
AutoAlt for Firefox - Alt Text for bsky.app
```

## Summary

```
Generate alt text for bsky.app images using your own AI key (OpenAI, Anthropic, Google, or local Ollama). Free with Gemini.
```

## Detailed description

```
AutoAlt makes it one-click easy to write good alt text for the images you post on bsky.app — using AI vision models you bring your own key for.

When you attach an image to a Bluesky post, a small ✨ Auto button appears next to Bluesky's own +ALT chip. Click it. A second or two later, the alt-text field is filled. The default prompt prioritizes transcribing any text visible in the image (memes, screenshots, signs, diagrams) and falls back to a short description if there's no text. You can edit the alt text afterward, and you can fully customize the prompt in Settings.

✦ FOUR PROVIDERS, BRING YOUR OWN KEY ✦

• Google Gemini (gemini-3.1-flash-lite-preview by default) — recommended for most users; the free tier easily covers normal social-media posting volume
• OpenAI (gpt-5.4-nano by default)
• Anthropic Claude (claude-haiku-4-5 by default) — typically the strongest at OCR on dense or hard-to-read images
• Ollama (gemma4:e2b by default) — fully local, runs on your own machine, no API key needed; slower and lower quality than the cloud options, but private and free

You can change the model name for any provider in Settings.

✦ COSTS A FRACTION OF A CENT ✦

Generating alt text for one image costs roughly $0.0002–$0.003 on cloud providers — fractions of a cent. For most people, Google Gemini's free tier means it's effectively free.

✦ PRIVACY POSTURE ✦

• Your API keys are stored only on your device, in the browser's extension local storage. They never reach the extension's developer — we have no backend.
• Images are sent ONLY to the AI provider you chose, directly from your browser. No middleman, no analytics, no telemetry, no tracking, no ads.
• Open source. Every claim above can be verified by reading the code: https://github.com/jslandau/autoalt-firefox

✦ HOW TO SET UP ✦

1. Click the AutoAlt toolbar icon → Settings
2. Pick your provider (Google's free tier is the easiest start)
3. Paste your API key
4. Click Save
5. Open bsky.app, attach an image to a post, click the ✨ Auto button

For Ollama users, see the project README for the few extra steps needed to allow Firefox extensions to talk to your local Ollama server (the OLLAMA_ORIGINS environment variable must include moz-extension://*).

✦ ACCESSIBILITY ✦

Alt text isn't decoration — it's how blind and low-vision Bluesky users actually read images. Posting images without alt text excludes those users entirely. AutoAlt exists to lower the friction so there's no excuse to skip it. Generated alt text is a starting point you can edit, not a substitute for thinking about your audience.

✦ OPEN SOURCE ✦

MIT licensed. Source, issue tracker, and full privacy policy at https://github.com/jslandau/autoalt-firefox
```

## Category

AMO's category taxonomy differs from the Chrome Web Store's. Recommended:

```
Social Media
```

(Alternatively, **Accessibility** is a defensible fit — AMO does not have a "Productivity" category.)

## Language

```
English
```

## Add-on ID

The `browser_specific_settings.gecko.id` in the manifest is set to:

```
autoalt@jslandau.cc
```

This is required for AMO submission and signing. It does not affect temporary (`about:debugging`) installs, which use a random ID.

## Privacy policy URL

```
https://github.com/jslandau/autoalt-firefox/blob/main/PRIVACY.md
```

(Uses the same privacy policy as the Firefox extension's source repo.)

## Single purpose statement

```
Generates alt text descriptions for images posted to bsky.app, using a user-supplied AI provider API key.
```

## Permission justifications

AMO has its own permissions review. The justifications are the same as those listed above. The only Firefox-specific manifest key is `browser_specific_settings.gecko`, which is metadata (extension ID + minimum version) and not a permission — it grants no capabilities.

### Data usage disclosures (AMO)

Check honestly:
- Personally identifiable info: **No**
- Health info: **No**
- Financial / payment info: **No**
- Authentication info: **Yes** — disclose: "User provides their own AI provider API key, stored locally on their device, transmitted only to the provider they configured."
- Personal communications: **No**
- Location: **No**
- Web history: **No**
- User activity: **No**
- Website content: **No** (we do not extract page content; we only inject UI and read the image the user themselves uploaded)

Certifications (must check all three):
- ✅ I do not sell or transfer user data to third parties, outside of the approved use cases
- ✅ I do not use or transfer user data for purposes that are unrelated to my item's single purpose
- ✅ I do not use or transfer user data to determine creditworthiness or for lending purposes
