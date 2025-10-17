
## 📄 `frequencies.json`

```json
{
  "radioStations": [
    {
      "id": 1,
      "name": "ASPOR",
      "frequency": "",
      "streamUrl": "http://trkvz-radyolar.ercdn.net/asporradyo/playlist.m3u8",
      "region": "Tüm Türkiye"
    },
    {
      "id": 2,
      "name": "GİMSA RADYO",
      "frequency": "",
      "streamUrl": "http://yayin1.canliyayin.org:9482/stream",
      "region": "Tüm Türkiye"
    }
  ],
  "tvChannels": [
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
    },
    {
      "id": 2,
      "name": "TRT 1",
      "streamUrl": "https://tv-trt1.medya.trt.com.tr/master_720.m3u8",
      "region": "Tüm Türkiye",
      "satellite": "Türksat 42E",
      "frequency": "11958",
      "polarization": "V",
      "symbolRate": "27500",
      "FEC": "5/6"
    }
  ]
}
```

## 📘 README.md (Güncellenmiş)

````markdown
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
````

---

## 💻 Usage Example (JavaScript)

```js
fetch("media.json")
  .then(res => res.json())
  .then(data => {
    data.tvChannels.forEach(tv => {
      console.log(`${tv.name} - Stream: ${tv.streamUrl}, Sat: ${tv.satellite}`);
    });
  });
```

---

## 🧠 Notes / Notlar

* Supports both **live IPTV URLs** and **satellite broadcast details**.
* `polarization` values are `"H"` for Horizontal and `"V"` for Vertical.
* `FEC` indicates the error correction rate (e.g., `5/6`, `3/4`).
* Use UTF-8 encoding when saving the file.
* Designed for **media players**, **EPG systems**, and **TV guides**.

---

📅 **Last Update / Son Güncelleme:** October 17, 2025
👨‍💻 **Created by / Hazırlayan:** Kerem Mutlu
