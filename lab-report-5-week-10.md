# How the Tests were Found
The method that I used to find the different results was to search through the results manually and compare the results. First, I went into my directory via the terminal and entered `bash script.sh > results-my-implement.txt` into the command line, which would create a separate file containing the results of all 652 tests for my implementation. Next, I went into the directory the implementation provided in lab 9 via the terminal and entered `bash script.sh > results-wk9-implement.txt` into the command line, which would create a separate file containing the results of all 652 tests for the week 9 implementation. Finally, I opened both `.txt` files and compared the results of the `.txt` files as shown below.

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159062466-028fc6b6-5f9b-4d4a-9af4-dec319aa2ab2.png)

It didn't take to long after going through each file to recognize that some of the files with discrepancies in terms of their output included `22.md` and `31.md`, which will be the two files used for this lab report.

# Test 1: `22.md`

According to the commonmark.js demo website, the correct output is supposed to be `[bar*]`. However, the following screenshot below illustrates the outputs from my implementation and the week 9 implementation respectively.

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159064346-be697b16-825f-4965-8286-2e82bf793959.png)

As we can see, none of the implementations produced the correct output since my implementation produced `[/bar\* "ti\*tle"]` while the week 9 implementation produced an empty list `[]`. Since both implementation are incorrect, we will examine my implementation and give a brief insight as to the problem with the code and how the problem can be fixed.

The following screenshot contains the contents of the `MarkdownParse.java` file...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159071100-133a93ce-6011-4450-81e2-0cd5e361c367.png)

In lines 21-30, we notice that the program simply takes the substring of any sort of text found between the character after the open parenthesis and the next closed parenthesis. This attempt to find a substring will be problematic when the program simply takes everything between the two parentheses without omitting unnecessary and unwanted text. Furthermore, the loop will simply stop once a certain index has been reached without actually inspecting the content of the string in between the parentheses. Thus, the program needs to be fixed such that it omits unnecessary characters, like the `/` before `bar` and the `/` after `bar`. Furthermore, we need to add additional code to ensure that the `"ti\*tle"` portion does not get included into the resulting link as it includes quotations.

Therefore, the main focus of the change to fix the bug will primarily deal with ensuring that parentheses and brackets are not the only components being inspected when deciding what should be included in the output.


# Test 2: `41.md`

According to the commonmark.js demo website, the correct output is supposed to be `[]` since the test does not included any valid links. However, the following screenshot below illustrates the outputs from my implementation and the week 9 implementation respectively.

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159078495-2329140c-23d8-4d99-bb35-8215660813bd.png)

As we can see, my implementation produced `[url &quot;tit&quot;]` while the week 9 implementation produced the correct output of an empty list `[]`. We will examine my implementation and give a brief insight as to the problem with the code and how the problem can be fixed such that an empty list `[]` is produced.

Again, for reference, the following screenshot contains the contents of the `MarkdownParse.java` file...

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159071100-133a93ce-6011-4450-81e2-0cd5e361c367.png)

The necessary change is somewhat similar to the change required for my implementation for the `22.md` file. In lines 21-30, we notice that the program simply takes the substring of any sort of text found between the character after the open parenthesis and the next closed parenthesis. It simply tries to find the placement of the parentheses and brackets in order to include any sort of characters between the parentheses. While the `22.md` file test included some text that was supposed to be included in the output list, namely the `bar*` output, this file isn't supposed to output anything at all since the entire URL is invalid. Furthermore, the loop will simply stop once a certain index has been reached without actually inspecting the content of the string in between the parentheses. Thus, we will need to add a series of if-statements to ensure that the `url &quot;tit&quot;` does not get interpreted as a link since it is merely a series of strings.

Therefore, the main focus of the change to fix the bug will primarily deal with ensuring that parentheses and brackets are not the only components being inspected when deciding what should be included in the output.


