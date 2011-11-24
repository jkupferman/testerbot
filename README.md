# testerbot
### Stupidly simple continuous testing

testerbot is a helpful little robot that watches your code and automatically runs your tests for you when it changes. It has no external dependencies and works with any testing tool that can be run from the command line.

### How do I run this awesomesauce?
* Clone the git repo `git clone git://github.com/jkupferman/testerbot.git`
* Go in the directory `cd testerbot`
* Run testerbot `./testerbot`

### Is it actually doing anything? It's just sitting there...
* Open `test/run` in your favorite editor in a separate tab
* Change `1999` to `2011`
* Hit save
* Watch it print `testerbot: the best since 2011`
* Sit and stare in awe...

### How do I run it with my testing tools
* Open `./testerbot` in your favorite editor and change RUN_TEST_COMMAND and DIRECTORIES_TO_WATCH
* Add it to your path
* Run it like boss

### How does it work?!
There is no magic here. We use `find` to determine if files have changed since the last test run. If files have changed we kick off the tests. Wrap that in a while true; and you pretty much have the code.

### Hey geniusboy, why not use autotest/inotify/(other existing tools)?
This is just a handy script I wrote to make sure I am always running the test suite. It is certainly not the smartest or most efficient script, but I find a lot of utility in the fact that has no dependencies and is language/framework independant unlike most other tools I've seen. 

Protip: If you are using Ruby use autotest, its *way* better than this :)

[Hank the testerbot](http://inhabitots.wpengine.netdna-cdn.com/wp-content/uploads/2010/06/snack-serving-robot-1.jpg)
