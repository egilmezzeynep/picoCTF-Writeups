# picoCTF - General Skills: Endianness (Easy)

##  Description  
This CTF challenge is designed to help us understand the concept of **endianness**, which refers to how computers store data.

##  Solution Steps  

1. Opened the terminal and ran the given **netcat** command:  
   ```bash
   nc titan.picoctf.net 59809
   ```


After executing the command, I was given a word and asked to find both its little-endian and big-endian representations.

Example word: uqszx (Note: The word may be different for each attempt!)

Used CyberChef to convert the word into hexadecimal format:

Applied the "To Hex" operation.

Enabled the "Reverse" operation to get the little-endian format.
    
Disabled the "Reverse" operation to get the big-endian format.
    
Submitted both formats in the terminal and retrieved the flag!

```
picoCTF{3ndi4n_sw4p_su33ess_02999450}
```


# What is Endianness?

Computers store numbers in two different ways: big-endian and little-endian.

    Big-Endian: The most significant byte (biggest part) is stored first.
    Little-Endian: The least significant byte (smallest part) is stored first.

 Example:

Suppose we have the number 1234. In hexadecimal (base 16), it would be:

1234 → 0x12 34

Little-endian representation would be:

0x34 12  (bytes are reversed)

 Using CyberChef:

Steps performed in CyberChef:

    Applied the "To Hex" operation to convert the word into hexadecimal.
    Used the "Reverse" operation to switch byte order, demonstrating the difference between little-endian and big-endian formats.

In summary: CyberChef helps visualize how data is stored in memory by reversing byte order!
