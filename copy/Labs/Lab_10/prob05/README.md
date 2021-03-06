# Find Number
Create a class called `Numbers`. Create two data members, an `int*` `values_` that points to a dynamically allocated array of numbers and an `int` `capacity_` that stores the total number of elements that the array can hold.

## Default Constructor
Create a default constructor that initializes (sets) the value of 10 to `capacity_` and initializes a new dynamically allocated array with a capacity of 10. It should call the `init` function inside the body of the constructor.

## Non-default Constructor
Create a non-default constructor that accepts an `int` parameter that is assigned to `capacity_` that is used as the capacity of the dynamically allocated array. It should also call the `init` function inside the body of the constructor.

## Destructor
Create a destructor that deletes the dynamically allocated array and initializes
the pointer to `nullptr`.

## Accessor
Create an accessor for `capacity_`. 

## Member functions

### init
The implementation of the `init` member function is already provided for you. You only need to create it's function prototype in `find_number.hpp`. This function should be a **private** member function that sets initial values of your dynamically allocated array according to the capacity.

### display_array
Create a member function `display_array` that displays the contents of the array, as shown in the output below.

```
2 4 6 8 10 12 14 16 18 20
```

### find_number
Create a member function `find_number` that takes in an `int` parameter representing the number you want to find. It should check to see if the array contains the number that
is passed. If the number is present, then display a statement saying that
the number is in the array as shown in the the output below.

```
2 is in the array
```

## Other instructions
The main function is already given to you. Do not edit `main.cpp`, but place your `Numbers` class in `find_number.hpp`. Member functions that take more than five lines or use complex constructs should have their function prototype in `find_number.hpp` and implementation in `find_number.cpp`.

## Sample Output
```
2 4 6 8 10 12 14 16 18 20
2 is in the array
10 is in the array
16 is in the array
```

# Submission checklist
1. Created function prototype and stored in `.hpp` file.
1. Created function implementation and stored in `.cpp` file (see [reference](https://github.com/ILXL-guides/function-file-organization)).
1. Call function in the driver
1. Compiled and ran the driver (`main`).
1. Manually checked for compilation and logical errors.
1. Ensured no errors on the unit test (`make test`).
1. Followed advice from the stylechecker (`make stylecheck`).
1. Followed advice from the formatchecker to improve code readbility (`make formatcheck`).

# Code evaluation
Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of `/home/student/labex02-tuffy` and you are currently in `/home/student` you can issue the following commands

```
cd labex02-tuffy
```

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

```
cd prob01
```

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in `prob01`, you can issue the following commands to go to the parent folder then go into another problem you want to answer; `prob02` for example.

```
cd ..
cd prob02
```

Use the `clang++` command to compile your code and the `./` command to run it. The sample code below shows how you would compile code saved in `find_number.cpp` and `main.cpp`, and into the executable file `main`. Make sure you use the correct filenames required in this problem.  Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

```
clang++ -std=c++17 main.cpp find_number.cpp -o main
./main
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
    git add main.cpp find_number.hpp find_number.cpp
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
