# JARVIS AI — Android starter

A native Android starter app with a burgundy/dark chat interface, Hindi speech input, Hindi text-to-speech replies, configurable OpenAI-compatible chat endpoint, and a small set of on-device shortcuts.

## On-device commands included
- `WhatsApp kholo` / `open WhatsApp`
- `YouTube kholo` / `open YouTube`
- `Camera kholo`
- `Settings kholo`
- `Wi-Fi settings` / `Bluetooth settings`
- `Dialer kholo` (opens dialer; does not place a call)
- `Alarm kholo`
- `Search <words>` / `Google par <words>`
- `Chrome kholo`

These commands launch Android screens/apps. They do not bypass Android permissions or silently send messages, make calls, or control protected settings.

## AI connection required
For general AI conversation, open the app's connection settings and enter an HTTPS OpenAI-compatible `/v1/chat/completions` endpoint and its API key. The starter defaults to model `gpt-4o-mini`. For a real deployment, use a private backend so a provider API key is not embedded in a public APK. No API key or backend is bundled.

## Build APK from a phone using GitHub Actions
1. Create a GitHub repository and upload the contents of this project folder to the repository root (not the parent folder).
2. Open the repository's **Actions** tab.
3. Select **Build Android APK** and tap **Run workflow**.
4. When the run completes, open it and download the `jarvis-ai-debug-apk` artifact. Extract it and install `app-debug.apk` on Android. You may need to allow installation from that browser/files app.

The workflow builds a debug APK. It is suitable for personal testing, not Play Store release signing.
