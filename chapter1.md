---
title       : Demo QW
description : Insert the chapter description here
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf


--- type:NormalExercise lang:python xp:100 skills:1 key:5bb5a77088
## Plot the movies yourself

Do you remember the plot of the last exercise? Let's make an even cooler plot!

A dataset of movies, `movies`, is available in the workspace.

*** =instructions
- The first function, `np.unique()`, uses the `unique()` function of the `numpy` package to get integer values for the movie genres. You don't have to change this code, just have a look!
- Import `pyplot` in the `matplotlib` package. Set an alias for this import: `plt`.
- Use `plt.scatter()` to plot `movies.runtime` onto the x-axis, `movies.rating` onto the y-axis and use `ints` for the color of the dots. You should use the first and second positional argument, and the `c` keyword.
- Show the plot using `plt.show()`.

*** =hint
- You don't have to program anything for the first instruction, just take a look at the first line of code.
- Use `import ___ as ___` to import `matplotlib.pyplot` as `plt`.
- Use `plt.scatter(___, ___, c = ___)` for the third instruction.
- You'll always have to type in `plt.show()` to show the plot you created.

*** =pre_exercise_code
```{python}
def harmonic_time_independent(x,n,L):
    amplitude = sin(n*pi*x / numpy.double(L))
    return amplitude

def harmonic_time_dependent(t,nu,n,L):
    amplitude = cos(pi*nu*n*t / numpy.double(L))
    return amplitude
```

*** =sample_code
```{python}
from matplotlib import pyplot as plt
import numpy

#Wave parameters
L = 10 #length of  (should we specify this?)
n = 1 #normal mode
x = numpy.linspace(0,10,1000) #Vector of position values
wave = harmonic_time_independent(x,n,L) #Get the time_independent solution

#PLOT
plt.plot(x, wave)
plt.xlabel('position')
plt.ylabel('Amplitude')
plt.title('First Harmonic at t = 0')
```

*** =solution
```{python}
from matplotlib import pyplot as plt
import numpy

#Wave parameters
L = 10 #length of  (should we specify this?)
n = 1 #normal mode
x = numpy.linspace(0,10,1000) #Vector of position values
wave = harmonic_time_independent(x,n,L) #Get the time_independent solution

#PLOT
plt.plot(x, wave)
plt.xlabel('position')
plt.ylabel('Amplitude')
plt.title('First Harmonic at t = 0')
```

*** =sct
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki



success_msg("Great work!")
```
