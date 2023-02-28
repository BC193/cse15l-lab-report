# CSE 15L Lab Report 4

## Table of Contents
- Logging into ieng6
- Cloning the Repository
- Tests Fail
- Fixing the Code
- Tests Pass
- Commit and Push

## Logging into ieng6

<img width="500" alt="Screen Shot 2023-02-27 at 2 03 50 PM" src="https://user-images.githubusercontent.com/83740546/221696316-bec1ee45-b5b7-46df-91de-1b8370b50036.png">

### Commands Used
- ```ssh cs15lwi23apj@ieng6.ucsd.edu```
- ```<enter>```

## Cloning the Repository

<img width="729" alt="Screen Shot 2023-02-27 at 2 09 28 PM" src="https://user-images.githubusercontent.com/83740546/221697127-e0174cee-e58b-4461-92d9-0b0525506638.png">

### Commands Used
- ```git clone git@github.com:BC193/lab7.git```
- ```<enter>```
- ```cd lab7```
- ```<enter>```


## Tests Fail
<img width="1061" alt="Screen Shot 2023-02-27 at 2 20 03 PM" src="https://user-images.githubusercontent.com/83740546/221698990-99524c74-7aaa-4d38-a307-88e5c8126469.png">

### Commands Used
- ```javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java```
- ```<enter>```
- ```java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests```
- ```<enter>```

## Fixing the Code
<img width="579" alt="Screen Shot 2023-02-27 at 5 24 38 PM" src="https://user-images.githubusercontent.com/83740546/221728449-79f734e9-bc2d-4381-b678-03ee9106213e.png">

### Commands Used
- ```git status```
- ```git add --all```
- ```nano ListExamples.java```
- ```<enter>```
- ```<down>``` 42 times
- ```<right>``` 12 times
- ```<backspace>```
- ```2```
- ```ctrl x```
- ```y```
- ```<enter>```

## Tests Pass
<img width="971" alt="Screen Shot 2023-02-27 at 5 31 15 PM" src="https://user-images.githubusercontent.com/83740546/221729441-d0e25431-df2a-4849-8012-d589beaed386.png">

### Commands Used
- ```<up>``` 3 times
- ```<enter>```
-  ```<up>``` 3 times
- ```<enter>```

## Commit and Push
<img width="512" alt="Screen Shot 2023-02-27 at 5 32 48 PM" src="https://user-images.githubusercontent.com/83740546/221729619-cfc6f62e-8de2-4ee6-9f49-5438a643fa7d.png">

<img width="487" alt="Screen Shot 2023-02-27 at 5 37 32 PM" src="https://user-images.githubusercontent.com/83740546/221730320-3b8ddb85-5500-47ca-b7d0-ddcb022e821d.png">

### Commands Used
- ```git commit -m "fixed code in the ListExamples.java file"```
- ```git push```
