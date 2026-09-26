# ♞ Cep Satrancı

Telefonda ve bilgisayarda tarayıcıdan oynanan satranç. Kurulum veya üyelik gerekmez.

**▶ Hemen oyna: https://debugshaman.github.io/satranc/**

## Neler var?

- **Bilgisayara karşı oyna:** 5 zorluk seviyesi var: Acemi, Kolay, Orta, Zor ve Usta. Bu mod internetsiz de çalışır.
- **Arkadaşınla oyna:** Davet linki oluşturup WhatsApp gibi bir uygulamadan gönderirsin. Arkadaşın linki açınca telefonlarınız doğrudan bağlanır ve hamleler anında görünür. Kimsenin hesap açmasına gerek yok.
- **Tüm satranç kuralları:** Rok, geçerken alma ve piyon terfisi var. Oyun şah mat, pat, üç kez tekrar, 50 hamle kuralı ya da yetersiz materyal ile biter.
- **Dokunarak ya da sürükleyerek oynama:** Önce taşa, sonra gideceği kareye dokunabilir ya da taşı parmağınla sürükleyebilirsin.
- **Oyun kaydı:** Sayfayı kapatsan bile oyun kaldığı yerden devam eder.
- Geri alma, tahtayı çevirme, hamle listesi ve alınan taşlar da var.

## Nasıl oynanır?

### Bilgisayara karşı
1. Sayfayı aç. Açılışta **Bilgisayara karşı** sekmesi seçili gelir.
2. Rengini ve zorluk seviyesini seç, sonra **Yeni oyun**'a dokun.

### Arkadaşınla
1. **Arkadaşla** sekmesinde rengini seç ve **Davet linki oluştur**'a dokun.
2. Linki **Paylaş** ya da **Linki kopyala** düğmesiyle arkadaşına gönder. Arkadaşın katılana kadar sayfayı açık tut.
3. Arkadaşın linki açınca oyun başlar. İstersen arkadaşın linki açmak yerine 6 haneli kodu **Katıl** kutusuna da yazabilir.
4. Oyun bitince **Rövanş** ile renkleri değiştirip yeniden oynayabilirsiniz.

> Bağlantı kurulamazsa Wi-Fi'da dene. Bazı mobil operatör ağları doğrudan bağlantıya izin vermiyor.

## Telefona uygulama olarak yükle

- **Android (Chrome):** Sayfadaki **Uygulama olarak yükle** düğmesine dokun.
- **iPhone (Safari):** Alttaki **Paylaş** düğmesine dokun, sonra **Ana Ekrana Ekle**'yi seç.

Yükledikten sonra oyun ana ekranda kendi ikonuyla tam ekran açılır.

## Teknik bilgiler

- Oyunun tamamı tek bir `index.html` dosyasında. Satranç kuralları ve yapay zekâ (alfa-beta araması) sıfırdan yazıldı, harici bir satranç kütüphanesi kullanılmıyor.
- Arkadaşla oyun, telefonlar arasında doğrudan (WebRTC) bağlantı kurar. Tarafların birbirini bulması için ücretsiz [PeerJS](https://peerjs.com/) sunucusu kullanılır. Oyun verisi herhangi bir sunucuda saklanmaz.
- `manifest.webmanifest` ve `sw.js` dosyaları oyunun uygulama olarak yüklenmesini ve internetsiz açılmasını sağlar.

| Dosya | Görevi |
|---|---|
| `index.html` | Oyunun kendisi: arayüz, kurallar, yapay zekâ ve çevrimiçi mod |
| `manifest.webmanifest` | Uygulama adı, ikonlar ve renkler |
| `sw.js` | Çevrimdışı çalışma için önbellek |
| `*.png` | Uygulama ikonları |
