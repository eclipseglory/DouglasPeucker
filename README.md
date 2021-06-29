# Douglas-Peucker algorithm
The Ramer–Douglas–Peucker algorithm implemented by JavaScript. 

The purpose of the algorithm is, given a curve composed of line segments (which is also called a Polyline in some contexts), to find a similar curve with fewer points. The algorithm defines 'dissimilar' based on the maximum distance between the original curve and the simplified curve (i.e., the Hausdorff distance between the curves). The simplified curve consists of a subset of the points that defined the original curve.

# Install
Download the ```douglas-peucker.js``` file and add it into your projects.
# Example
https://eclipseglory.github.io/rdp/

# How to use
In your js code , import the ```douglasPeucker``` method from the library file you downloaded:
```javascript
import { douglasPeucker} from 'SOME_PATH/douglas-peucker.js';
...

    // The curve points array
    let points = [.....];

    let epsilon = 20;

    // caculate and get the new points
    let newPoints = douglasPeucker(points, epsilon); 

...
```

## Method parameters
```javascript
function douglasPeucker(points, epsilon, start, end)
```
- ```points``` (*required*) : The curve points array. The array item is ```[x,y]``` array format, for example : 
```
    points = [[0,0],[100,100]....[200,200]];
```

- ```epsilon``` (*option*) : Default value is ```10```. It means the min distance between a point project to a line segment.
- ```start``` (*option*) : The start index of the ```points``` array. If it's ```null``` , it will be assigned to ```0```.
- ```end``` (*option*) : The end index of the ```points``` array. If it's ```null``` , it will be assigned to ```points.length-1```.