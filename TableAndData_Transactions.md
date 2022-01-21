## Sql Examples



#### Create - Drop Table and Data Manipulation(Update, Delete) Examples



##### dvdrental Database




```
test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```

> Create Table employee(id INTEGER,
>
> name VARCHAR(50),
>
> birthday DATE,
>
> email VARCHAR(100))



```
Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
```

> 1. Mockaroo.com' a girilir:
> 2. Mackaroo ya ilgili tablolar aşağıdaki görseldeki gibi belirlenir.
> 3. ![Mockaroo](/mockaroo.png)
>       - Burada rows kısmına kaç tane örnek istiyorsak yazılır.(50)
>       - Format seçmimi:  Dataları veritabanına aktarma yöntemimizi belirlemek için önemli zira bize 2 seçenek sunacak.
>           - Seçenek 1: Format kısmında Sql'i seçeceğiz ve tablo adını yazacağız. Ayrıca burada yeni bir tablo oluşturmamızı sağlayan bir checkbox da bulunuyor.Biz database oluşturmayı bir önceki adımda yaptığımız için bu adımda işaretlemedik.Sql'i seçersek(ben böyle yaptım) tablo ismine göre Insert Into komutları oluşur ve bu komutları preview'de görüntüleyebilir/kopyalayabiliriz ya da indiririz.
>           - Seçenek2 : CSV formatını kullanırsınız ve dataları indirirsiniz. Bu kısımda Create Database seçeneği yoktur.
>  4. ![pgadmin](/pgadmin.png)
>       - Bu adımda test database'inde bulunan employee tablosuna oluşturduğumuz dataları ekleyeceğiz.
>       - Eğer Seçenek 1 i kullanarak Sql Raw formatında dataları aldıysanız(kopyalayarak veya indirme yöntemiyle) Görseldeki panelde test-> tables içerisinde ilgili tabloya sağ clik ile Query Tool'u seçeriz ve sorgularımızı buraya taşıyarak çalıştırırız.
>       - Seçenek 2 yi kullanıyorsanız pgadmin görselindeki Import/Export a girerek indirilen dosyayı format tipini CSV yaparak seçeceğiz ve içeriye aktarmış olacağız.
>       - Select * from employee sorgusuyla verilerin gelip/gelmediğini kontrol edelim.
>   5. Eğer hata alıyorsak id'nin primary olarak tanımlanmadığından(oluşturduğumuz database e göre anlatıyorum, eğer id primary key ise mockaroo da id kısmını kaldırın ve sorguları böyle oluşturun.) ve sütunların doğru veri tipinde olduğundan emin olun.
>   6. İşlemimiz tamam.


```
Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```

> Update employee SET name='NewName' where id=3
> Update employee SET name='NewName',email='Newmail@gmail.com' where name='xx' and email='xyz@hotmail.com'
> Update employee SET name='xyz' where id=7
> Update employee SET name='MyName',birthday='1997-03-19' where name='prz' and birthday='2021-10-19'
> Update employee SET email='istanbul@ibb.gov' where email='emailis@requirement.com'


```
Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```


> 1. Delete from employee where id=5
> 2. Delete from employee where email='ekirwin14@admin.ch'
> 3. Delete from employee where name='Nolie' **aynı isimde birden fazla kişi varsa hepsini siler**
> 4. Delete from employee where birthday='2021-09-26'
> 5. Delete from employee where name='Cordey' and birthday='2021-05-29'

