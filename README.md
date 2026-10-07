# Teleprompter Studio

Free forever. A browser teleprompter, recorder and AI director with no paid services and no server code.

## Deploy to Vercel
1. Put this folder in a Git repository and import it in Vercel (no build step, preset: Other). No environment variables are needed.
2. Deploy. Vercel serves it over HTTPS, which the camera and microphone need. You can also use any free static host.

## Where things live
- Scripts, settings and the pronunciation dictionary are saved in the browser on the device.
- Every recording is saved in the browser database on the device that recorded it, and shows in the Recording library. Chrome and Edge on a computer can also write each take to a folder you choose.
- Nothing is uploaded. The app can be installed and used offline, apart from the AI download.

## Free AI
AI runs inside the browser with the open source WebLLM library and the open source Qwen2.5 1.5B model. It needs WebGPU (Chrome or Edge on a computer, recent Android Chrome). The first use downloads about 1 GB once and then it is cached. To use a bigger model, change the model name in index.html (search for Qwen2.5). Without WebGPU the local rules still plan pauses, breaths, emphasis and cues.

## Notes
- Overlay on video draws the script over the live preview and is never recorded. Float over other windows needs Chrome or Edge 116 or newer.
- Voice analysis and dictation use the browser speech recognition, which is free but may send audio to the browser vendor. They are off by default.
- The Content Security Policy in vercel.json allows the model download hosts. If the AI fails to load, check the browser console for a blocked host and add it.
