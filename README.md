# AcehScript untuk VS Code

Extension ini menambahkan dukungan **syntax highlighting** dan **icon file** untuk bahasa AcehScript (`.aceh`, `.as`) di VS Code.

## Fitur

- Syntax highlighting untuk seluruh 52 kata kunci AcehScript (deklarasi variabel, percabangan, perulangan, fungsi, class, error handling, module, dll)
- Highlight untuk string, komentar, dan angka
- Icon file khusus untuk ekstensi `.aceh` dan `.as`
- Auto-closing bracket & tanda kutip

## Instalasi (Manual/Lokal)

1. Copy folder extension ini ke folder extension VS Code:
   - **Windows**: `%USERPROFILE%\.vscode\extensions\acehscript-vscode`
   - **Mac/Linux**: `~/.vscode/extensions/acehscript-vscode`
2. Reload/restart VS Code
3. Syntax highlighting akan otomatis aktif untuk file `.aceh`/`.as`
4. Untuk mengaktifkan icon custom: `Ctrl+Shift+P` → ketik **"Preferences: File Icon Theme"** → pilih **"AcehScript Icons"**

## Struktur Project

```
acehscript-vscode/
├── package.json                    # manifest extension
├── language-configuration.json     # bracket matching, comment toggling
├── syntaxes/
│   └── aceh.tmLanguage.json        # grammar TextMate untuk highlighting
├── icons/
│   ├── acehscript.svg              # icon file explorer (kecil)
│   ├── acehscript-marketplace.svg  # icon marketplace (besar)
│   └── acehscript.png              # icon marketplace (PNG)
├── acehscript-icon-theme.json      # definisi icon theme
└── test.aceh                       # contoh file untuk uji highlighting
```

## Catatan

Icon theme ini **hanya** mendefinisikan ikon untuk `.aceh`/`.as` — file lain akan memakai ikon default VS Code (font-based), karena tema ini tidak melakukan override penuh terhadap seluruh jenis file.
