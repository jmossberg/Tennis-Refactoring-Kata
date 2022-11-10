# Tennis-Refactoring-Kata C++ with Google test

If working with an IDE with google test
support, such as CLion, the google-test gives a better overview
of issues. Downside is that google-test has to be obtained (by
git clone) during the cmake-setup process.

## Using CMake and Visual Studio, under Windows

### Option 1: Generate Visual Studio solution manually

1. Download and install CMake from cmake.org
2. Sample setup (in a Windows console, using Git), and considering
   you are already located in this folder:
   
   ```
   mkdir build
   cd build
   cmake .. -G "Visual Studio 17 2022"
   ```
3. Open Tennis-Kata.sln in Visual Studio 2022
   Visual Studio should start with the projects in it.
   You will have four executables, each one for a
   specific version of initial source code (1, 2, 3 and 4).
   Tests are already complete, code is ready to refactor!

### Option 2: Open directly in Visual Sudio 2022

1. Start Visual Studio 2022
2. Select `Open a local folder`
3. Select the folder containg this readme.
4. Visual Studio 2022 will generate a project and you can run tests for variant 1, 2, 3 or 4.

See https://learn.microsoft.com/en-us/cpp/build/cmake-projects-in-visual-studio?view=msvc-170 for more information.

## Using CMake and Mingw, under Windows

```
mkdir build
cd build
cmake .. -G "MSYS Makefiles"
cmake --build .
ctest
```
## Using cmake under Ubuntu GNU/Linux
Make sure cmake is installed (available as a snap or in the
repositories)
```
mkdir build
cd build
cmake .. 
cmake --build .
ctest
```
If you want to use a specific makefile generator, you can 
specify it with the -G flag, just as in windows.
(cmake --help will give you a list of available generators.)
