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


---

**ASP.Net Web Api Routing  nedir?**

ASP.NET Web API, Microsoft tarafından sunulan bir framework'tür ve HTTP protokolü üzerinden web servislerini oluşturmak için kullanılır. Web API, RESTful web servisleri oluşturmak için özellikle uygun bir şekilde tasarlanmıştır. Bu framework, ASP.NET MVC'nin avantajlarını kullanarak, web API'lerini oluşturmak ve yönetmek için kolay ve esnek bir yol sunar.

ASP.NET Web API Routing ise, Web API'de gelen isteklerin hangi yöntemlerle ve hangi kontrolcülerle eşleştirileceğini belirleyen bir mekanizmadır. Routing, gelen HTTP isteğinin URL'sine bakarak, hangi denetleyicinin ve eylemin işleneceğini belirler. Bu, Web API'nin, isteklerin doğru eyleme yönlendirilmesini sağlamak için kullanılan temel bir bileşenidir.

Örneğin, bir HTTP GET isteği "/api/products" URL'sine yönlendirildiğinde, Web API routing'i, bu isteği ProductsController içindeki bir GET metoduyla eşleştirebilir ve istemciye ürünlerin listesini döndürebilir.

Routing, RESTful prensiplere uygun bir şekilde, HTTP yöntemlerine (GET, POST, PUT, DELETE vb.) ve URL yapılarına dayalı olarak istekleri işleyerek, uygulamanın doğru davranışını sağlar. Bu şekilde, gelen isteklerin nasıl işleneceğini kontrol etmek ve yönlendirmek için esneklik sağlar.


Diyelim ki bir e-ticaret uygulaması yapıyorsunuz ve ürünlerin API'sini oluşturmak istiyorsunuz. Ürünlerle ilgili birkaç temel işlem yapmanız gerekecek: ürünleri listeleyebilirsiniz, belirli bir ürünü alabilirsiniz, yeni bir ürün ekleyebilirsiniz, mevcut bir ürünü güncelleyebilirsiniz veya silebilirsiniz.

Ürünleri Listeleme (**GET** isteği):

    -URL: /api/products
    -HTTP Metodu: GET
    -Bu URL'ye gelen bir GET isteği, tüm ürünleri listeleyen bir API işlemini tetikleyecektir.


Belirli bir Ürünü Alma (**GET** isteği):

    -URL: /api/products/{id}
    -HTTP Metodu: GET
    -Burada "{id}" yolu, belirli bir ürünün kimliğini temsil eder. Örneğin, /api/products/123 URL'sine gelen bir GET isteği, id'si 123 olan bir ürünün detaylarını getiren bir API işlemini tetikleyecektir.

Yeni Bir Ürün Ekleme (**POST** isteği):

    -URL: /api/products
    -HTTP Metodu: POST
    -Bu URL'ye gelen bir POST isteği, yeni bir ürün eklemek için bir API işlemini tetikleyecektir.

---

        // GET api/products
        public IHttpActionResult GetProducts()
        {
            return Ok(products);
        }

        

        // GET api/products/{id}
        public IHttpActionResult GetProduct(int id)
        {
            var product = products.FirstOrDefault(p => p.Id == id);
            if (product == null)
                return NotFound();

            return Ok(product);
        }

        

        // POST api/products
        public IHttpActionResult PostProduct(Product product)
        {
            if (!ModelState.IsValid)
                return BadRequest(ModelState);

            products.Add(product);
            return CreatedAtRoute("DefaultApi", new { id = product.Id }, product);
        }

        // PUT api/products/{id}
        public IHttpActionResult PutProduct(int id, Product product)
        {
            if (!ModelState.IsValid)
                return BadRequest(ModelState);

            var existingProduct = products.FirstOrDefault(p => p.Id == id);
            if (existingProduct == null)
                return NotFound();

            existingProduct.Name = product.Name;
            existingProduct.Price = product.Price;

            return StatusCode(HttpStatusCode.NoContent);
        }

        // DELETE api/products/{id}
        public IHttpActionResult DeleteProduct(int id)
        {
            var product = products.FirstOrDefault(p => p.Id == id);
            if (product == null)
                return NotFound();

            products.Remove(product);
            return Ok(product);
        }
    }


---

**ASP.Net Web Api Routing (Action Based Routing)?**

Action Based Routing, bir web uygulamasında HTTP isteklerini belirli işlemlere (action) yönlendirmek için kullanılan bir yönlendirme yöntemidir. Bu tür yönlendirme genellikle MVC (Model-View-Controller) mimarisine dayalı web uygulamalarında kullanılır.

Action Based Routing, bir HTTP isteğinin geldiği URL ve isteğin türüne (GET, POST, PUT, DELETE vb.) bakarak hangi işlemin gerçekleştirileceğini belirler. Bu yöntemde, isteğin URL'si ve isteğin türü, bir Controller sınıfındaki belirli bir Action metoduyla eşleştirilir.

