# ANABEYİN SOSYAL — TIPA TIP GÖRSEL TEMA DÖNÜŞÜMÜ + SINIRLI AJAN YAPISI

## ANA GÖREV

SADECE GÖRSEL TEMA DÖNÜŞÜMÜ YAP. BU TALİMATIN DIŞINA ÇIKMA.

GÖRSEL OLARAK TIPA TIP YAKLAŞTIRILACAK HEDEF:
https://anabeyin.com/eski-onizleme/

TEKNİK OLARAK AYNEN KORUNACAK, ŞU ANDA GERÇEKTEN ÇALIŞAN SİSTEM:
https://anabeyin.com/uygulama/

MEVCUT KULLANICI FRONTEND DOSYALARI:
/var/www/anabeyin/sosyal-ui/

ANA ÇALIŞMA ALANI:
/var/www/anabeyin/

## 1. İSTEDİĞİM ŞEYİ KESİNLİKLE DOĞRU ANLA

Eski önizleme sürümünün ALT YAPISINI istemiyorum.

Eski önizlemenin eski backend'ini, eski veritabanını, eski authentication sistemini, eski API'lerini, eski localStorage mantığını, eski route mantığını, eski uygulama JavaScript mantığını ve eski çalışmayan buton davranışlarını GERİ GETİRME.

Eski önizleme geçmişte görsel olarak çok başarılıydı fakat teknik olarak gerçek çalışan sosyal medya sistemi değildi. Birçok alanı görsel olarak vardı fakat arkasındaki sistem boştu veya eksikti. Bu nedenle eski sistemin teknik motoru rafa kaldırıldı.

Şu anda https://anabeyin.com/uygulama/ adresinde çalışan sistem ise sıfırdan geliştirilmiş gerçek AnaBeyin sistemidir. Bu sistemin backend'i, veritabanı, API'leri, auth'u, kullanıcı sistemi, session/token sistemi, profil sistemi, arkadaş sistemi, gönderileri, yorumları, medya yüklemesi, hikâyeleri, mesajları, bildirimleri, grupları, sayfaları, Reels sistemi, kaydedilenleri, keşfet sistemi, gizlilik/güvenlik sistemi, yönetim sistemi, ajan sistemi, AI sistemi, organizasyon sistemi, log/denetim sistemi ve servisleri ÇALIŞIYOR VE KORUNACAK.

SORUN MOTOR DEĞİL. SORUN SADECE KULLANICIYA GÖRÜNEN TASARIM.

DOĞRU FORMÜL:
ŞU ANDA ÇALIŞAN ANABEYİN SİSTEMİNİN MOTORU VE TÜM ÇALIŞAN FONKSİYONLARI + ESKİ ÖNİZLEMENİN KULLANICIYA GÖRÜNEN GÖRSEL KABUĞU = İSTENEN SONUÇ.

BU KEZ "ESKİ TEMADAN ESİNLEN", "BENZERİNİ YAP", "RENKLERİ YAKLAŞTIR", "MEVCUT CSS'E BİRKAÇ OVERRIDE EKLE" YETERLİ DEĞİLDİR.

İSTEDİĞİM: ESKİ ÖNİZLEMEDE KULLANICI EKRANDA NE GÖRÜYORSA, MEVCUT ÇALIŞAN SOSYAL UYGULAMANIN KULLANICI TARAFINDA ONU MÜMKÜN OLAN EN YÜKSEK GÖRSEL SADAKATLE YENİDEN ÜRET.

## 2. BU GÖREVİN NEDENİ

Şu an çalışan sistem teknik olarak başarılı fakat görsel olarak istediğim seviyede değil. Şu anki canlı tasarımda gereğinden fazla boşluk var, bazı alanlar çok iri, sol navigasyon seyrek, header eski önizlemeye göre fazla boş, sosyal ağ yoğunluğu düşük, kartlar fazla generic, placeholder/test görüntüsü fazla, gerçek sosyal ağ hissi yeterli değil, hikâyeler eski önizleme kadar yoğun değil, sağ panel daha cansız, üst menü daha basit, gönderi kartlarının oranları farklı ve ikon/yazı/spacing ölçüleri eski önizlemeyle aynı değil.

