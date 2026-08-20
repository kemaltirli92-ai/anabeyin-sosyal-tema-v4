# KIMI CODE DAYANIKLILIK + ANABEYIN TEMA V4 BASLATMA TALIMATI

Bu dosya Kimi Code tarafından **tamamı okunarak** uygulanacaktır. Amaç; önce uzun süreli Kimi Code çalışmasını durdurabilecek gerçek sebepleri araştırmak ve dayanıklılık/otomatik devam sistemini kurmak, ardından AnaBeyin Tema V4 ana RAW talimatını aynı session içinde tek bir Goal olarak başlatmak ve Goal gerçekten tamamlandığında otomatik resume davranışını kesin olarak durdurmaktır.

**Hiçbir şey sorma. Bu görevi sırasıyla ve tam otomatik yürüt.**

---

## ANA AMAÇ

1. ÖNCE Kimi Code'daki uzun süreli yüklemeyi/geliştirmeyi durdurabilecek TÜM gerçek sebepleri araştır.
2. SONRA bu sebeplere karşı VPS üzerinde kalıcı dayanıklılık/otomatik devam sistemini KODLA, KUR ve doğrula.
3. DAYANIKLILIK gerçekten hazır olmadan AnaBeyin Tema V4 geliştirmesine BAŞLAMA.
4. Dayanıklılık hazır olduktan sonra aşağıdaki RAW MD dosyasını indir, tamamını oku ve TEK BİR KALICI GOAL olarak başlat:
   https://raw.githubusercontent.com/kemaltirli92-ai/anabeyin-sosyal-tema-v4/refs/heads/main/ANABEYIN-SOSYAL-TEMA-V4-ANA-TALIMAT.md
5. Kullanıcının bilgisayarı, tarayıcısı veya Hostinger terminali kapalı olsa bile çalışma VPS üzerinde devam etsin.
6. Geçici bir engel ortadan kalkınca AYNI SESSION + AYNI GOAL kaldığı yerden devam etsin.
7. Goal gerçekten tamamlanınca KESİNLİKLE DUR. Bittiği halde /goal resume spam'i yapma.

==================================================
A — İLK İŞ: DURDURAN SEBEPLERİ ARAŞTIR VE LİSTELE
==================================================

Henüz Tema V4 dosyalarına dokunma.

Önce kurulu Kimi Code sürümünü tespit et:

kimi --version

Sonra kurulu sürümle uyumlu RESMİ Kimi Code dokümantasyonunu incele.

Özellikle:

- Goals lifecycle
- Sessions
- kimi command
- --session
- --continue
- --auto
- config.toml
- loop_control
- background
- subagent
- hooks
- SessionHeartbeat
- StopFailure
- Interrupt
- PreCompact/PostCompact
- permission mode
- provider/model errors
- quota/rate limits

konularını incele.

Bunun yanında Linux/VPS seviyesinde uzun çalışmayı durdurabilecek sebepleri de incele.

İLK ÇIKTIN terminalde şu başlık olsun:

=== KIMI CODE UZUN ÇALIŞMAYI DURDURABİLECEK SEBEPLER ===

Gerçekten mümkün olan bütün sebepleri numaralı olarak listele.

En az şu sınıfları kapsa:

- Goal complete
- Goal pause
- Goal cancel
- Goal replace
- Goal blocked
- turn interrupt
- model error
- provider error
- runtime error
- 401/authentication
- 403 quota/usage limit
- 429 rate limit
- 5xx
- network/DNS/TLS kopması
- timeout
- tool failure
- Bash timeout
- subagent timeout
- permission approval bekleme
- context compaction
- step/attempt limitleri
- Kimi process crash
- tmux kaybı
- systemd problemi
- VPS reboot
- VPS power loss
- OOM killer
- disk/inode dolması
- hook tarafından yanlış block
- session'ın yanlışlıkla yenilenmesi
- yeni session açılması
- yanlış session resume edilmesi
- eski watchdog'un yanlış /goal resume spam'i

Her sebebi şu üç sınıftan birine koy:

A) GERÇEK BİTİŞ — devam edilmemeli
B) GEÇİCİ ENGEL — sorun geçince aynı Goal devam etmeli
C) ALTYAPI KESİNTİSİ — VPS ayağa gelince aynı session/Goal geri kaldırılmalı

