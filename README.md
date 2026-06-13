Length of Last Word

Problem

Given a string s consisting of words and spaces, return the length of the last word in the string.

A word is a sequence of non-space characters.

Approach

Start from the end of the string.

Skip any trailing spaces.

Count characters until a space is encountered.

Return the count as the length of the last word.

Complexity

Time Complexity: O(n)

Space Complexity: O(1)

Key Insight

By traversing the string from right to left, we can directly find the last word without using extra space or splitting the string.

Example

Input:

s = "Hello World"

Output:

5

Input:

s = "   fly me   to   the moon  "

Output:

4

Code

def lengthOfLastWord(s):

    i = len(s) - 1

    while i >= 0 and s[i] == ' ':
        i -= 1

    length = 0

    while i >= 0 and s[i] != ' ':
        length += 1
        i -= 1

    return length
  
