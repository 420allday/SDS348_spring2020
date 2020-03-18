# SDS348 Spring 2020

We will use this GitHub repository for any technical discussions regarding SDS 348 lectures, labs, and assignments.

To participate, you will need a [GitHub account.](https://github.com/) You can sign up for free, and you don't have to use your real name. We will not be tracking which students are or are not participating in discussions. This is simply meant as an optional resource to help you get your questions answered.

All discussion will happen in [GitHub issues.](https://github.com/clauswilke/SDS348_spring2020/issues) The most important thing you need to know is that there are two types of issues, [open issues](https://github.com/clauswilke/SDS348_spring2020/issues?q=is%3Aopen+is%3Aissue) and [closed issues](https://github.com/clauswilke/SDS348_spring2020/issues?q=is%3Aissue+is%3Aclosed). Open issues are issues that have not yet been resolved. For example, a student has asked a question but no answer exists yet. Closed issues are issues for which a resolution has been found. For example, the question has been satisfactorily answerd. Be aware that after a while there will be a lot of useful material in closed issues! When you have a specific question, first check whether there is a relevant issue already. If not, click on the green ["New Issue" button](https://github.com/clauswilke/SDS348_spring2020/issues/new) and post your question.

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
    
    ``` python
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
> ``` python
> ---------------------------------------------------------------------------
> TypeError                                 Traceback (most recent call last)
> <ipython-input-1-9fa35d97d9b9> in <module>
>       1 x = 1
> ----> 2 x + "2"
> 
> TypeError: unsupported operand type(s) for +: 'int' and 'str'
> ```
