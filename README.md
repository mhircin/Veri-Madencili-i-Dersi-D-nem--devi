# Veri-Madencili-i-Dersi-D-nem--devi
Veri Madenciliği Dersi Dönem Ödevi
Konu: Telco Müşteri Kaybı (Churn) Analizi ve Tahminleme
Araç: Orange Data Mining Tool


1.	KISIM: Veriyi Tanıma ve Hazırlama (Preprocessing & EDA)
Ödevin Amacı: Ham veriyi işlenebilir hale getirmek ve görsel analizlerle müşteri profilini ortaya çıkarmak.

Yapılan İşlemler (Workflow Adımları):
1.	Veri Yükleme: Datasets widget'ını kullanarak "Telco Customer Churn" veri setini yüklendi.
2.	Veri Denetimi: Data Table ile veriye bakılıp. TotalCharges sütunundaki sayısal değerlerin neden "text" olarak algılandığını tespit edildi.
3.	Temizlik (Preprocess): * Impute widget'ı ile boş (NaN) değerleri ortalama (mean) ile dolduruldu.
o	Select Columns ile tahminleme için anlamsız olan customerID sütununu devre dışı bırakıldı.
4.	Görsel Analiz (EDA):
o	Distributions widget'ını kullanılarak: "Sözleşme tipi (Contract)" ile "Ayrılma (Churn)" arasındaki ilişkiyi gösteren grafik oluşturuldu.
o	Scatter Plot kullanılarak: "Aylık Ödeme (MonthlyCharges)" ve "Müşteri Sadakati (Tenure)" arasındaki ilişki Churn bazlı renklendirerek analiz edildi.

2. KISIM: Tahminleme ve Model Değerlendirme (Modeling & Evaluation)
Ödevin Amacı: Hazırlanan temiz veriyi kullanarak, bir müşterinin şirketi terk edip etmeyeceğini önceden tahmin eden yapay zeka modelleri kurmak.

Yapılan İşlemler (Workflow Adımları):
1.	Veri Ayırma: Data Sampler widget'ını kullanarak veri %80 Eğitim (Training) ve %20 Test (Testing) olarak ikiye bölündü.
2.	Model Kurma: Veri aynı anda şu üç farklı algoritmaya bağlandı:
o	Logistic Regression
o	Decision Tree (Karar Ağacı)
o	Random Forest
3.	Performans Ölçümü: Modeller Test and Score widget'ına bağlandı. "AUC" ve "Classification Accuracy" değerleri karşılaştırıldı.
4.	Hata Analizi: En iyi çalışan model için Confusion Matrix (Karmaşıklık Matrisi) oluşturuldu. Kaç müşterinin "ayrılacak" denmesine rağmen "kaldığı" (False Positive) bulundu.
5.	Görsel Model: Tree Viewer widget'ı ile Karar Ağacı'nın hangi kriterlere göre (örneğin: Fiber internet mi, Sözleşme süresi mi?) karar verdiği görselleştirildi

