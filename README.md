<div align="center">

# Tsukiyomi (æœˆèª­)

### Celestial Manga & Webtoon Reader for Android
Fast, 120Hz-optimized reader with an app-wide Celestial Carbon & Violet-Cyan-Sakura aesthetic, spring-animated navigation icons, floating pill Reader HUD, episode thumbnail previews, automatic Keiyoushi extension updates, and end-to-end AES-256-GCM automatic Supabase account syncing.

[![Latest Release](https://img.shields.io/github/v/release/Boladale-01/Tsukiyomi?label=Latest%20Release&color=9D7BFF&style=for-the-badge)](https://github.com/Boladale-01/Tsukiyomi/releases/latest)
[![Download APK](https://img.shields.io/badge/Download%20APK-v0.24.0%20(arm64)-38BDF8?style=for-the-badge&logo=android&logoColor=white)](https://github.com/Boladale-01/Tsukiyomi/releases/download/v0.24.0/Tsukiyomi-arm64-v8a-v0.24.0.apk)

</div>

---

## Direct APK Download (`v0.24.0`)

- **Latest Release (arm64-v8a â€” S23 Ultra & Modern Android Phones):**  
  [**Download Tsukiyomi-arm64-v8a-v0.24.0.apk**](https://github.com/Boladale-01/Tsukiyomi/releases/download/v0.24.0/Tsukiyomi-arm64-v8a-v0.24.0.apk)
- **All Releases:**  
  [https://github.com/Boladale-01/Tsukiyomi/releases](https://github.com/Boladale-01/Tsukiyomi/releases)

---

## Highlights in `v0.24.0`

- **Real Per-Device Account Isolation & Pre-Configured Supabase Sync (`tsukiyomi_accounts`):**
  - Fresh devices start unauthenticated (`Device XXXX â€” Not signed in`) so you never see another device's account until you explicitly **Sign In** or **Create Account**.
  - Pre-connected out of the box to `public.tsukiyomi_accounts` with **PBKDF2-HMAC-SHA256** + **AES-256-GCM** encryption and unique username enforcement.
- **Auto-Added Keiyoushi Extension Repo & Automatic Extension Updater:**
  - Automatically registers the official **Keiyoushi** extension repository on first launch and automatically downloads/installs updates for installed extensions.
- **Accurate Continue Reading & Episode Thumbnail Previews:**
  - Automatically excludes caught-up series (`unreadCount == 0`) from **Continue Reading** and shows real reading progress percentages.
  - Displays rounded `62x46dp` episode thumbnail previews with `EP #` badges across chapter lists.
