# picoCTF - Web Exploitation - Endianness (Easy)

## Description
In this CTF, we need to understand big-endian and little-endian conversions to find the correct answer.

## Solution Steps

1. **Starting the Machine**
   - First, start the given machine.
   - Enter the following command in the terminal:
     ```bash
     nc titan.picoctf.net 49304
     ```
   - Running the command, we see the following message:
     
     Welcome to the Endian CTF! You need to find both the little-endian and big-endian representations of a given word. If you get both correct, you will receive the flag.
     
   - Then, we are given a random word. For example: `uqszx`

2. **Using CyberChef**
   - Enter the given word into [CyberChef](https://gchq.github.io/CyberChef/).
   - Apply the "Reverse" and "To Hex" operations sequentially to obtain the little-endian representation.
   - Then, disable the "Reverse" operation to get the big-endian representation.

3. **Entering the Results and Getting the Flag**
   - Enter the little-endian and big-endian values into the terminal accordingly.
   - Once the correct answers are entered, we receive the flag.

Flag:
```
picoCTF{3ndi4n_sw4p_su33ess_02999450}
```

---

## Note
Computers store numbers using two different methods: **big-endian** and **little-endian**:

- **Big Endian:** The most significant byte is stored first.
- **Little Endian:** The least significant byte is stored first.

### Example
Suppose we have the number **1234**. In **hexadecimal**, it is written as:
```
1234 → 0x12 34
```
If stored in little-endian format:
```
0x34 12 (bytes are reversed)
```

Operations performed in CyberChef:
1. **"To Hex"** converts the word into a hexadecimal representation.
2. **"Reverse"** swaps the byte order, demonstrating the difference between little-endian and big-endian formats.

This method helps us understand how data is stored in computers.
