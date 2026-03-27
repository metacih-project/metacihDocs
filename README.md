# Repository of the MetaCIH documentation website

This is the code repository of the [docs.metacih.org](incandescent-fudge-873e29.netlify.app) documentation website. 📄
To check if new releases have been built correctly by [Netlify](https://www.netlify.com/), click on the badge below:

[![Netlify Status](https://api.netlify.com/api/v1/badges/9f38bde6-99f8-4fe5-8dac-af7b89e4372e/deploy-status)](https://app.netlify.com/projects/metapsydocs/deploys)


## 🔄 Updating the Documentation Database

The MetaCIH Documentation webpage uses a **static snapshot of all the MetaCIH metadata released to Zenodo**, which is saved to a JSON library (`/data/zenodo.json`).
This snapshot does not update automatically. Instead, we can refresh it manually whenever there are new releases.

### How it works

1. The GitHub Action **“Refresh Documentation Database”** downloads the latest version of the documentation database.
2. It saves this into `static/data/zenodo.json`.
3. If the file has changed, the Action **creates a commit on `master`** with the updated data.
4. That commit triggers a new **Netlify build**, so the website updates automatically.
5. If there are **no changes** in the database, nothing happens (no commit, no build).

### How to trigger a refresh

1. Go to the **Actions** tab in GitHub.
2. Select **“Refresh Documentation Database”**.
3. Click **“Run workflow”** (make sure the branch is `master`).
4. Wait \~1 minute for the workflow to finish.

   * ✅ If the database changed → a commit appears in `master` called
     `chore: refresh documentation database snapshot`.
   * ℹ️ If nothing changed → no commit is made.

## 🖌️ Using the Netlify CMS

The MetaCIH documentation site is built using [Hugo](https://gohugo.io/). We have created a **Content Management System (CMS)** for the website, which is provided on [docs.metapsy.org/admin](https://docs.metapsy.org/admin). If you want to have access to the backend, please approach [@PaulaKuper](www.github.com/PaulaKuper).


The forestry CMS provides you with a **code-free, visual text editor**. Using the CMS, you can change existing content, add new pages and entries, and upload media files.  After clicking on **save**, set the status to **ready**, and then click on **publish now**. Your changes are then **automatically deployed to this [Github repository](www.github.com/metapsy-project/metapsyDocs)**, and then released to the website shortly after.

### Pre-Defined Elements

Besides the visual editing functionality, there are also several **elements** that you can add to the documentation page via **shortcodes**. Here is an overview of the most important ones:


#### Zenodo DOI Badge 🛡️

Simply provide the "overall" (not version-specific) DOI created for the dataset or package. The badge will also automatically contain a link to the Zenodo repository.

```
{{< zenodo-badge doi="<INSERT DOI>" >}}
```

#### Zenodo GitHub Release Link 😺

Simply provide the "overall" (not version-specific) DOI created for the dataset or package.
The link text to be displayed can be specified in `text`.

```
{{< zenodo-github-release doi="<INSERT DOI>" text="link" >}}
```

#### Zenodo Last Update Date 📅

Simply provide the "overall" (not version-specific) DOI created for the dataset or package.

```
{{< zenodo-last-updated doi="<INSERT DOI>" >}}
```

#### Zenodo Last Search Date 🔍

Simply provide the "overall" (not version-specific) DOI created for the dataset or package.

```
{{< zenodo-last-search doi="<INSERT DOI>" >}}
```

#### Zenodo Latest Version 🔢

Simply provide the "overall" (not version-specific) DOI created for the dataset or package.

```
{{< zenodo-version doi="<INSERT DOI>" >}}
```

#### Zenodo "Browse All Versions" Block 🔢

Simply provide the "overall" (not version-specific) DOI created for the dataset or package.

```
{{< zenodo-all-versions doi="<INSERT DOI>" >}}
```

#### Zenodo Database Authors ✍🏽

Simply provide the "overall" (not version-specific) DOI created for the dataset or package.

```
{{< zenodo-authors doi="<INSERT DOI>" >}}
```

#### Zenodo Variable Description 📓 

Simply provide the "overall" (not version-specific) DOI created for the dataset or package.

```
{{< zenodo-variable-description doi="<INSERT DOI>" >}}
```


#### Note Box 🗒️

```
{{< notice note >}}
This is a simple note.
{{< /notice >}}
```

#### Tip Box 💡

```
{{< notice tip >}}
This is a simple tip.
{{< /notice >}}
```

#### Info Box ℹ️

```
{{< notice info >}}
This is a simple info.
{{< /notice >}}
```

#### Warning Box ⚠️

```
{{< notice warning >}}
This is a simple warning.
{{< /notice >}}
```

#### Tabs 📂

```
{{< tabs >}}

{{< tab "first" >}}
This is first tab
{{< /tab >}}

{{< tab "second" >}}
this is second tab
{{< /tab >}}

{{< tab "third" >}}
this is third tab
{{< /tab >}}

{{</ tabs >}}

```

#### R Code Chunk

To create an R code chunk, start with three [backticks](https://www.wikiwand.com/en/Backtick) and `r`, and end your code example with three backticks.

#### Tables 📈

Colons can be used to align columns.

```
| Tables        |      Are      |  Cool |
| ------------- | :-----------: | ----: |
| col 3 is      | right-aligned | $1600 |
| col 2 is      |   centered    |   $12 |
| zebra stripes |   are neat    |    $1 |
```

There must be at least 3 dashes separating each header cell.
The outer pipes (`|`) are optional, and you don't need to make the
raw Markdown line up prettily. You can also use inline Markdown.

```
| Markdown | Less      | Pretty     |
| -------- | --------- | ---------- |
| _Still_  | `renders` | **nicely** |
| 1        | 2         | 3          |
```

### Media Upload

Using the `Media` menu in the CMS, you can upload images, PDFs, files etc. After the upload, files are saved in the `images/uploads` folder. So, if you want to use e.g. `sample.pdf` in a documentation entry, you have to use `images/uploads/sample.pdf` as the URL. 

**Please note that all uploads go directly into the Github repo of this website!** So please only upload files that are actually used in the documentation, and make sure that the size is below 50MB.

### Attribution

The website uses the [dot-hugo](https://github.com/themefisher/dot-hugo) theme as basis. 








