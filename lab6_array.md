# 📘 Array Scripts Overview

This file explains and demonstrates **three core array operations** in **Shell Scripting (Bash)** — using fruits 🍎🍌🍇 instead of numbers for clarity and fun.

---

## 🔹 1. Using `for` Loop  
➡️ **Purpose:** Iterates through each fruit in the array.  
✅ **Best when:** You want to process each item one by one, cleanly and clearly.

### 🧾 Example:
```bash
#!/bin/bash

# Define an array of fruits
fruits=("Apple" "Banana" "Cherry" "Date" "Elderberry")

echo "🍽️ Listing all fruits using a for loop:"
for fruit in "${fruits[@]}"
do
  echo "🍉 $fruit"
done
💡 Tip:
Use "${fruits[@]}" to preserve each element, even if it contains spaces.

```
### 📸Screenshot 1 :For Loop Output


## 🔹 2. Using while Loop + Length

➡️ **Purpose:** Manually iterate using an index and the array’s length.
✅ **Best when:** You need fine control over index-based operations.

🧾 Example:
```bash
#!/bin/bash

# Define an array of fruits
fruits=("Fig" "Grape" "Honeydew" "IndianFig" "Jackfruit")

echo "📦 Displaying fruits using while loop:"
index=0
length=${#fruits[@]}

while [ $index -lt $length ]
do
  echo "🍍 ${fruits[$index]}"
  ((index++))
done
💡 Tip:
"${#fruits[@]}" gives the total number of elements — perfect for bounds checking.
```
### 📸Screenshot 2 :While Loop + Length Output

## 🔹 3. Array Slicing

➡️ **Purpose:** Extract specific portions of an array.
✅ **Best when:** You need just part of the data without changing the original.

### 🧾 Example:
```bash

#!/bin/bash

# Define an array of fruits
fruits=("Kiwi" "Lemon" "Mango" "Nectarine" "Orange" "Papaya" "Quince")

echo "🍒 Slicing the fruit array:"
echo "🥝 First three fruits: ${fruits[@]:0:3}"
echo "🍊 Last three fruits: ${fruits[@]: -3}"   # Note the space after :
echo "🍑 Middle fruits (index 2 to 4): ${fruits[@]:2:3}"

💡 Tip:
The format ${array[@]:start:length} makes slicing easy — and yes, negative indexing works with a space: ${array[@]: -3}
```
### 📸Screenshot 3 :Array Slicing Output
              
```

🌟 Bonus Tip: Bash arrays are zero-indexed and support powerful manipulation techniques. Mastering them boosts your scripting efficiency significantly!
```