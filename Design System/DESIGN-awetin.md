---
version: 1.0
name: Awetin-design-system
description: Awetin adalah marketplace reparasi informal (elektronik kecil, jahit/pakaian, sepatu, las) dengan jalur non-servis (jual/donasi/daur ulang resmi), disusun untuk PNBITC#18 — Desain UI/UX "Tech for Nature". Sistem ini menggabungkan token yang sudah dibangun di prototype HTML (blom_merged (awetin).html) dengan penyempurnaan brand & aksesibilitas, mengikuti arsitektur token 3-lapis (Primitive → Semantic → Component). Brand anchor: hijau ({colors.primary}), dipakai strategis — bukan disebar ke semua elemen. Nada visual: hangat, jujur, membumi (sesuai PRD Bagian 9), bukan korporat kaku atau startup-y. Target akhir: dikonversi jadi UI page design di Figma, frame iPhone 16 (393×852px).

colors:
  primary: "#00AA13"
  primary-hover: "#049F16"
  primary-pressed: "#038A10"
  primary-disabled: "#A9DCAE"
  primary-container: "#E3F7E4"
  on-primary: "#FFFFFF"
  on-primary-container: "#046B0C"
  secondary: "#F6A609"
  secondary-container: "#FFF1D6"
  on-secondary: "#1A1A1A"
  background: "#F4F6F6"
  surface: "#FFFFFF"
  surface-variant: "#F8FAFA"
  text-primary: "#14181A"
  text-secondary: "#5C6668"
  text-tertiary: "#8D9699"
  text-disabled: "#B7BEBC"
  border: "#E8EBEA"
  divider: "#F0F3F2"
  disabled-bg: "#EEF0EF"
  disabled-fg: "#B7BEBC"
  success: "#1E9E4A"
  success-container: "#E4F7EA"
  warning: "#B8790A"
  warning-container: "#FFF1D6"
  error: "#D42F2F"
  error-container: "#FCE7E7"
  information: "#2F72ED"
  information-container: "#E8F0FE"
  category-elektronik: "#6C63E0"
  category-elektronik-container: "#EDEBFC"
  category-elektronik-on-container: "#4A3FC7"
  category-jahit: "#E8628C"
  category-jahit-container: "#FDEAF0"
  category-jahit-on-container: "#C23D68"
  category-sepatu: "#8B4A3C"
  category-sepatu-container: "#F5E7E3"
  category-sepatu-on-container: "#6B3529"
  category-las: "#2C8C99"
  category-las-container: "#E2F3F5"
  category-las-on-container: "#1F6670"
  dark-background: "#0F1412"
  dark-surface: "#171D1B"
  dark-surface-variant: "#1E2523"
  dark-border: "#2A322F"
  dark-divider: "#232B28"
  dark-text-primary: "#F2F5F3"
  dark-text-secondary: "#AEB8B4"
  dark-text-tertiary: "#7C8884"
  dark-text-disabled: "#566158"
  dark-primary: "#3DDC5A"
  dark-on-primary: "#0B1F0E"
  dark-success: "#3BC97A"
  dark-warning: "#E3A63D"
  dark-error: "#F2685F"
  dark-information: "#5B9BFF"

typography:
  display:
    fontFamily: Plus Jakarta Sans
    fontSize: 34px
    fontWeight: 800
    lineHeight: 40px
    letterSpacing: -0.5px
  heading-1:
    fontFamily: Plus Jakarta Sans
    fontSize: 28px
    fontWeight: 800
    lineHeight: 36px
    letterSpacing: -0.4px
  heading-2:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: 700
    lineHeight: 32px
    letterSpacing: -0.3px
  heading-3:
    fontFamily: Plus Jakarta Sans
    fontSize: 20px
    fontWeight: 700
    lineHeight: 28px
    letterSpacing: -0.2px
  title:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: 700
    lineHeight: 24px
  body-l:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: 500
    lineHeight: 24px
  body-m:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: 500
    lineHeight: 20px
  body-s:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: 500
    lineHeight: 18px
    letterSpacing: 0.1px
  label-l:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: 700
    lineHeight: 20px
    letterSpacing: 0.1px
  label-m:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: 600
    lineHeight: 16px
    letterSpacing: 0.2px
  label-s:
    fontFamily: Plus Jakarta Sans
    fontSize: 11px
    fontWeight: 600
    lineHeight: 16px
    letterSpacing: 0.2px
  caption:
    fontFamily: Plus Jakarta Sans
    fontSize: 11px
    fontWeight: 500
    lineHeight: 16px
    letterSpacing: 0.3px
  numeric-price:
    fontFamily: JetBrains Mono
    fontSize: 20px
    fontWeight: 700
    lineHeight: 28px
  numeric-inline:
    fontFamily: JetBrains Mono
    fontSize: 14px
    fontWeight: 600
    lineHeight: 20px

