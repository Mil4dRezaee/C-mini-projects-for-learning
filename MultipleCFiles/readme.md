# Multi-File C Project Example

This demonstrates how to structure, compile, and use a C program split across multiple files. It serves as an educational example for beginners learning about modular C programming and CMake-based building.

## Project Structure

The project consists of the following files:

1. `main.c`: The main program file
2. `func.c`: Implementation of a utility function
3. `func.h`: Header file for function declarations
4. `CMakeLists.txt`: CMake configuration file for building the project

### File Purposes

- `main.c`: Entry point of the program. It includes `func.h` to use the `printInt` function.
- `func.c`: Contains the implementation of the `printInt` function.
- `func.h`: Declares the `printInt` function, making it available to other parts of the program.
- `CMakeLists.txt`: Specifies how to build the project, including which source files to compile.

## Key Concepts Demonstrated

1. **Header Files**: The use of `func.h` shows how to declare functions that can be used across multiple files.

2. **Function Implementation**: `func.c` demonstrates how to implement functions declared in a header file.

3. **Modular Programming**: By separating the `printInt` function into its own files, the project shows how to organize code for better maintainability and reusability.

4. **CMake Usage**: The `CMakeLists.txt` file shows how to set up a build system for a multi-file project.

## Building the Project

This project uses CMake to generate build files. Follow these steps:

1. Create a build directory:
   ```
   mkdir build
   cd build
   ```

2. Generate the build files:
   ```
   cmake ..
   ```

3. Build the project:
   ```
   cmake --build .
   ```

## Running the Program

After building, run the executable:

```
./untitled
```

The program will prompt you to enter an integer, which it will then print back to you.

## Understanding the Build Process

1. CMake reads `CMakeLists.txt` to understand the project structure.
2. It generates appropriate build files (e.g., Makefiles).
3. The build system compiles `main.c` and `func.c` separately.
4. The object files are then linked together to create the final executable.

## Extending the Project

To add more functionality:
1. Create new `.c` and `.h` files for new functions.
2. Include the new `.h` files where the functions are needed.
3. Add the new `.c` files to the `add_executable` command in `CMakeLists.txt`.

## Requirements

- C Compiler (supporting C11 standard)
- CMake (version 3.26 or higher)

## Learning Objectives

By studying and extending this project, you can learn:
- How to split C programs into multiple files
- The role of header files in C
- How to use CMake for multi-file projects
- Best practices for organizing C code
