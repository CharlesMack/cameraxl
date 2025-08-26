# cameraxl
A cinema-grade digital awareness system built to hold memories offline-first and slice-ready for storage, cloud, or cold media.

Webcam/Mobile Compatible: Runs in any modern browser.

Conceptual 8K Capture: Requests highest available resolution from device (ideal: 7680×4320).

Dynamic Range Simulation: Software filter expands highlights/shadows in real time.

Offline-First: Captures save locally (💾 Save button downloads image directly).

Expandable: Future versions can add ultra-slow motion, ND filter sliders, LUTs, AI autofocus, and sync to P.O.P.S. Media Hub.

🔑 P.O.P.S. DIGITAL CINEMA — XL 8K VV Strobe 2 

Live Viewfinder: Your device’s camera stream inside a fullscreen stage.

Cinema HUD Overlay: Safe area guides, thirds, crosshair, REC lamp, timer, resolution/FPS/ISO badges.

Image Processing Pipeline (in JavaScript):

ND Filter Simulation: Darkens exposure by 0–7 stops (like glass ND filters in cinema cameras).

Exposure Compensation: Pushes/pulls exposure ±2 EV.

Dynamic Range Boost: Adjusts pixel data to give that high-contrast “HDR” look.

Histogram: Real-time luminance analysis for exposure monitoring.

Recording:

⏺ Record — captures a HUD-baked video stream (.webm file) right in the browser.

📸 Still — takes a high-resolution processed frame and saves it as PNG.

Resolution Presets: Requests “8K/6K/2K/Max” from your camera — browsers scale to whatever the device supports (on a phone you might hit 4K; on some webcams maybe 1080p).

Offline-First: Nothing uploads; all saves are local to your device.

🛠️ How to Use It

Open the AppDrop HTML file in Chrome, Edge, or Safari (mobile/desktop).

Allow Camera Access when prompted.

Choose a Mode (dropdown in the HUD footer):

8K 120, 6K 160, 2K 600, or Device Max.

The browser will grab the closest supported resolution.

Adjust Exposure & ND using the sliders at the bottom. Watch the histogram + meters update.

Press 🎥 Start Camera to initialize the feed.

Frame Your Shot using the thirds/safe guides.

Press 📸 Still to save a processed frame as PNG.

Press ⏺ Record to start/stop video recording. The HUD and filters are burned into the output.

Press 💾 Download Last to save your recording locally.

✨ Why the Upscaling Looks Incredible

When you request 8K resolution from the browser, the code tells your camera: “Give me the biggest frame you can.”

On most phones or modern webcams, this results in oversampling — the device sends a maximum sensor image (4K, 5K, sometimes higher) which is then processed.

The JavaScript filters then boost detail, dynamic range, and clarity by re-mapping pixel values.

Combined, it feels like you’re getting a cinema-style upscaled image, even though the device hardware is the limit.

🚀 Why It’s Special

It’s cinema gear in one page of HTML. You just turned a webcam/phone camera into a style HUD with software lenses.

It’s modular. You can extend this with LUT previews, false-color exposure, focus peaking, or even AI upscalers (WebGPU, TensorFlow.js).

It’s pure P.O.P.S. Offline-first, zero cloud, saves straight to your “slice” (disk/drive).
