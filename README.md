# awk
Statistics using awk:

#### Mean
```
```
Population standard deviation of a list of numbers:
```
awk '{x+=$0;y+=$0^2}END{print sqrt(y/NR-(x/NR)^2)}'
```
Sample standard deviation:
```
awk '{sum+=$0;a[NR]=$0}END{for(i in a)y+=(a[i]-(sum/NR))^2;print sqrt(y/(NR-1))}
```
