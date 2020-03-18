# SDS348 Spring 2020

We will use this GitHub repository for any technical discussions regarding SDS 348 lectures, labs, and assignments.

To participate, you will need a [GitHub account.](https://github.com/) You can sign up for free, and you don't have to use your real name. We will not be tracking which students are or are not participating in discussions. This is simply meant as an optional resource to help you get your questions answered.

All discussion will happen in [GitHub issues.](https://github.com/clauswilke/SDS348_spring2020/issues) The most important thing you need to know is that there are two types of issues, [open issues](https://github.com/clauswilke/SDS348_spring2020/issues?q=is%3Aopen+is%3Aissue) and [closed issues](https://github.com/clauswilke/SDS348_spring2020/issues?q=is%3Aissue+is%3Aclosed). Open issues are issues that have not yet been resolved. For example, a student has asked a question but no answer exists yet. Closed issues are issues for which a resolution has been found. For example, the question has been satisfactorily answerd. Be aware that after a while there will be a lot of useful material in closed issues! When you have a specific question, first check whether there is a relevant issue already. If not, click on the green ["New Issue" button](https://github.com/clauswilke/SDS348_spring2020/issues/new) and post your question. Also, if you see an open issue you feel confident you can answer, please go ahead and do so.

## Asking questions about R

When entering questions or responses on GitHub, you can use Markdown, just like you are used to in RMarkdown. Code blocks are fenced off with three backticks. The only minor change is that the `r` after the backticks is not in curly braces. For example, to ask an R question, you might write the following:

    I am trying to add 2 to a variable holding the number 1, but I get an error. This is my code:
    
    ``` r
    x <- 1
    x + "2"
    ```
    This is the error I get: `Error in x + "2" : non-numeric argument to binary operator`

This question would be rendered as follows:

> I am trying to add 2 to a variable holding the number 1, but I get an error. This is my code:
>
> ``` r
> x <- 1
> x + "2"
> ```
> This is the error I get: `Error in x + "2" : non-numeric argument to binary operator`


## Asking questions about python

Questions regarding python work just the same as questions about R, only that you write `python` after the backticks instead of `r`: 

    I am trying to add 2 to a variable holding the number 1, but I get an error. This is my code:
    
    ``` python
    x <- 1
    x + "2"
    ```
    This is the error I get:
    
    ```
    ---------------------------------------------------------------------------
    TypeError                                 Traceback (most recent call last)
    <ipython-input-1-9fa35d97d9b9> in <module>
          1 x = 1
    ----> 2 x + "2"
    
    TypeError: unsupported operand type(s) for +: 'int' and 'str'
    ```

This question would be rendered as follows:

> I am trying to add 2 to a variable holding the number 1, but I get an error. This is my code:
>
> ``` python
> x <- 1
> x + "2"
> ```
> This is the error I get:
> 
> ```
> ---------------------------------------------------------------------------
> TypeError                                 Traceback (most recent call last)
> <ipython-input-1-9fa35d97d9b9> in <module>
>       1 x = 1
> ----> 2 x + "2"
> 
> TypeError: unsupported operand type(s) for +: 'int' and 'str'
> ```

## General advice about asking questions

Whenever you are asking questions, it is critical that you provide a **minimal** and **complete** example of your problem. The example needs to be as minimal as possible, and it should remove any code lines that aren't directly relevant. For example, if you are asking a question about making a plot, code lines that make the axes look nicer or pick a different color scale will generally be irrelevant unless your question is specifically about those issue. Remove those lines. A good example of a problem rarely needs more than 5-10 lines of code.

The example also needs to be complete. In other words, we need to be able to copy your code, as is, into a new R or python session and it must run. If the example is not complete we cannot figure out what exactly the problem is. I'll provide an example to help you understand. First a bad version:

> Q: I'm trying to plot the `iris` dataset with ggplot but it doesn't work. Here is what I do:
> ``` r
> iris %>%
>   ggplot(aes(Sepal.Length, Sepal.Width, color = Species)) +
>   geom_point()
> ```

We don't know how to answer this question, because the code looks correct. However, we are missing information. What libraries did the student use? What is the error the student sees? If we copy and paste the code as given above into a new R session, without loading any libraries, it won't run. (Try this out!) So this is not a complete example.

The complete example would look like this:

> Q: I'm trying to plot the `iris` dataset with ggplot but it doesn't work. Here is what I do:
> ``` r
> library(ggplot2)
> 
> iris %>%
>   ggplot(aes(Sepal.Length, Sepal.Width, color = Species)) +
>   geom_point()
> #> Error in iris %>% ggplot(aes(Sepal.Length, Sepal.Width, color = Species)): could not find function "%>%"
> ```

Now the student has provided the library they are using, and also the error message. We now see what the problem is: We cannot use `%>%` unless we have loaded the tidyverse library. With this issue figured out, we can provide an answer:

> A: You need to load the tidyverse library to use `%>%`.
> ``` r
> library(tidyverse)
> 
> iris %>%
>   ggplot(aes(Sepal.Length, Sepal.Width, color = Species)) +
>   geom_point()
> ```
> 
> ![](https://i.imgur.com/rP874U5.png)

Note that GitHub allows us to upload images, and this can be really helpful when a problem arises in a plot. **But please, do not upload images of your code.** We need to be able to copy and paste your code to figure out what the issue is.
