# GreatCircleFit
Python function for fitting a great circle to data points in 3D space.

## What is a great circle?
Basically it is the shotest path which connects two points on a sphere. Let's say you are flying your own plane from London to New York and you want to take the shortest path, and thus use as little fuel as possible (for some reason you can afford the plane, but not the fuel. Ok, let's say you are an ecologically conscious billionare, we'll leave it at that). The best bet to do that is to fit a great circle between these two cities and follow the path you get.

## How can I use this code?
Make sure you have these libraires installed, and you are good to go:
- Numpy
- Matplotlib
- Scipy

## Hey, this is cool, how does it work?
The code first fits a plane though you data points (NOTE: to successfuly fit a plane, you need at least 3 data points), then calculates the 'pitch' and the 'roll' of the fitted plane. Then you can use those two angles for the great circle which we have parametrically defined.

## Something's wrong, my fits are failing!
One of the assumptions I have made is that the radius of the circle is always R = 1, and it is always centered at C=(0, 0, 0). With this I have simplified the model, as I was fitting angular data (which you can easily transform to [Cartesian coordinates](https://en.wikipedia.org/wiki/Spherical_coordinate_system#Cartesian_coordinates)), so I could make those assumptions. If you want to fit the radius and the centre of the great circle, you will need to modify the greatCircle funtion to take those parameters into account (take a look at parametrically defining a [circle in 3D](http://demonstrations.wolfram.com/ParametricEquationOfACircleIn3D/)).

## References
Curt F. Marcus, "A note on fitting great circles by least squares", Communications of the ACM, Volume 4 Issue 8, Aug. 1961, Page 353
