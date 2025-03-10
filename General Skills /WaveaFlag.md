## Wave a Flag - picoCTF

### Challenge Description
We are given an executable file and need to determine how to extract the flag from it.

### Solution
1. **Download the given file:**
   We first download the provided file and check its properties.

   This command reveals that `warm` is an executable file.

   If the file does not have execute permissions, we need to grant them.

2. **Grant execution permissions:**
   ```bash
   chmod +x warm
   ```
   This makes the file executable.

3. **Run the executable:**
   ```bash
   ./warm
   ```
   The output is:
   ```
   Hello user! Pass me a -h to learn what I can do!
   ```

4. **Check available options:**
   ```bash
   ./warm -h
   ```
   This command provides the flag as output:
   ```
   Flag: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
   ```

### Flag
```
picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
```
