ANA GÖREV — ANABEYİN SOSYAL KULLANICI SİSTEMİNDE EKSİK KALAN GERÇEK SOSYAL MEDYA DAVRANIŞLARINI TAMAMLA, ÇALIŞMAYANLARI DÜZELT, GERÇEK VERİ AKIŞINI TEST ET VE TESLİM ET.

BU YENİ VE BAĞIMSIZ BİR GÖREVDİR.

ÖNCEKİ TEMA DÖNÜŞÜMÜ TAMAMLANMIŞTIR.
TEMA ÇALIŞMASINI YENİDEN BAŞLATMA.
ESKİ GOAL'U RESUME ETME.
ESKİ İŞİ TEKRAR YAPMA.

ANA ÇALIŞMA DİZİNİ:
/var/www/anabeyin/

MEVCUT CANLI SOSYAL UYGULAMA:
https://anabeyin.com/uygulama/

MEVCUT KULLANICI FRONTEND:
/var/www/anabeyin/sosyal-ui/

BU GÖREVİN KONUSU:
ŞU ANDA ÇALIŞAN SOSYAL MEDYA KULLANICI SİSTEMİNDE GÖZLE GÖRÜLEN VE GERÇEKTEN ÇALIŞMASI GEREKEN AŞAĞIDAKİ EKSİKLİKLERİ TAMAMLAMAKTIR.

BU GÖREVİN KONUSU DEĞİLDİR:
- yönetim sistemini yeniden yapmak
- ajan sistemini yeniden yapmak
- Patron AI geliştirmek
- organizasyon mimarisini değiştirmek
- bütün projeyi refactor etmek
- yeni bir sosyal medya sistemi sıfırdan kurmak
- gereksiz güvenlik/audit projeleri başlatmak
- ilgisiz özellikler geliştirmek.

MEVCUT ÇALIŞAN SİSTEMİ KORU.
VAR OLAN İŞLEVİ YENİDEN YAZMA.
ÖNCE İNCELE.
ÇALIŞIYORSA KORU.
EKSİKSE TAMAMLA.
BOZUKSA EN KÜÇÜK DOĞRU DEĞİŞİKLİKLE DÜZELT.

==================================================
1. ÇALIŞMAYA BAŞLAMADAN ÖNCE
==================================================

İlk değişiklikten önce:

1. /var/www/anabeyin/sosyal-ui/ için tarih-saatli güvenli yedek al.
2. Sosyal verilerin tutulduğu mevcut DB için tarih-saatli güvenli yedek al.
3. Mevcut sosyal frontend/API/veri modelini incele.
4. Hangi özellik zaten var, hangisi yarım, hangisi sadece görsel fakat işlevsiz, hangisi gerçekten eksik belirle.
5. Gereksiz yeni sistem kurma.

DB şemasını sırf kolayına geldiği için değiştirme.

Mevcut veri modeli yeterliyse mevcut tablo/alan/API'leri kullan.

Gerçekten zorunlu bir veri alanı eksikse:
- önce mevcut sistemle çözülemeyeceğini kanıtla,
- yedek al,
- minimum ve geri döndürülebilir migration kullan,
- başka tablo veya sistemi etkileme.

==================================================
2. SOL PANELDEKİ MENÜ YAZILARI GÖRÜNMÜYOR
==================================================

Ana sayfanın sol tarafında kullanıcı alanı bulunuyor.

Örneğin:
Ahmet Yılmaz

ve altında sosyal menü kategorileri var.

Şu anda bazı menülerde yalnızca ikon/logo görünüyor fakat ikonun sağındaki menü adı görünmüyor.

BUNU DÜZELT.

Her menü satırında:

[İKON] [MENÜ ADI]

net olarak görünmeli.

Örneğin gerçekten var olan bölümlerde:
- Akış
- Profilim
- Arkadaşlar
- Gruplar
- Sayfalar
- Reels
- Kaydedilenler
- Keşfet
- Ayarlar
ve mevcut diğer kullanıcı menüleri.

Kontrol et:
- text DOM'da gerçekten var mı?
- CSS tarafından display:none/width/overflow ile gizleniyor mu?
- font rengi background ile aynı mı?
- responsive breakpoint yanlış mı?
- ikon alanı bütün genişliği mi kaplıyor?

Sadece desktop değil:
- desktop
- tablet
- mobil

kontrol et.

Menü adları okunabilir olacak.

Mevcut route bağlantıları korunacak.

==================================================
3. SAĞ PANEL — ÖNERİLEN ARKADAŞLAR
==================================================

Ana sayfanın sağ tarafındaki önerilen arkadaşlar panelini gerçek çalışır hale getir.

Şu anda:
- avatar görülebiliyor,
- "4 ortak arkadaş" gibi bilgi görünüyor,
- "Arkadaş Ekle" butonu görünüyor,
fakat bazı kullanıcıların ADI görünmüyor.

HER ÖNERİDE ŞUNLAR GÖRÜNECEK:

- profil resmi
- kullanıcının görünen adı
- uygun ise kullanıcı adı
- ortak arkadaş sayısı veya mevcut öneri ikincil bilgisi
- Arkadaş Ekle butonu

KULLANICI ADINA VEYA PROFİL RESMİNE TIKLANINCA:
ilgili gerçek kullanıcı profil sayfasına gidecek.

