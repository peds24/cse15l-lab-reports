# Lab Report 5
## General Questions
* **How did you find the result discrepancy?**

I found the test descrepancy by running making a copy of the test file directory to my own markdown parser, then I ran `bash script.sh > results.txt` in order to run the script that runs the files and prints the results, then saves it to a file. I did this in the other repo and used vimdiff to open up the two files side by side and compare them. 
    
[Link to test file 194](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/194.md)

[Link to test file 201](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/201.md)

## Test 1
![file194](/LabReport5/file194.png)

### Common Mark Output for the File
![common194](/LabReport5/common194.png)

Here for this test both implementations are incorrrect because they both produce a wrong output. My implementation gives an error because it sees a space or invalid character between parenthesis and square bracket and exits the loop there. The other implementation returns (url), whioch is wrong as the common mark website returns Foo*bar].

### FIX

![codeSnippet](/LabReport5/codeSnippet.png)

The orange box is enclosing the if statment that is getting triggered once the parser recognizes another character that isnt a parenthesis after a square bracket. The bug here involves the break statment in the if statment. The break is preventing the parser to reach the second link that is the valid one. The fix for this would be to add a continue statment or change the constraints of the if statment. The general fix would be to maybe keep a boolean counter to see if something is correct or wrong so it can go chek the rest of the file. In the end if the counter returns false, then its okay to return an empty list, but maybe when it finds a valid link it gets triggered to True and then extracts the valid link.
****

## Test 2
![file201](/LabReport5/file201.png)

### Common Mark Output for the File
![common201](/LabReport5/common201.png)

For this test my code actually returns a correct ouput which is an empty list as the test file does not contain a valid link. The other repo is returning baz as its the item between the parenthesis. But as the image of the commonmark demonstarates, none of them are blue hightlighted meanin they are invalid links. Because my markdown parse test gives the correct output, there is no fix needed on my side.
