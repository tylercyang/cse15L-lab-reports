# Lab Report 4 

## The Two Repositories with MarkdownParse

[My Repository](https://github.com/tylercyang/markdown-parse)

[The Reviewed Repository](https://github.com/RyanRongY/markdown-parse)

## Links to the CommonMark Demo Website

[snippet #1](https://spec.commonmark.org/dingus/?text=%60%5Ba%20link%60%5D(url.com)%0A%0A%5Banother%20link%5D(%60google.com)%60%0A%0A%5B%60cod%5Be%60%5D(google.com)%0A%0A%5B%60code%5D%60%5D(ucsd.edu)%0A)

[snippet #2](https://spec.commonmark.org/dingus/?text=%5Ba%20%5Bnested%20link%5D(a.com)%5D(b.com)%0A%0A%5Ba%20nested%20parenthesized%20url%5D(a.com(()))%0A%0A%5Bsome%20escaped%20%5C%5B%20brackets%20%5C%5D%5D(example.com))

[snippet #3](https://spec.commonmark.org/dingus/?text=%5Bthis%20title%20text%20is%20really%20long%20and%20takes%20up%20more%20than%20%0Aone%20line%0A%0Aand%20has%20some%20line%20breaks%5D(%0A%20%20%20%20https%3A%2F%2Fwww.twitter.com%0A)%0A%0A%5Bthis%20title%20text%20is%20really%20long%20and%20takes%20up%20more%20than%20%0Aone%20line%5D(%0A%20%20%20%20https%3A%2F%2Fucsd-cse15l-w22.github.io%2F%0A)%0A%0A%0A%5Bthis%20link%20doesn%27t%20have%20a%20closing%20parenthesis%5D(github.com%0A%0AAnd%20there%27s%20still%20some%20more%20text%20after%20that.%0A%0A%5Bthis%20link%20doesn%27t%20have%20a%20closing%20parenthesis%20for%20a%20while%5D(https%3A%2F%2Fcse.ucsd.edu%2F%0A%0A%0A%0A)%0A%0AAnd%20then%20there%27s%20more%20text))

# How I tested My Repository

>In order to turn the snippets into tests in my implementation of `MarkdownParseTest.java`, I wrote code that looked something like this...

![myrepotest](Lab-Report-4-Photos\myrepotest.png)

>When I ran the tests, none of them passed as the actual output never matched the expected output. The JUnit output looked something like this...

![myrepotestfailing](Lab-Report-4-Photos\myrepotestfailing.png)

# How I tested the Reviewed Repository

>In order to turn the snippets into tests in the reviewed implementation of `MarkdownParseTest.java` I wrote code that looked like this...

![someimage](Lab-Report-4-Photos\reviewedrepotester.png)

>When I ran the tests, none of them passed as the actual ouput never matched the expected output. The JUnit output looked something like this...

![other image](Lab-Report-4-Photos\reviewedrepotestfail.png)

# How to Fix Snippet 1

>For snippet number 1, I think that adding some lines in the implementation that checks for the backticks in either the brackets or the parentheses. I believe the solution would involve checking if the first backtick that starts the code line begins inside either the brackets or parentheses, and if it does it should be considered part of the link or the name.

# How to Fix Snippet 2

>For snippet number 2, I understand that having forward slashes in front of a character changes some things in the text. Therefore, I would add a check to see if there were backslashes in front of a character and if there was, to ignore the usual open or close brackets and just take it as a normal string. I think this could be done in under 10 lines. Otherwise, completely doing the check for nested brackets and escaped brackets might take more than 10 lines.

# How to Fix Snippet 3

>For snippet number 3, I think that there might be a fix where if there are newline characters within the bracket text or the parenthetical text, you could trim the text to make it so the rest of the implementation could read it normally. 