# Herkese selamlar! 👋

Bu projede Web API üzerine eğiliyor olacağım. Hem kendime hatırlatmak için hem de faydalanmak isteyenler için hazırlıyorum, umarım faydalı olur.

Öncelikle **Web API Nedir?** Bu kavram üzerinde başlangıç yapmak daha yararlı olacaktır.

**Web API (Web Application Programming Interface)**, bir yazılım uygulamasının diğer yazılım uygulamalarıyla iletişim kurmasını sağlayan bir arayüzdür. Genellikle HTTP protokolü üzerinden erişilebilir ve web tabanlı hizmetlerin (web servisleri) bir türü olarak kullanılır.

Web API'ler, istemci uygulamalarının sunucu tarafında bulunan verilere veya işlemlere erişmesine olanak tanır. Genellikle *REST (Representational State Transfer)* mimarisine dayanır ve CRUD (Create, Read, Update, Delete) operasyonlarını destekler. Bu, web API'lerinin veri oluşturma, okuma, güncelleme ve silme işlemlerini gerçekleştirmek için kullanılabileceği anlamına gelir.

Web API'ler, farklı platformlar arasında iletişim kurmak için kullanılır. Örneğin, bir web uygulaması mobil uygulama, masaüstü uygulaması veya başka bir web uygulaması ile veri alışverişi yapabilir.

Özetlemek gerekirse, **Web API'ler**, yazılım uygulamaları arasında veri ve işlem alışverişi yapmak için kullanılan bir arayüzdür ve genellikle HTTP protokolü üzerinden erişilebilir.

---

**Neden Web API'i Seçmeliyiz?**

- Bir web service'e ihtiyacınız varsa ve SOAP'a ihtiyacınız yoksa en iyi seçenek Web API'dir
- Geliştirme süreci WCF de olduğu kadar zahmetli ve sıkıntılı değildir
- HTTP tabanlı olduğundan REST-ful servisler geliştirmek için en iyi seçenektir.
- Exception ve Cahce mimarileri oldukça performanslı ve yönetilebilir dir.
- Open source olduğundan sürekli olarak geliştirilip yeni özellikler eklenmektedir.

---

**Kullanım alanları nelerdir?**

- Mobil uygulamalar.
- SPA(Single Page Application) Web siteleri
- Entegrasyonlar
- Bir uygulamanın geliştiricilere açılması

---

**HTTP protokolü**

HTTP'nin açılış **Hyper Text Transfer Protocol'dür.** "Hypertext" terimi, bağlantılarla zenginleştirilmiş metinleri ifade ederken, "Transfer Protocol" ise verilerin iletimi için kullanılan bir protokol anlamına gelir.

---

**HTTP metotları**

| Method | Amaç                             |
|--------|----------------------------------|
| GET    | Bir kaynağı almak için kullanılır |
| POST   | Bir kaynağı oluşturmak için kullanılır |
| PUT    | Bir kaynağı güncellemek için kullanılır |
| DELETE | Bir kaynağı silmek için kullanılır |

---

**HTTP status code (Durum Kodları)**

| 1xx: Kod | Açıklama (Bilgi)       |
|----------|------------------------|
| 100      | Continue               |
| 101      | Switching Protocols    |
| 102      | Processing             |

| 2xx: Kod | Açıklama (Başarı)      |
|----------|------------------------|
| 200      | Ok                     |
| 201      | Created                |
| 204      | No Content             |

| 3xx: Kod | Açıklama (Yönlendime)  |
|----------|------------------------|
| 301      | Moved Permanently                     |
| 302      | Found                |
| 305      | Use Proxy              |

| 4xx: Kod | Açıklama (Client Hata)      |
|----------|------------------------|
| 400      | Bad Request                     |
| 401      | Unauthorized                |
| 405      | Method Not Allowed             |

| 5xx: Kod | Açıklama (Sunucu Hata)      |
|----------|------------------------|
| 500      | Internal Server Error                   |
| 501      | Not Implemented               |
| 503      | Service Unavailable           |

---

**HTTP Nasıl Çalışır**
HTTP’nin çalışma prensibi istemci(client) — sunucu(server) ilişkisine dayanmaktadır. 

Bu çalışma prensibini açıklamak gerekirse:

**Request (İstek):**
Kullanıcı bir web sayfasını görüntülemek, dosya indirmek veya form göndermek gibi bir işlemi gerçekleştirmek istediğinde istemci (client yani tarayıcı) bir HTTP isteği yapar. İstek, belirli bir kaynağı (örneğin bir web sayfasını) talep eden bir mesajdır. Bu mesaj, isteğin türünü (GET, POST gibi) ve talep edilen kaynağın adresini içerir.

