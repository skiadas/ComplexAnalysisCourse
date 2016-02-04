# Learning LaTeX

LaTex, pronounced "lay-tech", is a typesetting software particularly suitable for scientific writing. Some of its key features are:

1. Excellent support for properly writing mathematical equations.
2. Advanced algorithms for spacing between words, lines and sentences to properly justify text without leaving unnecessarily large spaces and to provide suitable page breaks.
3. You focus on writing your content and identifying its structural importance, and the formatting is taken care of uniformly through global settings.
4. In LaTeX you control a lot of the behavior via "commands", that all start with a backslash, `\`.
5. LaTeX is not a "what-you-see-is-what-you-get" editor. You end up sort of writing "code" intermingled with text. Lots of tools like [OverLeaf](overleaf.com) make that a bit more palatable. The programming language that LaTeX supports is strong enough to compute for instance prime numbers, though few people use those advanced features.
5. The final format is typically a PDF file.

## Starting a file

We will be using [OverLeaf](overleaf.com), that offers an easily accessible interface to LaTeX. If you would rather install software on your computer to work with LaTeX, contact me and we'll see what we can arrange.

We will work through many of the things you will need in this document. There are many online resources as well. The documents at [this page](https://www.sharelatex.com/learn/) that don't refer specifically to ShareLaTeX features are well organized and relevant to us. And you should always feel free to ask me if you are not sure how to do something.

1. You should all already have OverLeaf accounts (there is a free option), go ahead and log in.
2. You should see an option "MyProjects" near the top, select it. Then click on "new project". It should offer you a choice of templates to work with, for now we will go with the "Blank Paper" template that is the first item in Basics. This will start a new file for you with nothing in it.
3. You should see two windows. The left side is where we write stuff, and the write sides shows us what it looks like. You can use the arrows near the dividing line to expand one of the two sides to full screen. You can also drag the dividing line left or right to change the size of each section.
4. LaTeX documents have two main parts, the **preamble** and the **main document**. The preamble is used to provide instructions to the system. The main document is where you put the text you want to have show up.

## Preamble

In the blank document, add the following:

```
\documentclass[12pt]{article}
\usepackage[vmargin=0.5in, hmargin=0.5in]{geometry}
\usepackage[T1]{fontenc}
\usepackage{stix}

\usepackage{paralist}
\usepackage{attrib}

\usepackage{amsmath}
\usepackage{amsthm}

\title{Place your title here}
\author{Put your name here}
\date{\today}

\begin{document}
\maketitle

