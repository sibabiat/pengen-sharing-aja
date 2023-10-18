# Information Gathering
1. Subdomain Enumeration
2. Credential Harvesting
3. Mobile Apps Analysis


### Subdomain Enumeration
#### Enumerasi menggunakan amass (favorit)
Gatau kenapa tapi yang jelas ini favorit saya sih, super ngebut dan walaupun dengan API keys yang kita provide minim dia bisa subdomain or attack surface dengan result yang sangat banyak dan oke. Dan yang paling mantepnya lagi adalah, amass ini ngebut banget. Love OWASP, love amass.

```bash
$ amass enum -d site.com -passive -o scopes.txt
```


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
### Credential Harvesting
#### intelx.io
Sebenernya banyak banget yang jual-jual credential orang, tapi ada portal yang memudahkan kita sebenernya dan punya fitur free juga, yaitu intelx.io. Tinggal masukin aja email target, nanti juga akan berhasil login - kalo hoki.

