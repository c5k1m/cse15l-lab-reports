*Brief Note: In accordance to the lab write-up and written permission from Anzhi Weng, screenshots from Jaehoon Kim's repo (he is in my CSE 15L lab group) and links of his* ```.md``` *files were utilized to showcase the bugs that were experienced and the corrections that were ultimately made as his repo was used for demonstrations; I had a forking issue on my end during lab that Yasushi Oh can attest to, which is why I can't fork Jaehoon's repo and am using Jaehoon's repo as a reference to what we discussed during lab.*

# Code Change #1: All Brackets Need to be Looped

![alt text](https://user-images.githubusercontent.com/81746604/151634257-f6ac42e4-fd30-428a-9e7a-9e0e52900c74.png)

Link to Failure-Inducing Input: https://github.com/hungrypingu/markdown-parse/blob/main/test-file2.md

A symptom of the failure-inducing input was that the file would run properly even though there was an invalid input as seen the in the ```.md``` file that contains the line "[]link goes here!" Thus, we can assume that the original code only checked the first element and did not loop any further as it only checked the first element. We were able to change the ```.md``` code file such that it checks for all sorts of brackets, not just the ```nextOpenBracket``` input.


# Code Change #2: Invalid Links
![alt text](https://user-images.githubusercontent.com/81746604/151636944-99aecdcb-9517-4596-ab24-277f8c604e42.png)

Link to Failure-Inducing Input: https://github.com/hungrypingu/markdown-parse/blob/main/test-file3.md



# Code Change #3: Prevent Looping Forever
![alt text](https://user-images.githubusercontent.com/81746604/151633182-dfd1e949-9144-4948-95cf-1601d0ba9d82.png)

Link to Failure-Inducing Input: https://github.com/hungrypingu/markdown-parse/blob/main/test-file.md

![alt text](https://user-images.githubusercontent.com/81746604/151635904-61b9e92e-ddd2-4790-a375-6732eefc5c25.png))

As a result of not accounting for the possibility of an infinite loop, the code will continue running forever if there isn't a valid link to end the line in the ```.md``` file. As a result, the program kept running over and over again until Java had to throw its own error out for running an infinite loop.



