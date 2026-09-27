# Belajar Mandarin

## Git Branching

Project ini menggunakan 3 jenis branch:

```text
main
  |
  └── dev
       |
       ├── feature/login
       ├── feature/register
       ├── feature/flashcard
       ├── feature/quiz
       └── feature/...
```

### `main`

Branch untuk versi yang sudah stabil.

* Jangan langsung coding di `main`.
* Jangan push fitur langsung ke `main`.
* Perubahan masuk ke `main` melalui Pull Request dari `dev`.
* `main` digunakan sebagai versi yang siap digunakan atau didemokan.

### `dev`

Branch utama untuk development.

* Semua fitur yang sudah selesai akan digabungkan ke `dev`.
* Fitur baru dibuat dari `dev`.
* `dev` menjadi tempat menggabungkan pekerjaan seluruh anggota.

### `feature/*`

Branch untuk mengerjakan satu fitur atau task tertentu.

Contoh:

```text
feature/login
feature/register
feature/roadmap
feature/flashcard
feature/quiz
feature/hanzi
feature/auth-api
```

Gunakan nama branch berdasarkan fitur atau task, bukan nama anggota.

## 1. Sebelum Mulai Mengerjakan Fitur

Pastikan branch `dev` sudah menggunakan versi terbaru.

```bash
git checkout dev
git pull origin dev
```

Kemudian buat branch baru dari `dev`.

```bash
git checkout -b feature/nama-fitur
```

Contoh:

```bash
git checkout -b feature/login
```

## 2. Mengerjakan Fitur

Kerjakan fitur hanya di branch yang sudah dibuat.

Contoh:

```text
feature/login
```

## 3. Push Branch

Setelah fitur selesai:

```bash
git push -u origin feature/nama-fitur
```

Contoh:

```bash
git push -u origin feature/login
```

## 4. Membuat Pull Request

Setelah melakukan push, buka repository di GitHub.

Pilih:

```text
Pull requests
→ New pull request
```

Pastikan arah PR:

```text
base: dev
compare: feature/login
```

Fitur harus masuk ke `dev` terlebih dahulu.

Jangan membuat:

```text
feature/login → main
```

Gunakan:

```text
feature/login → dev
```

## 5. Isi Pull Request

### Title

Gunakan judul yang menjelaskan fitur.

Contoh:

```text
feat: add login page
```
