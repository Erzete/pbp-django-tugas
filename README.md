# Jawaban Tugas

## Tugas 2
Link : https://tugas2-rt.herokuapp.com/katalog/

1. https://ibb.co/X5SmKD6
2. Kita tetap bisa membuat aplikasi web berbasis Django tanpa menggunakan virtual environment tetapi tentunya akan lebih baik menggunakan Virtual environment
   Hal ini dikarenakan kita membutuhkan semacam sekat/batasan untuk setiap proyek Django, sehingga satu proyek dengan proyek lainnya tidak akan terganggu. Hal
   ini juga akan mencegah error ketika misalnya ada proyek yang menggunakan versi/dependencies yang berbeda.
3. Bagaimana cara saya melakukan tahap 1-4? Simpelnya ya tentu saja dengan tinggal mengikuti tutorial 2 yang telah ada. Kemudian saya ubah beberapa method, variabel
   yang ada untuk menyesuaikan dengan proyek katalog dan bukan wishlist (seperti nama method show_wishlist menjadi show_katalog dan menambahkan npm pada views. 
   Kemudian tentunya karena datanya berbeda saya juga harus menambahkan beberapa hal pada models.py Mungkin seperti itu saja sama dengan lainnya seperti .html
   Ketika deployment-nya saya mengalami  beberapa isu karena ketidakmen gertian saya terhadap Heroku. Akan tetapi, akhirnya saya bisa menemukan yang mana yang salah 
   sehingga saya bisa men-deploy project django ini ke Heroku.
   
## Tugas 3
Link : https://tugas3-rt.herokuapp.com/mywatchlist/html/, https://tugas3-rt.herokuapp.com/mywatchlist/xml/, https://tugas3-rt.herokuapp.com/mywatchlist/json/

Postman : https://imgur.com/a/FLAKjR0

1. JSON = Buat merepresentasikan objek, tidak ada end tag, ga bisa komen di file-nya, cuma bisa pake UTF-8 encoding
   XML = Dynamic, Markup language, menyimpan dan membawa data, ada start dan end tag, bisa komen, bisa pake encoding selain UTF-8, nama tags-nya bisa ditentukan                sendiri oleh user
   HTML = Static, fokusnya lebih ke tata (representasi) objek, teks, dan data pada web, bisa komen, bisa pake encoding lain dari UTF-8, tags 
          dalam HTML udah ada dari sananya., ada end tag tapi ga harus
2. Data delivery penting karena data ada bermacam-macam bentuknya baik dalam .json, .xml, .html, dan lain sebagainya. Pada kalanya data yang ada pada suatu file data      kita ingin untuk load atau direpresentasikan pada file data lainnya, ini salah satu pentingnya data delivery. Selain itu, dengan data delivery jika suatu data          membutuhkan data yang lain maka data itu akan tersedia.
3. Awal saya buat dulu app nya memakai 
   > python manage.py startapp mywatchlist
   
   Kemudian saya melakukannya seperti hal yang ada pada Lab 1 dan 2 bedanya di folder mywatchlist models.py saya isi dengan atribut yang ada pada soal. Kemudian saya      juga membuat initial_mywatchlist_data.json yang isinya 10 film beserta atributnya sesuai dengan yang ada pada models.py jangan lupa sama seperti lab 2 kita akan        menampilkan xml dan json-nya. Kemudian pada test.py saya mencoba untuk mengakses ketiga function yang ada pada views.py, semuanya udah OK. 
  
## Tugas 4
Link : https://tugas4-rt.herokuapp.com/todolist/ (Error di Heroku saat login, jalankan di localhost)
1. Kegunaan dari csrf_token sesuai namanya adalah sebagai proteksi website terhadapt Cross Site Request Forgeries. Jika pada laman terdapat kelemahan seperti yang        telah disebutkan maka suatu user bisa saja menjalankan hal yang mereka sebenarnya tidak inginkan terjadi seperti menghapus akun user ataupun hanya sekedar me-logout    user dari akunnya.
2. Ya tentu saja bisa, kita tinggal membuatnya dengan <form></form> isi body form tersebut terdiri dari label (untuk menunjukkan apa yang perlu diisikan user) dan        input beserta tipe input yang kita inginkan dari user.
3. Setelah kita mengisi form yang terdapat pada html, isian tersebut akan disimpan oleh database yang berisi objek-objek yang dimiliki oleh Task. Nah, ketika kita        ingin memunculkannya kita tinggal me-request data tersebut menggunakan show_todolist, objek Task akan difilter sesuai dengan user yang sedang logged in kemudian        akan dimunculkan dengan render
4. Untuk register, login, logout kurang lebih sama dengan yang ada di tutorial3, namun untuk show_todolist kita tidak akan memunculkan semua objek Task melainkan          difilter berdasarkan user yang sedang login. Kemudian saya tambahkan function add_task pada views yang berguna untuk menambah objek Task, function ini akan            bekerjasama form.html dan juga forms.py untuk menyimpan data tersebut. Jangan lupa tambahkan button tambah task baru yang akan meng-redirect user ke halaman yang      berisi form.html

## Tugas 5 (Late)
Link : https://tugas4-rt.herokuapp.com/todolist/ (Error di Heroku saat login, jalankan di localhost)

1. Inline CSS : Setiap tag dalam file html ditulis stylenya masing-masing. (Kekurangan) Paling tidak efektif karena harus menulis style setiap tag html, waktu loading                 lebih lama. (Kelebihan) Tidak perlu bikin file css, cocok untuk html singkat atau untuk nyoba-nyoba.
   Internal CSS : Style CSS-nya ditulis di setiap file HTML-nya. (Kekurangan) Tidak efektif karena setiap HTML harus ditulis CSS-nya, waktu loading bisa lebih lama.                     (Kelebihan) Tidak perlu load file CSS, bisa pake class dan ID selector.
   External CSS : Membuat file CSS, terus di-load ke file HTML. (Kekurangan) Perlu meload file CSS-nya, bisa makan waktu (Kelebihan) Paling efektif jika punya banyak                     file html, satu untuk semua, lebih rapih karena tidak beda-beda.
2. <button>, untuk bikin button. <a> buat nambahin link pake href. <head> menunjukkan itu bagian head html. <body>, menunjukkan itu bagian badan html. <nav> Untuk buat navbar. <h(1-6)> buat tulisan. <table> buat bikin tabel. Dan lain sebagainya.
3. (Gak ada yang saya ketahui, jawaban ini diambil dari google) ID selector (#..), akan mengubah style semua tag yang memiliki id ini. Element selector, akan mengubah style semua element yang memiliki tag tersebut (contoh, table, a, dan lainnya. Class selector, akan mengubah style semua element yang memiliki Class tersebut (class=".."). Universal selector (*), berlaku ke seluruh tag.
4. Saya mulai dari todolist.html, menambahkan line untuk load bootstrap-nya terlebih dahulu kemudian saya mengubah task yang tadinya direpresentasikan sebagai tabel      diubah menjadi card. Kemudian karena masih belum rapi saya ke tengahkan card tersebut menggunakan row jangan lupa tambahin md dan mt biar tidak ada card yang nempel    satu dengan lainnya. Terakhir button-nya juga saya ubah button menjadi ke tengah dan diberikan warna. Selanjutnya dibagian register di sini masih ada yang kurang      saya tidak tahu kenapa tapi tidak bisa ditunjukkan message-nya padahal di login muncul. Untuk ketiga login, register, dan form mirip yaitu tinggal membuat form        group, untuk name serta id pada tag tersebut saya mengambil dengan meng-inspect element html yang terdapat pada tugas 4 lalu tinggal diganti-ganti saja sesuai          dengan format bootstrap. Untuk deskripsi pada form menggunakan textarea.

## Tugas 6 (Late)
1. Asinkronus : Pengguna tidak harus me-refresh laman untuk mendapatkan data terbarunya, masih bisa berinteraksi dengan web tersebut selama data di-load
   Sinkronus : Untuk mendapatkan data terbaru, laman harus di-refresh oleh user.
2. Event-driven-programming adalah paradigma programming yang berfokus pada event dan alur jalan programnya ditentukan oleh event yang dibuat oleh user. User didorong    untuk berinteraksi dengan web/aplikasi tersebut untuk membuat event2 tersebut. Contohnya pada tugas ini adalah Tombol "Submit Task" yang akan menjalankan              addTodolist
   ketika ditekan.
3. AJAX akan membuat halaman web memperbarui datanya secara asinkronus dengan mengirimkan data ke server di balik layar, AJAX menggunakan browser untuk meminta data      dari web server dan JavaScript, menggunakan XML/JSON untuk mengirim data, serta HTML DOM untuk menampilkan data. 
4. Untuk GET, saya menggunakan getJSON untuk mengambil json yang ada di todolist/show_json, kemudian saya akan me-loop setiap data yang ada pada json tersebut untuk
   membuat Card yang sesuai dengan format pada tugas sebelumnya dan nanti hasilnya akan ditampilkan pada laman. Untuk POST, saya membuat fungsi add pada views.py yang
   isinya kurang lebih sama dengan fungsi add_task yang telah dibuat sebelumnya kemudian saya membuat url baru bernama todolist/add, todolist/add ini nantinya akan
   digunakan pada script di todolist.html. Kemudian di bagian script pada todolist.html akan dibuat 3 fungsi yaitu getTodolist, refreshTodolist, dan addTodolist. 
   getTodolist akan mengambil data dari show_json, refreshTodolist akan me-refresh todolist secara asinkronus, dan addTodolist akan digunakan untuk menambahkan
   data pada todolist. addTodolist akan berjalankan ketika kita memencet tombol Submit Task pada modal Add Task, setelah dipencet maka akan menjalankan                    refreshTodolist.
   
Mungkin itu saja, terima kasih telah membaca README ini
Salam,
Rama Tridigdaya
