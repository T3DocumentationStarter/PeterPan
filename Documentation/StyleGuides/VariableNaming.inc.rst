

Variable naming
===============

Ranges
------


martin.bless	[5:36 PM]  
Argh, I'm just doing some (Python) programming. If I only could find those non-ambiguous self-documenting variable names. I'm looking for a good naming scheme for ranges, limits, steps, points. And you don't want variable names be toooo long. 
*Example:* An integer variable v is allowed to have values from range 1 to 100. So 1 = minimum value = vmin = lower limit? And 100 = maximum value = vmax = upper limit? What would be the names for 0 and 101 then, the lower limit and upper limit OUTSIDE the legal range? border?

I would love to have a consistent naming scheme. What do you use?

ddbeck	[5:55 PM]  

With the caveat that self-documentation is a myth and there's no substitute for a good docstring, I think the convention is Python is to go for slightly wordier names. So, for instance, I'd expand this variable `v` to be whatever `v` actually represents and go from there. For example if `v` is `velocity` I'd probably go with `max_velocity` and `min_velocity`

As for the question of inclusive or non-inclusive ranges, I don't think naming is going to help you there. That's exactly the sort of thing I'd check the docs for

- range(start, stop, step)
- min\_something, max\_something
- from, to, upto
- first_day, last_day
- border? wall?

