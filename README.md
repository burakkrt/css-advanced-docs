# Css

### Border Radius

Genellikle direk pixel değeri vererek x ve y ekseni için eşit miktarda yuvarlama yaparız fakat raidus ‘u x ekseni için ayrı y ekseni için ayrı şekilde yuvarlama işlemi yapabiliriz.

![1](https://github.com/burakkrt/css-advanced-docs/assets/99482906/92a80f7c-653c-467f-8409-e7e00272047b)

```css
border-radius: 100px / 200px
```

![2](https://github.com/burakkrt/css-advanced-docs/assets/99482906/0a6ea644-4c84-4381-8291-8cb623204863)


### display: inline-flex

display: flex ‘den çok bir farkı yoktur. Ögeleri yan yana (row içeriside) sıralamak için kullanılır. Yatay olarak sıralar, taşma yapıyorsa overflow-hidden gibi taşırır, alt satıra geçmez. jusitfy-content, align-items gibi flex özellikleri kullanılabilir.

### filter: blur()

Bulanıklaştırma. Ekrandaki kaç pikselin birbirine karıştığını tanımlar

```css
filter: blur(4px);
```

### filter: brightness()

Parlaklığı arttır/azalt. 1 ‘default değer. 1 ‘den yukarısı parklaklaştır, aşağısı azalt. veya 100% ‘den yukarısı parlaklaştır veya azalt.

```css
filter: brightness(0) /* tamamen karanlık */
filter: brightness(1) /* olduğu gibi */
filter: brightness(1.3) /* parlak */
filter: brightness(100%) /* olduğu gibi */
filter: brightness(70%) /* parlaklığı azalt */
```

### filter: contrast()

Renkler arasındaki farkın derecesi olarak tanımlanır.  1 ‘default değer. 1 ‘den yukarısı parklaklaştır, aşağısı azalt. veya 100% ‘den yukarısı parlaklaştır veya azalt.

```css
filter: contrast(0) /* tamamen gri */
filter: contrast(1) /* olduğu gibi */
filter: contrast(1.3) /* contrast yüksek */
filter: contrast(100%) /* olduğu gibi */
filter: contrast(70%) /* contrast düşük */
```

### filter: drop-shadow()

Bir elementin etrafına bir gölge oluşturur. 

```css
filter: drop-shadow(X konum, Y konum, Bulanıklık, Renk);
filter: drop-shadow(4px 4px 4px rgba(0, 0, 0, 0.5));
```

### filter: grayscale()

Gri renk tonlarına dönüştürmeye yarar.

```css
filter: grayscale(0) /* olduğu gibi */
filter: grayscale(.7) /* hafif grileşme */
filter: grayscale(100%) /* tam gri */
filter: grayscale(1) /* tam gri */
```

### filter: hue-rotate()

Bir elementin renklerini çeşitli derecelerde döndürerek farklı renk efektleri elde etmenizi sağlar.

![3](https://github.com/burakkrt/css-advanced-docs/assets/99482906/de3060bf-d413-4857-8d55-6c57ea2226be)


text ‘in arkaplan rengini vermediğimiz halde hue-rotate ile rengi belirli derece döndürerek elde edebiliriz.

```css
 	filter: hue-rotate(-60deg);
  text-shadow: 2px 2px blue;
  background-color: magenta;
  color: goldenrod;
  border: 1em solid rebeccapurple;
  box-shadow: inset -5px -5px red, 5px 5px yellow;
```

### filter: invert()

Bir elementin renklerini ters çevirmek veya negatif bir görünüm oluşturmak için kullanılır.

```css
.box {
  width: 150px;
  height: 150px;
  background-color: blue;
  filter: invert(1);
}

/* return background-color: white; */
```

### filter: opacity()

Saydamlık seviyesini ayarlar.

```css
filter: opacity(1) /* olduğu gibi */
filter: opacity(100%) /* olduğu gibi */
filter: opacity(0) /* görünmez */
filter: opacity(50%) /* yarı oranda saydam */
```

### filter: saturated()

Renk doygunluğunu ayarlar.

```css
filter: saturated(1) /* olduğu gibi */
filter: saturated(0) /* renksiz (siyah beyaz) */
filter: saturated(100%) /* olduğu gibi */
filter: saturated(4) /* 4 katı oranda doygun renk */
filter: saturated(50%) /* yüzde elli oranında renksiz */
```

### filter: sepia()

Elementin renklerini sepia tonlarına dönüştürmek için kullanılır. Sepia tonları, eski fotoğraflarda sıkça görülen ve kahve tonlarına sahip bir renk tonlamasıdır.

```css
filter: sepia(0); /* olduğu gibi */
filter: sepia(.5); /* yarı oranında sepia renkler */
filter: sepia(1); /* tamamen sepia (kahverengi tonları) */
filter: sepia(100%); /* tamamen sepia (kahverengi tonları) */
```

### font

Yazı özelliklerini tek satırda tanımlamayı sağlar.

**small-caps :** Yazıdaki tüm küçük harfleri büyük harfe çevirir fakat boyutlarını küçük harfteki ile aynı şekilde bırakır. Büyük harfler, küçük harf boyutunda gösterilir.

```css
font: small-caps bold 18px/32px sans-serif;

/* font : <yazı tipi> <kalınlık> <boyut>/<satır yüksekliği> <yazı stili> */
```

### font-family

Yazı tipi stilinin belirlenmesi için kullanılır. Birden fazla değer alabilir ve bunlar virgün ile ayrılır. Eğer yazı tipi stili bulunamazsa bir sonraki yazı stilini uygular.

```css
font-family: "Gill Sans", sans-serif;
```

### font-size

Yazı boyutu.

```css
font-size: 12px;
font-size: 0.8em;
font-size: 1.2rem;
font-size: x-small;
```

### font-stretch

Yazıyı yüzeysel olarak daraltır veya genişletir. letter-spacing ‘e benzerdir ama stretch tüm yazıyı yüzeysel olarak daraltır veya genişletir.

```css
font-stretch: condensed; /* dar */
font-stretch: semi-expanded; /* yarı dar */
font-stretch: ultra-condensed; /* çok dar */
font-stretch: expanded; /* geniş */
font-stretch: semi-expanded; /* yarı genişlik */
font-stretch: ultra-expanded; /* tam genişlik */
font-stretch: 30%; /* yüzde otuz dar */
```

### font-style

Yazı şeklini ayarlar.

```css
font-style: normal;
font-style: italic;
```

### font-weight

Yazının kalınlığını ayarlar.

```css
font-weight: normal;
font-weight: bold;

font-weight: lighter;
font-weight: bolder;

font-weight: 100;
font-weight: 200;
font-weight: 300;
font-weight: 400; /* normal */
font-weight: 500;
font-weight: 600;
font-weight: 700; /* bold */
font-weight: 800;
font-weight: 900;
```

### line-height

Satır yüksekliğini ayarlar.

```css

line-height: normal;
line-height: 3.5;
line-height: 3em;
line-height: 34%;
```

### list-style-image

Listenin önüne resim koymanı sağlar. Resim boyutu ayarlanamadığı için boyutun küçük olmasına dikkat edilmelidir.

**tüm list-style özellikleri her zaman li etiketine verilir.**

```css
ul > li {
	list-style-image: url("star.png");
}
```

### list-style-type

li etiketlerini farklı semboller ile sıralama.

```css
list-style-type: decimal; /* sayısal, sıra ile 1. 2. 3. 4. */
list-style-type: square;  /* siyah kare */
list-style-type: circle;  /* içi boş yuvarlak */
list-style-type: disc;    /* siyah yuvarlak */

list-style-type: upper-roman; /* büyük roman rakamları ile (I, II, III, IV ...) */
list-style-type: lower-roman; /* küçük roman rakamları ile (i, ii, iii, iv ...) */

list-style-type: "Adı : "; /* listenin başına string ifade yazabiliriz. */
```

### list-style-position

List style özellikleri html ‘ye ::marker olarak li etiketinden önce yansıtılır. ::marker ‘lar default olarak `outside` olarak belirlenir yani listenin dışına taşabilir. li etiketinin içerisinde kullanmak ve taşmaları önlemek için `inside` özelliği kullanılmalıdır.

```css
ul > li {
	list-style-position: inside;
}
```

### list-style

Tek satırda tüm `list-style` işlemlerini uygulayabiliriz.

```css
list-style: square inside;
list-style: "Adı : " inside;
list-style: url("star.png")
```

### image-orientatiton

Bir görüntünün doğru şekilde görüntülenmesini sağlamak için kullanışlıdır, özellikle dikey veya yatay olarak döndürülmüş görüntülerle çalışırken.

Not: Her tarayıcı desteklemez bu nedenle kullanımı sakıncıladır. Sadece bilgi olsun yeterli.

```css
/* ekran yatay veya dikey konumda ise görüntü oryantasyonunu kendi otomatik tanımlasın.
ekranı yatay yaptığında görüntüde ona göre döndürülür. */
image-orientation: from-image;

image-orientation: 90deg;  /* görüntüyü 90 derece saat yönünde çevir. */
```

### image-renderig

Resimlerin büyütülmesi veya küçültülmesi sırasında kalite ve pikselleşme kontrolü için kullanılır.

```css
/* Aşağıdaki değerler resmin orginal boyutundan fazla büyültülmesi veya küçültülmesi
durumlarında vereceği sonuçları içerir.  */

/* Tarayıcı, performans ve görüntü kalitesi arasında bir denge sağlamaya çalışır.  */
image-rendering: auto;

/* Resmin daha net ve pikselsiz görüntülenmesini sağlar. (Sağdaki resim)  */
image-rendering: crisp-edges;

/* Pikselli bir görünümle büyütmeyi veya küçültmeyi sağlar. (Soldaki resim)
Bu genellikle retro tarzda görüntüler oluşturmak için kullanılır. */
image-rendering: pixelated;
```

![1](https://github.com/burakkrt/css-advanced-docs/assets/99482906/7734612d-750a-49bd-bfc4-948eb4163128)
![2](https://github.com/burakkrt/css-advanced-docs/assets/99482906/70862492-f9d7-4f14-9d0e-05e7959b309b)


### object-fit

Görüntülerin belirli bir boyutta nasıl sığdırılacağını belirtir.

```css
/* (default) Alanı tamamen kaplar, içerik çekilir veya sıkıştırılır. Görüntü korunmaz.  */
object-fit: fill;
/* Görüntünün hepsi görünür ve resim boyutu korunur, fazla alanlar boş kalır. */
object-fit: contain; 
/* Alanı tamamen kaplar, içerik korunur ve fazla alanlar görünmez. (kırpma işlemi)  */
object-fit: cover; 

object-fit: scale-down; // contain ile aynı;
```

### object-position

Görüntünün konteynır içerisinde hizalanması sağlar;

```css
object-position: center; /* ortalar */
object-position: right top; /* sağ üst */
object-position: 10px 10px; /* x ve y ekseninden 10 pixellik boşluk bırakır; */
object-position: 50% 20%; /* x ekseninde ortalar y ekseninde yüzde 20 aşağısı. */
```
