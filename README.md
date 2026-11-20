# T3 Code — Türkçe Topluluk Derlemesi (macOS Apple Silicon)

Bu depo, açık kaynaklı [T3 Code (`pingdotgg/t3code`)](https://github.com/pingdotgg/t3code) uygulamasının henüz ana dala birleştirilmemiş olan **Türkçe dil desteği PR'ı ([#38681](https://github.com/pingdotgg/t3code/pull/38681))** ile derlenmiş **macOS Apple Silicon (`arm64`)** paketini paylaşır.

> **Not:** Bu resmi bir T3 Tools yayını değildir. Resmi sürümde Türkçe dil desteği birleştirildiğinde doğrudan [t3.codes](https://t3.codes) üzerinden resmi uygulamayı kullanmanız önerilir.

---

## İndirme

En güncel `.dmg` dosyasını [**Releases**](https://github.com/SDcode19/t3code-turkish/releases) sayfasından indirebilirsiniz.

- **Sürüm:** `v0.1.11-tr` (commit `2b2d53f6` — `egegungordu/t3code@feat/i18n-turkish`)
- **Platform:** macOS Apple Silicon (`arm64` / M1, M2, M3, M4+)
- **SHA-256 (`T3-Code-0.1.11-arm64.dmg`):**
  ```text
  0c5814cdbbdf1778032a59602b39755c835ca57c3adccee744b4550ee7d10ec9
  ```

---

## Kurulum (macOS)

1. `T3-Code-0.1.11-arm64.dmg` dosyasını açın ve **`T3 Code (Beta).app`** uygulamasını **Uygulamalar (`Applications`)** klasörüne sürükleyin *(isterseniz mevcut resmi kurulumu korumak için adını `T3 Code (TR).app` yapabilirsiniz)*.
2. Yerel/topluluk derlemesi olduğu ve Apple Developer sertifikasıyla imzalanmadığı için ilk açılışta macOS Gatekeeper uyarısı çıkabilir. Karantina işaretini kaldırmak için Terminal'de şu komutu çalıştırın:
   ```bash
   xattr -cr "/Applications/T3 Code (Beta).app"
   ```
   *(Adını `T3 Code (TR).app` yaptıysanız komuttaki yolu ona göre yazın.)*
3. Uygulamayı açtıktan sonra **Settings → General → Language → Türkçe** yolunu izleyerek dili Türkçe yapabilirsiniz.

---

## Neler Değiştirildi?

Resmi `pingdotgg/t3code` (`main`) kaynağı üzerine **yalnızca** [PR #38681](https://github.com/pingdotgg/t3code/pull/38681) kapsamındaki 14 yerelleştirme dosyası (web: 9.737, masaüstü: 122, mobil: 4.815 çeviri anahtarı ve dil kayıtları) dahildir. Herhangi bir ek kod, paket veya telemetri değişikliği yoktur.

### Kendiniz derlemek isterseniz
```bash
git clone --depth 1 --branch feat/i18n-turkish https://github.com/egegungordu/t3code.git
cd t3code
pnpm install
T3CODE_DESKTOP_SIGNED=false pnpm run dist:desktop:dmg:arm64
```

---

## Kaynak ve Teşekkür

- **Ana proje:** [pingdotgg/t3code](https://github.com/pingdotgg/t3code) (MIT Lisansı)
- **Türkçe çeviri PR'ı:** [@egegungordu](https://github.com/egegungordu) — [pingdotgg/t3code#38681](https://github.com/pingdotgg/t3code/pull/38681)

## Lisans

Bu dağıtım [MIT Lisansı](./LICENSE) koşulları altında paylaşılmaktadır (`Copyright (c) 2026 T3 Tools Inc.`).
