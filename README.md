# Code Golf


### Overview
This competition focuses on short and succinct code. 
The challenge is to produce answers to the provided problems with as little code as possible.
Your score for each problem will be the file size of your source code for that problem. Your code will not be run. We will assume that your code runs. We will verify the answers your code produces.
However, we will have the 1st, 2nd, and 3rd place contestants run their code live for proof that
it runs and proof that it produces the correct output.
* **The actual code you submit cannot be generated text**
* Your code cannot call any external processes
* Your code must be able to be run independently of any other personal files (i. e. you can use standard libraries and other modules but you can't write code in another file and simply call it in your submission file)

### Submission
You will need to submit the source code for each question, so there will be a total of 6 files to submit.
Fork this GitHub repository, and just copy and paste your repository link [here](https://goo.gl/forms/86Y5OjwUCAlT9wI02)
* Each _solution_ file (your actual code) must be in a directory titled `solutions`
* Generate _answer_ files using your solution. The input files are in the `inputs` directory. Each individual input is separated by a newline. Separate your output in the file by newlines.
* Each _answer_ file (your generated answers) must be in a directory titled `answers`
* Each file must have the problem number somewhere in its name
* You should only submit the files we have asked for and nothing else
* There should be no dots ("." charachters) in your filename except before the extension
* The file size of your file will be evaluated with the python function [os.path.getzise](https://docs.python.org/2/library/os.path.html?highlight=os.path.getsize#os.path.getsize) on an Ubuntu OS. Make sure this is not problematic for your source code.
* **you cannot compress your files** you must submit your raw source code

#### Sample Valid Solution Filenames:
* prob_1.py
* prob1.py
* 1.java
* jibberish1jibberish.cpp

#### Sample Invalid Solution Filenames:
* i_dont_contain_a_number.py
* x.java
* get.ridOfThatExtraDot.cpp
* .filename.java

#### Sample Valid Answer Filenames:
* prob_1_out.txt
* prob1.txt
* 1.txt
* whatever1whatever.txt

#### Sample Invalid Answer Filenames:
* i_dont_contain_a_number.py
* x.txt
* get.ridOfThatExtraDot.cpp
* .filename.txt

### Questions

#### 1) Prime Counting Function

OVERVIEW
Given a positive integer, π(x) is the number of prime numbers less than or equal to x.

For example:
π(2) = 1
π(10) = 4
π(1000) = 168

The input has one value of x per line. You can expect x to be no greater than 1000. In the output, put one integer result per line.

#### 2) Prefix Notation

OVERVIEW
Given an expression in [prefix notation](https://en.wikipedia.org/wiki/Polish_notation), output the integer value.

For example:
+34 = 7
+5*34 = 12

The input has one expression per line. You can expect values between 0-9 (i.e. no numbers of multiple digits). Output one integer per line.

#### 3) Compound Words

OVERVIEW
Given a list of words, return all words that are _not_ compound and _not_ a part of a compound in the set. A compound word is a combination of two or more words in the set of words provided.

For example, if the set of words is:
'''
cat
dog
catdog
some
sometimes
'''

The output would be:
'''
some
sometimes
'''

Note that while `some` is a part of `sometimes`, `sometimes` is not a compound word because it is not a combination of two or more words in the set.

The input has one word in the set per line. In the output, put one word that meets the criteria per line.

#### 4) Best Fit

OVERVIEW
Given a list of `x` and `y` coordinates, produce the [least-squares best fit line](http://mathworld.wolfram.com/LeastSquaresFitting.html).

The input has one coordinate pair per line separated by a space.

Your output the ratio of `b/m`, when the equation is in the form:
```
y = mx + b
``` 
* Truncate (not round!) your answer to three (3) decimal places.
* Do not include a leading zero before the decimal for a number between 0 and 1 (i.e. .456, not 0.456)
* Include a negative sign (-) in front if necessary.

#### 5) Prime XML (from Google)

OVERVIEW
Given a positive integer, you will create a factor tree in a simple HTML/XML-like format.  For example, if the input was 2002 = 2 * 7 * 11 * 13, the correct output is:

```xml
<composite value="2002">
  <prime value="2">
  </prime>
  <composite value="1001">
    <prime value="7">
    </prime>
    <composite value="143">
      <prime value="11">
      </prime>
      <prime value="13">
      </prime>
    </composite>
  </composite>
</composite>
```

Each node must have 0 or 2 children.  A composite node's first child must be the smallest prime that divides into it.  Each line must be indented 2 spaces more than its parent.  No inputs will have prime factors larger than 40.

The input has one positive integer per line. In the output, put each factor tree (like above), separated by a newline.

#### 6) Big Numbers (from Google)

OVERVIEW
Given a spelled out integer between 0 and 999,999, your program will print out the numerical value of the number. There may or may not be commas and the word "and" in the standard places.

zero = 0
eighty-six = 86
one hundred and one = 101
nine hundred and ninety-nine = 999
three thousand, three hundred and thirty-three = 3333
nine hundred thousand, one hundred and eleven = 900111
nine hundred thousand and eleven = 900011

The input has one spelled out integer per line. In the output, put each numerical value on it's own line.