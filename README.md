# NLP_project
# Projeyi Yapanlar
- Okan Kocabaşoğlu  213405043
## Haber Metinlerini Özetleme
- Bu proje TF-IDF vektorizer kullanarak haber metinlerini özetler.
## Kullanılan Kütüphaneler
- BeautifulSoup
- requests
- pandas
- numpy
- re
- TfidfVectorizer
- simplemma
- nltk
# Veri Setinin Oluşturulması
Veri seti dunyahalleri.com 'dan requests ve BeautifulSoup kütüphaneleri kullanılarak oluşturulmuştur.
![](https://github.com/Okan27k/NLP_project/blob/main/jpgs/jpg1.jpg?raw=true)
- Görselde web sitesinin istediğimiz urllerini çektiğimiz kod var.
- Yaklaşık 800 url çektim.
- Metin özeti çalışması yaptığım için çok büyük bir veri setine ihtiyacım olmadı.
 
![](https://github.com/Okan27k/NLP_project/blob/main/jpgs/jpg2.jpg?raw=true)
- Bu görseldeki kodda web sitesinin html kodlarını inceleyerek elde ettiğim class bilgilerini kullanarak haber metinlerini çektim.


# Metinlerin Temizlenmesi

![](https://github.com/Okan27k/NLP_project/blob/main/jpgs/jpg3.jpg?raw=true)
- Metinde TF-IDF vectorizeri etkileyecek stop words, noktalama işaretleri, istenmeyen bazı metinleri(Haber ÖzetiTam Sürüm gibi) vb. temizledik.
# Metin Özetleyici
![](https://github.com/Okan27k/NLP_project/blob/main/jpgs/jpg4.jpg?raw=true=)
- Cümle puanı bir cümlenin vektörünün puanını hesaplayıp, 0dan farklı olan öğeleri filtreler ve bu öğelerin ortalamasını alır, ortalamayı döndürür. Yani cümlemize skor atamış olur.
- Metin özetle fonksiyonu önce metni cümlelere ayırır, temizleme fonksiyonuna yollar, temizledikten sonra da TF-IDF vectorizerla cümleleri vektörleştirir.
- Her cümlenin vektörünü cümle_puanı fonksiyonuna yollar.
- Puanlara göre cümlelerin sırasını belirleyip belirtilen cümle sayısına (cumle_sayisi) göre özet oluşturur.

## Sonuç
![image](https://github.com/Okan27k/NLP_project/assets/116784940/f3e3968f-d285-4d19-bf11-08e084272a90)

![](https://github.com/Okan27k/NLP_project/blob/main/jpgs/jpg6.jpg?raw=true)
- Bu görselde kullanıcıdan haber indexi ve kaç cümlede özetleneceğinin girilmesi istenir ve altında da özetlenmiş bir örnek vardır.
- Headline kısmını kullanıcın biraz olsun kıyaslama yapabilmesi için ekledim.
- Üstteki iki görselde metin özetleri idare eder.
![](https://github.com/Okan27k/NLP_project/blob/main/jpgs/jpg7.jpg?raw=true)
- Bu görselde de başarısız bir özet görüyoruz.
- TF-IDF ile özet yöntemi çok komplike bir yöntem olmadığı için çok başarılı bir özet çıkarmadı. Çünkü TF-IDF belirli bir belgedeki terimlerin önemini belirler bu da mantıklı bir özet çıkarmak için tek başına yeterli olmayabiliyor.
- Abstractive metin özetleme yöntemleri gibi kendi bir yazı oluşturmuyor. Zaten var olan cümleleri önem sırasına göre yazdırıyor.

