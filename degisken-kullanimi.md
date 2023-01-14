# Değişken Kullanımı

Öncelikle daha önce bir programlama dili ile çalışmamış kişiler için değişken kavramının ne olduğunu tanımlayalım.

> Değişken: uygulama çalışırken herhangi bir türde veri tutabilen kavramlardır.

Daha açık bir şekilde değişkeni şu şekilde tanımlayabiliriz.

> aylık 10.000₺ maaş aldığınızı varsayalım. Ne yaptınız bu beyninizde direkt şu tanımlamayı yaptınız. "aylık maaşım = 10.000₺" işte bunun aynısını programala da yaptığımızda değişken olur.

Örneğin PHP'de şu şekilde değişken oluştururuz.

```php
<?php

$aylik_maas = '10000₺';

?>
```
Yazdığımız bu kodu açıklayalım hemen

PHP'de değişken oluştururken değişken adında `ü-İ-ş-ç-ö-ğ` gibi türkçe karakter kullanılmaz. Ve değişken adında boşluk ve `-` ifadeleri de kullanılmaz.

Değişken oluştururken programın bizim değişken oluşturacağımızı anlaması için değişkenin başına `$` ifadesini koyarız.

### Biraz daha geliştirelim

Biraz daha geliştirelim çünkü yukarıda yazılan PHP kodlarını çalıştırdığınızda ekran da hiçbir şey görmeyeceksiniz. Ne demiştik önceki derste ekrana birşeyler basmak için `echo` komutunu kullanırız. Ve ekran da değişken değerini görmek istersek bunu şu şekilde yapabilirdik.

```php
<?php

$aylik_maas = '10000₺';
echo $aylik_maas;

?>
```

Bu kod bloğunu (parçasını) çalıştırdığınızda ekran da şu şekilde görünecek

```text
10000₺
```

Tabiki bu ekrana basılan bir kişi için ne ifade edebilir ki. `10000₺` ne? Bu sorunu da şu şekilde çözebiliriz. Eğer bu `10000₺` ifadesinin başına `Aylık Maaşım: ` ifadesini getirirsek. `Aylık Maaşım: 10000₺` olarak göreceğiz. Yani iki ifadeyi birleştireceğiz.

Biz bunu PHP'de `.` ifadesiyle yapıyoruz. O zaman örnek bir kod bloğu yazalım.

```php
<?php

$aylik_maas = '10000₺';
echo 'Aylık Maaşım: ' . $aylik_maas;

?>
```

Dolayısıyla bu bloğu çalıştırınca ekranda `Aylık Maaşım: 10000₺` şeklinde az öncekinden çok daha mantıklı bir ifade göreceksiniz.