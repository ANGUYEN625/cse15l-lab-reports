# Lab Report 5

## Test 1

![Image](./Screenshot%20(1075).png)

![Image](./Screenshot%20(1076).png)

I used `vimdiff` to find these. I think the provided repository is the correct answer because the preview shows that a link is provided and it is indicated in the test for it when there is a link added to the link list. My code is incorrect probably due to the fact that it confuses the end of link due to there being multiple closing parentheses. So i think our implementation needs a similar "findcloseParen" method that finds the correct closing parentheses, allowing the link to be correctly recognized. The method should be called and set to the closeParen variable: 

![Image](./Screenshot%20(1077).png)

## Test 2

![Image](./Screenshot%20(1078).png)

![Image](./Screenshot%20(1079).png)

I used `vimdiff` to find these. I think the provided repository is the correct answer since it clearly shows that a link was added to the list and the preview indicates that the format counts as a link. My code is incorrect due to it not accounting for when there is a new line in the file. Therefore, I would have to add a piece of code that would account for new lines. I would add something like this to my code:

![Image](./Screenshot%20(1080).png)

And it woudl probably be at the end of the method definition.

