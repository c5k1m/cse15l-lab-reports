*Brief Note: In accordance to the lab write-up and written permission from Yasushi Oh, screenshots from Jaehoon Kim's repo (he was in my CSE 15L lab group) were utilized to showcase the bugs that were experienced and the corrections that were ultimately made as his repo was used for demonstrations; I had a forking issue on my end during lab that Yasushi Oh can attest to, which is why I can't fork Jaehoon's repo and am using Jaehoon's repo as a reference to what we discussed during lab. However, the screenshots showing the symptoms and outputs as a result of the bugs are from my system.*

# Code Change #1: All Brackets Need to be Looped

![alt text](https://user-images.githubusercontent.com/81746604/151634257-f6ac42e4-fd30-428a-9e7a-9e0e52900c74.png)

Link to Failure-Inducing Input: https://github.com/hungrypingu/markdown-parse/blob/main/test-file3.md

![alt text](https://user-images.githubusercontent.com/81746604/153662839-a5f47647-0805-47d7-92c6-fa5e247c11cf.png)

A symptom of the failure-inducing input was that the file only checked to see if the first parenthesis was looped through as opposed to all sets of parenthesis, which threw an exception for `test-file3.md` as it contained the line `[]link goes here!`, which didn't include any text within the parenthesis. As a result, a `StringIndexOutOfBoundsException` was thrown where we began at index 0 and ended at index -1. We were able to change the `.md` code file such that it checks for all sorts of brackets, not just the `nextOpenBracket` input.


# Code Change #2: Prevent Infinite Loop
![alt text](https://user-images.githubusercontent.com/81746604/151633182-dfd1e949-9144-4948-95cf-1601d0ba9d82.png)

Link to Failure-Inducing Input: https://github.com/hungrypingu/markdown-parse/blob/main/test-file.md

![alt text](https://user-images.githubusercontent.com/81746604/151635904-61b9e92e-ddd2-4790-a375-6732eefc5c25.png))

As a result of not accounting for the possibility of an infinite loop, the code will continue running forever if there isn't a valid link to end the line in the `.md` file. As a result, the program kept running over and over again until Java had to throw its own error out for running an infinite loop. Thus, we made adjustments to the code such that the loop stops without continually looping on forever without the required condition to stop.


# Code Change #3: Fixing Invalid Inputs
![alt text](https://user-images.githubusercontent.com/81746604/153669316-d831b92c-0732-4094-9325-2dd42f62f661.png)

Link to Failure-Inducing Input: https://github.com/hungrypingu/markdown-parse/blob/main/test-file3.md

![alt text](https://user-images.githubusercontent.com/81746604/153669161-cf2a6aaa-6d84-4d91-8812-0d6be51e1b1b.png)

This function will account for brackets that don't contain any sort of text between them. Our original code was not able to account for the possibility of having an empty set of brackets. Thus, the wrong output was thrown, one that isn't even contained in the `test-file3.md` file. Fixing this error allowed us to prevent the method from throwing an output of `[https://something.com, some-page.html]` as opposed to the empty brackets in the `test-file3.md` file.
