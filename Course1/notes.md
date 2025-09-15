# Python for Everybody – Course 1 Notes

---

## 1. Writing & Running Programs in Python

- Write code in an editor (VS Code, PyCharm, etc.)
- Save with `.py` extension
- Run in terminal:
```bash
cd base_folder/sub_folder
python filename.py
```

**Steps:**

1. Type `cmd` & Enter
2. Navigate to folder with your `.py` file
3. Run the file with `python filename.py`

---

## 2. Variables, Constants & Expressions

- **Variables:** store values
```python
x = 5
```
- **Constants:** fixed values
```python
PI = 3.14159
```
- **Numeric Expressions:**
  - Addition: `+`
  - Subtraction: `-`
  - Multiplication: `*`
  - Power: `**`
  - Division: `/`
  - Remainder (modulus): `%`

> Always use PEMDAS rule for calculations

- *PEMDAS = ( ), ^, × ÷ %, + −*

> Same-level operators → solve left to right  

**Example:** 20 ÷ 5 * 2 = (20 ÷ 5) * 2 = 4 * 2 = 8

- **Comparison Operators:**
```
<   less than
>   greater than
==  equal
!=  not equal
<=  less than or equal
>=  greater than or equal
```

---

## 3. Type Conversion

- `input()` always returns a string. Convert for integers/floats:
```python
x = int(input("Enter a numeric value: "))
y = float(input("Enter a numeric value: "))
```
- Convert between types:
```python
int("10")    # → 10
float("3.5") # → 3.5
str(123)     # → "123"
```

---

## 4. Conditional Statements

```python
if x > 5:
    print("Big")
elif x == 5:
    print("Equal")
else:
    print("Small")
```

---

## 5. Loops

- **While Loop:** can be infinite, runs until condition is false
```python
x = 0
while x < 5:
    print(x)
    x = x + 1
```

- **For Loop:** usually finite, runs over a sequence or range
```python
for i in range(5):
    print(i)
```

---

## 6. Functions

- Reusable blocks of code

**With parameters:**
```python
def greet(name):
    print("Hello", name)
```

**Without parameters:**
```python
def say_hello():
    print("Hello!")
```

---

## 7. Error Handling

- `try/except` prevents program crash
```python
try:
    num = int(input("Enter a denominator: "))
except:
    print("Denominator cannot be 0")
```

---

## 8. Loops with Counting & Summing

**Counting:**
```python
count = 0
for i in [3, 5, 7]:
    count = count + 1
# Or use built-in function: len([3,5,7])
```

**Summing:**
```python
total = 0
for i in [3, 5, 7]:
    total = total + i
# Or use built-in: sum([3,5,7])
```

**Average:**
```python
nums = [3, 5, 7]
average = sum(nums) / len(nums)
```

**Largest:**
```python
largest = None
nums = [3, 5, 7]
for l in nums:
    if largest is None or l > largest:
        largest = l
# Or use built-in: max(nums)
```

**Smallest:**
```python
smallest = None
nums = [3, 5, 7]
for s in nums:
    if smallest is None or s < smallest:
        smallest = s
# Or use built-in: min(nums)
```

---

## 🛑 Common Mistakes in Python

- Variable names should only start with a letter or `_`
- Strings require quotes (`''` or `""`); numbers do not
- Remember type conversion if needed (`int()` / `float()`)
- Don’t forget commas in `print()`
```python
print("Hello", name)  # ✅ correct
print(Hello,name)     # ❌ wrong
```
- Avoid mixing tabs and spaces (use 4 spaces consistently)
- Python is case sensitive (`Name` ≠ `name`)
- Don’t forget `:` after `if`, `for`, `while`, `def`, `class`
```python
if x > 5:  # ✅ correct
if x > 5   # ❌ wrong
```
