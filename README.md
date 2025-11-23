This is a modified version of coupon collector model it is to check how many times random deletion is required to delete a string.
it uses two libraries matplotlib and random.
The game is till we remove all character of the title.

Step 1: Random Character Selection
Randomly picks character: 'e'

Remove all 'e' occurrences: "th matrix"

Result: "th matrix" (1 iteration)

Step 2: Random Character Selection
Randomly picks character: 'x' (not in current string)

Remove all 'x' occurrences: "th matrix" (no change)

Result: "th matrix" (2 iterations - wasted turn!)

Step 3: Random Character Selection
Randomly picks character: 't'

Remove all 't' occurrences: "h marix"

Result: "h marix" (3 iterations)

Step 4: Random Character Selection
Randomly picks character: 'h'

Remove all 'h' occurrences: " marix"

Result: " marix" (4 iterations)

Step 5: Random Character Selection
Randomly picks character: ' ' (space)

Remove all space occurrences: "marix"

Result: "marix" (5 iterations)

Step 6: Random Character Selection
Randomly picks character: 'm'

Remove all 'm' occurrences: "arix"

Result: "arix" (6 iterations)

Step 7: Random Character Selection
Randomly picks character: 'a'

Remove all 'a' occurrences: "rix"

Result: "rix" (7 iterations)

Step 8: Random Character Selection
Randomly picks character: 'r'

Remove all 'r' occurrences: "ix"

Result: "ix" (8 iterations)

Step 9: Random Character Selection
Randomly picks character: 'i'

Remove all 'i' occurrences: "x"

Result: "x" (9 iterations)

Step 10: Random Character Selection
Randomly picks character: 'x'

Remove all 'x' occurrences: ""

Result: "" (10 iterations - DONE!)

In such way 10 random deletion are required to delete a complete string of movie title.

Discover which films are hardest to erase and uncover the hidden patterns in probabilistic text manipulation.
