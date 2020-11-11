<!-- README.md is generated from README.Rmd. Please edit that file -->

# here

<!-- badges: start -->

[![Lifecycle: stable](https://img.shields.io/badge/lifecycle-stable-brightgreen.svg)](https://www.tidyverse.org/lifecycle/#stable) [![rcc](https://github.com/r-lib/here/workflows/rcc/badge.svg)](https://github.com/r-lib/here/actions) [![CRAN status](https://www.r-pkg.org/badges/version/here)](https://CRAN.R-project.org/package=here) [![Codecov test coverage](https://codecov.io/gh/r-lib/here/branch/master/graph/badge.svg)](https://codecov.io/gh/r-lib/here?branch=master)

<!-- badges: end -->

The goal of the here package is to enable easy file referencing. In contrast to using [`setwd()`](https://rdrr.io/r/base/getwd.html), which is fragile and dependent on the way you organize your files, here uses the top-level directory of a project to easily build paths to files.

## Installation

Install the released version of here from CRAN:

<pre class='chroma'>
<span class='nf'><a href='https://rdrr.io/r/utils/install.packages.html'>install.packages</a></span><span class='o'>(</span><span class='s'>"here"</span><span class='o'>)</span></pre>

## Usage

The here package creates paths relative to the top-level directory. The package displays the top-level of the current project on load or any time you call `here()`:

<pre class='chroma'>
<span class='kr'><a href='https://rdrr.io/r/base/library.html'>library</a></span><span class='o'>(</span><span class='nv'><a href='https://github.com/r-lib/here'>here</a></span><span class='o'>)</span>
<span class='c'>#&gt; here() starts at /home/kirill/git/R/here</span>
<span class='nf'><a href='https://here.r-lib.org//reference/here.html'>here</a></span><span class='o'>(</span><span class='o'>)</span>
<span class='c'>#&gt; [1] "/home/kirill/git/R/here"</span></pre>

You can build a path relative to the top-level directory in order to read or write a file:

<pre class='chroma'>
<span class='nf'><a href='https://here.r-lib.org//reference/here.html'>here</a></span><span class='o'>(</span><span class='s'>"files"</span>, <span class='s'>"data"</span>, <span class='s'>"iris.csv"</span><span class='o'>)</span></pre>
<pre class='chroma'>
<span class='nf'><a href='https://rdrr.io/r/utils/write.table.html'>write.csv</a></span><span class='o'>(</span><span class='nv'>iris</span>, <span class='nf'><a href='https://here.r-lib.org//reference/here.html'>here</a></span><span class='o'>(</span><span class='s'>"files"</span>, <span class='s'>"data"</span>, <span class='s'>"iris.csv"</span><span class='o'>)</span><span class='o'>)</span></pre>

These relative paths work regardless of where the associated source file lives inside your project, like analysis projects with data and reports in different subdirectories.

![](https://raw.githubusercontent.com/allisonhorst/stats-illustrations/master/rstats-artwork/here.png) *Illustration by [Allison Horst](https://github.com/allisonhorst)*

------------------------------------------------------------------------

## Code of Conduct

Please note that the here project is released with a [Contributor Code of Conduct](https://here.r-lib.org/CODE_OF_CONDUCT.html). By contributing to this project, you agree to abide by its terms.
