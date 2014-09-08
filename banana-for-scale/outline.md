Outline for the talk
====================

Late night ramblings...  Feel free to tear apart

Know your metrics
-----------------
Dive a bit into the metrics that people like to use - and then show why they do not work well (e.g. average)
Look at the different kinds of metrics given by codahale
Explain why 95th is good
TPS - what is it exactly


Know your system
----------------
Understand symptoms and what they point to - is it an app problem, or a resource issue (does it even differ?)
How often is it really the hardware that is not "big" enough

Cause and effect
----------------
(Just a thought for a third point...)
When something is different the next day, you want to be damn sure what the
reason (cause) of that was. Corollary: Make one change, then observe... if the
behaviour (performance) of your system is better, it was due to *this* change.
If you make 3 changes, and performance is better, you won't know which change
caused it.
Favorite quote: Assumptions is the mother of all ****-ups.
