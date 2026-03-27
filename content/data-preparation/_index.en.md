---
title: Data Preparation
date: 2018-12-29T11:02:05.000+06:00
icon: ti-layout-grid4
description: Formatting requirements for databases
type: docs
weight: "3"

---
***

<img src="/uploads/tidying.jpg" style="width: 100%;height: 250px;object-fit: cover;
 border-radius: 5px; border: 3px solid white; margin: 30px 0;">

<br>

This documentation section describes how the databases included in MetaCIH are prepared.

Before being released, all data is converted into a consistent, **standardized format**. This format ensures that data is compatible with other components of the MetaCIH infrastructure.

All released databases live in their own online [Github](https://github.com/) repository. These repositories are hosted by the [`metacih-project`](https://github.com/metacih-project) organization account. All database repository names start with `data-`, followed by the [shorthand](https://docs.metapsy.org/databases/#shorthand) of the database (e.g. `data-depression-psyctr`).

All MetaCIH databases hosted on Github follow the same folder structure. In particular, a [**metadata**](/data-preparation/metadata/) folder is included in each repository. This folder contains additional information associated with the dataset (e.g. the search date, the number of studies, or a variable description).

After a new database version has been uploaded to Github, data validators are used to check if the format conforms to the standard required by other components of the MetaCIH infrastructure (e.g. <!-- `metapsyData` and  -->`metapsyTools`).

Finalized database repositories are then officially [**released**](/release) via the Github Zenodo integration.

<br></br>