"Arkadaş Ekle" tıklanınca mevcut gerçek arkadaşlık sistemi kullanılacak.

Butona basıldıktan sonra state doğru değişmeli:
- istek gönderildi
- bekliyor
- arkadaş
gibi mevcut sistemde karşılığı olan durum doğru gösterilmeli.

Sayfa yenilendiğinde durum geri eskiye dönmemeli.

==================================================
4. ÖNERİLEN ARKADAŞLAR — SAYFALAR — GRUPLAR
==================================================

Sağ panelde üç ayrı öneri bölümü olacak:

1. ÖNERİLEN ARKADAŞLAR
2. ÖNERİLEN SAYFALAR
3. ÖNERİLEN GRUPLAR

ANA PANELDE HER BİRİ MAKSİMUM 5 KAYIT GÖSTERECEK.

ARKADAŞ ÖNERİSİ:
- avatar
- ad
- ikincil bilgi
- arkadaş ekle
- profile link

SAYFA ÖNERİSİ:
- sayfa profil/logo görseli
- sayfa adı
- uygun mevcut bilgi
- takip/beğen gibi mevcut gerçek aksiyon
- sayfanın kendisine link

GRUP ÖNERİSİ:
- grup görseli
- grup adı
- uygun mevcut üye/ortak arkadaş bilgisi
- katıl gibi mevcut gerçek aksiyon
- grubun kendisine link

HER BÖLÜMÜN ALTINDA:

DAHA FAZLA ÖNERİ

bağlantısı olacak.

BUNA TIKLANINCA:

ilgili öneri türüne özel geniş bir liste açılacak.

İlk geniş yüklemede EN AZ 30 gerçek öneri getir.

30 sabit hardcode kayıt oluşturma.

Mevcut gerçek kullanıcı/sayfa/grup verilerinden pagination ile getir.

Liste aşağı doğru kaydırıldıkça:
- sonraki sayfa otomatik yüklenebilir
veya
- "Daha Fazla" ile devam edebilir.

Ama kullanıcı 30 kayıttan sonra sona gelmiş gibi kalmamalı.

GERÇEK PAGINATION / INFINITE SCROLL DAVRANIŞI OLSUN.

Aynı kayıtlar sürekli tekrar etmesin.

Kendi profilini kendine önerme.

Zaten arkadaş olunan kullanıcıyı "Arkadaş Ekle" olarak göstermeme.

Zaten katılınmış grup veya takip edilen sayfa için mevcut durum doğru gösterilmeli.

==================================================
5. ÖNERİLERİN AKIŞ İÇİNDE DE GÖRÜNMESİ
==================================================

Facebook benzeri doğal akış davranışı için:

Ana feed uzun süre aşağı kaydırıldığında yalnız postlardan oluşmak zorunda değil.

Aralıklı olarak:
- Tanıyor Olabileceğin Kişiler
- Önerilen Sayfalar
- Önerilen Gruplar

gibi küçük öneri modülleri akışın arasında gösterilebilir.

BUNU ABARTMA.

Her birkaç postta bir öneri çıkarıp feed'i reklam panosuna çevirme.

Makul aralıklarla göster.

Aynı kullanıcıya sürekli aynı önerileri gösterme.

Tıklamalar gerçek profile/sayfaya/gruba gitmeli.

==================================================
6. FOTOĞRAFA TIKLAYINCA GERÇEK FOTOĞRAF GÖRÜNTÜLEYİCİ
==================================================

Şu anda profil resmi veya gönderi fotoğrafı gösteriliyor fakat resme tıklandığında sosyal medya seviyesinde bir medya görüntüleyici açılmıyor.

BUNU TAMAMLA.

Bir fotoğrafa tıklandığında Facebook/Instagram benzeri DAVRANIŞTA fakat AnaBeyin'e özgün tasarımlı bir LIGHTBOX / FOTOĞRAF GÖRÜNTÜLEYİCİ aç.

GÖRÜNÜM:
- ekranın büyük bölümünü kaplayan koyu/siyah overlay
- ortada yüksek kaliteli fotoğraf
- kapatma butonu
- önceki fotoğraf
- sonraki fotoğraf
- gerektiğinde klavye sağ/sol
- mobilde swipe
- uygun metadata/başlık
- fotoğraf sahibi
- uygun ise beğen/yorum gibi mevcut sosyal aksiyon alanı.

Kullanıcı bir profile ait fotoğrafa tıklarsa:

sağa/sola ilerledikçe ilgili kullanıcının o kategori içindeki diğer fotoğrafları gezilebilsin.

Lightbox açıldıktan sonra sayfayı komple yeniden yükleme.

URL/state mümkünse kullanıcı geri tuşuyla düzgün kapanacak şekilde yönetilsin.

==================================================
7. PROFİLDE FOTOĞRAF KATEGORİLERİ / ALBÜMLER
==================================================

Kullanıcı profilinde medya kategorize edilebilmeli.

Mevcut sistemle uyumlu şekilde en az:

FOTOĞRAFLAR
- Tüm Fotoğraflar
- Yüklenen Fotoğraflar
- Profil Fotoğrafları
- Kapak Fotoğrafları
- Albümler

destekle.

Eğer etiketlenen fotoğraflar için mevcut altyapı varsa:
- Etiketlenenler