rounded:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
  full: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 20px
  xl: 24px
  xxl: 32px
  xxxl: 40px
  section: 48px

elevation:
  level-1: "0 2px 8px rgba(20,24,22,0.04)"
  level-2: "0 4px 16px rgba(20,24,22,0.08)"
  level-3: "0 8px 24px rgba(20,24,22,0.12)"
  level-4: "0 16px 32px rgba(20,24,22,0.16)"
  bottom-nav: "0 -4px 24px rgba(0,0,0,0.06)"

motion:
  duration-fast: 150ms
  duration-base: 250ms
  duration-sheet: 300ms
  easing-standard: "cubic-bezier(0.4, 0, 0.2, 1)"
  easing-decelerate: "cubic-bezier(0, 0, 0.2, 1)"
  easing-accelerate: "cubic-bezier(0.4, 0, 1, 1)"
  easing-sheet: "cubic-bezier(0.16, 1, 0.3, 1)"

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-l}"
    rounded: "{rounded.md}"
    padding: "14px 24px"
    height: 48px
  button-primary-pressed:
    backgroundColor: "{colors.primary-pressed}"
  button-primary-disabled:
    backgroundColor: "{colors.primary-disabled}"
    textColor: "{colors.on-primary}"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary}"
    typography: "{typography.label-l}"
    rounded: "{rounded.md}"
    padding: "14px 24px"
    height: 48px
    border: "1.5px solid {colors.primary}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.text-primary}"
    typography: "{typography.label-l}"
    rounded: "{rounded.md}"
    padding: "10px 16px"
  button-danger:
    backgroundColor: "{colors.error}"
    textColor: "#FFFFFF"
    typography: "{typography.label-l}"
    rounded: "{rounded.md}"
    padding: "14px 24px"
    height: 48px
  card-base:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
    border: "1px solid {colors.border}"
  card-elevated:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
    shadow: "{elevation.level-2}"
  category-tile:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: "{spacing.md}"
    border: "1px solid {colors.border}"
  worker-card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
    shadow: "{elevation.level-1}"
  listing-card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.sm}"
    border: "1px solid {colors.border}"
  text-input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text-primary}"
    typography: "{typography.body-l}"
    rounded: "{rounded.sm}"
    padding: "12px 16px"
    height: 52px
    border: "1.5px solid {colors.border}"
  text-input-focused:
    border: "1.5px solid {colors.primary}"
  text-input-error:
    border: "1.5px solid {colors.error}"
  otp-input-box:
    backgroundColor: "{colors.surface-variant}"
    textColor: "{colors.text-primary}"
    typography: "{typography.heading-2}"
    rounded: "{rounded.sm}"
    border: "1.5px solid {colors.border}"
    height: 56px
    width: 48px
  search-bar:
    backgroundColor: "{colors.surface-variant}"
    textColor: "{colors.text-secondary}"
    typography: "{typography.body-m}"
    rounded: "{rounded.full}"
    padding: "12px 16px"
    height: 44px
  badge-category:
    typography: "{typography.label-s}"
    rounded: "{rounded.full}"
    padding: "4px 10px"
  badge-status-success:
    backgroundColor: "{colors.success-container}"
    textColor: "{colors.success}"
    typography: "{typography.label-s}"
    rounded: "{rounded.full}"
    padding: "4px 10px"
  badge-status-warning:
    backgroundColor: "{colors.warning-container}"
    textColor: "{colors.warning}"
    typography: "{typography.label-s}"
    rounded: "{rounded.full}"
    padding: "4px 10px"
  badge-status-error:
    backgroundColor: "{colors.error-container}"
    textColor: "{colors.error}"
    typography: "{typography.label-s}"
    rounded: "{rounded.full}"
    padding: "4px 10px"
  bottom-nav-user:
    backgroundColor: "{colors.surface}"
    shadow: "{elevation.bottom-nav}"
    height: 64px
  bottom-nav-tukang:
    backgroundColor: "{colors.surface}"
    shadow: "{elevation.bottom-nav}"
    height: 64px
  bottom-nav-item-active:
    textColor: "{colors.primary}"
    typography: "{typography.label-m}"
  bottom-nav-item-inactive:
    textColor: "{colors.text-tertiary}"
    typography: "{typography.label-m}"
  fab-perbaiki:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.full}"
    shadow: "{elevation.level-3}"
    height: 56px
    width: 56px
  bottom-sheet:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.xl} {rounded.xl} 0 0"
    padding: "{spacing.lg}"
    shadow: "{elevation.level-4}"
  confirmation-modal:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: "{spacing.xl}"
    shadow: "{elevation.level-4}"
  status-stepper-step-done:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
  status-stepper-step-active:
    backgroundColor: "{colors.primary-container}"
    textColor: "{colors.on-primary-container}"
    border: "2px solid {colors.primary}"
  status-stepper-step-pending:
    backgroundColor: "{colors.disabled-bg}"
    textColor: "{colors.text-disabled}"
  invoice-card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
    border: "1px solid {colors.border}"
  earnings-card:
    backgroundColor: "{colors.primary-container}"
    textColor: "{colors.on-primary-container}"
    rounded: "{rounded.lg}"
    padding: "{spacing.xl}"
  chat-bubble-sent:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-m}"
    rounded: "{rounded.md} {rounded.md} {rounded.xs} {rounded.md}"
    padding: "10px 14px"
  chat-bubble-received:
    backgroundColor: "{colors.surface-variant}"
    textColor: "{colors.text-primary}"
    typography: "{typography.body-m}"
    rounded: "{rounded.md} {rounded.md} {rounded.md} {rounded.xs}"
    padding: "10px 14px"
  toast-snackbar:
    backgroundColor: "{colors.text-primary}"
    textColor: "#FFFFFF"
    typography: "{typography.body-m}"
    rounded: "{rounded.sm}"
    padding: "12px 16px"
  reputation-alert-card:
    backgroundColor: "{colors.warning-container}"
    textColor: "{colors.warning}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
    border: "1px solid {colors.warning}"
  skeleton-loader:
    backgroundColor: "{colors.surface-variant}"
    rounded: "{rounded.sm}"
  empty-state:
    backgroundColor: "transparent"
    textColor: "{colors.text-tertiary}"
    typography: "{typography.body-m}"
  photo-uploader-slot:
    backgroundColor: "{colors.surface-variant}"
    rounded: "{rounded.md}"
    border: "1.5px dashed {colors.border}"
