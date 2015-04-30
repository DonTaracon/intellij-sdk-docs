---
layout: editable
title: 9. Commenter Test
---

In this test we will check if the commenter, implemented in the
[Commenter](commenter.html)
section of the
[Custom Language Support Tutorial](cls_tutorial.html),
works as we expect.

### 9.1. Define a test method

```java
public void testCommenter() {
    myFixture.configureByText(SimpleFileType.INSTANCE, "<caret>website = http://en.wikipedia.org/");
    CommentByLineCommentAction commentAction = new CommentByLineCommentAction();
    commentAction.actionPerformedImpl(getProject(), myFixture.getEditor());
    myFixture.checkResult("#website = http://en.wikipedia.org/");
    commentAction.actionPerformedImpl(getProject(), myFixture.getEditor());
    myFixture.checkResult("website = http://en.wikipedia.org/");
}
```

### 9.2. Run the test

Run the test and make sure it's green.

-----

[Previous](tutorials/writing_tests_for_plugins/find_usages_test.html) 
[Top](tutorials/writing_tests_for_plugins.html) 
[Next](tutorials/writing_tests_for_plugins/reference_test.html)

