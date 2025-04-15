Campus Navigation System
=========================

Project Name: Campus Navigation System

Developers:
1. Muhammad Saad Tahir
2. Fasih Ahmed
3. Umer Kamran

----------------------------------------

Description:
------------
This program is a Campus Navigation System designed to help users find directions between different locations within a university campus. It provides step-by-step instructions to navigate from a starting point to a desired destination. The system includes predefined locations (e.g., EE Building, Library, Cafeteria, Gym, etc.) and directional paths between them.

Key Features:
-------------
1. Location Database:
   - Contains a list of 20 predefined campus locations stored in a 2D array.
   - Examples:
     - EE Building
     - Library
     - Cafeteria
     - Sports Room
     - Main Gate

2. Directional Mapping:
   - Uses a 2D array (directions matrix) to store navigation instructions between every pair of locations.
   - Each entry contains a detailed textual description of the path from one location to another.

3. User Interaction:
   - Displays a list of available locations for the user to choose from.
   - Asks the user to input:
     - Current Location (starting point)
     - Desired Destination (end point)
   - Provides step-by-step directions if a valid path exists.

4. Case-Insensitive Matching:
   - Uses strcasecmp() to ensure the user's input matches location names regardless of letter case.

5. Error Handling:
   - Checks if the entered locations are valid.
   - Displays an error message if no direct path exists.

----------------------------------------

How It Works:
-------------
1. Initialization:
   - Defines an array of campus locations.
   - Dynamically allocates memory for a directions matrix (20x20).
   - Populates the matrix with pre-written navigation instructions.

2. User Input:
   - Prints available locations.
   - Takes user input for current location and destination.

3. Navigation Logic:
   - Uses find_location_index() to convert location names into matrix indices.
   - Retrieves and prints the corresponding directions from the matrix.

4. Cleanup:
   - Frees dynamically allocated memory to prevent memory leaks.

----------------------------------------

Example Usage:
--------------
Input:
  Current Location: EE Building
  Desired Location: Library

Output:
  Directions from EE Building to Library:
  Come to Main Entrance of EE building.
  From Main Entrance Move Straight 30 feet.
  You will pass by fountain and cross walkpath.
  Enter CS Building from gate in front of you.
  Walk straight to reach other end of CS building.
  Turn Right and move 10 feet.
  Turn Left and Enter Multi Purpose Building.
  Walk Straight 15 feet and move downstairs.
  You have reached Library.

----------------------------------------

Technical Details:
------------------
- Data Structures:
  - 2D arrays for locations and directions.
  - Dynamic memory allocation for the directions matrix.

- Functions:
  - find_location_index(): Finds the index of a location in the array.
  - navigate(): Retrieves and prints navigation instructions.

- Limitations:
  - Only supports direct paths (no intermediate waypoints).
  - Directions are hardcoded (no dynamic pathfinding algorithm).

----------------------------------------

Summary:
--------
This Campus Navigation System is a C program that helps users find their way around a university campus by providing pre-defined directions between key locations. It was collaboratively developed by Saad Tahir, Fasih Ahmed, and Umer Kamran and serves as a useful tool for students, faculty, and visitors navigating the campus.

Potential Improvements:
-----------------------
- Implement graph-based pathfinding (e.g., Dijkstra’s algorithm) for dynamic route calculation.
- Add GPS-based tracking for real-time navigation.
- Use file I/O to load locations and directions instead of hardcoding them.