Örneğin, bir web uygulamasında "/products" URL'sine yapılan bir HTTP GET isteği, "ProductsController" adlı bir Controller sınıfındaki "GetProducts" adlı bir Action metoduyla eşleştirilebilir. Benzer şekilde, "/products/create" URL'sine yapılan bir HTTP GET isteği, yine "ProductsController" sınıfındaki "Create" adlı bir Action metoduyla eşleştirilebilir.

Action Based Routing, bir web uygulamasının URL yapısını ve kullanılabilir işlemleri (action'ları) belirlemek için oldukça esnek bir yöntemdir. Bu sayede, istemcilere daha anlaşılır ve kolay kullanılabilir bir API sunulabilir.

Özetle, Action Based Routing, HTTP isteklerini belirli işlemlere yönlendirmek için URL ve isteğin türüne dayanan bir yönlendirme yöntemidir ve genellikle MVC tabanlı web uygulamalarında kullanılır.

**Action Based Routing**

    public static class WebApiConfig
    {
        public static void Register(HttpConfiguration config)
        {
            // Web API configuration and services

            // Web API routes
            config.MapHttpAttributeRoutes();

            config.Routes.MapHttpRoute(
                name: "DefaultApi",
                routeTemplate: "api/{controller}/{action}/{id}",
                defaults: new { id = RouteParameter.Optional }
            );
        }
    }

Yukarıdaki kod bir ASP.NET Web API uygulamasında bulunan WebApiConfig sınıfı içerisindeki Register metodu tanımlar. Bu metot, Web API'nin yapılandırılması ve hizmetlerin kaydedilmesi için kullanılır. İşlevlerini aşağıdaki gibi açıklayabiliriz:

config.MapHttpAttributeRoutes();: Bu satır, HTTP yönlendirme özniteliklerini kullanarak tanımlanmış rotaları eşlemek için kullanılır. Yani, Route özniteliği ile işaretlenmiş yönlendirmeleri etkinleştirir.

config.Routes.MapHttpRoute(...): Bu satır, belirli bir HTTP isteği için bir denetleyiciyi ve eylemi belirten varsayılan bir yönlendirme kuralı tanımlar. Bu örnekte, "DefaultApi" adında bir rota tanımlanmıştır. Bu rota, ***/api/{controller}/{id}*** şablonuna uyan istekleri karşılayacaktır. {controller} ve {id} yer tutucular, istekleri karşılayacak olan denetleyici ve isteğe bağlı olarak id parametresini belirtir. Eğer id belirtilmezse, RouteParameter.Optional kullanılarak varsayılan olarak belirtilir. 

---

![image](https://live.staticflickr.com/65535/53585308280_66ff5a3c44_n.jpg)

---

![image](https://live.staticflickr.com/65535/53584892586_1da41ac423_c.jpg)

---

-Action Based Routing örneğine geçecek olursak App_start klasörünün altındaki WebApiConfig.cs dosyasına gelerek {controller} sonra {action} ifadesinin gelenceğini belirtiyoruz. 

![image](https://live.staticflickr.com/65535/53584898961_76e55fc35a_z.jpg)

-Daha sonra controler ValuesController gidip metod isimlerini aşağıdaki gibi güncelleyebiliriz.

   public class ValuesController : ApiController
   {

       static List<string> degerler = new List<string>()
       { "Value0","Value1","Value2"};


       // GET api/values
       public IEnumerable<string> Degerler()
       {
           return degerler;
       }

       // GET api/values/5
       public string DegerGetir(int id)
       {
           return degerler[id];
       }

       // POST api/values
       public void DegerEkle([FromBody] string value)
       {
           degerler.Add(value);
       }

       // PUT api/values/5
       public void DegerGuncelle(int id, [FromBody] string value)
       {
           degerler[id] = value;   
       }

       // DELETE api/values/5
       public void DegerSil(int id)
       {
           degerler.RemoveAt(id);
       }
   }

   Yukarıdaki durumda Degeler metodu bize değerleri getirsin, DegerGetir metodu bize değeri getirsin DegerEkle metodu eklemeyi, DegerGuncelle  güncellemeyi, DegerSil ise bize silme işlemini yapsın. 
   Sadece bu hali ile action'ı çalıştırırsak bize 405 hatası vericektir açıklamak gerekirse HTTP istek yöntemini (GET, POST, PUT, DELETE, vb.) desteklemiyor hatasıdır. Bunun anlamı bu şekilde GET isteiğinde bulunamazsıız    anlamına geliyor. 
   
   Bunu aşmak için aşağıdaki **[HttpGet]** Niteliği (Attribute) eklememiz gerekiyor. attribute eklediğimiz taktirde bize 200 code dönecektir. 

            // GET api/values
        [HttpGet]
        public IEnumerable<string> Degerler()
        {
            return degerler;
        }


  

   
    


