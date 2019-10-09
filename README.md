# uas_documentation
The CONTINUOUSLY UPDATED one-stop-shop documentation for the BYU UAS competition team.

## Writing The Docs
The documentation is written in [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). 
The pages can be easily updated from the GitHub web interface (simply select
the file to be updated and click "Edit this file").

## Build The Docs
To build the documentation, clone this repository to your computer. You will 
need to have Sphinx installed.

### HTML Docs
From the toplevel directory, run:
```
make html
```

### Latex Docs
From the toplevel directory, run:
```
make latex
```

### PDF Docs
From the toplevel directory, run:
```
make latexpdf
```
You will likely need a latex engine installed on your computer.
