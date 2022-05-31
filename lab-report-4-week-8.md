# Lab Report 4

[My Markdown Parser](https://github.com/badnanx/markdown-parser-reborn.git)

[Other student's markdown parser](https://github.com/ddn005UCSD/markdown-parser.git)

* Snippet 1 expected output:

    `[url.com, `\``google.com, google.com, ucsd.edu]`
* Snippet 2 expected output:
    
    `[a.com, a.com((, example.com]`
* Snippet 3 expected output:

    `[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, github.com And there's still some more text after that. [this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/]`

* Test code:
![image](snippetTests.png)

- My output:
    
    * `testSnippet1()` and `testSnippet2()` passed but `testSnippet3()` failed

![image](myOutput.png)



- Other student's output:

    * `testSnippet1()` passed but `testSnippet2()` and `testSnippet3()` failed

![image](otherOutput.png)

