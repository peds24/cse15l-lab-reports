# Lab Report 4
**Repository Links**
* [Personal Repository](https://github.com/peds24/markdown-parser)
* [Week 7 Repository](https://github.com/TuannDang/markdown-parser)
---]
> **Note:** Images show only my personal MardownParse tests, but to test for the other parse implementation, you would just change line 4 to the different java file to be accessed.
## Snippet 1
### Expected Output
**Only Valid Link:**
```
[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```
**Expected Result:**
```
[`google.com, google.com, ucsd.edu]
```

### Evidence of Code --> Test
![snippet1](/LabReport4/snippet1test.png)

### Personal Implementation
![personalFail1](/LabReport4/personalFail1.png)

### Week 7 Implementation
![repoFail1](/LabReport4/repoFail1.png)

---
## Snippet 2
### Expected Output
**Only Valid Link:**
```
[nested link](a.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
**Expected Result:**
```
[a.com, a.com(()), example.com]
```

### Evidence of Code --> Test
![snippet2](/LabReport4/snippet2test.png)

### Personal Implementation
![personalFail2](/LabReport4/personalFail2.png)

### Week 7 Implementation
![repoFail2](/LabReport4/repoFail2.png)

---
## Snippet 3
### Expected Output
**Only Valid Link:**
```
[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)
```
**Expected Result:**
```
[https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule]
```

### Evidence of Code --> Test
![snippet3](/LabReport4/snippet3test.png)

### Personal Implementation
![personalFail3](/LabReport4/personalFail3.png)

### Week 7 Implementation
![repoFail3](/LabReport4/repoFail3.png)

---
# Questions
1. The first thing that comes to mind is to implement a counter or sensor that checks for Back ticks. The way this would work is that if the current character is a backtick, then it would note its position and keep a lookout for the next backtick that closes the first one. With this information stored it can check if both backticks are between the square brackest position in order to be a valid link. 

2. My implementation only missed the rest of the parenthesis in the second link. This is because it prematurley ended the loop and returned the valid link when it sensed the first parenthhesis, unawhere that there was more. I believe an implementation to solve this would be quite large because I imagine creating a new loop that checks the rest of the characters after the paranthesis that opens the link and checks what is after until a break in the line. This way it can count everything betwen the first parenthesis and until it finds the last one.

3. My implementation of MarkdownParse suffered heap space errors, that caused it to fail and not reach the valid link. I am not aware of how line breaks work as characters in a String, but I believe that a fix would be to create a check (if statment) that if a character to check if its parenthesis or square bracket, should check for this line break in order to break the loop as line breaks are not leagal to have within links in MarkDown. This way the lop will break in bad inputs and continue onto the next input instead of getting heap errors.
