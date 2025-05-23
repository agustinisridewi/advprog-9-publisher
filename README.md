# advprog-9-publisher
Agus Tini Sridewi / 2306276004/ ADPRO A

#### a. How much data your publisher program will send to the message broker in one run?

Program publisher mengirim 5 pesan ke message broker. Setiap pesan berukuran sekitar 17 byte (terdiri dari user_id 1 byte dan user_name 16 byte). Jadi, total data yang dikirim adalah sekitar:
5 pesan x 17 byte = 85 byte

#### The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

URL amqp://guest:guest@localhost:5672 berarti:
- amqp://: Protokol yang digunakan (AMQP).
- guest:guest: Username dan password untuk autentikasi.
- localhost: Host tempat broker AMQP (seperti RabbitMQ) berjalan, yaitu di mesin lokal.
- 5672: Port yang digunakan broker untuk koneksi AMQP.
Ini menunjukkan bahwa publisher dan subscriber menghubungkan ke broker AMQP di mesin lokal menggunakan kredensial default (guest:guest) dan port 5672.

#### Preparing Message Broker (RabbitMQ)
![alt text](image.png)

#### Sending and processing event
![alt text](image-1.png)
![alt text](image-2.png)
-> Publisher dan subscriber terhubung ke server RabbitMQ yang sama. Jadi, setiap kali publisher mengirimkan data, subscriber akan menerimanya.

#### Monitoring chart based on publisher
![alt text](image-3.png)
-> Saat kita menjalankan publisher, lebih banyak pesan yang dipublikasikan ke broker. Lonjakan ini menunjukkan peningkatan mendadak dalam laju pengiriman pesan dari publisher ke broker dan kemudian disampaikan ke subscriber.