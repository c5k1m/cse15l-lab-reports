*Brief Note: As expected, since each group's `MarkdownParse.java` file was different, a different format of a test between my Markdown-Parse Repo and the repo being reviewed was required for each code snippet.*

My Markdown-Parse Repo: https://github.com/c5k1m/markdown-parse

Repo being Reviewed: https://github.com/maotcha/markdown-parse

# Snippet 1

The code below illustrates how the actual test for Snippet 1 was conducted in the `MarkdownParseTest.java` file on my Markdown-Parse Repo, where the assert test includes what the test method should've produced per the CommonMark demo site...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157922566-66e309b1-444c-4671-bf9a-fadf21d64d34.png)


The code below illustrates how the actual test for Snippet 1 was conducted in the `MarkdownParseTest.java` file on the repo being reviewed, where the assert test includes what the test method should've produced per the CommonMark demo site...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157933989-a4d9855f-5f7d-433c-ace1-3086ed1ffdce.png)


The screenshot below provides the output of running Snippet 1 on my Markdown-Parse Repo...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157915930-872700f0-6f49-4d0e-9716-5fd40089b5d1.png)

As we can see, the test clearly failed because the correct output was supposed to be ``[`google.com, google.com, ucsd.edu]``, but the actual output also included the `url.com` links as well into the output as shown in the JUnit stack trace presented above as a result of the failed test.


The screenshot below provides the output of running Snippet 1 on the repo being reviewed...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157933887-243798bb-d69f-4fe9-aabe-bdb9b0949d95.png)

As we can see, the test clearly failed because the correct output was supposed to be ``[`google.com, google.com, ucsd.edu]``, but, similar to my Markdown-Parse repo, the actual output also included the `url.com` link as well in the front of the output.

**Code-Change Question (Snippet 1)**: In terms of a code change in my program, it will be a simple addition to the code, where we will add an if statement that checks to see if there is an invalid set of square brackets that requires the program to avoid including what appears to be a link as a link in the output. The line of code that initially starts off our while loop of iterating through the file is the line ``int nextOpenBracket = markdown.indexOf("[", currentIndex);``, where we only look for the opening square bracket and don't necessarily check to see if the bracket are valid per our method's goals. Thus, adding the condition will take less than 10 lines because given that the method took in "`[a link`](url.com)" as an input and treated `url.com` as a valid link, adding an if condition will definitly take elss than 10 lines to prevent `url.com` from being included in the output.


# Snippet 2

The code below illustrates how the actual test for Snippet 2 was conducted in the `MarkdownParseTest.java` file on my Markdown-Parse Repo, where the assert test includes what the test method should've produced per the CommonMark demo site...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157922706-08e587f3-9548-4988-a553-a93a63e0b020.png)


The code below illustrates how the actual test for Snippet 2 was conducted in the `MarkdownParseTest.java` file on the repo being reviewed, where the assert test includes what the test method should've produced per the CommonMark demo site...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157929139-49dcfb4f-89eb-499c-8efd-9f54b89483c2.png)

The screenshot below provides the output of running Snippet 2 on my Markdown-Parse Repo...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157933508-f38be5ee-194d-4482-a25c-bf2dfc419eec.png)

As we can see, the test clearly failed because the correct output was supposed to be `[a.com, a.com(()), example.com]`, but the actual output was `[a.com, a.com((, example.com]`, where `a.com((` is missing two closing parenthesis brackets as shown in the JUnit stack trace presented above as a result of the failed test. 


The screenshot below provides the output of running Snippet 2 on the repo being reviewed...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157933709-0d0f8415-b102-4f44-aa48-65053d1a15ba.png)

As we can see, the test clearly failed because the correct output was supposed to be `[a.com, a.com(()), example.com]`, but the actual output was `[a.com)](b.com, a.com(()), example.com]`, where it's clear that the `)](b.com` portion in the `a.com)](b.com` output was not supposed to be included in the output as shown in the JUnit stack trace presented above as a result of the failed test. 



# Snippet 3

The code below illustrates how the actual test for Snippet 3 was conducted in the `MarkdownParseTest.java` file on my Markdown-Parse Repo, where the assert test includes what the test method should've produced per the CommonMark demo site...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157929968-0408e6ba-d640-42f3-a5af-56fe23a50bff.png)


The code below illustrates how the actual test for Snippet 3 was conducted in the `MarkdownParseTest.java` file on the repo being reviewed, where the assert test includes what the test method should've produced per the CommonMark demo site...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157930272-b977aeca-fe90-4724-a67a-8f6f63b92c55.png)


The screenshot below provides the output of running Snippet 3 on my Markdown-Parse Repo...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157932392-2026d2aa-6434-4541-b1ab-96b971293a7f.png)

As we can see, the test clearly failed because the correct output was supposed to be `[https://ucsd-cse15l-w22.github.io/]`, but the actual output was a result that spenned multiple lines, included `https://www.twitter.com`, which isn't included in the expected output, and included some text that was not supposed to be treated as links, such as the text `And there's still some more text after that.`


The screenshot below provides the output of running Snippet 3 on the repo being reviewed...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/157933110-76460f34-12d2-4277-80fd-154ba801472c.png)

As we can see, the test clearly failed because the correct output was supposed to be `[https://ucsd-cse15l-w22.github.io/]`, but the actual output was an empty set of brackets, signifying that the method did not treat any of the input as valid links.
