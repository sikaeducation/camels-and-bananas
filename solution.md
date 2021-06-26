# Camels and Bananas

## Solution:

533 bananas

Read alternative solution, same answer, [here](http://www.crazyforcode.com/camel-bananas-puzzle/)

---

Solution for `n` bananas, where `n` is the number of bananas you own, and `c` is the number of bananas the camel can carry:

* For bananas `0` → `c`, the cost to move a banana is 11 banana per km.
* For bananas `c + 1` → `2c`, the cost to move a banana is 33 bananas per km.
* For bananas `2c + 1` → `3c`, the cost to move a banana is 55 bananas per km.

This is because, if the camel moves the bananas 1km at a time, he needs to make two trips for each load beyond his current capacity.

`t = ⌊nc⌋`. Therefore, the total number of miles the camel can reach is:

`(∑k = 1tc2k−1) + (n mod c)2t + 1`

In particular, plugging in the given `n=3000` and `c=1000`, we have that the camel can travel

`1000 + 333 + 200 = 1533 miles`

To figure out how many bananas remain for a given distance, subtract the extra miles and multiply back at the rate given above.

For the first 1000 miles, this number is just the distance beyond the total capacity `1533 − 1000 = 533`, or 533 bananas.
