---
layout: post
title: "Some useful latex hacks"
date: 2018-04-28
---
Here are some ideas and tricks I found useful when working with latex.

## include .pdf in your latex document or beamer
Have you ever considered reading in figures directly from pdf? No? Do it, it is really nice and if you present a paper, it prevents you from having thousands of small files with screenshots of the paper's figures!

### Here is how it works in latex beamer:
```latex
\begin{frame}{<Nameofyourframe>}
\begin{figure}
    \includegraphics[page=1,clip, trim={50 100 50 130},width=\textwidth]{<pathtoyourpaper>/<yourpaper.pdf>}
    \caption*{<yourcaption>}
\end{figure}
\end{frame}
```
notice that : ` trim={<left> <lower> <right> <upper>}`.

To be even more convenient, put a frame around your image, so you see much better where the image boarders are (and where the white background of your latex file begins). Therefore, you can just

`\frame{\includegraphics[page=1,clip, trim={50 100 50 130},width=\textwidth]{<pathtoyourpaper>/<yourpaper.pdf>}`

## Work with excel to make your latex tables
If I have large tables with long entries, I find it quite useful to first create it in an excel document. Once the table is finished, I create a new "latex-style" table with the excel function `CONCATENATE` witch does string concatenation, for example:
´´´
=CONCATENATE(B4, " & ")
´´´
I also found this link https://www.tablesgenerator.com/markdown_tables where you can generate a markdown table. What I try to encourage you here is to program something alike yourself in excel.
The result looks like this:
before :
```
bla	bla	bla
bla	bla	bla
bla	bla	bla
bla	bla	bla
bla	bla	bla
bla	bla	bla
bla	bla	bla
```
after :
```
bla & 	bla & 	bla \\
bla & 	bla & 	bla \\
bla & 	bla & 	bla \\
bla & 	bla & 	bla \\
bla & 	bla & 	bla \\
bla & 	bla & 	bla \\
bla & 	bla & 	bla \\

```
very easy and handy.

## Create figures in your latex beamer
Libre Office Impress or Power point are very handy for flowcharts or some other square-arrow shapes.
To create those in latex beamer, I use the package TikZ:
[TikZ](https://de.sharelatex.com/blog/2013/08/27/tikz-series-pt1.html).

## Creating a .bib file
The tedious thing about citing is usually the part of typing in the paper metadata. To prevent this, I usually research the paper I would like to cite either at the official website or in google scholar. There is a button for citing, where the BibTex formatted citation info can be copied out so you can directly paste it into your .bib file.

Here is an example for a Science paper:
![bibtex1]({{ "/assets/bibtex1.jpg" | absolute_url }})
![bibtex2]({{ "/assets/bibtex2.jpg" | absolute_url }})
![bibtex3]({{ "/assets/bibtex3.jpg" | absolute_url }})
