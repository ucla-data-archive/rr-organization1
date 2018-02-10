---
title: "File Organization: Naming"
teaching: 30
exercises: 10
questions:
- "What are the common file organization errors?"
- "What are best practices for file organization?"
objectives:
- "Highlight common SNAFUs"
- "Learn to employ unit testing"
keypoints:
- "File organization is important."
output:  
      html_document
---

## Names matter

### NO
```
myabstract.docx
Joe’s Filenames Use Spaces and Punctuation.xlsx
figure 1.png
fig 2.png
JW7d^(2sl@deletethisandyourcareerisoverWx2*.txt
```

### YES
```
2014-06-08_abstract-for-sla.docx
joes-filenames-are-getting-better.xlsx
fig01_scatterplot-talk-length-vs-interest.png
fig02_histogram-talk-attendance.png
1986-01-28_raw-data-from-challenger-o-rings.txt
```

## Three principles for (file) names:

1. Machine readable
1. Human readable
1. Plays well with default ordering

***
### Awesome file names :)

<img src="../fig/awesome_names.png" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" width="500px" style="display: block; margin: auto;" />

***
### Machine readable


#### Machine readable

- Regular expression and globbing friendly
    - Avoid spaces, punctuation, accented characters, case sensitivity
    - Easy to compute on

- Deliberate use of delimiters

***
#### Globbing

**Except of complete file listing**:

<img src="../fig/plasmid_names.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="500px" style="display: block; margin: auto;" />

*** 
**Example of globbing to narrow file listing**:

<img src="../fig/plasmid_names.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" width="500px" style="display: block; margin: auto;" />

***
**Same using Mac OS Finder search facilities**:

<img src="../fig/plasmid_mac_os_search.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="700px" style="display: block; margin: auto;" />

***
**Same using regex in `R`**:

<img src="../fig/plasmid_regex.png" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" width="600px" style="display: block; margin: auto;" />

***
#### Punctuation

Deliberate use of "-" and "_" allows recovery of meta-data from the filenames:

- "_" underscore used to delimit units of meta-data I want later.
- "-" hyphen used to delimit words so my eyes don't bleed.

<img src="../fig/plasmid_delimiters.png" title="plot of chunk unnamed-chunk-6" alt="plot of chunk unnamed-chunk-6" width="600px" style="display: block; margin: auto;" />

***
<img src="../fig/plasmid_delimiters_code.png" title="plot of chunk unnamed-chunk-7" alt="plot of chunk unnamed-chunk-7" width="600px" style="display: block; margin: auto;" />

This happens to be `R` but also possible in the `shell`, `Python`, etc.

***
### Recap: machine readable

- Easy to search for files later
- Easy to narrow file lists based on names
- Easy to extract info from file names, e.g. by splitting
- New to regular expressions and globbing? Be kind to yourself and avoid
- Spaces in file names
- Punctuation
- Accented characters
- Different files named `foo` and `Foo`

### Human readable

#### Human readable

- Name contains info on content
- Connects to concept of a *slug* from semantic URLs

*** 
#### Example

**Which set of file(name)s do you want at 3 a.m. before a deadline**?

<img src="../fig/human_readable_not_options.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="500px" style="display: block; margin: auto;" />

***
#### Embrace the *slug*

<img src="../fig/slug.jpg" title="plot of chunk unnamed-chunk-9" alt="plot of chunk unnamed-chunk-9" width="400px" style="display: block; margin: auto;" />

<img src="../fig/slug_filenames.png" title="plot of chunk unnamed-chunk-10" alt="plot of chunk unnamed-chunk-10" width="400px" style="display: block; margin: auto;" />

***
#### Recap: Human readable

Easy to figure out what the heck something is, based on its name

***

### Plays well with default ordering

#### Plays well with default ordering

- Put something numeric first
- Use the ISO 8601 standard for dates
- Left pad other numbers with zeros

#### Examples

**Chronological order**:

<img src="../fig/chronological_order.png" title="plot of chunk unnamed-chunk-11" alt="plot of chunk unnamed-chunk-11" width="600px" style="display: block; margin: auto;" />

***
**Logical order**: Put something numeric first

<img src="../fig/logical_order.png" title="plot of chunk unnamed-chunk-12" alt="plot of chunk unnamed-chunk-12" width="600px" style="display: block; margin: auto;" />

***

**Dates**: Use the ISO 8601 standard for dates: YYYY-MM-DD

<img src="../fig/chronological_order.png" title="plot of chunk unnamed-chunk-13" alt="plot of chunk unnamed-chunk-13" width="600px" style="display: block; margin: auto;" />

***

<img src="../fig/map_mmddyyy.tiff" title="plot of chunk unnamed-chunk-14" alt="plot of chunk unnamed-chunk-14" width="600px" style="display: block; margin: auto;" />

[From twitter](https://twitter.com/donohoe/status/597876118688026624)

***
**Left pad other numbers with zeros**

<img src="../fig/logical_order.png" title="plot of chunk unnamed-chunk-15" alt="plot of chunk unnamed-chunk-15" width="600px" style="display: block; margin: auto;" />

If you don’t left pad, you get this:

```
 10_final-figs-for-publication.R
 1_data-cleaning.R
 2_fit-model.R
```

which is just sad :(

***
#### Recap: Plays well with default ordering

- Put something numeric first
- Use the ISO 8601 standard for dates
- Left pad other numbers with zeros

### Recap

*** 
#### Three principles for (file) names

1. Machine readable
1. Human readable
1. Plays well with default ordering

#### Pros

- Easy to implement NOW
- Payoffs accumulate as your skills evolve and projects get more complex.

***
Go forth and use awesome file names :)

<img src="../fig/chronological_order.png" title="plot of chunk unnamed-chunk-16" alt="plot of chunk unnamed-chunk-16" width="600px" style="display: block; margin: auto;" />

<img src="../fig/logical_order.png" title="plot of chunk unnamed-chunk-17" alt="plot of chunk unnamed-chunk-17" width="600px" style="display: block; margin: auto;" />
