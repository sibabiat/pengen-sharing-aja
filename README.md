# laughing-chainsaw
Awesome one line for bug bounty and other things.

## Subdomain Enumeration
Subdomain enumeration adalah

#### Enumerasi menggunakan amass (favorit)
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
 - [Getting started with amass](https://github.com/owasp-amass/amass)

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
