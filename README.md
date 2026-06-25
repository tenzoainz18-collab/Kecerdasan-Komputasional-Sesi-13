**1)Apa yang dimaksud dengan State, Action, dan Reward dalam Reinforcement Learning?**

**State**

* Adalah suatu kondisi dimana berdasarkan persepsi AGEN,dalam Code Berikut terdapat 16 state (grid 4x4)
<img width="497" height="32" alt="image" src="https://github.com/user-attachments/assets/b40317b4-1a0e-4434-a7b5-05fccd8e95cf" />

<img width="221" height="23" alt="image" src="https://github.com/user-attachments/assets/e8b06f8c-777f-4490-81ed-d3cc36c492ec" />

**Action**

* Adalah Tindakan atau aksi yang dipilih oleh Agen untuk mencapai tujuan.

<img width="512" height="32" alt="image" src="https://github.com/user-attachments/assets/444e775f-2fbc-4f2e-b35a-b06954cc0ca5" />


Terdapat 4 Action,yaitu:

* Left(kiri)

* Kanan(right)

* Down(bawah)

* Up(atas)

<img width="292" height="32" alt="image" src="https://github.com/user-attachments/assets/6e1a7927-10da-4225-8942-9194d885edb6" />

**Reward**

* Adalah Sebuah Nilai yang diterima Agent setelah melakukan **Action**

Pada FrozenLake(codingan):

* Reward = 1 Jika berhasil mencapai Goal

* Reward = 0 Jika masih berada di jalur atau Gagal Mencapai Goal(Tujuan)

<img width="876" height="502" alt="image" src="https://github.com/user-attachments/assets/fe62d641-2af2-4fdb-a7a4-fd4b0d1910ff" />


**2.Apa fungsi dari Learning Rate (α)?**

* Fungsi Learning Rate adalah Digunakan untuk mengatur seberapa besar Informasi baru memengaruhi nilai Q yang sudah ada

<img width="365" height="41" alt="image" src="https://github.com/user-attachments/assets/1b940bf4-0977-4e9d-8a43-1c4eb52334f7" />

* Nilai (α)=0,8 Berarti saat Q-Tale diperbarui,80% bobot diberikan pada informasi atau pengalaman baru,sedangkan 20% sisanya dari Nilai lama

<img width="787" height="121" alt="image" src="https://github.com/user-attachments/assets/dd95a3f4-0c92-412d-a763-900d1273d5d6" />

**3.Apa fungsi dari Discount Factor (γ)?**

* Fungsi Discount Factor adalah digunakan untuk mempertimbangkan reward masa depan,Mendorong agent untuk mencari jalur terbaik menuju goal,semakin mendekati 1,semakint penting reward masa depan 

<img width="413" height="26" alt="image" src="https://github.com/user-attachments/assets/709e90c9-b85b-4779-9b64-e65de8548c84" />

(γ)=0,95 berarti agent mempertimbangkan reward masa depan sebesar 95% dari nilai aslinya.

<img width="736" height="65" alt="image" src="https://github.com/user-attachments/assets/0b7b95fe-879e-4e3c-af5a-f1f256eafddb" />

**4.Mengapa digunakan metode Exploration dan Exploitation?**

**Exploration**

<img width="443" height="115" alt="image" src="https://github.com/user-attachments/assets/0df0bd0d-8dbb-40d4-9a3e-46c80abc3f1b" />

Agent Mencoba Action Secara Acak dengan tujuan:

*Menjelajahi lingkungan baru

*menemukan jalur jalur baru

*mengumpulkan pengalaman untuk mengisi Q-Table 

<img width="403" height="28" alt="image" src="https://github.com/user-attachments/assets/3dce630c-3a8e-4466-be7b-4deec5098901" />

**Exploitation**

<img width="456" height="56" alt="image" src="https://github.com/user-attachments/assets/e61d2f97-4e9b-4693-a8b6-e3ab42840b02" />

dengan tujuan:

*memanfaatkan pengetahuan yang sudah dipelajari

*Memilih jalur yang memilki nilai Q tertinggi

Nilai Q adalah nilai yang menunjukkan seberapa baik suatu tindakan (action) jika diambil pada suatu keadaan (state) berdasarkan pengalaman agent.

Dengan menggunakan metode Exploration dan Exploitation

jika hanya Exploration:

*Agent terus mencoba secara acak

*Tidak pernah memanfaatkan hasil pembelajaran

jika hanya Exploitation

*Agent mungkin akan langsung memilih jalur yang tampak terbaik

*Bisa gagal menemukan jalur yang lebih optimal

Oleh karena itu digunakan epsilon-greedy:

<img width="451" height="120" alt="image" src="https://github.com/user-attachments/assets/62cf978e-4091-431b-af00-88cca23f0630" />

fungsi adalah menyeimbangkan Exploration dan Explotation
* Exploration=mencoba action secara acak untuk mencari pengalaman baru
* Exploitation=memilih action terbaik berdasarkan nilai Q yang sudah dipelajari

**5.Bagaimana perubahan nilai reward setelah training 2000 episode?**

Setelah training sebanyak 2000 episode,nilai reward mengalami peningkatan dan menjadi lebih stabil.
Hal ini terjadi karena agent telah mempelajari lingkungan FrozenLake melalui banyak percobaan sehingga Q-Table semakin optimal.
Akibatnya, agent lebih sering memilih action terbaik untuk mencapai Goal, sehingga tingkat keberhasilan dan rata-rata reward yang diperoleh menjadi lebih tinggi dibandingkan pada awal proses training.

Pada awal episode(sebelum di training)
* Q-Table masih bernilai 0.

* Agent bergerak secara acak.

* Reward sering bernilai 0 karena belum menemukan jalur menuju Goal.

Setelah 2000 episode
* Q-Table sudah terisi dengan nilai yang lebih baik.
  
* Agent mengetahui jalur yang mengarah ke Goal.
  
* Frekuensi mendapatkan reward = 1 menjadi lebih tinggi.
  
* Rata-rata reward meningkat dan lebih konsisten.

**Tugas Lanjutan**

*Modifikasi program sehingga:

Menggunakan environment Taxi-v3 Menampilkan rata-rata reward setiap 100 episode Membandingkan hasil training 1000, 2000, dan 5000 episode

* 1000 Episode:

<img width="1062" height="588" alt="image" src="https://github.com/user-attachments/assets/56d67117-0742-4011-b881-692e20a5d453" />

* 2000 Episode:

<img width="1081" height="602" alt="image" src="https://github.com/user-attachments/assets/c39e1fdc-99cf-4ad1-aa24-4858ae11c827" />

* 5000 Episode:

<img width="1072" height="598" alt="image" src="https://github.com/user-attachments/assets/90fc550f-d348-4087-bad9-6ca282b0508d" />


Hasil Perbandingan Training Q-Learning
Jumlah Episode	Pengamatan:
* 1000 Episode	Agent sudah mulai belajar menemukan goal, tetapi masih cukup sering gagal (reward = 0). Pola reward belum sepenuhnya stabil.
* 2000 Episode	Jumlah keberhasilan meningkat. Reward = 1 lebih baik dibandingkan 1000 episode. Agent semakin memahami mana jalur terbaik.
* 5000 Episode	Performa paling stabil. Reward = 1 mendominasi hampir seluruh episode dan kegagalan semakin jarang terjadi.
