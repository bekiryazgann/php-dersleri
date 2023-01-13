# Giriş

İlk dersimizden bu yana PHP'nin ne olduğunu neyle düzenleyip ne ile yorumlayıp görebileceğimizi gördük ve işledik. Çok fazla teknik bilgi içerikli olmasını istemediğim içinde kimin kaç yılında geliştirdiğini vs. söylemedim. Zira sizinde bu tarz teknikten ziyade PHP'nin mayası dediğimiz bilgilere ihtiyacınız yok. Çünkü biz PHP'ye rakip bir programlama dili çıkartmaktan ziyade PHP ile proje geliştirme nasıl kullanırız vs gibi konuları ele alacağız.

Öncelikle PHP kodları çoğunlukla `dosyadi.php` tarzında dosyalarda bulundurulur (yani php uzantılı). Kesinlikle `dosyadi.html` gibi dosyalarda (html uzantılı) çalışmaz.

Öncelikle MAMP uygulamanızı açıp sunucunuzu çalıştırarak ve sunucu ana dizinine giderek bir dosya oluşturun `index.php` (sunucular genelde ilk olarak index. türünde dosyaları ele alır. sayfa ilk açıldığında buu arar bulamazsa tüm klasörü görürsünüz) ve bu dosyayı `Visual Studio Code` uygulamanızı açarak içerisine atın.

Ve ilk denemeyi yapmak amaçlı aşağıdaki kodları yapıştırın ve kaydedin.


``` php
<!DOCTYPE html>
<html>
<head>
  <title> Örnek </title>
</head>
<body>

<?php
  echo "Merhabalar ben bir örneğim";
?>

</body>
</html>
```

Ve daha sonra `chrome`, `firefox`, `edge`, `opera` gibi bir tarayıcıdan [http://localhost/](http://localhost/) adresini gidin. Ekran da 

```
Merhabalar ben bir örneğim
```

Gibi bir yazı ve sekme başlığı olarak `Örnek` göreceksiniz. Eğer buraya kadar geldiyseniz hiçbir sorun yoktur. Şimdi bu kodu kopyala yapıştır yaptık ama bunu kendiniz yazmak için okuyorsunuz. O halde gelin bu kod satırlarını yorumlayalım.


Şunu belirteyim `<?php` ve `?>` bu ikisi arasında olan her şey birer php kodu. Diğerleri ise bu örnekte html kodu. Zaten bu örnekte yazılanım çoğu HTML'in ana iskelet yapısı. Ve bunu `Visual Studio Code`'da `!` ardından `tab(klavyedeki tuş)`'a basarak oluşturabiliyoruz. Yani aslında bizim bu örnekte odaklanmamız gerek yer sadece `<?php` ve `?>` arasındaki kodlar. Bu kodları da aşağıda sade bir şekilde tekrar yazalım.

``` php
<?php
  echo "Merhabalar ben bir örneğim";
?>
```
 
 Burada ve diğer bütün örneklerde dahil eğer php kodu yazacaksak php tagları dediğimiz tagları kullanmamız şart. Aksi takdirde sunucu bizim php mi yoksa html mi yazdığımızı anlayamaz. Tek php tagı açma yöntemi bu değil daha kısa ve efektif olan yöntemlerde var fakat bunları ilerleyen derslerde göstereceğim.
 
 PHP tagının bir da kapanması var. Fakat burada şöyle bir incelik var. Eğer HTML'de bir tagı kapatmazsanız çok büyük hatalar almazsınız ama PHP de bu biraz öyle değil. İsterseniz şuan bunu okumayı bırakıp PHP tagları içerisine html kodlarını yazın ve localhost'ta bir deneyin. Sunucu size direkt `ne yazdıysan anlamadım` diyecektir. Yani php taglarından sonra bir html kodu yazacaksanız açtığınız php tagını kapatmalısınız. ve bunu şu ifadeyle yapıyorsunuz `?>` yani günün sonunda php kodları `<?php` bu ekilde bir tag ile açılıp `?>` bu şekilde bir tag ile kapanıyor.
 
 Birde ekranda yazan `echo` ve tırnaklar içerisinde bir metin ve bu metnin sonunda da `;` ifadesi bulunuyor. `echo` herhangi bir ifadeyi ekrana basmak için kullanılır. yani ekrana basma aracı ve biz bunu sık sık kullanıyor olacağız. Aradaki metnin başında da tırnak işaretleri var çünkü program `Merhabalar ben bir örneğim` ifadesini yorumlayamaz. Zira biz de bunu youmlatmak istemedik. Yani kod haricinde bir veri saklamak istiyorsan bunu çift tırnak(") ya da tek tırnak(') işaretleri arasına yazarız. Sondaki noktalı virgül ne ayak ';'  php kodları kısaltılabilir. yani bu komutu kopyalayıp (taglar hariç) altına yapıştırabilirdik ya da kodumuz 1 satır daha uzayacağına yana doğru uzansın diyebilirdik. Burada çözüm olarak komutları ayırmak devreye giriyor. bunu ise noktalı virgül(;) ile yapıyoruz. 
