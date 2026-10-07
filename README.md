# Teleprompter Studio

Free forever. A browser teleprompter, recorder and AI director in a single file, with no paid services and no server code.

## Deploy
Push `index.html` and `vercel.json` to a Git repository and import it in Vercel (preset: Other, no build step). Any static host with HTTPS works.

## Free, open source AI that runs in the browser
- Natural voice over: Kokoro 82M (Apache 2.0) through kokoro-js.
- Speech recognition for dictation and the live pace check: OpenAI Whisper (MIT) through Transformers.js. Choose Fast (tiny), Balanced (base) or Most accurate (small).
- Script analysis and rewrites: Qwen2.5 1.5B through WebLLM.

Each model downloads once and is then cached by the browser. Audio and scripts never leave the device. A GPU (WebGPU in Chrome or Edge) makes them faster; without one they run on the processor.

## Where things live
Scripts, settings and recordings are saved in the browser on the device. Nothing is uploaded.

## Notes
- vercel.json sets cross-origin isolation headers so the models can use several processor threads.
- If a model fails to load, check the browser console for a blocked host and add it to connect-src in vercel.json.
