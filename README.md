# Greek_LaTeX
How set up LaTeX Editor for Greeks in Slackware current.
---

1. Assume you use slpkg and ponce repo:
```
slpkg -i texmaker hunspell-gr
```
2. Start texmaker and setup like this:
  ```
 - Options-|
           |-Configure texmaker-|
                                |-Quick Build -> Seletect: XeLaTex + View PDF
                                |- EDITOR --> Select: Font DejaVu Sans Mono
                                         |--> Select: Enconding UTF 8
                                         |--> Select: dictionaries /usr/share/myspell/dicts/el_GR.dic
```

3. Restart textmaker
4. Setup like this your *.tex files:
```
\documentclass[a4paper,11pt]{article}
\usepackage{fontspec}
\usepackage{xltxtra}
\usepackage{xgreek}
\usepackage{xunicode}
\usepackage{amsmath}
\usepackage{listings}
\usepackage{xcolor}
\usepackage{graphicx}
\title{Some Title}
\author{Your Name \\
email@gmail.com}
\date{/today} 
\setmainfont{DejaVu Sans}

\begin{document}
\maketitle

\section{Introduction (Εισαγωγή)}
Ο Γιώργος είναι πονηρός και αυτά που λέει μην τα τρως!
\section{Processing Steps (Αρχή Κυρίως Κειμένου)}
Είχαμε και λέγαμε και για να λέμε έχουμε... \\
μπλα μπλα μπλα
{}
\section{Summary - Final Stage (Σύνοψη - Τελικό Στάδιο)}
Τελικά ο Γιώργος είναι πονηρός αλλά η Γιωργία πονηρότερη!
\end{document}
```
Αν χρειάζεσαι κάτι παραπάνω που δεν είναι προεγκατεστημένο `slpkg -s tex`
