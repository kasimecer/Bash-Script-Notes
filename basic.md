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

```echo "2 + 4.6" | bc```

<pre>
echo "10 / 3" | bc

3

echo "scale=3; 10 / 3" | bc

3.333
</pre>

---

* Arrays:

```my_array=(1 2 3)```

<pre>
my_array=(1 3 5 2)
echo ${my_array[@]}

1 3 5 2


echo ${#my_array[@]}

4
</pre>

```array[@]:N:M```

<pre>
my_array=(15 20 300 42 23 2 4 33 54 67 66)
echo ${my_array[@]:3:2}

42 23
</pre>

Associative array (like dict in python)
<pre>
declare -A city_details # Declare first
city_details=([city_name]="New York" [population]=14000000) # Add elements
echo ${city_details[city_name]} # Index using key to return a value

New York
</pre>

-----