de eklenebilir.

Sırf kategori göstermek için fotoğrafın ayrı kopyalarını üretme.

Aynı medya kaydını mevcut metadata ile kategorize et.

Profil fotoğrafı değişiklik geçmişi mevcutsa Profil Fotoğrafları altında göster.

Kapak geçmişi mevcutsa Kapak Fotoğrafları altında göster.

Albümler:
- kullanıcı albüm oluşturabilsin
- mevcut fotoğrafları albüme ekleyebilsin
- albüm adını görebilsin
- albüm açılınca lightbox ile gezebilsin.

Gerçek veritabanı persistence olmalı.

Sayfa yenilendiğinde albüm/fotoğraf ilişkileri kaybolmamalı.

==================================================
8. PROFİLDE VIDEO KATEGORİSİ
==================================================

Profilde FOTOĞRAFLAR gibi VIDEOLAR bölümü de bulunmalı.

Kullanıcının gerçekten yüklediği:
- normal videolar
- Reels
- varsa canlı yayın tekrarları

uygun kategorilerde görülebilmeli.

Video kaydı yalnız feed'de görünüp profilden kaybolmamalı.

Video hangi kullanıcıya aitse o kullanıcının medya/profile kayıtlarında da bulunmalı.

==================================================
9. REELS — ÖZEL REELS SAYFASI
==================================================

Reels bölümü gerçek kısa video deneyimi olacak.

REELS SAYFASINDA:
kullanıcı bir Reel açtığında video tam ekran veya neredeyse tam viewport deneyimine geçsin.

Instagram Reels / Facebook Reels mantığına benzer DAVRANIŞ:
- dikey video
- ekranın büyük bölümünü video kaplasın
- kullanıcı adı/başlık
- beğen
- yorum
- paylaş
- ses
- mevcut uygun aksiyonlar
- sağ/alt kontrol alanları
- otomatik oynatma
- görünmeyen video pause
- aktif video play
- mute/unmute
- gerekirse progress.

YUKARI/AŞAĞI:
mouse wheel,
touch swipe,
uygun klavye hareketi

ile sonraki/önceki Reel'e geçilebilsin.

Bir Reel bittiğinde kullanıcı sistemden çıkmasın.

Keşfet/recommendation algoritmasının mevcut mantığı kullanılabiliyorsa diğer uygun Reel'ler gelsin.

Aynı üç Reel sonsuz tekrar etmesin.

Pagination olacak.

==================================================
10. ANA AKIŞTA REELS
==================================================

Ana feed yalnız metin/fotoğraf postlarından oluşmayacak.

Bir kullanıcının Reel'i akışta gösterilecekse:

FEED İÇİN:
Reel normal feed genişliği içinde uygun büyük video kartı olarak görünsün.

Feed'i otomatik olarak tam ekran ele geçirmesin.

Feed içindeki Reel:
- video önizleme/oynatma
- kullanıcı
- açıklama
- temel aksiyonlar
gösterebilir.

KULLANICI REEL'E TIKLARSA:
tam ekran Reels viewer açılsın.

Bundan sonra yukarı/aşağı ilerledikçe diğer Reels'ler gelsin.

Viewer kapatıldığında kullanıcı feed'deki kaldığı yere dönsün.

==================================================
11. NORMAL VIDEO PAYLAŞIMI
==================================================

Normal sosyal medya postlarında VIDEO gerçek bir içerik tipi olacak.

Gönderi composer'ında:
- Metin
- Fotoğraf
- Video
ve mevcut diğer uygun paylaşım türleri bulunmalı.

Video yükleme gerçekten çalışmalı.

Kullanıcı video seçsin.
Upload progress görsün.
Yükleme tamamlansın.
Post oluşturulsun.

Video:
- kullanıcının profilinde
- feed'de
- gerekiyorsa ilgili grup/sayfa feed'inde
gerçekten görünmeli.

==================================================
12. NORMAL VIDEO PLAYER
==================================================

NORMAL VIDEOLAR için AnaBeyin'e özgün fakat modern video player yap.

YouTube davranışından yararlan fakat tasarımını birebir kopyalama.

En az:
- play/pause
- progress bar
- kullanıcı istediği zamana sürükleyebilsin
- geçen süre
- toplam süre
- ses
- mute
- fullscreen
- uygun mobil kontroller
- loading/buffering göstergesi
- poster/thumbnail

olsun.

Mümkün ve mevcut altyapıyla uyumluysa:
- playback speed

eklenebilir.

Büyük yeni YouTube benzeri ayrı video platformunu ŞİMDİ KURMA.

İleride ayrı video platformu geliştirilecektir.

Şu an yalnız mevcut sosyal medya sistemi içindeki normal video deneyimini düzgün yap.

==================================================
13. HİKÂYELER — GÖRÜLDÜKTEN SONRA KAYBOLMASIN
==================================================

Şu anda bir arkadaşın hikâyesi görülmeden önce renkli halka ile görünüyor.

Kullanıcı hikâyeyi izledikten sonra hikâye ana sayfadan tamamen kayboluyor.

BU YANLIŞ.

DÜZELT.

DAVRANIŞ:

GÖRÜLMEMİŞ AKTİF HİKÂYE:
- renkli/canlı halka.

