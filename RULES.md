General Rules
=============


Plagiarism Note and Late Submissions
------------------------------------

Copying code (either from other students or from external sources) is strictly prohibited! We will be using automatic anti-plagiarism tools, and any violation of this rule will lead to expulsion from the class. Late submissions will be accepted with a grade penalty of 10% per day. In case of serious illness or emergency please notify the assistants and provide a relevant medical certificate.


Provided Software
-----------------

For this class, you will use the minimal framework provided with each assignment. It compiles on Windows, Linux and Mac. If you have trouble compiling follow the procedure used by the auto-builds when available (file `.travis.yml` for Mac/Linux, and file `.appveyor.yml` for Windows) before contacting the assistant. Make sure to [pull](http://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository) the more recent changes from the git repository as we might be updating the source code from time to time.

### Preparing the Build Environment

The assignments will use CMake as a build system. Before we can begin, you must install CMake on your computer.
I recommend installing it with a package manager instead of the [CMake download page](http://www.cmake.org/download/). E.g. on Debian/Ubuntu: `sudo apt-get install cmake`, with MacPorts on Mac: `sudo port install cmake`, and on Windows with [Chocolatey](https://chocolatey.org/): `choco install -y cmake`.

You must install a C++ compiler: `gcc/clang` on Linux, `clang` on Mac, [Visual Studio](https://www.visualstudio.com/) on Windows. If you are looking for an IDE to develop in C++, we recommend [CLion](https://www.jetbrains.com/clion) on Mac/Linux, and [Visual Studio](https://www.visualstudio.com/) on Windows. Students looking for more lightweight options might be interested in [SublimeText](https://www.sublimetext.com/), [Atom](https://atom.io/), or [VS Code](https://code.visualstudio.com/), all of which are very similar editors and run on both Linux/Mac/Windows.

### Compiling the Sample Projects

We will provide a folder for each assignment with some sample code to get you started. Included in each assignment folder is a CMake build system that should enable you to easily compile your code.
For each assignment, you will need to do the following:

1. Copy the assignment code from this github repository
2. Create a directory called `build` in the assignment directory, e.g.:
   ```
   cd assignment_X; mkdir build
   ```
3. Use CMake to generate the Makefile/project files needed for compilation inside the `build/` directory:
   ```
   cd build; cmake -DCMAKE_BUILD_TYPE=Debug ..
   ```
4. Compile and run the compiled executable by typing:
   ```
   make; ./assignmentX
   ```

If you run into problems, please create an issue on the github repository .


What to Hand In
---------------

The delivery of the exercises is done using nyu classes. The repository should follow the template provided in the starter code, and it must contain:

- The source code, together with the necessary CMake project files, but excluding all compiled binaries/libraries. Specifically, do not include the `build/` directory. The code must successfully compile in Travis on the Linux operating system.

- A small report (in pdf or text/markdown format) containing a description of what you’ve implemented, as well as explanations/comments on your results.

- Screenshots of all your results with associated descriptions in the report file.

Note: It will generally not be necessary to use additional external software for your assignments. If you find that you need to use additional binaries / external libraries other than those provided by us, please first get approval by filing an [issue](https://github.com/nyu-cg-fall-17/computer-graphics/issues).


Grading
-------

The code will be evaluated on Linux, if you develop on different operating systems the assistants might ask you to bring your laptop for the grading. In order to receive a grade, your code **must** compile on your laptop or on a vanilla ubuntu 18.04 LTS installation.

Your submission will be graded according to the quality of your image results, and the correctness of the implemented algorithms. The submitted code must reproduce exactly the images included in your readme.

To ensure fairness of your grade, you will be asked to briefly present your work to the teaching assistant. Each student will have 3-4 minutes to demo their submission and explain in some detail what has been implemented, report potential problems and how they tried to solve them, and point the assistants to the code locations where the various key points of the assignments have been implemented. If you cannot make it to the demo session, please schedule a separate meeting with the assistant in the week after the demo session.
