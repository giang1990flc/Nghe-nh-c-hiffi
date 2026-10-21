AURA HI-FI ONLINE — PROTOTYPE V2

What this prototype does:
- Accepts direct HTTP(S) audio-stream URLs (where the provider permits playback).
- Uses HTMLAudioElement and Media Session metadata/actions where supported.
- Provides browser-side DSP/EQ presets: Balanced, Warm & Bass, Vocal Clarity.
- Includes PWA manifest and service worker for installation from Safari after HTTPS deployment.

Important limitations:
- This is not an AI model. Presets are DSP/EQ; genuine AI enhancement needs an actual ML/DSP model, compute budget, and audio-quality testing.
- A normal YouTube/Spotify page URL is not a direct audio stream URL. Do not bypass DRM or service restrictions. Use official embeds/APIs or licensed stream endpoints.
- iOS web apps cannot guarantee reliable background playback in all states/versions. Web Audio EQ may be suspended or behave differently in the background.
- For the user's stated priority (stable lock-screen playback + sound processing), recommended production architecture is a native iOS app using AVPlayer/AVAudioSession for playback, MPRemoteCommandCenter/Now Playing metadata for lock-screen controls, and AVAudioEngine or a validated DSP/ML pipeline for processing.
- AirPods 2 use Bluetooth AAC; lossless Bluetooth playback is not supported.
- The sample demo radio URL may change, be unavailable, or disallow playback in some regions. Replace with a licensed/verified stream URL if needed.

Deploy:
1. Upload index.html, manifest.json, sw.js to HTTPS static hosting.
2. Open URL in Safari on iPhone.
3. Share -> Add to Home Screen.
4. Paste a direct stream URL that permits browser playback.
