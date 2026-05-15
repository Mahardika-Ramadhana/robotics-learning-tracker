# Robotics AI/ML Engineer — Learning Tracker

A self-directed checklist for becoming a robotics AI/ML engineer, focused on computer vision and reinforcement learning.

---

## 1. 🐍 Python

### Basic Problem Solving

- [ ] Tulis fungsi yang menerima list angka, return nilai rata-rata, tanpa numpy
- [ ] Tulis fungsi rekursif untuk hitung faktorial
- [ ] Buat program yang baca input user, validasi apakah angka atau bukan, loop sampai input valid
- [ ] Solve 5 soal di [Exercism](https://exercism.org/tracks/python)

### OOP

- [ ] Buat class `Robot` dengan atribut `name`, `speed`, `position`
- [ ] Tambahkan method `move(distance)` yang update posisi dan print hasilnya
- [ ] Buat class `Sensor` yang bisa di-attach ke `Robot`, dengan method `read()`
- [ ] Buat subclass `FastRobot` yang inherit dari `Robot` dengan speed default 2x

### File I/O + Data

- [ ] Buat CSV berisi 10 baris data sensor (timestamp, value), baca dengan Python, filter yang valuenya di atas 50
- [ ] Simpan hasil filter ke file baru
- [ ] Baca file JSON, modifikasi satu field, simpan kembali

### Debugging

- [ ] Ambil code Python orang lain yang ada bug-nya, identifikasi bugnya tanpa jalankan dulu
- [ ] Bisa baca error traceback dan tahu di baris mana masalahnya tanpa bantuan

---

## 2. 🌿 Git

### Workflow Dasar

- [ ] Init repo baru, buat file, commit pertama
- [ ] Buat branch baru, tambah perubahan, commit, merge ke `main`
- [ ] Push ke GitHub, clone repo yang sama di folder berbeda

### Skenario Umum

- [ ] Ada merge conflict — resolve sendiri, commit hasilnya
- [ ] Push ke branch yang salah — undo dengan `git reset` atau `git revert`
- [ ] Lihat history perubahan file tertentu dengan `git log -- filename`
- [ ] Bisa baca `git diff` sebelum commit

### Workflow Tim

- [ ] Fork repo orang lain di GitHub, buat perubahan, buat Pull Request
- [ ] Bisa review PR orang lain — comment di baris spesifik
- [ ] Pakai `.gitignore` dengan benar — `__pycache__`, `.env`, model weights tidak ter-commit

---

## 3. 🔦 PyTorch

Resource: [fast.ai Practical Deep Learning](https://course.fast.ai)

### Tensor Basics

- [ ] Buat tensor 3x3 berisi angka random, print shape-nya
- [ ] Lakukan operasi: tambah, kali, transpose dua tensor
- [ ] Ubah tensor ke numpy array dan sebaliknya
- [ ] Buat tensor di GPU dan CPU, pindahkan antara keduanya

### Define Model

- [ ] Buat neural network sederhana dengan `nn.Module` untuk klasifikasi 2 kelas
- [ ] Print summary model dan hitung jumlah parameter-nya manual
- [ ] Forward pass satu batch data, print output shape

### Training Loop

- [ ] Tulis training loop dari scratch: forward → loss → backward → update
- [ ] Plot training loss per epoch
- [ ] Training loop konverge di dataset sederhana (MNIST)

### Debug Training

- [ ] Sengaja buat learning rate terlalu besar, observe apa yang terjadi pada loss
- [ ] Sengaja lupa `optimizer.zero_grad()`, observe hasilnya
- [ ] Bisa jelaskan kenapa dua eksperimen di atas menghasilkan hasil yang berbeda

---

## 4. 🐧 Linux (Ubuntu)

### Navigasi Dasar

- [x] Navigasi filesystem lewat terminal (`cd`, `ls`, `pwd`, `mkdir`, `rm`, `mv`, `cp`)
- [x] Buka dan edit file dengan `nano` atau `vim`
- [x] Cari file berdasarkan nama dengan `find` dan isi dengan `grep`

### Package & Permission

- [x] Install package lewat `apt` dan `pip`
- [ ] Buat script bash, beri permission execute dengan `chmod +x`, jalankan
- [ ] Baca dan set file permission (`rwx`)

### Process Management

- [ ] Jalankan program di background dengan `&`, lihat dengan `ps aux`, kill dengan `kill`
- [ ] Pakai `htop` untuk monitor resource usage
- [ ] Pakai `tmux` untuk keep session alive saat disconnect

---

## 5. 🐳 Docker

Resource: [Play with Docker](https://labs.play-with-docker.com)

### Run Container

- [ ] Pull image `ubuntu` dan `python:3.11` dari Docker Hub
- [ ] Run container interaktif, masuk ke dalamnya, jalankan Python
- [ ] List container yang sedang jalan dan yang sudah stop
- [ ] Stop dan hapus container

### Build Image

- [ ] Tulis `Dockerfile` untuk project Python (install dependencies, copy code, set entrypoint)
- [ ] Build image dengan `docker build`
- [ ] Run container dari image sendiri

### Volume & Debug

- [ ] Mount folder lokal ke dalam container
- [ ] Masuk ke container yang sedang jalan dengan `docker exec -it`
- [ ] Debug container yang gagal start dengan `docker logs`

---

## 6. 👁️ OpenCV + Computer Vision

### Operasi Dasar

- [ ] Baca gambar, tampilkan, simpan ke file lain
- [ ] Resize, crop, rotate gambar
- [ ] Convert color space: BGR → grayscale, BGR → HSV
- [ ] Deteksi tepi dengan Canny edge detector

### Video Stream

- [ ] Buka webcam dengan `cv2.VideoCapture`, tampilkan live feed
- [ ] Simpan video stream ke file `.mp4`
- [ ] Baca video file frame per frame, process setiap frame

### Object Detection

- [ ] Jalankan YOLOv8 pretrained pada gambar statis, tampilkan bounding box
- [ ] Jalankan YOLOv8 pada live webcam feed secara real-time
- [ ] Bisa jelaskan apa itu confidence score dan IoU

---

## 7. 🤖 ROS 2

### Setup & Konsep

- [ ] Install ROS 2 (Humble), source `setup.bash`, jalankan `turtlesim`
- [ ] Bisa jelaskan perbedaan topic, service, dan action — kapan pakai yang mana
- [ ] List node dan topic aktif dengan `ros2 node list` dan `ros2 topic list`

### Publisher & Subscriber

- [ ] Buat ROS 2 node Python yang publish string message ke topic `/hello` setiap 1 detik
- [ ] Buat node lain yang subscribe ke `/hello` dan print setiap message
- [ ] Verifikasi dengan `ros2 topic echo`

### Project Integrasi

- [ ] Buat node yang baca webcam dengan OpenCV dan publish frame sebagai ROS 2 topic
- [ ] Buat node subscriber yang menerima frame dan tampilkan dengan `cv2.imshow`
- [ ] Cek frekuensi publish dengan `ros2 topic hz`

---

## 8. ☁️ Cloud Basics (GCP)

Resource: [GCP Free Tier](https://cloud.google.com/free) — $300 credit gratis 90 hari

### VM & SSH

- [ ] Launch Compute Engine VM, SSH masuk dari terminal lokal
- [ ] Install Python dan dependency di VM
- [ ] Jalankan Python script di VM, lihat outputnya
- [ ] Matikan VM setelah selesai

### Cloud Storage

- [ ] Buat bucket di Google Cloud Storage
- [ ] Upload file dari lokal lewat `gsutil` CLI
- [ ] Download file dari bucket ke VM
- [ ] Save model PyTorch ke GCS setelah training

---

## 9. ➕ C++ Dasar

Pelajari paralel dengan ROS 2 — baca source code, modifikasi hal kecil.

### Baca Sebelum Tulis

- [ ] Baca [ROS 2 C++ publisher example](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Cpp-Publisher-And-Subscriber.html), pahami setiap baris
- [ ] Bisa jelaskan: apa itu pointer (`int* ptr`), bedanya dengan reference (`int& ref`)
- [ ] Bisa jelaskan: apa yang terjadi kalau `new` dipakai tanpa `delete`

### Tulis & Compile

- [ ] Tulis fungsi yang menerima dua integer dan return yang terbesar, compile dengan `g++`
- [ ] Buat class sederhana dengan constructor, destructor, dan satu method
- [ ] Modifikasi ROS 2 C++ publisher — ubah message dan frekuensinya, compile ulang

---

## Progress

| Tool | Status |
|------|--------|
| Python | 🔴 |
| Git | 🔴 |
| PyTorch | 🔴 |
| Linux (Ubuntu) | 🔴 |
| Docker | 🔴 |
| OpenCV + CV | 🔴 |
| ROS 2 | 🔴 |
| Cloud basics | 🔴 |
| C++ dasar | 🔴 |

🔴 Not started · 🟡 In progress · 🟢 Done
