# JKT48 Lucky  🎰

## Cara Ganti Gambar

Tinggal **ganti file gambarnya** di folder `images/` dengan foto pilihanmu.
Nama file harus sama persis, ekstensi boleh .jpg / .png / .webp.

---

## Struktur Folder

```
jkt48-slot/
├── index.html
└── images/
    ├── slot/
    │   ├── symbol1.jpg   ← Simbol slot 1 (multiplier ×2)
    │   ├── symbol2.jpg   ← Simbol slot 2 (multiplier ×3)
    │   ├── symbol3.jpg   ← Simbol slot 3 (multiplier ×4)
    │   ├── symbol4.jpg   ← Simbol slot 4 (multiplier ×5)
    │   ├── symbol5.jpg   ← Simbol slot 5 (multiplier ×8)
    │   └── symbol6.jpg   ← Simbol slot 6 (multiplier ×10)
    └── photocard/
        ├── common.jpg     ← Photocard Common   (300 pts)
        ├── rare.jpg       ← Photocard Rare     (800 pts)
        ├── epic.jpg       ← Photocard Epic     (2.000 pts)
        └── legendary.jpg  ← Photocard Legendary (5.000 pts)
```

---

## Ubah Nama Member / Harga di VS Code

Buka `index.html`, cari bagian ini di dalam `<script>`:

### Slot Symbols
```js
const SLOT_SYMBOLS = [
  { id: 0, img: 'images/slot/symbol1.jpg', label: 'Freya',   multiplier: 2  },
  { id: 1, img: 'images/slot/symbol2.jpg', label: 'Shani',   multiplier: 3  },
  ...
];
```
- `label` → nama yang muncul di paytable
- `multiplier` → kelipatan kemenangan

### Photocards
```js
const PHOTOCARDS = [
  { id: 0, img: 'images/photocard/common.jpg', name: 'Regular Photo', cost: 300, rarity: 'common' },
  ...
];
```
- `name` → nama photocard
- `cost` → harga dalam points
- `rarity` → common / rare / epic / legendary

---

## Cara Buka Game

Karena game load gambar dari folder lokal, buka pakai **Live Server** di VS Code:
1. Install ekstensi **Live Server**
2. Klik kanan `index.html` → **Open with Live Server**
3. Game terbuka di browser ✦
