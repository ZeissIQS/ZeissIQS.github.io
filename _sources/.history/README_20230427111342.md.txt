# ZeissIQS-pages

Source the documentation in zeissiqs.github.io is generated from

## General

* The documentation accessible via [](https://zeissiqs.github.io) is generated from the files in this repository.
* The [sphinx documentation conversion tool](https://www.sphinx-doc.org) is used for that purpose.
* The generated documentation is then committed into a repository with some special name and can the be rendered by the github site.

## Installation

> For GOM software developers: The necessary tools are already part of the build system.

* You need a python 3 installation
* Add the necessary python packages:

~~~
python -m pip install sphinx sphinx_rtd_theme myst_parser
~~~

## Repositories

* Clone the source and the target repository into a common parent directory

~~~
cd my_working_directory
git clone https://github.com/ZeissIQS/ZeissIQS-pages.git
git clone https://github.com/ZeissIQS/ZeissIQS.github.io.git
~~~

## Editing

### Editing process

* Edit the documentation source (mostly markdown files) in the ZeissIQS-pages directory.
* Execute 'make.bat' from that ZeissIQS-pages directory to update the target repository.
* You can preview the generated documentation by opening ZeissIQS.github.io/index.html in a browser.

### Hints

* The markdown syntax uses the [MyST parser extensions](https://myst-parser.readthedocs.io/en/latest/index.html).
* The project documentation is based on [sphinx](https://www.sphinx-doc.org/en/master/index.html).


## Uploading

* Commit both source and target directory

~~~
cd ZeissIQS-pages
git add -A
git commit -m "Some useful message"
git push

cd ..

cd ZeissIQS.github.io
git add -A
git commit -m "Some useful message"
git push
~~~

* After the changes have been pushed into the 'ZeissIQS.github.io' repository, the live pages at [](https://zeissiqs.github.io) will be updated automatically after app. one minute.
