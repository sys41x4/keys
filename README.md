# GPG PUB KEYS for SIGNED PKG Verification
---

```
GPG PUB KEYS HOLDER : Arijit Bhowmick [sys41x4]
```

GPG-CHECKSUM : [CHECKSUM](CHECKSUM)


---

These keys can be used to verify the signed packages from the mentioned author <br>
GPG Keys can directly be fetched from this repository using the below command
<br>
```
Format:

curl https://sys41x4.github.io/keys/<KEY-ID>/ | grep -o '[^[:space:]]*\.gpg' | cut -d'>' -f 2 | xargs -I {} wget https://sys41x4.github.io/keys/<KEY-ID>/{} -O <LOCAL_DIR_PATH>/{}


[ Strictly For Directly saving the GPG KEY to ADMIN Restrictive Directory Path ]

curl https://sys41x4.github.io/keys/<KEY-ID>/ | grep -o '[^[:space:]]*\.gpg' | cut -d'>' -f 2 | xargs -I {} sudo wget https://sys41x4.github.io/keys/<KEY-ID>/{} -O <LOCAL_DIR_PATH>/{}
```
<br>
Example For Directly saving GPG Key having `KEY-ID : CDE57FED896A2F94` to `DIR_PATH : /etc/apt/trusted.gpg.d/`

```
curl https://sys41x4.github.io/keys/CDE57FED896A2F94/ | grep -o '[^[:space:]]*\.gpg' | cut -d'>' -f 2 | xargs -I {} sudo wget https://sys41x4.github.io/keys/CDE57FED896A2F94/{} -O /etc/apt/trusted.gpg.d/{}
```

---

CHECKSUM of GPG Keys of the branch can be generated as

```
find . -type f -name "*.gpg" -exec sh -c 'echo "MD5: $(md5sum "$1")"; echo "SHA1: $(sha1sum "$1")"; echo "SHA256: $(sha256sum "$1")"' sh {} \; > CHECKSUM
```
