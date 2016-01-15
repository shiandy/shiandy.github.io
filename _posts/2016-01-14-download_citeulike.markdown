---
title: Citation Management
layout: post
---

In this post, I'll show how to automate downloading citations from Citeulike
into BibTeX files.

<!--more-->

I've started writing my senior thesis, so I've started looking for a way to
manage all my sources. My thesis is being written in LaTeX, so using BibTeX was
an obvious choice. BibTeX uses a .bib file to hold information about all your
sources: see [here](https://en.wikibooks.org/wiki/LaTeX/Bibliography_Management)
for more details. You can populate this .bib file by hand, but it's easier to
use a citation manager. I went with [Citeulike](http://www.citeulike.org/).

You can give Citeulike a link to a journal article, a DOI, or a Pubmed ID, and
it will automatically gather relevant information. You can export your citations
to a .bib file, which is compatible with LaTeX. Even better, you can automate
this retrieval process, since Citeulike allows you to access your citations
using URLs, which can be processed with tools like wget or curl.

I wrote a [Python script
(link)](https://gist.github.com/shiandy/f7d53f7061748e599e10) to automate
fetching a BibTeX file for all your citations, based off [these wget
commands](http://linuxtoosx.blogspot.com/2012/10/downloadbackup-citeulike-library.html).

The script uses your Citeulike username and password to log in and then download
the .bib file. You need to log in, otherwise you would only be able to access
citation entries you made "public." The URL for accessing the .bib file is

    http://www.citeulike.org/bibtex/user/USERNAME

where USERNAME is your username.

Additionally, Citeulike allows you to tag your citation entries. If you use
Citeulike for multiple projects, you can have a tag for each project and
download the .bib file for the project with tag TAG using the following URL:

    http://www.citeulike.org/bibtex/user/USERNAME/tag/TAG

My script supports both these functions. The `-o` and `-t` arguments are
optional but can be used to change the output filename and what tag to use.

    usage: download_citations.py [-h] [-o OUTPUT] [-t TAG]

    Download bibtex citation file from citeulike.

    optional arguments:
      -h, --help            show this help message and exit
      -o OUTPUT, --output OUTPUT
                            Bibtex output file name. Default: export.bib
      -t TAG, --tag TAG     Which tag to use. By default, no tags are used.

You'll need to set the USERNAME and PASSWORD variables to your own Citeulike
username and password, respectively, before continuing. Using this script you
can automate fetching those bibliography files and make sure your citations are
up to date. Enjoy!

**Caveat**: Citeulike's security certificate expired on June 8, 2015 and hasn't
been renewed since, so I am using non-secure HTTP, not HTTPS, to log in. It's
probably best if you use a different password for Citeulike so that people can't
steal your Facebook/email/bank passwords.

<script src="https://gist.github.com/shiandy/f7d53f7061748e599e10.js"></script>

<noscript>Please enable Javascript to see a preview of this code, or <a
href="https://gist.github.com/shiandy/f7d53f7061748e599e10">view it on
Github</a>.</noscript>
