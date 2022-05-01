# Lab Report 2

## Code Change 1

![NoLinksCode](images/Week4/NoLinksCode.jpg)

[The test file for a failure-inducing input that prompted me to make that change
](https://github.com/Charlychee/markdown-parser/blob/main/test-file3.md)

![NoLinksError](images/Week4/NoLinksError.jpg)

> The symptom that we see here is that there is a `StringIndexOutOfBoundsException`. This is due to the fact that the `indexOf` method returns -1 since there is no link to find in the markdown file. The -1 is used to index the next string, which causes an exception to be thrown.

## Code Change 2

![ContentAfterEndCode](images/Week4/ContentAfterEndCode.jpg)

[The test file for a failure-inducing input that prompted me to make that change
](https://github.com/Charlychee/markdown-parser/blob/main/test-file4.md)

![ContentAfterEndError](images/Week4/ContentAfterEndError.jpg)

> The symptom is that there is no output and the program never ends. The bug is that the while loop never exits, resulting in the symptom observed. This is because the while loop exit condition is never reached due to the fact that the index of the link is not at the end of the input file.

## Code Change 3

![NestedBracketsCode](images/Week4/NestedBracketsCode.jpg)

[The test file for a failure-inducing input that prompted me to make that change
](https://github.com/Charlychee/markdown-parser/blob/main/test-file2.md)

![NestedBracketsError](images/Week4/NestedBracketsError.jpg)

> The symptom is that the entire link is not outputted, and instead only a portion of the link, up until the nested parentheses, is outputted.. The bug is that the while loop never exits, resulting in the symptom observed. This is because the while loop exit condition is never reached due to the fact that the search finds the second to last parentheses as the last character, rather than the actual last parentheses as the last character.
