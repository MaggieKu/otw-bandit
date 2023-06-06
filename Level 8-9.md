bandit8@bandit:~$ strings data.txt |sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

Note:

in the man page for uniq -- "'uniq' does not detect repeated lines unless they are adjacent.  You may want to sort the input  first, or use 'sort -u' without 'uniq'."

^When I tried the above command with sort -u it didn't work. 

