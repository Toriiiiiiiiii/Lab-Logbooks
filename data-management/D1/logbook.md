# Data Management Lab D1 Logbook

* Output of `grep -E '(colou?r|alumini?um|program(me)?|gr[ea]y)$' /usr/share/dict/words | wc -l`: 8
* Output of `grep -E gr[ea]y /usr/share/dict/words | sed s/[ea]/o/g | wc -c`: 1690
* Number of properties found from `cat AB_NYC_2019.csv | cut -d, -f3,10 | awk -F, 'BEGIN{sum=0} ($2>4){print $2;sum++} END{print "Found " sum " properties with over four reviews per month"}'`: 2988

## Understanding Test
* Number of unique users in dataset: 1076
* Number of usernames starting with a, b, c, d, or e: 294
* Number of characters of top 10 web pages: 
```
5084 sabf1u21
6780 gl1g23
9343 jgb1g21
9853 jp14g23
15359 pb8g23
16587 wp1g22
17875 dk1g22
20677 ng7g22
25965 sd8g22
421025 fjy1g23
```