GÖRÜLMÜŞ FAKAT HÂLÂ AKTİF HİKÂYE:
- hikâye listesinde kalacak
- avatar kalacak
- halka gri/sönük olacak.

Hikâye yalnız:
- gerçek süresi bittiğinde
- kullanıcı sildiğinde
- sistemde geçerli başka sona erme nedeni olduğunda

kaybolsun.

Sırf "seen=true" oldu diye listeden silinmesin.

Story seen state:
kullanıcı bazında persistence göstermeli.

Sayfa yenilendiğinde yeniden renkli olmamalı.

==================================================
14. HİKÂYE GÖRÜNTÜLEYİCİ
==================================================

Bir arkadaşın birden fazla story'si varsa:
- sırayla ilerlesin
- progress çizgileri olsun
- önceki/sonraki
- pause
- mobil tap/swipe
- kullanıcı adı
- avatar
- zaman
- kapat
gibi temel hikâye viewer davranışları düzgün çalışsın.

Bir kullanıcının story'si bittiğinde uygun ise sonraki arkadaşın story'sine geçebilsin.

==================================================
15. CANLI YAYIN / CANLI HİKÂYE
==================================================

Sosyal composer/hikâye alanında CANLI seçeneği eksik.

CANLI YAYIN GİRİŞ NOKTASI ekle.

Ama gereksiz dev ayrı streaming projesi geliştirme.

MEVCUT SİSTEMDE canlı yayın altyapısı zaten varsa onu kullan ve UI'ını tamamla.

Yoksa bu sosyal sistem içerisinde minimum gerçek çalışır canlı yayın akışını oluştur:

Yayıncı:
- canlı yayın başlat
- kamera/mikrofon izni
- yayın başlığı
- yayın başlat
- canlı olduğunu gör
- yayını bitir.

İzleyici:
- aktif canlı yayın işaretini gör
- avatar/story çevresinde LIVE/CANLI rozeti gör
- yayına tıklayabilsin
- canlı videoyu izleyebilsin
- mevcut yorum altyapısıyla canlı yorum yapılabiliyorsa kullan.

Canlı yayın bitince aktif story halkasında canlı görünmemeli.

Eğer tekrar kaydı özelliği mevcut veri yapısıyla güvenli şekilde destekleniyorsa kullanıcının video alanına kayıt eklenebilir.

Bu özellik için bütün site mimarisini değiştirme.

==================================================
16. FOTOĞRAF / VIDEO / REELS / STORY GERÇEK PERSISTENCE
==================================================

BU GÖREVİN EN KRİTİK KISIMLARINDAN BİRİ:

Görünürde çalışan buton yeterli değildir.

GERÇEKTEN VERİTABANINA / MEVCUT KALICI VERİ KATMANINA KAYDOLMASI GEREKİYOR.

Aşağıdakileri TEK TEK gerçek test et:

METİN POSTU:
- oluştur
- API success
- DB/persistence doğrula
- feed'de gör
- kullanıcının profilinde gör
- hard refresh sonrası hâlâ var mı kontrol et.

FOTOĞRAF POSTU:
- yükle
- media file gerçek kaydoldu mu
- DB media/post ilişkisi oluştu mu
- feed
- profil
- lightbox
- hard refresh
kontrol et.

NORMAL VIDEO:
- yükle
- post oluştur
- gerçek medya kaydı
- feed
- profil videoları
- player
- refresh
kontrol et.

REEL:
- oluştur/yükle
- Reel kaydı oluştu mu
- kullanıcının profil/Reels bölümünde var mı
- Reels feed'e düşüyor mu
- uygun ana feed'de görünüyor mu
- refresh sonrası kalıyor mu
kontrol et.

STORY:
- story oluştur
- story persistence
- arkadaşın ana sayfasında görünme
- seen state
- seen sonrası gri halka
- süre bitmeden kaybolmama
kontrol et.

CANLI:
- mevcut/live implementasyonu ölçüsünde gerçek start/end durumunu test et.

==================================================
17. ARKADAŞIN PAYLAŞIMINI ARKADAŞ GERÇEKTEN GÖRÜYOR MU?
==================================================

Test için bütün kullanıcıları kullanma.

3–5 mevcut test/demo hesabı yeterli.

Örneğin:

KULLANICI A
KULLANICI B
KULLANICI C

gerçek arkadaş ilişkisi kur.

A bir metin postu oluşturduğunda:

B arkadaşsa:
B'nin ilgili feed'inde görünmeli.

C arkadaş değilse:
post privacy/visibility kuralına göre görünmeli veya görünmemeli.

A fotoğraf koyduğunda da aynı.

A video koyduğunda da aynı.

A Reel koyduğunda mevcut feed/recommendation kurallarına göre görünmeli.

A story koyduğunda arkadaşının story şeridinde görünmeli.

Bu testi yalnız "DB'de satır var" diyerek geçme.

GERÇEK API + GERÇEK UI ile kontrol et.

==================================================
18. PRIVACY / VISIBILITY MANTIĞI
==================================================

Mevcut sistemde gönderi görünürlüğü seçenekleri varsa bunların çalıştığını doğrula.

Örneğin mevcut model destekliyorsa:
- Herkese Açık
- Arkadaşlar
- Sadece Ben
- grup/sayfa bağlamı

gibi scope doğru uygulanmalı.

