# hw6

```html
<import pylab #из модуля pylab
import numpy
def makeData():
    x = numpy.arange(-1, 1, 0.005)
    y = numpy.arange(-1, 1, 0.005)
    xgrid, ygrid = numpy.meshgrid(x, y)

    zgrid = (1-xgrid)**2 + 100*(ygrid-xgrid**2)**2 
    return xgrid, ygrid, zgrid
if __name__ == '__main__':
    x, y, z = makeData()
    pylab.contour(x, y, z)#функция, которая строит линии уровня 

    pylab.show()
>
```
```html
<import pylab
from mpl_toolkits.mplot3d import Axes3D
import numpy

def makeData():
    x = numpy.arange(-10, 10, 0.05)
    y = numpy.arange(-10, 10, 0.05)
    xgrid, ygrid = numpy.meshgrid(x, y)

    zgrid = (1-xgrid)**2 + 100*(ygrid-xgrid**2)**2  
    return xgrid, ygrid, zgrid

if __name__ == '__main__':
    x, y, z = makeData()

    fig = pylab.figure()
    axes = Axes3D(fig)

    axes.plot_surface(x, y, z)

    pylab.show()
>
```
```html    
    from scipy import optimize
import numpy

def f(x):
    return (1-x[0])**2 + 100*(x[1]-x[0]**2)**2 
result = optimize.brute(f,((-5, 5),(-5, 5)))
print (result)
[1.00001563 1.00003185]
>
```
```html    
<import pylab
import numpy


def makeData():
    x = numpy.arange(-10, 10, 0.05)
    y = numpy.arange(-10, 10, 0.05)
    xgrid, ygrid = numpy.meshgrid(x, y)

    zgrid = ((1+numpy.sin(xgrid)) *(1+ numpy.sin(ygrid)))
    return xgrid, ygrid, zgrid


if __name__ == '__main__':
    x, y, z = makeData()
    pylab.contour(x, y, z)

    pylab.show()
        >
    ```
    
 ```html
    <import pylab
from mpl_toolkits.mplot3d import Axes3D
import numpy


def makeData():
    x = numpy.arange(-10, 10, 0.05)
    y = numpy.arange(-10, 10, 0.05)
    xgrid, ygrid = numpy.meshgrid(x, y)

    zgrid = ((1+numpy.sin(xgrid)) *(1+ numpy.sin(ygrid)))
    return xgrid, ygrid, zgrid


if __name__ == '__main__':
    x, y, z = makeData()

    fig = pylab.figure()
    axes = Axes3D(fig)

    axes.plot_surface(x, y, z)

    pylab.show()
            >
    ```
    from scipy import optimize
import numpy

def f(x):
    return ((1+numpy.sin(x[0])) *(1+ numpy.sin(x[1])))
result = optimize.brute(f,((0, 2.5),(0, 2.5)))
print (result)
[ 0.24661217 -1.5707872 ]


    
