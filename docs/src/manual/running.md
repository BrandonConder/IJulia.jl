# Running IJulia


## Running the IJulia Notebook

If you are comfortable managing your own Python/Jupyter installation, you can just run `jupyter notebook` yourself in a terminal.   To simplify installation, however, you can alternatively type the following in Julia, at the `julia>` prompt:
```julia
using IJulia
notebook()
```
to launch the IJulia notebook in your browser.

You can
use `notebook(detached=true)` to launch a notebook server
in the background that will persist even when you quit Julia.
This is also useful if you want to keep using the current Julia
session instead of opening a new one.

```julia
julia> using IJulia; notebook(detached=true)
Process(`'C:\Users\JuliaUser\.julia\v0.7\Conda\deps\usr\Scripts\jupyter' notebook`, ProcessRunning)

julia>
```

By default, the notebook "dashboard" opens in your
home directory (`homedir()`), but you can open the dashboard
in a different directory with `notebook(dir="/some/path")`.

Alternatively, you can run
```
jupyter notebook
```
from the command line (the
[Terminal](https://en.wikipedia.org/wiki/Terminal_%28OS_X%29) program
in MacOS or the [Command
Prompt](https://en.wikipedia.org/wiki/Command_Prompt) in Windows).

A "dashboard" window like this should open in your web browser.  Click
on the *New* button and choose the *Julia* option to start a new
"notebook".  A notebook will combine code, computed results, formatted
text, and images, just as in IPython.  You can enter multiline input
cells and execute them with *shift-ENTER*, and the menu items are
mostly self-explanatory.  Refer to [the Jupyter notebook
documentation](https://jupyter-notebook.readthedocs.io/en/stable/) for more
information, and see also the "Help" menu in the notebook itself.

Given an IJulia notebook file, you can execute its code within any
other Julia file (including another notebook) via the [NBInclude](https://github.com/stevengj/NBInclude.jl) package.


## Running the JupyterLab

Instead of running the classic notebook interface, you can use the IDE-like JupyterLab. If you are comfortable managing your own JupyterLab installation, you can just run `jupyter lab` yourself in a terminal.   To simplify installation, however, you can alternatively type the following in Julia, at the `julia>` prompt:

```jl
using IJulia
jupyterlab()
```

`jupyterlab()` also supports `detached` and `dir` keyword options similar to `notebook()`.


## Running nteract

The [nteract Desktop](https://nteract.io/) is an application that lets you work with notebooks without a Python installation. First, install IJulia (but do not run `notebook()` unless you want a Python installation) and then nteract.


## Other IPython interfaces

Most people will use the notebook (browser-based) interface, but you
can also use the IPython
[qtconsole](http://ipython.org/ipython-doc/dev/interactive/qtconsole.html)
or IPython terminal interfaces by running `ipython qtconsole --kernel
julia-0.7` or `ipython console --kernel julia-0.7`, respectively.
(Replace `0.7` with whatever major Julia version you are using.)
