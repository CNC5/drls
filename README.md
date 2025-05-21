# Intro
A minimalistic V2 Docker Registry client for local management

**D**ocker **R**egistry **L**i**S**t
# Demo
```
 ❯❯❯ drls set-registry registry.example.com
Registry set to: registry.example.com
```
```
 ❯❯❯ drls list
Fetching catalog from registry.example.com...

library/mongo/
  4.4.0 -> sha256:ebd31eaac273a9544a33387aa859b0a8676565340a40fc824fa7bda686f462f1
library/python/
  3.11 -> sha256:6c19e87e80b457906d403e02f4a20244526774093b58a9a891f8b1aefd97621e
  3.12 -> sha256:cc0c258bf1a996da799103ac15740b5c07b956efead93264a246c13231728cb3
app/core/
  latest -> sha256:d129ec045aac9c436c330618aa7514242e76dabe347bc05d1373a5c70055df9c
app/crawler/
  latest -> sha256:86d4c69499f6659b6c0d721075a7844f355aa00a422509539e0882b39246dd63
```
```
 ❯❯❯ drls delete library/python 3.11
Deleted library/python:3.11 (digest: sha256:6c19e87e80b457906d403e02f4a20244526774093b58a9a891f8b1aefd97621e)
```
# Setup on linux
Copy drls to your preferred bin (`/bin`:`/usr/bin`...)
```
cp drls /usr/bin/drls
```

Create config directory
```
mkdir -p /etc/drls
chown root:docker /etc/drls/
chmod 770 /etc/drls/
```
