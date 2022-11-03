<h1 align="center"> Deploy Heroku </h1>

<p align="center">
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/heroku-%23430098.svg?style=for-the-badge&logo=heroku&logoColor=white" style="vertical-align:middle">
</p>
<p align="center">
    <img src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/gunicorn-%298729.svg?style=for-the-badge&logo=gunicorn&logoColor=white" style="vertical-align:middle">
    <img src="https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white" style="vertical-align:middle">    
</p>

## Overview

[REST](https://en.wikipedia.org/wiki/Representational_state_transfer) [API](https://en.wikipedia.org/wiki/API)s biasanya digunakan untuk mengekspos model Machine Learning (ML) ke layanan lain.

## Tools/Library

Semua daftar dependency/package Python yang diperlukan untuk menjalankan API dan model sebagai berikut:

- [flask](https://palletsprojects.com/p/flask/) → web framework
- [tensorflow](https://www.tensorflow.org/resources/learn-ml?gclid=CjwKCAjw0dKXBhBPEiwA2bmObUNdQN9NJKhqYxL3u2Iqjs7baLGf-bvFfwEdEXddXtHFyhkqv4O2QhoCbCoQAvD_BwE) → machine learning framework
- [gunicorn](https://gunicorn.org/) → WSGI (Web Server Gateway Interface) HTTP Server untuk bahasa pemrograman Python
- [numpy](https://numpy.org/) → proses komputasi numerik
- [scikit-learn](https://scikit-learn.org/stable/) → machine learning framework
- [pickle](https://docs.python.org/3/library/pickle.html) → menyimpan dan membaca data (machine learning) ke dalam /dari sebuah file

## Flask
[App Routing](https://flask.palletsprojects.com/en/2.2.x/quickstart/) berarti memetakan URL ke `fungsi tertentu` yang akan menangani logika untuk URL tersebut. Kerangka kerja web modern menggunakan URL yang lebih bermakna untuk membantu pengguna mengingat URL dan mempermudah navigasi.

```python
from flask import Flask

app = Flask(__name__)

@app.route('/', , methods=['GET', 'POST']) # endpoint("/"), HTTP Methods (GET, POST, PUT, DELETE)
def function(): # fungsi tertentu yang akan menangani logika untuk URL tersebut


    return value # mengembalikan nilai

if __name__ == '__main__':
    app.run(debug=True)
```

| HTTP Method |        Deskripsi       |
|     ---     |          ---           |
|     GET     |     Mengambil Data     |
|    POST     |     Menambah Data      |
|     PUT     |      Mengubah Data     |
|    DELETE   |     Menghapus Data     |

## Cara menjalankan API

1. Download repository dari GitHub [Linear Regression](https://github.com/alfanme/dts-deployment-linreg) atau [CNN](https://github.com/alfanme/dts-deployment-ann).
1. Pastikan Anda sudah menginstall Anaconda.
1. Buka terminal/command prompt/power shell.
1. Buat virtual environment dengan
   ```shell
   conda create -n <nama-environment> python=3.9
   ```
1. Aktifkan virtual environment dengan
   ```shell
   conda activate <nama-environment>
   ```
1. Install semua dependency/package Python dengan
   ```shell
   pip install -r requirements.txt
   ```
1. Masuk ke folder/repository dengan
   ```shell
   cd <nama-folder/repository>
   ```
1. Jalankan API menggunakan perintah
   ```shell
   python app.py
   ```

## Akses melalui Website

1. Anda akan diberikan URL untuk membuka website berupa `localhost:5000/` atau `127.0.0.1:5000/`.
1. Buka URL dengan browser, coba masukkan input yang ingin di prediksi.
1. Anda akan diberikan prediksi di halaman website.

## Deploy Flask ke Heroku

1. Download repository dari GitHub [Linear Regression](https://github.com/alfanme/dts-deployment-linreg) atau [CNN](https://github.com/alfanme/dts-deployment-ann).

2. Membuat GitHub Repository baru

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183363865-20a3d530-3d25-4a1a-9d48-8bea212d69fc.png" width="1080" style="vertical-align:middle">
</p>

3. Tulis nama repository

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364004-3f297f4f-37d8-4040-bc64-89847b1b96ee.png" width="1080" style="vertical-align:middle">
</p>

4. Pilih create repository

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364054-14b7a69a-f931-47c8-8aa0-9b0b74711774.png" width="1080" style="vertical-align:middle">
</p>

5. Upload semua file dan folder ke GitHub Repository

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364116-165110d8-047f-42f4-a85c-811a30e4da75.png" width="1080" style="vertical-align:middle">
</p>
<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364162-ad002f4d-9a2a-48ee-a424-6c2ad355953d.png" width="1080" style="vertical-align:middle">
</p>

6. Masuk ke heroku.com. Jika belum punya akun silahkan sign up terlebih dahulu.

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364190-6df010d5-80df-4cfc-8d19-97810f53bc9d.png" width="1080" style="vertical-align:middle">
</p>

7. Klik New dan pilih Create new app

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364215-d67a65af-ed82-4569-9ffc-a5097a1d5d30.png" width="1080" style="vertical-align:middle">
</p>

8. Masukkan nama-aplikasi. Kemudian create aplikasi

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364242-9e809987-6656-491c-8138-4b467b867161.png" width="1080" style="vertical-align:middle">
</p>

9. Pada Deployment method pilih GitHub. Kemudian masukkan nama repository dan pilih connect

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364276-b12621d5-2f15-4b4d-b09e-619bdbf17431.png" width="1080" style="vertical-align:middle">
</p>

10. Pilih Enable Automatic Deploys dan lakukan deploy dengan memilih Deploy Branch

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364310-d249c775-8a8b-4e12-97e2-16e627010bdb.png" width="1080" style="vertical-align:middle">
</p>

11. Tunggu setelah proses selesai. Jika sudah pilih view

<p align="center">
    <img src="https://user-images.githubusercontent.com/72246401/183364328-f1ec584a-c11c-4ccc-b167-ab1d9e5900c2.png" width="1080" style="vertical-align:middle">
</p>

12. Berikut hasilnya: https://nama-aplikasi.herokuapp.com

    <img src="https://user-images.githubusercontent.com/72246401/184166411-eca0a56e-9413-4359-84b4-74e4f5efc2b6.png" width="1080" style="vertical-align:middle">
</p>

