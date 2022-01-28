# Lab Report 2 - Symptoms, Bugs, and Failure-Inducing Input

>The original code that was given to us looked something like this...

![original code](Lab-Report-2-Photos\Original-Code.png)

## 1. First Bug

>Our first bug was encountered when the brackets and parentheses of the [links were misplaced or in the wrong order](https://github.com/tylercyang/markdown-parse/commit/e0c420283b9135bd54b1879b552ebdd6e754abab#diff-c1ee2d48f5f64b4463a98907818b5846f49cc9dd67f88882a8b551106ec320fb). In this case the expected output should be nothing. 

>To fix this, we moved some variables and added some if statements...

![bug 1 photo 1](Lab-Report-2-Photos\bug-1-photo-1.png)

![bug 1 photo 2](Lab-Report-2-Photos\bug-1-photo-2.png)

> Because the parentheses and brackets were misplaced, this caused the original code to stay in the while loop which created an infinite loop. It looked something like this...

![bug 1 photo 3](Lab-Report-2-Photos\bug-1-photo-3.png)

>To recap, the file that caused the bug switched one of the brackets and one of the parentheses which meant that in the original code, the while loop would continue infinitely. This would produce an infinite loop in the output. We fixed this by putting a if statement that breaks if the indexes of the parentheses/brackets were weird.

---

## 2. Second Bug

>Our second bug was encountered when the file [looked like a link file but contained a photo path](https://github.com/tylercyang/markdown-parse/commit/e0c420283b9135bd54b1879b552ebdd6e754abab#diff-8b79fb9106da4293b8fbbe72b2e0ccabcd0fa4ed999cedb59be79e4f2b3f9674). In this case, the expected output should be nothing. 

>To fix this, we added a for loop that looped through an array of common image extensions. If the for loop detected an image extension, it would break the for loop...

![bug 2 photo 2](Lab-Report-2-Photos\bug-2-photo-2.png)

![bug 2 photo 3](Lab-Report-2-Photos\bug-2-photo-3.png)

>Before this change, our output would still contain the path to the image which looked something like this...

![bug 2 photo 1](Lab-Report-2-Photos\bug-2-photo-1.png)

>To recap, our failure inducing input was a correctly formatted link, but instead of a link to a page on the internet, it contained a file path to an image. The correct output should be nothing but our code outputed the path to the image. To fix this, we created a loop that would break the outer while loop if it detected a common image extension in the "link".

---

# 3. Third Bug

> Our third bug was encountered when the file input was a link that contained white space either [between the bracket and parentheses](https://github.com/tylercyang/markdown-parse/commit/766ea47a3d1b5780635c507822599cc46614442a#diff-ed50ab3296d5413774c20fffeb1db53b1616553ca467a23f5b0580c2cec4c431) or [between the characters in the link](https://github.com/tylercyang/markdown-parse/commit/766ea47a3d1b5780635c507822599cc46614442a#diff-405a2041d351aaf3508b50349c600a460b24bda14d822281df19663894148396). Both inputs should give nothing as the output. 

>To fix this, we added and statements in one of the statement to check for white space where it shouldn't be...

![bug 3 photo 1](Lab-Report-2-Photos\bug-3-photo-1.png)

>Before this change, the output would still print out the links which looked something like this...

![bug 3 photo 2](Lab-Report-2-Photos\bug-3-photo-2.png)

>To recap, our failure inducing input was a correctly formatted link, but with white space between the brackets and parentheses. Additionally, another input that caused a bug was a file with white space between the characters in the link which shouldn't be possible. What caused this bug was white space where it shouldn't be, but this caused output to still print out the contents inside the parentheses.