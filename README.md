# Analisis Sentimen Publik Terkait Pelemahan Rupiah terhadap Dolar AS Menggunakan Algoritma Naive Bayes

Kondisi perekonomian saat ini menghadapi tantangan yang cukup signifikan, khususnya terkait fluktuasi dan melemahnya nilai tukar Rupiah terhadap Dolar AS. Isu ini memicu berbagai reaksi dan opini dari masyarakat luas yang tersebar di media sosial, salah satunya platform YouTube. Strategi pengambilan keputusan atau pemahaman terhadap respons publik seringkali terhambat karena data opini masyarakat masih berupa teks tidak terstruktur dengan banyak *noise* berupa emoji, tag HTML, simbol, dan ragam bahasa gaul (slang). Oleh karena itu, perlu dilakukan ekstraksi dan transformasi dari ribuan komentar mentah tersebut menjadi sebuah wawasan sentimen publik yang terstruktur agar mempermudah pemetaan opini masyarakat secara nyata dan terukur.

Maka saya melakukan analisis sentimen menggunakan algoritma Naive Bayes untuk melihat klasifikasi dan distribusi opini masyarakat Indonesia terkait isu ekonomi ini. Mengapa saya menggunakan algoritma Naive Bayes dan pendekatan pemrosesan bahasa alami (NLP) ini, dikarenakan metode tersebut sangat efektif dan efisien dalam mengklasifikasikan teks dalam jumlah besar menjadi probabilitas kategori yang terstruktur (Positif, Netral, Negatif). Dengan metode ini, saya dapat membersihkan *noise* pada data mentah dan membakukan ragam bahasa nonformal agar bermakna, sehingga hasil analisis tidak hanya berisi asumsi, melainkan metrik persentase sentimen publik yang dihitung secara eksplisit berdasarkan frekuensi kata kunci yang sesungguhnya.

Asumsi utama dalam projek ini yaitu opini masyarakat yang diekstrak dari kolom komentar YouTube dapat merepresentasikan sentimen publik secara umum terkait nilai kurs Rupiah, sehingga dapat dikombinasikan sedemikian rupa untuk menghasilkan klasifikasi opini yang objektif. Diasumsikan pula penggunaan kamus khusus *stopwords* dan *slang* dalam konteks kurs mata uang keakuratannya lebih tinggi dalam mempresentasikan makna komentar dibandingkan metode *preprocessing* teks tradisional.

# Import Library & Tech Stack

Ekstraksi, transformasi, dan analisis pada projek ini dibangun menggunakan *Tech Stack* berikut:

* **Python (Pandas, NumPy, Google API Client):** Digunakan untuk ekstraksi data (*scraping*) secara langsung dari YouTube, transformasi tipe data, serta manipulasi dan pembersihan *dataframe*.
* **NLTK & Sastrawi:** Digunakan untuk *Natural Language Processing* (NLP), mencakup tokenisasi, penghapusan *stopwords*, dan *stemming* yang dirancang khusus untuk bahasa Indonesia.
* **Matplotlib, Seaborn & WordCloud:** Digunakan untuk visualisasi data eksploratif (EDA) guna memetakan hasil analisis.

# Pengumpulan Data (Scraping)

Data dikumpulkan melalui proses *scraping* menggunakan **YouTube Data API v3**. Proses ini menghasilkan ribuan data teks komentar mentah (tidak terstruktur) yang masih mengandung elemen-elemen yang tidak relevan untuk analisis bahasa.

# Preprocessing

Pendekatan *preprocessing* dilakukan secara komprehensif untuk memastikan model klasifikasi dapat membaca data yang bersih dan bermakna:

* **Comprehensive Text Preprocessing:** Membersihkan teks dari elemen yang tidak relevan seperti URL, tag HTML, emoji, angka, dan simbol, serta mengaplikasikan *case folding* untuk menormalisasi seluruh huruf besar menjadi huruf kecil.
* **Slang Normalization & Stemming:** Menerjemahkan ragam bahasa nonformal dan singkatan (misal: "krna" menjadi "karena", "jgn" menjadi "jangan") menggunakan kamus khusus agar bermakna. Proses ini dilanjutkan dengan *stemming* menggunakan *library* Sastrawi untuk mengembalikan setiap kata ke bentuk dasarnya.
* **Tokenization & Stopword Removal:** Memecah teks menjadi unit-unit kata tunggal (token) dan mengeliminasi *stopwords* (kata hubung yang tidak berkontribusi signifikan) yang daftar eliminasi-nya telah disesuaikan khusus dengan konteks kurs mata uang.

# Key Insights (Hasil Temuan)

Berdasarkan penerapan model Naive Bayes pada dataset yang telah dibersihkan, didapatkan temuan strategis sebagai berikut:

* **Dominasi Sentimen Negatif:** Opini masyarakat Indonesia di YouTube sangat didominasi oleh komentar berupa pertanyaan atau pernyataan bernada negatif terkait nilai kurs Rupiah yang melemah.
* **Distribusi Sentimen Publik:** Meskipun sentimen negatif memimpin dengan telak, klasifikasi data juga menunjukkan adanya sejumlah sentimen netral (berkisar di angka setengah dari total sentimen negatif). Porsi kelompok netral ini terbukti jauh lebih besar dibandingkan dengan kelompok sentimen positif yang berada di urutan terakhir.

# Visualisasi Data Eksploratif (EDA)

Tahap ini memuat eksplorasi persentase kelas sentimen (Negatif, Netral, Positif) yang divisualisasikan menggunakan *bar chart* dan *pie chart* dari Matplotlib dan Seaborn, serta pemetaan kumpulan frekuensi kata kunci yang paling banyak diperbincangkan oleh masyarakat menggunakan *WordCloud*.

---

*Tertarik dengan proses dan penulisan kode analisis di balik layar?*
Silakan telusuri langsung melalui Jupyter Notebook di repositori ini. Jika Anda memiliki *feedback*, masukan, atau ingin berdiskusi mengenai peluang kolaborasi dan karir di bidang data, mari terhubung melalui [LinkedIn Saya](https://www.linkedin.com/in/deswita-nur-ardias-farsha-53a251284?utm_source=share_via&utm_content=profile&utm_medium=member_android) atau jangkau saya melalui email di **deswitanaf.work@gmail.com**.
