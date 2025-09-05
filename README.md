Microservices Demo

Bu proje, Python ile geliştirilmiş basit bir microservices mimarisini göstermektedir.  
Projede iki mikro servis vardır: `user_service` ve `product_service`.  
Docker ve Docker Compose kullanılarak kolayca çalıştırılabilir.

📦 İçerik
- `user_service/` – Kullanıcı yönetim servisi (CRUD işlemleri)  
- `product_service/` – Ürün yönetim servisi (CRUD işlemleri)  
- `tests/` – Basit testler (pytest ile çalıştırılabilir)  
- `docker-compose.yml` – Servisleri tek komutla ayağa kaldırmak için

⚙️ Gereksinimler
- [Python 3.9+](https://www.python.org/)  
- [Docker](https://www.docker.com/get-started)  
- [Docker Compose](https://docs.docker.com/compose/install/)  

🚀 Kurulum ve Çalıştırma
1. Proje klasörüne gidin
Terminal veya PowerShell açın ve projenin bulunduğu klasöre gidin:

```bash
cd /path/to/microservices

2. Ayağa kaldırın
docker compose up --build
Bu komut hem servisleri build eder hem de çalıştırır. Servisler arka planda çalışacaktır.

3. Servisleri durdurmak için
docker compose down

🌐 API Endpoints
User Service

GET	/users	Tüm kullanıcıları listeler
POST	/users	Yeni kullanıcı ekler

Product Service

GET	/products	Tüm ürünleri listeler
POST	/products	Yeni ürün ekler

Test için Postman veya curl kullanılabilir. Örnek:
curl -X GET http://localhost:5000/users
curl -X POST http://localhost:5000/users -H "Content-Type: application/json" -d '{"name": "Ali"}'

🧪 Testler

Basit testleri çalıştırmak için:
cd tests
pytest

Pytest testleri çalıştırır ve servislerin doğru çalışıp çalışmadığını kontrol eder.