Arkadaşlara özel post yabancı kullanıcı feed'ine düşmemeli.

Sadece Ben postu başka kullanıcı tarafından görülmemeli.

Bu görevde yeni dev gizlilik sistemi yazma.

Mevcut sistemi test et ve bozuksa düzelt.

==================================================
19. BEĞEN GERÇEKTEN ÇALIŞIYOR MU?
==================================================

KULLANICI A'nın postunu KULLANICI B beğensin.

Kontrol:

- UI state değişti mi?
- beğeni sayısı değişti mi?
- DB/persistence oluştu mu?
- refresh sonrası hâlâ beğenilmiş mi?
- aynı kullanıcı tekrar beğenirse duplicate kayıt oluşuyor mu?
- unlike varsa düzgün çalışıyor mu?
- post profile içinde açıldığında aynı state görünüyor mu?
- feed'de aynı state görünüyor mu?

ANA POST ACTION UI:
BEĞEN
YORUM YAP
PAYLAŞ

olacak.

Emoji reaction picker oluşturma.

==================================================
20. YORUMLAR GERÇEKTEN ÇALIŞIYOR MU?
==================================================

Kullanıcı B:
Kullanıcı A'nın postuna yorum yazsın.

Kontrol:

- yorum DB/persistence kaydoldu mu?
- feed postunda görünüyor mu?
- post kullanıcının profilinde açıldığında aynı yorum görünüyor mu?
- sayfa yenilendiğinde yorum duruyor mu?
- yorum sayacı doğru mu?
- yorum kullanıcı/avatar/profile link doğru mu?

Eğer mevcut sistem reply/yanıt destekliyorsa:
bir yoruma cevap ver ve persistence test et.

Eğer mevcut sistem yorum silme/düzenleme destekliyorsa:
yalnız sahibi/yetkilisi yapabiliyor mu kontrol et.

Yeni dev yorum özelliği icat etme; mevcut sistemi sağlamlaştır.

==================================================
21. PAYLAŞ GERÇEKTEN ÇALIŞIYOR MU?
==================================================

Bir post "Paylaş" ile paylaşıldığında:

mevcut sistem hangi paylaşım modelini destekliyorsa onu kullan.

Kontrol:
- paylaşım persistence
- paylaşan kullanıcının profil/feed ilişkisi
- orijinal post referansı
- sayaç
- refresh sonrası kalıcılık.

Aynı postun DB'de anlamsız duplicate tam kopyalarını oluşturma.

Mevcut paylaşım modelini kullan.

==================================================
22. SAYFALAR GERÇEKTEN ÇALIŞIYOR MU?
==================================================

Mevcut Sayfalar özelliği yalnız boş UI olmamalı.

En az 1–2 mevcut test sayfasıyla kontrol et:

- sayfa açılıyor mu
- sayfanın adı/avatar/kapak bilgileri doğru mu
- sayfa post paylaşabiliyor mu
- post sayfa feed'inde görünüyor mu
- uygun genel feed'de görünüyor mu
- yorum/beğen/paylaş çalışıyor mu
- takip/beğen ilişkisi varsa persistence çalışıyor mu
- sayfaya linkler doğru mu.

İlgisiz yeni yönetim sistemi kurma.

==================================================
23. GRUPLAR GERÇEKTEN ÇALIŞIYOR MU?
==================================================

En az 1–2 test grubuyla kontrol et:

- grup açılıyor mu
- üyelik
- katıl/ayrıl
- üye state refresh sonrası korunuyor mu
- grup postu oluşturuluyor mu
- grup feed'inde görünüyor mu
- yetkili visibility doğru mu
- beğen
- yorum
- paylaş
çalışıyor mu.

Grup postunu yanlışlıkla başka kullanıcının normal kişisel postu gibi kaydetme.

Group context korunmalı.

==================================================
24. PROFİLLER GERÇEKTEN DB'DE Mİ?
==================================================

Mevcut test/demo kullanıcıların frontend hardcode listesi olmadığını doğrula.

Profil için kontrol:

- kullanıcı gerçek users/kullanıcı veri modelinde var mı
- username/id gerçek mi
- profil URL doğru kullanıcıyı açıyor mu
- avatar gerçek media reference mı
- kapak gerçek media reference mı
- bio/bilgiler persistence
- kişinin postları doğru kullanıcıya ait mi
- arkadaş ilişkileri gerçek mi
- fotoğraflar doğru kişiye ait mi
- videolar doğru kişiye ait mi
- Reels doğru kişiye ait mi.

Frontend'de isim/avatar listesi hardcode edilerek gerçek profil taklidi yapılmışsa bunu kaldır ve gerçek veriye bağla.

==================================================
25. BİLDİRİMLER
==================================================

Mevcut notification sistemi varsa şu olaylarda gerçek bildirim üretimini kontrol et:

- arkadaşlık isteği
- arkadaşlık kabulü
- post beğenisi
- post yorumu
- yoruma cevap
- post paylaşımı
- grup/sayfa ile ilgili mevcut notification olayları.

Notification:
- doğru kullanıcıya ait olmalı
- yanlış kullanıcıya gitmemeli
- ilgili içeriğe tıklayınca doğru profile/post/group/page açılmalı
- read/unread state refresh sonrası korunmalı.

