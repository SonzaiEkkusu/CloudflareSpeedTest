# XIU2/CloudflareSpeedTest

[![Go Version](https://img.shields.io/github/go-mod/go-version/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Go&color=00ADD8&logo=go)](https://github.com/XIU2/CloudflareSpeedTest/)
[![Release Version](https://img.shields.io/github/v/release/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Release&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/releases/latest)
[![GitHub license](https://img.shields.io/github/license/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=License&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/)
[![GitHub Star](https://img.shields.io/github/stars/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Star&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/)
[![GitHub Fork](https://img.shields.io/github/forks/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Fork&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/)

Banyak situs web internasional yang menggunakan Cloudflare CDN, tetapi IP yang dialokasikan untuk pengunjung dari daratan Cina tidak ramah (latensi tinggi, banyak kehilangan paket, kecepatan lambat).  
Meskipun Cloudflare mengungkapkan semua [rentang IP](https://www.cloudflare.com/zh-cn/ips/), menemukan IP yang sesuai di antara begitu banyak IP dapat sangat melelahkan, jadi software ini dibuat.

**"Pilih IP Terbaik" untuk menguji latensi dan kecepatan Cloudflare CDN, dan mendapatkan IP tercepat (IPv4+IPv6)**! Jika bermanfaat, **beri `⭐` sebagai dukungan~**

> _Bagikan proyek open-source saya yang lain: [**TrackersList.com** - Daftar Tracker BT Terpopuler di seluruh web! Meningkatkan kecepatan unduh BT secara efektif~](https://github.com/XIU2/TrackersListCollection) <img src="https://img.shields.io/github/stars/XIU2/TrackersListCollection.svg?style=flat-square&label=Star&color=4285dd&logo=github" height="16px" />_  
> _[**UserScript** - 🐵 Unduh cepat Github, peningkatan Zhihu, halaman otomatis tanpa batas, mode perlindungan mata, dan beberapa **skrip pengguna** lainnya~](https://github.com/XIU2/UserScript) <img src="https://img.shields.io/github/stars/XIU2/UserScript.svg?style=flat-square&label=Star&color=4285dd&logo=github" height="16px" />_  
> _[**SNIProxy** - 🧷 Proxy SNI sederhana yang saya gunakan (mendukung semua platform, semua sistem, proxy depan, konfigurasi mudah, dll~](https://github.com/XIU2/SNIProxy) <img src="https://img.shields.io/github/stars/XIU2/SNIProxy.svg?style=flat-square&label=Star&color=4285dd&logo=github" height="16px" />_  

> Proyek ini juga mendukung pengujian latensi untuk **CDN / IP situs web lainnya** (seperti: [CloudFront](https://github.com/XIU2/CloudflareSpeedTest/discussions/304), [Gcore](https://github.com/XIU2/CloudflareSpeedTest/discussions/303) CDN), tetapi pengujian unduhan perlu mencari alamat sendiri

> [!IMPORTANT]
> Untuk **proxy yang menggunakan Cloudflare CDN**, perlu diketahui bahwa ini seharusnya menjadi **solusi cadangan**, bukan **satu-satunya solusi**, harap tidak terlalu bergantung pada [#382](https://github.com/XIU2/CloudflareSpeedTest/discussions/382) [#383](https://github.com/XIU2/CloudflareSpeedTest/discussions/383)
****
## # Cara Cepat Menggunakan

### Unduh dan Jalankan

1. Unduh file executable yang sudah dikompilasi ( [Github Releases](https://github.com/XIU2/CloudflareSpeedTest/releases) / [Lanzou Cloud](https://pan.lanpw.com/b0742hkxe) ) dan ekstrak.  
2. Klik dua kali pada file `CloudflareST.exe` (sistem Windows), tunggu hingga pengujian selesai...

<details>
<summary><code><strong>「 Klik di sini untuk melihat contoh penggunaan di sistem Linux 」</strong></code></summary>

****

Perintah berikut hanya sebagai contoh, periksa [**Releases**](https://github.com/XIU2/CloudflareSpeedTest/releases) untuk nomor versi dan nama file.
``` yaml
# Jika ini adalah pertama kalinya Anda menggunakan, disarankan untuk membuat folder baru (langkah ini dapat dilewati pada pembaruan berikutnya)
mkdir CloudflareST

# Masuk ke folder (pada pembaruan berikutnya, Anda hanya perlu mengulangi perintah unduh dan ekstrak dari sini)
cd CloudflareST

# Unduh paket CloudflareST (sesuaikan URL dengan [versi] dan [nama file] sesuai kebutuhan)
wget -N https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# Jika Anda mengunduh dari lingkungan jaringan domestik, gunakan salah satu dari cermin akselerasi berikut:
# wget -N https://download.scholar.rr.nu/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://ghproxy.cc/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://ghproxy.net/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://gh-proxy.com/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://mirror.ghproxy.com/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# Jika unduhan gagal, coba hapus parameter -N (jika untuk pembaruan, ingat untuk menghapus file zip lama terlebih dahulu rm CloudflareST_linux_amd64.tar.gz)

# Ekstrak (tidak perlu menghapus file lama, akan menimpa langsung, sesuaikan nama file sesuai kebutuhan)
tar -zxf CloudflareST_linux_amd64.tar.gz

# Berikan hak akses eksekusi
chmod +x CloudflareST

# Jalankan (tanpa parameter)
./CloudflareST

# Jalankan (contoh dengan parameter)
./CloudflareST -dd -tll 90
```

> Jika **latensi rata-rata sangat rendah** (misalnya 0.xx), ini menunjukkan bahwa CloudflareST **menggunakan proxy** saat pengujian, harap matikan perangkat lunak proxy sebelum melakukan pengujian.  
> Jika menjalankan di **router**, disarankan untuk mematikan proxy di router (atau mengecualikannya), jika tidak, hasil pengujian mungkin **tidak akurat/tidak dapat digunakan**.

</details>

****

> _Panduan sederhana untuk menjalankan CloudflareST secara **mandiri di ponsel**: **[Android](https://github.com/XIU2/CloudflareSpeedTest/discussions/61)、[Android APP](https://github.com/xianshenglu/cloudflare-ip-tester-app)、[IOS](https://github.com/XIU2/CloudflareSpeedTest/discussions/321)**_

> [!NOTE]
> Perhatian! Perangkat lunak ini hanya berlaku untuk situs web, **tidak mendukung pemilihan IP Cloudflare WARP yang menggunakan protokol UDP**, lihat detailnya di: [#392](https://github.com/XIU2/CloudflareSpeedTest/discussions/392)

### Contoh Hasil

Setelah pengujian selesai, secara default akan menampilkan **10 IP tercepat**, contoh:
``` bash
Alamat IP         Terkirim   Diterima   Tingkat Kehilangan   Latensi Rata-Rata   Kecepatan Unduh (MB/s)
104.27.200.69         4         4              0.00                146.23                28.64
172.67.60.78          4         4              0.00                139.82                15.02
104.25.140.153        4         4              0.00                146.49                14.90
104.27.192.65         4         4              0.00                140.28                14.07
172.67.62.214         4         4              0.00                139.29                12.71
104.27.207.5          4         4              0.00                145.92                11.95
172.67.54.193         4         4              0.00                146.71                11.55
104.22.66.8           4         4              0.00                147.42                11.11
104.27.197.63         4         4              0.00                131.29                10.26
172.67.58.91          4         4              0.00                140.19                9.14
...

# Jika latensi rata-rata sangat rendah (misalnya 0.xx), ini menunjukkan bahwa CloudflareST **menggunakan proxy** saat pengujian. Silakan matikan perangkat lunak proxy terlebih dahulu sebelum melakukan pengujian lagi.
# Jika menjalankan di **router**, disarankan untuk mematikan proxy di router (atau mengecualikannya), jika tidak, hasil pengujian mungkin **tidak akurat/tidak dapat digunakan**.

# Karena setiap pengujian dilakukan pada IP acak di setiap rentang IP, hasil pengujian setiap kali tidak mungkin sama, ini adalah hal yang normal!

# Perhatian! Saya menemukan bahwa latensi pengujian pertama setelah komputer dinyalakan akan jauh lebih tinggi (sama seperti TCPing manual), pengujian berikutnya normal.
# Oleh karena itu, disarankan untuk menguji beberapa IP secara sembarangan setelah menyalakan komputer sebelum melakukan pengujian yang sebenarnya (tidak perlu menunggu pengujian latensi selesai, cukup jika bilah kemajuan bergerak bisa langsung ditutup).

# Proses keseluruhan perangkat lunak dengan parameter default kira-kira langkah-langkahnya adalah:
# 1. Pengujian latensi (mode default TCPing, mode HTTPing memerlukan parameter manual)
# 2. Pengurutan latensi (latensi diurutkan dari rendah ke tinggi dan difilter sesuai kondisi, tingkat kehilangan paket yang berbeda akan diurutkan secara terpisah, sehingga beberapa IP dengan latensi rendah tetapi kehilangan paket mungkin berada di belakang)
# 3. Pengujian unduh (dari IP dengan latensi terendah, lakukan pengujian unduh satu per satu, secara default berhenti setelah 10 IP diuji)
# 4. Pengurutan kecepatan (kecepatan diurutkan dari tinggi ke rendah)
# 5. Menampilkan hasil (mengontrol apakah menampilkan hasil di baris perintah (-p 0) atau menulis ke file (-o ""))

# Perhatian: File hasil output result.csv akan menampilkan karakter China yang tidak dapat dibaca dengan benar di Microsoft Excel, ini normal; perangkat lunak spreadsheet lainnya/notepad menampilkan dengan benar
```

测速结果第一行就是**既下载速度最快、又平均延迟最低的最快 IP**！

完整结果保存在当前目录下的 `result.csv` 文件中，用**记事本/表格软件**打开，格式如下：

```
IP 地址,已发送,已接收,丢包率,平均延迟,下载速度 (MB/s)
104.27.200.69,4,4,0.00,146.23,28.64
```

> _大家可以按自己需求，对完整结果**进一步筛选处理**，或者去看一看进阶使用**指定过滤条件**！_

****
## \# 进阶使用

直接运行使用的是默认参数，如果想要测速结果更全面、更符合自己的要求，可以自定义参数。

```Dart
C:\>CloudflareST.exe -h

CloudflareSpeedTest vX.X.X
Uji latensi dan kecepatan semua IP Cloudflare CDN, dapatkan IP tercepat (IPv4+IPv6)!
https://github.com/XIU2/CloudflareSpeedTest

Parameter:
    -n 200
        Jumlah thread pengujian latensi; semakin banyak thread, semakin cepat pengujian latensi, perangkat dengan kinerja rendah (seperti router) sebaiknya tidak menggunakan terlalu banyak; (default 200, maksimum 1000)
    -t 4
        Jumlah pengujian latensi; jumlah pengujian latensi untuk setiap IP; (default 4 kali)
    -dn 10
        Jumlah pengujian unduh; jumlah pengujian unduh setelah pengujian latensi dan pengurutan berdasarkan latensi terendah; (default 10)
    -dt 10
        Waktu pengujian unduh; waktu maksimum untuk pengujian unduh setiap IP, tidak boleh terlalu pendek; (default 10 detik)
    -tp 443
        Port pengujian yang ditentukan; port yang digunakan untuk pengujian latensi/pengujian unduh; (default port 443)
    -url https://cf.xiu2.xyz/url
        Alamat pengujian yang ditentukan; alamat yang digunakan untuk pengujian latensi (HTTPing)/pengujian unduh, alamat default tidak menjamin ketersediaan, disarankan untuk menggunakan alamat yang dibuat sendiri;

    -httping
        Ubah mode pengujian; ubah mode pengujian latensi menjadi protokol HTTP, alamat pengujian yang digunakan adalah parameter [-url]; (default TCPing)
        Catatan: HTTPing pada dasarnya juga merupakan tindakan pemindaian jaringan, jadi jika Anda menjalankannya di server, turunkan tingkat konkurensi (-n), jika tidak, layanan Anda mungkin akan dihentikan oleh beberapa penyedia yang ketat.
        Jika Anda mengalami kasus di mana jumlah IP yang dapat diuji dengan HTTPing awalnya normal, tetapi semakin sedikit atau bahkan nol setelahnya, dan kembali normal setelah jeda, ini mungkin karena operator atau CDN Cloudflare menganggap Anda sedang melakukan pemindaian jaringan dan memicu mekanisme pembatasan sementara. Disarankan untuk menurunkan konkurensi (-n) untuk mengurangi kejadian ini.
    -httping-code 200
        Kode status yang valid; kode status HTTP yang valid yang dikembalikan oleh halaman selama pengujian latensi HTTPing, hanya satu; (default 200 301 302)
    -cfcolo HKG,KHH,NRT,LAX,SEA,SJC,FRA,MAD
        Cocokkan wilayah tertentu; nama wilayah dengan kode bandara tiga huruf, dipisahkan dengan koma, mendukung huruf kecil, mendukung Cloudflare, AWS CloudFront, hanya tersedia dalam mode HTTPing; (default semua wilayah)

    -tl 200
        Batas latensi rata-rata; hanya output IP yang memiliki latensi rata-rata di bawah batas yang ditentukan, batas atas dan bawah dapat digunakan bersama; (default 9999 ms)
    -tll 40
        Batas bawah latensi rata-rata; hanya output IP yang memiliki latensi rata-rata di atas batas yang ditentukan; (default 0 ms)
    -tlr 0.2
        Batas tingkat kehilangan paket; hanya output IP yang memiliki tingkat kehilangan paket di bawah atau sama dengan batas yang ditentukan, rentang 0.00~1.00, 0 untuk menyaring IP tanpa kehilangan paket; (default 1.00)
    -sl 5
        Batas kecepatan unduh; hanya output IP yang memiliki kecepatan unduh di atas batas yang ditentukan, pengujian akan berhenti setelah mencapai jumlah yang ditentukan [-dn]; (default 0.00 MB/s)

    -p 10
        Jumlah hasil yang ditampilkan; langsung menampilkan jumlah hasil yang ditentukan setelah pengujian, 0 berarti tidak menampilkan hasil dan langsung keluar; (default 10)
    -f ip.txt
        File data rentang IP; jika jalur mengandung spasi, tambahkan tanda kutip; mendukung rentang IP CDN lainnya; (default ip.txt)
    -ip 1.1.1.1,2.2.2.2/24,2606:4700::/32
        Data rentang IP yang ditentukan; langsung menentukan rentang IP yang akan diuji melalui parameter, dipisahkan dengan koma; (default kosong)
    -o result.csv
        Tulis file hasil; jika jalur mengandung spasi, tambahkan tanda kutip; jika kosong, tidak menulis ke file [-o ""]; (default result.csv)

    -dd
        Nonaktifkan pengujian unduh; jika dinonaktifkan, hasil pengujian akan diurutkan berdasarkan latensi (default diurutkan berdasarkan kecepatan unduh); (default aktif)
    -allip
        Uji semua IP; uji setiap IP dalam rentang IP (hanya mendukung IPv4); (default uji satu IP secara acak dalam setiap rentang /24)

    -v
        Tampilkan versi program + periksa pembaruan versi
    -h
        Tampilkan petunjuk bantuan
```

### 界面解释

为了避免大家对测速过程中的**输出内容产生误解（可用、队列等数字，下载测速一半就"中断"？）**，我特意解释下。

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

> 该示例把常用参数都给加上了，即为：`-ttl 40 -tl 150 -sl 1 -dn 5`，最后输出结果如下：

```python
# XIU2/CloudflareSpeedTest vX.X.X

开始延迟测速（模式：TCP, 端口：443, 范围：40 ~ 150 ms, 丢包：1.00)
321 / 321 [-----------------------------------------------------------] 可用: 30
开始下载测速（下限：1.00 MB/s, 数量：5, 队列：10）
3 / 5 [-----------------------------------------↗--------------------]
IP 地址           已发送  已接收  丢包率  平均延迟  下载速度 (MB/s)
XXX.XXX.XXX.XXX   4       4      0.00    83.32    3.66
XXX.XXX.XXX.XXX   4       4      0.00    107.81   2.49
XXX.XXX.XXX.XXX   4       3      0.25    149.59   1.04

完整测速结果已写入 result.csv 文件，可使用记事本/表格软件查看。
按下 回车键 或 Ctrl+C 退出。
```

****

> 刚接触 CloudflareST 的人，可能会迷惑**明明延迟测速可用 IP 有 30 个，怎么最后只剩下 3 个了呢？**  
> 下载测速里的队列又是什么意思？难道我下载测速还要排队？

CloudflareST 会先延迟测速，在这过程中进度条右侧会实时显示可用 IP 数量（`可用: 30`），但注意该可用数量指的是**测试通过没有超时的 IP 数量**，和延迟上下限、丢包条件无关。当延迟测速完成后，因为还指定了**延迟上下限、丢包**的条件，所以按照条件过滤后只剩下 `10` 个了（也就是等待下载测速的 `队列：10`）。

即以上示例中，`321` 个 IP 延迟测速完成后，只有 `30` 个 IP 测试通过没有超时，然后根据延迟上下限范围：`40 ~ 150 ms` 及丢包上限条件过滤后，只剩下 `10` 个满足要求的 IP 了。如果你 `-dd` 禁用了下载测速，那么就会直接输出这 `10` 个 IP 了。当然该示例并未禁用，因此接下来软件会继续对这 `10` 个 IP 进行下载测速（`队列：10`）。

> 因为下载测速是单线程一个个 IP 挨着排队测速的，因此等待下载测速的 IP 数量才会叫做 `队列`。

****

> 你可能注意到了，**明明指定了要找到 5 个满足下载速度条件的 IP，怎么才 3 个就 “中断” 了呢？**

下载测速进度条中的 `3 / 5`，前者指的是找到了 `3` 个满足下载速度下限条件的 IP（即下载速度高于 `1 MB/s` ），后者 `5` 指的是你要求找到 `5` 个满足下载速度下限条件的 IP（`-dn 5`）。

> 另外，提醒一下，如果你指定的 `-dn` 大于下载测速队列，比如你延迟测速后只剩下 `4` 个 IP 了，那么下载测速进度条中后面的数字就会和下载测速队列一样都是 `4` 个，而非你 `-dn` 指定的 `5` 个了。

软件在测速完这 `10` 个 IP 后，只找到了 `3` 个下载速度高于 `1 MB/s` 的 IP，剩下的 `7` 个 IP 都是 “不及格” 的。

因此，这不是 `“每次测速都不到 5 就中断了”`，而是所有 IP 都下载测速完了，但却只找到了 `3` 个满足条件的。

****

如果不想遇到这种全部测速一遍都没几个满足条件的情况，那么就要**调低下载速度上限参数 `-sl`**，或者移除。

因为只要指定了 `-sl` 参数，那么只要没有凑够 `-dn` 的数量（默认 10 个），就会一直测速下去，直到凑够或全部测速完。移除 `-sl` 并添加 `-dn 20` 参数，这样就是只测速延迟最低的前 20 个 IP，测速完就停止，节省时间。

****

另外，如果全部队列 IP 都测速完了，但一个满足下载速度条件的 IP 都没有，那么就会**直接输出全部队列 IP 的下载测速结果**，这样你就能看到这些 IP 的下载速度都有多少，心里也就有数了，然后**适当调低 `-sl` 再试试**。

同样，延迟测速方面，`可用: 30`、`队列：10` 这两个数值也可以让你清楚，你设置的延迟条件对你来说是否过于苛刻。如果可用 IP 一大堆，但条件过滤后只剩下 2、3 个，那不用说就知道需要**调低预期的延迟/丢包条件**了。

这两个机制，一个是告诉你**延迟丢包条件**是否合适的，一个是告诉你**下载速度条件**是否合适的。

</details>

****

### 使用示例

Windows 要指定参数需要在 CMD 中运行，或者把参数添加到快捷方式目标中。

> [!TIP]
> - 各参数均有**默认值**，使用默认值的参数是可以省略的（**按需选择**），参数**不分前后顺序**。  
> - Windows **PowerShell** 只需把下面命令中的 `CloudflareST.exe` 改为 `.\CloudflareST.exe` 即可。  
> - Linux 系统只需要把下面命令中的 `CloudflareST.exe` 改为 `./CloudflareST` 即可。

****

#### \# CMD 带参数运行 CloudflareST

对命令行程序不熟悉的人，可能不知道该如何带参数运行，我就简单说一下。

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

很多人打开 CMD 以**绝对路径**运行 CloudflareST 会报错，这是因为默认的 `-f ip.txt` 参数是相对路径，需要指定绝对路径的 ip.txt 才行，但这样毕竟太麻烦了，因此还是建议进入 CloudflareST 程序目录下，以**相对路径**方式运行：

**方式 一**：
1. 打开 CloudflareST 程序所在目录  
2. 空白处按下 <kbd>Shift + 鼠标右键</kbd> 显示右键菜单  
3. 选择 **\[在此处打开命令窗口\]** 来打开 CMD 窗口，此时默认就位于当前目录下  
4. 输入带参数的命令，如：`CloudflareST.exe -tll 50 -tl 200`即可运行

**方式 二**：
1. 打开 CloudflareST 程序所在目录  
2. 直接在文件夹地址栏中全选并输入 `cmd` 回车来打开 CMD 窗口，此时默认就位于当前目录下  
4. 输入带参数的命令，如：`CloudflareST.exe -tll 50 -tl 200`即可运行

> 当然你也可以随便打开一个 CMD 窗口，然后输入如 `cd /d "D:\Program Files\CloudflareST"` 来进入程序目录

> **提示**：如果用的是 **PowerShell** 只需把命令中的 `CloudflareST.exe` 改为 `.\CloudflareST.exe` 即可。

</details>

****

#### \# Windows 快捷方式带参数运行 CloudflareST

如果不经常修改运行参数（比如平时都是直接双击运行）的人，建议使用快捷方式，更方便点。

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

右键 `CloudflareST.exe` 文件 - **\[创建快捷方式\]**，然后右键该快捷方式 - **\[属性\]**，修改其**目标**：

``` bash
# 如果要不输出结果文件，那么请加上 -o " "，引号里的是空格（没有空格会导致该参数被省略）。
D:\ABC\CloudflareST\CloudflareST.exe -n 500 -t 4 -dn 20 -dt 5 -o " "

# 如果文件路径包含引号，则需要把启动参数放在引号外面，记得引号和 - 之间有空格。
"D:\Program Files\CloudflareST\CloudflareST.exe" -n 500 -t 4 -dn 20 -dt 5 -o " "

# 注意！快捷方式 - 起始位置 不能是空的，否则就会因为绝对路径而找不到 ip.txt 文件
```

</details>

****

#### \# IPv4/IPv6

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****
``` bash
# 指定自带的 IPv4 数据文件可测速这些 IPv4 地址（-f 默认值就是 ip.txt，所以该参数可省略）
CloudflareST.exe -f ip.txt

# 指定自带的 IPv6 数据文件可测速这些 IPv6 地址
# 另外，v2.1.0 版本后支持 IPv4+IPv6 混合测速并移除了 -ipv6 参数，因此一个文件内可以同时包含 IPv4+IPv6 地址
CloudflareST.exe -f ipv6.txt

# 也可以直接通过参数指定要测速的 IP
CloudflareST.exe -ip 1.1.1.1,2606:4700::/32
```

> 测速 IPv6 时，可能会注意到每次测速数量都不一样，了解原因： [#120](https://github.com/XIU2/CloudflareSpeedTest/issues/120)  
> 因为 IPv6 太多（以亿为单位），且绝大部分 IP 段压根未启用，所以我只扫了一部分可用的 IPv6 段写到 `ipv6.txt` 文件中，有兴趣的可以自行扫描增删，ASN 数据源来自：[bgp.he.net](https://bgp.he.net/AS13335#_prefixes6)

</details>

****

#### \# HTTPing

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

目前有两种延迟测速模式，分别为 **TCP 协议、HTTP 协议**。  
TCP 协议耗时更短、消耗资源更少，超时时间为 1 秒，该协议为默认模式。  
HTTP 协议适用于快速测试某域名指向某 IP 时是否可以访问，超时时间为 2 秒。  
同一个 IP，各协议去 Ping 得到的延迟一般为：**ICMP < TCP < HTTP**，越靠右对丢包等网络波动越敏感。

> 注意：HTTPing 本质上也算一种**网络扫描**行为，因此如果你在服务器上面运行，需要**降低并发**(`-n`)，否则可能会被一些严格的商家暂停服务。如果你遇到 HTTPing 首次测速可用 IP 数量正常，后续测速越来越少甚至直接为 0，但停一段时间后又恢复了的情况，那么也可能是被 运营商、Cloudflare CDN 认为你在网络扫描而**触发临时限制机制**，因此才会过一会儿就恢复了，建议**降低并发**(`-n`)减少这种情况的发生。

> 另外，本软件 HTTPing 仅获取**响应头(response headers)**，并不获取正文内容（即 URL 文件大小不影响 HTTPing 测试，但如果你还要下载测速的话，那么还是需要一个大文件的），类似于 curl -i 功能。

``` bash
# 只需加上 -httping 参数即可切换到 HTTP 协议延迟测速模式
CloudflareST.exe -httping

# 软件会根据访问时网页返回的有效 HTTP 状态码来判断可用性（当然超时也算），默认对返回 200 301 302 这三个 HTTP 状态码的视为有效，可以手动指定认为有效的 HTTP 状态码，但只能指定一个（你需要提前确定测试地址正常情况下会返回哪个状态码）
CloudflareST.exe -httping -httping-code 200

# 通过 -url 参数来指定 HTTPing 测试地址（可以是任意网页 URL，不局限于具体文件地址）
CloudflareST.exe -httping -url https://cf.xiu2.xyz/url
# 如果你要 HTTPing 测试其他网站/CDN，那么指定一个该网站/使用该 CDN 的地址（因为软件默认地址是 Cloudflare 的，只能用于测试 Cloudflare 的 IP）

# 注意：如果测速地址为 HTTP 协议，记得加上 -tp 80（这个参数会影响 延迟测速/下载测速 时使用的端口）
# 同理，如果要测速 80 端口，那么也需要加上 -url 参数来指定一个 http:// 协议的地址才行（且该地址不会强制重定向至 HTTPS），如果是非 80 443 端口，那么需要确定该下载测速地址是否支持通过该端口访问。
CloudflareST.exe -httping -tp 80 -url http://cdn.cloudflare.steamstatic.com/steam/apps/5952/movie_max.webm
```

</details>

****

#### \# 匹配指定地区(colo 机场三字码)

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

``` bash
# 该功能支持 Cloudflare CDN、AWS CloudFront CDN，且这两个 CDN 的机场三字码是通用的
# 注意：如果你要用于筛选 AWS CloudFront CDN 地区，那么要通过 -url 参数指定一个使用该 CDN 的地址（因为软件默认地址是 Cloudflare 的）

# 指定地区名后，延迟测速后得到的结果就都是指定地区的 IP 了（也可以继续进行下载测速）
# 节点地区名为当地 机场三字码，指定多个时用英文逗号分隔，v2.2.3 版本后支持小写

CloudflareST.exe -cfcolo HKG,KHH,NRT,LAX,SEA,SJC,FRA,MAD

# 注意，该参数只有在 HTTPing 延迟测速模式下才可用（因为要访问网页来获得）
```

> 两个 CDN 机场三字码通用，因此各地区名可见：https://www.cloudflarestatus.com/

</details>

****

#### \# 文件相对/绝对路径

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

``` bash
# 指定 IPv4 数据文件，不显示结果直接退出，输出结果到文件（-p 值为 0）
CloudflareST.exe -f 1.txt -p 0 -dd

# 指定 IPv4 数据文件，不输出结果到文件，直接显示结果（-p 值为 10 条，-o 值为空但引号不能少）
CloudflareST.exe -f 2.txt -o "" -p 10 -dd

# 指定 IPv4 数据文件 及 输出结果到文件（相对路径，即当前目录下，如含空格请加上引号）
CloudflareST.exe -f 3.txt -o result.txt -dd


# 指定 IPv4 数据文件 及 输出结果到文件（相对路径，即当前目录内的 abc 文件夹下，如含空格请加上引号）
# Linux（CloudflareST 程序所在目录内的 abc 文件夹下）
./CloudflareST -f abc/3.txt -o abc/result.txt -dd

# Windows（注意是反斜杠）
CloudflareST.exe -f abc\3.txt -o abc\result.txt -dd


# 指定 IPv4 数据文件 及 输出结果到文件（绝对路径，即 C:\abc\ 目录下，如含空格请加上引号）
# Linux（/abc/ 目录下）
./CloudflareST -f /abc/4.txt -o /abc/result.csv -dd

# Windows（注意是反斜杠）
CloudflareST.exe -f C:\abc\4.txt -o C:\abc\result.csv -dd


# 如果要以【绝对路径】运行 CloudflareST，那么 -f / -o 参数中的文件名也必须是【绝对路径】，否则会报错找不到文件！
# Linux（/abc/ 目录下）
/abc/CloudflareST -f /abc/4.txt -o /abc/result.csv -dd

# Windows（注意是反斜杠）
C:\abc\CloudflareST.exe -f C:\abc\4.txt -o C:\abc\result.csv -dd
```
</details>

****

#### \# 测速其他端口

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

``` bash
# 如果你想要测速非默认 443 的其他端口，则需要通过 -tp 参数指定（该参数会影响 延迟测速/下载测速 时使用的端口）

# 如果要延迟测速 80 端口+下载测速（如果 -dd 禁用了下载测速则不需要），那么还需要指定 http:// 协议的下载测速地址才行（且该地址不会强制重定向至 HTTPS，因为那样就变成 443 端口了）
CloudflareST.exe -tp 80 -url http://cdn.cloudflare.steamstatic.com/steam/apps/5952/movie_max.webm

# 如果是非 80 443 的其他端口，那么需要确定你使用的下载测速地址是否支持通过该非标端口访问。
```

</details>

****

#### \# 自定义测速地址

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

``` bash
# 该参数适用于下载测速 及 HTTP 协议的延迟测速，对于后者该地址可以是任意网页 URL（不局限于具体文件地址）

# 地址要求：可以直接下载、文件大小超过 200MB、用的是 Cloudflare CDN
CloudflareST.exe -url https://cf.xiu2.xyz/url

# 注意：如果测速地址为 HTTP 协议（该地址不能强制重定向至 HTTPS），记得加上 -tp 80（这个参数会影响 延迟测速/下载测速 时使用的端口），如果是非 80 443 端口，那么需要确定下载测速地址是否支持通过该端口访问。
CloudflareST.exe -tp 80 -url http://cdn.cloudflare.steamstatic.com/steam/apps/5952/movie_max.webm
```

</details>

****

#### \# 自定义测速条件（指定 延迟/丢包/下载速度 的目标范围）

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

> 注意：延迟测速进度条右边的**可用数量**，仅指延迟测速过程中**未超时的 IP 数量**，和延迟上下限条件无关。

- 仅指定 **[平均延迟上限]** 条件

``` bash
# 平均延迟上限：200 ms，下载速度下限：0 MB/s
# 即找到平均延迟低于 200 ms 的 IP，然后再按延迟从低到高进行 10 次下载测速
CloudflareST.exe -tl 200
```

> 如果**没有找到一个满足延迟**条件的 IP，那么不会输出任何内容。

****

- 仅指定 **[平均延迟上限]** 条件，且**只延迟测速，不下载测速**

``` bash
# 平均延迟上限：200 ms，下载速度下限：0 MB/s，数量：不知道多少 个
# 即只输出低于 200ms 的 IP，且不再下载测速（因为不再下载测速，所以 -dn 参数就无效了）
CloudflareST.exe -tl 200 -dd
```

- 仅指定 **[丢包几率上限]** 条件

``` bash
# 丢包几率上限：0.25
# 即找到丢包率低于等于 0.25 的 IP，范围 0.00~1.00，如果 -tlr 0 则代表过滤掉任何丢包的 IP
CloudflareST.exe -tlr 0.25
```

****

- 仅指定 **[下载速度下限]** 条件

``` bash
# 平均延迟上限：9999 ms，下载速度下限：5 MB/s，数量：10 个（可选）
# 即需要找到 10 个平均延迟低于 9999 ms 且下载速度高于 5 MB/s 的 IP 才会停止测速
CloudflareST.exe -sl 5 -dn 10
```

> 如果**没有找到一个满足速度**条件的 IP，那么会**忽略条件输出所有 IP 测速结果**（方便你下次测速时调整条件）。

> 没有指定平均延迟上限时，如果一直**凑不够**满足条件的 IP 数量，就会**一直测速**下去。  
> 所以建议**同时指定 [下载速度下限] + [平均延迟上限]**，这样测速到指定延迟上限还没凑够数量，就会终止测速。

****

- 同时指定 **[平均延迟上限] + [下载速度下限]** 条件

``` bash
# 平均延迟上限、下载速度下限均支持小数（如 -sl 0.5）
# 平均延迟上限：200 ms，下载速度下限：5.6 MB/s，数量：10 个（可选）
# 即需要找到 10 个平均延迟低于 200 ms 且下载速度高于 5 .6MB/s 的 IP 才会停止测速
CloudflareST.exe -tl 200 -sl 5.6 -dn 10
```

> 如果**没有找到一个满足延迟**条件的 IP，那么不会输出任何内容。  
> 如果**没有找到一个满足速度**条件的 IP，那么会忽略条件输出所有 IP 测速结果（方便你下次测速时调整条件）。  
> 所以建议先不指定条件测速一遍，看看平均延迟和下载速度大概在什么范围，避免指定条件**过低/过高**！

> 因为 Cloudflare 公开的 IP 段是**回源 IP+任播 IP**，而**回源 IP**是无法使用的，所以下载测速是 0.00。  
> 运行时可以加上 `-sl 0.01`（下载速度下限），过滤掉**回源 IP**（下载测速低于 0.01MB/s 的结果）。

</details>

****

#### \# 单独对一个或多个 IP 测速

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

**方式 一**：
直接通过参数指定要测速的 IP 段数据。
``` bash
# 先进入 CloudflareST 所在目录，然后运行：
# Windows 系统（在 CMD 中运行）
CloudflareST.exe -ip 1.1.1.1,2.2.2.2/24,2606:4700::/32

# Linux 系统
./CloudflareST -ip 1.1.1.1,2.2.2.2/24,2606:4700::/32
```

****

**方式 二**：
或者把这些 IP 按如下格式写入到任意文本文件中，例如：`1.txt`

```
1.1.1.1
1.1.1.200
1.0.0.1/24
2606:4700::/32
```

> 单个 IP 的话可以省略 `/32` 子网掩码了（即 `1.1.1.1`等同于 `1.1.1.1/32`）。  
> 子网掩码 `/24` 指的是这个 IP 最后一段，即 `1.0.0.1~1.0.0.255`。


然后运行 CloudflareST 时加上启动参数 `-f 1.txt` 来指定 IP 段数据文件。

``` bash
# 先进入 CloudflareST 所在目录，然后运行：
# Windows 系统（在 CMD 中运行）
CloudflareST.exe -f 1.txt

# Linux 系统
./CloudflareST -f 1.txt

# 对于 1.0.0.1/24 这样的 IP 段只会随机最后一段（1.0.0.1~255），如果要测速该 IP 段中的所有 IP，请加上 -allip 参数。
```

</details>

****

#### \# 一劳永逸加速所有使用 Cloudflare CDN 的网站（不需要再一个个添加域名到 Hosts 了）

我以前说过，开发该软件项目的目的就是为了通过**改 Hosts 的方式来加速访问使用 Cloudflare CDN 的网站**。

但就如 [**#8**](https://github.com/XIU2/CloudflareSpeedTest/issues/8) 所说，一个个添加域名到 Hosts 实在**太麻烦**了，于是我就找到了个**一劳永逸**的办法！可以看这个 [**还在一个个添加 Hosts？完美本地加速所有使用 Cloudflare CDN 的网站方法来了！**](https://github.com/XIU2/CloudflareSpeedTest/discussions/71) 和另一个[依靠本地 DNS 服务来修改域名解析 IP 为自选 IP](https://github.com/XIU2/CloudflareSpeedTest/discussions/317) 的教程。

****

#### \# 自动更新 Hosts

考虑到很多人获得最快 Cloudflare CDN IP 后，需要替换 Hosts 文件中的 IP。

可以看这个 [**Issues**](https://github.com/XIU2/CloudflareSpeedTest/discussions/312) 获取 **Windows/Linux 自动更新 Hosts 脚本**！

****

## 问题反馈

如果你遇到什么问题，可以先去 [**Issues**](https://github.com/XIU2/CloudflareSpeedTest/issues)、[Discussions](https://github.com/XIU2/CloudflareSpeedTest/discussions) 里看看是否有别人问过了（记得去看下  [**Closed**](https://github.com/XIU2/CloudflareSpeedTest/issues?q=is%3Aissue+is%3Aclosed) 的）。  
如果没找到类似问题，请新开个 [**Issues**](https://github.com/XIU2/CloudflareSpeedTest/issues/new) 来告诉我！

> [!NOTE]
> **注意**！_与 CloudflareST 本身 `反馈问题、功能建议` 无关的，请前往项目内部 论坛 讨论（顶部的 `💬 Discussions`_  

****

## 赞赏支持

![微信赞赏](https://github.com/XIU2/XIU2/blob/master/img/zs-01.png)![支付宝赞赏](https://github.com/XIU2/XIU2/blob/master/img/zs-02.png)

****

## 衍生项目

- _https://github.com/xianshenglu/cloudflare-ip-tester-app_  
_**CloudflareST 安卓版 APP [#202](https://github.com/XIU2/CloudflareSpeedTest/discussions/320)**_

- _https://github.com/mingxiaoyu/luci-app-cloudflarespeedtest_  
_**CloudflareST OpenWrt 路由器插件版 [#174](https://github.com/XIU2/CloudflareSpeedTest/discussions/319)**_

- _https://github.com/immortalwrt-collections/openwrt-cdnspeedtest_  
_**CloudflareST OpenWrt 原生编译版本 [#64](https://github.com/XIU2/CloudflareSpeedTest/discussions/64)**_

- _https://github.com/hoseinnikkhah/CloudflareSpeedTest-English_  
_**English language version of CloudflareST (Text language differences only) [#64](https://github.com/XIU2/CloudflareSpeedTest/issues/68)**_

> _此处仅收集了在本项目中宣传过的部分 CloudflareST 相关衍生项目，如果有遗漏可以告诉我~_

****

## 感谢项目

- _https://github.com/Spedoske/CloudflareScanner_

> _因为该项目已经很长时间没更新了，而我又产生了很多功能需求，所以我临时学了下 Go 语言就上手了（菜）..._  
> _本软件基于该项目制作，但**已添加大量功能及修复 BUG**，并根据大家的使用反馈积极添加、优化功能（闲）..._

****

## 手动编译

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

为了方便，我是在编译的时候将版本号写入代码中的 version 变量，因此你手动编译时，需要像下面这样在 `go build` 命令后面加上 `-ldflags` 参数来指定版本号：

```bash
go build -ldflags "-s -w -X main.version=v2.3.3"
# 在 CloudflareSpeedTest 目录中通过命令行（例如 CMD、Bat 脚本）运行该命令，即可编译一个可在和当前设备同样系统、位数、架构的环境下运行的二进制程序（Go 会自动检测你的系统位数、架构）且版本号为 v2.3.3
```

如果想要在 Windows 64位系统下编译**其他系统、架构、位数**，那么需要指定 **GOOS** 和 **GOARCH** 变量。

例如在 Windows 系统下编译一个适用于 **Linux 系统 amd 架构 64 位**的二进制程序：

```bat
SET GOOS=linux
SET GOARCH=amd64
go build -ldflags "-s -w -X main.version=v2.3.3"
```

例如在 Linux 系统下编译一个适用于 **Windows 系统 amd 架构 32 位**的二进制程序：

```bash
GOOS=windows
GOARCH=386
go build -ldflags "-s -w -X main.version=v2.3.3"
```

> 可以运行 `go tool dist list` 来查看当前 Go 版本支持编译哪些组合。

****

当然，为了方便批量编译，我会专门指定一个变量为版本号，后续编译直接调用该版本号变量即可。  
同时，批量编译的话，还需要分开放到不同文件夹才行（或者文件名不同），需要加上 `-o` 参数指定。

```bat
:: Windows 系统下是这样：
SET version=v2.3.3
SET GOOS=linux
SET GOARCH=amd64
go build -o Releases\CloudflareST_linux_amd64\CloudflareST -ldflags "-s -w -X main.version=%version%"
```

```bash
# Linux 系统下是这样：
version=v2.3.3
GOOS=windows
GOARCH=386
go build -o Releases/CloudflareST_windows_386/CloudflareST.exe -ldflags "-s -w -X main.version=${version}"
```

</details>

****

## License

The GPL-3.0 License.
