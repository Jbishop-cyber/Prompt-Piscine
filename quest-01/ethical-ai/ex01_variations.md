**Modify your palindrome function to**

Ignore spaces and punctuation.

Be case-insensitive.

Return the position where the string stops being a palindrome (if not one).
    
```py
    def palindrome(string):  
    # Prepare the string
    # We will create a new string that contains only letters and numbers, all lowercase
    # This ensures spaces, punctuation, and capital letters do not affect the check
    clean = ""
    for char in string:
        if char.isalnum(): # Keep only letters and numbers
            clean += char.lower() # Convert to lowercase for uniform comparison
    
    # Determine the length of the cleaned string
    length = len(clean)
    
    # Compare characters from the start and end
    # Only need to go halfway since we are checking mirrored positions
    for i in range(0, length // 2):
        if (clean[i] != clean[length - i - 1]):
            # Not a palindrome if any characters don't match
            return False
    
    # If all character comparisons pass, it is a palindrome
    return True
```

```py
# Test cases
string1 = "racecar"
print(palindrome(string1))  # Expected: True

string2 = "hello"
print(palindrome(string2))  # Expected: False

string3 = "A man a plan a canal Panama"
print(palindrome(string3))  # Expected: True
```

**Reflection on what AI added**

I tried adding a new function that converts the uppercase to lowercase but the spaces was still an issue. So using AI, a function simplified string that contains only letters and numbers was added, and this string ensures spaces, punctuation, and capital letters do not affect the check.