---

## Overview

Awetin dibangun untuk demo kompetisi UI/UX bertema *"Tech for Nature"* — jadi sistem desain ini sengaja **tidak rumit**: satu keluarga font, satu warna brand (hijau), token yang gampang dipetakan langsung jadi Figma Variables & Text Styles. Fondasinya diambil dari token yang sudah dibangun di prototype HTML tim (`blom_merged (awetin).html`) — sistem penamaan gaya Material (`default/hover/pressed/disabled/container/on-container`) yang sudah cukup matang — lalu disempurnakan dengan lapisan kategori jasa dan dark mode yang belum ada sebelumnya.

**Karakteristik kunci:**
- Hijau ({colors.primary}) sebagai satu-satunya brand anchor — dipakai strategis untuk CTA utama, nav aktif, dan elemen terpilih, **bukan** disebar ke semua elemen (latar & surface tetap netral)
- Plus Jakarta Sans di seluruh UI teks; JetBrains Mono khusus untuk angka harga/invoice — memberi kesan presisi finansial yang mendukung prinsip transparansi PRD
- 4 warna aksen kategori jasa (Elektronik/Jahit/Sepatu/Las) untuk wayfinding visual, sengaja dipilih beda hue dari 4 warna semantic (success/warning/error/info) supaya tidak ambigu
- Radius membulat konsisten (8-24px) dan ikon line rounded — mendukung nada "hangat, jujur, membumi" dari PRD, bukan korporat kaku
- Dark mode sebagai token resmi (wajib per PRD Bagian 11), bukan tempelan

