# leetcode-68-typescript
 Leetcode problem solving, task 48 - Solution by @pstktech

Approach taken to solve the problem - TypeScript
The approach to solving this problem involves iterating through the list of words and building lines of text while considering the maxWidth constraint. We use the variable str to build a line of text and the variable x to keep track of the starting index of words for the current line.

Initialize an empty array res to store the justified lines of text.

Initialize variables str and i to an empty string and 0, respectively. The variable n is used to store the number of words, and x is used to keep track of the starting index of words for the current line.

Iterate through the words:
If adding the next word to the current line str does not exceed the maxWidth, add the word and a space to str, and increment i.

If adding the next word would exceed the maxWidth, adjust the line str by evenly distributing the extra spaces between words. Add the justified line str to the res array. Reset str and set x to i, and continue the iteration.

After the iteration, if str is not empty, it means there are words left for the last line. Add extra spaces to make the line have exactly maxWidth characters, and then add it to the res array.



___________________________
Problem 68 description:

"Given an array of strings words and a width maxWidth, format the text such that each line has exactly maxWidth characters and is fully (left and right) justified.

You should pack your words in a greedy approach; that is, pack as many words as you can in each line. Pad extra spaces ' ' when necessary so that each line has exactly maxWidth characters.

Extra spaces between words should be distributed as evenly as possible. If the number of spaces on a line does not divide evenly between words, the empty slots on the left will be assigned more spaces than the slots on the right.

For the last line of text, it should be left-justified, and no extra space is inserted between words.

Note:

A word is defined as a character sequence consisting of non-space characters only.
Each word's length is guaranteed to be greater than 0 and not exceed maxWidth.
The input array words contains at least one word.
 

Example 1:

Input: words = ["This", "is", "an", "example", "of", "text", "justification."], maxWidth = 16
Output:
[
   "This    is    an",
   "example  of text",
   "justification.  "
]
Example 2:

Input: words = ["What","must","be","acknowledgment","shall","be"], maxWidth = 16
Output:
[
  "What   must   be",
  "acknowledgment  ",
  "shall be        "
]
Explanation: Note that the last line is "shall be    " instead of "shall     be", because the last line must be left-justified instead of fully-justified.
Note that the second line is also left-justified because it contains only one word.
Example 3:

Input: words = ["Science","is","what","we","understand","well","enough","to","explain","to","a","computer.","Art","is","everything","else","we","do"], maxWidth = 20
Output:
[
  "Science  is  what we",
  "understand      well",
  "enough to explain to",
  "a  computer.  Art is",
  "everything  else  we",
  "do                  "
]
 

Constraints:

1 <= words.length <= 300
1 <= words[i].length <= 20
words[i] consists of only English letters and symbols.
1 <= maxWidth <= 100
words[i].length <= maxWidth"

https://leetcode.com/problems/text-justification/description/