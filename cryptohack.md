
CRYPTOHACK
==========

INDRODUCTION
============

GREAT SNAKES
------------
* run the script and get the flag

NETWORK-ATTACKS
--------------
* connect to the netcat and sent the JASON OBJECT
"{"buy":"flag"}"

ENCODING
========

ASCII
-----
* python solution
```
	a=[99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]
	for i in a:
		print(chr(i))
```


HEX
---
*python solution
```
	a='63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d'
	print(bytes.fromhex(a))

```
BASE64
------
*python solution
```
	from base64 import b64
	a="72bca9b68fc16ac7beeb8f849dca1d8a783e8acf9679bf9269f7bf"
	a=bytes.fromhex(a)
	print(b64encode(a))
```
BYTES AND BIG INTEGERS
----------------------


XOR
===

XOR-STARTER
-----------
```
	a="label"
	for i in label:
		print(i^13)

```
XOR PROPERTIES
--------------
```
	import codecs
	KEY1 = int('a6c8b6733c9b22de7bc0253266a3867df55acde8635e19c73313',16)
	KEY21=int(' 37dcb292030faa90d07eec17e3b1c6d8daf94c35d4c9191a5e1e',16)
	KEY23 = int('c1545756687e7573db23aa1c3452a098b71a7fbf0fddddde5fc1',16)
	kFLAG =int(' 04ee9855208a2cd59091d04767ae47963170d1660df7f56f5faf,16) 
	k123=KEY1^KEY23
	flag=KFLAG^K123
	flag=codecs.decode(flag,'hex_decode')
	
```
FAVOURATIE BYTES
----------------

```
	form pwn import xor
	a=bytes.fromhex(73626960647f6b206821204f21254f7d694f7624662065622127234f726927756d)
	for i in range(256):
		print(xor(a,i))
		
```
