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
The symptom was that the test failed due to the output n

Show a screenshot of the code change diff from Github (a page like this)

Link to the test file for a failure-inducing input that prompted you to make that change

Show the symptom of that failure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)

Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.
