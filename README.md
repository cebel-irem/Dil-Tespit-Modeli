#  Dil Tespit Modeli
Bu proje, kullanıcıdan alınan veya veri setinden gelen metinlerin **hangi dile ait olduğunu otomatik olarak tespit edebilen** bir makine öğrenimi modelini içermektedir. Birden fazla model eğitilip karşılaştırmalı performans analizleri yapılmış, en iyi sonuç veren modelle canlı tahmin yapılabilir hale getirilmiştir.

## Projenin Amacı

Amaç, verilen bir metnin hangi dilde yazıldığını yüksek doğrulukla tahmin edebilen bir sınıflandırma modeli geliştirmektir. Bu amaçla farklı makine öğrenmesi algoritmaları denenmiş, başarı oranları karşılaştırılmıştır.

## Geliştirme ve Test Ortamı

* **Ortam:** Google Colab (T4 GPU aktif)
* **Python Sürümü:** 3.10
* **Kütüphaneler:**

  * `pandas`
  * `numpy`
  * `scikit-learn`
  * `matplotlib`
  * `seaborn`
  * `re`
  * `time`

> Kurulum için:

```bash
pip install -r requirements.txt
```

##  Veri Seti Bilgileri

* **Kaynak:** Kaggle - Language Detection Dataset (CSV formatında)
* **Sütunlar:** `Text`, `Language`
* **Dil Sayısı:** 20
* **Toplam Satır:** 20.000+
* **Ön İşleme:**

  * Noktalama işaretleri kaldırıldı
  * Tüm metinler küçük harfe çevrildi
  * 3 kelimeden az cümleler uyarı vererek tahmine dahil edildi
  * TF-IDF ile karakter tabanlı `n-gram` vektörleştirme yapıldı



## Kullanılan Modeller

Aşağıdaki modeller eğitildi, test edildi ve karşılaştırıldı:

1. **Multinomial Naive Bayes**
2. **Logistic Regression**
3. **Random Forest Classifier**
4. **Linear SVC**

> Eğitim süreleri ve başarı oranları analiz raporuna dahil edilmiştir.

---

## Sonuçlar

* Her modelin doğruluk oranı, eğitim süresi ve test sonuçları karşılaştırmalı olarak analiz edilmiştir.
* En başarılı model, gerçek zamanlı dil tespiti için seçilmiş ve kullanıcı girişine entegre edilmiştir.


## Kullanım

1. Projeyi Google Colab veya VS Code ortamında açın

2. Gerekli kütüphaneleri yükleyin:

   ```bash
   pip install -r requirements.txt
   ```

3. Veri seti yolu Colab dışındaki çalıştırmalarda manuel olarak ayarlanmalıdır.
   Kod içinde yorum satırı olarak eklenmiştir → yorum satırını aktif hale getirin.

4. Son olarak, dosyayı çalıştırmak için:

   * Google Colab'da: `Runtime > Run All`
   * VS Code'da: `F5` veya terminalden çalıştır

