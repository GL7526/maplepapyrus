
<p align = "center">
  <img src = "images/cleaned1plus1times1.jpg">
</p>

# Maple Papyrus
Maple Papyrus is a minigame in the game Maplestory where you obtain 3 numbers sequentially from 1 to 16 to fit the format (a+b)\*c, where a, b, and c are numbers from 1 to 16. You can then either keep your current order or reroll the order. The goal of this minigame is to get as high of a result as possible.
The python script, maplepapyrus, lets you input the 3 numbers and tells you the best course of action to take.


# The Numbers
At it's core, Maple Papyrus just a simple game of combinatorics and statistics. We can list out the possible combinations and assign the probabilities to get each of them, which luckily for us, seems to be equal. If our current combination is higher than the expected value of all the possible outcomes, then it is better to keep the current combination. Otherwise, we should reroll.

Listed out, there are six possible combinations:
<br>
(a+b)\*c
<br>
(a+c)\*b
<br>
(b+a)\*c
<br>
(b+c)\*a
<br>
(c+a)\*b
<br>
(c+b)\*a

You might have noticed that thanks to the commutative property of addition, we really have only three possible outcomes:
<br>
(a+b)\*c
<br>
(a+c)\*b
<br>
(b+c)\*a

These three values are initial, alt1, and alt2, in the script.
<br>
The expected value would be the sum of these three values divided by 3, and with this, we can tell the user to either keep or reroll their current value.
<br>
<br>
### The Gamblers
However, there's also a chance that the user is willing to take risks, no matter what. An example of this is if someone rolls something like (1+16)\*15.
<br>
Their current outcome would be 255. If they reroll, they can either get the same value, 256, or 31. Logically, it would make sense to keep their current outcome because the potential loss greatly outweighs how much they can gain. However, for someone who may want to gamble for any potential gain, they can, and will reroll. Therefore, it may be better to have four different recommendations in the script.
<br>
The two obvious recommendations should occur when the user already has either the highest or lowest possible outcome. If the person obtains the highest possible outcome, they should not reroll, and if the person obtains the lowest possible outcome, they should always reroll.
<!-- write out the values. increase of only 1 vs loss of ___ etc -->

# **Work In Progress**
## Currently, the python script is outdated because it was created at the release of the minigame, where I made some incorrect assumptions. I assumed that all 3 numbers are unique from each other and that we cannot obtain our current combination again upon rerolling.
