# Part 1

## Questions
1. The bug does not always move with each step. If its front is clear it will move but if it isn't it will turn.
2. The bug will always move forward.
3. It turns right 45° .
4. It leaves behind flowers.
5. If it is facing the edge it will turn untill its face is clear then it will move. The edge is treated as an obstacle.
6. Anytime the bug encounters an obstacle it will turn 45° untill the obstacle is no longer in front of the bug.
7. A flower does not move.
8. A flower gets darker every step following its creation.
9. A rock just acts as an obstacle. It does not move nor rotate nor change color.
10. More than one actor cannot be in the same location.

## Exercises
|°|Direction|
|:---:|:---:|
|0|North|
|45|Northeast|
|90|East|
|135|Southeast|
|180|South|
|225|Southwest|
|270|West|
|315|Northwest|
|360|North|
2. You can move the bug any legal place, neither the direction nor the distance matter. If you try to move the bug outside of the grid, an invalid location error is thrown.
3. To change the color of an actor, the setColor() method is used.
4. The bug is destroyed.

# Part 2


## Questions
1. The instance variable sideLength determines the size of the box the bug creates.
2. The instance variable steps tells the bug when to start its turn
3. The turn method only turns a bug 45°. The bug must turn 90° so the method must be called twice.
4. The BoxBug class inherits from the Bug class so it is guaranteed to have the classes availible to the Bug class.
5. The BoxBug's sideLength variable will not change after construction.
6. The BoxBug will turn and begin a new square of the same size once its front is clear.
7. The value of steps will be zero after each turn.

## Exercises
1. It turns 45° after the steps is equal to the sideLength instead of 90°. It makes a oxagon.
5. To create a new BoxBug called Jimmy it should be initialized in the runner. If initialized in this way, jimmy will be blue in color and start near the top left corner.
```java
BoxBug jimmy = new BoxBug();
jimmy.setColor(Color.BLUE);
world.add(new Location(1, 1), jimmy);
```

# Part 3

## Questions

### Set 3
1. To get the row: public int firstRow = getRow(loc1)
2. The locations are not the same so the boolean's value will be false
3. Loc3 will be at (4, 4)
4. dir will be 135
5. The method takes in a direction. It will place the new actor one space away from the original actor, in the direction given

### Set 4
1. You can make a for loop that starts on the second row and uses the Arraylist method getNeighbors(Location loc), repeating this for every third line. This will use he fewest amount of check. In order to ensure everything is checked, you must make it check the second to last line in every grid
2. The method isValid(10, 10) will return true if the location is exists and false if it doesn't
3. The Grid class is an interface so it just contains a list of methods. The methods are contained in the Bounded and Unbounded classes.
4. The ArrayList is a better choice as its length can be altered while an Array's length cannot

### Set 5
1. Every actor has a color, location, and direction
2. Default direction is north and default color is red
3. Actor needs to be a class and not an interface because it needs to have methods
4. An actor cannot be in two places at once. It only has one location. Therefore it must remove itself before it can replace itself. It also cannot remove itself twice either. An acor can place and remove itself
5. The actor must turn twice in order to turn 90° to the right

### Set 6
1. It checks to see if the next spot is null (filled) 
``` java
if (gr == nul) {
    return false;
}
```
2. It checks to see if the next spot exists
``` java
if (!gr.isValid(next)) {
    return false;
}
```
3. The canMove() method must use the isValid method from the grid interface in order to work
4. The canMove() method uses the getAdjacentLocation() method in order to know what spot to check for validity
5. The methods getGrid() and getLocation()
6. The method will return false if the next location is out of the grid or filled by something due to the canMove() method.
7. It is possible to use the getLocation() method exclusively but it would not be as efficient as using the loc variable
8. Both the bug and the flower it drops inherrit from the same place
9. It will place a flower after it has been removed from the grid. Both happen in the move() method
10. This is how a bug places a flower
``` java
Flower flower = new Flower(getColor());
flower.putSelfInGrid(gr, loc);
```
11. To turn 180° it will have to call the turn() method 4 times

# Part 4

## Questions

### Set 7
