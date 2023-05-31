# PCA (Principal Component Analysis)

Çok uzun boyutlarda alan içeren veriniz var ve bu veriler gerek önişleme (preprocessing), gerek eğitim (training) ve gerekse tahmin (predict) aşamalarında gerek süre açısından gerekse de işlem maliyetleri açısından maliyetler oluşturabilmektedir. İşte PCA analizi tam da burada devreye girmektedir. Şimdi genel tanımlamalarına değinerek gerçek bir örnek üzerinde çalışma yapalım.
 
**PCA (Temel Bileşen Analizi)**,  özellikle denetimsiz öğrenme uygulamalarında sıklıkla kullanılan bir boyut küçültme (dimension reduction) algoritmasıdır. Bu algoritma veri kümesi üzerinde ki yararsız alanların çıkarılarak verinin optimize edilmesini sağlar. Şimdiden duyar gibiyim : “Peki bu durum doğruluk açısından modelin performansını etkilemez mi?” . Evet, az/çok etkiler. Bunların hepsine değineceğiz. 

# Peki neden PCA algoritmasını kullanmalıyız?

Öncelikle modeli gürültülü verilerden arındırarak probleme daha iyi odaklanmasını sağlamak için.
Buyutta azalmalar ile modelin train ve predict aşamalarında ki işlem hızını azaltmak için.
Veriyi yorumlama ve görselleştirme aşamasında daha basit ve okunaklı sonuçlar almak için.
Tabii ki bence en önemlisi verideki değişkenler arasındaki ilişkinin tespit edilmesi için. Verideki değişkenler arasındaki ilişkinin tespiti, modelin tüm aşamalarında (preprocessing, train, predict)  performansı etkileyecektir.

# Peki, PCA algoritması nasıl çalışır?

PCA, bir veri kümesinin gerçek boyutunu tanımlar. Yani doğru bir tahmin yapmak için gereken en az sayıda özelliğin tanımlanmasını sağlar. Hepinizin bildiği üzere bir veri kümesinde birçok özellik olabilir. Fakat bu özelliklerin ne kadarı tahminlerde etkilidir ne kadarının ise bir etkisi bulunmamaktadır? Bu önemlidir çünkü gürültülü özellikler hem tahmin (predict) performansını hem de işlem maliyeti performansını olumsuz yönde etkiler. Az sayıda özellik barındıran veriler için bu durum önemsiz gibi görünsede yüzlerce hatta belki binlerce özelliği barındıran veri kümeleri için büyük öneme sahiptir.

Öncelikle PCA analizi sonucunda tutulan özellikler, önemli varyansa (ilişki) sahip olan özelliklerdir. BAzı teknik terimlerinde üzerinden kısaca geçerek gerçek bir örnek üzerinde çalışmaya başlayalım. PCA:

**Verilerin daha düşük boyutlu bir uzaya doğrusal eşlenmesi ve varyansın en üst düzeye çıkarılması şeklinde gerçekleşir.**
**Düşük varyansa sahip özelliklerin alakasız olduğunu ve yüksek varyansa sahip özelliklerin bilgilendirici olduğunu varsayar.**

# Önceden bir hazırlık gerekir mi ?

Veri üzerinde normalizasyon yapmak her durumda gerektiği gibi burada da bazı adımlar uygulanması gerekmektedir. Öncelikle veri sayısallaştırılmalı ve Encoding (Label Encoder, One Hot Encoder) işlemleri gerçekleştirilmiş olmalıdır. Ayrıca verinin ölçeklenmesi de gerekmektedir.

Bu çalışmada StandardScaler kullanarak veriler ölçeklendirilcektir. StandardScaler, her özelliğin μ = 0 ve σ = 1 olması için ortalamayı kaldırarak ve varyansı birim varyansa ölçeklendirerek özellikleri standartlaştıracaktır. 

Gerekli teorik bilgilere değindikten sonra artık örnek uygulamamıza başlayabilir, sonuçları karşılaştırabiliriz.

Yazı serisinin tamamını okumak için [tıklayınız](https://www.brain-tr.com/pca-principal-component-analysis-kullanarak-boyut-azaltma-nasil-gerceklestirilir/).

Notebook dosyası için [tıklayınız](https://github.com/tr-brain-com/pca/blob/main/pca.ipynb).

