+++
keywords = ["pull", "github", "upload"]
title = "Upload"
weight = 3

+++
***

Following the data preparation according to the MetaCIH data standard, all files are collected in a Github repository. The standard folder structure can be seen below:

<br>

* 💾 **`data.csv`**
* 📄 **`license`**
* 📄 **`readme.md`**
* 📁 **`metadata`**
  * 📄 **`authors.json`**
  * 📄 **`last_search.txt`**
  * 📄 **`number_studies.txt`**
  * 📄 **`references.json`**
  * 📄 **`search_string.txt`**
  * 📄 **`search_flow.json`**
  * 📄 **`shorthand.txt`**
  * 📄 **`variable_description.json`**

<br>

All database repositories are hosted by the [`metacih-project`](https://github.com/metacih-project) organization account. The repository name is also standardized: it is `data-`, followed by the [shorthand](/databases/#shorthand) of the database (e.g. `data-depression-psyctr`).

In the "About" section on the Github repository page, one can find a brief description of the database, as well as a link to the specific [database documentation](/databases/) entry.

Once a repository has been created (or updated) this way, an official database [release](/release/) is published. This workflow is documented in the next section.

<br></br>