Yeni dev notification altyapısı kurma; mevcut olanı sağlamlaştır.

==================================================
26. SAYAÇLAR VE STATE SENKRONİZASYONU
==================================================

Aynı verinin farklı ekranda farklı görünmesini engelle.

Örneğin bir post:

Ana feed'de 3 yorum gösteriyorsa,
profilde aynı post 0 yorum göstermemeli.

Kontrol et:

- like count
- comment count
- share count
- friend state
- page follow state
- group membership state
- story seen state
- notification count.

Ana feed,
profil,
lightbox,
group,
page,
Reels viewer

aynı backend gerçeğini kullanmalı.

==================================================
27. HARD REFRESH TESTİ
==================================================

Bir özelliği test ederken yalnız anlık frontend state'e güvenme.

Her temel CRUD/interaction testinden sonra en az bir kez:

Ctrl+Shift+R / hard refresh

mantığında tekrar yükle.

Şunlar refresh sonrası kaybolmamalı:

- post
- comment
- like
- share
- friend request
- group membership
- page follow
- uploaded media
- album
- story seen state
- Reel.

==================================================
28. PAGINATION / INFINITE SCROLL
==================================================

Feed ve büyük listelerde bütün DB'yi tek request ile çekme.

Mevcut pagination mekanizması varsa kullan.

Yoksa mevcut API tasarımına uygun minimum pagination uygula.

Özellikle:
- ana feed
- comments
- recommendations
- photos
- videos
- Reels
- followers/friends
- groups/pages

listelerinde sayfa büyüdükçe sistem çökmemeli.

Infinite scroll:
aynı kayıtları duplicate yüklememeli.

==================================================
29. MEDIA HATALARI
==================================================

Fotoğraf/video yüklemede şunları kontrol et:

- desteklenen dosya tipi
- hatalı dosya
- boyut limiti
- yarım upload
- upload failure
- kullanıcıya hata mesajı
- media post oluşturulmadan önce upload başarısı
- silinen postun orphan medya davranışı mevcut sistem standardına uygun mu.

Gereksiz disk temizleme operasyonu yapma.

Gerçek kullanıcı medyasını silme.

==================================================
30. LINK / ROUTING
==================================================

Kullanıcı adı,
avatar,
post sahibi,
arkadaş önerisi,
sayfa önerisi,
grup önerisi,
notification,
commenter

gibi tıklanabilir kullanıcı nesnelerinin tamamı doğru route'a gitmeli.

404 veya yanlış profile gitmemeli.

Browser geri tuşu mümkün olduğunca doğal çalışmalı.

Lightbox/Reels viewer kapandığında kullanıcı geldiği yere geri dönmeli.

==================================================
31. LOADING / EMPTY / ERROR STATE
==================================================

Gerçek sosyal medya deneyiminde yalnız success ekranı olmaz.

Temel kullanıcı alanlarında:

LOADING:
gereksiz boş beyaz alan yerine mevcut tema ile uyumlu loading state.

EMPTY:
hiç öneri yoksa veya hiç post yoksa düzgün boş-state metni.

ERROR:
API başarısızsa sessizce kaybolmak yerine kullanıcıya uygun hata.

Yeni tasarım dilini bozma.

==================================================
32. AJAN YAPISI — KONTROLLÜ
==================================================

ANA KIMI koordinatör olacak.

BU GÖREV İÇİN MAKSİMUM 6 UZMAN ALT AJAN KULLAN.

AJANLAR BAŞKA AJAN OLUŞTURMAYACAK.

SUBAGENT → SUBAGENT YASAK.

Yüzlerce ajan YASAK.

--------------------------------------------------
AJAN 1 — SOL/SAĞ PANEL VE NAVİGASYON
--------------------------------------------------

Görevi:
- sol menü text bug
- arkadaş önerileri
- sayfa önerileri
- grup önerileri
- daha fazla öneri
- pagination
- doğru profile/page/group linkleri
- feed içi öneri modülleri.

--------------------------------------------------
AJAN 2 — FOTOĞRAF / ALBÜM / PROFİL MEDYA
--------------------------------------------------

Görevi:
- photo lightbox
- next/previous
- photo albums
- profile photos
- cover photos
- uploaded photos
- profil video kategorileri
- media ownership/persistence.

--------------------------------------------------
AJAN 3 — VIDEO / REELS / STORY / LIVE
--------------------------------------------------

Görevi:
- normal video upload/player
- Reels fullscreen viewer
- feed Reels
- vertical navigation
- story seen/unseen ring
- story viewer
- live entry/viewer
- video/reel/profile media bağları.

--------------------------------------------------
AJAN 4 — SOSYAL VERİ / API / PERSISTENCE
--------------------------------------------------

Görevi:
- posts
- likes
- comments
- replies
- shares
- friendship
- page/group ilişkileri
- story persistence
- Reel persistence
- profile ownership
- notifications
- visibility
- DB/API/UI consistency.

BU AJAN gereksiz backend rewrite yapmayacak.
Sadece gerçek bozuk bağlantıları minimum değişiklikle düzeltecek.

--------------------------------------------------
AJAN 5 — E2E / GERÇEK KULLANICI AKIŞI QA
--------------------------------------------------

3–5 test/demo kullanıcı ile gerçek senaryoları uçtan uca test edecek.

