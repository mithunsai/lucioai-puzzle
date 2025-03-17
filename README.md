# lucioai-puzzle

# Decrypting a Fernet-Encrypted String

## Step 1: Base64 Decoding

An **online Base64 decoder** was used to decode the given encoded string. 

*VGhpcyB3YXMgZWFzeS4gTGV0J3MgdHJ5IHNvbWV0aGluZyBoYXJkZXIuIE1yIENyeX
B0byBuZWVkcyB5b3VyIGhlbHAgdG8gdW5kZXJzdGFuZCB0aGlzIHRleHQ6IAoKZ0FBQU
FBQm5ibjhvTzBPN09tcXRxdWZjcDZOazVsNDQ4NEtwZ0xzNmFpaThLejJmX24yWFA2W
mIzSUpmbXhPTzdpVHVfQXFZZWRPeTl3cEFLVk9ZNWttN3NxREpoVGR6dTJaQmxkbDg
tdnd1bnJ2SGFMNjAyX1pPc09OLWtvRmJvOVNVZW13NHNjQm1JTkJFU1p0akJCUHljW
UliNnV1WjZhV1E3MHl3bnNxWXJuOFp5cjVGYzJ1bVJrYUVnaFU1SlM4ZUt4VTlGQThLU
1ptTWVxd2VDbFlNNG1tNEN5TzNuems3UEh3aHQ4dXNZU3BLbU5CclFjY1dDenZHQ3h
GbDRUX1EwdFRKTWsxSklRX1dXaEpDY3hRTWVLTWxCSlYwb0UwQW9NZDRBd19vN0Iz
UWpURVFvckk9CgpIZSB0ZWxscyB5b3UgJ1NvbWV0aW1lcywgbWFjaGluZXMgaGF2ZS
BuYW1lcyB0aGF0IGh1bWFucyBjYW4ndCByZWFkIHNvIHlvdSBuZWVkIGEgYm9vayB0by
Bsb29rIHVwIHRoZWlyIG5hbWVzLiBDaGVjayB0aGUgcHViJ3MgcmVjb3JkcyBpbiB0aGU
gYm9vayBhbmQgeW91J2xsIGZpbmQgc29tZXRoaW5nIHRoYXQgbWlnaHQgYmUgdXNl
ZnVsLic=”

The decoded result was:

```
This was easy. Let's try something harder. Mr Crypto needs your help to understand this text:

gAAAAABnbn8oO0O7Omqtqufcp6Nk5l4484KpgLs6aii8Kz2f_n2XP6Zb3IJfmxOO7iTu_AqYedOy9wpAKVOY5km7sqDJhTdzu2ZBldl8-vwunrvHaL602_ZOsON-koFbo9SUemw4scBmINBESZtjBBPycYIb6uuZ6aWQ70ywnsqYrn8Zyr5Fc2umRkaEghU5JS8eKxU9FA8KSZmMeqweClYM4mm4CyO3nzk7PHwht8usYSpKmNBrQccWCzvGCxFl4T_Q0tTJMk1JIQ_WWhJCcxQMeKMlBJV0oE0AoMd4Aw_o7B3QjTEQorI=
```

Along with the following clue:

> "Sometimes, machines have names that humans can't read so you need a book to look up their names. Check the pub's records in the book and you'll find something that might be useful."

## Step 2: Identifying the Key

Interpreting the clue, it was deduced that it referred to **DNS records**. The DNS records of `www.lucioai.com` were examined using **Google Admin Toolbox**.

From the DNS records, the **Fernet key** required to decrypt the encrypted string was obtained.

The image is uploaded in the repo as well (fernet-key.png)

## Step 3: Decrypting the Fernet String

Using the retrieved Fernet key, the encrypted string was successfully decrypted. The final result was:

```
Congratulations! Please fill this form and we'll schedule your interview: https://in.bigin.online/org60035757117/forms/lucio-technical-hiring.

The passkey is TECHGENIUS.
```


