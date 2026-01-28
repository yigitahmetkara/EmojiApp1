EmojiApp - Set Game (SwiftUI)
Bu proje, Stanford Üniversitesi'nin CS193p (Developing Applications for iOS) kursu kapsamında geliştirilen, mantık ve dikkat gerektiren bir Set Game uygulamasıdır. Uygulama, SwiftUI kullanılarak MVVM (Model-View-ViewModel) mimarisine uygun şekilde inşa edilmiştir.
🚀 Özellikler
Dinamik Izgara Düzeni: AspectVGrid yapısı sayesinde masadaki kart sayısı değiştikçe (12'den 81'e kadar) kartlar en boy oranını bozmadan ekrana otomatik sığar.
Set Mantığı: Seçilen 3 kartın renk, şekil, sayı ve gölgeleme özelliklerine göre bir "Set" oluşturup oluşturmadığı anlık olarak kontrol edilir.
Akıllı Kart Dağıtımı: "Deal 3 More Cards" butonu, masada eşleşmiş bir set varsa bu kartları yenileriyle değiştirir; yoksa masaya 3 yeni kart ekler.
Görsel Belirleyiciler:
Seçim: Seçilen kartlar turuncu çerçeve ile vurgulanır.
Eşleşme: Eşleşen (Set olan) kartlar mavi çerçeve ile belirtilir.
Sıfırlama: "New Game" butonu ile deste karıştırılır ve oyun 12 yeni kartla baştan başlatılır.
🏗 Mimari Yapı (MVVM)
Uygulama üç ana katmandan oluşmaktadır:
Model (EmojiAppModel.swift): Oyunun kurallarını, kart destesini (81 kart), masadaki kartları ve Set kontrol mantığını yönetir.
ViewModel (EmojiAppViewModel.swift): Model ile View arasında köprü görevi görür. Görsel yardımcıları (renkler, opaklıklar) hesaplar ve kullanıcı eylemlerini (intent) modele iletir.
View: Kullanıcı arayüzünü temsil eder.
SetGameView: Ana ekran düzeni ve butonlar.
CardView: Tek bir kartın tasarımı ve içeriği.
AspectVGrid: Kartların matematiksel yerleşim motoru.
Diamond: Özel elmas şekli çizimi.
🎨 Tasarım Detayları
Ödev gereksinimlerine uygun olarak kartlar şu özelliklere sahiptir:
Şekiller: Elmas, Dikdörtgen ve Oval (Capsule).
Gölgeleme: Tam Dolu (Solid), Çizgili/Yarı Şeffaf (Striped - %30 Opaklık) ve Boş (Open).
Renkler: Kırmızı, Yeşil ve Mor.
🛠 Kurulum
Bu projeyi bilgisayarınıza indirin.
EmojiApp.xcodeproj dosyasını Xcode ile açın.
Command + R tuşlarına basarak simülatörde çalıştırın.

Uygulama Ekran Görüntüleri
<img src="Ekran Resmi 2026-01-28 20.22.18.png" width="300" alt="Uygulama Ekran Goruntusu">
<img src="Ekran Resmi 2026-01-28 20.22.26.png" width="300" alt="Uygulama Ekran Goruntusu">
<img src="Ekran Resmi 2026-01-28 20.22.29.png" width="300" alt="Uygulama Ekran Goruntusu">
