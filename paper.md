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
  - name: Nasser M Abbasi
    orcid: ?????????????
    affiliation: 3
affiliations:
 - name: Unaffiliated, co-author of the Derive computer algebra system
   index: 1
 - name: Leipzig University, Saxonian Incubator for Clinical Translation, Philipp-Rosenthal-Straße 55, 04103 Leipzig
   index: 2
 - name: ????????????????
   index: 3
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

![Figure 1](figure1.png)

Figure 1 shows the computation of

$$\int \frac{\sec(x)^2+\sec(x)^2\cdot\tan(x)}{(2-\tan(x))\cdot\sqrt{1+\tan(x)^3}} \; dx$$

using Rubi when all integration steps are displayed.
The specific rules that are applied are shown in red and it is possible to open the rule display to inspect the exact conditions that need to hold to make the transformation valid.
In blue, the intermediate expressions are visible and at the end the final antiderivative is returned.
It should be noted that the size of the found antiderivative is 25, counting the leafs of the expression tree.
In comparison, Mathematica 11.3 returns an antiderivative that has a leaf count of 290 and contains complex terms.

# Acknowledgements

We to thank David Jeffrey, Daniel Lichtblau, David Stoutemyer, Martin Welz for contributions and fruitful discussion

# References
