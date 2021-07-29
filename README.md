## Show Markdown from within Code Cells in Jupyter and VS Code's Interactive Python

## Description
Display markdown from within code cells in IPython output, while ignoring it when run in normal Python (like usual comments).

More details and explanation on [randompearls.com](https://randompearls.com/science-and-technology/information-technology/coding-and-development-reference-and-tools/show-markdown-within-code-cells-jupyter-and-vs-code-interactive-python/).

## Installation
You can install it as a package by running `pip install git+https://github.com/manisar2/ipyccmd.git` .
<br>Or copy the code from *src/ipy_ccmd/\_\_init\_\_.py* into your project.

Note that *forbiddenfruit* is installed as a dependency, so that statements of the form `"anystring".md(type=DisplayType.Type)` can be used conveniently.<br>
You may instead choose to use the functionality like `display_string("anystring", type=DisplayType=Type)`.

Also, *IPython* is not installed automatically, but it is a dependency.<br>
Please make sure you have it in your Python environment.

## Usage
It can be used in two ways.<br>
Note that you will not need the import statements if you have copy-pasted the code from *src/ipy_ccmd/\_\_init\_\_.py* into your current file.

### A. Using curse (*forbiddenfruit*):
```python
from ipyccmd import DisplayType
"Now we'll calculate the area as per $A = \pi r^2 + 2 \pi r h$.".md()
"V = {1 \over 3} \pi r^2 h".md(DisplayType.MATH)
```

### B. Without using curse (you can uninstall *forbiddenfruit*):
```python
from ipyccmd import display_string, DisplayType
display_string("Now we'll calculate the area as per $A = \pi r^2 + 2 \pi r h$.")
display_string("V = {1 \over 3} \pi r^2 h", DisplayType.MATH)
```

### See a [.py](example/example.py) or [.ipynb](example/ipy_md.ipynb) example.

### The display can be modified in these ways (using `type` argument):
* MARKDOWN
* LATEX
* MATH
* HTML
* PRETTY

