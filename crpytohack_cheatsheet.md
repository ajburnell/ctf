# Cryptohack Cheat Sheet

### ASCII
Use `chr()` to turn an ASCII ordinal number to a character, and `ord` to reverse.

Given the integer array:
```python
list = [22, 44, 66, 88]
for i in list:
  # Use end="" so print doesn't put a newline.
  print(chr(i), end="")
```
### Hex

`bytes.fromhex()` can convert from hex to bytes, while `hex()` can be called to get their hex representation.
```python
hexstring = "SomethingInHex"
bytes.fromhex(hexstring)
```

### Base64

```python
import base64
base64.b64encode()
base64.b64decode()
```

### Big Integers & PyCryptodome

Cryptosystems built on numbers but messages are characters so need to be convereted so math operations can be applied. Most common way is to take ordinal bytes, convert to hex and concatenate. This could then be interpreted as a base-16 or base-10 number.

```python
message = 534958739485739485128376837239423049280432973648273649238470123894723
Crypto.Util.number.long_to_bytes(message)

# Reverse with:
Crpyto.Util.number.bytes_to_long()
```

### XOR

Denoted as ⊕ in textbooks or often in challenges/programming as `^`.

XOR'ed value returns 0 if bits are the same, or 1 if different.
`0 ^ 0 = 0`  
`0 ^ 1 = 1`  
`1 ^ 0 = 1`  
`1 ^ 1 = 0`  

`pwntools` has `xor()` function.





