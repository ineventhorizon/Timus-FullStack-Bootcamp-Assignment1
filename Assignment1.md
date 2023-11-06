 **1**. **Javascript nedir ve tarihsel gelişiminden bahsedin**.
 JavaScript, web tarayıcılarında kullanılan bir programlama dilidir. Web sayfalarına dinamiklik kazandırmak, kullanıcı etkileşimi sağlamak, veri işleme, form doğrulama gibi birçok görev için kullanılır. 
 1995 yılında bir scripting language olarak Mocha ismi altında tasarlandı, daha sonrasında LiveScript en sonunda da günümüzdeki adını alan JavaScript adını aldı. Normal bir programlama dili aksine scripting dillerin farkı derlenmesine gerek olmamasıydı. Zamanla daha kullanıcı dostu oldu. Web 2.0'ın gelişmesi ile birlikte kullanımı hızlandı ve popülerleşti. Halen geliştirilmeye devam eden JavaScript her versiyonunda yeni bir özellikle karşımıza çıktı. Şuanda tarayıcılar haricinde Node.js gibi frameworkler sayesinde sunucu tarafında da kullanılıyor.

 **2. Java ile JavaScript arasındaki fark nedir?**
 Java ile JavaScript adları dışında pek bir benzerlikleri yoktur. Her ikisi de farklı ihtiyaçları karşılayan farklı programlama dilleridir. En önemli farkı ise Java normal bir programlama dili olarak çalıştırmak için derlenmeye ihtiyaç duyarken JavaScript bir scripting dili olduğu için böyle bir gereksinimi yoktur.

 **3. JavaScript'teki veri tipleri nelerdir açıklayınız.**
 JavaScript'teki data tiplerini iki ana kategoriye ayırabiliriz; Primitive data tipleri ve Non-Primitive data tipleri olarak. Primitive Data tiplerinde, Number, String, Boolean, Null, Undefined ve Symbol yer alırken Non-Primitive data tiplerinde ise Object yer alır. 

1. **Number**:Number veri tipi sayısal değerleri göstermek için kullandığımız bir veri tipidir. Tam sayı değerler dışında ondalık sayılar da bu kategoriye girer.

   ```javascript
   var x = 12;     // Tam sayı
   var y = 3.14;   // Ondalık sayı
   ```

2. **String**: Metin verilerini göstermek için kullandığımız veri tipidir. 

   ```javascript
   var name = "Yusuf Ekrem Keçilioğlu"; // " ", kullanıldığı gibi string ifadelerini belirtmek için ' ' kullanılabilir.   
   ```

3. **Boolean**: Sadece iki değer bulundurabilen bir veri tipidir. Bu tutulan veriler sadece doğru ve yanlış gibi değerler olarak tanımlanabilir. Genellikle mantık ve koşullu ifadelerin tanımında kullanılırlar. 

   ```javascript
   var isTrue = true;
   var isFalse = false;
   ```

4. **Undefined**: Bir değişken tanımlandığında fakat bir değer atanmadığında aldığı veri tipidir. Fonksiyon parametrelerinde parametre olarak verilmeyen değerler yerine geçen default değer de undefined olarak geçer. 

   ```javascript
   var x;  // Tanımlandı fakat herhangi bir değer atanmadı, değeri Undefined olur.
   ```

5. **Null**: Herhangi bir değeri olmadığını belirten veri tipidir. Undefined ile karıştırılmaması gerekir, Null kasti olarak boş bırakılırken Undefined atanmayan bir değer olduğu anlamına gelir.

   ```javascript
   var x; // Undefined değer
   var y = null;  // Null değer
   ```

6. **Symbol**: ES6 ile gelen semboller, unique ve değiştirilemez değerlerdir. Genelde objelerin property keylerini tanımlamada kullanılır. 
   ```javascript
   var uniqueSymbol = Symbol("unique");
   ```

7. **Object**:Objeler karmaşık veri yapılarıdır ve key-value çifti olarak tutulur. Nesneler, fonksiyonlar, diziler vb. gibi çeşitli veri tiplerini içerebilirler. Non-primitive bir data tipidir. 
   ```javascript
   var person = {
       name: "Yusuf",
       age: 26,
       city: "Eskişehir"
   };
   ```


**4. null ile undefined arasıdaki fark nedir açıklayınız.**
Null kasti olarak boş bırakılan bir değere karşılık gelirken Undefined atanmayan bir değer olduğu anlamına gelir.
   ```javascript
   var x; // Undefined değer
   var y = null;  // Null değer
   ```

