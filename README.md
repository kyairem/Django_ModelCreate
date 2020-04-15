# Django_ModelCreate
Python - Django' da model.py dosyası oluşturma  

Ubuntu' da bir django projesi ve app oluşturma örneğidir.

#Django projesi oluşturma

İlk olarak django' yu kullanabilmek için sanal bir django ortamı kurulmuş olmalıdır.
Bu sanal ortam env adında kurulduktan sonra bu sanal ortam aktif edilmelidir. 
Bu sanal ortamı aktif etmek için sanal ortam içerisinde olunmalıdır. 
(Sanal ortamı kurmuş olduğum yer Desktop/django klasorüdür)
cd Desktop/django #sanal ortamın bulunduğu klasör 
(manage.py dosyasıyla aynı klasör içerisinde olmalıdır)
source env/bin/activate #sanal ortamı aktif etmek 
(env)>django-admin startproject blog . 
#blok adında içerisinde bulunulan klasöre django projesi oluşturulur
(env)>python manege.py migrate  #oluşturulan projeyi veritabanı yükleme
(env)>python manege.py runserver 
#gelen ip adresi ile web browser'da giriş yapıldığında django projesi görülür

#Django uygulama ve veritabanı oluşturma

(env)>python manage.py startapp post #post adında bir app oluşturulur
(env)>python manage.py makemigrations 
#app için veritabanı oluşturma post/migrations/0001_initial.py adında dosya oluşur
(env)>python manage.py migrate #app için çalışıcak veritabanı aktif etmek 
(env)>python manage.py sqlmigrate post 0001 
#post adındaki app' in veritabanının dilini sql diline çevirmeye yarar

#Djanjo projesi app ve veritabanı işlemlerinden sonra web browser' da 
uygulamayı görüntüleyebilmek için admin.py dosyası düzenlenmelidir.

/Desktop/django/post/admin.py dosyasının içeriğini düzenlemek gerekir.
(env)>python manege.py runserver #gelen ip adresiyle admin paneli 
için web browsera giriş yapılırsa oluşturulmuş olan post adında ki app gelmiş olmalıdır 
(örnek:127.0.0.1:8000\admin)
