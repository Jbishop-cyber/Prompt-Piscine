**Write pseudocode for a function that checks if a string is a palindrome**

*Step 1: Pseudocode*

A string is a palindrome if it remains the same on reading from both ends

A string is not a palindrome when it does not read the same forwards and backwards

We determine whether the string is a palindrome by reversing the string and comparing it

If at any point the characters do not match, then the string is not a palindrome.

If all characters match, the string is a palindrome

**Implement your solution in Python**

*Step 2: Python Implementation*

```py
def palindrome(string):
    
    # Get the length of the string so we know how far to compare
    length = len(string)
    
    # Loop from the start to the middle of the string
    for i in range(0, length // 2):
        
        # Compare characters from the front and back
        if string[i] != string[length - i - 1]:
            
            return False  # Not a palindrome if any characters don't match

    # If all character comparisons pass, it is a palindrome
    return True
```

**Test with examples like "racecar", "hello", and "A man a plan a canal Panama**

*Step 3: Test cases*

```py
string1 = "racecar"
print(palindrome(string1))  # Expected: True

string2 = "hello"
print(palindrome(string2))  # Expected: False

string3 = "A man a plan a canal Panama"
print(palindrome(string3))  # Expected: False (for now)
```

**Add comments explaining your reasoning.**

*Step 4: Comments explaining my reasoning*

The length function determines the length so we know how many characters we need to compare
The for Loop runs from the start of the string to the middle and this only need to go halfway because we compare the start and end simultaneously
Then we compare character at position i with the character at the mirrored position from the end, if they are different, the string cannot be a palindrome, so the code should stop immediately when a mismatch is found. But if the loop completes without finding a mismatch, then all characters match; therefore, the string is a palindrome. For example "racecar" reads the same forward and backward, so we expect it to print true, but, "hello" doesn't so we expect it to print false. Although, "A man a plan a canal Panama" reads the same forward and backward, it reads false because it has spaces and capital letters and our current function is not designed to handled spaces and capital letters.

*Step 5: Reflection*

1. What did you learn from solving it before asking AI?
    Before using AI, I was able to solve the palindrome problem myself by writing the pseudocode first, this made me have a proper understanding of the task.
2. How is your understanding different now?
   After solving the palindrome problem, I see how spaces, punctuations and capitalization affects the results.
3. Could you now write similar functions (e.g., reverse a string) without help?
   Using the same code I used for my palindrome program, yes I can.
