# laughing-chainsaw
Awesome one line for bug bounty and other things.

SUBDOMAIN ENUMERATION
RHOSTS=site.com; amass enum -d $RHOSTS -passive -o scopes.txt &&\ 
subfinder -d $RHOSTS >> scopes.txt &&\ 
assetfinder -subs-finder $RHOSTS >> scopes.txt &&\ 
cat scopes.txt | dnsx | tee scopes.txt

RHOSTS=site.com; amass enum -d $RHOSTS -passive -o scopes.txt &&\ 
subfinder -d $RHOSTS >> scopes.txt &&\
assetfinder -subs-finder $RHOSTS >> scopes.txt &&\
cat scopes.txt | httprobe | grep https | tee scopes.txt
