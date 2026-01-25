# Decision Tree Classification – Bank Personal Loan Modelling

Bu proje, **Bank Personal Loan Modelling** veri seti kullanılarak bir **ikili sınıflandırma (binary classification)** problemi üzerinde **Decision Tree (Karar Ağacı)** algoritmasının uygulanmasını kapsamaktadır. Çalışmada veri analizi, model eğitimi, hiperparametre optimizasyonu, model karşılaştırması ve kapsamlı görselleştirmeler yer almaktadır. Proje, makine öğrenmesi sınıflandırma süreçlerini uçtan uca göstermek amacıyla bir **Jupyter Notebook** ortamında hazırlanmıştır.

---

## Proje Amacı

Bu çalışmanın temel amaçları şunlardır:

* Banka müşterilerinin **kişisel kredi (Personal Loan)** alıp almayacağını tahmin etmek
* Decision Tree algoritmasının sınıflandırma performansını incelemek
* Hiperparametre optimizasyonunun model başarısına ve genelleme yeteneğine etkisini analiz etmek
* Aşırı öğrenme (overfitting) problemini tespit etmek ve azaltmak
* Karar ağacı yapısını ve model sonuçlarını görselleştirerek yorumlamak

---

## Kullanılan Algoritma: Decision Tree Classifier

**Decision Tree (Karar Ağacı)** algoritması, veriyi özelliklere göre dallara ayırarak karar kuralları oluşturan denetimli bir öğrenme yöntemidir. Bu projede:

* Sınıflandırma problemi için `DecisionTreeClassifier` kullanılmıştır
* Bölünme kalitesi **Gini** ve **Entropy** kriterleri ile değerlendirilmiştir
* Ağaç derinliği ve yaprak koşulları kontrol edilerek model karmaşıklığı yönetilmiştir

---

## Proje Akışı

Notebook içerisinde aşağıdaki adımlar izlenmiştir:

1. Gerekli kütüphanelerin yüklenmesi
2. Veri setinin okunması ve incelenmesi
3. Gereksiz sütunların (ID) çıkarılması
4. Keşifsel veri analizi (info, describe)
5. Bağımlı ve bağımsız değişkenlerin ayrılması
6. Eğitim ve test verilerinin oluşturulması
7. İlk (kısıtsız) Decision Tree modelinin eğitimi
8. Model performansının değerlendirilmesi
9. GridSearchCV ile hiperparametre optimizasyonu
10. Orijinal ve optimize edilmiş modellerin karşılaştırılması
11. Karar ağacı, doğruluk, karmaşıklık ve özellik önemlerinin görselleştirilmesi

---

## Kullanılan Teknolojiler ve Kütüphaneler

* Python
* Jupyter Notebook
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

## Kurulum ve Çalıştırma

Repoyu klonlayın:

```bash
git clone https://github.com/isil-ada/Decision-Tree-Personal-Loan.git
```

Proje dizinine girin:

```bash
cd Decision-Tree-Personal-Loan
```

Jupyter Notebook’u başlatın:

```bash
jupyter notebook
```

Ardından notebook dosyasını açarak hücreleri sırasıyla çalıştırın.

---

## Model Değerlendirme

Model performansı aşağıdaki metriklerle değerlendirilmiştir:

* Accuracy (Doğruluk)
* Confusion Matrix
* Precision ve Recall
* Classification Report

İlk eğitilen model ile hiperparametre optimizasyonu sonrası elde edilen model karşılaştırılmıştır.

---

## Hiperparametre Optimizasyonu

GridSearchCV kullanılarak aşağıdaki parametreler optimize edilmiştir:

* `max_depth`
* `min_samples_split`
* `min_samples_leaf`
* `criterion`

Bu sayede modelin genelleme yeteneği artırılmış ve aşırı öğrenme azaltılmıştır.

---

## Overfitting Analizi

* Eğitim ve test doğrulukları karşılaştırılmıştır
* Eğitim-test farkı (train-test gap) hesaplanmıştır
* Optimize edilmiş modelin daha dengeli sonuçlar verdiği gözlemlenmiştir

---

## Görselleştirmeler

Proje kapsamında aşağıdaki görselleştirmeler oluşturulmuştur:

* Orijinal ve optimize edilmiş karar ağaçlarının karşılaştırılması
* Eğitim ve test doğruluklarının bar grafiği
* Confusion Matrix ısı haritası
* Özellik önem (Feature Importance) grafiği

Bu görseller modelin karar mekanizmasını daha anlaşılır hale getirmektedir.

---

## Feature Importance

Optimize edilmiş Decision Tree modeli kullanılarak hangi özelliklerin kredi tahmininde daha etkili olduğu analiz edilmiştir. Bu analiz, bankacılık ve finans alanında karar destek sistemleri için önemli içgörüler sunmaktadır.

---

## KNN ile Karşılaştırma

Bu projede kullanılan **Decision Tree** algoritması, daha önce uygulanan **K-Nearest Neighbors (KNN)** algoritması ile karşılaştırıldığında:

| Kriter                 | Decision Tree                 | KNN                                      |
| ---------------------- | ----------------------------- | ---------------------------------------- |
| Model Yapısı           | Kural tabanlı, yorumlanabilir | Mesafe tabanlı, yorumlanabilirliği düşük |
| Eğitim Süresi          | Hızlı                         | Hızlı                                    |
| Tahmin Süresi          | Çok hızlı                     | Yavaş (tüm veri ile mesafe hesabı)       |
| Ölçeklendirme İhtiyacı | Yok                           | Gerekli                                  |
| Overfitting Riski      | Yüksek (kontrol edilmezse)    | Orta                                     |
| Feature Importance     | Var                           | Yok                                      |

Decision Tree modeli, özellikle **yorumlanabilirlik** ve **özellik önemlerinin çıkarılması** açısından KNN’ye göre avantaj sağlamaktadır. KNN ise küçük veri setlerinde ve düzgün ölçeklendirilmiş verilerde etkili sonuçlar verebilmektedir.

---

## Sonuç

Bu proje, Decision Tree algoritmasının sınıflandırma problemlerinde nasıl etkin şekilde kullanılabileceğini, hiperparametre optimizasyonu ve görselleştirmelerle detaylı biçimde ortaya koymaktadır. Bankacılık gibi kararların açıklanabilirliğinin önemli olduğu alanlarda Decision Tree algoritması güçlü bir alternatiftir.

📎 **Not:** Bu proje öğrenme amacıyla hazırlanmıştır.