UI'dan oluştur.
Başka kullanıcıyla gör.
Etkileşim yap.
Refresh yap.
DB/API kalıcılığı doğrula.

Kod değiştirmeyecek.
Bulgu raporlayacak.

--------------------------------------------------
AJAN 6 — DENETLEYİCİ / KAPSAM KORUYUCU
--------------------------------------------------

BU AJAN DİĞERLERİNİ DENETLEYECEK.

Şunları engelleyecek:

- gereksiz backend refactor
- yönetim sistemine müdahale
- ajan sistemine müdahale
- Patron AI değişikliği
- sistem mimarisi değişikliği
- gereksiz migration
- gereksiz yüzlerce test
- yeni dev özellik paketleri
- YouTube platformunu şimdi kurmak
- yüzlerce agent
- subagent zinciri
- gereksiz dokümantasyon üretimi
- gerçek kullanıcı verisine müdahale
- scope dışı çalışmalar.

Kapsam dışı işlem görürse:
DUR — KAPSAM DIŞI
diye ana Kimi'yi uyaracak.

Kod yazmayacak.

==================================================
33. PARALEL ÇALIŞMA KURALI
==================================================

Aynı dosyada iki ajan aynı anda WRITE yapmasın.

Örneğin sosyal-ui/app.js üzerinde iki ayrı ajan paralel edit yapmasın.

Ana Kimi write ownership koordine etsin.

Read-only analiz paralel yapılabilir.

Write değişiklikleri kontrollü birleştirilsin.

==================================================
34. TEST MATRİSİ
==================================================

Bütün kullanıcıları test etme.

3–5 test/demo kullanıcı,
1–2 test sayfası,
1–2 test grup

yeterli.

AMA ORTAK SİSTEMİN GERÇEKTEN ÇALIŞTIĞINI KANITLA.

Minimum gerçek test matrisi:

A → metin postu
B → postu görür
B → beğenir
B → yorum yapar
C → reply varsa cevaplar
B → paylaşır
refresh → hepsi korunur

A → fotoğraf postu
B → feed'de görür
fotoğrafa tıklar
lightbox açılır
next/prev çalışır
profil albümünde görünür

A → normal video
B → feed'de açar
progress/scrub/fullscreen test
profil Videos bölümünde görünür

A → Reel
Reels bölümünde görünür
fullscreen viewer açılır
sonraki Reel geçişi
feed'den Reel açılışı

A → Story
B story şeridinde görür
B izler
story kaybolmaz
ring gri olur
refresh sonrası gri kalır

Arkadaş önerisi:
isim + avatar + link + arkadaş ekle
refresh sonrası state korunur

Sayfa önerisi:
sayfa link + action

Grup önerisi:
grup link + membership

Sayfa postu:
sayfa feed persistence

Grup postu:
group context persistence.

==================================================
35. BAŞARI KRİTERİ — GÖRSEL "VAR" DEMEK YETERLİ DEĞİL
==================================================

Bir özellik ancak:

UI_VAR=EVET
API_CALISIYOR=EVET
PERSISTENCE=EVET
REFRESH_SONRASI_KORUNUYOR=EVET
DOGRU_KULLANICIYA_BAGLI=EVET
DIGER_ILGILI_EKRANLARDA_TUTARLI=EVET

ise tamamlandı kabul edilecek.

==================================================
36. FİNAL DENETİM
==================================================

İş sonunda DENETLEYİCİ ve QA birlikte kontrol etsin.

Şunların tamamını cevapla:

SOL_MENU_YAZILARI=
ARKADAS_ONERI_ISIMLERI=
ARKADAS_PROFILE_LINKLERI=
ARKADAS_EKLE_PERSISTENCE=

ONERILEN_ARKADASLAR_5_LIMIT=
ONERILEN_SAYFALAR_5_LIMIT=
ONERILEN_GRUPLAR_5_LIMIT=
DAHA_FAZLA_ONERI_30_PLUS=
ONERI_PAGINATION=

PHOTO_LIGHTBOX=
PHOTO_NEXT_PREVIOUS=
PHOTO_ALBUMLERI=
PROFIL_FOTOGRAFLARI=
KAPAK_FOTOGRAFLARI=
YUKLENEN_FOTOGRAFLAR=

PROFIL_VIDEO_KATEGORISI=
NORMAL_VIDEO_UPLOAD=
NORMAL_VIDEO_PLAYER=
VIDEO_PROGRESS_SCRUB=
VIDEO_FULLSCREEN=

REELS_FULLSCREEN_VIEWER=
REELS_VERTICAL_SCROLL=
REELS_PAGINATION=
FEED_REELS=
FEED_REEL_TO_FULLSCREEN=

STORY_UNSEEN_COLOR_RING=
STORY_SEEN_GRAY_RING=
STORY_SEEN_SONRASI_KAYBOLMUYOR=
STORY_VIEWER=
LIVE_ENTRY=
LIVE_START_STOP=
LIVE_VIEWER=

METIN_POST_PERSISTENCE=
FOTO_POST_PERSISTENCE=
VIDEO_POST_PERSISTENCE=
REEL_PERSISTENCE=
STORY_PERSISTENCE=

FRIEND_FEED_VISIBILITY=
PRIVACY_VISIBILITY=

