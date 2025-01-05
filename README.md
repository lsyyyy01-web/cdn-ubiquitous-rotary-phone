# cdn-ubiquitous-rotary-phone
CDN Services. Only use load-balance, not fastly,g-core,bunny or cloudflare !

Get github raw file like:
```
//raw.githubusercontent.com/lsyyyy01-web/cdn-ubiquitous-rotary-phone/refs/heads/main/README.md
```
Change "raw.githubusercontent.com" into "load-balance-ghcdn.755554.xyz"

How it works?
```
User -> laod-balance
             |
       Cloudflare DNS
             |
      Cloudflare Worker ------------------ \
        /                                        \
     User:CN                                   User:Other
    Repo User=lsyyyy11 or lsyyyy01-web             |
     |                        \                    |- to Origin (Github raw)
     301 -> G-Core CDN     301 -> Cloudflare
```
