Geçen yılın hava durumunu çektiğimiz site
https://www.visualcrossing.com/weather-history/

Bugüne ait nem rüzgar basıncı çektiğimiz site
https://openweathermap.org/api


Bugün için sıcaklık verisini çekmek yerine, diğer hava durumu faktörlerini (nem, rüzgar hızı, basınç gibi) API'den alıp, bu verileri kullanarak tahmini bir sıcaklık değeri oluşturacağız. Bu değeri de geçen yılın aynı gününe ait sıcaklıkla işlem yaparak bugünün sıcaklık tahminini elde edeceğiz.

Adımlar:
API'den Nem, Rüzgar Hızı ve Basınç Gibi Verileri Çekme:
  API'den sadece sıcaklık yerine diğer hava durumu verilerini çekeceğiz.
Bugünün Sıcaklık Tahmini Hesaplama:
  API'den alınan nem, rüzgar hızı gibi faktörleri kullanarak tahmini bir sıcaklık değeri hesaplayacağız.
Geçen Yılın Verisiyle İşlem Yapma:
  Geçen yılın aynı gününe ait sıcaklık verisini, bugünün hesaplanan tahmini sıcaklığıyla birleştirerek bugünün sıcaklığını tahmin edeceğiz.

Açıklamalar:
API'den Çekilen Veriler:
  Nem (main.humidity)
  Rüzgar Hızı (wind.speed)
  Basınç (main.pressure)
Bu üç faktör, bugünkü tahmini sıcaklık hesaplamasında kullanılacak.

Tahmin Hesaplama:

Bu faktörler üzerinde belirli ağırlıklarla hesaplama yapıyoruz. Örneğin:
Nem, sıcaklık üzerinde %40 etkili.
Rüzgar hızı %20 etkili.
Basınç da %20 etkili.
Bu veriler, geçen yılın aynı gününe ait sıcaklık verisiyle birleştiriliyor.

Geçen Yılın Verisi:

Geçen yılın aynı gününe ait sıcaklık verisini historicalWeatherUrl üzerinden çekiyoruz.
Sonuç:

Bugün için tahmini sıcaklık, hem mevcut verilerle hem de geçen yılın verisiyle birleştirilerek elde ediliyor.
