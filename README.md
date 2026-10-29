# ДЗ Урок 6
---

***1. Аудит хэшей пользователей***
```
Определить тип хэша  sha-256
user:MILO2008
admin:hxtour
web_admin:t061584
root:washington1776
db_user:mmr431723
```

***2. Оптимальный подбор PIN-код***

---
```
 тип хэша SHA512
5d25e48a3d92c398bb6a7873d6a22281f6bdd50f78956f666f717135190127cbbeec3fd35b9fb03925d6bf595baa022d10d247104cced3a0a8f4a6656c4bf6a:5472
684a71e209bad7d9c3a802386150a24b31be323e7e42624bbe787e381cfe0796820fb1aeabb45ec966c6e427babb5ece40824297dac97c37f2e41be6958ea324:497235
8f2090b09018f7431d25a92da885c6f3e80ea538778639072aa15b7484b44d92ecb6cae59350f3bd1846ab492e8604f8d3b25f0e5842c2335b0b03bae5e690c0:11082
7765080f31bffe1d14ff17db9316b538db5761ea5592454f3d7a71961567af39e91c1c60898bda23f0c6514b0c6ff8e3c830a22846fe1af94b2d6023c89449a1:4653
7c3a635c9bbedd8f74ddb9cdcea921368e728b6f65cdae7a6eec537748cf8831e57a8706494220b9caf695b4cb79aa655c7c6b635b49c1fdc318ea410c0ae49f:17456

john --format=raw-sha512 --incremental=Digits --min-length=4 --max-length=6 hash.txt  
Using default input encoding: UTF-8
Loaded 5 password hashes with no different salts (Raw-SHA512 [SHA512 512/512 AVX512BW 8x])
Warning: poor OpenMP scalability for this hash type, consider --fork=8
Will run 8 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
5472             (?)     
11082            (?)     
4653             (?)     
17456            (?)     
497235           (?)     
5g 0:00:00:01 DONE (2026-10-29 22:21) 3.759g/s 739127p/s 739127c/s 1663KC/s 478958..98751
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
```

***3. Атака с учётом соли***

---
```
SHA-256,
Результат: 
user → 54cami9
admin → 431728dst 
web_admin → 662610
root → ruddrooney 
db_user → cutecsly 
```

***4*. Взлом MD5 через радужные таблицы ***

---
```
d1e576b71ccef5978d221fadf4f0e289	md5	superpassword
22d7fe8c185003c98f97e5d6ced420c7	md5	qwertyui
8a24367a1f46c141048752f2d5bbd14b	md5	P@ssw0rd!
8344711654700fe530f0d2ac74599a48	md5	aezakmi
a67e565b11cd18f7a922b58f5476b569	md5	hesoyam

https://crackstation.net
https://hashes.com/en/decrypt/hash
```
