Command-Line & Bash Script

- Simple command-line Bash scripts 

```ls```

```cd```

```echo```


```cat```: concatenates le contents line-by-line

```(e)grep```: filters input based on regex paern matching

```tail```, ```head```: give only the last -n (a ag) lines

```wc```: does a word or line count (with ags -w -l )

```sed```: does paern-matched string replacement

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
```cat example.csv | sed 's/exist_name/new_name/g' | sed 's/exist_name/new_name/g' > example_edited.csv```

* Arguments with standart stream codes

STDIN (standard input): A stream of data into the program

STDOUT (standard output): A stream of data out of the program

STDERR (standard error): Errors in your program

STDIN exp:
```
cat file.txt > new_file.txt
```

* ARGV:

```$@```  and ```$*``` give all the arguments in ARGV

```$#``` gives the length (number) of arguments


---

* Variables

```var1="Come on!"```

```echo $var1```


<pre> 
var='ABCDE'
var_singlequote='$var'
echo $var_singlequote

$var 

var_doublequote="$var"
echo $var_doublequote

ABCDE
</pre>

----

```date```



<pre>
var="The date is`date`."
echo $var

The date is Mon 5 Feb 2020 14:44:12 AEDT.
</pre>

<pre>
var1="The date is`date`."
var2="The date is $(date)."
echo $var1
echo $var2

The date is Mon 5 Feb 2020 14:43:55 AEDT.
The date is Mon 5 Feb 2020 14:43:55 AEDT.
</pre>

---
```bc``` (basic calculator) 
