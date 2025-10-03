# Python for Everybody - Course 2 Notes‎

## 1. Strings  

‎-Strings are **sequences of characters**.  
‎-Strings are written inside **single `' '` or double `" "` quotes**.  
‎-Strings are **immutable** → once created, they cannot be changed (only new strings can be made).

‎### Indexing & Length
‎```python
‎text = "Hello World"
‎
‎print(text[0])      # 'H' → first character
‎print(text[-1])     # 'd' → last character
‎print(len(text))    # 11 → total characters
‎```
‎
### Slicing
‎```python
‎s = "university"
‎print(s[0:4])    # "univ"
‎print(s[5:])     # "rsity"
‎print(s[:3])     # "uni"
‎```

‎### Common String Methods
‎```python
‎word = "python"
‎
‎print(word.upper())       # "PYTHON"
‎print(word.lower())       # "python"
‎print(word.startswith("py"))  # True
‎print(word.replace("py", "my"))  # "mython"
‎print("a" in word)        # True
‎```

## 2. Files  

‎‎-Python can read and write text files using the `open()` function.  
‎-Always **close** the file after use (or use `with`).  
‎
### Reading a File
‎```python
‎# Open a file in read mode
‎f = open("sample.txt", "r")
‎or 
‎with open("sample.txt","r") as f:
‎
‎# Read the whole file
‎print(f.read())
‎
‎# Read line by line
‎for line in f:
‎    print(line.strip())
‎
‎f.close()
‎```

‎### Writing a File
‎```python
‎# Open in write mode (overwrites file)
‎f = open("output.txt", "w")
‎f.write("Hello, file!\n")
‎f.close()
‎``` 

‎## 3. Lists

‎-Lists store **multiple values in order**.  
‎-Lists are **mutable** (you can change them).  
‎-Written with square brackets `[ ]`.

‎### Creating & Accessing
‎```python
‎numbers = [10, 20, 30, 40]
‎
‎print(numbers[0])   # 10
‎print(numbers[-1])  # 40
‎print(len(numbers)) # 4
‎```

‎### List Operations
‎```python
‎nums = [1, 2, 3]
‎
‎nums.append(4)       # [1, 2, 3, 4]
‎nums.insert(1, 10)   # [1, 10, 2, 3, 4]
‎nums.remove(10)      # [1, 2, 3, 4]
‎```

## 4. Dictionaries 

‎‎-Dictionaries store data as **key-value pairs**.  
‎-Keys must be **unique & immutable** (strings, numbers, tuples).  
‎-Written with curly braces `{ }`.
‎-Format is **{key:value}** & **dict [key] = value**
‎
### Creating & Accessing
‎```python
‎student = {
‎    "name": "Alice",
‎    "age": 20,
‎    "grade": "A"
‎}
‎‎print(student["name"])   # Alice
‎print(student.get("age")) # 20
‎```

### Updating Dictionary
‎```python
‎student["age"] = 21
‎student["city"] = "New York"
‎print(student)
‎```

### Looping
‎```python
‎for key, value in student.items():
‎    print(key, ":", value)
‎```

## 5. Tuples 

‎‎-Tuples are like lists but **immutable**.  
‎-Written with parentheses `( )`.  
‎
### Creating & Accessing
‎```python
‎point = (10, 20, 30)
‎
‎print(point[0])   # 10
‎print(point[-1])  # 30
‎```

## Summary  
‎
‎-**Strings** → immutable text data.  
‎-**Files** → read/write persistent data.  
‎-**Lists** → key/value,orderedmutablele collections.  
‎-**Dictionaries** → key-value pairs.  
‎-**Tuples** → ordered, immutable collections-