Eski önizlemede özellikle yoğun ama düzenli üst navigasyon, çok sayıdaki küçük üst menü, kompakt sol kullanıcı ve menü paneli, arama alanlarının biçimi, orta feed genişliği, composer tasarımı, hikâye sırası, gerçek yüzlü avatarlar, küçük ve zarif gönderi kartları, sağ arkadaş paneli, kırmızı aktif vurgular, küçük ikonlar, ince borderlar, hafif gölgeler, yazı boyutları, kolon oranları ve bütün sayfanın dolu/yaşayan sosyal ağ görünümü beğenilmektedir.

## 3. ESKİ ÖNİZLEME GÖRSEL HEDEFTİR

https://anabeyin.com/eski-onizleme/ adresini bir fikir veya ilham olarak kullanma. ONU GÖRSEL HEDEF OLARAK KULLAN.

Eski önizlemeyi aç. Ana ekranı, profil dahil erişilebilen diğer ortak kullanıcı ekranlarını incele. Gerekirse aynı ekranı birkaç kez incele. Screenshot al. Sonra https://anabeyin.com/uygulama/ içindeki aynı ekranı aynı viewport'ta aç. Yan yana karşılaştır. Tahmin ederek UI yapma.

## 4. GÖRSEL OLARAK KOPYALANACAK HER ŞEY

Kullanıcı ekranında gördüğü her şey bu görevin kapsamındadır: sayfa genel genişliği/max-width, sayfa arka planı, kolon yapısı ve oranları, kolon konumları/boşlukları, header yüksekliği/border/shadow, logo konumu ve alanı, üst navigasyon, ikon/yazı oranları, aktif menü, kırmızı vurgular, notification badge'leri, sağ kullanıcı alanı, arama kutusunun konumu/genişliği/yüksekliği/radius'u/renkleri/fontu, sol kullanıcı alanı, avatar boyutu, kullanıcı adı/alt bilgi, online noktası, menü satırları, ikonlar, aktif menü arka planı, scrollbar, orta kolon, composer, story, filtre/chip, post kartları, post aralıkları, avatarlar, post meta satırları, üç nokta menüsü, medya oranları, separatorlar, aksiyon satırları, sağ panel, dropdown/popup/modal/input/textarea/button/tab/chip, hover/focus/active, font-family/font-weight/font-size/line-height, muted renkler, border/kırmızı/gri tonları, margin/padding sistemi ve responsive görünüm.

KULLANICI EKRANDA GÖRÜYORSA GÖRSEL DÖNÜŞÜMÜN PARÇASIDIR.

## 5. ESKİ ÜST MENÜYÜ EKSİK KOPYALAMA

Eski önizlemedeki üst navigasyon görünümünü tam olarak yeniden üret. Eski önizlemede görünen Ana, Eşleş, Kesit, Canlı, Video, Blog, Forum, Sözlük, Düzenlemek, İlanlar, Hizmet, Oyun, Yapay zeka ve diğer görünen üst menü elemanları tasarımın görsel bütünlüğünün parçasıdır.

Şu anda çalışan sistemde bunların bazılarının teknik altyapısı henüz yoksa ARKALARINA YENİ BACKEND YAZMA, DB TABLOSU OLUŞTURMA, API OLUŞTURMA, BÜYÜK YENİ ÖZELLİK GELİŞTİRME. Ama eski önizlemenin header'ını eksik bırakarak tasarımı bozma. Görsel menü elemanlarını eski önizlemedeki yerlerinde göster. Henüz teknik karşılığı olmayan alanlara tıklandığında tasarımla uyumlu boş içerik alanı veya henüz doldurulmamış kullanıcı ekranı gösterilebilir. Bu boş alanlar daha sonra ayrıca geliştirilecektir.