## Colors

> Sumber: token Tailwind di `blom_merged (awetin).html` (base), diperluas untuk kategori jasa & dark mode (baru).

### Arsitektur 3-Lapis

```
Primitive   → nilai hex mentah (mis. #00AA13)
Semantic    → alias tujuan (mis. {colors.primary} = primitive hijau)
Component   → dipakai spesifik komponen (mis. button-primary.backgroundColor = {colors.primary})
```

Frontmatter di atas sudah di level **Semantic** (siap jadi nama Figma Variable) — primitive mentahnya cukup jadi catatan asal di bawah tiap grup.

### Brand (Primary & Secondary)
- **Primary** ({colors.primary} `#00AA13`): satu-satunya brand anchor. Dipakai untuk CTA utama, tab nav aktif, ikon terpilih, progress "selesai" di status stepper.
- **Primary Hover/Pressed**: state tekan tombol (mobile — bukan hover asli, dipakai untuk state `:active`/pressed).
- **Primary Disabled** ({colors.primary-disabled}): tombol primary nonaktif.
- **Primary Container** ({colors.primary-container}): latar lembut untuk badge/chip terpilih, earnings card.
- **Secondary** ({colors.secondary} `#F6A609`, amber): aksen sekunder untuk highlight non-CTA (mis. badge "Tukang Favorit", tips banner) — dipakai jarang, bukan warna kompetisi dengan hijau.

### Kategori Jasa (baru)
- **Elektronik** ({colors.category-elektronik}, indigo)
- **Jahit/Pakaian** ({colors.category-jahit}, rose)
- **Sepatu** ({colors.category-sepatu}, rust-brown)
- **Las** ({colors.category-las}, teal)

Masing-masing punya varian `-container` (latar lembut) dan `-on-container` (teks di atasnya) — konsisten dengan pola primary/secondary. Dipakai HANYA untuk tag kategori, ikon kategori di direktori tukang, dan aksen kartu kategori — tidak untuk CTA atau status. **Selalu dipasangkan dengan ikon + label teks**, tidak pernah cuma warna sendirian (wajib PRD Bagian 11).

### Netral (Surface, Background, Text, Border)
- **Background** ({colors.background} `#F4F6F6`): latar layar utama.
- **Surface** ({colors.surface} `#FFFFFF`): kartu, sheet, input.
- **Surface Variant** ({colors.surface-variant}): latar kartu sekunder, skeleton loader, search bar rest state.
- **Text Primary/Secondary/Tertiary/Disabled**: 4 tingkat hierarki teks, kontras terhadap `{colors.surface}` diverifikasi sesuai ambang di bagian Aksesibilitas.
- **Border/Divider**: garis pemisah 1px.

### Semantic Status
- **Success/Warning/Error/Information**: dipakai KHUSUS untuk status sistem (verifikasi berhasil, alert reputasi, error form, info netral) — tidak pernah dipakai untuk kategori jasa supaya makna tidak tertukar.

### Dark Mode (baru — wajib per PRD Bagian 11)
Latar mendekati hitam murni dengan tint hijau samar (OLED-friendly, hemat daya):
- **Dark Background** ({colors.dark-background} `#0F1412`), **Dark Surface** ({colors.dark-surface}), **Dark Surface Variant**
- **Dark Primary** ({colors.dark-primary} `#3DDC5A`) — hijau **dicerahkan** dari primary light-mode, karena `#00AA13` di atas latar nyaris-hitam berisiko kontras kurang di ukuran teks kecil. On-primary dark pakai `{colors.dark-on-primary}` (hijau sangat gelap), bukan putih, supaya kontras tombol tetap tinggi.
- Success/Warning/Error/Information versi dark juga dicerahkan (`dark-success`, dll.) dengan alasan kontras yang sama.
- Warna kategori jasa TIDAK perlu varian dark terpisah untuk versi awal — cukup pakai versi light-nya di atas `{colors.dark-surface}` (kontrasnya masih memadai karena semua cukup gelap/jenuh); **verifikasi ulang di Figma** kalau nanti dipakai di teks kecil.

## Typography

