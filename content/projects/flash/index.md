---
title: "Flash Search Engine 🔦"
draft: false
description: "Full-text search engine for Ubuntu written in Go"
hideSummary: false
ShowReadingTime: true
ShowBreadCrumbs: true
cover:
    image: "cover.webp"
    alt: "Flash screenshot"
---

<a href="https://github.com/Andy9oo/flash">
    <img id="github" style="margin: auto" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" />
</a><br/>

Flash is a full-text desktop search engine, designed to help users find their files. Using preprocessing techniques, flash creates an index that allows the user to search without the need to crawl the filesystem; substantially reducing search times. Flash is written purely in Go to allow for the use of concurrency during preprocessing and search.

There are several other tools that a user can use to search their file system, such as `find` and `grep`. These tools work well for specific use cases; however, they each have drawbacks. `find` can only search for file names, and `grep` has to crawl the file system for each search.

Flash solves both of these problems, by building an inverted index to perform a full-text search over the file system, without the need to crawl it each time. Comparing its performance to `grep` (as shown below), `flash` can search various datasets in near-constant time, well outperforming grep and providing a much better user experience. 

{{<figure src="./grep.webp">}}

In addition to the command line interface shown above `flash` has a GUI, which was developed using the GTK3 framework, that a user can use to quickly find files. The `flash gui` command can be bound to any keyboard shortcut to quickly bring up the search box, shown below.

{{<figure src="./results.webp">}}

To get started with flash, follow the instructions listed on the [github page](https://github.com/Andy9oo/flash).