## 6. SOL MENÜDE DE AYNI KURAL

Eski önizlemenin sol menüsünün görsel düzenini koru. Eski önizlemede görünmesine rağmen yeni sistemde teknik karşılığı olmayan alanlar için backend icat etme. Ama tasarımın görsel yoğunluğunu ve menü düzenini eksik bırakma. Mevcut çalışan sosyal route'lar gerçek fonksiyonlarına bağlı kalacak.

## 7. ORTAK SAYFALARDA ÇOK SIKI SADAKAT

Ana sayfa, profil, hikâyeler, gönderiler ve composer iki sistemde de varsa canlı çalışan sürüm görsel olarak eski önizleme sürümüne dönüştürülecek. Arkadaşlar, gruplar, sayfalar, Reels, kaydedilenler, keşfet, mesajlar, bildirimler ve ayarlar gibi mevcut gerçek özellikler korunacak ve eski önizleme tasarım sisteminin aynı görsel ailesinde sunulacak.

## 8. GÖNDERİ AKSİYONLARI İÇİN ÖZEL VE KESİN KURAL

Gönderilerin altında kullanıcıya görünen ANA aksiyonlar SADECE:
BEĞEN
YORUM YAP
PAYLAŞ
olacak.

Muhteşem, Öfkeli, Haha, Üzgün, Sevgi veya başka emoji reaction seçenekleri ve emoji reaction picker GÖRSEL ARAYÜZDEN KALDIRILACAK. Backend veya DB'de reaction tabloları/verileri varsa SİLME, DB şemasını değiştirme, backend'i bozma. Sadece kullanıcı arayüzünde emoji reaction çeşitlerini gösterme.

Kaydet işlevi backend'de varsa silme; gerekiyorsa üç nokta menüsüne veya ikincil kullanıcı alanına taşı. ANA GÖRÜNÜM: BEĞEN | YORUM YAP | PAYLAŞ.

## 9. GERÇEKÇİ AVATAR / PROFİL / MEDYA

Eski önizleme kaynaklarında VPS üzerinde bulunan avatarları, profil resimlerini, kapakları, hikâye görsellerini, post fotoğraflarını ve video/Reel medyalarını envanterle. Sadece mevcut test/demo/sentetik kullanıcılara mevcut çalışan sistemin gerçek API/DB/media yapısıyla bağla. Frontend'e hardcode etme, sahte JSON yapma, base64 gömme. DB şeması değiştirme, migration/yeni tablo/yeni medya altyapısı/yeni backend endpoint oluşturma. Gerçek kullanıcı verisine, şifrelere ve auth'a dokunma.

## 10. ESKİ UYGULAMANIN BUGLARINI KOPYALAMA

GÖRSEL GÖRÜNÜMÜ KOPYALA, BUGLARI KOPYALAMA. Bozuk resim ikonları, eski marka artıkları, eski auth/localStorage/API/backend/routing/çalışmayan buton mantığı ve eski minified uygulama motoru kopyalanmayacak.

## 11. ÇALIŞMA ALANI VE YASAK ALANLAR

ESAS ÇALIŞMA ALANI: /var/www/anabeyin/sosyal-ui/

İlk değişiklikten önce sosyal-ui klasörünün tarih-saatli yedeğini al. Test/demo medya verisinde izin verilen değişiklik olacaksa mevcut DB'nin güvenli yedeğini al.

KESİNLİKLE DOKUNMA: /yonetim/, /ajan/, core backend, DB şeması, migration sistemi, auth, password sistemi, token/session sistemi, API contract, Patron AI, ajan organizasyonu, yönetim sistemi, dijital ikiz sistemi, nginx, SSL, SSH, recovery/keeper/watchdog, systemd ve unrelated projeler.

BU GÖREVDE DAYANIKLILIK ALTYAPISINI YENİDEN GELİŞTİRME. TEMA İŞİ YAP.

