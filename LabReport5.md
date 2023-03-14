# CSE 15L Lab Report 5

## Table of Contents
- Part 1: Grading Script
- Part 2: Testing Submissions

## Part 1: Grading Script
<img width="610" alt="Screen Shot 2023-03-13 at 11 10 58 PM" src="https://user-images.githubusercontent.com/83740546/224911461-49d5fbae-74ce-4fb3-8a20-aa3e897a50e1.png">
> Grading Script for the ListExamples class

### What Each Part Checks:
* The variables ```FILE``` and ```CPATH``` are used to increase clarity in the code and add flexibility if different files are to be ran or checked
* ```rm -rf``` clears the entirety of ```student-submissions``` repo in order to make sure there are no colliding files with each test
* Multiple remove statements are used to clear possibly messy implmentations of code
* The first ```if``` statement checks if there exists a file that is named ```ListExamples.java``` using ```-e``` and an ```echo``` statement is used to announce it exists and if there isn't the process is stopped by ```exit 1``` indicating a missing file
* ```cp``` is used to move the submission files into the main directory and allow for the tester to have direct access to the file we are testing
* ```Method1``` and ```Method2``` use ```grep - o``` in order to find a particular line in the code while ```awk{print $ }``` specifies what word to save as a string
* Through the use of ```-n``` it allows use to find if the ***merge*** and ***filter*** method exist because if the method headers were found then something will be stored at the variables
* An if statement with ```echo``` and ```exit``` are used again to discern if the method headers are correctly implemented and the script should continue
* After compiling the file and tester we can check if it was compiled with another ```if``` statement that follows a similar logic to the other statements. If it worked as intended continue but if it fails ```exit```
* Then we can initialize the tester and redirect the output into a ```.txt``` file
* By directing the result of the JUnit Tests into a file it creates a situation where you can read the file and ```grep``` to find specific information
* Just like the ```Method``` variables we can check for: total, passed, and failed cases through the use of ```grep -o``` and ```awk```
* By filtering through an ```if``` statement it can present the results to the student

## Part 2: Testing Submissions

<img width="788" alt="Screen Shot 2023-03-13 at 7 56 47 PM" src="https://user-images.githubusercontent.com/83740546/224881344-0e448492-0564-44ab-a812-df7a98a37568.png">

>This shows a failing submission. The code tracks that there exists the correct file and method. The code compiles but the implmentation is incorrect. We later can see it was a bug in incrementing index2.

<img width="822" alt="Screen Shot 2023-03-13 at 11 27 05 PM" src="https://user-images.githubusercontent.com/83740546/224914320-ad458012-81e1-4791-8ea1-6d9b1119c14a.png">

>This shows a working submission. The code tracks that there exists the correct file and method. The code compiles and the tester works correctly.

<img width="846" alt="Screen Shot 2023-03-13 at 9 59 05 PM" src="https://user-images.githubusercontent.com/83740546/224897536-5fb635b0-0396-4eaa-b8c1-4fc2a41ca014.png">

>There is a compilation error as the code is missing a semicolon. The other ascpects work as the file exists and has the proper methods.


><img width="827" alt="Screen Shot 2023-03-13 at 10 00 35 PM" src="https://user-images.githubusercontent.com/83740546/224897723-d00972f4-d59d-4b53-8992-cd5d9d11c393.png">

>There is a method format error. The arguments of ```filter``` are in the wrong order giving the implication that the proper ```filter``` does not exist. The other aspects of the file work as the file exists but the methods are the issue. 


<img width="821" alt="Screen Shot 2023-03-13 at 10 01 40 PM" src="https://user-images.githubusercontent.com/83740546/224897877-7f7051c0-c194-475a-a24c-23b359492aeb.png">

>There is a file name error. The name is ```ListMethods.java``` instead of ```ListExamples.java```. This would give the implication that the correct file does not exist.


<img width="802" alt="Screen Shot 2023-03-13 at 10 03 00 PM" src="https://user-images.githubusercontent.com/83740546/224898079-9274a4c9-7579-4e6b-b19c-b5d2cdd962da.png">

>Similar to the file name error, while there is a correct implementation, there lacks the correct naming order. In this instance it is placed in a folder named ```pa1```. This would not be recognized as the correct file. 
