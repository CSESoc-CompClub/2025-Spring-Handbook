# 2.3: Encoding with Cyberchef

After decoding and modifying our save file, we will need to encode the save file before the game we were playing can use it.

For example, if a game's save file was originally encoded in base64, the game will only accept new saves that use base64.

In cyberchef, this means we will need to encode our modified save file using the *opposite* recipe of how we decoded it.

We can do this like:

1. For every operation in our recipe, find the opposite operation using the search feature, and replace it using the opposite operation.

> Some common examples may be:
> - *From Base64* becomes *To Base64*
> - *Zlib inflate* becomes *Zlib deflate*
> - *Unzip* becomes *Zip*

2. Then reverse the order of the operations - if your recipe was:

> 1. *From Base64*
> 2. *Zlib inflate*

After reversing each operation and their order, we should have the recipe

> 1. *Zlib deflate*
> 2. *To Base64*

The encoded save file should now be in the "Output" section, ready for use!