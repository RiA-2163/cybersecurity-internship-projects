# Password Cracking using John the Ripper

## Objective

This project demonstrates an offline password security audit by generating password hashes from a simulated employee database and recovering weak passwords using John the Ripper.

---

## Tools Used

- Kali Linux
- Python 3
- John the Ripper
- Nano Editor

---

## Technologies

- Python
- MD5 Hashing
- Dictionary Attack

---

## Workflow

Employee List

↓

Weak Password List

↓

Python Hash Generator

↓

MD5 Hash Database

↓

John the Ripper

↓

Recovered Passwords

---

## Steps Performed

### Step 1

Created a simulated employee database.

### Step 2

Created a weak password dictionary.

### Step 3

Developed a Python script to generate MD5 password hashes.

### Step 4

Generated the hashes database.

### Step 5

Performed a dictionary attack using John the Ripper.

### Step 6

Recovered weak passwords successfully.

---

## Commands Used

Generate hashes

```bash
python3 generate_hashes.py
```

Crack hashes

```bash
john --format=Raw-MD5 --wordlist=weak_passwords.txt hashes.txt
```

Display recovered passwords

```bash
john --show --format=Raw-MD5 hashes.txt
```

---

## Skills Learned

- Password Hashing
- MD5
- Password Auditing
- Dictionary Attack
- John the Ripper
- Python Automation

---

## Educational Notice

This project uses a simulated employee database created for educational purposes. No real credentials were used.
