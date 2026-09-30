# FlowChart

Repository untuk menyimpan, mendokumentasikan, dan menampilkan **business process flowchart** secara terstruktur.

Fokus utama repository ini adalah dokumentasi **LCV FlowChart**, yang menggambarkan integrasi antara Power Apps, SharePoint Online, Power Automate, UiPath, dan SharePoint On-Premises.

## LCV FlowChart

### Tujuan

LCV FlowChart mendokumentasikan alur proses dari pengisian form oleh pengguna sampai dokumen atau hasil pemrosesan disimpan ke **SharePoint On-Premises**.

### Alur Utama

```text
User
  │
  ▼
Power Apps
  │
  │ Mengisi form
  ▼
SharePoint Online
  │
  │ Data tersimpan
  ▼
Power Automate
  │
  │ Mencari data terbaru
  ▼
Program Budaya?
  │
  ├── Bestie
  │     │
  │     ├── Rename File
  │     │
  │     └── Kirim Queue ID
  │
  └── Selain Bestie
        │
        └── Kirim proses ke UiPath
                    │
                    ▼
                  UiPath
                    │
                    ▼
              Program Budaya?
               │
               ├── Bestie
               │     │
               │     ├── Download dokumen
               │     └── Upload dokumen
               │
               └── Selain Bestie
                     │
                     └── Create Excel
                              │
                              ▼
                   SharePoint On-Premises
```

> **Catatan:** Diagram sumber adalah referensi utama untuk detail koneksi, branching, dan urutan aktivitas. Flow di atas merupakan ringkasan dokumentasi agar alur mudah dipahami dari README.

### Preview

**[Buka LCV FlowChart di diagrams.net](https://viewer.diagrams.net/?url=https%3A%2F%2Fraw.githubusercontent.com%2Ffajarinsanfi-ops%2FFlowChart%2Fmain%2FLCV_FlowChart)**

Preview menggunakan file sumber yang tersimpan di repository sehingga diagram dapat dilihat tanpa mengubah source.

### Source Diagram

**[LCV_FlowChart](./LCV_FlowChart)**

File tersebut merupakan **draw.io XML source** yang dapat diedit menggunakan diagrams.net. File sengaja dipertahankan sebagai source diagram sehingga perubahan proses dapat dilacak melalui Git.

## Komponen Proses

| Komponen | Fungsi |
|---|---|
| **Power Apps** | Antarmuka pengguna untuk mengisi form LCV |
| **SharePoint Online** | Menyimpan data hasil pengisian form |
| **Power Automate** | Mencari data terbaru dan menjalankan orkestrasi proses |
| **UiPath Queue** | Menyediakan mekanisme antrean untuk proses otomasi UiPath |
| **UiPath** | Menjalankan proses dokumen dan menghasilkan output |
| **SharePoint On-Premises** | Tujuan akhir penyimpanan dokumen/hasil proses |
| **Excel** | Output yang dibuat untuk alur program tertentu |

## Struktur Repository

```text
FlowChart/
├── README.md
├── index.html
├── style.css
├── flowchart.md
└── LCV_FlowChart
```

| File | Keterangan |
|---|---|
| `README.md` | Dokumentasi project dan LCV FlowChart |
| `index.html` | Halaman browser untuk menampilkan flowchart |
| `style.css` | Styling halaman browser |
| `flowchart.md` | Source flowchart berbasis Mermaid |
| `LCV_FlowChart` | Source diagram draw.io dalam format XML |

## Membuka dan Mengedit Diagram

### Dengan diagrams.net

1. Buka **[diagrams.net](https://app.diagrams.net/)**.
2. Pilih opsi untuk membuka diagram dari device/repository.
3. Buka file `LCV_FlowChart`.
4. Lakukan perubahan pada diagram.
5. Simpan kembali source diagram.
6. Commit perubahan ke branch yang sesuai.
7. Perbarui README jika struktur atau logika proses berubah.

### Hanya Melihat Diagram

Gunakan preview berikut:

**[Open LCV FlowChart Preview](https://viewer.diagrams.net/?url=https%3A%2F%2Fraw.githubusercontent.com%2Ffajarinsanfi-ops%2FFlowChart%2Fmain%2FLCV_FlowChart)**

## Browser Flowchart

Repository juga menyediakan flowchart berbasis **Mermaid** melalui `index.html`.

File terkait:

- `index.html`
- `style.css`
- `flowchart.md`

Untuk penggunaan dasar, tidak diperlukan Node.js, npm, atau build process.

## Menjalankan Secara Lokal

Clone repository:

```bash
git clone https://github.com/fajarinsanfi-ops/FlowChart.git
cd FlowChart
```

Kemudian buka:

```text
index.html
```

di browser modern.

## GitHub Pages

Bagian HTML/CSS dapat dipublikasikan sebagai static site menggunakan GitHub Pages.

Konfigurasi yang digunakan:

```text
Branch: main
Folder: / (root)
```

Source diagram draw.io tetap disimpan di repository dan tidak bergantung pada deployment halaman web.

## Pedoman Perubahan Diagram

Saat memperbarui LCV FlowChart:

1. Pertahankan nama sistem dan proses agar konsisten.
2. Jangan menghilangkan source diagram editable.
3. Perbarui preview setelah source berubah.
4. Perbarui ringkasan README jika alur bisnis berubah.
5. Pastikan **SharePoint On-Premises** tetap terdokumentasi sebagai tujuan akhir jika memang demikian pada proses.
6. Gunakan commit message yang menjelaskan perubahan.
7. Hindari menyimpan kredensial, token, connection string, atau data sensitif di repository.

## Teknologi

| Teknologi | Penggunaan |
|---|---|
| **draw.io / diagrams.net** | Membuat dan mengedit business process diagram |
| **Mermaid** | Flowchart ringan berbasis teks |
| **HTML5** | Presentasi flowchart melalui browser |
| **CSS3** | Styling halaman |
| **GitHub** | Version control dan kolaborasi |

## Roadmap

- [ ] Preview diagram langsung di halaman web
- [ ] Interactive flowchart viewer
- [ ] Katalog beberapa flowchart
- [ ] Search dan filtering flowchart
- [ ] Export PNG/SVG
- [ ] Dark mode
- [ ] Metadata dokumentasi proses
- [ ] Automated diagram preview
- [ ] GitHub Pages documentation site

## License

Repository ini belum memiliki lisensi open-source yang ditentukan secara eksplisit.

---

**Repository:** **[fajarinsanfi-ops/FlowChart](https://github.com/fajarinsanfi-ops/FlowChart)**
