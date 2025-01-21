Tags: [[hacking_fundamentals]]

## Apa itu Bug Bounty?

**Bug Bounty** adalah program yang diadakan oleh perusahaan atau organisasi untuk mengevaluasi dan meningkatkan keamanan sistem mereka. Melalui program ini, perusahaan menawarkan hadiah atau insentif kepada individu atau profesional di bidang keamanan siber yang berhasil menemukan dan melaporkan kerentanan atau bug di sistem atau aplikasi mereka.

Program Bug Bounty menjadi sangat populer karena memungkinkan perusahaan untuk mendapatkan pengujian keamanan dari banyak profesional dengan beragam keahlian dan perspektif, sekaligus memberikan insentif kepada mereka yang berhasil menemukan potensi kerentanannya.

---

## Cara Mengikuti Program Bug Bounty

1. **Mencari Program Bug Bounty**
    
    - Beberapa perusahaan memiliki program Bug Bounty terbuka yang dapat diikuti siapa saja.
    - Ada juga yang bersifat tertutup, di mana hanya individu yang diundang atau yang memiliki undangan yang dapat berpartisipasi.
    - Program ini bisa ditemukan di situs web perusahaan tertentu atau di platform seperti **[HackerOne](https://www.hackerone.com/)**, **[BugCrowd](https://www.bugcrowd.com/)**, dan **[Synack](https://www.synack.com/)**.
2. **Pahami Peraturan Program**
    
    - **Jenis Kerentanan yang Diterima**: Program Bug Bounty hanya menerima jenis kerentanan tertentu. Pastikan Anda memahami apa yang dapat dilaporkan dan apa yang tidak.
    - **Batas Geografis**: Beberapa program mungkin membatasi siapa yang dapat berpartisipasi berdasarkan lokasi geografis.
    - **Hadiah yang Ditawarkan**: Hadiah dapat berupa uang, merchandise, sertifikat, atau ucapan terima kasih dari perusahaan.
3. **Cari dan Laporkan Bug**
    
    - Jika menemukan kerentanan, segera buat laporan yang jelas dan rinci mengenai kerentanannya. Sertakan langkah-langkah untuk mereplikasi bug tersebut dan dampak yang dapat ditimbulkan.
    - Laporan umumnya dikirim melalui email atau platform yang disediakan oleh penyelenggara program. Jika bug yang dilaporkan valid, Anda akan menerima hadiah sesuai ketentuan program.

---

## Mencari Event Bug Bounty dengan Google Dorking

**Google Dorking** adalah teknik yang menggunakan operator pencarian canggih di Google untuk menemukan informasi tersembunyi atau situs web tertentu. Anda bisa menggunakan teknik ini untuk menemukan halaman atau program yang menawarkan Bug Bounty.

```
inurl: /bug bounty
```
```
inurl: /responsible disclosure
```
```
inurl /bug bounty
inurl : / security
inurl:security.txt
inurl:security "reward"
inurl : /responsible disclosure
inurl : /responsible-disclosure/ reward
inurl : / responsible-disclosure/ swag
inurl : / responsible-disclosure/ bounty
inurl:'/responsible disclosure' hoodie
responsible disclosure swag r=h:com
responsible disclosure hall of fame
inurl:responsible disclosure $50
responsible disclosure europe
responsible disclosure white hat
white hat program
insite:"responsible disclosure" -inurl:nl
intext responsible disclosure
site eu responsible disclosure
site .nl responsible disclosure
site responsible disclosure
responsible disclosure:sites
responsible disclosure r=h:nl
responsible disclosure r=h:uk
responsible disclosure r=h:eu
responsible disclosure bounty r=h:nl
responsible disclosure bounty r=h:uk
responsible disclosure bounty r=h:eu
responsible disclosure swag r=h:nl
responsible disclosure swag r=h:uk
responsible disclosure swag r=h:eu
responsible disclosure reward r=h:nl
responsible disclosure reward r=h:uk
responsible disclosure reward r=h:eu
"powered by bugcrowd" -site:bugcrowd.com
"submit vulnerability report"
"submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone"
site:*.gov.* "responsible disclosure"
intext:"we take security very seriously"
site:responsibledisclosure.com
inurl:'vulnerability-disclosure-policy' reward
intext:Vulnerability Disclosure site:nl
intext:Vulnerability Disclosure site:eu
site:*.*.nl intext:security report reward
site:*.*.nl intext:responsible disclosure reward
"security vulnerability" "report"
inurl"security report"
"responsible disclosure" university
inurl:/responsible-disclosure/ university
buy bitcoins "bug bounty"
inurl:/security ext:txt "contact"
"powered by synack"
intext:responsible disclosure bounty
inurl: private bugbountyprogram
inurl:/.well-known/security ext:txt
inurl:/.well-known/security ext:txt intext:hackerone
inurl:/.well-known/security ext:txt -hackerone -bugcrowd -synack -openbugbounty
inurl:reporting-security-issues
inurl:security-policy.txt ext:txt
site:*.*.* inurl:bug inurl:bounty
site:help.*.* inurl:bounty
site:support.*.* intext:security report reward
intext:security report monetary inurl:security
intext:security report reward inurl:report
site:security.*.* inurl: bounty
site:*.*.de inurl:bug inurl:bounty
site:*.*.uk intext:security report reward
site:*.*.cn intext:security report reward
"vulnerability reporting policy"
"van de melding met een minimum van een" -site:responsibledisclosure.nl
inurl:responsible-disclosure-policy
"If you believe you've found a security vulnerability"
intext:"BugBounty" and intext:"BTC" and intext:"reward"
intext:bounty inurl:/security
inurl:"bug bounty" and intext:"€" and inurl:/security
inurl:"bug bounty" and intext:"$" and inurl:/security
inurl:"bug bounty" and intext:"INR" and inurl:/security
inurl:/security.txt "mailto*" -github.com  -wikipedia.org -portswigger.net -magento
/trust/report-a-vulnerability
site:*.edu intext:security report vulnerability
"cms" bug bounty
"If you find a security issue"  "reward"
"responsible disclosure" intext:"you may be eligible for monetary compensation"
inurl: "responsible disclosure", "bug bounty", "bugbounty"
intext: we offer a bounty
responsible disclosure inurl:in
site:*.br responsible disclosure
site:*.at responsible disclosure
site:*.be responsible disclosure
site:*.au responsible disclosure
site:*/security.txt "bounty"
inurl:bug bounty intext:"rupees"
inurl:bug bounty intext:"₹"
inurl:responsible disclosure intext:"INR"
```
Dengan menggunakan dorking ini, Anda dapat menemukan halaman-halaman yang menginformasikan tentang program Bug Bounty yang dapat diikuti.

---

## Keuntungan Mengikuti Bug Bounty

- **Penghargaan dan Pengakuan**: Anda bisa mendapatkan hadiah, baik berupa uang tunai, merchandise, atau pengakuan atas kontribusi Anda dalam meningkatkan keamanan suatu sistem.
- **Pengembangan Keahlian**: Dengan mengikuti Bug Bounty, Anda dapat mengasah keterampilan dan keahlian dalam menemukan kerentanan keamanan di berbagai sistem.
- **Kontribusi pada Keamanan Dunia Maya**: Anda turut berkontribusi untuk meningkatkan keamanan dan melindungi data penting dari potensi ancaman atau serangan.

Bug Bounty merupakan cara yang efektif dan menarik untuk menguji keterampilan keamanan siber Anda sambil mendapatkan hadiah yang layak.