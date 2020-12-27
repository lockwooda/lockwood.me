---
title: "2019 UK General Election and PR"
date: 2019-12-18T12:04:31Z
draft: false
math: true
---

Well, that was an election and a half.
After a long campaign, the Conservatives have come out on top with 365 of the 650 seats in the House of Commons.

As to be expected, interest in proportional representation has increased due to the lack of proportionality of the results.
Although I will not be sharing my personal feelings on PR in this post, I will nonetheless look into what if the 2019 UK general election used a proportional system.

# Party Positions

In the most recent general election, the Liberal Democrats, Plaid Cymru and UKIP included commitments to a proportional voting system in their manifestos. It is worth noting that the Scottish National Paty and the Brexit Party have made prior commitments to proportional representation.
Labour made no commitment to voting systems in their manifestos, but did commit to a Constitutional Convention to look into the 'renewal of ... Parliament' through the use of citizens' assemblies.
On the contrary, the Conservatives made a direct commitment to uphold First Past the Post in their manifesto.

Of the parties that did make promises for proportional representation, they did not make them one of their big manifesto promises. I'm not even going to touch on why they didn't, because I imagine at this point it is pretty obvious why.

# Mixed-member Proportional

In one of my previous blog posts, I discussed about the Additional Member System (AMS), an electoral system used in Scottish parliamentary, Welsh and London assembly elections. 
It is a variant of an older system, mixed-member proportional representation, or MMP. It was in essence adopted by what was then West Germany in 1957 and is still used, albeit in a modified form, to this day. It is known for its complexity, with the need to balance proportional elections with local representation and representation of minorities at state level.

MMP requires voters to cast two votes; one vote is for their local representative, their 'first vote', and the other vote is for their favourite party, the 'second vote'. To the keen eyed, yes, this is also how voting in AMS works. However, the difference between the systems is in how the votes are handled once they are all counted.

AMS and MMP both use proportional representation to balance out the results of the constituencies (the first vote) to match the party vote (the second vote) as much as possible. As a result, members of Parliament can be elected in two ways; either as a local representative or as a 'list' member.

As a result of this, political parties are baked into the fabric of the electoral system; this is in contrast to FPTP, where parties could be deemed 'unnecessary' and the system would still function with independent candidates.

If you don't want the fancy details, here is how MMP roughly works:
- Elect MPs to constituencies based on plurality of the vote in a constituency
    - Essentially, this is First Past the Post
- Determine how many MPs a party should have at a regional level from second votes
    - If a party won less MPs than entitled under second vote, give list MPs
    - If a party won more MPs than entitled under second vote, increase the size of Parliament to accommodate extra winners 
- Combine regional MP totals to determine how many MPs a party should have at national level
- Balance out the number of MPs such that each party has roughly the same proportion of second votes per MP

## Details

As with FPTP, the candidate with the plurality of votes in a constituency (having the most votes of any candidate) will be designated the elected member for the constituency. These play an important role in the German MMP system.

The allocation of 'second vote' seats in Germany happens at a state level rather than at a federal level, although parties require 5% of the second votes nationally or three constituencies nationally to be allocated any of these seats. 
If a party that does not make the second vote threshold or an independent wins a seat, this seat is considered 'lost' and not counted in the number of seats in the state. Successful votes for a candidate that did not qualify for second vote will be discarded.

For the sake of converting FPTP to MMP, I will ignore the 5% of the federal second vote requirement. This is down to the complexities of British politics, having nationalist parties in Scotland and Wales and an essentially separate political system in Northern Ireland.

The seats are allocated using the second votes through the Sainte-Laguë system, which is essentially the D'Hondt system mention in the previous blog post but with a different formula:
$$ \text{quot} = \frac{V}{2s + 1} $$

All the seats in a state, that being the constituency seats and the list seats, are allocated to the parties based on the second votes in the state using the Sainte-Laguë system. This determines how many seats a party are entitled to a state level; unsurprisingly, this is known as the *entitlement*.

In Germany, there is the concept of '**Überhangmandate**', which translates to overhang seats. Overhang seats happen when a party wins more constituencies in a state
than seats that they have from their entitlement.

For example, a party may win 11 constituencies in a state but their second votes in the state only entitles them to 8. There are 3 overhang seats in this state for the party. If a person is elected from a constituency, they (obviously) must be given their seat. As a result, the party will get their state entitlement increased to 11 and the number of representatives in parliament is increased by 3.

All the seats that a party has won from all the states are summed together to calculate their *minimum entitlement* seats in the parliament.

There is still a few more steps to go to get the final number of MPs. Electoral law had to be changed in 2013, due to the fact that overhang seats can leave the parliament unproportional as it no longer matched the second votes.

