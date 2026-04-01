# AI Hub — Kişisel AI Uygulaması

Nano Banana, Kling, FLUX, Stable Audio, Claude ve Gemini'yi tek çatı altında toplayan PWA.

## Deploy (5 dakika)

### 1. GitHub'a yükle

1. github.com → **New repository** → isim: `ai-hub` → Create
2. Bilgisayarına klasörü zip'le, ya da:

```bash
cd ai-hub
git init
git add .
git commit -m "ilk sürüm"
git remote add origin https://github.com/KULLANICI_ADIN/ai-hub.git
git push -u origin main
```

### 2. Vercel'e bağla

1. vercel.com → **Add New Project**
2. GitHub hesabını bağla → `ai-hub` repo'sunu seç
3. **Deploy** — bitti!
4. Sana bir URL verir: `ai-hub-xxx.vercel.app`

### 3. Telefona ekle

**iPhone:** Safari → ai-hub-xxx.vercel.app → Paylaş → **Ana Ekrana Ekle**
**Android:** Chrome → ai-hub-xxx.vercel.app → Menü → **Ana ekrana ekle**

### 4. API Key'lerini gir

Uygulamada **Ayarlar** sekmesi → key'leri yaz → Kaydet.

Key'ler tarayıcının güvenli deposunda (localStorage) saklanır, sunucuya gitmez.

## Modeller

| Model | Sağlayıcı | Tür |
|-------|-----------|-----|
| Nano Banana | fal.ai | Görsel |
| FLUX Dev | fal.ai | Görsel |
| FLUX Pro 1.1 | fal.ai | Görsel |
| Kling v3 | fal.ai | Video |
| Stable Audio | fal.ai | Ses |
| Claude Sonnet 4 | Anthropic | Sohbet |
| Gemini 2.5 Pro | Google | Sohbet |

## Yeni model eklemek

`index.html` içinde `falModelIds` objesine ekle:
```js
'yeni-model': 'fal-ai/model-adi',
```

## Dosya yapısı

```
ai-hub/
├── public/
│   ├── index.html      ← tek sayfa uygulama
│   ├── manifest.json   ← PWA tanımı
│   ├── sw.js           ← service worker (offline)
│   ├── icon-192.png
│   └── icon-512.png
└── vercel.json         ← Vercel ayarları
```