**5. NaN nedir açıklayınız.**
NaN, Not a number yani sayısal olmayan bir değer demektir. 
 ```javascript
 var y = 3 + 'x'; // Number(y) yapmaya çalıştığımızda NaN değerini almış oluruz.
   ```
**6.JavaScript’te yorum satırı eklemenin kaç farklı yolu vardır?**
Çoklu satır ve tek satır olarak yorum ekleyebiliriz. Örnek; 
```javascript
 // Tek satır yorumlar için
   
 /* Birden fazla
 satır
 yorumlar için *\
   ```
**7.Global değişken ne demektir açıklayınız.**
Global scope'ta tanımlanan değişkenlere verilen addır. Global scope'un içindeki tüm scopelarda bu değişkenlere erişilebilir olur.

```javascript
var globalValue = 3; //Bu değişkenle aynı scopeta her yerden erişilebilir. Global Değişkendir.
   ```

**8.JavaScript’te this anahtar kelimesi nedir açıklayınız**
This keyword'ü farklı yerlerde farklı anlamlara gelebilir. 
Global scope'ta tanımlanan this global nesneye karşılık gelir. Tarayıcılarda bu this window olurken Node.js kapsamında bu değer global'e işaret eder. Bir sınıf veya doğrudan obje tanımı içinde kullanılan this ise oluşturulan objeye/class'a işaret eder. 

```javascript
console.log(this); // Tarayıcılarda window'u işaret ederken Node.js'te globali işaret eder.
   
function Person(name) {
    this.name= name;
}
var myPerson = new Person("Yusuf"); // 'this' 'myPerson'a işaret eder
   ```


**9. == ile === farkını örnekler ile açıklayınız.**

== type farketmeksizin veri dönüşümü yaparak değerleri karşılaştırmayı yaparken, === operatörü ise değerler yanında veri dönüşümü yapmadan karşılaştırılan verilerin type'larını da karşılaştırır.

```javascript
5 == "5";  // Doğru olarak döner
5 == 5;  // Doğru olarak döner

5 === "5";  // Yanlış olarak döner
5 === 5;  // Doğru olarak döner
   ```


**10. let var const farkını tablo yapınız.**

| | var | let| const|
|--|--|--|--|
|  Block Scope| - |+|+
|  Global Scope| + |-|-
|  Function Scope| + |+|+
|  Değer değiştirme| + |+|-
|  Tekrar tanımlama| + |-|-


**11. Arrow fonksiyonun normal fonksiyondan farkları nelerdir**

Arrow functionlar içinde arguments objesine erişim sağlanamaz iken normal fonksiyonlarda fonksiyonun argümanlarına arguments ile erişim sağlanılabilir.
Diğer bir farkı ise, arrow function'lar this keyword'ü ile global scope'u işaret ederken normal fonksiyonlar kendi scope'unu işaret eder.

**12. Switch bloğu içinde hatasız nasıl değişken tanımlanır?**
Switch bloğunda her case'de değişken tanımlamak istiyor isek bu değişkenlerin her birinin adı farklı olması gerekir. Eğer bir değeri değiştirmek istiyorsak Switch case'den önce değişken tanımlanalarak içi doldurulur.
   
```javascript
var count = 2
let result;
switch (count) { 
	case  1: 
		result = 'one'; 
		break; 
	case  2: 
		result = 'two'; 
		break; 
	default: 
		result = null; }
		
console.log(result); //Çıktı 'two' olur.
   ```

**13. Pure fonksiyon ne demektir açıklayınız**
 Pure fonksiyonlar aldıkları argümanlar üzerinde herhangi bir etkisi olmayan, üzerlerinde hiçbir değişiklik yapmayan fonksiyonlara verilen addır.

```javascript
function sum(a, b){
return a + b} // Pure fonksiyona bir örnek.
   ```
   
**14. Rest operatör nedir örnekle açıklayınız**
Rest operatörü belirsiz sayıda değişkeni bir dizi olarak kabul etmesine yarar ve bunu tanımlamayı sağlar. Örneğin:

```javascript
function f(a, b, ...theArgs) {
  // ...
}
f(1, 2, 3, 4, 5, 6, 7) 
   ```

**15. Object destructuring nedir örnekle açıklayınız**
Destructuring bir object veya bir array içinden her elemanın başka bir değişken içine kaydedilmesine verilen addır. 

```javascript
const example { name: 'Yusuf', age:26}
const name = example.name
const age = example.age
// Ya da 
const {name, age} = example
//Şeklinde destructuring yapılabilir.
   ```
**16. 2 elemanlı bir objeyi 6 farklı şekilde oluşturunuz.**

--