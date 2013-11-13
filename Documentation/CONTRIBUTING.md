Contributing to LDR Importer
============================

There are a few guidelines that must be followed at all times when developing **LDR Importer**

Thou Shalt Do The Dance
-----------------------

* Fork the repository by clicking ![the Fork button](http://i81.servimg.com/u/f81/16/33/06/11/forkme12.png)
* Clone the script onto your computer by running ```git clone https://github.com/yourusername/LDR-Importer.git``` or if you are using a GUI client, however you clone repositories.
* Read up on the code and project layout and guidelines [below](#for-your-reading-pleasure)
* Edit away! A list of stuff to do is in the [Issues](https://github.com/le717/LDR-Importer/issues).
* Once you finish your work, submit a [Pull Request](https://github.com/le717/LDR-Importer/pulls) by clicking ![the Pull Request button](http://i81.servimg.com/u/f81/16/33/06/11/pullre10.png)
* If everything checks out, your changes will be merged! :grinning:
* Don't forget to share the project with your friends and ![Star!](http://i81.servimg.com/u/f81/16/33/06/11/star11.png)


For Your Reading Pleasure
-------------------------

### Python Code Layout ###

* [PEP 8](http://www.python.org/dev/peps/pep-0008/) should be followed at all times. Line length should be followed when possible
(it is not always feasible to keep lines at 79 characters. You can use the [PEP8 online](http://pep8online.com/) website to
check for errors.
* The [Blender Python API style guidelines](http://www.blender.org/documentation/blender_python_api_2_69_0/info_best_practice.html),
which is mainly a small extension of PEP 8.
* Use double quotes (`""`) when possible. For multi-line strings, use triple quotes (`''' '''`, `""" """`).
* [`str.format()`](http://docs.python.org/3/library/stdtypes.html#str.format) is the preferred way to join strings.
It a single line string is more than 79 characters and does not need to be on a second line, `str.format()` to keep it on one line
and wrap the extended string on the next physical  line.
It is better than the [% operator](http://docs.python.org/3/tutorial/inputoutput.html#old-string-formatting),
and using `+` (plus) signs is just bad practice. :wink:
* Always trim whitespace from the end of lines, blank lines, and around operators.
* Please try to document your code as much as possible. It is understood you may not have the time to and others might need to do it,
but if you do have the time do document, go right ahead and do it and perhaps whatever else may need it!

### Separate Branches ###

The project into is divided into two separate, distinct branches, in addition to feature branches.

* The `master` branch is where stable, complete, mostly bug-free code belongs. It is this script that will make up the next, official release. If someone
wanted to download a prerelease version and not worry about it being broken, they would download this branch.

* The `unstable` branch is where all beta, draft, and buggy code belongs. Features that may be harder to implement or take longer to add go here so the
master branch does not contain error code. If someone wanted to download the newest, possible broken script, they would download ths branch.

The `unstable` branch is never to be merged into the ``master` branch. When the changes made in the unstable is to be added into the master, you need to
manually merge them and commit it.

* **Feature branches** are created when large changes need to be made or tested, and it does not need to be done in the `master` branch.
Both forks and the main repository should follow this. Not only does it make the process of merging pull requests easier,
but it also gives freedom to experiment with new changes without polluting the commit history too much.

### Releases ###

* Releases will be tagged when the script is deemed by the current contributors to be in working order and contains good changes to release.
* Releases are created using `setup.py`, which automatically creates a Zip archive of the release and any additional files.
* Releases will be tagged and and the Zip archive hosted using [GitHub Releases](https://github.com/le717/LDR-Importer/releases).
[Semantic versioning](http://semver.org/) is used to denote both the script version and tag URL.
* Normally a condensed change log highlighting notable new features, changes, and bug fixes is listed in the release notes.
* When the version number is changed, _always_ remember to update the version in `__version.py__`, as it defines the version number
`setup.py` uses. The version number is expressed in integers and tuple, i.e. `(1, 1, 0)`.
