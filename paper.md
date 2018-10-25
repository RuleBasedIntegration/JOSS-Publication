---
title: 'Rule-based integration: An extensive system of symbolic integration rules'
tags:
  - Mathematics
  - Integration
  - dynamics
  - galactic dynamics
  - milky way
authors:
  - name: Albert Rich
    orcid: ?????????
    affiliation: 1
  - name: Patrick Scheibe
    orcid: 0000-0003-0361-9063
    affiliation: 2
affiliations:
 - name: Unaffiliated, co-author of the Derive computer algebra system
   index: 1
 - name: Leipzig University, Saxonian Incubator for Clinical Translation, Philipp-Rosenthal-Straße 55, 04103 Leipzig
   index: 2
date: 30 October 2018
bibliography: paper.bib
---

# Summary

Finding the antiderivative of expressions is challenging and requires advanced mathematical skills
and knowledge even for unsuspicious looking problems. Nowadays, computer algebra systems (CAS)
like Mathematica [XXX], Maple [XXX], Maxima [XXX], and others [XXX], provide algorithms
to compute antiderivatives symbolically, but it often is impossible to gain insight into how a
solution was found or why an antiderivative could not be computed.

In this work, we present Rubi, an extensive system of symbolic integration rules that can be
systematically applied to determine the antiderivative of a wide variety of mathematical expressions.
Rubi contains currently over 6600 integration rules derived from known integration tables [XXX]
and incorporated into Mathematica's powerful pattern-matching language. The key to the success of Rubi
is the rigorous definition of conditions for the integration steps that determine under which circumstances
the application of a specific rule is correct and meaningful.
Therefore, Rubi produces optimal antiderivatives often dramatically simpler than provided by the commercial CAS integrators.

Rubi is implemented as a Mathematica package that gives the user the possibility to inspect integration
steps and conditions in detail. 
An extensive test suite of over 70.000 integrals with known, optimal antiderivatives is employed to
verify its correctness. To compare the results of Rubi with other integrators, the test suite is
available for Axiom, Maple, Mathematica, and Maxima.

However, the value of Rubi goes far beyond its Mathematica implementation. All integration rules are
available in human readable form as PDF file or Mathematica notebook which contain additional details
and references to the relevant literature. Since Rubi's rules in general only require a system for
manipulating symbolic expressions by applying pattern-based rules, it is feasible to implement the
integration rules in other systems. Therefore, Rubi is the integration engine behind Symja,
an open-source Java system for symbolic math. Furthermore, there are efforts to include Rubi into SymPy,
a Python library for symbolic mathematics, which would directly open the way to use it in Sage,
a free and open-source CAS.


# Short Example


# Mathematics

Single dollars ($) are required for inline mathematics e.g. $f(x) = e^{\pi/x}$

Double dollars make self-standing equations:

$$\Theta(x) = \left\{\begin{array}{l}
0\textrm{ if } x < 0\cr
1\textrm{ else}
\end{array}\right.$$


# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

# Figures

Figures can be included like this: ![Example figure.](figure.png)

# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References
