# Pseudogens

All calculate_pseudogens_optimized() functions are solutions to optimization problems.
The doc strings clarify which is which:  one works more accurately but is prone to recursion
with networks that contain cycles (usually uncle-niece unions), whereas the second is robust
enough to handle all networks, but does not properly shift enough nodes 'up' from the bottom generation
(the algorithm relies on a bottom-up approach that labels all nodes at the bottom generation, Gen 0,
before shifting select nodes up based on our constraints, such as that the parents should be from a
'higher' generation than their child[ren], etc.).  Note that some heuristics already should probably change here.
For example, in the event a union resulted in a child (a so-called 'productive union'), then both nodes
in that union are forced to be in the same generation.  'Unproductive unions' -- or those without children --
are more relaxed, allowing for one generation of separation between partners.  I've since decided that
that wasn't the right way to enforce the constraints and that is related to the Discord message I sent on
Wednesday, 11 June 2025 asking what our priorities should be.  I have even thought of removing any constraints
related to the generation of the two union partners, so that the generation number is purely based on lineage
(like how FamilySearch considers generations solely based on how many forefathers are between person X and
person Y).

As always, please feel free to reach out to me with any questions, big or small.  Love y'all and thanks for
all your hard work!

~Japheth
