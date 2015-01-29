HOMEWORK 0: TRANSFORMATIONS & OPENGL WARMUP


NAME:  david allen


TOTAL TIME SPENT:  8.5 hours
Please estimate the number of hours you spent on this assignment.

20150128 — 14:00–16:00 — read all provided files, formatted some for legibility
20150128 — 16:00–18:00 — declared properties in "ifs.h", wrote intial code pass in "ifs.cpp"
20150128 — 19:30–20:30 — tested initial code (compiled and ran, but iteration of transformations was still a bit off)
20150128 - 23:15–23:40 — made it work with points (still need to figure out cubes)
20150128 - 23:40–02:40 — wrote recursive cube function
----
8.5 hours so far
----
TODO: finish gradesheet? (See Barb or TA for assistance)


COLLABORATORS AND OTHER RESOURCES: List the names of everyone you
talked to about this assignment and all of the resources (books,
online reference material, etc.) you consulted in completing this
assignment.

- http://www.cs.rpi.edu/~cutler/classes/advancedgraphics/S15/hw0_opengl.php
- http://stackoverflow.com/questions/12885356/random-numbers-with-different-probabilities

Remember: Your implementation for this assignment must be done on your
own, as described in "Academic Integrity for Homework" handout.



OVERALL PERFORMANCE

1) Rendering points seems relatively fast. I was able to create and manipulate 100000 points with 90 iterations for the fern IFL in approximately 3 seconds. Rendering them seems completely interactive as well without any noticeable frame drop when rotating the canvas around.

2) Drawing cubes for the same number of iteractions, on the other hand, made my computer unresponsive just in the loading and setup of the application. Displaying cubes for any of the IFS's approaching or exceeting 10 iteractions or so started to take considerably longer to load, and dropped frames when rotating the canvas around. Approaching 30 iterations simply made the application unresponsive for longer than the several minutes I waited for './ifs -input ../src/sierpinski_triangle.txt -points 10000 -iters 30 -size 200 -cubes' to finish loading. I can only imagine that the interactivity would have dropped even further had it finally loaded.



KNOWN BUGS IN YOUR CODE:
1) There might even be some stack overflow going on for higher cube recursions — should probably be capped at some reasonable number.

2) Would be nice to have it error out after a considerable amount of time has passed, or to at least have some kind of progress metering. 

NEW FEATURES OR EXTENSIONS FOR EXTRA CREDIT:
Include instructions for use and test cases and sample output as appropriate.

1) I implemented a version of Menger's Cube './ifs -input ../src/menger_cube.txt -points 100000 -iters 4 -size 1000 -cubes'
