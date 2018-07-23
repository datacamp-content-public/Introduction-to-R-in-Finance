---
title       : Simple plots
description : This chapter will cover how to create simple plots.
---
## Your first plot in R!

```yaml
type: NormalExercise
key: 82cd86ba50
lang: r
xp: 100
skills: 1
```

Now that you understand variables and data structures in R, it is time we started presenting information. Know the proverb *a picture says more than a thousand words*? Well, I agree. So let's start exploring R's capabilities when it comes to illustrating data.


`@instructions`
I have created a vector called `EvenNumbers`, which contains the values 0, 2, 4, 6, 8 and 10. Don't believe me? Type `EvenNumbers` to check!

You should now try to plot the contents of `EvenNumbers`. To do so, simply type `plot(EvenNumbers)` and see what happens!

`@hint`
First type `EvenNumbers`, then type `plot(EvenNumbers)`. Make sure you capitalize the E and the N in `EvenNumbers`. Then run your code!

`@pre_exercise_code`
```{r}
EvenNumbers<-seq(0,10,2)
```

`@sample_code`
```{r}
# First view the contents of EvenNumbers.


# Then use 'plot(EvenNumbers)' to graphically present the numbers in 'EvenNumbers'.

```

`@solution`
```{r}
EvenNumbers
plot(EvenNumbers)
```

`@sct`
```{r}
success_msg("Excellent, your first R plot! R has taken the contents of `EvenNumbers` and plotted it on the vertical axis, using a simple index (running from 1 to 6, for the six numbers in `EvenNumbers`) for the horizontal axis.

Now - despite this success, you are not happy with how the figure looks? Well, let's see about that in the next exercise ...")
```

---
## Plotting something more useful

```yaml
type: NormalExercise
key: 9476388da9
lang: r
xp: 100
skills: 1
```

Now that you have whet your appetite with a first plot, let's plot something nicer to look at than six simple numbers. How about that sine wave you learnt about in highschool? Let's try to plot that!

`@instructions`
First we need to create the *grid*, i.e., the x-coordinates over which we are going to plot our function. We are going to do this by creating a variable `x` which we will fill by numbers incrementing from zero to two times pi (yes, the same pi we use to calculate the area of a circle). Why two times pi? Because that will give us one full sine wave. We do this by assigning to `x` the numbers 0, 0.1, 0.2, etc.

Once that is done, we can define `y` as the sine of `x` and plot the outcome.

`@hint`
First, calculate and save in `y` the sine of `x` by assigning the outcome of `sin(x)` to `y`.

Then, plot the outcome using `plot(x,y)`.

`@pre_exercise_code`
```{r}

```

`@sample_code`
```{r}
# First we fill x by numbers running from 0 to two times pi in steps of 0.1.
x <- seq(from = 0, by = 0.1, to = 2 * pi)

# Then, we calculate y as the sine of `x`, using the built-in function `sin()`.


# Finally, we plot the result, sending both the x and the y variables to the `plot()` function. The first argument of the function (the first variable name there) will be interpreted as the x-coordinate, the second as the y-coordinate.

```

`@solution`
```{r}
x <- seq(from = 0, by = 0.1, to = 2 * pi)
y <- sin(x)
plot(x, y)
```

`@sct`
```{r}
success_msg("Good work! Your highschool teacher would be proud of you!")
```
