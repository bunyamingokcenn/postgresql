Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.

    ```sql
        CREATE TABLE employee(
	        id SERIAL,
	        name VARCHAR(50),
	        birthday DATE,
	        email VARCHAR(100)
        );

    ```

2. Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

    ```sql 
        insert into employee (name, birthday, email) values ('Constance Crookall', '1909-05-19', 'ccrookall0@imdb.com');
        insert into employee (name, birthday, email) values ('Dorisa Hatchett', '1968-10-08', 'dhatchett1@yolasite.com');
        insert into employee (name, birthday, email) values ('Johnnie Zarfai', '1911-12-06', 'jzarfai2@so-net.ne.jp');
        insert into employee (name, birthday, email) values ('Sal Campaigne', '1936-07-23', 'scampaigne3@stumbleupon.com');
        insert into employee (name, birthday, email) values ('Michelle Stolting', '1994-07-25', 'mstolting4@jiathis.com');
        insert into employee (name, birthday, email) values ('Legra Loxley', null, 'lloxley5@home.pl');
        insert into employee (name, birthday, email) values ('Brigham Bleakley', '1998-11-04', 'bbleakley6@oaic.gov.au');
        insert into employee (name, birthday, email) values ('Tanner McCrystal', null, 'tmccrystal7@livejournal.com');
        insert into employee (name, birthday, email) values ('Veriee Savary', '2003-05-12', 'vsavary8@opensource.org');
        insert into employee (name, birthday, email) values ('Ricki Szymon', '1954-12-25', 'rszymon9@51.la');
        insert into employee (name, birthday, email) values ('Bartel Adamovsky', '1962-09-29', 'badamovskya@etsy.com');
        insert into employee (name, birthday, email) values ('Bethina MacScherie', null, 'bmacscherieb@1und1.de');
        insert into employee (name, birthday, email) values ('Cicily Kubecka', null, 'ckubeckac@msu.edu');
        insert into employee (name, birthday, email) values ('Aube Stansbie', '1925-12-22', 'astansbied@hexun.com');
        insert into employee (name, birthday, email) values ('Anthony McCloid', '1986-07-28', 'amccloide@skype.com');
        insert into employee (name, birthday, email) values ('Pauletta Georgelin', null, 'pgeorgelinf@ucla.edu');
        insert into employee (name, birthday, email) values ('Nap Bushnell', '1982-01-28', 'nbushnellg@behance.net');
        insert into employee (name, birthday, email) values ('Amargo Baroch', '1911-08-13', 'abarochh@ibm.com');
        insert into employee (name, birthday, email) values ('Oralle Praton', '1967-08-10', 'opratoni@nyu.edu');
        insert into employee (name, birthday, email) values ('Lukas Corzor', '1981-01-27', 'lcorzorj@multiply.com');
        insert into employee (name, birthday, email) values ('Dwight Sprulls', null, 'dsprullsk@multiply.com');
        insert into employee (name, birthday, email) values ('Odessa MacKeogh', '1963-02-28', 'omackeoghl@theatlantic.com');
        insert into employee (name, birthday, email) values ('Kit Clilverd', null, 'kclilverdm@hugedomains.com');
        insert into employee (name, birthday, email) values ('Leone Kamenar', '1929-10-17', 'lkamenarn@pagesperso-orange.fr');
        insert into employee (name, birthday, email) values ('Bryn Batham', '1910-08-24', 'bbathamo@dailymail.co.uk');
        insert into employee (name, birthday, email) values ('Quinta Kornas', '1956-05-13', 'qkornasp@nbcnews.com');
        insert into employee (name, birthday, email) values ('Roldan Silverthorn', '1931-08-12', 'rsilverthornq@wordpress.org');
        insert into employee (name, birthday, email) values ('Georgeanne Dunton', '1902-04-02', 'gduntonr@hud.gov');
        insert into employee (name, birthday, email) values ('Bertine Enrdigo', '1980-11-17', 'benrdigos@mozilla.com');
        insert into employee (name, birthday, email) values ('Cora Headford', '1902-09-03', 'cheadfordt@unblog.fr');
        insert into employee (name, birthday, email) values ('Fallon Suart', '1913-12-01', 'fsuartu@squarespace.com');
        insert into employee (name, birthday, email) values ('Lila McKelloch', '1983-02-12', 'lmckellochv@nyu.edu');
        insert into employee (name, birthday, email) values ('Priscella Hartmann', '1916-06-26', 'phartmannw@furl.net');
        insert into employee (name, birthday, email) values ('Willi Cossans', null, 'wcossansx@moonfruit.com');
        insert into employee (name, birthday, email) values ('Maurene Janousek', '1916-12-01', 'mjanouseky@meetup.com');
        insert into employee (name, birthday, email) values ('Gerrie Strowlger', '1995-01-12', 'gstrowlgerz@theguardian.com');
        insert into employee (name, birthday, email) values ('Josee Taber', '1976-06-21', 'jtaber10@indiegogo.com');
        insert into employee (name, birthday, email) values ('Elysee Piniur', null, 'epiniur11@free.fr');
        insert into employee (name, birthday, email) values ('Heddie Dawber', '1949-10-24', 'hdawber12@nifty.com');
        insert into employee (name, birthday, email) values ('Patrice Chess', '1918-04-28', 'pchess13@netvibes.com');
        insert into employee (name, birthday, email) values ('Ernestus Atwel', '1945-06-11', 'eatwel14@goo.gl');
        insert into employee (name, birthday, email) values ('Austine Jacobowitz', '1957-02-21', 'ajacobowitz15@google.ca');
        insert into employee (name, birthday, email) values ('Rora Atwool', '1935-09-02', 'ratwool16@yolasite.com');
        insert into employee (name, birthday, email) values ('Minnaminnie Byrne', '1940-08-29', 'mbyrne17@angelfire.com');
        insert into employee (name, birthday, email) values ('Nelson Fenwick', '1973-12-15', 'nfenwick18@sfgate.com');
        insert into employee (name, birthday, email) values ('Florry Guiraud', '1981-09-28', 'fguiraud19@bandcamp.com');
        insert into employee (name, birthday, email) values ('Brennan Dreinan', '1965-12-02', 'bdreinan1a@ebay.com');
        insert into employee (name, birthday, email) values ('Hilliard Bohills', '1964-04-30', 'hbohills1b@geocities.com');
        insert into employee (name, birthday, email) values ('Walker Lisciardelli', '1911-01-15', 'wlisciardelli1c@ebay.com');
        insert into employee (name, birthday, email) values ('Vance Yaknov', '1929-06-24', 'vyaknov1d@vinaora.com');
        
    ```

3. Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.

    ```sql 
        UPDATE employee
        SET name = 'UPDATED NAME'
        WHERE name = 'Ricki Szymon'
        RETURNING *;
        
        UPDATE employee
        SET name = 'Test Person'
        WHERE name = 'Nelson Fenwick'
        RETURNING *;
        
        UPDATE employee
        SET birthday = '1995-01-12'
        WHERE name = 'Heddie Dawber'
        RETURNING *;
        
        UPDATE employee
        SET email = 'mjanouseky@meetup.com'
        WHERE name = 'Lila McKelloch'
        RETURNING *;
        
        UPDATE employee
        SET birthday = '1964-04-30'
        WHERE name = 'Georgeanne Dunton'
        RETURNING *;
 
    ```
4. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

    ```sql 
        DELETE FROM employee
        WHERE id = 8
        RETURNING *;
        
        DELETE FROM employee
        WHERE name = 'Veriee Savary'
        RETURNING *;
        
        DELETE FROM employee
        WHERE id = 16
        RETURNING *;
        
        DELETE FROM employee
        WHERE name = 'Odessa MacKeogh'
        RETURNING *;
        
        DELETE FROM employee
        WHERE email = 'bdreinan1a@ebay.com'
        RETURNING *;

    ```
