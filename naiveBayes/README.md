  # Naive Bayes Projesi

 ## Problem Tanımı

Bu proje, Naive Bayes yöntemini kullanarak ikili sınıflandırma yapmayı amaçlamaktadır. Proje kapsamında, Scikit-learn kütüphanesinden bir Naive Bayes sınıfı kullanarak eğitim ve test işlemleri yapılacaktır. Ayrıca, aynı veri seti üzerinde bir Python sınıfı olarak yazılmış özelleştirilmiş Naive Bayes modeli ile karşılaştırma yapılacaktır.

 ## Veri
Veri, kalp hastalığı tahmini üzerine çalışılan bir tabular veri kümesidir. Veri seti, çeşitli özelliklere sahip bireylerin kalp hastalığına sahip olup olmadığını sınıflandırmaktadır.

 ## Yöntem
Bu projede, Gaussian Naive Bayes algoritması kullanılmıştır. Modelin doğruluğu Accuracy, Precision, Recall, ve Specificity gibi metrikler ile değerlendirilmiştir. Bunlar:

-Accuracy : Modelin tüm tahminleri içinde doğru tahminlerin oranıdır.

-Precision : Modelin pozitif tahminleri arasında ne kadarının gerçekten pozitif olduğunu gösterir.

-Recall : Modelin pozitif sınıf tahminlerinde ne kadar doğru olduğunu gösterir

-Specificity : Modelin negatif örnekleri doğru şekilde tespit etme oranıdır.

 ## Sonuçlar
Modelin performansı aşağıdaki gibidir:

Accuracy    0.8967

Precision   0.9109

Recall  0.9020

Specificity 0.8902

 ## Yorum / Tartışma
Modelin doğruluğu iyi seviyededir ancak yanlış negatif sonuçların sayısını azaltmak için farklı metrikler (örneğin, recall) göz önünde bulundurulabilir. Ayrıca, modelin geliştirilmesi için farklı sınıflandırıcılar da denenebilir.

 ## Kaynakça
https://www.kaggle.com/code/tarekfathalla17/heart-failure-prediction 
sklearn 1.3.0 - pandas 2.1.4 - numpy 1.24.3

