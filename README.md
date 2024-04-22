### What is **amqp**?
    
amqp atau Advanced Message Queuing Protocol (AMQP) adalah sebuah open standard application layer protocol untuk message-oriented middleware. AMQP dirancang untuk mendukung komunikasi yang handal, asinkron, dan aman *software components* yang terpisah.

Dalam konteks kode ini, AMQP digunakan untuk menghubungkan aplikasi ini dengan antrean pesan yang dipantau oleh `CrosstownBus` sehingga dapat mengirim dan menerima pesan dari antrean yang terhubung ke broker AMQP, dalam hal ini dijalankan lokal pada port 5672.
    

### What does **`guest:guest@localhost:5672`** mean? what is the first **guest**, and what is the second **guest**, and what is **`localhost:5672`** is for? 
   
`guest:guest@localhost:5672` menandakan connection string URI dalam format `<username>:<password>@<host>:<port>`:

1. `guest` yang pertama menandakan username pengguna yang dipakai untuk *authentication* di RabbitMQ server, biasanya default di RabbitMQ memang `guest` usernamenya.
2. `guest` kedua mewakili `password`nya. Di RabbitMQ, password defaultnya biasanya juga `guest`.
3. `localhost:5672` adalah hostname dan port number broker AMQP. Dalam kasus ini, localhost berarti broker berjalan pada mesin yang sama di mana kode dijalankan, dan 5672 adalah default port untuk komunikasi AMQP.