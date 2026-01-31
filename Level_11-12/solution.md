# Bandit Level 11 → Level 12

## 🎯 Level Goal

The password for the next level is stored in the file `data.txt` and is encoded using **ROT13**.

ROT13 is a simple letter substitution cipher that replaces each letter with the letter 13 positions after it in the alphabet.

---

## 🔑 Solution Steps

### Step 1: View the File Content

Check what’s inside the file:

```bash
cat data.txt
```
You will see text that looks readable but doesn’t make sense — it is ROT13 encoded.

---

### Step 2: Decode Using tr Command
Use the tr command to convert ROT13 back to normal text:

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
This command shifts each letter back by 13 positions and prints the decoded password.

---

### Step 3: Copy the Password
Copy the decoded output shown in the terminal. This is the password for the next level.

---

### Step 4: Login to the Next Level
Use the password to log in as bandit12:
```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
```
Paste the password when prompted.

---

### 🧠 What You Learn from This Level
- What ROT13 encoding is

- How character substitution works

- Using the tr command for text transformation

- Piping commands in Linux (|)

---

### Output

![Step 1](screenshots/step_1.png)

![Step 2](screenshots/step_2.png)