# **Lab Report 5** <br />
Margaret Jones <br />
Monday 4PM - 6PM <br />

# Part 1 - Debugging Scenario

## 1. Original student Edstem post
* Student message:
```
"I am getting an error from running the testReversed2(ArrayTests) against my "reversed" method. The test
should says that the method should take the array {5, 10} and reverse it to {10, 5}. The **symptom** is that the test expects 5 but gets 10 which means that the method is incorrectly returning the array {10, 10}. I think that the method is somehow stuck on adding the same index of the old array into the new array I just am unsure where this is happening in the code. I believe it is either the for loop or the body of the for loop. Below, I have attached a screenshot of the symptom. Is there a suggested way for me to solve this bug?"
```
![Image](symptom.png)


## 2. A response from a TA asking a leading question or suggesting a command to try
* TA message:
```
"Hello, thank you for your question. I would first try a couple larger examples to further determine the pattern. A lot of times this helps give context to examples that are particularly small like the array, {5, 10}. I believe that part of your hypothesis is correct. Think about which part (the for loop or the body of the for loop) is the part that actually assigns the values to the newArray to be returned. These two parts of the for loop should be incrementing by i each iteration."
```

## 3. Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.





# Part 2 - Reflection
Learning about jdb was my favorite topic that we learned about in the last half of the quarter because of the ability to stop at a 
certain line in a program and step through each part of the code until you are able to decipher the error. The error we got in lab 
didn't tell us enough about what was going on with the code, but setting a breakpoint and checking the local variables at the 
part of the function we thought was recursive helped us find the bug easily. 

