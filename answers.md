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
1.
| °   | Direction |
|-----|-----------|
| 0   | North     |
| 45  | Northeast |
| 90  | East      |
| 135 | Southeast |
| 180 | South     |
| 225 | Southwest |
| 270 | West      |
| 315 | Northwest |
| 360 | North     |
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