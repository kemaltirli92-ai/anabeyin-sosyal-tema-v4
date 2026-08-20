# ANABEYIN SOSYAL TEMA V4 — ANA TALİMAT

## ANA GÖREV

Mevcut çalışan AnaBeyin Sosyal sisteminin **yalnızca kullanıcı tarafı temasını**, eski önizleme temasının tasarımına dönüştür.

**Hiçbir şey sorma. Bu görevi baştan sona otomatik yürüt.**  
Gereken incelemeyi kendin yap, frontend değişikliklerini kendin planla, uygula, test et ve bitir.

---

## 1. KAYNAK TEMA

Kullanılacak tasarım referansı:

- Canlı statik önizleme: `https://anabeyin.com/eski-onizleme/`
- Asıl korunmuş kaynak: `/root/anabeyin-eski-referans-20260812-192751/`
- İlk temanın ana build'i: `/root/anabeyin-eski-referans-20260812-192751/assets/index-DmZZ_QCq.js`
- CSS: `/root/anabeyin-eski-referans-20260812-192751/assets/index-BnffXGZ9.css`
- Giriş: `/root/anabeyin-eski-referans-20260812-192751/index.html`

Bu, kullanıcının beğendiği ilk AnaBeyin tasarımıdır. İçinde örneğin:

- ana akış
- üst alan
- sol/sağ navigasyon
- kartlar
- profil görünümü
- gönderi alanları
- görseller
- Alışveriş
- Eşleş
- Forum
- Bakkal
- diğer eski kullanıcı ekranları

bulunur.

**Eski temanın backend'ini kullanma.**  
**Eski auth sistemini kullanma.**  
**Eski DB'yi geri getirme.**

Eski sistem yalnızca **tasarım, UI, UX, sayfa yerleşimi, bileşen görünümü ve görsel dil referansıdır.**

---

## 2. HEDEF SİSTEM

Hedef, şu anda çalışan yeni AnaBeyin Sosyal V2 sistemidir.

- Ana çalışma alanı: `/var/www/anabeyin`
- Kullanıcı uygulaması: `https://anabeyin.com/uygulama/`

Mevcut yeni sistemin şu parçaları **aynen korunacak**:

- backend
- Express API'leri
- SQLite veritabanı
- mevcut tablolar
- mevcut auth sistemi
- kullanıcı hesapları
- şifre sistemi
- session/token sistemi
- güvenlik sistemi
- izin/yetki sistemi
- gizlilik sistemi
- mesaj sistemi
- bildirim sistemi
- moderasyon sistemi
- AI sistemleri
- ajan sistemi
- capability sistemi
- yönetim dijital ikizleri
- AI operasyon ikizleri
- log/denetim sistemi
- mevcut servisler
- nginx
- SSL
- yedekleme
- recovery/keeper/watchdog

Bunları yeniden yazma, silme, sıfırlama veya eski sistemle değiştirme.

Bu görev **frontend kullanıcı temasının değiştirilmesidir.**

---

## 3. YÖNETİM VE AJAN SİSTEMİNE DOKUNMA

Şunlara tasarım değişikliği yapma:

- `/yonetim/`
- `/ajan/`

Yönetim paneli ve ajan merkezi bu görevin kapsamında değildir.

Frontend'lerine, API'lerine, auth sistemlerine veya verilerine dokunma.

---

## 4. YENİ SAYFA UYDURMA

Sırf eski temada var diye yeni ürün veya backend özelliği oluşturma.

Mevcut V2 sistemde zaten bulunan kullanıcı özelliklerini ve sayfaları, eski temanın görsel diliyle yeniden giydir.

Formül:

**MEVCUT V2 ÖZELLİĞİ + ESKİ TEMANIN TASARIM DİLİ = YENİ ANABEYİN KULLANICI ARAYÜZÜ**

Mevcut V2'de bulunmayan eski ürün alanlarını sırf temada görünüyor diye backend özelliğine dönüştürme.

---

## 5. ESKİ TEMAYI AYRINTILI İNCELE

Önce eski önizlemeyi ve kaynak build'i ayrıntılı incele.

Şunları çıkar:

- genel sayfa genişliği
- header yüksekliği
- logo konumu
- navigasyon yapısı
- sidebar düzeni
- renk sistemi
- arka planlar
- borderlar
- border-radius değerleri
- gölgeler
- kart stili
- tipografi
- başlık ölçüleri
- ikon yerleşimleri
- gönderi kartı
- composer/gönderi oluşturma alanı
- yorumlar
- reaksiyonlar
- avatarlar
- profil kartları
- kapak alanları
- hikâye görünümleri
- medya gridleri
- modal/dialog yapıları
- form alanları
- butonlar
- sekmeler
- mobil navigasyon
- tablet düzeni
- desktop düzeni
- boşluk sistemi
- görsel oranları

Sonra mevcut V2 frontend'deki gerçek bileşenlere uygula.

---

## 6. ESKİ KODU KÖRLEME KOPYALAMA

Eski minify edilmiş JS bundle'ını yeni çalışan sisteme doğrudan yapıştırma.

