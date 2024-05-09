# 🎯 subdomain-enumeration

```
$ amass enum -brute -passive -d target.com | httpx -silent -status-code | tee domain.txt
$ cat domain.txt | grep 200 | cut -d "[" -f1 > urls.txt
$ gf xss domain.txt | grep -Eo 'https?://[^\"]+' > domain.txt
```

#### Track new subdomains:

```bash
gungnir -r domain.txt | anew subs-com.txt | notify -id asset
```
