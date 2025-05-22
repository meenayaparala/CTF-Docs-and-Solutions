
# Obedient Cat Challenge 🐱

## Challenge Description
In this challenge, you are tasked with reading the contents of a file to find the hidden flag. It’s designed to teach you how to use basic command-line tools to access and view files — a fundamental skill in cybersecurity and system exploration.

The challenge folder contains a file with the flag inside. Your job is to find and read that file.

---

## Why This Challenge Matters
In real-world cybersecurity, you often need to explore file systems to locate sensitive information or configuration details. Knowing how to quickly view file contents using command-line tools is essential for:

- Investigating systems  
- Extracting clues or secrets  
- Understanding system states  

This challenge is a safe environment to practice those basics.

---

## Prerequisites
Before attempting this challenge, you should be familiar with:

- Navigating directories in a terminal (`cd`, `ls`)  
- Basic file operations in Unix/Linux  
- How to use the `cat` command to display file content

If you’re new, don’t worry! We’ll walk through the steps.

---

## Tools Required
- Access to a terminal or command line interface (Linux/macOS terminal, Windows WSL, or any Unix shell)  
- Basic Linux commands like `ls`, `cat`

---

## Step-by-Step Solution

### Step 1: Explore the challenge folder
First, open your terminal and navigate to the `Obedient Cat` challenge directory.

Use this command to list the files:

```bash
ls -la
````

This will show all files, including hidden ones, along with permissions and file details.

### Step 2: Identify the file to read

Look for files that seem relevant — usually text files or files with readable content. It might be named something like `flag.txt` or `readme.txt`.

### Step 3: Use `cat` to display file contents

Once you find the target file, use the `cat` command to read its contents:

```bash
cat flag.txt
```

This prints the entire file content to your terminal.

### Step 4: Locate the flag

Inside the file, look for a string formatted like `picoCTF{...}` — this is the flag you need to submit.

---

## Explanation of Commands

* `ls -la`
  Lists all files with detailed info, including hidden files (those starting with a dot).

* `cat filename`
  Displays the content of the file named `filename` directly in the terminal.

---

## Additional Tips

* If the file content is too long, you can use `less filename` to scroll through it page by page.
* If you want to view only the first few lines, use `head filename`.
* For viewing the last lines, use `tail filename`.

---

## Flag

```
picoCTF{c47_15_0b3d13n7}
```

---

## Summary

The Obedient Cat challenge helps build a strong foundation in basic Linux commands to view files — an essential first step in many cybersecurity investigations and CTFs. Mastering these commands will help you explore file systems confidently and find hidden clues quickly.

---

Happy hacking! 🐾
