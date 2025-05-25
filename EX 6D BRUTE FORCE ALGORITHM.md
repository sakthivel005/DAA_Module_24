# EX 6D BRUTE FORCE ALGORITHM
## DATE:
## AIM:
To write a python program using brute force method of searching for the given substring in the main string.

## Algorithm

1. Read the main string (string) and the substring (sub) from the user.

2. Determine the lengths of both strings using len().

3. Iterate through the main string from index 0 to len(string) - len(sub) to check all possible starting positions.

4. Compare each character of the substring with the corresponding part of the main string using a nested loop.

5. Print "Found at index i" if a complete match is found at that starting position.


## Program:

```
To implement the program using brute force method of searching for the given substring in the main string.

Developed by: SAKTHIVEL R
Register Number: 212222100044
```

```py
def match(string, sub):
    l = len(string)
    ls = len(sub)
    for i in range(l - ls + 1):
        match_found = True
        for j in range(ls):
            if string[i + j] != sub[j]:
                match_found = False
                break
        if match_found:
            print(f"Found at index {i}")

str1 = input()
str2 = input()
match(str1, str2)

```

## Output:

![24d](https://github.com/user-attachments/assets/9c7c595b-f8c9-41cf-9e24-e84e75336b94)


## Result:

Thus the above program was executed successfully for searching the substring at respective index.