LIKE_PERSISTENCE=
COMMENT_PERSISTENCE=
REPLY_PERSISTENCE=
SHARE_PERSISTENCE=

PROFILE_DATA_REAL=
PROFILE_POST_OWNERSHIP=
MEDIA_OWNERSHIP=

GROUP_MEMBERSHIP=
GROUP_POST=
PAGE_FOLLOW=
PAGE_POST=

NOTIFICATION_PERSISTENCE=
NOTIFICATION_DEEP_LINK=

COUNT_SYNC=
HARD_REFRESH_TEST=
PAGINATION_TEST=
ROUTING_TEST=
ERROR_STATE_TEST=

==================================================
37. KORUNACAK SİSTEMLER
==================================================

BU GÖREV SONUNDA RAPORLA:

YONETIM_SISTEMI_DEGISTI=
AJAN_SISTEMI_DEGISTI=
PATRON_AI_DEGISTI=
ORGANIZASYON_DEGISTI=
NGINX_DEGISTI=
SSL_DEGISTI=
SYSTEMD_DEGISTI=
AUTH_YENIDEN_YAZILDI=
GEREKSIZ_BACKEND_REFACTOR=
GEREKSIZ_DB_SCHEMA_DEGISIKLIGI=

HEDEFLENEN CEVAP:
HAYIR.

Sosyal özelliklerin gerçekten çalışması için ZORUNLU küçük API/backend/data düzeltmeleri yapılmışsa bunları ayrı ayrı ve neden gerekli olduklarıyla raporla.

==================================================
38. ÇALIŞMA SIRASI
==================================================

SIRAYI KORU:

1. Backup.
2. Mevcut sosyal sistem read-only incelemesi.
3. Eksik/bozuk özellik matrisi.
4. Sol menü text düzeltmesi.
5. Sağ öneriler.
6. Önerilen sayfalar.
7. Önerilen gruplar.
8. Daha fazla öneri/pagination.
9. Photo lightbox.
10. Profil fotoğraf/albüm.
11. Profil video kategorisi.
12. Normal video upload/player.
13. Reels viewer.
14. Feed Reels.
15. Story seen/unseen düzeltmesi.
16. Story viewer.
17. Live.
18. Post persistence.
19. Feed visibility.
20. Like/comment/share persistence.
21. Profile data consistency.
22. Groups.
23. Pages.
24. Notifications.
25. Counters/state consistency.
26. Hard refresh test.
27. Pagination.
28. Responsive check.
29. QA.
30. Denetleyici.
31. Eksiklerin final düzeltmesi.
32. Final yeniden test.
33. Son rapor.
34. DUR.

==================================================
39. SON EMİR
==================================================

BU GÖREVDE AMACIM:

"GÖRSEL OLARAK VARMIŞ GİBİ DURAN SOSYAL MEDYA"

DEĞİL.

GERÇEKTEN ÇALIŞAN SOSYAL MEDYA İSTİYORUM.

KULLANICI BİR ŞEY PAYLAŞTIĞINDA GERÇEKTEN KAYDOLACAK.

ARKADAŞI GERÇEKTEN GÖRECEK.

KULLANICININ PROFİLİNDE GERÇEKTEN GÖRÜNECEK.

FOTOĞRAF GERÇEK LIGHTBOX/ALBÜM SİSTEMİNDE AÇILACAK.

VIDEO GERÇEKTEN YÜKLENECEK VE OYNAYACAK.

REELS GERÇEKTEN REELS DENEYİMİYLE ÇALIŞACAK.

STORY İZLENDİ DİYE YOK OLMAYACAK; GRİ/SÖNÜK OLARAK KALACAK.

ARKADAŞ/SAYFA/GRUP ÖNERİLERİ GERÇEK VERİDEN GELECEK.

KULLANICI ADINA TIKLAYINCA GERÇEK PROFILE GİDİLECEK.

BEĞENİ GERÇEKTEN KAYDOLACAK.

YORUM GERÇEKTEN KAYDOLACAK.

PAYLAŞIM GERÇEKTEN KAYDOLACAK.

SAYAÇLAR BÜTÜN EKRANLARDA AYNI GERÇEĞİ GÖSTERECEK.

GRUPLAR VE SAYFALAR SADECE GÖRSEL KABUK OLMAYACAK; MEVCUT SİSTEMİN İZİN VERDİĞİ GERÇEK İŞLEVLER ÇALIŞACAK.

BUNLARI TEST ETMEDEN "TAMAMLANDI" DEME.

AMA KAPSAMI DAĞITMA.

YENİ YOUTUBE PLATFORMU KURMA.

BÜTÜN ANABEYİN'İ YENİDEN YAZMA.

YÖNETİM VE AJAN SİSTEMİYLE UĞRAŞMA.

BU TEK SOSYAL KULLANICI GÖREVİNİ BİTİR.

QA VE DENETLEYİCİ ONAYI OLMADAN COMPLETE VERME.

GERÇEKTEN BİTTİĞİNDE:

SOSYAL_KULLANICI_EKSIKLERI_TAMAMLANDI=YES
GERCEK_PERSISTENCE_TESTLERI=PASS
QA_FINAL=PASS
KAPSAM_DENETIMI=PASS
ANA_HEDEF_TAMAMLANDI=YES

yaz.

SONRA DUR.