Listeyi çıkardıktan sonra BENDEN ONAY BEKLEME.
Doğrudan aşağıdaki dayanıklılık sistemini kur.

==================================================
B — MEVCUT DAYANIKLILIK SİSTEMİNİ ÖNCE İNCELE
==================================================

Çalışma dizini:
/var/www/anabeyin

Şunları incele:

/root/.kimi-code/config.toml
/root/.kimi-code/tui.toml
/root/.kimi-code/hooks/
~/.kimi-code/session_index.jsonl
~/.kimi-code/sessions/

/etc/systemd/system/anabeyin-kimi-keeper.service
/etc/systemd/system/anabeyin-kimi-watchdog.service
/etc/systemd/system/anabeyin-kimi-watchdog.timer

tmux kimioto

ve mevcut recovery/watchdog/keeper logları.

VAR OLAN sistemi körlemesine silip yeniden kurma.

Önce mevcut yapıyı anlamlandır.
Sonra idempotent biçimde düzelt/güçlendir.

SESSION dizinlerindeki state.json/wire.jsonl dosyalarını ELLE DEĞİŞTİRME.
Bunları yalnızca durum tespiti için READ-ONLY kullanabilirsin.

AnaBeyin uygulamasının backend/DB/frontend dosyalarına bu aşamada DOKUNMA.

==================================================
C — KIMI CONFIG: UNATTENDED ÇALIŞMA
==================================================

Mevcut config yapısını bozmadan şu davranışı sağla:

[loop_control]
max_steps_per_turn = 0
max_attempts_per_step = 60

[background]
keep_alive_on_exit = true
bash_auto_background_on_timeout = true
bash_task_timeout_s = 0

[subagent]
timeout_ms = 0

Duplicate TOML section oluşturma.

Deprecated max_retries_per_step kullanma.

Permission modu AUTO olacak.

Kimi yeniden kaldırılırken:

kimi --session <PINNED_SESSION_ID> --auto

kullan.

Normal `kimi` çalıştırıp yanlışlıkla yeni session oluşturma.

==================================================
D — VPS / TMUX / SYSTEMD KORUMASI
==================================================

Amaç:

Kullanıcı:
- laptopu kapatsa
- laptop uykuya geçse
- Chrome kapansa
- Hostinger terminali kapansa
- SSH kopsa
- yerel interneti kesilse

Kimi VPS üzerinde çalışmaya devam edecek.

Kimi process gerçekten çökerse:

AYNI SESSION ID
+
/var/www/anabeyin
+
--auto

ile tekrar kaldır.

tmux session adı:
kimioto

Aynı anda iki Kimi process açılmasını engelle.

VPS reboot olursa systemd boot sonrasında keeper/watchdog tekrar ayağa kalksın ve aynı session'a dönsün.

NOT:
VPS gerçekten kapalı olduğu sürede veya provider kotası fiziksel olarak kapalı olduğu sürede model çalışamaz.
Ancak bu durumlarda Goal/session KAYBOLMAYACAK.
VPS/provider tekrar kullanılabilir olduğunda AYNI GOAL kaldığı yerden devam edecek.

==================================================
E — WATCHDOG KARAR MOTORU
==================================================

Watchdog'un en önemli kuralı:

SADECE GERÇEKTEN PAUSED veya RECOVERABLE BLOCKED olan MEVCUT Goal resume edilebilir.

ASLA ekran yazısına körlemesine göre karar verme.
Kurulu sürümde mevcut olan native Goal/session state/event verisini güvenli READ-ONLY şekilde doğrula.

KESİN KURALLAR:

ACTIVE GOAL
→ hiçbir şey yapma, çalışmasına izin ver.

PAUSED GOAL
→ sebebi geçiciyse cooldown sonrası /goal resume.

RECOVERABLE BLOCKED GOAL
→ sorun çözülebiliyorsa çöz ve aynı Goal'u devam ettir.

NO CURRENT GOAL / goal=null
→ /goal resume YASAK.

GOAL COMPLETE
→ /goal resume YASAK.

