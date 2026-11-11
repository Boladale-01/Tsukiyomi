<div align="center">

# Tsukiyomi (月読)

### Celestial Manga & Webtoon Reader for Android
Fast, 120Hz-optimized reader with an app-wide Celestial Carbon & Violet-Cyan-Sakura aesthetic, spring-animated navigation icons, floating pill Reader HUD, episode thumbnail previews, automatic Keiyoushi extension updates, and end-to-end AES-256-GCM automatic Supabase account syncing.

[![Latest Release](https://img.shields.io/github/v/release/Boladale-01/Tsukiyomi?label=Latest%20Release&color=9D7BFF&style=for-the-badge)](https://github.com/Boladale-01/Tsukiyomi/releases/latest)
[![Download APK](https://img.shields.io/badge/Download%20APK-v0.26.0%20(arm64)-38BDF8?style=for-the-badge&logo=android&logoColor=white)](https://github.com/Boladale-01/Tsukiyomi/releases/download/v0.26.0/Tsukiyomi-arm64-v8a-v0.26.0.apk)

</div>

---

## Direct APK Download (`v0.26.0`)

- **Latest Release (arm64-v8a — S23 Ultra & Modern Android Phones):**  
  [**Download Tsukiyomi-arm64-v8a-v0.26.0.apk**](https://github.com/Boladale-01/Tsukiyomi/releases/download/v0.26.0/Tsukiyomi-arm64-v8a-v0.26.0.apk)
- **All Releases:**  
  [https://github.com/Boladale-01/Tsukiyomi/releases](https://github.com/Boladale-01/Tsukiyomi/releases)

---

## Highlights in `v0.26.0`

- **R8-Minified Production-Speed Release (`devRelease`):**
  - Ships non-debuggable R8-shrunk APKs signed for in-place updates so compose UI, image decoding, and navigation run without debug-build overhead.
- **WEBTOON-Style Lightweight Delta Sync:**
  - Eliminates full `.tachibk` exports and multi-MB vault re-uploads during reading and chapter marking; syncs lightweight AES-256-GCM gzipped delta feeds (~1–3 KB) over WebSocket broadcast + `handle`/`updated_at` while reserving full vault uploads for structural library/category/extension changes.
  - Stops unnecessary 5s REST polling whenever Realtime WebSocket is live (switching to reconnect + foreground catch-up + 45s offline fallback) and flushes pending progress on app background.
- **Reliable Unseen Recommendations:**
  - Home recommendations reactively wait for extensions to initialize, prioritize your active/language-matched sources, and strictly exclude library series, reading history, finished/non-library read titles, and cross-source duplicates, with clean loading and Retry controls.
- **Faster Chapter Thumbnails & Continue Reading:**
  - Downsamples and crops cached JPEG chapter thumbnails (`ChapterThumbnailFetcher` v2) and removes stacked dual-image/alpha-layer overdraw on chapter rows (`MangaChapterListItem`), plus parallelizes Continue Reading loading.

---

## Previous Highlights (`v0.25.0`)

- **Instant Always-On Sync (Phone <-> Tablet via Supabase Realtime):**
  - Live **Supabase Realtime Broadcast WebSockets** stream reading page updates and chapter completions between your signed-in devices within milliseconds while persisting coalesced AES-256-GCM snapshots to `public.tsukiyomi_accounts`.
  - Optional always-running **`dataSync` foreground service** keeps live sync connected in the background with an **Always-On: ON/OFF** toggle directly in the profile card.
- **Backup File Corruption Fix:**
  - Atomic staged `.tachibk` creation with pre-write validation, safe truncation (`wt`), multi-layer GZIP/ZLIB/ZIP decoding support, defaulted model fields, and metadata field recovery prevent false `"Backup file is corrupted"` errors on manual, automatic, and cloud restores.
- **Real Chapter Thumbnails & Clean Solid Material UI:**
  - Displays real first-page chapter artwork via `ChapterThumbnailFetcher` on solid Material surfaces and badges (`EP #`) with liquid/frosted glass effects removed.
- **Silent Automatic Extension Downloader:**
  - Signing in on a new device automatically downloads missing/synced extensions in the background with a clean `"These extensions will be downloaded"` status dialog instead of manual install buttons.
- **Faster Navigation & Snappy Scrolling:**
  - Reduced transition latency and zero-crossfade chapter thumbnail rendering for smoother performance across both flagship and mid-range Android devices.

---

## Previous Highlights (`v0.24.0`)

- **Real Per-Device Account Isolation & Pre-Configured Supabase Sync (`tsukiyomi_accounts`):**
  - Fresh devices start unauthenticated (`Device XXXX — Not signed in`) so you never see another device's account until you explicitly **Sign In** or **Create Account**.
  - Pre-connected out of the box to `public.tsukiyomi_accounts` with **PBKDF2-HMAC-SHA256** + **AES-256-GCM** encryption and unique username enforcement.
- **Auto-Added Keiyoushi Extension Repo & Automatic Extension Updater:**
  - Automatically registers the official **Keiyoushi** extension repository on first launch and automatically downloads/installs updates for installed extensions.
- **Accurate Continue Reading:**
  - Automatically excludes caught-up series (`unreadCount == 0`) from **Continue Reading** and shows real reading progress percentages.
