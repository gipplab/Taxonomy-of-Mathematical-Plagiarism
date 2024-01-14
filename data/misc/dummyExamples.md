## Differrent Presentation

\subsubsection{Case:}

We present several examples to illustrate the cases for this obfuscation as the conditions are borderline. 

\textbf{First}, the canonical example of a Different Presentation is a simple change of variable names 
\begin{lquote}{pres1_src}
$f(x)$    
\end{lquote}
versus \begin{rquote}{pres1_sim}
    $g(x)$.
\end{rquote} 
Here, we assume that the two expressions have the same meaning. 
However, in real cases, it might have to be determined from the surrounding context.

\textbf{Second}, an example allowing different placement of subexpressions and even adding symbols, as in the pair with source 
\begin{lquote}{pres2_src}
$M(i,j)$    
\end{lquote}
and similar expression 
\begin{rquote}{pres2_sim}
$M_{i,j}$    
\end{rquote} describing the entries of a matrix $M$ in two different ways. 

\textbf{Third}, an example through shorthand writing notation for a list of objects 
\begin{lquote}{pres2_src}
$ \begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22} 
\end{bmatrix}  $    
\end{lquote}
and a similar expression 
\begin{rquote}{pres2_sim}
$A$.  
\end{rquote}
Both represent the same matrix.

\textbf{Fourth}, 
\begin{lquote}{pres3_src}
$a_1+\dots+a_n$
\end{lquote}
is derived through a different presentation from 
\begin{rquote}{pres3_sus}
$\sum_{i=1}^n a_i$.
\end{rquote}
Namely, Similar Passage \rquoteref{pres3_sus} is formed through the application of the summation operator $\sum_{i=.}^.a_i$ to the integers $1$ and $n$. 
With this, we can match $1$ to $1$, $n$ to $n $, and $a_*+\dots+a_*$ to $\sum_{i=*}^{*} a_i$ without loss in semantics. 

## Formula Manipulation

\subsubsection{Case}
The following example
\begin{lquote}{type1_src}
$v^T=q^T$
\end{lquote}
and
\begin{rquote}{type1_sim}
    $v=q$,
\end{rquote}
which can be regarded as an application of a bijective operation to both sides of an equation, might help to delineate formula manipulation from the \textbf{variation of subject} obfuscation operator to be introduced below.

A more complex example might consist of the application of coordinate changes, e.g. expressing a complex number
\begin{lquote}{type1_src}
$z = a+bi$
\end{lquote}
in polar coordinates as 
\begin{rquote}{type1_sim}
    $z=re^{i\phi}$.
\end{rquote}

An example of formula manipulation in a text might be given through De Morgan's laws:
\begin{lquote}{type1_src}
$a$ lies outside both $A$ and $B$.
\end{lquote}
vs. 
\begin{rquote}{type1_sim}
$a$ lies in the intersection of the respective complements of $A$ and $B$.
\end{rquote}
