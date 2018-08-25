# chokotto
trivial scripts

## bash_scripts/chuuryaku
print head lines and tail lines
### usage
```
$ seq 30 50 | ./bash_scripts/chuuryaku
30
31
32
︙
48
49
50
$ seq 10 10000 | .bash_scripts/chuuryaku 5
10
11
12
13
14
︙
9996
9997
9998
9999
10000
```
one-liner version
```
$ (function cr(){ $1|(d=$(cat);l=${2:-3};echo "$d"|head -n $l;echo "︙";echo "$d"|tail -n $l)};cr "seq 100 2000" 5)
100
101
102
103
104
︙
1996
1997
1998
1999
2000
```
## bash_scripts/fizzbuzz
print fizzbuzz
### usage
```
$ ./bash_scripts/fizzbuzz | ./bash_scripts/chuuryaku 15
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
︙
86
Fizz
88
89
FizzBuzz
91
92
Fizz
94
Buzz
Fizz
97
98
Fizz
Buzz
```
