# Manual acceptance checklist

Run `npm start`, then open the printed localhost address.

- Home: all dock links and journey links open the correct pages.
- Create: empty title is blocked; unsupported file and >25 MB file are rejected; valid photo/audio/video/story saves.
- Memories: saved content remains after reload; category, search and favorites combine correctly.
- Detail: story text such as `<script>` is rendered as text; media controls work; candle lights once per detail opening.
- Backup: export, import into a different browser/origin, verify media and stories; malformed backup must not replace data.
- Delete: cancel leaves memory; confirm removes it (use a disposable test memory).
- More/Profile: preference and name changes remain after reload.
- Screen: verify at 390 px, 768 px and desktop; keyboard focus remains visible.
- WebGL: desktop drag and arrow keys change viewpoint/memory; resize remains correct.
- WebGL unavailable: screen-only gallery opens, arrows/swipe work, VR button explains the requirement.
- Headset: HTTPS + compatible browser; enter/exit immersive-vr, confirm stereo scale, select input and repeated entry.
- Privacy: no network requests for personal media; IndexedDB belongs only to the current origin.

Automated checks: `npm run check && npm test` (no installation required).
