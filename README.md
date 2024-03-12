<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web API Nedir?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
        }
        h1 {
            color: #333;
        }
        p {
            color: #666;
            margin-bottom: 20px;
        }
        strong {
            color: #000;
        }
        em {
            font-style: italic;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Herkese selamlar! 👋</h1>
        <p>Bu projede Web API üzerine eğiliyor olacağım. Hem kendime hatırlatmak için hem de faydalanmak isteyenler için hazırlıyorum, umarım faydalı olur.</p>
        <p>Öncelikle <strong>Web API Nedir?</strong> Bu kavram üzerinde başlangıç yapmak daha yararlı olacaktır.</p>
        <p><strong>Web API (Web Application Programming Interface)</strong>, bir yazılım uygulamasının diğer yazılım uygulamalarıyla iletişim kurmasını sağlayan bir arayüzdür. Genellikle HTTP protokolü üzerinden erişilebilir ve web tabanlı hizmetlerin (web servisleri) bir türü olarak kullanılır.</p>
        <p>Web API'ler, istemci uygulamalarının sunucu tarafında bulunan verilere veya işlemlere erişmesine olanak tanır. Genellikle <em>REST (Representational State Transfer)</em> mimarisine dayanır ve CRUD (Create, Read, Update, Delete) operasyonlarını destekler. Bu, web API'lerinin veri oluşturma, okuma, güncelleme ve silme işlemlerini gerçekleştirmek için kullanılabileceği anlamına gelir.</p>
        <p>Web API'ler, farklı platformlar arasında iletişim kurmak için kullanılır. Örneğin, bir web uygulaması mobil uygulama, masaüstü uygulaması veya başka bir web uygulaması ile veri alışverişi yapabilir.</p>
        <p>Özetlemek gerekirse, <strong>Web API'ler</strong>, yazılım uygulamaları arasında veri ve işlem alışverişi yapmak için kullanılan bir arayüzdür ve genellikle HTTP protokolü üzerinden erişilebilir.</p>
    </div>

    <div class="container">
        <p><strong>Neden Web API'i Seçmeliyiz?</strong></p>
        <ul>
            <li>Bir web service'e ihtiyacınız varsa ve SOAP'a ihtiyacınız yoksa en iyi seçenek Web API'dir</li>
            <li>Geliştirme süreci WCF de olduğu kadar zahmetli ve sıkıntılı değildir</li>
            <li>HTTP tabanlı olduğundan REST-ful servisler geliştirmek için en iyi seçenektir.</li>
            <li>Exception ve Cahce mimarileri oldukça performanslı ve yönetilebilir dir.</li>
            <li>Open source olduğundan sürekli olarak geliştirilip yeni özellikler eklenmektedir.</li>
        </ul>

    </div>
    <div class="container">
    <p><strong>Kullanım alanları nelerdir.</strong></p>
    <ul>
        <li>Mobil uygulamalar.</li>
        <li>SPA(Single Page Application) Web siteleri</li>
        <li>Entegrasyonlar</li>
        <li>Bir uygulamanın geliştiricilere açılması</li>
    </ul>
    </div>

    <div class="container">
        <p><strong>HTTP protokolü</strong></p>
        <p>HTTP'nin açılı <em>Hyper Text Transfer Protocol'dür.</em> "Hypertext" terimi, bağlantılarla zenginleştirilmiş metinleri ifade ederken, "Transfer Protocol" ise verilerin iletimi için kullanılan bir protokol anlamına gelir </p>

    </div>

    <div class="container">

        <p><strong>HTTP metotları</strong></p>
        <table>
            <thead>
                <tr>
                    <th>Method</th>
                    <th>Amaç</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>GET</td>
                    <td>Bir kaynağı almak için kullanılır</td>
                </tr>
                <tr>
                    <td>POST</td>
                    <td>Bir kaynağı oluşturmak için kullanılır</td>
                </tr>
                <tr>
                    <td>PUT</td>
                    <td>Bir kaynağı güncellemek için kullanılır</td>
                </tr>
                <tr>
                    <td>DELETE</td>
                    <td>Bir kaynağı silmek için kullanılır</td>
                </tr>
    </div>


</body>
</html>
