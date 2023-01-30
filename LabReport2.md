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

### Multiple methods are called 
- ```.getPath()```: retrieves the URL information and the current address
- ```.equals()```: checks the value of a string with (in this instance) the URL arguments
- ```.getQuery()```: looks for the **query** command, ```?```, and the information that follows it
- ```.split()```: finds the information after the designated value

### Method Usage




<img width="455" alt="Screen Shot 2023-01-30 at 3 05 41 PM" src="https://user-images.githubusercontent.com/83740546/215616813-fb82e8d1-9ebf-4899-93b9-32e53c69f69f.png"> <img width="486" alt="Screen Shot 2023-01-30 at 3 06 09 PM" src="https://user-images.githubusercontent.com/83740546/215616826-1bb75983-377a-42bd-82b9-dc198ef29a67.png">

## Part 2: Identifying Bugs

## Part 3: Reflections
