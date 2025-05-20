---
title: API integráció
sidebar_position: 2
---
# 🌐 API Integráció Útmutató

## 📌 Bevezetés
Ez a dokumentáció segít az API integráció lépéseiben, a hitelesítés beállításától kezdve a végpontok használatáig.

## 🔐 API Hitelesítés
Az API használatához először hitelesítési adatokra van szükség. A leggyakoribb módszerek:
**API kulcs:** Egyszerű és gyors hitelesítés egy adott kulccsal.
**OAuth 2.0:** Biztonságosabb, token-alapú autentikáció.
**JWT Tokenek:** Biztonságos és skálázható megoldás.

Példa API kulcs használatára:
## 🔄 API Kérések és Végpontok
Az API végpontok segítségével különböző műveleteket hajthatunk végre. Példák:

**📥 Adatlekérés (GET)**
http
GET /data HTTP/1.1
Host: api.example.com
Authorization: Bearer YOUR_API_KEY


**📥 Adatküldés (POST)**
POST /users HTTP/1.1
Host: api.example.com
Content-Type: application/json
Authorization: Bearer YOUR_API_KEY
  "name": "John Doe",
  "email": "johndoe@example.com"

**🛠 Adatmódosítás (PUT)**
PUT /users/123 HTTP/1.1
Host: api.example.com
Content-Type: application/json
Authorization: Bearer YOUR_API_KEY
  "email": "newemail@example.com"

**❌ Adattörlés (DELETE)**
DELETE /users/123 HTTP/1.1
Host: api.example.com
Authorization: Bearer YOUR_API_KEY

## 📡 API Válaszok
Az API által küldött válaszkódok a következőket jelzik:

**200 OK** – Sikeres válasz

**201 Created** – Az erőforrás létrejött

**400 Bad Reques** – Hibás kérés

**401 Unauthorized** – Nincs jogosultság

**404 Not Found** – Erőforrás nem található

**500 Internal Server Error** – Szerverhiba