# Lab Report 2

## Code Change #1
![Image](./Screenshot%20(809).png)

**Links for the test files that failed previously:**

* [Test File 5](https://github.com/michaelndiaz/markdown-parser/blob/main/test-file5.md)
* [Test File 6](https://github.com/michaelndiaz/markdown-parser/blob/main/test-file6.md)

**The failing output looked like this:**

```
Time: 0.022
There were 2 failures:
1) File5Test(MarkdownParseTest)
java.lang.AssertionError: expected:<[]> but was:<[page.com]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.File5Test(MarkdownParseTest.java:64)
2) File6Test(MarkdownParseTest)
java.lang.AssertionError: expected:<[]> but was:<[page.com]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.File6Test(MarkdownParseTest.java:70)

FAILURES!!!
Tests run: 9,  Failures: 2
```
The symptom of this bug is that we expect it to just return an empty list, but it returns a list with a link in it. The failure inducing inputs (the test files) are (1) a file with something in between the brackets and the parentheses and (2) a file that is formatted like an image, not a link. Due to this, the bug in the program is that it recognizes a link when it isn't supposed to because it does not recognize that (1) things in between the brackets and the parentheses does not follow a link format and (2) the exclamation mark in front of a similar link format is an image instead of a link. 

## Code Change #2

![Image](./Screenshot%20(807).png)


**Links for the test files that failed previously:**

* [Test File 1](https://github.com/michaelndiaz/markdown-parser/blob/main/test-file.md)
* [Test File 2](https://github.com/michaelndiaz/markdown-parser/blob/main/test-file2.md)
* [Test File 8](https://github.com/michaelndiaz/markdown-parser/blob/main/test-file8.md)

**The failing output looked like this:**

```
Time: 0.022
There were 3 failures:
1) File8est(MarkdownParseTest)
java.lang.AssertionError: expected:<[a link on the first line]> but was:<[]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.File8est(MarkdownParseTest.java:80)
2) File1Test(MarkdownParseTest)
java.lang.AssertionError: expected:<[https://something.com, some-thing.html]> but was:<[]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.File1Test(MarkdownParseTest.java:43)
3) File2Test(MarkdownParseTest)
java.lang.AssertionError: expected:<[https://something.com, some-page.html]> but was:<[]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.File2Test(MarkdownParseTest.java:49)

FAILURES!!!
Tests run: 9,  Failures: 3
```

The symptom of this bug is that it returns an empty list when it should return the links within the files. The test files that cause this error are test file 1, 2, and 8. Both 1 and 2 have consecutive links after another and 8 has an empty bracket with a link in parentheses and then an open bracket afterwards. The bug that causes this problem is from the fact that we put `openParen - closeBracket > 0`. This tells us that the distance between the open parentheses and the close bracket is zero. However, that is incorrect as it should be 1 since the open parentheses should just follow right after the close bracket, not be at the same index. That is why it returns an error for these test files, since it essentially cannot recognize and return a link when our code is written this way.

## Code Change #3
![Image](./Screenshot%20(808).png)

**Links for the test files that failed previously:**

* [Test File 6](https://github.com/michaelndiaz/markdown-parser/blob/main/test-file6.md)


**The failing output looked like this:**

```
Time: 0.019
There was 1 failure:
1) File6Test(MarkdownParseTest)
java.lang.AssertionError: expected:<[]> but was:<[page.com]>
        at org.junit.Assert.fail(Assert.java:89)
        at org.junit.Assert.failNotEquals(Assert.java:835)
        at org.junit.Assert.assertEquals(Assert.java:120)
        at org.junit.Assert.assertEquals(Assert.java:146)
        at MarkdownParseTest.File6Test(MarkdownParseTest.java:70)

FAILURES!!!
Tests run: 9,  Failures: 1
```
The symptom of this bug is that it returns a list with a link instead of an empty list. The test file is the same as before: a string with the format of an image. However, the program still does not recognize an image, and since the format is so similar, it treats it as a link and adds it into the list. That is why, in order to fix this bug, we added a piece of code that would check to see if there is an exclamation mark in front of the brackets and thus, not treat it as a link. 



