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
