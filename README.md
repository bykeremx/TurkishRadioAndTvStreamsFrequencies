# 📺🎵 Media Stations JSON Data / Radyo ve TV Verileri

This dataset includes both **radio stations** and **TV channels** from Turkey in a well-structured JSON format.  
It supports both **internet (IPTV)** and **satellite (DVB)** stream information.

Bu veri seti, **Türkiye'deki radyo istasyonlarını** ve **TV kanallarını** JSON formatında içerir.  
Hem **internet (IPTV)** hem de **uydu (DVB)** yayın bilgilerini destekler.

---

## 🧩 TV Channel Structure / TV Kanal Yapısı

| Field | Type | Description (EN) | Açıklama (TR) |
|-------|------|------------------|----------------|
| `id` | Number | Unique ID for the channel | Kanal için benzersiz kimlik |
| `name` | String | Channel name | Kanal adı |
| `streamUrl` | String | Online stream link | İnternet yayın bağlantısı |
| `region` | String | Broadcast area | Yayın yapılan bölge |
| `satellite` | String | Satellite name | Uydu adı |
| `frequency` | String | Frequency (MHz) | Frekans (MHz) |
| `polarization` | String | Signal polarization (H/V) | Polarizasyon (Yatay/Dikey) |
| `symbolRate` | String | Symbol rate (KS/s) | Sembol oranı (KS/s) |
| `FEC` | String | Forward Error Correction rate | Hata düzeltme oranı |

---

## 📺 Example TV Channel / Örnek TV Kanalı

```json
{
  "id": 1,
  "name": "4U TV",
  "streamUrl": "https://hls.4utv.live/hls/stream.m3u8",
  "region": "Tüm Türkiye",
  "satellite": "Türksat 42E",
  "frequency": "12034",
  "polarization": "H",
  "symbolRate": "30000",
  "FEC": "5/6"
}