Now, '**ausgleichsmandate**', or compensation seats, are given to make up to other parties for the fact that parties are given the overhang seats. These seats are added to make it as proportional as possible to the total second votes across the country.

The process to calculate the number of compensation seats to be given to each party is slightly complex. Firstly, calculate for each party the *number of second votes per seat*, that is
$$\frac{\text{Second Votes}}{\text{Minimum Seats } - 0.5}$$
Once all of these have been calculated for parties that made the second vote threshold, we then take the one with the smallest value and make that the 'federal divisor'.
$$ \text{Federal Divisor} = \text{min }_\text{all parties}\left(\frac{\text{Second Votes}}{\text{Minimum Seats } - 0.5}\right) $$
We then calculate for each party how many seats they would have attained, if the federal divisor was the number of second votes per seat.

$$ \text{Entitled Seats }\_\text{Party A} = \frac{\text{Second Votes }_\text{Party A}}{\text{Federal Divisor}} $$

If decimal points come out of this, these are rounded to the nearest integer. Therefore, we can determine the number of compensation seats by taking the minimum number of seats away from the new value.

We now have the number of seats each party is entitled to in the parliament. Parties then distribute these seats to the states using the Sainte-Laguë system and their second votes in each state.

# 2019 UK General Election under MMP

So, how would the UK election look under MMP? We use the same splitting of constituencies to list MPs as beforehand:

| Region | Constituencies | Party MPs |
|--------|----------------|-----------|
| East of England | 35 | 23 |
| East Midlands | 28 | 18 |
| London | 41 | 32 |
| North East England | 19 | 10 |
| North West England | 47 | 28 |
| Northern Ireland | 11 | 7 |
| Scotland | 37 | 22 |
| South East England | 50 | 34 |
| South West England | 34 | 21 |
| Wales | 28 | 12 |
| West Midlands | 37 | 22 |
| Yorkshire and the Humber | 33 | 21 |
| UK | 400 | 250 |

The last step of MMP to give balance seats increases the size of the House of Commons from 650 seats to 757 seats.

Therefore, we can map the results of the constituencies in the 2019 general election to 450 constituencies. We make an assumption that the popular vote in a region is the second vote, as there isn't any way of extracting a true second vote from FPTP.

Therefore, the results come out as follows:

|Party|MPs|% of votes|% of seats|
|-----|---|----------|----------|
|Conservative|332|43.6%|43.9%|
|Labour|245|32.1%|32.4%|
|Liberal Democrat|88|11.6%|11.6%|
|SNP|30|3.9%|4.0%|
|Green (England and Wales)|21|2.7%|2.8%|
|Brexit Party|16|2.0%|2.1%|
|DUP|6|0.8%|0.8%|
|Sinn Fein|5|0.6%|0.6%|
|Alliance|4|0.4%|0.5%|
|Plaid Cymru|4|0.5%|0.5%|
|SDLP|3|0.3%|0.4%|
|UUP|3|0.3%|0.4%|

Proportionally, this looks like an utterly superb result. With a maximum difference of 0.3% between the percentage of votes and percentage of seats, you can't do much better than that.

To empirically measure the proportionality, I'll use the Gallagher index that I brought up in my previous blogpost. You essentially check the difference between the percentage of seats and percentage of votes.

$$ Lsq = \sqrt{\frac{1}{2}\sum\limits_{i=1}^n \left(V_i - S_i\right)^2} $$


|Party|% of votes|% of seats|Difference|Sq. Dif|
|-----|----------|----------|----------|-------|
|Conservative|43.6%|43.9%|0.3%|0.09|
|Labour|32.1%|32.4%|0.3%|0.09|
|Liberal Democrat|11.6%|11.6%|0%|0|
|SNP|3.9%|4%|0.1%|0.01|
|Green (England and Wales)|2.7%|2.8%|0.1%|0.01|
|Brexit Party|2.0%|2.1%|0.1%|0.01|
|DUP|0.8%|0.8%|0%|0|
|Sinn Fein|0.6%|0.6%|0|0|
|Alliance|0.4%|0.5%|0.1%|0.01|
|Plaid Cymru|0.5%|0.5%|0|0|
|SDLP|0.3%|0.4%|0.1%|0.01|
|UUP|0.3%|0.4%|0.1%|0.01|

Summing the square differences up, halving the result and the square rooting it gives us **an index of 0.3464**.

## Sources

This blogpost would not have been possible if it wasn't for [Wahlrecht.de](https://www.wahlrecht.de/index.htm), the Holy Grail for explaining the German electoral system.

Furthermore, the results of the regions was calculated using the flat file of results from [Electoral Calculus](https://www.electoralcalculus.co.uk/homepage.html), a superb website that does in-depth analysis and predictions of UK elections.
