# MATH4710J
Numerical Methods 
## Homework 
LaTeX template for homework assignments $\Rightarrow$ [here](./MATH4710JFA2025(2025-2026%20Fall%20Manuel%20CHARLEMAGNE)/homework/homework1/homework1.tex) or copy from below.  
### ✅ Features
- [x] Homework template in LaTeX
- [x] Pseudocode environment using `algorithm2e`
- [x] Code environment using `listings`

```latex
% MATH471 Homework LaTeX Template
% Compile with: pdflatex MATH471_homework_template.tex (or xelatex/lualatex)
\documentclass[11pt,a4paper]{article}

% Packages
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{geometry}
\geometry{left=25mm,right=25mm,top=25mm,bottom=25mm}
\usepackage{amsmath,amssymb,amsthm}
\usepackage{mathtools}
\usepackage{enumitem}
\usepackage{graphicx}
\usepackage{float}
\usepackage{xcolor}
\usepackage{fancyhdr}
\usepackage{tikz}
\usepackage{caption}
\usepackage{booktabs}
\usepackage{listings}
\usepackage[linesnumbered,ruled,longend]{algorithm2e}
\usepackage[colorlinks=true,linkcolor=blue]{hyperref}
\SetKwInOut{Input}{Input}
\SetKwInOut{Output}{Output}
\SetKwProg{Fn}{Function}{\string:}{end}
\SetKwFunction{algohw}{AlgoHw}
% Theorem environments
\newtheorem{theorem}{Theorem}[section]
\newtheorem{lemma}[theorem]{Lemma}
\newtheorem{corollary}[theorem]{Corollary}
\theoremstyle{definition}
\newtheorem{definition}[theorem]{Definition}
\newtheorem{remark}[theorem]{Remark}

% Homework-specific environments
\newcounter{problem}
\newenvironment{problem}[1][]{\refstepcounter{problem}\par\medskip
\noindent{\bf Problem~\theproblem.}\ifx\relax#1\relax\else\ (#1)\fi\newline
}{\medskip}

\newenvironment{solution}{\par\noindent{\it Solution.} }{\hfill $\square$ \par}

% Header / Footer
\pagestyle{fancy}
\fancyhf{}
\lhead{MATH4710J --- Numerical Methods}
\chead{}
\rhead{Homework \#\hwnumber}
\lfoot{Student: \studentname}
\cfoot{\thepage}
\rfoot{October 1st, 2025}

% User commands (edit these in document body)
\newcommand{\coursenum}{MATH4710J}
\newcommand{\coursename}{Numerical Methods}
\newcommand{\instructor}{Manuel CHARLEMAGNE}
\newcommand{\studentname}{Turingw1}
\newcommand{\studentid}{000000}
\newcommand{\hwnumber}{1}

% Shortcuts
\newcommand{\R}{\mathbb{R}}
\newcommand{\N}{\mathbb{N}}
\newcommand{\abs}[1]{\left\lvert#1\right\rvert}
\newcommand{\norm}[1]{\left\lVert#1\right\rVert}

% Document
\begin{document}

% Title block (edit fields below)
\begin{center}
  {\Large \textbf{Homework \#\hwnumber}}\\[6pt]
  {\large \textbf{\coursenum\ --- \coursename}}\\[4pt]
  {Instructor: Manuel CHARLEMAGNE}\\[4pt]
  {Student: \studentname\ (ID:\@ \studentid)}\\[4pt]
  {Due date: October 1st, 2025}
\end{center}

\vspace{8pt}
\hrule
\vspace{12pt}

% Example problems
% If you have multiple parts
\begin{problem}
\begin{enumerate}
  \item  Subproblem 1
\end{enumerate}
\begin{solution}
\begin{enumerate}
  \item Solution to subproblem 1
\end{enumerate}
\end{solution}
\end{problem}


\begin{problem}[pseudocode and MATLAB code]
  1. Write the pseudocode for at least one the following strategy to approximate $\pi$.
  \begin{enumerate}[label = (\alph*)]
    \item The polygons method;
    \item Machin's formula $\frac{\pi}{4} = 4 \arctan \frac{1}{5} - \arctan \frac{1}{239}$
    and Taylor series;
  \end{enumerate}
2. Implement at least one of the previous algorithms in MATLAB.
\end{problem}\\

\begin{solution}\\

\begin{enumerate}
  \item 
  \begin{itemize}
  \item[a)] Using the polygons method to approximate $\pi$\\

\begin{algorithm}[H]
\Input{this file}
\Output{nice algorithms in the homework}
\BlankLine
\Fn{\algohw{this file}}{
download file\;
open file\;
compile file\;
\While{not at end of this document}{
read\;
\uIf{understand}{
go to next line\;
current line becomes this one\;
}
\uElseIf{want to know more on algorithms in \LaTeX} {refer to
\href{http://tug.ctan.org/tex-archive/macros/latex/contrib/algorithm2e/doc/algorithm2e.pdf}
{algorithm2e documentation}}
\Else {restart reading from the beginning\;}
}
\For{exercise $\leftarrow$ 1 \KwTo 7}{
\If{algorithm is requested} {
solve the problem\;
A[$exercise$] $\leftarrow $ write the algorithm in \LaTeX\;
}
}
\KwRet{A}
}
\caption{Algorithms in the homework}
\end{algorithm}
\end{itemize}
  \item Here is a MATLAB implementation of the polygon method to approximate $\pi$:
\begin{lstlisting}[language=Matlab, caption=Polygon Method to Approximate Pi]
function pi_approx = approximate_pi_polygon(n, k)
    % n: initial number of sides (e.g., 6)
    % k: number of iterations (doublings)
    c_n = 2 * sin(pi / n); % side length of inscribed polygon
    p_n = n * c_n;         % perimeter of inscribed polygon
    for i = 1:k
        c_n = sqrt(2 - 2 * sqrt(1 - c_n^2 / 4));
        p_n = 2 * n * c_n;
        n = 2 * n;
    end
    pi_approx = p_n;
end
\end{lstlisting}
\end{enumerate}
\end{solution}
\vfill
\noindent{\small Compiled with \LaTeX.}
\end{document}

```

- Homework 1: due October 1st, 2025