**Plus Jakarta Sans** — humanis, geometris, hangat; cocok brand voice "kamu" bukan "Anda" dari PRD.
**JetBrains Mono** — khusus angka (`{typography.numeric-price}`, `{typography.numeric-inline}`) di invoice, earnings card, harga di listing. Jangan dipakai untuk prosa.

| Token | Ukuran | Weight | Pemakaian |
|---|---|---|---|
| `{typography.display}` | 34px/800 | Splash, angka besar dashboard dampak |
| `{typography.heading-1}` | 28px/800 | Judul halaman |
| `{typography.heading-2}` | 24px/700 | Judul section |
| `{typography.heading-3}` | 20px/700 | Judul kartu besar |
| `{typography.title}` | 16px/700 | Judul kartu standar, nama tukang |
| `{typography.body-l}` | 16px/500 | Body utama, isi form |
| `{typography.body-m}` | 14px/500 | Body sekunder, deskripsi |
| `{typography.body-s}` | 12px/500 | Body kecil, metadata |
| `{typography.label-l}` | 14px/700 | Label tombol |
| `{typography.label-m}` | 12px/600 | Label nav, tab |
| `{typography.label-s}` | 11px/600 | Badge, tag kategori |
| `{typography.caption}` | 11px/500 | Timestamp, keterangan kecil |
| `{typography.numeric-price}` | 20px/700 mono | Harga besar di invoice/earnings |
| `{typography.numeric-inline}` | 14px/600 mono | Harga inline di card/list |

## Layout

### Grid & Frame
- Target Figma: **iPhone 16 frame, 393×852px** (sesuai syarat lomba) — bukan grid marketing web.
- Margin horizontal konsisten `{spacing.lg}` (20px) di semua layar.
- Container maksimal = lebar frame; tidak ada breakpoint desktop yang relevan (murni mobile).

### Spacing Scale
Base unit 4px, dari `{spacing.xxs}` (4px) sampai `{spacing.section}` (48px). Jarak antar-card dalam list = `{spacing.md}` (16px); padding internal card standar = `{spacing.lg}` (20px).

## Elevation & Depth

| Level | Treatment | Pemakaian |
|---|---|---|
| 0 (flat) | Border `{colors.border}`, tanpa shadow | Card default, list item |
| 1 | `{elevation.level-1}` | Worker card, kartu ringan terangkat |
| 2 | `{elevation.level-2}` | Card elevated, modal kecil |
| 3 | `{elevation.level-3}` | FAB "Perbaiki", kartu mengambang di atas konten |
| 4 | `{elevation.level-4}` | Bottom sheet, confirmation modal |
| bottom-nav | `{elevation.bottom-nav}` | Shadow ke atas khusus bottom navigation |

## Shapes

| Token | Nilai | Pemakaian |
|---|---|---|
| `{rounded.xs}` | 4px | Chip kecil, sudut asimetris chat bubble |
| `{rounded.sm}` | 8px | Input, search bar segi |
| `{rounded.md}` | 12px | Card standar, tombol |
| `{rounded.lg}` | 16px | Card besar, category tile |
| `{rounded.xl}` | 24px | Bottom sheet (sudut atas) |
| `{rounded.full}` | 9999px | Badge, FAB, search bar pill, avatar |

## Iconography & Illustration

- **Ikon:** line/outline, stroke 1.5–2px, sudut membulat (bukan tajam) — selaras radius card yang membulat. Rekomendasi pustaka: **Phosphor Icons** atau **Lucide** (keduanya line-style, gratis, lengkap kategori jasa/reparasi/lokasi/dokumen yang dibutuhkan Awetin) — pilih satu, jangan campur dua pustaka ikon dalam satu file Figma.
- **Ilustrasi (empty state, onboarding):** flat, organik, motif alam ringan (daun, lingkaran repair/recycle) — konsisten tema "Tech for Nature". Hindari gaya 3D render generik atau ilustrasi stok yang tidak konsisten gaya.
- Ikon kategori jasa memakai warna `{colors.category-*}` masing-masing, tapi ikon status/sistem (centang, alert, error) selalu memakai warna semantic, tidak pernah warna kategori.

## Components

> Mobile-only: state yang didokumentasikan adalah **Default / Pressed / Disabled / Focus** — tidak ada hover.

