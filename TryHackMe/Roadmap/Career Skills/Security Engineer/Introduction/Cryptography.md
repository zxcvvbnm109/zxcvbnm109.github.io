###### Task 1

```
Q: You have received the following encrypted message:

“Xjnvw lc sluxjmw jsqm wjpmcqbg jg wqcxqmnvw; xjzjmmjd lc wjpm sluxjmw jsqm bqccqm zqy.” Zlwvzjxj Zpcvcol

You can guess that it is a quote. Who said it?

A: Miyamoto Musashi

E: Paste text into quipqiup
```

###### Task 2

Programs that use asymmetric encryption:
- GNU Privacy Guard (GPG) - implements OpenPGP standard
- OpenSSL Project - maintains the OpenSSL software

```
gpg --symmetric --cipher-algo CIPHER message.txt
gpg --decrypt message.gpg --output original.txt

openssl aes-256-cbc -e -in message.txt -out encrypted_message
openssl aes-256-cbc -d -in encrypted_message -out original_message.txt
```

```
Q: Decrypt the file `quote01` encrypted (using AES256) with the key `s!kR3T55` using `gpg`. What is the third word in the file?

A: waste

E: gpg --decrypt quote01.txt.gpg
```

```
Q: Decrypt the file `quote02` encrypted (using AES256-CBC) with the key `s!kR3T55` using `openssl`. What is the third word in the file?

A: science

E: openssl aes-256-cbc -d -in quote02 -out q02
```

```
Q: Decrypt the file `quote03` encrypted (using CAMELLIA256) with the key `s!kR3T55` using `gpg`. What is the third word in the file?

A: understand

E: gpg --decrypt quote03.txt.gpg
```

