# Kukode VSCode Icon Theme

Screenshot

![sample icon](./image.png)

### 1. Build dan Jalankan Sementara

Buka VS Code dan jalankan:

```bash
code --extensionDevelopmentPath=path/to/vscode-icon-theme
```

Pilih tema ikon Anda di `File > Preferences > File Icon Theme.`


### 2. Kemas Ekstensi yang sudah dibuat

Jalankan perintah berikut untuk melakukan buid

```bash
vsce package
```

Jika sukses, Anda akan mendapatkan file .vsix di root proyek Anda, misalnya `my-icon-theme-0.1.0.vsix`.

### 3. Install Ekstensi di VS Code Biasa

Berikut langkan untuk install icon:

- Buka VS Code.
- Tekan Ctrl+Shift+P (Windows/Linux) atau Cmd+Shift+P (macOS) untuk membuka Command Palette.
- Ketik dan pilih Extensions: Install from VSIX....
- Pilih file `.vsix` yang telah Anda buat.
- Setelah terinstal, Anda dapat memilih tema ikon Anda di:

```bash
File > Preferences > File Icon Theme > My Icon Theme
```

### 4. Update Ekstensi (Jika Diperlukan)

Jika Anda melakukan perubahan pada tema ikon:

- Perbarui versi di `package.json` (contoh, dari 0.1.0 ke 0.1.1).
- Ulangi langkah untuk membuat paket `.vsix` dan instal ulang.

### 5. Opsional: Publikasikan ke Marketplace

Jika Anda ingin membagikan tema ikon Anda kepada orang lain:

- Daftar akun di [Azure DevOps](https://dev.azure.com/) untuk mendapatkan personal access token (PAT).
- Login ke VSCE dengan token:
  ```bash
  vsce login <your-publisher-name>
  ```
- Publikasikan ekstensi Anda:
  ```bash
  vsce publish
  ```

### 6. Sample JSON File

Sample fileIcons.json

```json
{
    "iconDefinitions": {
	    "javascript": {
		    "iconPath": "./icons/javascript.svg"
		},
		"python": {
		    "iconPath": "./icons/python.svg"
		}
	},
	"fileExtensions": {
		"js": "javascript",
		"py": "python"
	},
	"fileNames": {
		"package.json": "javascript"
	},
	"languageIds": {
		"javascript": "javascript",
		"python": "python"
	}
}
```