## 12. AJAN YAPISI — SINIRLI, KONTROLLÜ VE TEK HEDEFLİ

ANA KIMI KOORDİNATÖR OLACAK. AJANLAR KENDİ BAŞLARINA BAŞKA AJAN OLUŞTURMAYACAK. SUBAGENT → SUBAGENT zinciri YASAK. Yüzlerce ajan ve ilgisiz ajan YASAK. MAKSİMUM 5 UZMAN ALT AJAN KULLAN.

### AJAN 1 — GÖRSEL REFERANS / PİKSEL KARŞILAŞTIRMA AJANI
Görevi: eski önizleme ile canlı uygulamayı aynı viewport'ta karşılaştırmak; header, üst menü, arama, sol panel, kolon oranları, story, composer, feed, post, sağ panel, profil, font, ikon, spacing, renk, radius, border, shadow, modal ve responsive farklarını somut listelemek. KOD/DOSYA/DB/BACKEND DEĞİŞTİRMEYECEK.

### AJAN 2 — FRONTEND UYGULAMA AJANI
Görevi: sadece /var/www/anabeyin/sosyal-ui/ altında görsel fark listesini uygulamak. CSS, gerekli kullanıcı UI JS, gerekli HTML/DOM/markup ve kullanıcı UI assetleri ile çalışacak. Backend/DB/auth/yönetim/ajan/nginx/systemd tarafına dokunmayacak.

### AJAN 3 — DEMO MEDYA / GÖRSEL İÇERİK AJANI
Görevi: eski önizlemede VPS üzerinde bulunan uygun medya dosyalarını bulmak ve yalnız mevcut test/demo/sentetik kullanıcılar için avatar, profil, kapak, hikâye, fotoğraflı gönderi ve varsa video/Reel eşleşmelerini mevcut veri modeli ile hazırlamak. Yeni backend/DB şeması oluşturmayacak, gerçek kullanıcıya dokunmayacak.

### AJAN 4 — RESPONSIVE VE GÖRSEL QA AJANI
Görevi: uygulama bittikten sonra desktop 1440+, tablet 768–1024 ve mobil 360–430 görünümünü eski önizlemeyle karşılaştırmak; hizalama, spacing, font, ikon, card width, kolon, overflow, mobil menü ve viewport hatalarını raporlamak. KOD YAZMAYACAK.

### AJAN 5 — DENETLEYİCİ / KAPSAM KORUYUCU AJAN
Görevi: ana Kimi ve diğer ajanların bu talimatın dışına çıkıp çıkmadığını denetlemek. Gereksiz backend, DB şeması, yönetim, ajan sistemi, Patron AI, systemd/keeper/watchdog, ilgisiz güvenlik işi, yeni özellik, gereksiz test/rapor, fazla ajan, subagent zinciri, eski teknik sistemi geri getirme veya gerçek kullanıcı verisine dokunma girişiminde ANA KIMI'YE "DUR — KAPSAM DIŞI" diyecek. Kendi başına proje kodu değiştirmeyecek veya yeni ajan oluşturmayacak.

## 13. ANA KIMI'NİN AJANLARI KOORDİNE ETME KURALI

Ana Kimi aynı dosyada iki frontend ajanına paralel write yaptırmayacak; visual agent ile implementation agent'i ayıracak; denetleyiciyi kapsam koruyucu olarak kullanacak; QA bulgularından sonra gerekli final düzeltmeleri yapacak; 5 ajanın dışına çıkmayacak; ajanların kendi ajanlarını oluşturmasına izin vermeyecek.

## 14. GÖRSEL ÇALIŞMA SIRASI

