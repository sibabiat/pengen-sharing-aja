# Gatau saya mau sharing aja
Pengen sharing aja saya mah bener ga pengen yang lain

## Subdomain Enumeration
Subdomain enumeration adalah

#### Enumerasi menggunakan amass (favorit)
Gatau kenapa tapi yang jelas ini favorit saya sih, super ngebut dan walaupun dengan API keys yang kita provide minim dia bisa subdomain or attack surface dengan result yang sangat banyak dan oke. Dan yang paling mantepnya lagi adalah, amass ini ngebut banget. Love OWASP, love amass.

```bash
$ amass enum -d site.com -passive -o scopes.txt
```

| Parameter | Description                       |
| :-------- | :-------------------------------- |
| `amass`      | **Required**. Id of item to fetch |
| `enum`      | **Required**. Id of item to fetch |
| `-d`      | **Required**. Id of item to fetch |
| `site.com`      | **Required**. Id of item to fetch |
| `-passive`      | **Required**. Id of item to fetch |
| `-o`      | **Required**. Id of item to fetch |
| `scopes.txt`      | **Required**. Id of item to fetch |

##### Bahan bacaan
 - [Mempelajari amass](https://github.com/owasp-amass/amass)

#### Enumerasi menggunakan subfinder
```bash
$ subfinder -d site.com >> scopes.txt
```

#### Enumerasi menggunakan assetfinder
```bash
$ assetfinder -subs-only site.com >> scopes.txt
```

#### Enumerasi menggunakan kombinasi ketiganya
```bash
$ RHOSTS=site.com; amass enum -d $RHOSTS -passive -o scopes.txt &&\ 
subfinder -d $RHOSTS >> scopes.txt &&\ 
assetfinder -subs-finder $RHOSTS >> scopes.txt &&\ 
cat scopes.txt | sort -u | tee scopes.txt
```

#### Enumerasi menggunakan assetfinder
```bash
$ assetfinder -subs-only site.com >> scopes.txt
```

#### Enumerasi pada DNS yang tersedia
```bash
$ RHOSTS=site.com; amass enum -d $RHOSTS -passive -o scopes.txt &&\ 
subfinder -d $RHOSTS >> scopes.txt &&\ 
assetfinder -subs-finder $RHOSTS >> scopes.txt &&\ 
cat scopes.txt | dnsx | tee scopes.txt
```
```bash
$ RHOSTS=site.com; amass enum -d $RHOSTS -passive -o scopes.txt &&\ 
subfinder -d $RHOSTS >> scopes.txt &&\
assetfinder -subs-finder $RHOSTS >> scopes.txt &&\
cat scopes.txt | httprobe | grep https | tee scopes.txt
```
