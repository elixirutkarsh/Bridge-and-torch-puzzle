# Bridge-and-torch-puzzle
The Bridge and Torch problem is a classic logic puzzle that involves a group of people trying to cross a bridge at night. The bridge can only support a certain weight at a time, and the group has only one torch to navigate in the dark. The puzzle is to find the minimum amount of time required for the entire group to cross the bridge.

Here is one possible solution to the Bridge and Torch problem using a recursive algorithm:

Define a function crossBridge that takes the following parameters:

times: A list of times required for each person to cross the bridge.
currentSide: A list representing the current side of the bridge, where 1 represents the starting side and 0 represents the ending side.
timeElapsed: The total time elapsed so far.
minTime: A list to store the minimum time found.
Base case:

If there are no people remaining on the starting side (all elements in currentSide are 0), update minTime if timeElapsed is less than the current minimum time.
Recursive case:

Iterate through all possible pairs of people to send across the bridge.
For each pair, calculate the time it takes for the slower person to cross.
Recursively call crossBridge with the updated state (moving the people across the bridge) and the updated time.
After the recursive call, restore the original state by moving the people back to the starting side.
Call the crossBridge function with the initial parameters: times, a list of 1 representing the starting side, 0 representing the ending side, initial timeElapsed as 0, and an initial minTime set to a large value.

Return the minimum time found stored in minTime.
