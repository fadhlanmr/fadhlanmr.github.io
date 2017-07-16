---
title: Petualangan ZTE Nubia Z9 Max
---

Ayahku mendapatkan *smartphone* ini disaat ia sedang mengunjungi <abbr title="Mobile World Congress">MWC 2016 </abbr>di barcelona, sebagai representasi Telkom Indonesia dalam bidang Digital Produk dengan kerjasama ZTE, mengunjukkan produk IndiHome.

Beruntung ayah saya mendapatkan rejeki diberi produk baru mereka yang baru saja muncul dipasar dengan 3 varian nya.
<hr size='12px'>

## ZTE Nubia Z9

![Nubia Z9](img\nubiaz9.jpg "ZTE Nubia Z9")
sekilas saya mencari tahu di google, terlihat bahwa *smartphone* ini memiliki layar yang *bezel-less*, saya menjadi tertarik untuk menjelajahi nya. Saya juga sudah sangat **terjaga** bahwa *smartphone* dari China ini akan memuat Bloatware[^fn-bloatware] yang berisi Social Media Regional China dan juga [Baidu](http://www.baidu.com/) yang sangat <del>terkenal</del> mengganggu itu.

Ternyata, yang diterima ayah saya bukanlah seri Z9 ini,
melainkan

## ZTE Nubia Z9 Max

![Nubia Z9 Max](img\z9max.jpg "ZTE Nubia Z9 Max")
"Lah itukan sama dlan"

"iya sama merk" 

menggunakan background hitam, karena untuk tidak menampilkan bezel yang ada di sisi nya.
Bedanya? lumayan sedikit,

- Layar
- Kamera
- Internal
- Infrared

CPU, GPU, OS, SIM masih sama, selengkapnya bisa dilihat [disini](http://www.gsmarena.com/compare.php3?idPhone1=7116&idPhone2=7207&idPhone3=7149 "Perbandingan ZTE Nubia Z9 Series") karena saya capek ngetik, perbandingan udah sama Nubia Z9 Mini yang masuk Series Z9. 

# Let's Get Down to the Root

First things that i always do, is to install *One Root Click*
...

Nah, Just Kidding. I gotta search the Custom ROM for this alienated device.
because it's pretty rare to have a Custom ROM for an unpopular smartphone. 

Fortunately, i found **Plenty** ROM for Nubia Z9 series, mine have NX512J series number if you're interested to search. Also don't forget the GAPPS for Google Play Store Service which can be downloaded and completely functional and have many version for Android version 4.4 - 7.1 from [OpenGAPPS](http://opengapps.org/ "Open GAPPS Download Link").

Every Nubia Z9 series, has pre-installed UI, the Nubia UI 2.8.
![Nubia UI 2.8](http://media2.intoday.in/indiatoday/images/stories//2015JUNE/ui_061515011911.jpg "Nubia UI 2.8") It's not great, rather decent. The settings UI is awful, ![UI Settings](https://regmedia.co.uk/2015/03/24/z9_in_hand_and_notifications.jpg) so hard to see and a mess. But, the Camera Feature and UI are awesome, lots of manual settings and slider, also a lock screen shot (double click volume button when it's locked, you get 3 different shutter shot) are one of the best out there.... 

Wait why i had to review this crap UI.
it's come in with Android 5.0.1, Lolipop.

at first, i tried to install TWRP Recovery with adb & fastboot.
{% highlight text %}
adb devices
a3obo3 device

adb reboot fastboot
{% endhighlight %}
just making sure that it's listed, but the series number seems different... No, it's **really** different, but i couldn't care less for it, i think it's natural.

i'm not shocked when the bootloader(fastboot mode) has been unlocked, it's a China Device!
And the problem start here.
{% highlight text %}
fastboot flash recovery recovery.img
< waiting for device >
{% endhighlight %}
Damn, what did i miss. I was trying to search for custom TWRP for Nubia, but it's not working well. I also trying to search 'adb waiting for device fix', and it's a device certification problem, only if you didn't have the devices registered

then, i found [this](http://www.alegrecompra.com/blog/instalar-twrp-recovery-root-gapps-para-nubia-z9-nx508j-z9-mini-nx511j-z9-max-nx510jnx512jnx518j/) custom ZTE android driver, with adb and fastboot config.
Oh! so that's why it doesn't listed the same as it's series number....

because it's come with custom TWRP for NX512J, i said why the fuck not?
![The Fuck not](http://www.alegrecompra.com/blog/wp-content/uploads/2016/08/zte-nubia-z11-twrp-recovery-root-gapps-4.jpg) i don't speak mexican and chinese (or it seems). But lucky me, it come with typed instructions. Gotta translate the shit out of it

I chose <del>you, Pikachu!</del> number 4, because i had already in fastboot mode.
{% highlight text %}
adb reboot recovery
{% endhighlight %}
And it did work, with some magic.

Of course, i've already put the ROM in my external SD card, it's  
> lineage-14.1-20170619-UNOFFICIAL-nx512j.zip

Don't ask why it's [unofficial](http://www.cyanogenmods.org/forums/topic/zte-nubia-z9-max-lineage-14-1-nougat-7-1-rom/).
It got the sweet Android 7.1 Nougat, the things that i want to use RAW, i've seen it in samsung, it's cool but not the default android. And for the past 3 years, i've been using Android 4.4 KitKat, feels like an old one.

The hype train stop here, with Error 7 Log
![i got it online, but it's the same error, so just go with it](http://uploads.tapatalk-cdn.com/20160407/cca0e65290b469b45ae9f0ae15c88932.jpg)
lord, why thou hast forsaken me.

exploring the XDA forum and got a quick&simple problem solve ![it's quick, for real](img/solve.jpg) the cause is, that i'm trying to install a Custom ROM for a different targeted Device, although it's compatible. To fix it, you just have to remove the authentification assuring it's the right device.

and yet it's still doesn't work.

why tho.



-----

[^fn-bloatware]: [*Software*](https://en.wikipedia.org/wiki/Software_bloat#Bloatware) yang telah ter-install terlebih dahulu dalam *Smartphone*