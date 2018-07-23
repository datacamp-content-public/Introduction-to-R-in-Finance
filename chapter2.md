---
title       : Simple plots
description : This chapter will cover how to create simple plots.
---
## Your first plot in R!

# Test

```yaml
type: NormalExercise
key: 82cd86ba50
lang: r
xp: 100
skills: 1
```


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
success_msg("Excellent, your first R plot! Despite this success, you are not happy with how the figure looks? Well, let's see about that in the next exercise ...")
```
