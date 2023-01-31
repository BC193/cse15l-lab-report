# CSE 15L Lab Report 2

## Table of Contents
- Part 1: Creating A Web Server
- Part 2: Identifying Bugs
- Part 3: Reflections

## Part 1: Creating A Web Server
>Goal: Creating a web server called ```StringServer```

- We want to read requests that look like ```/add-message?s=<string>```
- The method below achieves this

<img width="528" alt="Screen Shot 2023-01-30 at 2 53 53 PM" src="https://user-images.githubusercontent.com/83740546/215614885-8c47ebe5-894b-46cf-ba37-0e37a10fdfdd.png">

#### Multiple methods are called 
- ```.getPath()```: retrieves the URL information and the current address
- ```.equals()```: checks the value of a string with (in this instance) the URL arguments
- ```.contains()```: compares the argument with the path to find if a phrase is present
- ```.getQuery()```: looks for the **query** command, ```?```, and the information that follows it
- ```.split()```: finds the information after the designated value

#### Method Usage
- ```.equals()```: the arguments **"/"** and **"s"** are two more filters we use in finding the correct course of action to take when are presented with a URL 
- ```.contains()```: we use the argument **"/add-message"** to find if we are attempting to add a message
- ```.split()```: the argument **"="** is used in order to find the actual arguments in the URL path

#### Values Changed
- The main value that is changed is messages.
  - messages is a string that holds all the messages we add through the use of the web server
  - It will update when we refresh the page or run a web server command

### Example 1
<img width="455" alt="Screen Shot 2023-01-30 at 3 05 41 PM" src="https://user-images.githubusercontent.com/83740546/215616813-fb82e8d1-9ebf-4899-93b9-32e53c69f69f.png"> 

- Uses all the above methods
- Uses all the above methods and their arguments except ```.equals("/")```
- messages is updated to ```"CSE15L" + '\n'```

### Example 2
<img width="486" alt="Screen Shot 2023-01-30 at 3 06 09 PM" src="https://user-images.githubusercontent.com/83740546/215616826-1bb75983-377a-42bd-82b9-dc198ef29a67.png">

- Uses all the above methods
- Uses all the above methods and their arguments except ```.equals("/")```
- messages is updated to ```"CSE15L" + '\n' + "It works!" + '\n'```

## Part 2: Identifying Bugs
```  
 @Test
 public void sameNumber(){
   double[] input1 = {8.0, 8.0, 8.0, 8.0};
   assertEquals(8.0, ArrayExamples.averageWithoutLowest(input1), 0.0001);
 }
  ```
>Failure Inducing Input

```
  @Test
  public void testaverageWithoutLowest(){
    double[] input1 = {8.0, 9.0, 10.0, 11.0};
    assertEquals(10.0, ArrayExamples.averageWithoutLowest(input1), 0.0001);
  }
  ```
  >Working Input

<img width="888" alt="Screen Shot 2023-01-30 at 6 19 18 PM" src="https://user-images.githubusercontent.com/83740546/215643421-a3417f42-df3e-4ad1-9345-319f51e93a2d.png">


```
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
  ```
  >averageWithoutLowest method with bug


```
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    int count = 1;
    for(double num: arr) {
      if(num == lowest && count == 1) { 
      count --;
      continue; }
    } else{ sum+= num; }
    return sum / (arr.length - 1);
  }
  ```
  >averageWithoutLowest method without bug
  
  - I flipped the if statement by moving its inside parts to an else statement and creating an instance where it will iterate to the next number only once. 
  - The count variable ensures it will only happen once and prevent duplicates of the smallest number to be left out.


## Part 3: Reflections
>Within the course of two lab sessions I have learned many new skills. From creating web servers to using the desktop version of 
Github, each skill was a new source of knowledge to supplement the skills I have been learning in my other CSE classes. One skill 
that has really stuck out to me is the creation of web servers and dealing with requests. Being able to launch a server and run 
different methods and programs based off of the paths you dictate has been an interesting experience. Through the use of many 
methods in the Java language we can account for different instances and in turn create interesting results.
