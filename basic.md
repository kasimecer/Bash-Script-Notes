Command-Line & Bash Script

- Simple command-line Bash scripts 
```ls``` \n
```cd``` \n
```cat``` concatenates le contents line-by-line
```(e)grep``` filters input based on regex paern matching
```tail``` \ head give only the last -n (a ag) lines
```wc``` does a word or line count (with ags -w -l )
```sed``` does paern-matched string replacement

exp:
```
cat example.txt | egrep 'fisrt_word|second_word' | wc -l
```

- To cut out a relevant field with
```
cut
```
- like .value_counts:
```
uniq -c
```

exp: 
```
cat example.csv | cut -d "," -f 2 | tail -n +2 | sort | uniq -c
```

