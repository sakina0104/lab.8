import math
def f(x):
    return x + math.log(x) - 0.5
a = 0.1  
b = 1.0
eps = 1e-6  

if f(a) * f(b) > 0:
    print("Bu intervallarda kök yoxdur.")
else:
    while (b - a) / 2 > eps:
        c = (a + b) / 2
        if f(c) == 0:
            break
        elif f(a) * f(c) < 0:
            b = c
        else:
            a = c
    print("Təqribi kök:", (a + b) / 2)
