<div align="center"><img src="deps/ijulialogo.png" alt="IJulia logo" width="150"/></div>

[![](https://img.shields.io/badge/docs-stable-blue.svg)](https://JuliaLang.github.io/IJulia.jl/stable)
[![](https://img.shields.io/badge/docs-latest-blue.svg)](https://JuliaLang.github.io/IJulia.jl/dev)
[![Build Status](https://github.com/JuliaLang/IJulia.jl/workflows/CI/badge.svg)](https://github.com/JuliaLang/IJulia.jl/actions?query=workflow%3ACI+branch%3Amaster)

# IJulia

**IJulia** is a [Julia-language](http://julialang.org/) backend
combined with the [Jupyter](http://jupyter.org/) interactive
environment (also used by [IPython](http://ipython.org/)).  This
combination allows you to interact with the Julia language using
Jupyter/IPython's powerful [graphical
notebook](http://ipython.org/notebook.html), which combines code,
formatted text, math, and multimedia in a single document.
IJulia is a Jupyter language kernel and works with a variety of notebook
user interfaces. In addition to the classic Jupyter Notebook, IJulia
also works with [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/), a Jupyter-based
integrated development environment for notebooks and code.
The [nteract notebook desktop](https://nteract.io/) supports IJulia with
detailed instructions for its [installation with nteract](https://nteract.io/kernels/julia).

(IJulia notebooks can also be re-used in other Julia code via
the [NBInclude](https://github.com/stevengj/NBInclude.jl) package.)

## Quick start

Install IJulia from the Julia REPL by pressing `]` to enter pkg mode and entering:

```
add IJulia
```

If you already have Python/Jupyter installed on your machine, this process will also install a
[kernel specification](https://jupyter-client.readthedocs.io/en/latest/kernels.html#kernelspecs)
that tells Jupyter how to launch Julia. You can then launch the notebook server the usual
way by running `jupyter notebook` in the terminal.

Alternatively, you can have IJulia create and manage its own Python/Jupyter installation.
To do this, type the following in Julia, at the `julia>` prompt:

```julia
using IJulia
notebook()
```

to launch the IJulia notebook in your browser.

For more advanced installation options, such as specifying a specific Jupyter
installation to use, see the [documentation](https://JuliaLang.github.io/IJulia.jl/stable).
