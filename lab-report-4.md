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
```
**Expected Result:**
```
[`google.com]
```

### Evidence of Code --> Test
![snippet1](/LabReport4/snippet1test.png)

### Personal Implementation

### Week 7 Implementation

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
[a.com, a.com, example.com]
```

### Evidence of Code --> Test
![snippet2](/LabReport4/snippet2test.png)

### Personal Implementation

### Week 7 Implementation
---
## Snippet 3
### Expected Output
**Only Valid Link:**
```
[nested link](a.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
**Expected Result:**
```
[a.com, a.com, example.com]
```

### Evidence of Code --> Test
![snippet3](/LabReport4/snippet3test.png)

### Personal Implementation

### Week 7 Implementation
---
# Questions
1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.
