# Lab Report 2: Debugging
## Example 1
### Error on strings without "()"
![error()](error1.png)
[Link to the test file that promted the error](https://github.com/peds24/markdown-parser/blob/16965b69b21be5bb90ca3ec745c901722bb1f035/noParenth.md)

#### Symptom
![ouput1](ouput1.png)

#### Explination 
*Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.*

***
## Example 2
### Error on strings without "[]"
![error[]](error2.png)
[Link to the test file that promted the error](https://github.com/peds24/markdown-parser/blob/addeb07649e63d409f806df129581d30738d723f/justParenth.md)

#### Symptom
![ouput2](output2.png)

#### Explination 
*Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.*

***
## Example 3
### Error on strings with space "in between"
![spaceError](error3.png)
[Link to the test file that promted the error](https://github.com/peds24/markdown-parser/blob/c430fa89f03a6383d4b77ac2485af86b43ed9cff/spaceBetween.md)

#### Symptom
![ouput3](output3.png)
**There is no error in compilation, yet this input is invalid and the code should be able to catch that. What we are texting are links in .md files so the example passed here** `[link]          (link.html)` **has the incorrect formatting so it would not be a valid link. The code should identify thi serror and not parse it, as its not a valid input.**

#### Explination 
*Write 2-3 sentences describing the relationship between the bug, the symptom, and the failure-inducing input.*
