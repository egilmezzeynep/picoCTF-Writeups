
#  picoCTF - General Skills: Super SSH (Easy)

##  Description  
This CTF challenge is designed to teach how to establish an SSH connection. If your device doesn’t have a terminal, you can use the [web shell](https://webshell.picoctf.org).  

##  Solution Steps:  
1. I opened the terminal and connected using the given SSH details:  
   ```bash
   ssh ctf-player@titan.picoctf.net -p 53615

    Since this was my first connection, I typed "yes" to confirm.
    I entered the provided password and successfully logged into the server.
    I navigated through the terminal and found the flag:
 ```
picoCTF{s3cur3_c0nn3ct10n_5d09a462}
 ```