GOAL CLEAR complete sonrası
→ /goal resume YASAK.

GOAL CANCELLED
→ /goal resume YASAK.

YENİ GOAL
→ watchdog kendiliğinden oluşturmayacak.

`/goal next`
→ watchdog hiçbir zaman kullanmayacak.

==================================================
F — HATA / RETRY POLİTİKASI
==================================================

TRANSIENT:
- network
- DNS
- TLS
- timeout
- normal 429
- 502
- 503
- 504
- geçici provider/runtime hatası

Bunlarda kontrollü retry/resume yap.

KOTA:
- usage limit
- exhausted quota
- billing-cycle limit
- kota kaynaklı 403/429

Bunlarda Goal'u:
SİLME
CANCEL ETME
REPLACE ETME
YENİ SESSION AÇMA.

Aynı hatayı saniyeler içinde spam etme.

Cooldown uygula.
Örneğin 30 dakika veya kurulu sürüm/dokümana göre daha güvenli makul periyot.

Kota tekrar açıldığında aynı Goal'u resume et.

401/auth:
credential değiştirme.
Goal'u koru.
Seyrek kontrollü deneme yap.

Tool/test/build/subagent hatasında:
Goal'u terk etme.
Hatayı araştır.
Gerekirse yeniden dene veya farklı güvenli yöntem kullan.

==================================================
G — HOOKLAR
==================================================

Resmi hooks mekanizmasını kullanırken:

- SessionHeartbeat
- StopFailure
- Interrupt
- SessionStart/SessionEnd
- compact eventleri

gibi olayları gerekiyorsa gözlem amacıyla kullan.

Hook hatası ana çalışmayı yanlışlıkla durdurmasın.

Bilerek block eden exit=2 davranışını yalnız gerçekten gerekli ise kullan.

Dayanıklılığın tek noktası hook OLMASIN.
Asıl process geri kaldırma systemd/tmux tarafından da güvence altında olsun.

==================================================
H — COMPLETE KİLİDİ: GEÇEN SEFERKİ HATAYI TEKRARLAMA
==================================================

BU BÖLÜM ZORUNLU.

Bu yeni V4 çalışması için durum marker'ları oluştur.

Örneğin:

/root/.kimi-code/ANABEYIN_THEME_V4_RUNNING
/root/.kimi-code/ANABEYIN_THEME_V4_COMPLETE

RUNNING içinde en az:
- session ID
- Goal kimliği/tespit bilgisi
- RAW URL
- RAW SHA256
- başlangıç zamanı

bulunsun.

COMPLETE yalnız bu yeni V4 Goal GERÇEKTEN complete olduğunda oluşturulsun.

Daha önceden kalmış aynı isimli marker varsa:
KÖRLEMESİNE güvenme.

İçindeki:
- session
- RAW hash
- zaman
- goal bilgisi

bu yeni çalışmayla eşleşmiyorsa onu STALE olarak yedekle/ayır.
Yeni V4 işini tamamlandı sanma.

V4 Goal gerçek complete olduğunda:

1. COMPLETE marker oluştur.
2. RUNNING marker kaldır.
3. Final log'a:
   THEME_V4_COMPLETE=YES
   yaz.
4. Watchdog bundan sonra V4 için NO-OP olsun.
5. `/goal resume` GÖNDERME.
6. yeni Goal oluşturma.
7. `/goal next` kullanma.
8. model çağrısı başlatma.
9. bitmiş işi yeniden yüklemeye çalışma.
10. kullanıcı yeni görev vermeden hiçbir geliştirme başlatma.

GEÇEN SEFERKİ:
Goal complete → No current goal → watchdog /goal resume → 403 → pause → resume

DÖNGÜSÜ KESİNLİKLE TEKRARLANMAYACAK.

Goal complete gerçek bitiştir.

==================================================
I — DAYANIKLILIK DOĞRULAMASI
==================================================

Tema V4'e başlamadan önce kendi yazdığın sistemi güvenli şekilde doğrula.

Canlı projeyi bozacak test yapma.

Şunların gerçekten doğru olduğunu kanıtla:

