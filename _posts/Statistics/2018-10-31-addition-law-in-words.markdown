---
layout: post
title:  "The Addition Law of Probability, in words"
date:   2018-10-31 15:51:30
categories: Statistics
---

When I was learning the basics of probability for the first time, I found that I needed to justify the Addition Law of Probability for myself beyond the standard Venn diagram illustration of overlapping sets. This felt unusual, because I’m normally a highly visual learner, but for whatever reason I felt that I needed a more explicit demonstration that the law <i>had</i> to be formulated as it was, rather than fitting the illustration simply by happenstance.
<br><br>
The Addition Law concerns the probabilities of outcomes which fall within certain sets of interest. These sets can be thought of as conditions which are met (or not) by elements of the sample space (i.e. potential outcomes). We can think of “event” <i>A</i> as identifying the case that an outcome <i>x</i> satisfies condition <i>A</i>. The Law states that the probability of the union of two events (<i>A</i> &cup; <i>B</i>) is equal to the sum of the individual probabilities of the events minus the probability of the intersection of the events (<i>A</i> &cap; <i>B</i>):
<br><br><center>
Pr(<i>A</i> &cup; <i>B</i>) = Pr(<i>A</i>) + Pr(<i>B</i>) - Pr(<i>A</i> &cap; <i>B</i>)
</center><br>
In words, this means that the probability of an outcome satisfying <i>at least one of</i> (i.e., either or both of) conditions <i>A</i> and <i>B</i> is equal to the probability that the outcome will satisfy condition <i>A</i>, plus the probability that the outcome will satisfy condition <i>B</i>, minus the probability that the outcome will satisfy <i>both</i> conditions <i>A</i> and <i>B</i>.
<br><br>
Something about this never struck me as intuitive, at least not as presented above. Of course, if the two conditions are mutually exclusive (i.e. the sets do not overlap), Pr(<i>A</i> &cap; <i>B</i>) = 0, so the union probability is simply the sum of the individual condition probabilities—that’s all easy to see.
<br><br>
The explanation for the subtracted term in the general equation states that the individual condition probabilities end up double-counting outcomes which satisfy both, so the intersection probability must be subtracted from the total to correct. But this felt (to me, at least) unnatural—I couldn’t “see” this from the equation. To prove this to myself, I was able to derive the Law while expressing it using words, and make clear why the correction is both necessary and successful.
<br><br>
Beginning with the (much more intuitive) equation for the case of mutually exclusive condition sets, we have:
<br><br><center>
Pr(<i>A</i> &cup; <i>B</i>) = Pr(<i>A</i>) + Pr(<i>B</i>)
</center><br>
As noted above, this is valid because there are no outcomes satisfying both conditions (the sets do not overlap). If we wish to extend a formal definition of the union probability to a case of non-mutually exclusive conditions, we must modify this equation somehow. We can find the way forward by parsing the condition probabilities.
<br><br>
If some elements of the sample space will satisfy both conditions, then each of the condition probabilities in the equation can be parsed to probabilities of outcomes satisfying <i>only</i> the given condition and those satisfying <i>both</i> the given condition <i>and</i> the second condition. In words, the parsed equation is:
<br><br><center>
Pr(<i>A</i> &cup; <i>B</i>) ≠ Pr(<i>A</i> <b>only</b>) + Pr(<i>A</i> <b>and</b> <i>B</i>) + Pr(<i>B</i> <b>only</b>) + Pr(<i>B</i> <b>and</b> <i>A</i>)
</center><br>
The doubly satisfied conditions are ordered above to show that they correspond to the first and second terms in the original equation that have been parsed, but there is of course no difference between first stating one met condition or the other. Explicitly:
<br><br><center>
Pr(<i>A</i> <b>and</b> <i>B</i>) = Pr(<i>B</i> <b>and</b> <i>A</i>)
</center><br>
Thus, we can simplify the parsed equation to:
<br><br><center>
Pr(<i>A</i> &cup; <i>B</i>) ≠ Pr(<i>A</i> <b>only</b>) + Pr(<i>B</i> <b>only</b>) + 2 Pr(<i>A</i> <b>and</b> <i>B</i>)
</center><br>
As this effectively represents the outcomes as complementary portions of the sample space, grouped by the conditions met, we can see that there are only three types of outcomes: <i>x</i> meets <i>A</i> only, <i>B</i> only, or both. Yet, as written above, the original equation is counting the last group <i>precisely</i> twice, and once too many. The correction to ensure validity in the non-mutually exclusive case is thus to subtract this term once (and note that the equality sign is then returned):
<br><br><center>
Pr(<i>A</i> &cup; <i>B</i>) = Pr(<i>A</i> <b>only</b>) + Pr(<i>B</i> <b>only</b>) + 2 Pr(<i>A</i> <b>and</b> <i>B</i>) - Pr(<i>A</i> <b>and</b> <i>B</i>)
</center><br>
We move from this equation to the standard statement of the Addition Law by recombining our parsed terms:
<br><br><center>
Pr(<i>A</i> &cup; <i>B</i>) = Pr(<i>A</i>) + Pr(<i>B</i>) - Pr(<i>A</i> <b>and</b> <i>B</i>)
</center><br>
The final term is defined as the intersection of <i>A</i> and <i>B</i>, so the final form notation of the equation above is:
<br><br><center>
Pr(<i>A</i> &cup; <i>B</i>) = Pr(<i>A</i>) + Pr(<i>B</i>) - Pr(<i>A</i> &cap; <i>B</i>)</center>
