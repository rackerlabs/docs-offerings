# Contributor guidelines

Use this template to create contributor guidelines in your API docs repo. To
customize the template, view the source and replace the following placeholders
with the values for your API documentation project:

- Replace ``{{repo.location}}`` with the repository (repo) location.

  ``{{repo.location}}`` is usually https://github.rackspace.com for
  internal, private documentation and https://github.com for external, public
  documentation.

- Replace ``{{repo.org}}``.

  ``{{repo.org}}`` is usually ``IX`` for internal,  private documentation
  and ``rackerlabs`` for external, public documentation.

- Replace ``{{repo.name}}`` with the name you assigned to the repo.

  The name usually starts with ``docs``, for example, ``docs-cloud-load-balancers``.

- Replace or delete ``{{folder.name}}``.

  The ``{{folder.name}}`` variable appears in links to the content files in
  the repo. If your repo contains more than one Sphinx project (for example
  content for v1 and v2 of an API), the content goes in separate folders inside
  the ``api-docs`` folder. In this case, update the ``{{folder.name}}`` to
  point to the current version, and add a note to the project description that
  points to the folder for the older version. If one of the versions, is in
  beta or early release, indicate that in the note.

  If you have only one version, delete the ``{{folder.name}}/`` pattern from
  the URLs.

Use the following sections and boilerplate text in your file, changing
variables as noted.  

These guidelines provide the general process for maintaining source code that
builds the Rackspace ``{{product-name}}`` developer documentation.

- [Project description](#project-description)
- [Updating and adding content](#updating-and-adding-content)
- [Using writing guidelines](#using-writing-guidelines)
- [Submitting your content](#submitting-changes)
- [Previewing changes](#previewing-changes)

## Project description
<!-- Provide as little or as much information about architecture as needed to help
contributors figure out which file to update.-->

This project is developed and built by using the
[Python Sphinx documentation generator](http://sphinx-doc.org/). Content is
written in [reStructuredText](http://sphinx-doc.org/rest.html), which is the
markup syntax and parser component of
[Python Docutils](http://docutils.sourceforge.net/index.html).

Source files for the Sphinx documentation project are in the ``api-docs``
directory. Following are the key files that define project and content
architecture:

**Note:** Update the source for this table with the information for your
project. Replace ``{{repo.location}}:{{repo.org}}/{{repo-name}}`` and
``{{folder-name}}`` as noted at the beginning of this document. If you have
multiple Sphinx doc projects in the same repo, add information for both
projects in this contributing document. **After updating the table with the
correct links for your content, remove the double tick marks to make the links
live.**

Content | File
--- | ---
|Index page for the main content structure| ``[index.rst](https://{{repo.location}}:{{repo.org}}//blob/master/api-docs/{{folder-name}}/index.rst)``
|Getting Started index| ``[getting-started/index.rst](https://{{repo.location}}:{{repo.org}}/{{repo-name}}/blob/master/api-docs/{{folder-name}}/getting-started/index.rst.rst)``
|General API information index|``[general-api-info/index.rst](https://{{repo.location}}:{{repo.org}}/{{repo-name}}/blob/master/api-docs/{{folder-name}}/general-api-info/index.rst)``
|API Reference index|``[api-reference/index.rst](https://{{repo.location}}:{{repo.org}}/{{repo-name}}/blob/master/api-docs/{{folder-name}}/api-reference/index.rst)``
|API operations methods, including code samples|``[api-reference/methods](https://{{repo.location}}:{{repo.org}}/{{repo-name}}/tree/master/api-docs/{{folder-name}}/api-reference/methods)``
|Release notes index|``[release-notes/index.rst](https://{{repo.location}}:{{repo.org}}/{{repo-name}}/blob/master/api-docs/{{folder-name}}/release-notes/index.rst)``
|Sphinx documentation configuration file| ``[conf.py](https://{{repo.location}}:{{repo.org}}/{{repo-name}}/blob/master/api-docs/{{folder-name}}/conf.py)`` For new projects, replace the following values in the conf.py file with values for your API project: ``product``= name of the API service, ``v#``= contract version, ``v#.r#``= ``release number``
|Linux and OS X build script|``Makefile``|
|Windows build script|``make.bat``|
|Installation requirements for building locally|``[requirements.txt](https://{{repo.location}}:{{repo.org}}/docs-common/blob/master/requirements.txt)``


## Updating and adding content

Contributions are submitted, reviewed, and accepted by using GitHub pull
requests (PRs), following the [GitHub workflow](GITHUBING.md) for this repository.

To update existing source files or add new ones, follow the
[GitHub workflow](GITHUBING.md) for this repository.

* Update source files by using the GitHub editor or any plain text editor.
* Format source files with
  [reStructuredText syntax](http://www.sphinx-doc.org/en/stable/rest.html).
* For quick syntax checking, try the
[Online reStructuredText editor](http://rst.ninjs.org/).

## Using writing guidelines

When you add or update content, use the writing and style guidelines
in the [Style guidelines for technical content](http://rackerlabs.github.io/docs-rackspace/style-guide/index.html).
Start with the guidelines in the [Quickstart](http://rackerlabs.github.io/docs-rackspace/style-guide/quickstart.html#quickstart)
section.

## Submitting changes

When you've completed your changes, submit a PR. Someone on the
Information Development team will review your PR.
- Minor updates and corrections get a quick review to ensure that content is
  error-free and doesn't introduce other issues.
- More complex changes or additions require both technical and editorial review.

Depending on the review feedback, you might be asked to make additional changes.

After content has been reviewed and approved, the updates can be merged to the
master branch. The merge triggers the build and deploy process. Typically, new
content is available on **developer.rackspace.com** within a minute or two
after it is merged. Larger updates might take a bit longer.

## Previewing changes

When you submit a PR, the build process creates a preview of your changes in a
staging environment. After the build process is complete, a message is
displayed in the PR comments with a link to the content in the staging
environment.

You can also build the project locally by using the [Sphinx documentation
generator](http://sphinx-doc.org/). For details, see
[Building from source](https://github.com/rackerlabs/docs-rackspace/blob/master/doc/tools/build-from-source.rst).
