# TuffyTravel Milestone 4

This is milestone 4 of the [TuffyTravel Project](https://docs.google.com/document/d/1v1ZAH-vt8ih500WFyDb_j5PO2L3_XS4_3CswPRJ5qNE/edit?usp=sharing).

# Requirements
Update your menu to add a new functionality to find a route given the time a user wishes to leave.

First, create a function called `get_time_to_leave` that does not accept any parameters. It will ask the user to provide the time they wish to leave. The function will return the time that the user provided.

Second, create a function called `find_route` that accepts three parameters. The array of `Route` objects, the number of elements in the array, and the time the user wishes to leave. The function should search through the array of available routes to find the earliest `Route` that leaves on or after the user's preferred time to leave. The function will then display the information about the `Route` that satisfies the user's search (possibly by using its `display` function).

Take note that the program should display appropriate error messages when there are no `Routes` in the array and if there is no `Route` that accommodates the user's time to leave. For example:

##### No routes created yet
```
Sorry, there are no routes available.
```
##### No routes matched the user's expected time to leave
```
Sorry, there is no route that leaves on or after the time you plan to leave.
```

This functionality is similar to what you did for Milestone 1, but its implementation should now be able to handle any number of routes stored in the array.

Finally, modify your menu to add a new option to find routes. When the user types in **F** the program should use the `get_time_to_leave` function to ask the user for the time they wish to leave, then pass all necessary arguments to the `find_route` function that will display the best route for the user.

All previous functionalities of the program should still work after adding this new feature.

The code should be organized so that class and function prototypes are placed in a header file (`route.hpp`) while their implementations are placed in a source file (`route.cpp`). Finally, the *main* method should be in the driver file (`tuffytravel.cpp`).

Please see the sample output below to guide the design of your program.

# Sample output
<pre>
Welcome to TuffyTravel!

What do you want to do? 
R - Create routes
D - Display routes
X - Exit
Action: <b>R</b>

Please enter the name of the route: <b>57x Brea Mall Xpress</b>
Please enter the departure time of the route: <b>1623</b>
Please enter the arrival time of the route: <b>1637</b>

What do you want to do? 
R - Create routes
D - Display routes
X - Exit
Action: <b>R</b>

Please enter the name of the route: <b>153 Brea Mall</b>
Please enter the departure time of the route: <b>1642</b>
Please enter the arrival time of the route: <b>1703</b>

What do you want to do? 
R - Create routes
D - Display routes
X - Exit
Action: <b>R</b>

Please enter the name of the route: <b>57x Brea Mall Xpress</b>
Please enter the departure time of the route: <b>1648</b>
Please enter the arrival time of the route: <b>1702</b>

What do you want to do? 
R - Create routes
D - Display routes
X - Exit
Action: <b>D</b>

Available Routes:

Route: 57x Brea Mall Xpress
Departure time: 1623
Arrival time: 1637

Route: 153 Brea Mall
Departure time: 1642
Arrival time: 1703

Route: 57x Brea Mall Xpress
Departure time: 1648
Arrival time: 1702


What do you want to do? 
R - Create routes
D - Display routes
F - Find route
X - Exit
Action: <b>F</b>

Please enter the time you plan to leave: <b>1630</b>
We suggest you take this route:

Route: 153 Brea Mall
Departure time: 1642
Arrival time: 1703


What do you want to do? 
R - Create routes
D - Display routes
X - Exit
Action: <b>X</b>


Thank you for using TuffyTravel!
</pre>

# Submission checklist
1. Created classes.
1. Created function prototypes.
1. Created function implementation.
1. Called functions in the driver accordingly.
1. Followed the [proper file structure for using functions](https://github.com/ILXL-guides/function-file-organization)
1. Compiled and ran the driver (`tuffytravel`).
1. Manually checked for compilation and logical errors.
1. Designed and tested your own test cases.
1. Ensured no errors on the unit test (`make test`).
1. Ensured no errors on the style check (`make stylecheck`).
1. Ensured no errors on the format check (`make formatcheck`).
1. Completed reflection file ([reflection.md](reflection.md))

# Code evaluation
Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of `/home/student/ms01-tuffy` and you are currently in `/home/student` you can issue the following commands

```
cd ms01-tuffy
```

Use the `clang++` command to compile your code and the `./` command to run it. The sample code below shows how you would compile code save in `tuffytravel.cpp` and into the executable file `tuffytravel`. Make sure you use the correct filenames required in this problem.  Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

```
clang++ -std=c++17 tuffytravel.cpp route.cpp -o tuffytravel
./tuffytravel
```

You can run one, two, or all the commands below to `test` your code, `stylecheck` your code's design, or `formatcheck` your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

```
make test
make stylecheck
make formatcheck
```

A faster way of running all these tests uses the `all` parameter.

```
make all
```

# Submission
1. When everything runs correctly,  let's copy your code into the Github repository. The first step is to add your code to what is called the staging area using git's `add` command. The parameter after `add` is the name of the file you want to add. There are cases when you have multiple changed files, so you can just type . (period) to add all modified files.

    ```
    git add tuffytravel.cpp route.cpp route.hpp
    ```
1. Once everything is in the staging area, we use the `commit` command to tell git that we have added everything we need into the staging area.

    ```
    git commit
    ```
1. In case it asks you  to configure global variables for an email and name, just copy the commands it provides then replace the dummy text with your email and Github username.

    ```
    git config --global user.email "tuffy@csu.fullerton.edu"
    git config --global user.name "Tuffy Titan"
    ```
    When you're done, make sure you type `git commit` again.    
1. Git will ask you to describe what you have added to the staging area. By default, you will use a command-line based editor called *nano*. Go ahead and provide a description then press <kbd>Ctrl</kbd> + <kbd>x</kbd> to exit. Press <kbd>Y</kbd> to confirm that you want to make changes and then press <kbd>Enter</kbd>.
1. Lets push all changes to the Github repository using git's `push` command. Provide your Github username and password when you are asked.

    ```
    git push
    ```
1. When you finish the exercise, go back to Titanium and click on the `Add submission` button in the lab exercise page. Provide a short message in the text area such as "finished lab exercise" and click on `Save changes`. Finally click on `Submit assignment` to inform your instructor that you are done.
