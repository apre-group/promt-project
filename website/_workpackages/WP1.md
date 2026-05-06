---
number: 1
title: Controlling Termination
leader: Ezio Bartocci
---

Controlling termination of probabilistic loops can be achieved through proof
rules based on term rewriting, sized types, Büchi automata, or weakest precondition calculi.
Most of these approaches provide sufficient conditions for (dis)proving termination, with recent
work also ensuring completeness. These proof rules require auxiliary expressions over program variables,
such as invariants and supermartingales. 

Supermartingale synthesis is undecidable in general and
current approaches fail for simple programs. We will develop "relaxed" proof rules for termination for certain classes
of programs, and develop new synthesis techniques.

