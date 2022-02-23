# Math-for-DS
import numpy as np
import scipy as sp
import sympy as smp
from scipy.misc import derivative

def grad(a,b):
    x,y = smp.symbols('x y', real=True )
    f = (x ** 2) * y - x * (y**2 )
    dfdx = (2*(x**(2-1)*y) - (x**(1-1))*(y**2))
    dfdy = ((x**2)*(y**(1-1)) - (2*x*y))
    res=dfdx.subs(x,a).subs(y,b)
    res1=dfdy.subs(x,a).subs(y,b)
    return res,res1
    
    #when function call occurs as below
    grad(2,3)
    # gives output as
    (3,-8)