AUTO_MODE=YES
SAME_SESSION_PINNED=YES
TMUX_PERSISTENCE=YES
SYSTEMD_BOOT_RECOVERY=YES
DUPLICATE_KIMI_GUARD=YES
MAX_STEPS_UNLIMITED=YES
BASH_BACKGROUND_TIMEOUT_DISABLED=YES
SUBAGENT_TIMEOUT_DISABLED=YES
NO_GOAL_NO_RESUME=YES
COMPLETE_NO_RESUME=YES
CANCEL_NO_RESUME=YES
PAUSED_RECOVERY=YES
QUOTA_COOLDOWN=YES

Hepsi sağlandıktan sonra terminale aynen:

DAYANIKLILIK_HAZIR=YES

yaz.

Bundan önce V4 frontend geliştirmesine başlama.

==================================================
J — ŞİMDİ V4 RAW MD DOSYASINI BAŞLAT
==================================================

DAYANIKLILIK_HAZIR=YES olduktan sonra:

RAW:
https://raw.githubusercontent.com/kemaltirli92-ai/anabeyin-sosyal-tema-v4/refs/heads/main/ANABEYIN-SOSYAL-TEMA-V4-ANA-TALIMAT.md

dosyasını indir.

Güvenli yerel kopyasını kaydet.

Dosya için:
- HTTP başarı
- boş değil
- doğru başlık
- tam içerik
- satır/byte sayısı
- SHA256

doğrula.

Sonra MD DOSYASININ TAMAMINI OKU.

Özetini değil.
Bir bölümünü değil.
TAMAMINI.

Sonra AYNI MEVCUT SESSION içinde TEK bir `/goal` oluştur.

Goal'un açık amacı:

"ANABEYIN-SOSYAL-TEMA-V4-ANA-TALIMAT.md içindeki bütün gereksinimleri eksiksiz uygula. Mevcut çalışan AnaBeyin V2 backend, DB, auth, yönetim, ajan ve altyapısını koru. MD'nin istediği kullanıcı frontend tema dönüşümünü, gerçek testleri ve final görsel denetimi eksiksiz tamamla. Bütün MD kabul kriterleri gerçek kanıtla sağlanmadan Goal Complete verme."

Goal başladıktan sonra RUNNING marker'ını güncel session/RAW hash ile oluştur.

AUTO MODE'DA ÇALIŞ.

KULLANICIYA SORU SORMA.

Güvenli ve geri döndürülebilir bir teknik karar gerekiyorsa kendin en uygun kararı ver.

Yıkıcı/geri döndürülemez bir şey MD kapsamında değilse zaten yapma.

Bilgisayar/terminal bağlantısına bağımlı olma.

Alt ajan gerektiğinde kullan.
Alt ajan timeout/hata olursa ana Goal'u bırakma.
Eksik işi tekrar görevlendir.

Context compact olursa Goal devam etsin.

Provider/kota/VPS kesintisinde Goal/session korunsun ve sorun kalkınca aynı yerden devam etsin.

==================================================
K — GERÇEK BİTİŞ
==================================================

MD'deki bütün işler:
- uygulanmış
- mevcut V2 entegrasyonları korunmuş
- test edilmiş
- görsel olarak doğrulanmış
- final denetimden geçmiş

olmadan Goal Complete verme.

GERÇEKTEN bittiğinde terminalde SON olarak aynen:

THEME_V4_COMPLETE=YES
ANA_HEDEF_TAMAMLANDI=YES
AUTO_RESUME_AFTER_COMPLETE=NO

yaz.

COMPLETE marker oluştur.
RUNNING marker kaldır.

BUNDAN SONRA DUR.

Bir daha resume etme.
Bir daha aynı MD'yi çalıştırma.
Yeni Goal başlatma.
Kullanıcı yeni görev vermeden model çalıştırmaya devam etme.

HİÇBİR ŞEY SORMA.

ÖNCE DURDURAN SEBEPLERİ ARAŞTIR VE LİSTELE.
SONRA DAYANIKLILIĞI KODLA/KUR.
DAYANIKLILIK_HAZIR=YES SONRASI V4 RAW MD'Yİ BAŞLAT.
ANA HEDEF TAMAMLANANA KADAR DEVAM ET.
ANA HEDEF TAMAMLANINCA KESİNLİKLE DUR.
