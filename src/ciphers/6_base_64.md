# 🤖 Base 64 🤖

Base 64 is an encoding scheme for text and binary data. 
We write out our input as binary data, group it into groups of six bits, and then use a Base 64 alphabet to write it down.

If you're curious, here's the whole alphabet!
```
ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/
```

If the input does not cleanly fit into 6 bit groups, we add `=` at the end for padding.

## Why?

Allows us to encode arbitrary binary data as printable text! Very useful for e.g. sending it over the web.

## Example

```
I <3 Compclub!
```
is
```
01001001 00100000 00111100 00110011 00100000 01000011 01101111 01101101 01110000 01100011 01101100 01110101 01100010 00100001
```
in Binary.

Group into groups of six:
```
010010 010010 000000 111100 001100 110010 000001 000011 011011 110110 110101 110000 011000 110110 110001 110101 011000 100010 0001
```
Convert to Base 64 Alphabet:
```
SSA8MyBDb21wY2x1YiE=
```
