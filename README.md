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

**HTTP Nasıl Çalışır**
HTTP’nin çalışma prensibi istemci(client) — sunucu(server) ilişkisine dayanmaktadır. 

Bu çalışma prensibini açıklamak gerekirse:

**Request (İstek):**
Kullanıcı bir web sayfasını görüntülemek, dosya indirmek veya form göndermek gibi bir işlemi gerçekleştirmek istediğinde istemci (client yani tarayıcı) bir HTTP isteği yapar. İstek, belirli bir kaynağı (örneğin bir web sayfasını) talep eden bir mesajdır. Bu mesaj, isteğin türünü (GET, POST gibi) ve talep edilen kaynağın adresini içerir.

**Processing (İşleme):**
Sunucu, isteği aldıktan sonra talep edilen kaynağı bulur ve gerekli işlemleri gerçekleştirir. Bu işlemler nedir? Veri tabanı sorguları, dosya okuma/yazma işlemleri veya dinamik içerik oluşturma gibi çeşitli işlemlerdir.

**Response (Yanıt):**
Sunucu talep edilen işlemi tamamladıktan sonra bir HTTP yanıtı oluşturur. Yanıt, sunucunun yaptığı işlemlerin sonucunu içerir.
