# Teleprompter

Free, simple, and private. The script follows your voice: it scrolls as you say the words and waits when you pause.

## Deploy to Vercel
1. Put this folder in a Git repository and import it in Vercel (no build step, preset: Other).
2. Deploy. No environment variables are needed. Vercel gives you HTTPS, which the camera and microphone need.

## Notes
- Voice following uses the browser speech recognition (Chrome, Edge, Safari). In Chrome the audio may be processed by Google. Firefox is not supported, but you can tap any word to move the script.
- Recordings are saved in the browser on the device that recorded them.
- Mac notch mode is in Settings. Use it with the browser in fullscreen so the panel sits just under the camera.
