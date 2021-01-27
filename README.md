# rr-wrangle
Demo on data wrangling using Bash

## Assigned play

* The Tragedy of Coriolanus by "Shakespeare"

``` 
http://shakespeare.mit.edu/coriolanus/full.html
```

* Speaker 1 :- BRUTUS
* Speaker 2 :- CORIOLANUS

## Bash Commands
- curl command to fetch the data 
```
curl "http://shakespeare.mit.edu/coriolanus/full.html" -O > input.txt
```
- To count the number of times 'BRUTUS' 
```
grep -i 'BRUTUS' input.txt -c
```
- To calculate the number of words "CORIOLANUS"
```
grep -i 'CORIOLANUS' input.txt -c
```
- Total number of words calculated for both 'BRUTUS' and 'CORIOLANUS'
```
$ eval "$(paste -d+ <(sed 's/\(.*\)/echo $((\1/' brutusCount.txt) <(sed 's/\(.*\)/\1))/' coriolanusCount.txt))"

```

## Resources
- [Total count of two words](https://unix.stackexchange.com/questions/501486/how-do-i-add-numbers-from-two-txt-files-with-bash)
- [Calculation of multiple words](https://stackoverflow.com/questions/7171891/how-do-i-find-the-count-of-multiple-words-in-a-text-file)