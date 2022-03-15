# Unit Testing 

### What Unit Testing Isn’t ?
-  Not every test you could conceivably write qualifies as a unit test.
-  Unit tests don’t deal with their environment and with external systems to the codebase.
-  Unit tests don’t generate random data and pepper your application with it in unpredictable sequences
-  Unit tests don’t exercise multiple components of your system and how they act.

### What Unit Testing Is ?
- Unit tests isolate and exercise specific units of your code
- used to take each unit in my code and test it separetly,to check if code is working as expected.

 ### Generate unit test project :
* From the code editor window, right-click and choose Create Unit Tests from the right-click menu.
* Click OK to accept the defaults to create your unit tests, or change the values used to create and name the unit test project and the unit tests

### Run Unit test:
- Go to test>>>>> test explorer
- select unit test name after that right click then run

### unit test life cycle
![img](./img/testCycle.png)
---
### Unit Testing Best Practices

1- Arrange, Act, Assert (AAA):

* Arrange: you need to organize the data needed to execute that piece of code (input)

* Act: execute the code being tested (exercise the behaviour)

* Assert: you will check if the result is the same as you were expecting.

2- One Assert Per Test Method.

3- Avoid Test Interdependence.

4- Keep It Short, Sweet, and Visible.

5- Recognize Test Setup Pain as a Smell.

6- Add them to the build

---
## Documentation
Good documentation matters. We use a README file for this purpose. Its job is to inform our users, other devs, or really anyone else who is interested in our product the WHAT, HOW, WHY and more about our product.

## A good README should:

1- Tell others WHAT our product is,
2- Show others what our product looks like in action,
3- Show them HOW to use it,
4- Fill in any other relevant details and information.