### Buttons
- **`button-primary`** — CTA utama satu per layar. Background `{colors.primary}`, height 48px, rounded `{rounded.md}`. Pressed → `{colors.primary-pressed}`. Disabled → `{colors.primary-disabled}`.
- **`button-secondary`** — outline hijau, dipakai untuk aksi kedua (mis. "Batal" di samping "Konfirmasi").
- **`button-ghost`** — aksi tersier tanpa border (mis. "Lewati").
- **`button-danger`** — aksi destruktif (mis. "Batalkan Pesanan"), selalu dipasangkan `confirmation-modal`.

### Cards
- **`card-base`** / **`card-elevated`** — kontainer konten umum.
- **`category-tile`** — ubin kategori di grid Perbaiki/Direktori, pakai warna `{colors.category-*}` sebagai aksen ikon/border tipis.
- **`worker-card`** — kartu tukang di direktori (foto, nama, rating, jarak, badge kategori).
- **`listing-card`** — kartu listing Jual-Beli.

### Inputs
- **`text-input`** — field standar, height 52px (lebih besar dari web, untuk kenyamanan sentuh mobile & Persona B).
- **`otp-input-box`** — kotak OTP individual 48×56px.
- **`search-bar`** — pill search, dipakai di Direktori Tukang & Pencarian Teks.

### Badges & Tags
- **`badge-category`** — pakai warna kategori (container bg + on-container text) + ikon kategori.
- **`badge-status-success/warning/error`** — status pesanan, verifikasi, alert.

### Navigation
- **`bottom-nav-user`** (5 tab: Home/Pesanan/Perbaiki/Tukang/Profil, sesuai PRD 5.2 final) dan **`bottom-nav-tukang`** (4 tab: Pesanan Masuk/Profil Usaha/Pendapatan/Notifikasi, sesuai PRD 5.3 final — **bukan** versi 5-tab dari spec handoff Saif yang sudah diaudit menyimpang).
- **`fab-perbaiki`** — tombol tengah menonjol di bottom-nav-user, satu-satunya elemen yang boleh "mengambang" di atas nav bar.

### Overlay
- **`bottom-sheet`** — sudut atas membulat `{rounded.xl}`, dipakai untuk aksi kontekstual ringan (pilih metode bayar, filter).
- **`confirmation-modal`** — dialog tengah, dipakai untuk aksi destruktif/ireversibel (batalkan pesanan, logout).

### Flow-Specific
- **`status-stepper`** (done/active/pending) — progres pesanan Barang Besar.
- **`invoice-card`** — rincian harga final.
- **`earnings-card`** — pendapatan tukang, latar `{colors.primary-container}` (satu-satunya card non-status yang boleh pakai container hijau, karena earnings = sinyal positif).
- **`chat-bubble-sent/received`** — chat Barang Kecil & negosiasi Jual-Beli.
- **`reputation-alert-card`** — latar warning, dipasangkan copy transparan dari PRD Bagian 9.

### Feedback States
- **`toast-snackbar`** — latar gelap netral (bukan hijau, supaya tidak tertukar makna sukses).
- **`skeleton-loader`** — loading state kartu performa & list.
- **`empty-state`** — ilustrasi + teks jujur (lihat prinsip copy PRD Bagian 9), selalu ada CTA lanjutan (tidak ada jalan buntu).
- **`photo-uploader-slot`** — border dashed, dipakai untuk KTP, foto lokasi usaha, before/after.

## Do's and Don'ts

### Do
- Pakai `{colors.primary}` hanya untuk satu CTA utama per layar, nav aktif, dan status "selesai"
- Pasangkan warna kategori & status SELALU dengan ikon + label teks
- Pakai `{typography.numeric-price}`/`{typography.numeric-inline}` (JetBrains Mono) khusus untuk angka uang
- Jaga radius konsisten: 12px untuk card/tombol standar, 24px hanya untuk bottom sheet
- Gunakan copy jujur ala PRD Bagian 9 di setiap empty/error state — jangan pernah layar kosong tanpa arahan

