
CRYPTOPALS-SET-1
================

CONVERT HEX TO BASE64
---------------------

```
	import base64
	a=bytes.fromhex('49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d')
	print(base64.b64encode(a))


```


FIXED XOR
---------
```
	from pwn import xor
	a=bytes.fromhex('1c0111001f010100061a024b53535009181c')
	b=bytes.fromhex('686974207468652062756c6c277320657965')
	c=bytes.hex(xor(a,b))

```
single-byte xor cipher
-----------------------
```
	from pwn import xor
	a=bytes.fromhex('1b37373331363f78151b7f2b783431333d78397828372d363c78373e783a393b3736')
	for i in range(256):
		print(xor(a,i))

```
Cooking MC's like a pound of bacon"
