# 🔢 Palindrome Numbers Explained with Shell Scripting 🐚

## What is a Palindrome Number?

A **palindrome number** is a number that reads the **same forwards and backwards**!  
It's like a mirror number!

### Examples:  
- `121` ✅  
- `12321` ✅  
- `45654` ✅  
- `123` ❌  
- `10` ❌  

---

## How to Check Palindrome Numbers in Shell Script? 🐚

We can write a **simple Bash script** to check if a number is a palindrome using string manipulation.

---

## Bash Script Example 🖥️

```bash

#!/bin/bash
# palindrome_num.sh
# Usage: ./palindrome_num.sh 1221

if [ $# -ne 1 ]; then
  echo "Usage: $0 <non-negative-integer>"
  exit 1
fi
n="$1"
if ! [[ $n =~ ^[0-9]+$ ]]; then
  echo "Must be a non-negative integer."
  exit 1
fi

orig="$n"
rev=0
while [ "$n" -gt 0 ]; do
  rev=$(( rev * 10 + (n % 10) ))
  n=$(( n / 10 ))
done

[ "$orig" -eq "$rev" ] && echo "$orig is a palindrome." || echo "$orig is NOT a palindrome."

```

**How It Works 🔍**

- Input: User enters a number. 📝

- Reverse: We use the rev command to reverse the string representation of the number. 🔄

- Compare: Check if original and reversed strings match. 🤝
