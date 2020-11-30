# NumPy tutorials

This set of tutorials and educational materials is being developed,
IT IS NOT INTEGRATED IN THE HTML DOCS AT https://www.numpy.org/devdocs/

The goal of this repository is to provide high-quality resources by the
NumPy project, both for self-learning and for teaching classes with. If you're
interested in adding your own content, check the [Contributing](#contributing)
section.

To download a local copy of the `.ipynb` files, you can either
[clone this repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)
or navigate to any of the documents listed below and download it individually.

## Content

0. [Learn to write a NumPy tutorial](content/tutorial-style-guide.md): our style guide for writing tutorials.
1. [Tutorial: Linear algebra on n-dimensional arrays](content/tutorial-svd.md)
2. [Tutorial: CS231n Python Tutorial](content/cs231_tutorial.md)
3. [Tutorial: Determining Moore's Law with real data in NumPy](content/mooreslaw-tutorial.ipynb)
4. [Tutorial: Saving and sharing your NumPy arrays](content/save-load-arrays.ipynb)

## Contributing

We very much welcome contributions! If you have an idea or proposal for a new
tutorial, please [open an issue](https://github.com/numpy/numpy-tutorials/issues)
with an outline. 

Don’t worry if English is not your first language, or if you can only come up
with a rough draft. Open source is a community effort. Do your best – we’ll help
fix issues.

Images and real-life data make text more engaging and powerful, but be sure what
you use is appropriately licensed and available. Here again, even a rough idea
for artwork can be polished by others.

Pull requests are reviewed in markdown format. The 

### Why Jupyter Notebooks?

The choice of Jupyter Notebook in this repo instead of the usual format 
([reStructuredText, through Sphinx](https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html))
used in the main NumPy documentation has two reasons:

 * Jupyter notebooks are a common format for communicating scientific
   information.
 * rST may present a barrier for some people who might otherwise be very
   interested in contributing tutorial material.

#### Note

You may notice that some of our content is in markdown format (`.md` files). 
This is part of an ongoing restructuring of the repository workflow. However, 
you can still submit your content as a Jupyter Notebook file.

### Adding your own tutorials

If you have your own tutorial in the form of a Jupyter notebook (a `.ipynb`
file) and you'd like to add it to the repository:

#### Create or pair your [`myst`](https://jupytext.readthedocs.io/en/latest/formats.html#myst-markdown) notebook

The NumPy tutorials are reviewed and executed as a
[MyST-NB](https://myst-nb.readthedocs.io/) notebooks. The benefit is that
content is easier to review in this markdown format. You can convert or
pair your `.ipynb` to `myst` using
[Jupytext](https://jupytext.readthedocs.io/en/latest/index.html).
Install `jupytext` using:

```
pip install jupytext
```
or
```
conda install jupytext -c conda-forge
```

Once installed, you can start your `jupyter lab` or `jupyter notebook`
in the browser. When launching `jupyter lab` it will ask you to rebuild
to include the Jupytext extension. 

##### Convert the `.ipynb` to `myst`

To convert your `notebook.ipynb` to MyST-NB, run the following command:

```
jupytext --to myst notebook.ipynb
```

You will now have a `notebook.md` file that is in the MyST-NB format. 

##### Pair the `.ipynb` to `myst`

If you want to keep your `notebook.ipynb` synced to your `notebook.md`
file, you can pair the two formats in the classic Jupyter, Jupyter Lab,
or the command line:
<ul>
<details>
    <summary>
        <b>1. Classic Jupyter Jupytext pairing</b>.
    </summary>
    <img src="site/_static/01-classic.gif" width=80% height=80%>
</details>
    
<details>
    <summary>
        <b>2. Jupyter Lab Jupytext pairing</b>
    </summary>
    <img src="site/_static/02-jupyterlab.gif" width=80% height=80%>
</details>
</ul>

__3. Command line Jupytext pairing__

```
jupytext --set-formats ipynb,myst notebook.ipynb
```
update either the MyST-NB or notebook:
```
jupytext --sync notebook.ipynb
```

#### Create an issue

Go to [https://github.com/numpy/numpy-tutorials/issues](https://github.com/numpy/numpy-tutorials/issues)
and create a new issue with your proposal. Give as much detail as you can about
what kind of content you would like to write (tutorial, how-to) and what you
plan to cover. We will try to respond as quickly as possible with comments, if
applicable.

#### Check out our suggested template

You can use our [Tutorial Style Guide](content/tutorial-style-guide.md) to make
your content consistent with our existing tutorials.

#### Upload your content

Remember to convert your `.ipynb` to `.md` (MyST-NB) before uploading it. 

<ul>
<details>
    <summary>
        <b>Fork this repository</b> (if you haven't before).
    </summary>
    <img src="site/_static/01-fork.gif" width=80% height=80%>
</details>
    
<details>
    <summary>
        <b>In your own fork, create a new branch for your content.</b>
    </summary>
    <img src="site/_static/02-create_new_branch.gif" width=80% height=80%>
</details>

<details>
    <summary>
        <b>Add your notebook to the <code>content/</code> directory.</b>
    </summary>
    <img src="site/_static/03-upload.gif" width=80% height=80%>
</details>

<b>Update the <code>environment.yml</code> file with the dependencies for your
tutorial</b> (only if you add new dependencies).

<details>
    <summary>
        <b>Update this <code>README.md</code> to include your new entry.</b>
    </summary>
    <img src="site/_static/04-add_to_readme.gif" width=80% height=80%>
</details>

<b>Update the attribution section (below) to credit the original tutorial
author, if applicable.</b>

<details>
    <summary>
        <b>Create a <a href="https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests">pull request.</a></b>
    </summary>
    <img src="site/_static/05-create_PR.gif" width=80% height=80%>
</details>

:tada: <b>Wait for review!</b>
</ul>

For more information about GitHub and its workflow, you can see
[this document](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests).

### Attribution

 - The cs231n tutorial is by [@jcjohnson][jj]. The full tutorial in 
   its original form is linked via [numpy.org][learn].
 - The SVD tutorial is by [@melissawm][mwm]. The full tutorial is available
   via the [tutorials page][np_tutorials] of the official NumPy documentation.

[jj]: https://github.com/jcjohnson
[mwm]: https://github.com/melissawm
[np_tutorials]: https://numpy.org/devdocs/user/tutorials_index.html

## Useful links and resources

The following links may be useful:

- [NumPy Code of Conduct](https://numpy.org/doc/stable/dev/conduct/code_of_conduct.html)
- [Main NumPy documentation](https://numpy.org/doc/stable/)
- [NumPy documentation team meeting notes](https://hackmd.io/oB_boakvRqKR-_2jRV-Qjg?both)
- [NEP 44 - Restructuring the NumPy documentation](https://numpy.org/neps/nep-0044-restructuring-numpy-docs.html)
- [Blog post - Documentation as a way to build Community](https://labs.quansight.org/blog/2020/03/documentation-as-a-way-to-build-community/)

Note that regular documentation issues for NumPy can be found in the [main NumPy
repository](https://github.com/numpy/numpy/issues) (see the `Documentation`
labels there). 

