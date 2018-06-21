# How to create an API guide

The ``template-api-guide`` folder in the docs-starter-kit repository
(repo) contains templates that you can use to create an API guide for
your product. The folder contains templates for information that is
common across Rackspace product APIs: getting started information,
general information, and reference information for each method that
is part of your API. You use the templates that you need to create
content that is relevant for your users.

## Before you begin

Before starting the work described in this document, be sure to read
and perform the tasks described in the
[Welcome to the docs-starter-kit repo! (main README.md)](https://github.rackspace.com/IX/docs-starter-kit/blob/master/README.md)
file. After doing so, you will have accomplished the following actions:

1. Decided who your audience is and what templates you need to use.

2. Created a new repo in GitHub to house your content. Generally, the
   repo is either in GitHub Enterprise for internal (Racker-only) content
   or in the rackerlabs organization in GitHub for external
   (customer-facing) content.

3. Forked and cloned the [docs-starter-kit repo](https://github.rackspace.com/IX/docs-starter-kit).
   You now have a copy of the docs-starter-kit repo on your computer.

4. Forked and cloned your new doc repo. You now have a copy of your new doc
   repo on your computer.

5. On your computer, copied the ``template-api-guide`` folder to your new
   doc repo as the ``api-guide`` folder.

6. Set up remotes so that you are ready to start creating changes for which you
   eventually create pull requests (PRs).

7. Set up your repository so that automatic builds and publishing occur.

## API guide template files

The ``template-api-guide`` folder that you copied to your new doc repo includes the following files:

- An ``api-docs`` folder that contains all template files for the API guide content,
  as well as some configuration files and a ``spelling_wordlist.txt`` file

- A ``Makefile`` for building the documentation using Sphinx

- A ``conf.py`` build configuration file that is set up when you follow the information in the [README file in the tools-internal-repo directory](https://github.rackspace.com/IX/docs-starter-kit/blob/master/tools-internal-repo/README.md) or the [README file in the tools-external-repo directory](https://github.rackspace.com/IX/docs-starter-kit/blob/master/tools-external-repo/README.md)

- A ``CONTRIBUTING.md`` file template that you can modify to help
  others who will contribute to your repo

- A ``GITHUBING.md`` file template that you can modify to help others
  set up and use git and GitHub with your repo

- This ``README.md`` file with instructions about using the templates

## Content files and structure

The content for the API guide is developed in reStructuredText (RST). The
API guide templates include the following template and index files that
create an API guide with the following structure and file names:

- Opening page and top-level index (index.rst)
- Getting started (getting-started/index.rst)
  - Get your credentials (getting-started/get-credentials-include.rst)
  - Install CLI clients (getting-started/install-CLI-client.rst)
  - Send API request to |service| (getting-started/send-request-ovw.rst)
  - Authenticate to the Rackspace Cloud (getting-started/authenticate.rst)
  - |Service| concepts (getting-started/concepts.rst)
  - Create and manage |service| (getting-started/using-cloud-load-balancers)
  - Examples (getting-started/examples)
- General API information (general-api-info/index.rst)
  - Service access (general-api-info/service-access.rst)
  - Request and response types (general-api-info/request-response.rst)
  - Content compression (product-specific-general-api-content.rst)
  - Persistent connections (general-api-info/persistent-connections.rst)
  - Paginated collections (general-api-info/paginated-collections.rst)
  - Limits (general-api-info/limits.rst)
  - Faults (general-api-info/faults.rst)
  - Date and time format (general-api-info/date-time-format.rst)
  - API behavior and statuses(general-api-info/api-behavior.rst)
  - Role-based access control (RBAC) (general-api-info/role-based-access-control.rst)- API reference
- API reference (api-reference/index.rst)
  - Template for a resource topic (api-reference/resource-one-method.rst)
  - Methods templates and examples (api-reference/methods)
    - API methods documentation guidelines (api-reference/methods/documentation-guidelines.rst)
    - Document an API method (api-reference/methods/method-template.rst)
    - Update an image (api-methods/methods/patch-update-image.rst)
    - List images (api-methods/methods/get-list-images.rst
- Release notes (release-notes/index.rst)
  - releases (release-notes/releases)
    - |release| Month DD, YYYY (release-notes/releases/release-notes-template.rst)
    - Example: API |contract version| release, March 19, 2015 (release-notes/releases/cn_v2_20150319.rst)
    - Example: API |contract version| release, September 30, 2014 (release-notes/releases/cn_v2_20140903.rst)
- Service updates (service-updates.rst)
- Additional resources (additional-resources.rst)
- Disclaimer (disclaimer.rst)

## Updating the files

Follow these steps to update the files in your new repo.

1.  Update the RST templates and indexes in the ``api-guide``
    folder with your content.

    Add or delete templates as necessary to fit your content.

2.  Update reference anchors, as needed. The reference anchors
    appear at the top of the file. Each topic must have a reference
    anchor if you want to link to that topic from another topic.
    Reference anchors must be unique across the project.

3.  Test your build locally as you add content to find and fix any errors.

    You can use ``tox``, which is set up when you set up publishing for your
    repo. You can also run the ``make.bat`` file, which is also set up at that
    time.

4. Check in your changes.

    When a PR is committed against your repo, the Jenkins server begins testing
    the PR. After it passes, a staging link appears in your PR, for example,
    https://github.rackspace.com/IX/docs-XXX/pull/6. Staging links are valid for
    14 days. Merging the PR publishes the doc to the production site, for example,
    https://pages.github.rackspace.com/IX/docs-XXX/. Until the production site is
    linked to the main landing page, Rackers must use the staging link to see the
    content, so you can continue to update and merge until the content is complete.

5.  When your doc is ready to be published to either the [internal
    docs landing
    page](https://pages.github.rackspace.com/IX/internal-docs-landing-page/)
    or the [external docs landing
    page](https://developer.rackspace.com/docs/), contact the [InfoDev
    Tools Team](mailto:mailto:infodev-tools@rackspace.com) to do the
    linking.

    After the linking is done, merging a PR against the repo updates the
    published content.

## Support and feedback

We welcome feedback, comments, and bug reports. Follow the
[contributor guidelines](https://github.rackspace.com/IX/docs-starter-kit/blob/master/CONTRIBUTING.md) to propose a source file change, or
[submit a GitHub issue](https://github.rackspace.com/IX/docs-starter-kit/issues)
to request an update or to provide feedback.

You can also contact the
[Rackspace documentation team](mailto:infodev@rackspace.com) directly for
general issues or questions about the content.
