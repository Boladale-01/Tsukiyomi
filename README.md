<div align="center">

# Tsukiyomi (æœˆèª­)

### Celestial Manga & Webtoon Reader for Android
Fast, 120Hz-optimized reader with an app-wide Celestial Carbon & Violet-Cyan-Sakura aesthetic, spring-animated navigation icons, floating pill Reader HUD, and end-to-end AES-256-GCM automatic Supabase account syncing.

[![Latest Release](https://img.shields.io/github/v/release/Boladale-01/Tsukiyomi?label=Latest%20Release&color=9D7BFF&style=for-the-badge)](https://github.com/Boladale-01/Tsukiyomi/releases/latest)
[![Download APK](https://img.shields.io/badge/Download%20APK-v0.23.0%20(arm64)-38BDF8?style=for-the-badge&logo=android&logoColor=white)](https://github.com/Boladale-01/Tsukiyomi/releases/download/v0.23.0/Tsukiyomi-arm64-v8a-v0.23.0.apk)

</div>

---

## Direct APK Download (`v0.23.0`)

- **Latest Release (arm64-v8a â€” S23 Ultra & Modern Android Phones):**  
  [**Download Tsukiyomi-arm64-v8a-v0.23.0.apk**](https://github.com/Boladale-01/Tsukiyomi/releases/download/v0.23.0/Tsukiyomi-arm64-v8a-v0.23.0.apk)
- **All Releases:**  
  [https://github.com/Boladale-01/Tsukiyomi/releases](https://github.com/Boladale-01/Tsukiyomi/releases)

---

## Highlights in `v0.23.0`

- **Refined Tsukiyomi Lunar Eclipse Emblem:** Nested dual-crescent Lunar Eclipse (`#9D7BFF` + `#F8FAFC`) with a 4-point celestial star (`#38BDF8` + `#F472B6`) on a deep `#090B10` circular backdrop.
- **Automatic Supabase Cloud Vault Sync (`tsukiyomi_accounts`):**
  - Automatically backs up and restores your library and categories in the background using **PBKDF2-HMAC-SHA256** + **AES-256-GCM** encryption.
  - Strictly isolated to `public.tsukiyomi_accounts` / `public.tsukiyomi_profiles` â€” never touches any other table in your Supabase project.
  - Enforces unique usernames across accounts.
- **120Hz S23 Ultra & Low-End Device Speed Overhaul:**
  - Native 120Hz high refresh rate display mode lock.
  - `@Immutable` Compose state models across Home & Recommendation engines to eliminate unnecessary recompositions.
  - Instantaneous 0ms tab switching with spring-animated bottom bar icons.
- **Fixed In-App Update Loop:** Internal version (`0.23.0`) matches the GitHub release tag (`v0.23.0`) and marks installed updates automatically.
