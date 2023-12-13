# How to Install Pentaho on Mac

## Step 1 : Install JDK

* Pastikan sudah terinstall homebrew
* Install JDK melalui homebrew (disarankan menggunakan Versi JDK 11) 
* install menggunakan script tersebut` brew install openjdk@11 `  atau coba buka link berikut https://formulae.brew.sh/formula/openjdk@11

## Step 2 : Install Pentaho

* Unduh Pentaho pada link berikut https://www.hitachivantara.com/en-us/products/pentaho-plus-platform/data-integration-analytics/pentaho-community-edition.html
* Pilih bagian Client Tools pada file dengan format pdi-ce-<versi pentaho>.zip
* Ekstrak hasil unduhan
* Buka Terminal
* Masuk ke direktori hasil Ekstrak (default nama direktori adalah data-integration)
* Jalakan pentaho dengan menggunakan script ` ./spoon.sh `

## Step 3 : Jika Muncul Error 1

* Jika muncul error pada saat menjalankan ` ./spoon.sh ` sepertti error di bawah ini
` I'm sorry, this Mac platform [arm64] is not yet supported!
Please try starting using 'Data Integration 32-bit' or
'Data Integration 64-bit' as appropriate. `
* Jalakan pentahoo dengan menggunakan Rossetta, yaitu dengan cara
* Buka menu setting pada terminal
* Tambah Profile baru dengan klik tombol panah di kiri bawah
* Berikan nama Profile 
* Buka tab Shell
* Check "Run command" lalu isikan ` env /usr/bin/arch -x86_64 /bin/zsh --login `
* UnCheck ` Run inside shell `
* Tutup menu setting
* Buka window terminal baru dengan profile yang telah kita buat tadi
* masuk ke direktori pentaho dan Jalakan kembali pentaho

## Step 3 : Jika Muncul Error 2

* Jika muncul error pada saat menjalankan ` ./spoon.sh ` sepertti error di bawah ini
` java.lang.UnsatisfiedLinkError: Could not load SWT library. Reasons: `
* Buka direktori pentaho (default nya adalah data-integration)
* buka folder libswt/osx64
* hapus file swt.jar
* Unduh swt.jar baru melalui link berikut  https://github.com/prasetyanurangga/how_to_install_pentaho_on_mac/raw/main/swt.jar
* copy swt.jar yang telah di unduh tadi ke folder  libswt/osx64 pada direktori pentaho
* Jalakan kembali pentaho

## Step 3 : Jika Muncul Error 3

* Jika saat membuka pentaho dan membuka halaman setting pentaho tulisan tidak muncul, seperti gambar di bawah
![alt text](https://raw.githubusercontent.com/prasetyanurangga/how_to_install_pentaho_on_mac/main/screenshoot/1*na1p0ZJSweD7r9N53jxTPQ.webp)
* Buka halaman setting pentaho
* pilih tab seperti gambar di bawah
![alt text](https://raw.githubusercontent.com/prasetyanurangga/how_to_install_pentaho_on_mac/main/screenshoot/1*na1p0ZJSweD7r9N53jxTPQ.webp)
* Centang seperti gambar di bawah dan Klik Button seperti gambar di bawah
![alt text](https://raw.githubusercontent.com/prasetyanurangga/how_to_install_pentaho_on_mac/main/screenshoot/1*17WA4VunzEcbVQFqkqXxvw.webp)
* Restart pentaho