**Processing (İşleme):**
Sunucu, isteği aldıktan sonra talep edilen kaynağı bulur ve gerekli işlemleri gerçekleştirir. Bu işlemler nedir? Veri tabanı sorguları, dosya okuma/yazma işlemleri veya dinamik içerik oluşturma gibi çeşitli işlemlerdir.

**Response (Yanıt):**
Sunucu talep edilen işlemi tamamladıktan sonra bir HTTP yanıtı oluşturur. Yanıt, sunucunun yaptığı işlemlerin sonucunu içerir.

---

**HTTP HEADER ve BODY Nedir?***
HTTP başlıkları (headers) ve gövdesi (body), HTTP iletişimi sırasında taşınan bilgilerin iki ana bileşenidir:

**HTTP Başlıkları (HTTP Headers):**

HTTP başlıkları, istek veya yanıtın (response) meta bilgilerini içerir. Başlıklar, istek veya yanıtın niteliklerini, içeriğini, sunucu özelliklerini ve daha fazlasını tanımlar. Örneğin, ***isteğin hedefi (Host)***, ***kabul edilebilir içerik türleri (Accept)***, ***istemci bilgisi (User-Agent)*** gibi bilgileri içerebilirler. Başlıklar, anahtar-değer çiftleri şeklinde gelir ve her bir başlık bir ihtiyacı veya özelliği tanımlar.

**HTTP Gövdesi (HTTP Body):**

HTTP gövdesi, istek veya yanıtın (response) ana içeriğini taşır. İstek gövdesi, genellikle istemci tarafından sunucuya gönderilen verileri içerir. Örneğin, bir web formunun doldurulması sonucunda gönderilen veriler, bir dosya yükleme isteği veya bir API talebi gibi. Yanıt gövdesi ise sunucudan istemciye gelen veriyi içerir. Örneğin, bir web sayfasının HTML içeriği, bir resim dosyası veya bir JSON verisi gibi. Gövde, isteğin veya yanıtın içeriğine göre değişebilir ve bazen boş olabilir. Gövde, başlık bölümünden ayrı olarak gelir ve genellikle istek veya yanıtın sonunda yer alır. Gövde, metin, resim, video, JSON veya XML gibi farklı veri türlerini içerebilir.

**HTTP REQUEST**

- Host
    -
    Bir HTTP isteğinin hedefi olan sunucunun host adını belirtir. Bu genellikle bir IP adresi veya bir alan adı olabilir. Örneğin, "www.example.com" gibi bir alan adı veya "192.0.2.1" gibi bir IP adresi olabilir. Bu, sunucunun talebin gönderildiği belirli bir adresi belirtir ve sunucunun doğru kaynaklara yönlendirilmesini sağlar.
- Accept
    -
    Bu başlık, istemcinin (genellikle tarayıcı) sunucuya hangi medya türlerini veya dosya türlerini alabileceğini belirtir. Örneğin, bir web tarayıcısı HTML belgelerini, görsel resim dosyalarını veya JSON verilerini kabul edebilir. Sunucu, bu başlıkta belirtilen formatlarda yanıtlar döndürebilir veya dönmeden önce uygun bir formata dönüştürebilir.
- User-Agent
    - 
    Bu, istemcinin (tarayıcı veya uygulama) kendini sunucuya tanımladığı bir dizedir. Genellikle, tarayıcı adı ve sürümü, işletim sistemi ve diğer istemci özelliklerini içerir. Sunucu, bu bilgileri kullanarak, kullanıcı deneyimini iyileştirmek veya tarayıcıya uygun içerik sunmak için istemci hakkında daha fazla bilgi edinebilir.
- Accept-Encoding
    -
    Bu başlık, istemcinin sunucudan almayı kabul ettiği içerik kodlamalarını belirtir. Örneğin, "gzip" veya "deflate" gibi sıkıştırma algoritmalarını belirtebilir. Sunucu, içeriği sıkıştırarak, veri transferini azaltabilir ve daha hızlı yanıtlar sağlayabilir. Bu başlık, istemcinin sıkıştırılmış içeriği kabul edip etmediğini belirtir.

**Not:**
GET isteiğinde BODY yer almaz. 
PUT, POST gibi metot istekleri BODY alanı ile beraber yapılır. Bunun sebebi ***GET*** işlemi okuma amaçlı yapılan bir işlem bu nedenle body yer almaz. ***PUT,POST ve DELETE*** data gönderileceği için datayı tutacak bir request body'ninde olması gerekir. 
