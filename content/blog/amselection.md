+++
title = "Keeping the Blog Updated and Proportional UK Elections"
date = "2019-04-19T17:32:54+01:00"
draft = true
+++
Having it been just over eight months since I have penned a blog post to this area of my website, I figured it was about time that something new was added. After all, a lot has changed since [my last blog post.](./smallpeice-2018/) Time has become a commodity in my second year of university; being over-encumbered with pieces of coursework, lecture notes and revision for exams, as well as other extra-curricular activites leaves little time for other items.

Anyways, with the consequence of facing revision, I did the best thing I could - do something completely different. Somewhere in this mix was a splash of politics (never a good idea), leading me down to the road to creating a small Python program. The program in question takes general election results and converts the result into that of an election run under the additional member system (AMS). In this blog post, I will attempt to maintain a non-partisan view of the electoral systems in the UK and reason the benefits and downsides of each mentioned for the sake of balance.

As of writing, general elections in the UK use FPTP to elect Members of Parliament to constituencies. In practice, there are 650 mini-elections that take place, all deciding the fate of political parties on a national scale. FPTP takes the candidate with the most votes and declares them the winner of the election. One obvious benefit is that the concepts of FPTP are extremely easy to understand; the candidate with the most votes wins. However, there are a host of downsides to FPTP. FPTP encourages the practice of tactical voting, where voters are discouraged from voting for candidates that they may actually want to vote for and are encouraged to vote for candidates that they feel will most likely defeat the candidate they do not like. Furthermore, if an ideologically similar candidate to the favourite stands in the constituency, it can have the side-effect of diluting the amount of votes that each candidate would get - this in turn leads to an opposing candidate, with no rival, to claim victory; this is known as the spoiler effect.

## Proportionality and the Gallagher Index
One major gripe with FPTP is that it is not a proportional system; that is, the amount of votes cast for a political party indicates the percentage of the seats that the party wins. As there is no mechanism for this to occur in FPTP, it becomes apparent that it can lead to disproportionate results.

Take for example the 2015 UK General Election; under the leadership of David Cameron, the Conservative Party won 36.8% of the votes cast across the UK. However, they won 330 of the 650 seats available (50.8%), leading to an outright majority.

Furthermore, the UK Independence Party, under the leadership of Nigel Farage, managed to achieve 12.6% of the nationwide vote. They gained a single seat (0.2% of the available seats).

After this election, the disparity between votes cast and the number of seats attained lead to calls for electoral reform for general elections. Specifically, people referenced something known as the 'Gallagher index' to illustrate the disproportionality of the elections. 

![Image of the Gallagher index formula][gallagher]
Shown above is the formula for the Gallagher index. In plain English, the formulas sums together the square of the difference between the percentage of the votes cast for a party and the percentage of the seats that the party won. It then halves the sum and then square roots it, giving the Gallagher index. According to the Canadian Special Committee on Electoral Reform, a government should 'seek to design a system that achieves a Gallagher score of 5 or less.' The 2015 UK General Election achieved a Gallagher index of 15.04, illustrating a high disproportionality.

[gallagher]: /img/gallagher.png