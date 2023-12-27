Pytest Decoratorleri


Pytest kütüphanesi, Python dilinde yazılmış bir test framework’tür ve test yazımını kolaylaştırmak için bir dizi özellik sağlar. Bu özelliklerden biri de "decorator" adı verilen özel işaretçilerdir. Bu decoratorler, testlerin nasıl çalıştırılacağını, hangi ortamların kullanılacağını ve test sonuçlarının nasıl yorumlanacağını kontrol etmek için kullanılabilir. İşte Pytest kütüphanesinde sıkça kullanılan bazı decoratorler:
@pytest.mark.skip: Bu decorator, bir testin geçici olarak atlanılması gerektiğini belirtir.Belirli bir testin koşullarının geçici olarak uygun olmadığı durumlarda testin çalıştırılmasını engeller. Genellikle testin henüz tamamlanmamış olduğu, bir hata içerdiği veya geçici bir sorun nedeniyle çalıştırılmadığı durumlarda kullanılır.
@pytest.mark.skipif:Bu decorator, testin yalnızca belirli bir koşul sağlandığında atlanması gerektiğini belirtir. Yani, testin çalıştırılıp çalıştırılmaması, belirli bir koşulu sağlayıp sağlamadığına bağlı olarak belirlenir.
@pytest.mark.parametrize:Bu decorator, testin birden çok parametreyle çalıştırılmasını sağlar. Aynı testi farklı parametre setleriyle tekrarlamak için kullanılır.
@pytest.mark.xfail:Bu decorator,  bir testin beklenen bir şekilde başarısız olmasını işaretlemek için kullanılır.Testin geçici bir hata veya eksiklik içerdiğini, ancak bu durumun gelecekte düzeltileceğini belirtir. Bu şekilde, test sonucu başarısız olmasına rağmen, bu başarısızlık test raporlarına "beklenen bir başarısızlık" olarak işlenir ve test sonuçları üzerinde olumsuz bir etkisi olmaz.



@pytest.fixture: Bir test fonksiyonu veya metodu için önceden tanımlanmış bir durumu (fixture) oluşturmak için kullanılır.  Fixture'lar, testlerin ihtiyaç duyduğu önceden ayarlanmış durumları, verileri veya nesneleri sağlamak için kullanılır. Bu, testlerin belirli bir başlangıç durumuyla çalışmasını ve tekrarlanabilirliği sağlar.

@pytest.mark.parametrize ile indirect=True: Decorator'ü indirect=True parametresiyle birlikte kullanarak, parametre değerlerinin, bir başka işlevin sonuçlarını döndüren bir başka işleve iletilmesini sağlar. Bu, test durumlarını daha dinamik ve esnek hale getirerek, test fonksiyonlarına çeşitli ve karmaşık parametre setlerinin sağlamasını mümkün kılar.

@pytest.mark.parametrize ile ids: Parametre setlerine özel kimlikler eklemek için kullanılır. Bu, testlerin çıktısını daha anlamlı hale getirmenize yardımcı olabilir.

@pytest.mark.timeout: Bir testin belirli bir sürede tamamlanması gerektiğini belirtmek için kullanılır.Özellikle zamanla duyarlı test senaryolarında veya testlerin anormal bir şekilde uzun sürmesi durumunda fark edilmesini sağlar.

@pytest.mark.flaky: Bu decorator, belirli bir testin zamanla değişken bir şekilde başarılı veya başarısız olabileceğini belirtmek için kullanılır. Yani, bu decorator, bazı test senaryolarının zaman içinde değişen koşullara bağlı olarak geçebilir veya başarısız olabilir olduğunu ifade eder.Bir testin kaç kez tekrarlanması gerektiğini ve bu tekrarlamalar sırasında testin kaç kez başarılı olması gerektiğini belirlemek için kullanılır. Bu özellik, özellikle bazı durumlarda test sonuçlarının rastgele veya çevresel koşullara bağlı olarak değişebileceği durumlar için kullanışlıdır.

@pytest.mark.asyncio: Python'daki asyncio kütüphanesini kullanarak asenkron (async) testler yazmak için kullanılan bir decorator'dür. Asenkron programlamada yaygın olarak kullanılan asyncio kütüphanesi, Python'da asenkron işlevselliği sağlamak için kullanılır.
@pytest.mark.benchmark: Bu decorator, belirli bir test fonksiyonunun çalışma süresini ve diğer performans metriklerini ölçmeye olanak tanır.Performans testleri, bir işlevin veya algoritmanın belirli koşullar altında ne kadar süre aldığını ölçmek ve performansı değerlendirmek amacıyla kullanılır.
