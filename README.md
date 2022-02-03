# Mars Rover kata
Mars Rover kata using UML, TDD, Java
### Design
UML Class Diagram
### Commands to explore Mars
All rovers need a plateau to land on, currently only rectangular shaped plateaus are supported.
#### Create a plateau 
Enter the maximum x and y coordinates of the plateau, e.g.
Creates a 10x10 square with 0,0 coordinate at the bottom left-hand corner On successful creation a plateau id will be returned. Multiple plateaus can be created. Maximum size for a Quad Plateau is 9999999,9999999
#### Create a rover
To create a rover on the current plateau specify its x and y coordinates and heading, e.g. 0 0 N
Creates a rover on the current plateau at coordinates 3,5 with a heading of North Direction.
Plateaus can support multiple rovers.
#### Move and Spin commands 
Rover move and spin commends are available to enable exploring:
spin left, e.g. if current heading is North, new heading is East
spin right
move one grid position in the direction of the current heading
A single command can contain multiple move and spin instructions, e.g. LLMMMRMMM
#### Other commands
SWITCH PLATEAU 
SWITCH ROVER 
LIST PLATEAUS
LIST ROVERS
SHOW MAP
HIDE MAP
FINISH
HELP
On exit a report of all rover positions is produced.

### Move logic
Rovers cannot land on or move to the space as another Rover on the same plateau.  
On receipt of a move command the rover calculates its new coordinates and validates the move with the plateau.
The plateau check the coordinates are within bounds and the position of any other rovers. Two rovers cannot share the same coordinates
 ### Running the application
The application can run using manual input from the command line or a file containing instructions can be passed as a parameter.
Example instruction files are available in the test data folder.
### Future enhancements
Different shaped plateaus
Flying Rover
Additional Capcoms

