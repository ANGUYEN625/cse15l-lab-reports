# Lab Report 4

## Links:

[Link to my Repo](https://github.com/ANGUYEN625/markdown-parser)

[Link to Reviewed Repo](https://github.com/JasonMorris1/markdown-parser)

## My `markdown-parse`:

**Tests**
![Image](./Screenshot%20(1069).png)

**Output:**
![Image](./Screenshot%20(1071).png)

Snippet 1: failed

* I think that for this code, there would need to be a more involved change due to the fact that code blocks are now being factored in. Since code blocks have an entirely spearate function from links, it has to be accounted for in the code as well.

Snippet 2: failed

* We can add a condition to check if there is an open parentheses after a closed bracket in order to make sure that is where the brackets end and the parentheses containing the link can start. That way, it won't just end at any other closed bracket.

Snippet 3: failed

* We can add a condition where is the 

## Reviewed `markdown-parse`:

**Tests**
![Image](./Screenshot%20(1072).png)

**Output:**
![Image](./Screenshot%20(1073).png)

Snippet 1: failed

* I also think that the code needs a more involved change since, like my code, it does not account for code blocks which are indicated by the backticks (`). We would have to add more conditions for code blocks.

Snippet 2: failed

* It could 

Snippet 3: failed

