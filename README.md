# CodeMonkey_scrm

```bash
git clone https://github.com/shajoezhu/CodeMonkey_scrm.git
cd CodeMonkey_scrm
```

```bash
git submodule add https://github.com/scrm/scrm.git
```

```bash
$ cat .gitmodules 
[submodule "scrm"]
	path = scrm
	url = https://github.com/scrm/scrm.git
```

```bash
$ git submodule init
$ git submodule update
```

Compile scrm
```bash
$ cd scrm
$ ./bootstrap
$make -mj4
```

```bash
$ git checkout -b doc origin/doc
$ sudo apt-get install doxygen graphviz
$ ./bootstrap
$ make doxygen-run
$ google-chrome doc/html/index.html 
```

file:///home/joezhu/CodeMonkey_scrm/scrm/doc/html/classForest.html
file:///home/joezhu/CodeMonkey_scrm/scrm/doc/html/classParam.html
file:///home/joezhu/CodeMonkey_scrm/scrm/doc/html/classModel.html

goto
Forest (Model *model, RandomGenerator *random_generator)
sampleNextGenealogy ()

```bash
$ ls tests/unittests/
$ make check -mj4
```

You should see
```
PASS: unit_tests
PASS: algorithm_tests
make[3]: Entering directory '/home/joezhu/CodeMonkey_scrm/scrm'
make[3]: Nothing to be done for 'all'.
make[3]: Leaving directory '/home/joezhu/CodeMonkey_scrm/scrm'
============================================================================
Testsuite summary for scrm 1.3.2.9000
============================================================================
# TOTAL: 2
# PASS:  2
# SKIP:  0
# XFAIL: 0
# FAIL:  0
# XPASS: 0
# ERROR: 0
============================================================================
```

```
$ cat .travis.yml
```

```bash
git checkout -b omp origin/omp
cd ..
aclocal
autoconf
automake -a
./configure
```

cd ..
time ./codeMonkey_scrm 30 1000 -r 100 10000 -seed 1 > /dev/null
real	0m6.035s
user	0m6.001s
sys	0m0.012s
time ./codeMonkey_scrm_omp 30 1000 -r 100 10000 -seed 1 > /dev/null
real	0m2.081s
user	0m7.533s
sys	0m0.658s
```

 - Import scrm as a submodule
 - Automake
 - Doxygen
 - Write a simple program
 - Tests utility
 - Continuous intergration
