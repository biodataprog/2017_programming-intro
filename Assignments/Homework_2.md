Homework 2: Python Basics
=========================

1. __Write a python program called `print_triples.py`__.
Print out all the numbers from 0 to 100 and print a * next to the numbers which are perfectly divisible by 3.

 - Do this by making a loop which counts up from 0..100
 - Check the number to see if it is divisible perfectly by 3 (no remainder)
 - Print a `*` next to the number if that is the case

__Output should look some like__
: ```
0
1
2
3 *
4
5
6 *
```

2. __Write a replacement for the unix tool word count: `wc`.__
The program should print out the number of lines in an input file - store your
code in the script `wc.py`.

* _Bonus for the more advanced_ - also print out the number words and characters found in the file.

3. __Read in the codon table file and print some specific patterns.__
The file is `codon_table_compact.txt` and is provided in the homework
template you will get when you clone the repository. It is also
available
[codon_table_compact.txt](https://biodataprog.github.io/programming-intro/data/codon_table_compact.txt). This
file has 3 columns which list the 3 letter codon, the amino acid
abbreviation, and the full amino acid name.  Your program will be
written in the script `codon_table_count.py`

* For each amino acid, print out the number of codons which code for it
* Print out the total number of amino acids and codons seen.
* Print out the number of Amino acids which are four-fold degerate
  (are encoded by 4 or more codons).  Also print out these amino acids
  at the end.

The report can look something like:

: ```
Amino acid X is encoded by Y codons
...
...
===
There are X total amino acids and X codons
There are X AAs which are four-fold or six-fold degenerate
These AAs are:
  X
  Y
  Z
```
