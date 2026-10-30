# Analisis-Sentimen-pada-Youtube-Terkait-Melemahnya-Nilai-Tukar-Rupiah-Terhadap-Dolar-
End-to-end data analysis and clustering of Sentimen pada Youtube Terkait Melemahnya Nilai Tukar Rupiah Terhadap Dolar  using Python and K-Prototypes.
Mengubah ribuan komentar mentah dari YouTube menjadi wawasan sentimen publik yang terstruktur. Proyek ini menganalisis opini masyarakat Indonesia terkait melemahnya nilai tukar Rupiah terhadap Dolar AS menggunakan algoritma Naive Bayes.

Data dikumpulkan melalui proses *scraping* menggunakan YouTube Data API v3, yang menghasilkan data teks tidak terstruktur dengan banyak *noise* berupa emoji, tag HTML, simbol, dan ragam *slang* (bahasa gaul). Pendekatan Saya:

* **Comprehensive Text Preprocessing:** Membersihkan teks dari elemen yang tidak relevan seperti URL, tag HTML, emoji, angka, dan simbol, serta mengaplikasikan *case folding* untuk menormalisasi huruf besar menjadi huruf kecil.


* **Slang Normalization & Stemming:** Menerjemahkan ragam bahasa nonformal dan singkatan (misal: "krna" menjadi "karena", "jgn" menjadi "jangan") menggunakan kamus khusus agar bermakna, dilanjutkan dengan proses *stemming* menggunakan *library* Sastrawi untuk mengembalikan kata ke bentuk dasarnya.


* **Tokenization & Stopword Removal:** Memecah teks menjadi unit-unit kata (token) dan mengeliminasi *stopwords* (kata hubung yang tidak berkontribusi signifikan) yang disesuaikan khusus dengan konteks kurs mata uang.



Didapatkan temuan (Key Insights) dari projek ini adalah:

* **Dominasi Sentimen Negatif:** Opini masyarakat Indonesia di YouTube sangat didominasi oleh komentar berupa pertanyaan atau pernyataan bernada negatif terkait nilai kurs Rupiah.


* **Distribusi Sentimen Publik:** Meskipun sentimen negatif memimpin dengan telak, terdapat juga sejumlah sentimen netral (sekitar setengah dari total sentimen negatif), yang porsinya terbukti lebih besar dibandingkan dengan kelompok sentimen positif.



Tech Stack & Tools yang digunakan pada projek ini ialah:

* **Python (Pandas, NumPy, Google API Client):** Ekstraksi data (*scraping*) langsung dari YouTube, transformasi tipe data, dan pembersihan *dataframe*.


* **NLTK & Sastrawi:** *Natural Language Processing* (NLP) untuk tokenisasi, penghapusan *stopwords*, dan *stemming* khusus bahasa Indonesia.


* **Matplotlib, Seaborn & WordCloud:** Visualisasi data eksploratif (EDA) untuk melihat perbandingan kelas sentimen (Negatif, Netral, Positif) secara persentase serta memetakan kumpulan frekuensi kata kunci (WordCloud) dari opini masyarakat.



Tertarik dengan proses analisis di balik layar? Silakan telusuri Jupyter Notebook di repositori ini. Jika Anda memiliki *feedback* atau ingin berdiskusi mengenai peluang kolaborasi dan karir di bidang data, mari terhubung melalui LinkedIn saya ([https://www.linkedin.com/in/deswita-nur-ardias-farsha-53a251284?utm_source=share_via&utm_content=profile&utm_medium=member_android](https://www.linkedin.com/in/deswita-nur-ardias-farsha-53a251284?utm_source=share_via&utm_content=profile&utm_medium=member_android)) atau email saya deswitanaf.work@gmail.com.
