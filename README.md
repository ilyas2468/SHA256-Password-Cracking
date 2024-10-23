# SHA256-Password-Cracking
Created a tool to crack SHA256 hashed passwords using a dictionary attack. This project highlights hash vulnerability awareness and cracking techniques.
# SHA256 Password Cracking Script

This Python script attempts to crack a given SHA256 hash using a brute-force approach. The script utilizes the popular `rockyou.txt` wordlist and hashes each word in the list using the SHA256 algorithm, comparing it against the target hash provided via command line argument. It also features a progress bar to display live updates during the password cracking process.

## Features
- **Argument validation**: Ensures the correct input format (i.e., a SHA256 hash) is provided.
- **Wordlist-based brute force**: Uses the `rockyou.txt` wordlist to check potential passwords.
- **Progress tracking**: Displays a live progress bar indicating the number of password attempts made.
- **Attempts counter**: Tracks how many passwords have been hashed and compared.
- **Success detection**: Stops execution once the correct password is found, displaying the password and the number of attempts.

## Screenshots

### 1. Initial Code Setup
This shows the initial code setup, where the script imports necessary libraries (`pwn` and `sys`), validates arguments, and prepares for password cracking.
![Initial Code Setup](https://i.imgur.com/R6qjewB.png)

- Argument validation to ensure correct input.
- Uses `rockyou.txt` as the password wordlist.
- Tracks the number of password hashes attempted.

### 2. Running the Script - Password Cracking Attempt
This demonstrates the script running in a Kali Linux environment. The user provides a target SHA256 hash, and the script begins iterating through the `rockyou.txt` wordlist, providing live feedback for each password attempt.
![Running the Script](https://i.imgur.com/DgACwXW.png )

- Input SHA256 hash: `114a6a60b...`
- Iterates through the wordlist with live status updates via a progress bar.
- Hashes each word using SHA256 and compares it to the target hash.

### 3. Success - Password Found
This shows the script successfully cracking the SHA256 hash after 16,470 attempts. The correct password is displayed, and the script stops execution once the match is found.
![Password Found](https://i.imgur.com/CBGaYQM.png )

- Successful password crack after 16,470 attempts.
- The target hash matches the generated hash for the cracked password.
- Displays the number of attempts and the cracked password.

## Usage

1. Clone the repository and navigate to the script directory.
2. Ensure you have the `rockyou.txt` wordlist file.
3. Run the script with the following command:

   ```bash
   python sha256_cracker.py <SHA256_hash>
