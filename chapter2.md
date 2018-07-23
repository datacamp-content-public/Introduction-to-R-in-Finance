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
## Plotting a sine wave

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

---
## Changing plot format and adding labels

```yaml
type: NormalExercise
key: '4429362060'
lang: r
xp: 100
skills: 1
```

While it is nice to see that sine function plot, nobody plots continuous functions using separate dots. Let's use a continuous line instead, why don't we? And while we're at it, we should add a title and particularly axis labels to your plot - remember how your highschool teacher used to nag you about those?

`@instructions`
To change the appeareance of a plot, we can add *options* to the plot function call. These are additional parameters, telling R how to format the plot output.

Let's start by telling R to format your data as a line instead of as individual dots. You do this by specifying the `type` parameter as `type="l"`. Note that this is a lower case "L" in the quotes, not the number "one". I have already prepared this for you in the script window. Put your cursor into the first line of code and hit <CTRL>-<ENTER> to run this piece of code.

Once you have done this, add a figure title and axis labels to your plot using the options `main`, `xlab` and `ylab`.

`@hint`
You can add the title and axis label options by using the argument name and assigning it a value. For the plot title, this would look as follows: `main="Sine wave"`.

`@pre_exercise_code`
```{r}
x <- seq(from = 0, by = 0.1, to = 2 * pi)
y <- sin(x)
```

`@sample_code`
```{r}
plot(x, y, type = "l") #Plots y over x as a line graph

# Now add a main title "Sine wave", an x-axis label "X" and a y-axis label "sin(X)" to your plot. Complete the following line of code (don't forget to close the brackets!):
plot(x, y, type = "l", 

```

`@solution`
```{r}
plot(x, y, type = "l")
plot(x, y, type = "l", main = "Sine wave", xlab = "X", ylab = "sin(X)")
```

`@sct`
```{r}
success_msg("Very nice - this looks like a proper graph of a sine wave!")
```

---
## Colored and more pronounced lines

```yaml
type: NormalExercise
key: c740f8f7a3
lang: r
xp: 100
skills: 1
```

In the exercise after this one, we will add another plot to our graph. If we do so and again use a black, thin line, it will be hard to distinguish the two plots. So before we add another plot, let's make the sine wave a bit more distinctive by making it thicker and assigning it a color.

`@instructions`
R offers a number of different ways to specify colors. One of them is simply to use one of several pre-defined color names. By assigning a color to our line (in this case "red"), we can cause it to turn red. The relevant parameter in the `plot` function is `col`.

Furthermore, we can specify the parameter `lwd` to assign a line width to our sine function plot to make it somewhat bolder and more distinctive. The default width is 1. How about setting it to 4 instead?

`@hint`
Using `col="blue"` makes the line turn blue, while `lwd=2` sets the line's width to 2. Can you now make the line red and width 4?

`@pre_exercise_code`
```{r}
x <- seq(from = 0, by = 0.1, to = 2 * pi)
y <- sin(x)
```

`@sample_code`
```{r}
#Modify the plot function call to plot the line in red and test it by selecting the below line and pressing <CTRL>-<ENTER>
plot(x, y, type = "l", main = "Sine wave", xlab = "X", ylab = "sin(X)")

#Modify the plot function call from above to also make the line width equal 4


```

`@solution`
```{r}
plot(x, y, type = "l", main = "Sine wave", xlab = "X", ylab = "sin(X)", col="red")
plot(x, y, type = "l", main = "Sine wave", xlab = "X", ylab = "sin(X)", col="red", lwd=4)
```

`@sct`
```{r}
success_msg("Excellent, this looks beautiful!")
```

---
## Adding a cosine plot

```yaml
type: NormalExercise
key: c11a2c1e90
lang: r
xp: 100
skills: 1
```

In the exercise after this one, we will add another plot to our graph. If we do so and again use a black, thin line, it will be hard to distinguish the two plots. So before we add another plot, let's make the sine wave a bit more distinctive by making it thicker and assigning it a color.

`@instructions`
R offers a number of different ways to specify colors. One of them is simply to use one of several pre-defined color names. By assigning a color to our line (in this case "red"), we can cause it to turn red. The relevant parameter in the `plot` function is `col`.

Furthermore, we can specify the parameter `lwd` to assign a line width to our sine function plot to make it somewhat bolder and more distinctive. The default width is 1. How about setting it to 4 instead?

`@hint`
Using `col="blue"` makes the line turn blue, while `lwd=2` sets the line's width to 2. Can you now make the line red and width 4?

`@pre_exercise_code`
```{r}
x <- seq(from = 0, by = 0.1, to = 2 * pi)
y <- sin(x)
```

`@sample_code`
```{r}
#Modify the plot function call to plot the line in red and test it by selecting the below line and pressing <CTRL>-<ENTER>
plot(x, y, type = "l", main = "Sine wave", xlab = "X", ylab = "sin(X)")

#Modify the plot function call from above to also make the line width equal 4


```

`@solution`
```{r}
plot(x, y, type = "l", main = "Sine wave", xlab = "X", ylab = "sin(X)", col="red")
plot(x, y, type = "l", main = "Sine wave", xlab = "X", ylab = "sin(X)", col="red", lwd=4)
```

`@sct`
```{r}
success_msg("Excellent, this looks beautiful!")
```
