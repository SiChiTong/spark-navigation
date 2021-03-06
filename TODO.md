All algorithms
==============

- external properties, e.g. reaching goal or reporting error

ND
--

- giant loop (in)variant

VFH
---

- use Arctan instead of Init::Cell_Direction

- gnatd.V flag makes proof _much_ longer because of extensive
  flow-analysis

SND
---

- enabling assertions results in internal compiler error; the
  workaround is to comment the assertion that causes the problem

Formal.Numerics
---------------

- runtime assertions for exclusive ranges, e.g. positive

- build scenarios with Ada and libc floating-point elementary functions

GNATProve
---------

- 'Loop_Entry in Loop_(In)Variants create constant values even if no assertions
  are checked (-gnata option is missing); reported to AdaCore as N213-026 GAP

- 'Remainder attribute: full formalization

- loop invariants in nested loops require non-obvious framing contexts

- loop variables, such as I in "for I in ..", cannot be used with Global aspect
  of subprograms nested in a loop

GNATcheck (style)
-----------------

- binary operators should be surrounded by spaces with '-gnatyt
  option', but 'a := Sqrt (c * c - b*b)' expression is accepted;
  reported to GCC as http://gcc.gnu.org/bugzilla/show_bug.cgi?id=60163
