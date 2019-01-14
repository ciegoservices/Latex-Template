# Latex-Template
A Latex Template for MA701 at ESU

# How does this work?
This is both a paper-style template, with a bibliography example to help introduce you to LaTex.  Frankly, I love LaTex, but I hate how verbose LaTex can get.  To that end, I've created a ton of new commands to make things faster to type up.

## Theorem Styling
First, here are some tools that my old professor gave me to track references for theorems more conveniently.

```latex
\newtheorem{theorem}{Theorem}[section]
\newtheorem{lemma}[theorem]{Lemma}
\newtheorem{proposition}[theorem]{Proposition}
\newtheorem{corollary}[theorem]{Corollary}
\newtheorem{definition}[theorem]{Definition}
\newtheorem{example}[theorem]{Example}
\newtheorem{note}[theorem]{Note}
```
So, for instance, if we want to make a new example, we write:
```latex
\begin{example}
Example text goes in here.
\end{example}
```

## Second, I made a ton of simple commands that make typing LaTex faster:
```latex
%numbers convenience
\newcommand{\R}{\mathbb{R}} %real numbers 
\newcommand{\Q}{\mathbb{Q}} %rational numbers
\newcommand{\N}{\mathbb{N}} %naturally the naturals
\newcommand{\goesto}{\rightarrow} %x\rightarrow a is really annoying to type x \goesto a is nicer and reads more like what I'm thinking.

%partial derivative stuff
\newcommand{\pd}[2][ ]{\frac{\partial #1}{\partial #2}} %builder for PDEs
\newcommand{\pdx}{\pd{x}}
\newcommand{\pdy}{\pd{y}}w
\newcommand{\pdfdx}{\pd[f]{x}}
\newcommand{\pdfdy}{\pd[f]{y}}
\newcommand{\pdfdz}{\pd[f]{z}}
\newcommand{\pdzds}{\pd[z]{s}}
\newcommand{\pdzdx}{\pd[z]{x}}
\newcommand{\pdzdy}{\pd[z]{y}}
\newcommand{\pdxds}{\pd[x]{s}}
\newcommand{\pdxdt}{\pd[x]{t}}
\newcommand{\pdyds}{\pd[y]{s}}
\newcommand{\pdydt}{\pd[y]{t}}

\newcommand{\grad}{\nabla} %typing \nabla is super unintuitive
\newcommand{\evaluatedat}[2]{\bigg\vert_{#1}^{#2}}

%basic derivative notation stuff
\newcommand{\dee}{\text{ d}}
\newcommand{\dx}{\text{ d}x}
\newcommand{\dy}{\text{ d}y}
\newcommand{\dz}{\text{ d}z}
\newcommand{\dr}{\text{ d}r}
\newcommand{\dt}{\text{ d}t}
\newcommand{\du}{\text{ d}u}
\newcommand{\dv}{\text{ d}v}
\newcommand{\dtheta}{\text{ d}\theta}
\newcommand{\ddx}{\frac{\dee}{\dx}}
\newcommand{\dd}[2][]{\frac{\dee #1}{\dee #2}}
\newcommand{\dzdt}{\dd[z]{t}}
\newcommand{\dxdt}{\dd[x]{t}}
\newcommand{\dydt}{\dd[x]{t}}
\newcommand{\dydx}{\dd[y]{x}}

%more convenience because typing \frac{a}{b} is super time consuming and unintuitive
\newcommand{\oneover}[1]{\frac{1}{#1}}
\newcommand{\onehalf}{\frac{1}{2}}
\newcommand{\onethird}{\frac{1}{3}}
\newcommand{\onefourth}{\frac{1}{4}}
\newcommand{\onefifth}{\frac{1}{5}}
\newcommand{\onesixth}{\frac{1}{6}}
\newcommand{\oneseventh}{\frac{1}{7}}
\newcommand{\oneeighth}{\frac{1}{8}}
\newcommand{\oneninth}{\frac{1}{9}}

%other common fractions
\newcommand{\twothirds}{\frac{2}{3}}

%this is for typing pi/n a bunch of times
\newcommand{\piover}[1]{\frac{\pi}{#1}}

%the syntax for square roots sucks in LaTex
\newcommand{\rt}[1]{\sqrt{#1}}
\newcommand{\roottwo}{\rt{2}}
\newcommand{\rootthree}{\rt{3}}
\newcommand{\rootfour}{\rt{4}}
\newcommand{\rootfive}{\rt{5}}
\newcommand{\rootsix}{\rt{6}}

%this is something humorous that also makes life easier
\newcommand{\bigma}[2]{\sum_{#1}^{#2}}

%vector notation stuff
\newcommand{\vecr}{\mathbf{r}}
\newcommand{\vecu}{\mathbf{u}}
\newcommand{\vecv}{\mathbf{v}}
\newcommand{\vecw}{\mathbf{w}}
\newcommand{\vecx}{\mathbf{x}}
\newcommand{\vecy}{\mathbf{y}}
\newcommand{\vecz}{\mathbf{z}}
\newcommand{\yhat}{\hat{\vecy}}


%linear algebra stuff 
\newcommand{\transpose}[1]{#1^T}
\newcommand{\norm}[1]{\lVert#1\rVert}
\newcommand{\dist}[2]{\text{dist($\mathbf{#1}$,$\mathbf{#2}$)}}
```
These are all prety self explanatory, please let me know if you have any questions.

For those of you who are new to LaTex, personally, I use [Visual Studio Code](https://code.visualstudio.com/) to type my LaTex files, it's free, just like overleaf, and this semester I plan on pushing them to GitHub for convenience and cloud storage.

For a WYSIWYG editor, I use [LaTex Preview](https://marketplace.visualstudio.com/items?itemName=ajshort.latex-preview), and for code highlighting, and debugging tools I use [LaTex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop).  It's pretty good.  This semester I plan on skipping the use of Overleaf (even though I really do like it) and using github and my local repository for all my LaTex work.  As I add stuff to my set of commands in the header, I'll try to remember to update them here.  I'm thinking of trying to make a tool that you can use to simplify the process of generating papers with LaTex.  We'll see what I can come up with.

Pat Pragman
ppragman@g.emporia.edu
