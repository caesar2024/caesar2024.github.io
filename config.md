<!--
Add here global page variables to use throughout your website.
-->
+++
author = "Markus Petters and Jefferson Snider"
mintoclevel = 2

# Add here files or directories that should be ignored by Franklin, otherwise
# these files might be copied and, if markdown, processed by Franklin which
# you might not want. Indicate directories by ending the name with a `/`.
# Base files such as LICENSE.md and README.md are ignored by default.
ignore = ["node_modules/"]

# RSS (the website_{title, descr, url} must be defined to get RSS)
generate_rss = false
website_title = "CAESAR-2024"
website_descr = "Cold-Air Outbreak Experiment"
website_url   = ""
+++

<!--
Add here global latex commands to use throughout your pages.
-->
\newcommand{\R}{\mathbb R}
\newcommand{\scal}[1]{\langle #1 \rangle}

\newcommand{\concept}[1]{@@concept @@title **✔ Key Concept**@@ @@content #1 @@ @@}
\newcommand{\outline}[1]{@@outline @@title **✎ Lecture Outline**@@ @@content #1 @@ @@}
\newcommand{\mathnote}[1]{@@note @@title **✎ Mathematical Representation**@@ @@content #1 @@ @@}
\newcommand{\learning}[1]{@@learning @@title **⏻ Learning Objectives**@@ @@content #1 @@ @@}
\newcommand{\caution}[1]{@@warning @@title **⚠ Caution**@@ @@content #1 @@ @@}
\newcommand{\exercise}[1]{@@exercise @@title **？ Exercise**@@ @@content #1 @@ @@}