Eski bundle eski uygulama mantığı içeriyor.

Yapman gereken:

1. Eski görünümü analiz et.
2. Mevcut V2'nin çalışan frontend bileşenlerini o görünümle yeniden tasarla.
3. Gerekiyorsa eski CSS'ten yalnızca güvenli görsel kuralları çıkar.

Şunlar yeni sisteme taşınmayacak:

- eski auth
- eski fetch mantığı
- eski localStorage auth
- eski API URL'leri
- eski kullanıcı mantığı
- eski backend varsayımları

---

## 7. MEVCUT TÜM V2 ÖZELLİKLERİ KORUNACAK

Eski temada olmayan fakat V2'de çalışan yeni özellikleri silme.

Örneğin:

- yeni gizlilik seçenekleri
- güvenlik özellikleri
- hesap kurtarma
- mesaj özellikleri
- bildirimler
- hikâyeler
- grup fonksiyonları
- sayfa fonksiyonları
- takip
- öneriler
- reaksiyonlar
- gelişmiş profil fonksiyonları
- KVKK/güvenlik ekranları
- mevcut sosyal capability'ler

Eski temada görünmüyorsa bile bunları yeni temanın görsel diliyle tasarla.

**ESKİ TEMA GÖRÜNÜMÜ + YENİ V2'NİN TÜM ÇALIŞAN ÖZELLİKLERİ = SON ÜRÜN**

---

## 8. PROFİL VE GÖNDERİLER

Eski tema yedeğindeki uygun ve güvenli:

- profil resimleri
- kapak resimleri
- gönderi resimleri
- hikâye görselleri
- video/media örnekleri
- kullanıcı görselleri

incelenebilir.

Uygun olanlar mevcut V2 test kullanıcılarına **gerçek test verisi** olarak bağlanabilir.

Ancak:

- mevcut kullanıcıları silme
- kullanıcı şifrelerini değiştirme
- kullanıcı adlarını değiştirme
- auth tablolarını bozma
- mevcut gönderileri silme
- mevcut veriyi sıfırlama

Sadece gerçekçi test dünyasını zenginleştirmek amacıyla:

- avatar
- kapak resmi
- normal gönderi
- medya gönderisi
- gerekiyorsa hikâye

eklenebilir.

Bunlar UI'da gerçek backend/DB üzerinden görüntülensin.

Frontend'e sahte statik JSON gömme.

DB'ye eklenecek her kayıt mevcut V2 veri modeli/API mantığıyla uyumlu olsun.

Aynı içeriği gereksiz çoğaltma.

---

## 9. RESİM YÜKLEME VE MEDYA ALANLARI

Yeni sistemdeki gerçek resim/video yükleme fonksiyonları çalışmaya devam etsin.

Yalnızca görsel arayüzünü eski temaya uyarla.

Örneğin:

- profil fotoğrafı yükleme
- kapak yükleme
- gönderiye fotoğraf ekleme
- gönderiye medya ekleme
- hikâye yükleme
- görsel önizleme
- lightbox
- silme/değiştirme kontrolleri

eski temanın estetiğine geçirilsin.

Gerçek backend endpoint'leri aynen kullanılmaya devam etsin.

---

## 10. ANA AKIŞ

Ana sosyal akış eski önizlemedeki güçlü görünümü taşısın.

Özellikle:

- üst navigasyon
- sol alan
- orta feed
- sağ alan
- gönderi oluşturma
- hikâyeler
- gönderi kartları
- kullanıcı avatarları
- medya
- reaksiyonlar
- yorum alanları
- açılır menüler
- profil erişimi
- navigasyon

tasarım olarak eski temaya çok daha yakın olsun.

Ancak tüm butonlar ve fonksiyonlar yeni V2 backend'ine bağlı kalsın.

---

## 11. PROFİL SAYFASI

Profil sayfasını eski önizlemedeki başarılı tasarım karakterine getir:

- geniş kapak
- profil resmi
- isim
- kullanıcı bilgileri
- takip/arkadaş alanları
- sekmeler
- içerik
- medya
- gönderiler
- sağ/sol bilgi alanları

Mevcut V2'nin ekstra profil/gizlilik/güvenlik özelliklerini koru ve aynı tasarım dilinde göster.

---

## 12. DİĞER MEVCUT KULLANICI SAYFALARI

Mevcut V2 içinde gerçekten var olan tüm kullanıcı sayfalarını tek tek tara.

Her birini eski önizleme temasının tasarım sistemiyle uyumlu hale getir.

Bir sayfanın görünümü eski temada doğrudan yoksa; eski temanın:

- renk
- spacing
- kart
- header
- sidebar
- form
- tipografi

kurallarından türet.

**Generic veya bomboş panel yapma.**

---

## 13. MOBİL / TABLET / DESKTOP

Sadece desktop'a bakıp bitirme.

Ayrı ayrı doğrula:

- mobil
- tablet
- desktop

Mobilde şu sorunlar kalmayacak:

- içerik taşması
- yatay scroll
- üst üste binme
- kırık modal
- görünmeyen buton
- kesilen metin

