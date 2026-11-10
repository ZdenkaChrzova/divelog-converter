# DiveLog Converter 1.5.0

DiveLog Converter převádí fotografie a PDF ručně psaných potápěčských deníků do údajů ke kontrole a následně do CSV pro Diving LogBook.

## Novinky ve verzi 1.5.0

- cloudové rozpoznávání rukopisu pomocí modelu `gemini-3.8-flash`,
- bezpečné volání přes Cloudflare Worker `divelog-converter-api`,
- API klíč není součástí frontendového kódu ani GitHubu,
- podpora JPG, PNG, WEBP a PDF do 10 MB,
- kontrola délky ponoru podle času začátku a konce,
- ruční kontrola všech rozpoznaných hodnot před exportem.

## Cloudová služba

Frontend volá `https://divelog-converter-api.z-chrzova.workers.dev/analyze-dive`. Nahraný soubor je odeslán ke zpracování do Google Gemini API. Cloudflare Worker soubor trvale neukládá.

## Nasazení

Nahraj obsah ZIPu do kořenové složky GitHub repozitáře. Staré soubory `app.js`, `app-1.4.3.js` a `app-debug3.js` už aplikace nepoužívá a lze je po úspěšném ověření odstranit.