1. sosyal-ui yedeği
2. görsel karşılaştırma ajanının eski/canlı ekran analizi
3. denetleyici kapsam kontrolü
4. ana desktop layout
5. header
6. üst navigasyon
7. search
8. sol panel
9. orta feed
10. composer
11. hikâyeler
12. post kartları
13. post aksiyonları
14. sağ panel
15. profil
16. login/kayıt/kurtarma görselleri
17. arkadaşlar
18. gruplar
19. sayfalar
20. Reels
21. kaydedilenler
22. keşfet
23. mesajlar
24. bildirimler
25. ayarlar/gizlilik/güvenlik
26. demo/test medya zenginleştirmesi
27. tablet
28. mobil
29. QA ajanı kontrolü
30. denetleyici kapsam kontrolü
31. gerekli final düzeltmeler
32. son yan yana görsel kontrol
33. hedefli fonksiyon testi
34. bitiş.

## 15. GÖRSEL KARŞILAŞTIRMA DÖNGÜSÜ

Her ana ekranda: eski önizlemeyi aç, canlı karşılığını aç, aynı viewport kullan, screenshot al, yan yana incele, fark listesini çıkar, farkları uygula, tekrar screenshot al, yeniden karşılaştır ve belirgin fark varsa düzelt. Bir kere bakmak yeterli değildir.

## 16. FAZLA TEST YAPMA

Bütün AnaBeyin sistemini, yönetim veya ajan sistemini tekrar tekrar test/audit etme. Sadece tema değişikliğinin çalışan sosyal fonksiyonları bozmadığını kanıtlayacak hedefli minimum testleri çalıştır: login, logout, ana feed, post oluşturma, foto/video yükleme, beğen, yorum, paylaş, hikâye, profil, arkadaş, grup, sayfa, Reels, mesaj, bildirim, keşfet, ayarlar.

## 17. DESKTOP / TABLET / MOBİL

Desktop en önemli görsel referanstır. Eski önizleme desktop görünümüne çok yüksek sadakat sağla. Sonra tablet ve mobile uyarla. Mobilde yatay overflow, görünmeyen menü, üst üste binme, kesilen buton, viewport dışı modal, dev boşluk ve kullanılamayan navigasyon olmayacak.

## 18. BAŞARI KRİTERİ

İki sekmede https://anabeyin.com/eski-onizleme/ ve https://anabeyin.com/uygulama/ açıldığında ilk bakışta "aynı tema, ama ikincisinin arkasında gerçek çalışan AnaBeyin sistemi var" görülmelidir. Sadece renklerin benzemesi, bazı avatarların aktarılması, style.css değişmesi veya testlerin PASS olması kabul edilmez. GÖRSEL EKRANIN KENDİSİ HEDEFTİR.

## 19. FİNAL GÖRSEL DENETİM

Finalde şu maddeleri gerçek ekran görüntüsüyle doğrula:
HEADER_ESKIYLE_AYNI_GORSEL_YAPI=
UST_MENU_ESKIYLE_AYNI_GORSEL_YAPI=
UST_MENU_ELEMAN_DUZENI=
ARAMA_ESKIYLE_AYNI_GORSEL_YAPI=
SOL_PANEL_ESKIYLE_AYNI_GORSEL_YAPI=
ANA_FEED_ESKIYLE_AYNI_GORSEL_YAPI=
COMPOSER_ESKIYLE_AYNI_GORSEL_YAPI=
STORIES_ESKIYLE_AYNI_GORSEL_YAPI=
POST_KARTLARI_ESKIYLE_AYNI_GORSEL_YAPI=
POST_AKSIYONLARI=BEGEN_YORUM_YAP_PAYLAS
EMOJI_REACTION_UI=YOK
SAG_PANEL_ESKIYLE_AYNI_GORSEL_YAPI=
PROFIL_ESKIYLE_AYNI_GORSEL_YAPI=
FONT_OLCULERI_ESKIYLE_UYUMLU=
IKON_OLCULERI_ESKIYLE_UYUMLU=
KOLON_ORANLARI_ESKIYLE_UYUMLU=
SPACING_ESKIYLE_UYUMLU=
BORDER_RADIUS_ESKIYLE_UYUMLU=
RENKLER_ESKIYLE_UYUMLU=
DESKTOP_GORSEL_SADAKAT=
TABLET_GORSEL_SADAKAT=
MOBIL_GORSEL_SADAKAT=
DEMO_TEST_AVATARLARI=
DEMO_TEST_KAPAKLARI=
DEMO_TEST_FOTOGRAFLI_POSTLAR=
DEMO_TEST_STORY_MEDYA=
DEMO_TEST_VIDEO_REEL=
BACKEND_DEGISTI=HAYIR
DB_SEMASI_DEGISTI=HAYIR
AUTH_DEGISTI=HAYIR
YONETIM_DEGISTI=HAYIR
AJAN_SISTEMI_DEGISTI=HAYIR
NGINX_DEGISTI=HAYIR
SYSTEMD_DEGISTI=HAYIR

