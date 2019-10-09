# uas_documentation
The CONTINUOUSLY UPDATED one-stop-shop documentation for the BYU UAS competition team.

## Read The Docs
You can read the documentation [directly in your browser](https://github.com/BYU-AUVSI/uas_documentation/blob/master/source/index.md) in GitHub.  

## Write The Docs
The documentation is written in [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). 
The pages can be easily updated from the GitHub web interface (simply select
the file to be updated and click "Edit this file").

## Build The Docs
To build the documentation, clone this repository to your computer. You will 
need to have Sphinx installed.

The docs have a dependency on Recommonmark. Install it:
```
pip3 install recommonmark
```

The following commands all need to be run from the toplevel directory:

For HTML docs, run `make html`.  
For Latex docs, run `make latex`.  
For PDF docs, run `make latexpdf` (you will likely need a latex engine installed on your computer).  
