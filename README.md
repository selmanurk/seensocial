<div align="center">

# ✦ SEEN

### *culture worth sharing*

A culture-sharing iOS app where you curate your taste in **film, TV, books and music** —
and recommend it directly to the friends who'll love it. No algorithm. No feed-chasing.
Just your taste, sent to the people who get you.

[![Download on the App Store](https://img.shields.io/badge/Download-App_Store-0D96F6?style=for-the-badge&logo=apple&logoColor=white)](https://apps.apple.com/app/id6783413583)
&nbsp;
[![Website](https://img.shields.io/badge/seenapp.online-B45A2C?style=for-the-badge&logo=safari&logoColor=white)](https://seenapp.online)

</div>

---

<p align="center">
  <img src="screenshots/01_taste.png" width="19%" alt="Taste profile" />
  <img src="screenshots/02_discover.png" width="19%" alt="Discover" />
  <img src="screenshots/03_share.png" width="19%" alt="Share card" />
  <img src="screenshots/04_post.png" width="19%" alt="Recommendations" />
  <img src="screenshots/05_tagged.png" width="19%" alt="Tagged inbox" />
</p>

## What it does

- **Build a taste profile** — your top picks across Movies, TV, Books and Music, searched live from real catalogs
- **Recommend to friends** — tag someone on anything worth their time; it lands in their personal *Tagged* inbox
- **Two gentle feeds** — *Following* (people you trust) and *Discover* (new taste), no infinite scroll
- **One-tap share card** — export your taste as an Instagram Story in the app's own aesthetic
- **The essentials** — Sign in with Apple, push notifications, dark mode, profile photos, and full account controls

## Tech stack

![Expo](https://img.shields.io/badge/Expo_SDK_54-000020?logo=expo&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-20232A?logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?logo=prisma&logoColor=white)
![Neon Postgres](https://img.shields.io/badge/Neon_Postgres-4169E1?logo=postgresql&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)

| Layer | Built with |
|---|---|
| **Mobile app** | React Native (Expo SDK 54), TypeScript, React Navigation, Reanimated |
| **Backend** | Node.js / Express, deployed serverless on Vercel |
| **Database** | Neon Postgres with Prisma ORM |
| **Auth** | JWT sessions + Sign in with Apple |
| **Image storage** | Vercel Blob |
| **Push** | Expo Notifications |
| **External data** | TMDB (film/TV), Google Books, iTunes (music) |
| **Build & delivery** | EAS Build / Submit, EAS Update (OTA) |

## Architecture

```mermaid
flowchart LR
  App["📱 React Native app<br/>(Expo, TypeScript)"]
  API["⚙️ Express API<br/>(Vercel serverless)"]
  DB[("🗄️ Neon<br/>Postgres")]
  Blob["🖼️ Vercel Blob"]
  Ext["🎬 TMDB · 📚 Google Books · 🎵 iTunes"]
  Push["🔔 Expo Push"]

  App -->|JWT over HTTPS| API
  App -->|live search| Ext
  API --> DB
  API --> Blob
  API --> Push
```

## Status

**Live on the App Store** — available in the US, UK, Canada, Australia and Türkiye.
Shipped end-to-end: real database, authentication, push notifications, legal pages and
over-the-air updates.

## About

Designed and built by **Selma Nur Keskin**.

<sub>This product uses the TMDB API but is not endorsed or certified by TMDB. Artwork and
metadata belong to their respective rights holders.</sub>
