# Kredi Hesaplama (GANO-DANO) 🎓

**Türkiye'deki üniversite öğrencileri için geliştirilmiş modern ve kullanıcı dostu not ortalaması hesaplama aracı.**

## 🌟 Özellikler

### 📊 Çoklu Not Sistemi Desteği
- **Sistem 1**: AA, BA, BB, CB, CC, DC, DD, FD, FF
- **Sistem 2**: AA, AB, BA, BB, BC, CB, CC, CD, DC, DD, FF  
- **Sistem 3**: A, A-, B+, B, B-, C+, C, C-, D+, D, D-, F
- **Sistem 4**: A1, A2, A3, B1, B2, B3, C1, C2, C3, D, F

### 🎯 Ana Fonksiyonlar
- **GANO Hesaplama**: Genel Ağırlıklı Not Ortalaması hesaplaması
- **DANO Hesaplama**: Dönem Ağırlıklı Not Ortalaması hesaplaması
- **Önceki Dönem Entegrasyonu**: Mevcut kredi ve ortalama bilgilerini dahil etme
- **Dosya Yükleme**: Excel (.xlsx, .xls) ve metin (.txt) dosyalarından veri aktarma
- **Yüzdelik Karşılık**: GPA'nin yüzdelik karşılığını gösterme
- **Durum Değerlendirmesi**: Akademik durumunuzu analiz etme

### 🎨 Modern Arayüz
- **Dracula Teması**: Göz yormayan koyu renk paleti
- **Responsive Tasarım**: Mobil ve masaüstü cihazlarda mükemmel görünüm
- **Animasyonlar**: Yumuşak geçişler ve görsel efektler
- **Kullanıcı Dostu**: Sezgisel ve kolay kullanım

## 🚀 Kullanım

### 1. Temel Kullanım
1. **Not Sistemi Seçimi**: Üniversitenizin kullandığı not sistemini seçin
2. **Önceki Dönem Bilgileri**: Mevcut toplam kredi ve ortalama bilgilerinizi girin
3. **Ders Sayısı**: Bu dönem aldığınız ders sayısını seçin
4. **Ders Ekleme**: "Ders Ekle" butonu ile derslerinizi ekleyin
5. **Hesaplama**: "Hesapla" butonu ile sonuçları görüntüleyin

### 2. Dosyadan Veri Yükleme
- **Excel Dosyası**: Ders adı, not ve kredi bilgilerini içeren Excel dosyası yükleyin
- **Metin Dosyası**: Virgülle ayrılmış format (CSV) ile ders bilgilerini yükleyin

**Örnek dosya formatı:**
```
Ders Adı,Not,Kredi
Matematik I,AA,6
Fizik I,BA,5
Algoritma ve Programlama,BB,4
```

### 3. Sonuçları Anlama
- **GANO**: Genel ağırlıklı not ortalamanız (0.00-4.00 arası)
- **Yüzdelik**: GPA'nizin yüzdelik karşılığı (0-100 arası)
- **Durum**: Akademik durumunuz (Başarılı, Şartlı, Başarısız)

## 📁 Dosya Yapısı

```
KrediHesaplama(Gano-Dano)/
├── index.html          # Ana uygulama dosyası
├── notlar.txt          # Örnek ders verileri
├── README.md           # Bu dosya
```

## 🛠️ Teknik Detaylar

### Kullanılan Teknolojiler
- **HTML5**: Modern web standartları
- **CSS3**: Özel stil ve animasyonlar
- **JavaScript (ES6+)**: Hesaplama algoritmaları ve DOM manipülasyonu
- **Tailwind CSS**: Responsive ve modern tasarım
- **XLSX.js**: Excel dosya okuma desteği
- **Inter Font**: Modern tipografi

### Desteklenen Dosya Formatları
- **Excel**: .xlsx, .xls
- **Metin**: .txt (CSV formatı)

### Tarayıcı Desteği
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

## 📖 Kullanım Örnekleri

### Örnek 1: Yeni Öğrenci
```
Önceki Dönem Kredi: 0
Önceki Dönem Ortalama: 0
Dönem Ders Sayısı: 6

Dersler:
- Matematik I (AA, 6 kredi)
- Fizik I (BA, 5 kredi)
- Kimya I (BB, 4 kredi)
- Türk Dili I (AA, 2 kredi)
- Atatürk İlkeleri I (BA, 2 kredi)
- Bilgisayar Programlama (AA, 4 kredi)
```

### Örnek 2: Devam Eden Öğrenci
```
Önceki Dönem Kredi: 45.5
Önceki Dönem Ortalama: 2.85
Dönem Ders Sayısı: 5

Dersler:
- Veri Yapıları (BB, 4 kredi)
- Nesneye Yönelik Programlama (BA, 4 kredi)
- Elektroteknik (CB, 4 kredi)
- Sayısal Devreler (CC, 4 kredi)
- Proje Yönetimi (BA, 5 kredi)
```

## 🔧 Özelleştirme

### Yeni Not Sistemi Ekleme
JavaScript kodunda `notSistemleri` objesi içerisine yeni sistem ekleyebilirsiniz:

```javascript
const notSistemleri = {
    // Mevcut sistemler...
    sistem5: {
        harfler: ['A+', 'A', 'A-', 'B+', 'B', 'B-', 'C+', 'C', 'C-', 'D', 'F'],
        puanlar: {
            'A+': 4.00, 'A': 3.75, 'A-': 3.50, 'B+': 3.25,
            'B': 3.00, 'B-': 2.75, 'C+': 2.50, 'C': 2.25,
            'C-': 2.00, 'D': 1.00, 'F': 0.00
        }
    }
};
```

### Tema Özelleştirmesi
CSS değişkenleri ile renk temasını özelleştirebilirsiniz:

```css
:root {
    --dracula-bg: #282a36;
    --dracula-foreground: #f8f8f2;
    --dracula-purple: #bd93f9;
    /* Diğer renkler... */
}
```

## 🤝 Katkıda Bulunma

1. Projeyi fork edin
2. Yeni özellik dalı oluşturun (`git checkout -b yeni-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Dalınızı push edin (`git push origin yeni-ozellik`)
5. Pull Request oluşturun

## 📝 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için LICENSE dosyasını inceleyebilirsiniz.

## 🆘 Destek

Sorularınız veya önerileriniz için:
- Issue açın
- E-posta gönderin
- Katkıda bulunun

---

**Not**: Bu uygulama Türkiye'deki üniversite öğrencileri için geliştirilmiştir ve Türk yükseköğretim sistemine göre tasarlanmıştır.