## 20. DENETLEYİCİ AJAN FİNAL ONAYI

İş tamamlandı denmeden önce denetleyici ajan son kez kontrol edecek: sadece tema mı yapıldı; backend/DB/yönetim/ajan gereksiz değişti mi; gereksiz özellik/ajan/test/araştırma yapıldı mı; eski teknik sistem taşındı mı; görsel hedef gerçekten eski önizleme mi; ortak ekranlar yüksek sadakatle yaklaştı mı; emoji reaction UI kaldırıldı mı; ana post aksiyonları Beğen/Yorum Yap/Paylaş mı; test/demo kullanıcılarında uygun gerçek medya görünüyor mu; kullanıcı isteği dışında gereksiz değişiklik var mı. Denetleyici KAPSAM_UYGUN=EVET demeden görev tamamlanmış kabul edilmesin.

## 21. KESİN YASAKLAR

Backend rewrite, DB schema change, migration, auth rewrite, şifre/token değiştirme, yönetim paneli geliştirme, ajan sistemi geliştirme, organizasyon geliştirme, Patron AI geliştirme, nginx/SSL/SSH/recovery/keeper/watchdog/systemd değiştirme, yeni sistem mimarisi, yeni sosyal motor, yeni büyük özellik paketi, yüzlerce ajan, subagent'ın subagent oluşturması, gereksiz uzun araştırma/rapor ve bütün sistemin yeniden audit edilmesi YASAKTIR.

## 22. SON VE BAĞLAYICI EMİR

ESKİ ÖNİZLEME: https://anabeyin.com/eski-onizleme/ GÖRSEL HEDEFTİR.
CANLI ÇALIŞAN SİSTEM: https://anabeyin.com/uygulama/ TEKNİK GERÇEKTİR.
MOTORU KORU. KAPORTAYI ESKİ ÖNİZLEMEYE DÖNÜŞTÜR.

Menüden arama kutusuna, header'dan sol panele, story'den composer'a, avatardan post kartına, sağ panele, font/ikon boyutuna, spacing'e, border'a, radius'a, renge ve profil sayfasına kadar kullanıcının gözüyle görülen her şey eski önizlemeye mümkün olan en yüksek sadakatle yaklaşacak.

Arka planda çalışan gerçek sistemleri bozma. Eski uygulamanın çalışmayan motorunu geri getirme. Görsel olarak gerekli fakat teknik karşılığı olmayan eski menüleri tasarımı tamamlamak için göster; arkalarına yeni backend icat etme. Mevcut gerçek sosyal fonksiyonları koru.

POST ANA AKSİYONLARI: BEĞEN, YORUM YAP, PAYLAŞ. EMOJI REACTION UI OLMAYACAK.

Ajanlar sadece bu hedef için çalışacak. Denetleyici ajan kapsam dışına çıkışı engelleyecek. Fazla iş yapma. Bu tek işi doğru yap. Görsel hedef gerçekten yakalanmadan TAMAMLANDI deme. Gerekli düzeltmeleri yap, son QA'yı yap, denetleyici onayını al ve sonra bitir.