Tema tamamen responsive olacak.

---

## 14. ÖNCE YEDEK

Herhangi bir frontend dosyasını değiştirmeden önce yalnızca güvenlik amacıyla mevcut kullanıcı frontend'inin tarih-saatli yedeğini al.

DB'ye eski görseller/test gönderileri eklenecekse önce mevcut SQLite DB'nin güvenli, tutarlı yedeğini al.

Ancak bu yedekleme dışında backend mimarisini değiştirme.

---

## 15. YASAKLAR

Kesinlikle yapma:

- DB şeması değiştirme
- migration yazma
- auth sistemi değiştirme
- şifre değiştirme
- erişim anahtarı değiştirme
- kullanıcı silme
- mevcut gönderi silme
- mevcut API sözleşmelerini gereksiz değiştirme
- anabeyin-core mimarisini yeniden yazma
- nginx yapısını değiştirme
- SSL'ye dokunma
- SSH'ye dokunma
- `/yonetim/` temasını değiştirme
- `/ajan/` temasını değiştirme
- recovery/keeper/watchdog değiştirme
- organizasyon sistemini değiştirme
- AI yönetim sistemini değiştirme
- çalışan capability'leri kaldırma
- eski backend'i yeniden kurma

---

## 16. GELİŞTİRME ŞEKLİ

Bu işi kapsamlı bir frontend dönüşümü olarak ele al.

Gerekiyorsa mevcut frontend dosyalarını/bileşenlerini kendin analiz et.

Tek bir dev CSS dosyasıyla üstünü boyayıp "tamam" deme.

Gerçek bileşenleri doğru şekilde düzenle.

Teknik borç bırakma.

Tema tutarlı olsun.

Bir ekranda eski tema, diğerinde yeni basit tema kalmasın.

Kullanıcı uygulamasının tamamında tek görsel sistem olsun.

---

## 17. TEST

Dönüşüm sonunda mutlaka:

1. `/uygulama/` HTTP 200
2. mevcut test kullanıcısı ile giriş
3. ana feed
4. profil
5. gönderi oluşturma
6. fotoğraf yükleme
7. yorum
8. reaksiyon
9. mesaj
10. bildirim
11. hikâye
12. grup
13. sayfa
14. takip/öneri
15. ayarlar/gizlilik/güvenlik
16. mobil
17. tablet
18. desktop

testlerini yap.

Ayrıca mevcut regresyon testlerini çalıştır.

Tema değişikliği nedeniyle backend davranışı bozulmuşsa frontend entegrasyonunu düzelt; çözüm backend'i yeniden tasarlamak olmasın.

---

## 18. BAĞIMSIZ GÖRSEL DENETİM

İş bitti zannettiğinde hemen bitmiş sayma.

Eski önizleme ile yeni `/uygulama/` görünümünü karşılaştır.

Kontrol et:

- eski temanın karakteri gerçekten taşındı mı?
- ana sayfa hâlâ eski basit V2 teması gibi mi?
- kartlar tutarlı mı?
- profil tutarlı mı?
- navigasyon tutarlı mı?
- responsive düzgün mü?
- eski temadaki kalite hissi yakalandı mı?
- yeni V2 özellikleri temaya düzgün yerleştirildi mi?
- hiçbir mevcut özellik kayboldu mu?

Eksik varsa düzelt.

---

## 19. SONUÇ KRİTERİ

Görev ancak şu durumda tamamdır:

- mevcut V2 backend tamamen korunmuş
- mevcut DB sistemi korunmuş
- auth korunmuş
- bütün yeni sosyal özellikler korunmuş
- kullanıcı tarafındaki eski basit tema kaldırılmış
- eski önizlemedeki beğenilen tasarım karakteri kullanıcı uygulamasına geçirilmiş
- mevcut tüm kullanıcı sayfaları aynı tasarım diliyle uyumlu
- eski temanın uygun görselleri mevcut test kullanıcılarında gerçek backend verisi olarak görünür
- medya yükleme çalışıyor
- mobil/tablet/desktop düzgün
- mevcut testler yeşil
- `/yonetim/` değişmemiş
- `/ajan/` değişmemiş
- backend mimarisi değişmemiş
- sistem çalışır durumda

---

## 20. ÇALIŞMA TARZI

**Hiçbir şey sorma.**

İşi kendin:

- incele
- planla
- gerekiyorsa uygun sayıda frontend/tasarım/test alt ajanı oluştur
- aynı işi tekrarlatma
- yap
- test et
- eksikleri bul
- düzelt
- tekrar test et
- tamamlanana kadar devam et

Ana prensip:

**ESKİ ANABEYİN'İN BEĞENİLEN TEMASI  
+  
BUGÜNKÜ ANABEYİN V2'NİN ÇALIŞAN BACKEND/DB/ÖZELLİKLERİ  
=  
YENİ KULLANICI ARAYÜZÜ**

**YÖNETİM VE AJAN TARAFINA DOKUNMA.**

**ANA HEDEF TAMAMLANANA KADAR DEVAM ET.**
