#  **Description - picoCTF 2024**  

##  Challenge Description  
In this challenge, we need to **establish an SSH connection and solve a number guessing game**.  

---

## 🕵 Solution Steps  

### 1. Extracting the ZIP File  
First, I **unzipped the provided ZIP file** and examined its contents.  

Inside, there was a **Python script that generates a random number and prompts the user to guess it**.  
The script continues until the user **correctly guesses the number**.  

---

###  2. Establishing an SSH Connection  
I used the **Linux terminal to establish an SSH connection**:  

```bash
ssh -p 58039 ctf-player@atlas.picoctf.net
```

After entering "yes" to proceed, I entered the given password:

Password: 
```
84b12bae
```

Once connected, the number guessing game started!
 3. Playing the Guessing Game

The game required guessing a number between 1 and 1000.
I used the binary search approach to efficiently narrow down the possibilities.
 My Guesses:

    500 → Lower (The correct number is smaller)
    250 → Higher (The correct number is larger)
    350 → Lower
    300 → Higher
    325 → Lower
    315 → 🎉 Correct guess!

 Final Flag

After winning the game, I received the following flag:
```
picoCTF{g00d_gu355_2e90d29b}
```

Note: Since the number is randomly generated, your guesses might be different! 
