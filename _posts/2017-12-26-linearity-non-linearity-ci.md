---
layout: post
title:       "Linearity & Non-Linearity & CI"
date:        2017-12-26
tags:
  - muse
categories:
  - geekery
  - tdd
  - modern-synthesis
---
when we talk about software methods, very early on we come to a place where we simply have to develop a comfortable grasp of non-linear effects.

so many conversations founder here, where the relationship between two values becomes something other than a more or less straight line on a piece of graph paper. we spend a lot of time talking about the cluster of concepts we normally shorthand as "complexity". that's a good enterprise, i think, but i also think it's a few chapters ahead of where our decision-makers are. it doesn't take chaotic dynamics to understand why continuous integration (CI) is so important, for instance.

we all come very early on to understand that more pieces means more work. that concept needs no introduction. for the overwhelming majority of problems, "more pieces" = "more actions", trivial knowledge every infant knows.

the interesting point isn't really that pieces and actions are related. they are nearly always correlated: when the pieces go up, the actions go up. the interest comes when we ask, "how *much* does the count of actions go up when the count of pieces goes up?"

and here we meet a whole bunch of mathy words: "linear" vs "non-linear". "arithmetic" v. "geometric" v. "exponential" progression. "asymptotic", and so on. these are all words that sketch different answers to that question for different problems.

(aside: obviously, i'm comfy with math, and so is much of my downstream, and we all know this shit. i'm reviewing at such a starter level cuz many of the people we work with *aren't* comfy there, and i am seeking easy ways in to it.)

some problems look like this: "no matter how many pieces you have, if you add one more piece, it will cost you one more action to finish the larger problem." if you start with 1 piece, it takes 1 action. 10 pieces, 10 actions. 100 pieces, 100 actions. the usual example is moving bricks. it takes 1 action to move 1 brick, so it takes 10 actions to move 10 bricks, and so on. this is called "linear" btw, because the simplest abstract picture of it, a graph where pieces are on the vertical and actions are on the horizontal, makes a straight line.

there are lots and lots of problems that are like this, so it's perfectly natural to wonder if all problems are. the answer is no.

in linear problems, one extra piece means one extra action, regardless of the total number of pieces. but there are a lot of problems where the action-cost of adding a piece is *different* depending on how many pieces are already in the problem. what kind of problems are these "non-linear" ones? well, any problem where adding one more piece means relating it somehow to some or all of the other pieces.

here's a problem: i will give you some playing cards. each card i give you, tell me if it's bigger or smaller than all the others you have. if you have a 3 and i give you an 8, say "yes". if i give you a 2 say "no".

how hard is this, how many actions does it take? ahhhhhh, well. that depends on how many cards you start with. you have to compare the new card with every card you already have before you can answer. the more cards you already have, the more comparisons you'll have to make, the more actions it costs. so the cost for adding a card doesn't go up a fixed amount every time. (if you draw this one, you get a curve instead of a straight line.)

it's no coincidence that this problem involves comparison. one of the earliest lesson-sets young geeks have to master is exactly this kind of sorting task. we have to learn a bunch of clever ways to arrange and compare the cards as they get given to us, to reduce the actions.

in a linear problem, add one piece and the problem gets "bigger". in a non-linear problem, add one piece and the problem gets, well, "bigger-er". the more pieces there are, the higher the number of actions required to add just one more piece.

(geek-grin: there are even problems where the action-cost goes up so fast per additional piece that for even relatively small numbers of pieces they become NOT DOABLE IN THE TIME REMAINING BEFORE THE SUN BURNS OUT. how cool is *that*?)

alright let's bring this vague crap back to continuous integration (CI).

integrating code, merging two versions of a codebase, can be done once a month, a week, a day, or an hour. generally, in CI we push to make the elapsed time between merges as small as possible, in some shops we're talking tens of minutes. why?

the longer the elapsed time, the more differences there are between the two codebases. differences are the pieces here.

naturally, the more pieces the bigger the cost of merging them. BUT, it's worse than that. it turns out that merging pieces is a non-linear problem.  with each additional piece, the cost doesn't just get bigger, it actually gets bigger-er. i don't have a formula, but we have ample evidence that 100 pieces is much harder than just 100 times 1 piece.

we practice CI because of this non-linearity. 8 merges, each of one hour's worth of changes, takes less action than 1 merge of eight hour's worth of changes. now that's some cool-assed theory, yeah? if you hung in this far, you now have a grasp of *why* CI is a cornerstone of the modern synthesis. but that's not why i started this monstrous thread.

do you know who totally got why CI would work before they actually tried it? just about no one. oh, a few did, a few do, don't get me wrong. but the great unwashed mass of geeks, including me, never got it until we did it. this is especially remarkable given that the sonnet turns at non-linear effects, a subject nearly all geeks have spent substantial time studying and experimenting around.

there might be a lot of morals to this story. normally, i enumerate several of them myself. but ya know what? it's the day after christmas, i'm out of smokes, and it was a long rambling muse, so i'll leave it to u. pick from it any lurking lessons there. if u feel so moved, tweet them to the thread so we can all savor them. thanks for following along!