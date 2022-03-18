# How the Tests were Found
The method that I used to find the different results was to search through the results manually and compare the results. First, I went into my directory via the terminal and entered `bash script.sh > results-my-implement.txt` into the command line, which would create a separate file containing the results of all 652 tests for my implementation. Next, I went into the directory the implementation provided in lab 9 via the terminal and entered `bash script.sh > results-wk9-implement.txt` into the command line, which would create a separate file containing the results of all 652 tests for the week 9 implementation. Finally, I opened both `.txt` files and compared the results of the `.txt` files as shown below.

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159062466-028fc6b6-5f9b-4d4a-9af4-dec319aa2ab2.png)

It didn't take to long after going through each file to recognize that some of the files with discrepancies in terms of their output included `22.md` and `32.md`, which will be the two files used for this lab report.

# Test 1: `22.md`

Accoring to the commonmark.js demo website, the correct output is supposed to be `foo`.

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159064346-be697b16-825f-4965-8286-2e82bf793959.png)


# Test 2: `32.md`

![markdown-parse repo picture](https://user-images.githubusercontent.com/81746604/159064670-505a3e90-2f15-4744-83bf-a0d7f84d5ef1.png)
