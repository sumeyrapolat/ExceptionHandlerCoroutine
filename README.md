
Bu Kotlin kodu, bir Android uygulamasındaki MainActivity sınıfını içerir. Bu sınıf, yaşam döngüsü (lifecycle) kapsamında lifecycleScope kullanarak çeşitli coroutine örneklerini göstermektedir. Aynı zamanda CoroutineExceptionHandler kullanarak hata yönetimi konseptini de örneklemektedir.

İşte kodun özeti:

Normal Coroutine Kullanımı:

İki coroutine başlatılır, ancak hata (exception) oluştuğunda, bu hata try-catch bloğu içinde yakalanmaz. Bu durumda, hata yukarı doğru iletilir ve uygulama çökebilir.
Try-Catch ile Coroutine Hata Yönetimi:

İkinci bir coroutine başlatılır ve bu sefer hata try-catch bloğu içinde yakalanır. Ancak, tüm işleri bu şekilde yapmak uygun olmayabilir.
CoroutineExceptionHandler Kullanımı:

CoroutineExceptionHandler kullanılarak bir hata yönetimi stratejisi tanımlanır. Bu strateji, hata oluştuğunda belirtilen işlemleri gerçekleştirir. İki coroutine başlatılır, ancak birinde hata oluştuğunda diğerinin çalışması durur.
supervisorScope Kullanımı:

supervisorScope kullanılarak hata yönetimi. İki coroutine başlatılır, ancak birinde hata oluştuğunda diğerinin çalışması devam eder.
CoroutineScope ile CoroutineExceptionHandler:

CoroutineScope kullanılarak, belirli bir dispatcher üzerinde çalışan bir coroutine başlatılır ve CoroutineExceptionHandler kullanılarak hata yönetimi sağlanır.
Bu örneklerde, coroutine'lerin nasıl başlatılacağı, hata durumlarının nasıl yönetileceği ve farklı hata yönetimi stratejilerinin nasıl uygulanacağı gösterilmektedir.
