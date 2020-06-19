#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
O(n)
It is a single while loop, and the time it takes increases by n because even though the loop runs until a < n^3, a increases by n^2 each iteration 


b)
O(n^2)
It is a while loop nested inside a for loop. For each iteration of the for loop (which will iterate n times), the while loop will also iterate n times


c)
O(n)
It is a recursive method that executes exactly as many times as "bunnies" is equal to
If bunnies is equal to 10, it will execute with a 10, then 9, then 8, and so on until it reaches 0

## Exercise II

For this example, assume the building has 100 stories

1. Find the half way point between the top and bottom of the building (so if it's a 100 story building, go to floor 50)
2. Throw an egg off the side
3. (case a) If it breaks, go down to the half way point between floor 50 and 0 (Floor 25)
3. (case b) If it doesn't break, go up to the half way point between floor 50 and 100
(Floor 75)
4. Repeat Steps 2 and 3 until the min floor and max floor are the same number
5. Return the point in which the min floor and max floor are equal

The runtime complexity would be O(log n) because the data set is split in half each time as it approaches the point of which the egg no longer breaks


the function would look something along the lines of this

def floorfind(height): 
    minfloor = 0
    maxfloor = height
    bestheight = 0
    locationfound = false:
    while not locationfound:
        if((throwEggFromFloor((maxfloor + minfloor) / 2) == False):
            minfloor = (maxfloor + minfloor) / 2
        if((throwEggFromFloor((maxfloor + minfloor) / 2) == True):
            maxfloor = (maxfloor + minfloor) / 2
        if(minfloor == maxfloor):
            bestheight = minfloor (or maxfloor, doesn't really matter)
    return bestfloor
            

def throwEggFromFloor(floorNum):
    this function throws the egg from the floor passed in as a parameter
    if it breaks, it returns True
    if it does not break, it returns False