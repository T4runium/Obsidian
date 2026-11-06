Configurations of items can be represented using the **Balls in Boxes** analogy
"How many ways to sort $k$ into $n$?" depends on what counts as a different **configuration**

**Balls in boxes**: Both balls and boxes can be distinguishable or not (boxes may be empty)
	label the balls and boxes, then ask whether the labels matter

| balls | boxes | example (5 into 3) | count |
| --- | --- | --- | --- |
| distinguishable | distinguishable | 5 diners each pick 1 of 3 desserts | $n^k$ ([[Arrangements#Standard Problem 1\|SP1]]) |
| indistinguishable | distinguishable | 5 identical £1 coins into 3 charity boxes | ${}^{n+k-1}C_{k}$ ([[Arrangements and Combinations with Repetitions#Combinations with repetitions\|stars and bars]]) |
| distinguishable | indistinguishable | 5 people split into up to 3 teams | not covered in Michaelmas |
| indistinguishable | indistinguishable | 5p using at most 3 stamps | [[Partitions]] of 5 into at most 3 parts |

where $n=$ boxes and $k=$ balls

Distinguishable balls and bins:
Configurations $= n^k$  ^fd7bcd

**Context matters:** from the kitchen's point of view the diners are indistinguishable, so the dessert problem becomes the coins case. If the teams had names, the teams problem becomes the desserts case