### Don't
- Jangan pakai warna kategori jasa untuk elemen status sistem (sukses/warning/error/info) — beresiko ambigu
- Jangan pakai hijau primary untuk latar besar/body text — hanya untuk aksen & CTA
- Jangan campur dua pustaka ikon berbeda gaya dalam satu file Figma
- Jangan buat komponen baru di luar daftar ini tanpa alasan — cek dulu apakah kebutuhan bisa dipenuhi varian yang sudah ada
- Jangan sampaikan status HANYA lewat warna (wajib checklist aksesibilitas PRD Bagian 11)

## Aksesibilitas (Checklist Wajib — PRD Bagian 11)

| Syarat PRD | Penerapan di Sistem Ini |
|---|---|
| Target sentuh minimal 44×44pt | `button-primary/secondary/danger` = 48px height; `text-input` = 52px; `otp-input-box` = 48×56px — semua di atas ambang |
| Kontras teks-latar minimal 4,5:1 | `{colors.text-primary}` (#14181A) di atas `{colors.surface}` (#FFFFFF) jauh di atas ambang; **kombinasi warna kategori & dark-mode wajib dicek ulang dengan contrast checker langsung di Figma** sebelum dikunci final — nilai di dokumen ini estimasi desain, bukan hasil pengukuran alat |
| Label deskriptif, bukan "klik di sini" | Berlaku di semua microcopy tombol, ikuti nada PRD Bagian 9 |
| Teks bisa diperbesar tanpa merusak layout | Gunakan unit relatif saat implementasi Figma (auto-layout + text resize), hindari height tetap yang memotong teks besar |
| Mode gelap sebagai pilihan | Token dark mode di atas — **belum ada di `blom_merged.html`**, ini kebutuhan baru yang perlu dibangun dari sistem ini, bukan diambil dari build lama |
| Status tidak hanya lewat warna | Semua badge/tag di atas mewajibkan ikon+label, dicatat eksplisit di Do's/Don'ts |

## Catatan Handoff ke Figma

Rekomendasi struktur saat dipindah ke Figma Variables:
1. **Collection "Primitive"** — nilai hex mentah (kalau mau expose scale lebih detail dari yang ada di dokumen ini).
2. **Collection "Semantic"** — persis token di bagian `colors:` frontmatter atas, dengan 2 mode: **Light** dan **Dark** (isi dari tabel Dark Mode di atas) — supaya toggle tema di Figma tinggal switch mode, bukan bikin file duplikat.
3. **Text Styles** — satu style per baris tabel Typography di atas, penamaan `Awetin/{token-name}` (mis. `Awetin/heading-1`).
4. **Effect Styles** — satu per level elevation.
5. Komponen di section **Components** di atas dijadikan Figma Components dengan variant property `state` (Default/Pressed/Disabled/Focus) — bukan file terpisah per state.

## Known Gaps (perlu ditindaklanjuti sebelum dikunci final)

- 4 warna kategori jasa & seluruh token dark-mode adalah **hasil estimasi desain manual** (bukan diambil dari pengukuran kontras otomatis) — wajib diverifikasi dengan contrast checker asli begitu masuk Figma.
- Pustaka ikon belum final dipilih (Phosphor vs Lucide) — cukup dipilih sekali sebelum mulai menyusun komponen di Figma.
- Ilustrasi empty-state/onboarding belum ada aset konkretnya — baru arahan gaya (flat, organik, motif alam).
- Sistem ini **tidak mengatur ulang** keputusan arsitektur "1 app 2 mode vs 2 app terpisah" yang masih terbuka (lihat `Audit - Kesesuaian Handoff Saif vs PRD.md`) — token & komponen di sini berlaku untuk kedua kemungkinan tanpa perlu diubah, karena itu keputusan struktur navigasi, bukan keputusan visual.

## Referensi

- `blom_merged (awetin).html` — sumber token dasar (warna, tipografi, radius, elevation, motion)
- `PRD Lengkap - Awetin.md` — Bagian 4 (Prinsip Desain), 5 (Navigasi), 9 (Microcopy), 11 (Aksesibilitas)
- `CLAUDE.md` — keputusan navbar final (Bagian 4)
- `Audit - Kesesuaian Handoff Saif vs PRD.md` — konteks penyimpangan navbar Mitra yang sengaja TIDAK diikuti di sistem ini
- Metodologi token 3-lapis & rasio pemakaian warna — skill `ui-ux-pro-max:brand` & `ui-ux-pro-max:design-system`
