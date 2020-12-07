# test-1
This specification is developed on GitHub with the help of the ECMAScript community. There are a number of ways to contribute to the development of this specification:

GitHub Repository: https://github.com/tc39/ecma262
Issues: All Issues, File a New Issue
Pull Requests: All Pull Requests, Create a New Pull Request
Test Suite: Test262
Editors:
Jordan Harband (@ljharb)
Shu-yu Guo (@_shu)
Michael Ficarra (@smooshMap)
Kevin Gibbons (@bakkoting)
Community:
Discourse: https://es.discourse.group
IRC: #tc39 on freenode
Mailing List Archives: https://esdiscuss.org/
Refer to the colophon for more information on how this document is created.

Description
slice() extracts the text from one string and returns a new string. Changes to the text in one string do not affect the other string.

slice() extracts up to but not including endIndex. str.slice(1, 4) extracts the second character through the fourth character (characters indexed 1, 2, and 3).

As an example, str.slice(2, -1) extracts the third character through the second to last character in the string.


Changes in the project

What else?
Something about Github


beginIndex
The zero-based index at which to begin extraction. If negative, it is treated as str.length + beginIndex. (For example, if beginIndex is -3, it is treated as str.length - 3.) If beginIndex is not a number after Number(beginIndex), it is treated as 0.

If beginIndex is greater than or equal to str.length, an empty string is returned.

endIndex Optional
The zero-based index before which to end extraction. The character at this index will not be included.

If endIndex is omitted or undefined, or greater than str.length, slice() extracts to the end of the string. If negative, it is treated as str.length + endIndex. (For example, if endIndex is -3, it is treated as str.length - 3.) If it is not undefined and not a number after Number(endIndex), an empty string is returned.

If endIndex is specified and startIndex is negative, endIndex should be negative, otherwise an empty string is returned. (For example, slice(-3, 0) returns "".)

If endIndex is specified, and startIndex and endIndex are both positive or negative, endIndex should be greater than startIndex, otherwise an empty string is returned. (For example, slice(-1, -3) or slice(3, 1) returns "".)
