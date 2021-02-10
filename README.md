# UD Data Science Tutorial

This repo provides setup and files for a Julia data science tutorial at the University of Delaware.

## Installation and setup

1. Follow the directions at [https://julialang.org/downloads](https://julialang.org/downloads) to install Julia.
2. If you are familiar with git, clone the repo as usual. Otherwise, click the "Code" button above and select the zip file to download. Unpack it and take note of the location.
3. Start Julia. You will get a prompt "julia>". This is called the REPL.
4. At the prompt, enter `cd("path/to/this/repo")` to change to the root directory of the tutorial. (It's where this file is located for you.)
5. At the prompt, hit the "]" key. This changes the prompt's color, and it ends with "pkg>". This is the package manager mode.
6. At the prompt, enter `activate .` to activate the environment defined in this directory.
7. At the prompt, enter `instantiate` and then wait as the package manager downloads all the dependencies for the tutorial. On Windows in particular, this may take a lot of time (something to do with downloading tons of small files).
8. When the prompt returns, hit the Backspace key (Delete on Mac). This returns you to the main prompt.
9. It's recommended that you also enter `include(joinpath("src","preload.jl"))` now in order to cause all the packages to be fully compiled. This will take a long time on every platform. (They're working on it.) When it's done, your browser should open to an instance of Jupyter notebook. You can close this.
10. Hit Ctrl-C or Command-C to interrupt the notebook server.
11. You can now quit Julia by closing the window, or by hitting Ctrl-D or Command-D.

## Usage

First, follow steps 3-6 above to activate the tutorial's project. Then return to the main Julia prompt and enter

````julia
using IJulia
notebook(dir=pwd())
````

This should launch a Jupyter notebook interface in your browser, open to the the tutorial directory.