Some text here
\end{document}
```

If all has worked well, you should see on the right-side a rendering of your document, showing the title, the name and some text. Everything else is invisible but gives instructions to the system for various things. We will discuss them in a minute.

### Document classes and packages

The content between the lines `\begin{document}` and `\end{document}` is the "main document". This is where you will be putting most of your work. The stuff that comes earlier is the preamble.

The first line in the document is always a `\documentclass` line. In this case it tells the system that it should use the format rules for an article, which specifies title size, author and date placement, and other stylistic choices. In this case we also tell it that we want the base font size to be 12 points. Unfortunately you do not have too many options for the font size 12 points is the largest that it can go.

Then we have a couple of `\usepackage` commands that load packages that do useful things. The first one is the "geometry" package, which allows you to control the margins of the page. Try to change the numbers to see the effect. "hmargin" is for horizontal margins, "vmargin" controls vertical margins. You can use different measuring units rather than inches, for instance `1cm` will create 1 centimeter spacing. All this information within the square brackets is called the "package options".

Notice a bit further down a `\usepackage{paralist}`. This allows us to customize lists later on. And `\usepackage{attrib}` allows attributions in quotes, if you ever need those.

### Fonts

The next two lines set up an appropriate font, in this case a font called Stix. I encourage you not to do this right now, but you can find a long list of available fonts as well as the instructions for how to enable them [here](http://www.tug.dk/FontCatalogue/). Aim for the section that says "Fonts with math support". You can only have one font choice per document, without a fair bit of extra work.

You will find that LaTeX makes some things hard. For instance, if you want different parts of your text to have different fonts, it is not easy to do. LaTeX aims to provide you uniform styles, and gives you control over setting those uniform styles, but doesn't allow you to deviate a lot. The main stylistic choices you have are:

1. Normal text. This is what happens most of the time. You can also use `\textrm{normal text here}` in situations where normally typing text would not treat it as normal.
2. Italic text, indicated by the command `\emph{put the text you want italic here}`. It will also automatically enable italic text in certain settings like theorem statements, depending on the document class setting. In those instances, the above command will make the text in it normal, i.e. it always makes it "stand out from its surrounding text". You can also use `\textit{italic text here}`.
3. Bold text, indicated by the command `\textbf{put the text you want bold here}`.
4. Math mode. We will discuss this later, but you can enter a math mode where normal text rules are suspended. A specific math font is used in those instances.

### Document info

After the font specifications there are a couple of lines that define information about the document, in this case a title, the author, and a date specification to automatically pick up today's date. You could just instead write out a specific date as you want it to appear, instead of `\today`.

There are many more things we can put in the preamble. But for now this will suffice.

## The main document

The main document is contained within the block created by the `\begin{document}` and `\end{document}`. Everything you type there is going to appear as text on the right, but there are some important rules to keep in mind:

1. Backslashes and curly braces have special meaning, as do dollar signs. If you need to insert any of those into the text for some reason, you need to prepend them with a backslash, for instance `\{` or `\$` or `\\`.
2. Multiple spaces are ignored and treated as one space. LaTeX automatically adjusts the spacing between words to achieve the best possible result, including extra spaces after the ends of sentences.
3. Newlines are ignored, unless there are at least 2 of them back to back. So in order to start a new paragraph you have to hit "return" twice. Like so:
    ```
    A paragraph here

    A new paragraph here
    ```
4. There are special ways for creating section headings and for creating itemized or enumerated lists. We will be discussing these shortly.
5. There are two ways to enter "math mode". We will also be discussing theses shortly. All your mathematics should be done in this mode.

### Sections

There are special commands to use when you want to start a new section, subsection etc. For articles, the options we have are *section*, *subsection*, *subsubsection*, *paragraph* and *subparagraph*. Each of these has a corresponding command, with a backslash in front, and then in braces you put the name of the section. So here is some example text, type (or copy-paste) it in and see how it looks:

```
\section{This is a section heading}
Stuff about the first section in here. The settings for how these headings appear are set globally, and you should not try to change them.
\subsection{A subsection within the first section}
Stuff about the subsection. Notice that the subsection is numbered within the section.
\subsection*{An unnumbered subsection}
You can disable the numbering on any of these elements by putting the star before the curly brace like in the line above.
\subsubsection{A sub-subsection}
Subsubsection text.
\paragraph{A paragraph}
Some paragraph text. Notice that paragraphs and subparagraphs do not follow the numbering.

"Paragraph" here just means a part of the text identified as a unit smaller than a subsubsection. It does not need to be a literal paragraph. But it is convenient to use for paragraphs that have a "title".
\subparagraph{A subparagraph}
Subparagraph text.
You really do not need to use all those 5 different levels. But they are available.
```

### Lists

There are three kinds of lists you can make in LaTeX: Numbered (enumerated) lists, itemized ("bullet") lists and "description lists". Here's some examples, paste them in the text to see how they would look:
```
Lists start and end with a begin-end block:
\begin{enumerate}
    \item This is the first item in the list. Notice that the numbering started automatically at 1. You can customize that if you need to, but you should not have to. We will now start a sublist within this first item: We indented it a bit to remind us of the fact that it's a sublist, but LaTeX won't care either way.
   \begin{enumerate}
      \item Here's a subitem.
      \item Another subitem.
   \end{enumerate}
   We will now make another sublist that is formatted slightly differently. Notice the i and dot, telling it to use latin numerals and a dot instead of a parenthesis:
   \begin{enumerate}[i.]
      \item First!
      \item Second!
      \item[Hey!] You can interrupt the numbering by inserting whatever you want in brackets, and it will replace the number. But use this sparringly.
   \end{enumerate}
   \item Here's a second item on the main list.
   \begin{itemize}
      \item And here's a bullet list.
      \begin{itemize}
         \item And one inside it.
      \end{itemize}
      \item A second item.
   \end{itemize}
   You can also make lists with less space between the items:
   \begin{compactenum}
      \item See.
      \item We're close!
      \item you can also try replacing "compactenum" at the begin/end with "asparaenum" and "inparaenum" and see how they look like.
      \item You also have the choices of "compactitem", "asparaitem", "inparaitem".
   \end{compactenum}
\end{enumerate}

Description lists expect each item to have a "term" and a "description" like so:
\begin{description}
\item[A term] The term's description.
\item[Another] They are formatted this way.
\end{description}
You can also try "compactdesc", "asparadesc" and "inparadesc".
```

### Quotes

If you want to suggest a "quote", there are two possible "environments", quote and quotation. Paste the following in to see their difference:
```
Quote:
\begin{quote}
A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line.
\attrib{The author}

Starting a new paragraph. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line.
\end{quote}
Quotation:
\begin{quotation}
A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line.
\attrib{The author}

Starting a new paragraph. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line. A long text here to make sure we move to a new line.

\end{quotation}
```

### Other normal text features

Here are some other features when writing "normal" text. Just paste them in and see the effect:
```
Use two backticks ``to start a left double-quote, and two single quotes to close it''. This will insert better looking quotes than if you use the "normal double-quote" character. Do the same for `single quotes'.

Using consecutive dashes has the effect of producing what is known as an "en-dash" (--) or an "em-dash" (---).
```

### Theorems, corollaries, proofs

There are a number of provided environments for creating standard math document sections like a theorem statement, a proof and so on. Most of these were loaded with the "amsthm" package that was loaded at the preamble. Here's some example uses. You can read a lot more about what this package provides at its [documentation page](ftp://ftp.ams.org/pub/tex/doc/amscls/amsthdoc.pdf), but we'll discuss the main things you'll need in these notes, and the next section which focuses on writing math.

You should first add the following lines to the preamble, below the `\usepackage{amsthm}` line:
```
\theoremstyle{plain}
\newtheorem{theorem}{Theorem}[section]
\newtheorem{lemma}[theorem]{Lemma}
\newtheorem{corollary}[theorem]{Corollary}
\theoremstyle{remark}
\newtheorem*{remark}{Remark}
\newtheorem*{note}{Note}
\theoremstyle{definition}
\newtheorem{definition}{Definition}[section]
```

The lines above created 5 new environments:

1. `theorem`, which prints "Theorem" and is numbered within sections.
2. `lemma` and `corollary`, which both follow the theorem's numbering.
3. `remark` and `note`, both unnumbered.

Here's an example of using these. Paste it in the main document section to see how it looks. You also will see how we can add a "proof" with the special nice box at the end.
```
\begin{theorem}
Here's the theorem's statement. Notice the numbering, which is based on the section number.
\end{theorem}
\begin{proof}
Here is where we would write the proof.

This could take many pages. We will learn how to put math here in the next section.
\end{proof}
\begin{corollary}
See how the numbering of this corollary follows the theorem's numbering.
\end{corollary}
\begin{lemma}
Lemmas also follow the numbering from theorem.
\end{lemma}
\begin{proof}
And here's the lemma's proof.
\end{proof}
Now let's add a remark:
\begin{remark}
Here is the remark's text. Notice how the remarks are formatted differently than the previous items. That is because we had a line about a different "theoremstyle" in the preamble where we defined the remark environment.
\end{remark}
\begin{definition}
And here is a definition. Notice that its style is different from both of the previous two style. And it follows an independent numbering from the theorems lemmas etc, but still below sections.
\end{definition}
```

### Mathematics

Now we discuss how to write mathematics in LaTeX, one of its main strengths. There are two different math modes:

- *inline math* mode, which you use to add math within normal text. You can start math mode by `\(` and close it by `\)`. You can also use one dollar sign to open and close, but you should use the backslashed parentheses instead.
- *display math* mode, which you use for equations that are not meant to be in the middle of text but their own. You typically start and end display math mode by typing `\[` and `\]`. There are also other ways to create more complicated math environments, as well as ways to number the equations for later reference.

A lot of things are different in either math mode:

- Text has a different meaning. Putting letters next to each other does not make them form words; they are instead treated as the individual variables that are multiplied together.
- All spaces are basically ignored. spacing in math formulas is automatically controlled by the system. There are a few ways to manipulate it if you really feel you need the space, ask me about it if you do.
- Use an underscore to indicate a subscript and a "hat" `^` to indicate superscripts. If you want to put more than one character as subscript or superscript, enclose it in curly braces. In general curly braces group together things you want to treat as "one".
- There are numerous commands for producing special symbols. You can find many of them in the [amsmath documentation](ftp://ftp.ams.org/pub/tex/doc/amsmath/amsldoc.pdf) and the [comprehensive LaTeX symbol list](http://tug.ctan.org/info/symbols/comprehensive/symbols-a4.pdf). In the sample below we will demonstrate the most common ones. If you can't find a symbol, just ask.
- If you really need to add some plain text in a math equation, use `\textrm{...}`.

Here's some sample text. Paste it in to see how it looks:
```
Here's an inline equation: \( e^{x + \frac{2}{x}} \).
Here's some display math:
\[
   \cos x + i \sin x
\]
You can create numbered equations by using the equation environment. Also notice the use of left and right commands around the parentheses, which makes them enlarge to the correct size to match their content:
\begin{equation}\label{eqn:important}
\sum_{i=1}^n \cos\left(x + \frac{1}{x^2+1}\right) > \prod_{i}^{i\leq 5} a_i b_i
\end{equation}
We also created a "label". What that does is store the number that the equation has. We can then automatically insert it in the text by saying something like: equation~\eqref{eqn:important} is useful or just~\ref{eqn:important}. if you don't want the parentheses. You can do the same thing on theorems, for example we can refer to theorem~\ref{thm:coolTheorem} below:
\begin{theorem}\label{thm:coolTheorem}
A cool theorem whose number we can reference!
\end{theorem}
There is a special environment for aligned equations. The ampersand indicates the place where things should align vertically (often the equals sign), while the double backslash at the end of a line indicates that a new line should start:
\begin{align*}
y &= x + 3\\
  &= 5 + 4 = 2
\end{align*}
```

There are lots of other possibilities. Just ask if you want to do something and you're not quite sure how to do it!

### Some standard mathematical symbols

Paste them in and see how they look:
```
$\mathbb{C}$
$\mathbb{N}$
$\exists x \in A$
$\forall x\, x > 3 \implies x > 2$
$x \mapsto f(x)$
$\alpha \beta \gamma \Gamma$
```

### FAQs

- How do I do lines over characters (conjugates)?

    For a single character, do `\bar z`. For a longer line, do `\overline{...}`

- How do I include graphics I have made in some other application?

    See this link: [https://www.overleaf.com/help/111-how-do-i-insert-an-image-into-my-document#.VrOBGWQrJcw](https://www.overleaf.com/help/111-how-do-i-insert-an-image-into-my-document#.VrOBGWQrJcw). The important parts are:
    1. upload your file in the project
    2. add the line `\usepackage{graphicx}` in the preamble if it's not already there
    3. Use something like `\includegraphics[width=\textwidth]{YOUR-FILE-NAME-HERE}` where you want the file to be inserted. You can also use `0.8\textwidth` if you want it to take up 80% of the text's width, or you can insert a precise measure like `2.4in`.
