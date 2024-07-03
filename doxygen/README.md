# Purpose
Often when you inherit a code base (such as a Bitbucket git repo) you are tasked with finding all the entry points and navigating to all the points of interest so you can write unit tests, fix bugs, add features. Although IDEs do a great job of assisting with that they can be slow to navigate and do not typically generate inheritance and collaboration diagrams (which are invaluable). With Doxygen (https://www.doxygen.nl/   you can do all this as well as inline all the source code and make all the keywords in the source clickable. This is a great tool to have in your toolkit.

# Method
1. Check out your repo
2. Copy the pre-written `Doxyfile` to the root of your repo
3. Modify `PROJECT_NAME` at the very least to match your project name
4. run `doxygen` in the same folder as the `Doxyfile`
    1. can be installed using brew or other package managers
5. or, Run it using docker 
    1. further reading see https://gitlab.com/pommalabs/docker/doxygen
    2. Run `% docker run -it --rm --name Doxygen -v ${PWD}:/opt/prj pommalabs/doxygen`
    * __Note:__ if using windows, use powershell 7+ such that the ${PWD} will work.
6. View the results
    1. On macos run `open doxygen/html/index.html`
    2. On windows run `start doxygen/html/index.html`