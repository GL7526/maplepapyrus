# Maple Papyrus
Maple Papyrus is a minigame in the game Maplestory where you obtain 3 numbers sequentially from 1 to 16 to fit the format (a + b) * c, where a, b, and c are numbers from 1 to 16. You can then either keep your current order or reroll the order.
The python script, maplepapyrus, lets you input the 3 numbers and tells you the best course of action to take.

# The Numbers
At it's core, Maple Papyrus just a simple game of combinatorics and statistics. We can list out the possible combinations and assign the probabilities to get each of them, which luckily for us, seems to be equal. If our current combination is higher than the expected value of all the possible outcomes, then it is better to keep the current combination. Otherwise, we should reroll.
