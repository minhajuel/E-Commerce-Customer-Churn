# E-commerce-Customer-Churn
Purwadhika Capstone project

#### **Outline**
1. Business Problem
2. Data Understanding
3. Exploratory Data Analysis
4. Data Preparation
5. Modeling
6. Conclusion and Recommendation

**Context**

Tim Marketing dari sebuah perusahaan E-Commerce X ingin melakukan evaluasi terhadap terjadinya "Customer Churn", yaitu pelanggan yang berhenti menggunakan layanan atau membeli produk di platform E-Commerce X. Jika dibiarkan, customer churn akan menyebabkan E-Commerce X kehilangan pelanggannya, yang berarti kehilangan pendapatan dan harus mencari pelanggan baru. Hal ini tentu akan menyebabkan kerugian besar bagi E-Commerce X, sebab **cost untuk mencari pelanggan yang baru memakan biaya lima kali lebih mahal** daripada menjaga pelanggan yang sudah ada. Maka dari itu pentingnya untuk menjaga customer agar tetap loyal.

**Problem Statement**

"Customer Churn" merupakan masalah yang signifikan dalam bisnis. Salah satu strategi yang dapat diterapkan oleh E-Commerce X adalah melakukan pendekatan melalui promosi khusus bagi pelanggan E-Commerce X. Namun jika promosi diberikan kepada semua pelanggan akan tidak efisien apabila yang menerima promosi tersebut adalah pelanggan yang ternyata tidak berpotensi churn, sebab tanpa diberi promosi pun mereka tetap akan menggunakan layanan. Maka itu promosi khusus harus diprioritaskan kepada pelanggan yang berpotensi akan churn. 

**Goals**

Berdasarkan permasalahan sebelumnya, E-Commerce X perlu memprediksi pelanggan yang berpotensi churn. Dengan mengetahui pelanggan mana yang berpotensi churn beserta faktor apa yang menyebabkan pelanggan churn, perusahaan dapat membuat strategi yang tepat untuk mempertahankan pelanggan dengan biaya yang lebih efisien.

**Pendekatan Analitis**

Pendekatan analitis adalah membuat, mengevaluasi, dan mengimplementasikan model *machine learning* klasifikasi yang dapat memprediksi apakah pelanggan akan *churn* atau tidak berdasarkan riwayat data yang ada. 

Target:   
0 : Pelanggan tidak *churn*  
1 : Pelanggan *churn*


**Metrik Evaluasi**

- **True Positive (TP)**: Pelanggan diprediksi churn dan kenyataannya churn.
- **False Positive (FP)**: Pelanggan diprediksi churn, namun kenyataannya tidak churn.
- **True Negative (TN)**: Pelanggan diprediksi tidak churn dan kenyataannya tidak churn. 
- **False Negative (FN)**: Pelanggan diprediksi tidak churn, namun kenyataannya churn.

Dalam melakukan prediksi, kesalahan yang dapat terjadi yaitu:

**Type 1 error** : False Positive  
Konsekuensi: Biaya promosi terbuang percuma

**Type 2 error** : False Negative  
Konsekuensi: Kehilangan pelanggan 

Berdasarkan konsekuensinya, model yang dibuat akan lebih **menekankan untuk dapat mengurangi False Negative**, sebab konsekuensi kehilangan pelanggan (False Negative) lebih merugikan karena cost untuk mencari pelanggan baru untuk menggantikan pelanggan yang *churn* akan memakan biaya lima kali lebih mahal. 

Namun promosi untuk menjaga pelanggan agar tidak churn harus dilakukan dengan tepat agar biaya promosi tidak terbuang percuma (False Positive). Maka itu metric yang digunakan adalah **F2 Score**. F2 score dapat digunakan untuk mengevaluasi performa model klasifikasi di mana kesalahan false negative lebih penting untuk dihindari daripada false positive.


Struktur dari project analisis ini yaitu:

  ├── README.md <- Berisi latar belakang dan pernyataan masalah yang harus dijawab.
  ├── docs <- berisi dokumen pendukung.
  ├── model <- final model
  ├── src <- code dan data set yang digunakan untuk project .
  └── requirements.txt <- The requirements file untuk memproduksi analysis environment, e.g. generated with `pipreqs > requirements.txt`