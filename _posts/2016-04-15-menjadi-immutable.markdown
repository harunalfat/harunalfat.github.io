---
layout: post
title: "Menjadi Immutable"
date: 2016-04-17 23:12:45
author: Alfat Saputra Harun
categories: Software
tags: curhat hidup
cover: "/assets/instacode.png"
---
### Blog Pindahan

Pertama, mari kita ucapkan alhamdulillah atas diresmikan blog baru saya ini. [Blog lama](https://blog.harunalfat.com) saya masih aktif, namun terdapat beberapa kesalahan di dalamnya sejak saya memigrasi kode-nya.

Intinya tulisannya di halaman luar memang masih bisa dibaca, namun *user tools* di belakangnya berantakan, *sigh*... Mungkin tulisan-tulisan di dalam blog lama akan saya migrasi kesini, karena beberapa memuat ilmu-ilmu yang cukup sayang jika dibuang begitu saja :)

### Menulis Seri

Cukup cerita dengan blog lama saya, sekarang kita masuk ke babak baru kehidupan (duuh). Jadi, sudah sejak lama saya ingin menulis tentang hubungan antara manusia dan software, baik secara kiasan ataupun realita.

Terkadang ketika saya koding dalam pekerjaan saya dan menerapkan teknik-teknik software engineering, banyak hal bisa sangat erat dikaitkan dengan kehidupan manusia. Hal-hal inilah yang sering saya renungi, dan mungkin akan lebih baik jika saya tulis dan bagikan ke teman-teman lain di luar sana. Maka oleh itu, saya akan mulai rutin menulis serial **"Sofware dan Manusia"** di blog ini.

Seri tulisan saya ini meskipun sesedikit memuat hal-hal teknis, namun tetap bisa dibaca oleh orang-orang yang tidak mempunyai pengalaman pemrograman kok :). Saya akan berusaha membuat hal teknisnya sesedikit mungkin.

### Immutable

Bagi beberapa orang yang sudah pernah berkutat dengan pemrograman, mungkin Anda sudah mengenal kata *immutable*. Jika diartikan ke dalam bahasa Indonesia mungkin bisa dimaknai *tidak bisa berubah*. Nah, ada apa dengan *immutable* ini?

Dalam pemrograman objek, mungkin Anda sering membuka akses ke dalam nilai attribut-attribut suatu objek, entah melalui akses langsung atau *method get/set* yang punya tingkat akses publik.

contoh *mutable* 1 :

{% highlight java %}
public class Orang {

  public int umur;
  public String nama;

}
{% endhighlight %}

contoh *mutable* 2 :

{% highlight java %}
public class Orang {

  private int umur;
  private String nama;

  public int getUmur(){...}
  public void setUmur(){...}

  public String getNama(){...}
  public void setNama(){...}

}
{% endhighlight %}

ini merupakan praktik yang kurang baik. Bisa dibaca lebih jelas di banyak tulisan, salah satunya [disini](http://www.yegor256.com/2014/06/09/objects-should-be-immutable.html).

Berikut contoh untuk kode yang *immutable* :

{% highlight java %}
public final class Orang {

  private final int umur;
  private final String nama;

  public Orang(int umur, String nama){
    this.umur = umur; // final sekali set
    this.nama = nama; // final sekali set
  }

  public int getUmur(){...}
  public String getNama(){...}

}
{% endhighlight %}

### Immutable Dalam Kehidupan

Dijelaskan diatas bagaimana *immutable* dalam pemrograman. Untuk *immutable* dalam kehidupan sebenarnya kira-kira seperti apa? Banyak, salah satunya adalah istiqomah.

Sebagaimana objek dalam pemrograman, ketika Anda membuka akses ke atribut internal si objek, maka akan banyak tangan-tangan programmer jahil yang mencoba merubah nilai atribut dari sang objek sehingga bisa memberikan respon sesuai yang diinginkan mereka, padahal sesungguhnya mereka menggerus perlahan-lahan struktur program itu sendiri.

Manusia juga terkadang mengeskpos isi diri mereka keluar, dengan segala kelemahannya. Terkadang ketika Anda sudah menetapkan suatu hal di dalam hati, mungkin ingin bekerja di luar negeri, mungkin manjadi pengusaha sukses, mungkin bertobat untuk perbuatan dosa, ada saja yang Anda biarkan datang dan merubah ketetapan hati Anda.

Seringkali orang-orang akan mengomentari Anda, dan kebanyakan bukan dengan komentar baik. Mungkin mereka mengatakan

- "kemampuan bahasa inggris minim kok mau ke luar negeri?"
- "halah, sekarang aja jualannya kamu malah rugi"
- "ntar aja tobatnya bro, dikit-dikit juga diulangi"

Awalnya mendengar satu dua komentar miring Anda mungkin masih kalem saja. Namun semakin sering orang berkomentar negatif, Anda mulai terseret dengan cara mereka berpikir, "jangan-jangan mereka benar?". Perlahan-lahan keyakinan di hati tadi mulai tergerus, berganti keraguan hingga akhirnya terhapus menjadi mimpi yang tak tersampaikan.

Jika Anda belajar dari sebuah objek *immutable*, ketika dia terlahir di suatu program dengan perintah `new Orang(...)`, nilai-nilai yang dia pegang **tidak akan pernah berubah** hingga objek tersebut mati.

Kita manusia ketika terlahir di dunia diperintahkan untuk beribadah, namun dengan segala ke-*mutable*-an kita, seringkali kita berubah haluan dan tersesat dalam perjalanan kita. Segala hal-hal baik yang bisa membantu kita dalam beribadah mulai tergantikan dengan hal-hal kecil yang kurang bermanfaat.

Alangkah luar biasanya jika hati ini bisa menjadi *immutable*, yang jika sekali kita berniat hingga akhir zaman tidak akan pernah terbelokkan oleh apapun juga.
