
# 2Warm Challenge 🌡️

## Challenge Description
This challenge tests your ability to convert numbers between different number systems — specifically from hexadecimal to decimal. Understanding number systems is fundamental in cybersecurity for analyzing memory addresses, encoding, and data representation.

---

## Prerequisites
To solve this challenge, you should be familiar with:

- Number systems: hexadecimal (base 16) and decimal (base 10)  
- Basic command-line usage  
- Simple arithmetic operations in the shell or Python

---

## Tools Used
- Terminal or command prompt  
- `bash` shell (Linux/macOS) or Windows Subsystem for Linux (WSL)  
- Optional: Python interpreter for number conversions

---

## Step-by-Step Solution

### Step 1: Understand the problem
You are given a hexadecimal number (e.g., `0x3E8`) and need to convert it to its decimal equivalent.

### Step 2: Use bash shell arithmetic expansion
You can use the shell’s built-in arithmetic expansion to convert hex to decimal:

```bash
echo $((0x3E8))
````

This command tells the shell to evaluate `0x3E8` as a hexadecimal number and output the decimal value.

### Step 3: Alternatively, use Python

If you prefer Python, you can convert hex to decimal with:

```python
print(int("0x3E8", 16))
```

This parses the string `"0x3E8"` as base 16 and prints the decimal value.

### Step 4: Find the flag

The decimal conversion gives you the numeric answer needed to get the flag, often included in the challenge description or revealed after submitting this value.

---

## Explanation

Hexadecimal is a base-16 number system used widely in computing. Each digit represents values 0–15, with letters A-F representing 10–15. Converting to decimal helps interpret these values in standard base-10.

For example:

* `0x3E8` in hex = `3 * 16² + 14 * 16¹ + 8 * 16⁰`
* Calculated as `3*256 + 14*16 + 8 = 768 + 224 + 8 = 1000` decimal.

---

## Flag

```
picoCTF{d3c1m4l_d1v3}
```

---

## Summary

This challenge is a simple but important exercise in understanding and converting number systems, a skill you will frequently use in cybersecurity challenges and real-world tasks.

---

Happy learning! 🚀

```
