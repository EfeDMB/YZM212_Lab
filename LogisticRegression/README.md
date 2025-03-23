  #Logistic Regression
 ##1. Proje Açıklaması
Bu proje, kredi geri ödememe (loan default) durumlarını tahmin etmek için Logistic Regression yöntemini kullanmaktadır.

Veri seti: Kaggle - Loan Default Dataset

Örnek sayısı: 25,535

Özellik sayısı: 10

Hedef: Kredi geri ödememe durumunu (1: Ödemedi, 0: Ödedi) tahmin etmek

İki farklı model oluşturulmuştur:

Scikit-learn Logistic Regression modeli

Özel olarak geliştirilmiş Logistic Regression modeli (Maksimum Likelihood ve Gradient Descent kullanılarak)

Bu iki modelin performansları karmaşıklık matrisi (confusion matrix) ve çalışma süreleri üzerinden karşılaştırılmıştır.

##3. Veri Analizi
Sınıf Dağılımı: Kredi geri ödememe durumu dengesizdir.

Özellik Türleri: Kategorik değişkenler kaldırılarak sadece sürekli değişken içermesi sağlanmıştır.

Eksik Veriler: Eksik veri yoktur
##4. Model Açıklamaları
#Scikit-learn Logistic Regression Modeli
Scikit-learn'ün LogisticRegression sınıfı kullanılmıştır.

Varsayılan parametrelerle çalıştırılmıştır.

#Özel Logistic Regression Modeli
Maksimum Likelihood Estimation (MLE) tabanlı maliyet fonksiyonu kullanılmıştır.

Gradient Descent ile optimizasyon yapılmıştır.

Öğrenme oranı ve iterasyon sayısı deneysel olarak belirlenmiştir.

##5. Model Karşılaştırması
Aşağıda iki modelin performans metrikleri ve çalışma süreleri verilmiştir.

Model	Accuracy	Precision	Recall	F1 Score	Eğitim Süresi (s)	Tahmin Süresi (s)
Özel Logistic Regression	0.5704	0.1793	0.7636	0.2904	1.65303	0.00043
Scikit-learn Logistic Regression	0.8847	0.5000	0.0272	0.0515	0.00817	0.00034
#Sonuçların Yorumlanması
Scikit-learn modeli, doğruluk (accuracy) açısından daha iyi performans gösteriyor (0.88 vs. 0.57).

Özel modelin recall değeri çok yüksek (0.76), ancak precision değeri çok düşük (0.18).

Scikit-learn modelinde ise precision yüksek (0.50), ancak recall çok düşük (0.027).

Eğitim süresi açısından Scikit-learn modeli çok daha hızlı.
##6. Tartışma ve Sonuç
Kredi geri ödememe (loan default) gibi dengesiz veri içeren problemler için sadece doğruluk (accuracy) tek başına yeterli bir ölçüt değildir.

Bu tür problemlerde önemli metrikler şunlardır:

Recall (Duyarlılık) → Kredi ödemeyen müşterileri doğru şekilde tespit etme yeteneği.

Precision (Kesinlik) → Ödememe olarak tahmin edilenlerin gerçekten ödemediğini gösterme oranı.

Scikit-learn modeli yüksek doğruluk sunarken recall değeri çok düşük. Bu, kredi ödemeyecek kişileri tespit etmede başarısız olduğu anlamına gelir. Gerçek hayatta bankalar için recall değeri çok kritik çünkü ödeme yapmayacak müşterileri kaçırmak büyük maddi kayıplara yol açabilir.
