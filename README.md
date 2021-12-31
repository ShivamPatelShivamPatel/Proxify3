# Proxify3

### A version of the original proxify by Somdev Sangwan that is compatable for recent versions of python.  I was recommended his tool, but upon trying to get it from pip/pip3 I encountered version errors. So I decided to download his source code, see the compatability problem, fix it, and reupload it to PyPi as proxify3 as the original package is a few years old and they haven't answered to 2 year old user complaints from 2019, since im having the same problem now in December 2021.  Hopefully I'll be more responsive if people want me to make it more backwards compatable, change the implementation, add a function and things like that since I intend to use this package myself.

### other than that as far as code modification you can see the commit log in the proxify repo that I forked off the original people who made it, when I tried to run some functions from the original proxify.py that was throwing the versioning error(when you tried to use pip to install it) it had an out of bounds error on the list in list2dict:

"it might be because the original author was using an older version.  But problem is that in the list2dict, for some proxy types there may not be an x[7].  Perhaps its due to the implementation of the underlying modules like urllib and re changed after python 2.8 since the error from pip, pip3 is "ERROR: Package 'proxify' requires a different Python: 3.7.9 not in '<=2.8,>=2'"

### My intent in the use of this package is to be able to bypass API/Request limits when webscraping, for example my laptop has 4 cores, so web scraping tasks in theory could get a 4x speed up if you could use all the cores and assign them jobs cleverly if it wasn't for the target website logging IP addresses and User Agents.  But since this package will generate you a list of proxys to essentially feed as a parameter into the requests module(these proxys will be dirty in all likelihood so use with caution, probably used excessively in illicit activities, but I don't imagine that will inhibit anyone trying to scrape government websites or listing website.)  Other than that, the code and usage of the module is essentially the same as the original outside of checking for an out of bounds error, so see the original authors README for documentation and usage: https://github.com/s0md3v/proxify

