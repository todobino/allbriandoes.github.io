---
title:       "Non-Linearity & The Thinking Knee: More On Fundamentals Of Agility"
date:        2017-12-30
tags:
  - muse
categories:
  - geekery
  - tdd
  - modern-synthesis
---
so we talked about non-linearity <a href="http://geepawhill.org/linearity-non-linearity-ci/">here</a>, wrapping it into the context of explaining why we prefer continuous integration (CI). but non-linearity isn't just a good rationale for CI, it's actually a driving factor for several of the practices of agility. it's worth it to take a little more time to look hard.

we've said that some problems are linear and some non-linear. non-linear problems don't just get bigger when you add more pieces, they get "bigger-er". why?

one thing that causes non-linearity we've already touched on: if you have to relate the newest piece to all of the older pieces to solve the problem, *whoosh*, we're in non-linear land for sure.

in the first example, a new card had to be compared to each old card to answer the question "is this one greater than all the others?" but, as my more astute -- not to say less attractive in any way -- readers pointed out, you might solve that particular problem in another way. what if you just always remember the biggest card you've seen so far? then compare the new card to that, and you'll know the answer.

that move, of tweaking the algorithm, the formal recipe we use for solving the problem, is one we use every day. in this case, the problem goes from being non-linear to perfectly linear with just that one trick.the non-linearity there was all embedded in the algorithm, and a clever person could eliminate all of it just by changing that algorithm.

(if you think that's just the bee's knees, you should prolly a) learn to geek for a living and b) stop using expressions from America's 30's and 40's, you hep-cat.)

in that case we beat non-linearity by changing the process. can we always do that? 

wellllllllllll. that's a very tricky question. the official current formal answer ranges from "no" to "not yet". people invent new algorithms every day for doing this outwitting of non-linearity. some problems, tho, have had generations of fine minds looking for alternatives, and the consensus on them is "there's no faster way".

sometimes, the fix isn't in the algorithm per se, the process we use to solve the problem, it's in the performance of the processor. if it's a computer solving the problem, well, computers have gotten twice as fast about every 18 months for, what, 3 decades, 4? look up moore's law. there, the non-linearity doesn't go away, it's just that the cost-per-action goes down. the *number* of actions stills goes up "bigger-er" than the number of pieces, but because actions go faster, it feels like we've mitigated our problem.

sometimes, non-linearity isn't very smooth. that is, the problem is linear up to a certain number of pieces, then it goes violently non-linear after that. imagine a problem that costs 1 action for 1 piece, 10 actions for 7 pieces, and a 1000 actions for 11 pieces. (do such problems exist? oh, hell yeah.) these problems are linear or mildly non-linear for a while, then they take a sharp turn. they have a "knee" or an "elbow" at some point.

sometimes, that knee is so sharp that, for all practical purposes, when we push the problem beyond a certain number of pieces, it becomes NOT SOLVABLE.

and now, finally, we march out of the abstract math land into direct human territory. because problems whose solution depends on the performance of human bodies nearly *always* have this property.

there are limits to nearly anything you can see a body do, but in this case, i want to hone in on one particular limit, and that is the limit of how many pieces a human can think about at one time.

the metaphor i go for here is the juggling metaphor: how many independent pieces can a human juggle at one time? the answer is fuzzy. if the pieces are truly unrelated, that number is under 10, well under 10. (if the human finds it easy to relate the pieces in question, it can go up a little. if the human finds it harder to relate the pieces in question, it can go way down.)

when we talked about CI, we said that merging say 100 pieces of code into a codebase is way more than a 100 times harder than merging 1 piece. why? it's the human.

think about it. the *computer* can actually do those merges in nearly linear time. but the computer doesn't have to understand those changes. it just has to make them. the human has to grasp them. the computer doesn't know or care if the new build breaks the north american power grid, or drops planes out of the sky, or prevents us from tweeting long muses, or hard-formats the drive of everyone who runs it. the human cares very much, and *has* to know.

human thinking is non-linear AND it has a very sharp knee at a very low number of pieces. and that insight lies at the heart of a great many of the techniques agilists advocate.

when we push for CI, we are trying to keep piece-counts small to reduce the non-linear effects, and so small that we are "inside" the thinking knee. and it's not just CI. there are several other practices that adhere to this pattern. let's name three of them at random.

TDD writes small tests interactively as we write the code. we are keeping piece counts small.

story-shaped development -- iterative and incremental -- wants stories we expect to take less than a day or two to implement. stories that small help us keep the piece counts low.

the emphasis in merciless refactoring on killing off duplication? hmmmm. makes fewer pieces, doesn't it?

and our reaction to the thinking-knee isn't just limited to reducing piece count in gross obvious ways. there are other practices that attack the knee by introducing a variety of other techniques. (i'll take a look at a couple of these in a muse coming soon to a twitter near you.)

for now, it's enough that you grasp the significance of both non-linearity and the idea of knees in the non-linear curve.

with the thinking-knee under your belt, you'll see piece-counts all around you, and you'll be sensitized to the variety of ways we seek to reduce them. you'll be, in short, ready for the crazy non-intuitive practices agilists have been struggling towards for the last 20 years.
