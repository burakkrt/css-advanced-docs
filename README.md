# Css

Hazırlayan : 

> GitHub : [**/burakkrt**](https://github.com/burakkrt)

### Border Radius

Genellikle direk pixel değeri vererek x ve y ekseni için eşit miktarda yuvarlama yaparız fakat raidus ‘u x ekseni için ayrı y ekseni için ayrı şekilde yuvarlama işlemi yapabiliriz.

![1](https://github.com/burakkrt/css-advanced-docs/assets/99482906/92a80f7c-653c-467f-8409-e7e00272047b)

```css
border-radius: 100px / 200px
```

![2](https://github.com/burakkrt/css-advanced-docs/assets/99482906/0a6ea644-4c84-4381-8291-8cb623204863)


### linear-gradient

İki veya daha fazla renk arasında aşamalı bir geçişten oluşan özel bir <image> türüdür

```css
background-image: linear-gradient(yönü, renk1, renk2 ...);
/* default yukarıdan aşağıya doğru renk geçişleri */
background-image: linear-gradient(red,blue);

/* 4 farklı yöne doğru renk geçişi */
background-image: linear-gradient(to right,red,blue);
background-image: linear-gradient(to left,red,blue);
background-image: linear-gradient(to top,red,blue);
background-image: linear-gradient(to bottom,red,blue);

/* sağ aşağıya doğru biten */
background-image: linear-gradient(to bottom right,red,blue);
/* sol yukarıya doğru biten */
background-image: linear-gradient(to top left,red,blue);
```

### attr

Bir öğenin herhangi bir attribute ‘unu css ‘de kullanmamızı sağlar.

```css
<a href="#" aciklama="bu bir a etiketidir">Hello my button</a>

/* a etiketinin after ile sonrasına bir element ekliyorum ve içeriğini
a etiketinin aciklama adındaki attributunu yazdırıyorum, ister class, ister
style gibi istebilen attribute 'yi alabiliriz */
a:after {
	content: ' 'attr(aciklama)' ';
	color: red;
}
```

### background-blend-mode: multipy

Üst üste konumlandırılan iki veya daha fazla arkaplanın, renklerinin karıştırılması sonucu ortak bir rengin ortaya çıkmasıdır. Özellikle bir resim ile arkaplan rengini birleştirmede oldukça kullanışlıdır.

```css
#div {
  width: 300px;
  height: 300px;
  background: url("br.png"), url("tr.png");
  background-blend-mode: multiply;
}
```

![Opera Anlık Görüntü_2023-09-16_144348_devdocs io](https://github.com/burakkrt/css-advanced-docs/assets/99482906/2dd3c78e-d353-49dd-aa7b-8458dd35d39a)


### background-attachment

Bir arka plan görüntüsünün konumunun görüntü alanı içinde sabit olup olmayacağını veya içeren blokla birlikte kaydırılıp kaydırılmayacağını belirler.

```css
/* scroll 'y kaydırsak bile arkaplan sabit kalır, güzel bir görünüm */
background-attachment: fixed;
```

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

/* Resmin daha net ve pikselsiz görüntülenmesini sağlar. (İlk resim)  */
image-rendering: crisp-edges;

/* Pikselli bir görünümle büyütmeyi veya küçültmeyi sağlar. (İkinci resim)
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

## MEDİA QUERİES

### *@media* (any-hover: hover)

Kullanıcının fare veya işaretçi benzeri bir cihaz kullanarak herhangi bir öğe üzerine işaret koyma yeteneğine sahip olup olmadığını belirler. `hover`  işlemleri uygularken dokunmatik ekran kullananların `hover` özelliğini kullanamazlar. `any-hover` ile sadece öğe üzerine gelebilen cihazlar için `hover` özelliğini kullanmamız daha güvenli olacaktır.

```css
/* eğer kullancının fare vb. işaretçisi var ise p nin üzerine geldiğinde renk
maviye dönüşebilir, işaretçisi yok ise hover özelliği kullanılmaz. */
p{
	color: black;
}

@media (any-hover: hover) {
	p:hover{
		color: blue;
	}
}
```

### *@media* (pointer , any-pointer)

Kullanıcının hangi türde işaretçi kullandığını belirler. `fine` kullanıcı işaretçisi varsa, `coarse` kullanıcı dokunmatik ekran tarzı bir işaretçi kullanıyor ise. Bu özellik genellikle masaüstü veya mobil için ayrı stillendirmede kullanılır.

```css
/* Eğer kullanıcı herhangi bir türde işaretçi cihazı kullanıyorsa (PC, Dokunmatik ekran
@media (any-pointer: fine) {
	p{
		color: red;
	}
}

/* Eğer sadece fare gibi bir işaretçi cihazı kullanıyor ise */
@media (pointer: fine) {
  p{
		color: blue;
	}
}
```

### *@media* (color)

Kullanıcının renk kapasitesini ve renk destek seviyesini tanımlamak için kullanılır.

```css
@media (color) {...}  /* Kullanıcının ekranı renkli gösteriyor ise */
@media (min-color: 8) {...} /* Kullanıcı en az 8 bit renk değerini karşılıyor ise */
@media (color-index) {...} /* Kullanıcı sadece siyah beyaz renk destekliyor ise */
```

### *@media* (display-mode)

Kullanıcının web sitesini nereden ve nasıl çalıştığını kontrol eder. Dört farklı değer alır.

```css
/* Kullanıcı bir tarayıcıdan web sitesine giriyor ise */
@media (display-mode: browser) {...} 
/* Kullanıcı bir tarayıcıdan tam ekran modunda web sitesine giriyor ise */
@media (display-mode: fullscreen) {...} 
/* Kullanıcı, web sayfasını bir uygulamanın içerisinden görüntülüyor ise */
@media (display-mode: fullscreen) {...} 
/* Kullanıcı web sayfasını minimal bir kullanıcı arabirimi (UI) ile görüntülüyor ise*/
@media (display-mode: minimal-ui) {...} 
```

### *@media* (hover: hover)

Kullanıcının bir HTML etiketinin üzerine gelip gelemiyeceğini kontrol eder. Mobil cihazlarda fare işaretcisi olmadığı için kullanıcı etiketlerin üzerinde dolaşamaz. normal `:hover` özelliği ile aynıdır fakat hover olabilecek ögelere hover vererek daha kullanışlı kod yazmamızı sağlar.

```css
/* eğer hover destekleniyor ise p etiketine hover özelliği verir */
@media (hover: hover) {
	p:hover {
		color: red;
	}
}
/* hover desteklensede desteklenmese de hover özelliği verir. */
p:hover {
	color: red;
}
```

### *@media* (orientation)

Kullanıcının ekranı dikey veya yatay kullanımını belirler. Özellikle mobil cihazlarda ekran döndürme olayları için kullanışlıdır.

```css
/* Ekran dikey (portre) modunda ise */
@media (orientation: portrait) {
  p{
    color: red;
  }
}
/* Ekran yatay(manzara) modunda ise */
@media (orientation: landscape) {
  p{
    color: blue;
  }
}
```

### Javascript ile dinamik media kontrolü

Javascript ile media sorgularını kontrol edip buna göre aksiyonlar gerçekleştirebiliriz.

```jsx
const mediaQueryList = window.matchMedia("(orientation: portrait)");

if(mediaQueryList.matches){
		console.log("Şuan dikey ekrandasın");
} else {
		console.log("Şuan yatay ekrandasın");
}
```

```jsx
const responsive = window.matchMedia("(max-width: 768px)");

if(responsive.matches) {
	div.styled.backgroundColor = "blue";
}
```

```jsx
/* chance işlemi : belirtilen koşul her değiştiğinde kod bloğu çalışır */
window.matchMedia("(max-width: 390px)").addEventListener("change", (e) => {
    if(e.matches){
      console.log("390px 'den küçük ekran");
    } else {
      console.log("390px 'den büyük ekran");
    }
})
```

### *@media* (width)

Tarayıcının genişlik veya uzunluk özelliklerine göre aksiyonlar almamızı sağlar. Farklı cihaz ölçeklerine göre stil methodları oluşturmamızı sağlar.

```jsx
/* tarayıcı genişliği veya uzunluğu belirli bir pixelde ise */
@media (width: 360px) {
  div {
    color: red;
  }
}
@media (height: 360px) {
  div {
    color: red;
  }
}

/* tarayıcı genişliği veya uzunluğu belirli bir pixelin üzerinde ise */
@media (min-width: 350px) {
  div {
    background: yellow;
  }
}
@media (min-height: 350px) {
  div {
    background: yellow;
  }
}

/* tarayıcı genişliği veya uzunluğu belirli bir pixelin aşağısında ise */
@media (max-width: 1920px) {
  div {
    border: 2px solid blue;
  }
}
@media (max-height: 1920px) {
  div {
    border: 2px solid blue;
  }
}
```

## Transform Methods

### translate()

Bir öğenin yatay ve/veya dikey eksende belirli bir mesafe boyunca hareket etmesini sağlar.

```css
transform: translateX(30px); /* x ekseninde içeriği 30 px sağa kaydırır */
transform: translateX(-30px); /* x ekseninde içeriği 30 px sola kaydırır */
transform: translateY(30px); /* x ekseninde içeriği 30 px aşağıya kaydırır */
transform: translateY(-30px); /* x ekseninde içeriği 30 px yukarıya kaydırır */

/* içeriği x ekseninde 30 px sola, y ekseninde 30px aşağıya kaydırır */
transform: translate(30px, 30px); 
```

### matrix()

Bir öğeyi x,y,z ekseninde döndürmeye yarar. transform ‘un `scale`, `rotate` vb. gibi özelliklerini bir arada kullanma gibi düşünebiliriz. **Güzel animasyonlar elde edilebilir.**

```css
transform: matrix(a, b, c, d, tx, ty);
/*
a, öğenin yatay boyutunu (ölçek faktörü) temsil eder.
b, öğenin yatay kaydırmasını ve döndürmesini temsil eder.
c, öğenin dikey kaydırmasını ve döndürmesini temsil eder.
d, öğenin dikey boyutunu (ölçek faktörü) temsil eder.
tx, öğenin yatayda konumunu temsil eder.
ty, öğenin dikeyde konumunu temsil eder.
*/

transform: matrix(0.5, -0.866, 0.866, 0.5, 100, 100);
```

### rotate()

Öğeyi x, y veya z ekseninde döndürmeyi sağlar.

```css
transform: rotateX(90deg);  /* dikey döndürme */
transform: rotateY(180deg);  /* yatay döndürme */
transform: rotateZ(180deg);  /* soldan sağa doğru döndürme */
transform: rotate(180deg); /* rotateZ ile aynı */

transform: rotateY(1turn); /* y ekseninde 1 tur döndürmek için */
transform: rotateY(0.5turn); /* y ekseninde yarım tur döndürme yani 180 derece */
transform: rotate(1turn); /* x ve y ekseninde 1 tur döndürmek */

transform: rotate(3.142rad); /* deg 'in rad cinsinden değeri (gereksiz) */
```

### scale()

Bir öğenin boyutunu yatayda ve dikeyde ölçeklendirmek için kullanılır.

```css
transform: scaleX(1.3);  /* içeriği x ekseninde 1.3 katında büyült */
transform: scaleY(2);  /* içeriği x ekseninde 2 katında büyült */
transform: scale(2);  /* içeriği x ve y ekseninde eşit olarak 2 katında büyült */

/* içeriği x ekseninde 1.5, y ekseninde 2 kat olarak 2 katında büyült */
transform: scale(1.5 , 2);  
```

### skew()

Bir öğenin yatay veya dikey düzlemde eğik bir şekilde çarpılmasını veya döndürülmesini sağlar.

```css
transform: skewX(30deg); /* x ekseninde 30 derece eğik yap */
transform: skewY(80deg); /* y ekseninde 80 derece eğik yap */
transform: skew(30deg, 80deg); /* x ve y ekseninde eğik yap */
```

## Animation Methods

Not : Aşağıda tanımlanan rotate adındaki animasyon tüm anımasyon metotlarını anlatırken kullanılacaktır. rotate kavramı aşağıdaki animasyon ‘dan gelmekte olacak.

```css
@keyframes rotate {
  from{
    transform: rotate(0);
  }
  to {
    transform: rotate(360deg);
  }
}
```

### animation-name()

Oluşturulan animasyonu belirli bir elemente ekleme.
Önemli: Animasyonu tanımlarken süresini de tanımlamak zorundayız aksi halde animasyon görüntüleyemeyeceğimiz hızda çalışır ve bunu fark etmeyiz.

```css
.box{
	animation-name: rotate; /* rotate adındaki animasyonu box class 'ına tanımladık */
	animation-duration: 0.7;
}
```

### animaton-duration()

Animasyonu toplam ne kadar sürede tamamlanacağını belirtir.

```css
.box{
	animation-name: rotate;
	animation-duration: 1s; /* toplam 1 saniyede animasyonu oynat */
}
```

### animation-direction()

Animasyonun ileriye mi yoksa geriye doğru mu oynatılacağını belirtir.

```css
animation-duration: normal; /* animasyonu ileriye doğru oynat (default) */
animation-duration: reverse; /* animasyonu geriye doğru oynat*/
/* animasyonu ilk ileriye doğru oynatıp bitirir ve ardından geriye doğru oynatır */
animation-duration: alternate; 
/* animasyonu ilk geriye doğru oynatıp bitirir ve ardından ileriye doğru oynatır */
animation-duration: alternate-reverse; 

```

### animation-iteration-count()

Animasyonun kaç kere oynatılacağını belirtir.

```css
animation-iteration-count: 4; /* animasyonu 4 kere oynatıp bitirir */
animation-iteration-count: 1.5; /* animasyonu 1 kere tam 1 kere yarım oynatıp bitirir */
animation-iteration-count: infinite; /* animasyonu sonsuz kere oynatır.*/
```

### animation-timing-function()

Animasyonun her döngüde nasıl bir hızda ilerleyeceğini belirler.

```css
/* başlangıçtan sona kadar eşit hızla ilerler */
animation-timing-function: linear;

/* başlangıçta yavaş sonunda yavaş */
animation-timing-function: ease;

/* başlangıç yavaş sonlara doğru hızlı */
animation-timing-function: ease-in;

/* başlangıç hızlı sonlara doğru yavaş*/
animation-timing-function: ease-out;

/* başlangıç yavaş ortası hızlı sonlar yavaş*/
animation-timing-function: ease-in-out;

/* cubic-bezier ile özelleştirilmiş animasyon hızı oluşturulabilir*/
animation-timing-function: cubic-bezier(0.42,0,0.8,1);

animation-timing-function: steps(adımSayısı, atlamaAnahtarKelime);
/* Animasyonu 5 adımda tamamla (%20, %20, %20, %20, %20) */
animation-timing-function: steps(5, start)
```

### animation-delay()

Animasyona tanımlar ve başlamadan önce ne kadar süre bekleyeceğini belirtir.

```css
animation-delay: 1s;  /* 1saniye sonra animasyonu oynatmaya başlar */
animation-delay: -3s;  /* animasyonu 3. saniyesinden itibaren başlatır */
```

### animation-fill-mode()

Belirli bir süre içinde nasıl davranacağını tanımlayan bir özelliktir.

```css
@keyframes rotate {
  from{
    transform: rotate(45deg);
  }
  to {
    transform: rotate(180deg);
  }
}

/* Animasyona başlangıç değeri rotate 45deg verdik ve bitişi 180deg olacağını söyledik.
.box class 'ında rotate ile ilgili bir değer olmadığına dikkat edelim. */

/* none methodu animasyon bittikten sonra animasyonda tanımlanan özelliklerin 
hiçbirinin .box class 'ına aktarılmayacağını belirtir. Yani animasyon 45 dereceden 
180 dereceye dönmeye başlar ve animasyon bitince animasyonda tanımlanan tüm
methodlar .box class 'ından kaldırılır. */

.box {
	animation-name: rotate;
  animation-duration: 3s;
	animation-fill-mode: none;
}

/* forwards 'da animasyonda tanımlanan son (yani bitiş) methodlarının değerleri .box
class 'ına eklenir. Yani burada son adım olan rotate(180deg) animasyon bitiminde
.box class 'ına aktarılır ve animasyon bitse bile .box class 'ı 180 derece döndrülmüş
şekilde kalmaya devam eder */

.box {
	animation-name: rotate;
  animation-duration: 3s;
	animation-fill-mode: forwards;
}

/* ek olarak backwards ve both özellikleride verilebilir ama kullanıam gerek yoktur. */
```

### animation-play-state()

İlgili animasyonun durdurulması veya oynatılması durumunu kontrol etmemizi sağlar.

```css
animation-play-state: running;  /* animasyon etkin, devam ediyor */
animation-play-state: paused;  /* animasyon durduruldu, devam etmiyor */

/* Javascript ile animasyonu durdurup, devam ettirebiliriz 
running ve paused adında iki class oluşturdum ve yukarıdaki methodları tanımladım.
Bu class 'ları butona her tıklandığında animasyon bulunan elemente ekleyerek animasyonu
durdurup veya yeniden başlatabiliriz.
*/

.paused{
  animation-play-state: paused;
}

.running{
  animation-play-state: running;
}

document.querySelector('#button').addEventListener("click", () => {
  let tt = document.querySelector('#animasyonDiv');
  if(tt.classList.contains("running")){
    tt.classList.remove("running");
    tt.classList.add("paused")
  } else {
    tt.classList.remove("paused");
    tt.classList.add("running")
  }
})
```

## Pseudo Elements

## ::after

Bir öğenin sonuna ekstra içerik veya stil özellikleri eklemek için kullanılır.

```css
<p class="text">Buraya herhangi bir metin girdim</p>

.text::after{
	content: "Metinden sonra bunu yazdım";
	color: red;
	margin-left: 4px;
}

.text::after{
	content: url(../images/bird.png);
	width: 150px;
	height: 150px;
	object-fit: cover;
}
```

## ::before

Bir öğenin başına ekstra içerik veya stil özellikleri eklemek için kullanılır.

```css
<p class="text">Buraya herhangi bir metin girdim</p>

.text::before{
	content: "Metinden önce bunu yazdım";
	color: red;
	margin-left: 4px;
}

.text::before{
	content: url(../images/bird.png);
	width: 150px;
	height: 150px;
	object-fit: cover;
}
```

### ::file-selector-button

Dosya seçme butonunun stil özelliklerini değiştirmek için kullanılır.

```css
<input class="fileBtn" type="file" name="avatar" accept="image/png, image/jpeg" />

.fileBtn::file-selector-button {
  background-color: black;
  color:white;
  border-radius: 8px;
}

/* eğer .fileBtn {..} içerisinde stil işlemleri yaparsak bu butonu etkilemez
butonun yanındaki "Dosya seçiniz" yazısının stilini etkiler. Button tasarımı için
::file-selector-button özelliğini kullanmamız gerekir. */
```

### ::first-letter

Bir öğenin ilk satırının ilk karakterinin stil özelliğini değiştirmek için kullanılır. Sadece text ögeleri için geçerlidir ve ilk eleman text olmalıdır.

```css
<p class="text">Buraya herhangi bir metin girdim</p>

/* B karakterine aşağıdaki stilleri uygular */
.text::first-letter {
	color: red;
	font-size: 28px;
	font-weight: bold;
}

/* ilk p etiketindeki ilk karakter "L" ilgili stilleri uygular */
<div class="text">
  <p>Lorem ipsum dolor sit</p>
  <p>Lorem ipsum dolor sit</p>
</div>
```

### ::first-line

Bir öğenin ilk satırına ilgili stilleri uygular.

```css
/* ilk p etiketindeki ilk karakter "L" ilgili stilleri uygular */
<div class="text">
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid, 
     doloremque eius ipsam laborum modi numquam quos reprehenderit. 
     Accusantium cum, dolore dolorum earum esse facilis, hic necessitatibus
     odit pariatur recusandae vitae.</p>
  <p>Lorem ipsum dolor sit</p>
</div>

/* ilk satıra ilgili stilleri uygular */
.text::first-letter {
	color: red;
	font-size: 28px;
	font-weight: bold;
}

```

### ::marker

li elementlerinin önüne ifade eklememizi veya var olan içeriği stillendirmemizi sağlar. Sadece liste elemanlarında çalışır.

```css
<ul class="list-items">
    <li class="list-item-1">test 1</li>
    <li class="list-item-2">test 2</li>
    <li class="list-item-3">test 3</li>
</ul>

.list-item-1::marker {
  content: "1=";
  color: red;
}
/* zaten bir içerik var ise bunu stillendirebiliriz */
.list-item-1::marker {
  color: red;
	background-color: blue;
}
```

### ::placeholer

input ve textarea gibi elementlerde tanımlanan placeholder text ‘inin stil özelliklerini belirtmemizi sağlar. placeholder ‘ı html etiketinde tanımladıktan sonra stil işlemleri uygulayabiliriz.

```css
<input type="text" class="input" placeholder="isim giriniz">

.input::placeholder{
  color:red;
	font-weight: bold;
}
```

### ::selection

Kullanıcı tarafından bir metin seçildiğinde, seçilen metine stil özellikleri uygulamamızı sağlar.

```css
<p class="text">Buraya herhangi bir metin girdim</p>

.text::selection {
	color: black;
  background-color: #EBB02D;
}
```

## Selectors

### :active

Kullanıcı bir elementin üzerine tıkladığında çalışır.

```css
button:active {
	color: red;
}
```

### :any-link

Bir öğede herhangi bir yönlendirici (href) var ise aktifleşir. Genellikle a etiketleri için kullanılır.

```css
<a class="link" href="#">Burası bir link</a>

/* href özelliği olan tüm a etiketlerine stil verdik */
a:any-link {
	color: blue;
	text-decoration: underline;
}
```

### :autofill

İnput elementlerinde tarayıcıda kayıtlı kullanıcı bilgilerinin otomatik doldurulması durumunda çalışır. Not: Kullanıcı input ‘da bir değişiklik yaparsa stiller kaldırılır.

```css
<input type="text" class="input" placeholder="isim giriniz">

/* Eğer kullanıcı bilgileri tarayıcıda kayıtlı ise ve kullanıcı bu alanları otomatik
doldurdu ise ilgili input elementlerinde stil uygulanır */
input:autofill {
	color: gray;
	background-color: green;
}
/* bu özelliği tarayıcı destekli kullanmak daha faydalı olacaktır */
input:-webkit-autofill {
	color: gray;
	background-color: green;
}
```

### :checked

Checkbox veya radio gibi input elementleri eğer işaretldi ise (checked) , ilgili stiller uygulanır.

```css
<input type="checkbox" name="active" id="check">

/* checkbox her stil 'i kabul etmez, bu checkbox ile ilgili bir durumdur */
input:checked {
  outline: 2px solid black;
}
```

### :default

Form elementlerinde default olarak tanımlanan değeri olan elementleri seçer.

```css
<input type="checkbox" name="active" id="check" checked>

/* inputlarda default olarak tanımlanmış değeri olan tüm elemanları seçer */
input:default {
  border: none;
  outline: 2px solid deeppink;
}
```

### :disabled

Bir form öğesi devre dışı bırakılmış, seçilemiyorsa, üzerine tıklanamıyorsa, içine yazılamıyorsa veya odak kabul edemiyorsa devre dışı kabul edilir ve devre dışı edilmiş elementleri seçer.

```css
<input type="checkbox" name="active" id="check" disabled>

input:disabled {
  outline: 2px solid red;
}
```

### :enabled

Bir form öğesi etkin ise , seçilebiliyor, üzerine tıklanıyor, içine yazılıyor veya odak kabul ediyor ise etkin kabul edilir ve etkin elementleri seçer. (`:disable` nin tersi)

```css
<input type="checkbox" name="active" id="check">

input:enabled{
  outline: 2px solid blue;
}
```

### :empty

İçeriği boş olan elementleri seçer. Bir elementin altında boşta olsa bir element var ise o elementi dolu kabul eder. Boşluk karakteri olan elementleri de dolu kabul eder.

```css
div:empty {
	height: 20px;
  width: 400px;
  border: 2px solid red;
}

<div></div>  /* empty element */

<div>
	<p></p>  /* no empty element */
</div>  

<div>    </div>  /* no empty element (spaces) */
```

### :first-child

Bir grup kardeş öğe arasından ilk öğeyi seçer. Önemli : bu seçicide kardeş öğelerin hepsinin aynı etikete sahip olması gerekir.

```css
<ul class="list-items">
  <li class="list-item">test 1</li>
  <li class="list-item">test 2</li>
  <li class="list-item">test 3</li>
</ul>

/* list-items class 'ının altındaki tüm li etiketlerinden ilk öğeyi seçiyorum */
.list-items > .list-item:first-child {
  color: red;
}

<ul class="list-items">
	<span >bu span etiketi</span>
  <p>bu p etiketi</p>
  <li class="list-item">test 1</li>
  <li class="list-item">test 2</li>
  <li class="list-item">test 3</li>
</ul>

/* bu çalışmaz çünkü alt elemanların hepsi li öğesi olmalıdır */
.list-items > li:first-child {
  color: red;
}
```

### :first-of-type

`:first-child` ‘daki alt ögelerin hepsinin aynı olması sorununu ortadan kaldırarak sadece ilgili elementlerin ilk elemanını seçer. Alt öğeler farklı olsa bile.

```css
<ul class="list-items">
	<span >bu span etiketi</span>
  <p>bu p etiketi</p>
  <li class="list-item">test 1</li>
  <li class="list-item">test 2</li>
  <li class="list-item">test 3</li>
</ul>

/* .list-items 'in altındaki sadece li elementlerindeki ilk öğeyi seçiyorum */
.list-items > li:first-of-type {
  color: red;
}
```

### :last-child

Bir grup kardeş öğe arasından son öğeyi seçer. Önemli : bu seçicide kardeş öğelerin hepsinin aynı etikete sahip olması gerekir.

```css
<ul class="list-items">
  <li class="list-item">test 1</li>
  <li class="list-item">test 2</li>
  <li class="list-item">test 3</li>
</ul>

/* list-items class 'ının altındaki tüm li etiketlerinden ilk öğeyi seçiyorum */
.list-items > .list-item:last-child {
  color: red;
}

<ul class="list-items">
	<span >bu span etiketi</span>
  <p>bu p etiketi</p>
  <li class="list-item">test 1</li>
  <li class="list-item">test 2</li>
  <li class="list-item">test 3</li>
</ul>

/* bu çalışmaz çünkü alt elemanların hepsi li öğesi olmalıdır */
.list-items > li:last-child {
  color: red;
}
```

### :last-of-type

`:last-child` ‘daki alt ögelerin hepsinin aynı olması sorununu ortadan kaldırarak sadece ilgili elementlerin son elemanını seçer. Alt öğeler farklı olsa bile.

```css
<ul class="list-items">
	<span >bu span etiketi</span>
  <p>bu p etiketi</p>
  <li class="list-item">test 1</li>
  <li class="list-item">test 2</li>
  <li class="list-item">test 3</li>
</ul>

/* .list-items 'in altındaki sadece li elementlerindeki ilk öğeyi seçiyorum */
.list-items > li:last-of-type {
  color: red;
}
```

### :nth-child

İlgili elementin kardeş elementlerini baştan başlayarak index sırasına göre seçer. 
**Not:** Altında birbirinden farklı etikette öğeler var ise doğru seçim için `:nth-of-type` kullan.

```css
<ul class="custom-list">
	<li>İtem 1</li>
  <li>İtem 2</li>
  <li>İtem 3</li>
  <li>İtem 4</li>
  <li>İtem 5</li>
  <li>İtem 6</li>
  <li>İtem 7</li>
  <li>İtem 8</li>
  <li>İtem 9</li>
  <li>İtem 10</li>
</ul>

/* li öğelerinden 2. sıradaki */
.custom-list > li:nth-child(2) {
  background-color: #EBB02D;
}

/* li öğelerinden çift sayıdakiler (item 2,4,6,8,10, bu seçim index numarasına göre)*/
.custom-list > li:nth-child(event) {
  background-color: #EBB02D;
}

/* li öğelerinden tek sayıdakiler (item 1,3,5,7,9 bu seçim index numarasına göre)*/
.custom-list > li:nth-child(odd) {
  background-color: #EBB02D;
}

/* sayısal işlemler ise kardeş öğe seçimi */
/* n değeri 0 dan başlayarak sonsuza kadar tüm pozitif tam sayıları içerir (0,1,2...)*/
.custom-list > li:nth-child(n) {
  background-color: #EBB02D;
}
/* [2*0 = 0],[2*1=2],[2*2=4] .. şeklinde çift sayıları temsil eder */
.custom-list > li:nth-child(2n) {
  background-color: #EBB02D;
}

/* [5*0 = 0],[5*1=5],[5*2=10] .. şeklinde 5 in katlarını temsil eder */
.custom-list > li:nth-child(5n) {
  background-color: #EBB02D;
}
```

### :nth-last-child

İlgili elementin kardeş elementlerini sondan başlayarak index sırasına göre seçer. Ters.

```css
<ul class="custom-list">
	<li>İtem 1</li>
  <li>İtem 2</li>
  <li>İtem 3</li>
  <li>İtem 4</li>
  <li>İtem 5</li>
  <li>İtem 6</li>
  <li>İtem 7</li>
  <li>İtem 8</li>
  <li>İtem 9</li>
  <li>İtem 10</li>
</ul>

/* li öğelerinden sondan 2. sıradaki (İtem 9) */
.custom-list > li:nth-last-child(2) {
  background-color: #EBB02D;
}

```

### :nth-of-type

Eğer bir elementin altındaki elementler farklı etiketlerde ise `:nth-child` doğru çalışmaz. Bu soruna çözüm olarak `nth-of-type` ile sadece ilgili etiketler arasında sıralamaya göre seçim yapar.

```css
<ul class="custom-list">
	<li>İtem 1</li>
  <li>İtem 2</li>
  <li>İtem 3</li>
  <li>İtem 4</li>
		<ul>
      <li>İtem 4.1</li>
      <li>İtem 4.2</li>
      <li>İtem 4.3</li>
      <li>İtem 4.4</li>
    </ul>
  <li>İtem 5</li>
  <li>İtem 6</li>
  <li>İtem 7</li>
  <li>İtem 8</li>
  <li>İtem 9</li>
  <li>İtem 10</li>
</ul>

/* İtem 4 ile İtem 8 'i seçecektir.
.custom-list > li:nth-of-type(4n) {
  background-color: #EBB02D;
}
```

### :only-child

İlgili elementin altında sadece 1 çocuk öğe var ise seçer.

```css
<ul>
	<li>İtem 1</li>
</ul>

<ul>
	<li>İtem 3</li>
	<li>İtem 4</li>
</ul>

/* ul etiketlerinden sadece 1 çocuğu olanın, çouğuna (li) ilgili stili uygular,
yani burada İtem 1 'in arkaplanını değiştirir.*/
ul > :only-child {
  background-color: #EBB02D;
}
```

### :focus

Kullanıcı bir öğeye odaklandığında çalışır. Form elementlerinde kullanışlıdır.

```css
<input type="text" class="input" placeholder="isim giriniz" >

input:focus {
  background-color: red;
}
```

### :focus-visible

Fare veya işaretçi ile değil de klavye ile gezinirken bir öğeye odaklandığında çalışır.

```css
<input type="text" class="input" placeholder="isim giriniz" >

input:focus-visible {
  background-color: blue;
}
```

### :focus-within

Kullanışlı ! Bir kapsayıcı öğenin alt öğelerinden birine odaklandığında kapsayıcı öğeyi seçmeyi sağlar.

```css
<div class="container">
	<p>ileri seviye css öğreniyorum</p>
	<span>github 'dan burakkrt 'yi takip etmeyi unutma :)</span>
	<input type="text">
</div>

/* container class 'ının altındaki harhangi bir öğeye odaklanma durumunda
.container 'e stil özellikleri uygular */

.container:focus-within {
	background-color: yellow;
}
```

### :hover

İlgili öğenin herhangi bir işaretçi ile üzerine gelindiğinde stil uygular.

```css
<p>burası bir p etiketidir</p>

p:hover{
	color: red;
}
```

### :in-range

Form elementlerinde belirtilen değer tanımlanan min ve max ‘değer aralığında ise yani karşılıyor ise stil uygular.

```css
<input type="number" min="1" max="100"  />

input {
	backgorun-color: red;
}
/* eğer girilen değe 1 ile 100 arasında ise ilgili stil uygulanır */
input:in-ranger {
	background-color: green;
}
```

### :out-of-range

Form elementlerinde belirtilen değer tanımlanan min ve max ‘değer aralığının dışında ise stil uygular.

```css
<input type="number" min="1" max="100"  />

input {
	backgorun-color: red;
}
/* eğer girilen değe 1 ile 100 arasında değil ise ilgili stil uygulanır */
input:out-of-range {
	background-color: green;
}
```

### :invalid

Form elementlerinde belirtilen değer tanımlanan min ve max ‘değer aralığında değilse yani karşılamıyor ise stil uygular. `:in-range` ‘nin tersi.

```css
<input name="age" type="number" value="5" min="18" />
<input name="secret" type="text" value="test" pattern="[a-z]+" />

input:invalid {
	outline: 2px solid red;
}
```

### :is

Belirli bir öğenin altındaki öğeleri seçmemizi sağlar. :first-of-type ‘dan daha kullanışlı ve yazımı rahattır.

```css
<ul class="list-items">
    <span >bu span etiketi</span>
    <p>bu p etiketi</p>
    <li class="list-item">test 1</li>
    <li class="list-item">test 2</li>
    <li class="list-item">test 3</li>
    <input type="text" class="input" placeholder="isim giriniz" >
</ul>

/* list-items altındaki elemanlardan etiketi li veya p olan elementleri seçer */
.list-items > :is(li,p) {
	border: 1px solid red;
}

<div class="container">
	<div>
		<p>beni github 'dan takip etmeyi unutma</p>
	</div>
  <ul class="list-items">
    <span >bu span etiketi</span>
    <p>bu p etiketi</p>
    <li class="list-item">test 1</li>
    <li class="list-item">test 2</li>
    <li class="list-item">test 3</li>
    <input type="text" class="input" placeholder="isim giriniz" >
  </ul>
</div>

/* container altındaki elementlerden class 'ı list-items olanın altındaki 
tüm p ve li etiketlerini seçer */
.container > :is(.list-items) > :is(p, li) {
  border: 1px solid red;
}
```

### :where

:is ile aynı özelliktedir, birden çok seçiciyi bir arada tanımlar.

```css
<ul class="list-items">
    <span >bu span etiketi</span>
    <p>bu p etiketi</p>
    <li class="list-item">test 1</li>
    <li class="list-item">test 2</li>
    <li class="list-item">test 3</li>
    <input type="text" class="input" placeholder="isim giriniz" >
</ul>

/* list-items in altındaki tüm span ve p etiketlerini seçer ve stil uygular */
.list-items > :where(p,span){
	color: red;
}
```

### :not

İlgili element ile eşleşmeyen diğer tüm elementleri seçer.

```css
<ul class="list-items">
  <span>bu span etiketi</span>
  <p>bu p etiketi</p>
  <li class="list-item">test 1</li>
  <li class="list-item">test 2</li>
  <li class="list-item">test 3</li>
  <input type="text" class="input" placeholder="isim giriniz" >
</ul>

/* list-items altındaki li elementi hariç tüm öğeleri seçer */
.list-items > :not(li) {
  color: yellow;
}

/* birden çok etiket, class, id belirtilebilir */
.list-items > :not(span, .list-item) {
  color: yellow;
}

/* ayrı ayrı da belirtilebilir */
.list-items > :not(span):not(li) {
  color: yellow;
}
```

### :lang

Html etiketlerinde belirtilmiş dilleri olan elementlere seçmemizi sağlar. Not: <html lang=”tr-TR”> tanımlanmış ise altındaki tüm öğelere stil uygular çünkü tüm sayfa tr-TR olarak tanımlanmıştır. Fakat sadece belirli etiketlere farklı lang etiketi uygulanmış ise sadece o elementlere stil uygular.

```css
<p lang="en-US">Hello, my name is Burak. I am a developer.</p>
<p lang="tr-TR">Selam, benim adım Burak. Ben bir geliştiriciyim.</p>

*:lang(tr-TR){
	color: red;
}

*:lang(en-US){
	color: blue;
}
```

### :link

Henüz ziyaret edilmemiş bağlantıları seçer.

```css
<a href="#">Click me</a>

/* henüz tıklanmadı ise uygular */
a:link {
	color: blue;
}
```

### :visited

Eğer bağlantı ziyaret edilmiş (açılmış) ise.

```css
<a href="#">Click me</a>

/* ziyaret edildikten sonra */
a:link {
	color: grey;
}
```

### :optional

Form elementlerinde bir form elementine içerik girmesini zorunlu kılmak için `required` (zorunlu) terimini etiket içerisinde belirtiriz. Zorunlu olmayan öğeleri seçer.

```css
<form>
	<input name="name" type="text" required />
	<input name="birth" type="date" />
	<select name="origin" required>
    <option>Google</option>
    <option>Facebook</option>
    <option>Advertisement</option>
  </select>
</form>

/* form öğesinin altındaki zorunlu olmayan elementeri seçer */
form > :optional {
	border: 2px solid grey;
}
```

### :required

Form elementlerinde bir form elementine içerik girmesini zorunlu kılmak için `required` (zorunlu) terimini etiket içerisinde belirtiriz. Sadece zorunlu öğeleri seçer.

```css
<form>
	<input name="name" type="text" required />
	<input name="birth" type="date" />
	<select name="origin" required>
    <option>Google</option>
    <option>Facebook</option>
    <option>Advertisement</option>
  </select>
</form>

/* form öğesinin altındaki zorunlu elementeri seçer */
form > :required{
	border: 2px solid grey;
}
```

### :placeholder-shown

Form elementlerinde placeholder öğesini görüntüleyen öğeleri seçer. Kullanıcı değer girmeye başladığı an stiller kaldırılır.

```css
<input type="number" placeholder="Bir sayı girin" >

/* placeholder bulunan öğelere ilgili stili uygular. Eğer kullanıcı inputa değer
girmeye başlarsa placeholder text 'i kaybolacağı için stiller de kaldırılır.
İnput içeriğini temizler&siler ise placeholder tekrar gözükeceğinden stillerde
tekrar yüklenir */
:input:placeholder-shown{
	outline: 2px solid orange;
}
```

### :ready-only

Sadece okunabilen, değer girilmeyen, değiştirilmeyen öğeleri seçer. 

```css
<div class="tt2">
  <a class="a1">dasdasdas</a>
  <a class="a2">dasdasdas</a>
  <select>
    <option>item 1</option>
    <option>item 2</option>
    <option>item 3</option>
  </select>
  <a class="a4">dasdasdas</a>
  <input type="text">
	<input type="checkbox">
</div>

/* input text ve checkbox değer girilebilir veya değiştirelebilir bunun haricinde
a etiketi ve select 'ler sadece okunabilir olduğu için, okunabilir ögeleri seçer */
*:ready-only {
	color: red;
}
```

### :ready-write

Sadece değer girelebilen ve seçilen öğeleri seçer.

```css
<div class="tt2">
  <a class="a1">dasdasdas</a>
  <a class="a2">dasdasdas</a>
  <select>
    <option>item 1</option>
    <option>item 2</option>
    <option>item 3</option>
  </select>
  <a class="a4">dasdasdas</a>
  <input type="text">
	<input type="checkbox">
</div>

/* input text ve checkbox değer girilebilir veya değiştirelebilir */
*:ready-only {
	color: red;
}
```

### :root

En üst kapsayıcı elemanı belirtir. Buda html elementine denktir. html elementine css değişkenlerini tanımlamak için kullanılır.

```css
/* html etiketine backgorund verebiliriz ve tüm sayfanın arkaplanı değişir */
:root {
	backgorund-color: orange;
}

/* değişken tanımlayabiliriz ve alt öğelerde çağırabiliriz, dinamik yapı oluşur */
:root {
	--main-color: black;
	--main-background: yellow;
}
/* color 'a --main-color adındaki değişkeni tanımladık yani black */
.box {
	color: var(--main-color)
}
```
