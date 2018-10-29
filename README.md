# Problem Set 4

Problem Set 4 challenges your ability to use (primarily) the `String` class and (to a lesser extent) the `Math` class. It is also the first problem set where, rather than printing output to the console, you'll be returning values from your methods.

## Getting Started

To get started, you'll need to create a [GitHub](https://github.com/) repository to store your Problem Set 4 code. After cloning my skeleton repository, you'll need to setup a remote to push your code to your repository instead of mine. Steps to accomplish this are outlined below.

### Setup

01. Login to your [GitHub](https://github.com/) account and create a new repository named `problem-set-4`.
02. In GitBash, navigate to your `APCSA` folder.
```
cd ~/Desktop/APCSA
```
03. Clone my skeleton repository from [GitHub](https://github.com/). This will make a copy of my repository and store it locally.
```
git clone git@github.com:rwilson-ucvts/java-pset-4-skeleton.git
```
04. The cloning process will have created a folder named `java-pset-4-skeleton`. Rename this folder to `pset4`.
```
mv java-pset-4-skeleton pset4
```
05. Change directories to get into your `pset4` folder.
```
cd pset4
```
06. Originally, the remote will be pointing at my repository. We need to overwrite this.
```
git remote rename origin upstream
```
07. Lastly, we need to add a new remote that points at the repository you created earlier. Make sure you replace `YOUR-USERNAME` with your actual username.
```
git remote add origin git@github.com:YOUR-USERNAME/problem-set-4.git
```
08. Launch Eclipse and set the `Workspace` to the `APCSA` folder you created on your `Desktop`. Make sure you're using your `Workspace`, as others' will be similarly named.
09. From within the `Package Explorer` (the left-most panel), right-click and select `Import...`.
10. Select `Git > Projects from Git`, and click `Next >`.
11. Select `Existing local repository` and click `Next >`.
12. Click the `Add...` button, and then the `Browse...` button.
13. Navigate to the `APCSA` folder on your `Desktop`, click the `pset4` project folder, and click `Open`.
14. Select the checkbox next to your project and click `Finish`.
15. Now that we've imported the Git project, we can click `Next >`, `Next >`, and `Finish` once more.

You should now see a `Project` in the `Package Explorer` in Eclipse.

16. Expand the `Project` folder. You should see the ```JRE System Library``` folder, as well as the ```src``` folder.
17. Expand the `src` folder. You should see a single source file named `ProblemSet4.java`. Double-click to open it.

## Exercises

Problem Set 4 contains 10 exercises, each of which will be written in separate methods. The `main` method has already been declared for you, but you'll need to implement most of it. You'll also need to declare and implement each of the 10 exercise methods. The specifications for this are included in this `README.md` file, as well as in comments within the `ProblemSet4.java` file.

### Exercise 1 (`surroundMe`)

`surroundMe` shoud be a publicly available  method that accepts a pair of `String`s as input, and returns a `String` as output.

Given two `String`s, `out`and `in`, return a new `String` built by surrounding `in` with the first and last two characters of `out`. Return `null` if the following specifcations are not met.
* `out` and `in` must not be `null`
* `out` must be exactly 4 characters
* `in` must be exactly 3 characters

```
surroundMe("<<>>", "abc") returns <<abc>>
surroundMe("[[]]", "xyz") returns [[xyz]]
surroundMe("abc", "abc") returns null
surroundMe("(())", "qwerty") returns null
surroundMe(null, "abc") returns null
surroundMe("<<>>", null) returns null
```

### Exercise 2 (`endsMeet`)

`endsMeet` shoud be a publicly available method that accepts a `String` and an `int` as input, and returns a `String` as output.

Given a `String`, `str`, and an `int`, `n`, return a new `String` built by combining the first `n` and last `n` characters of `str`. Return `null` if the following specifcations are not met.
* `str` must not be `null`
* `str` must be between 1 and 10 characters (inclusive)
* `n` must be a positive integer between 1 and the length of `str`

```
endsMeet("qwerty", 2) returns qwty
endsMeet("basketball", 3) returns basall
endsMeet("qwerty", -1) returns null
endsMeet("basketball", 0) returns null
endsMeet("qwerty", 9) returns null
endsMeet("programming", 2) returns null
endsMeet(null, 1) returns null
```

### Exercise 3 (`middleMan`)

`middleMan` shoud be a publicly available method that accepts a `String` as input, and returns a `String` as output.

Given a `String`, `str`, return a new 3-character `String` built from the 3 middle characters of `str`. Return `null` if the following specifications are not met.
* `str` must not be `null`
* the lenght of `str` must be odd

```
middleMan("candy") returns and
middleMan("programming") returns ram
middleMan("even") returns null
middleMan(null) returns null
```

### Exercise 4 (`doubleVision`)

`doubleVision` shoud be a publicly available method that accepts a `String` as input, and returns a `String` as output.

Given a `String`, `str`, return a new `String` built from duplicating every character in `str`. Return `null` if the following specifcations are not met.
* `str` must not be `null`

```
doubleVision("qwerty") returns qqwweerrttyy
doubleVision("a") returns aa
doubleVision(null) returns null
```

### Exercise 5 (`centered`)

`centered` shoud be a publicly available method that accepts a pair of `String`s as input, and returns a `boolean` as output.

Given two `String`s, `str` and `target`,  determine whether or not `target` is in the middle of `str`. `target` will be considered in the middle of `str` if the number of characters to its left and right differ by 0 or 1. Return `false` if the following specifcations are not met.
* `str` and `target` must not be `null`
* `target` must be exactly 3 characters

```
centered("candy", "and") returns true
centered("programming", "ram") returns true
centered("qwerty", "qwe") returns false
centered("qwerty", "er") returns false
centered("qwerty", null) returns false
centered(null, "abc") returns false
centered(null, null) returns false
```

### Exercise 6 (`upOrDown`)

`upOrDown` shoud be a publicly available method that accepts a `double` and a `char` as input, and returns an `int` as output.

Given a decimal value, `number`, and a character, `operation` (representing either round, `r`, floor, `f`, or ceiling, `c`), return the result of the operation as an integer. Return -1 if the following specifcations are not met.
* `operation` is not within the set [`r`, `f`, `c`]

```
upOrDown(12.7, 'r') returns 13
upOrDown(12.2, 'r') returns 12
upOrDown(12.7, 'f') returns 12
upOrDown(12.2, 'c') returns 13
upOrDown(12.7, 'x') returns -1
```

### Exercise 7 (`countMe`)

`countMe` shoud be a publicly available method that accepts a `String` and a `char` as input, and returns an `int` as output.

Given a `String`, `text`, and a character, `end`, count and return the number of words in `text` that end with `end`. For our purposes, the end of a word will be defined as an alphabetic character followed by a whitespace character (i.e., a space, tab, or line break) or no character at all (i.e., the end of the `String`). Return -1 if the following specifcations are not met.
* `text` must not be `null`
* `end` must be in the set [`Aa-Zz`]

```
countMe("these are just some sample words", 'e') returns 3
countMe(null, 'n') returns -1
countMe("and some more sample words", '+') returns -1
countMe("one more batch of sample words", 'h') returns 1
```

### Exercise 8 (`isNotEqual`)

`isNotEqual` shoud be a publicly available method that accepts a `String` as input, and returns a `boolean` as output.

Given a `String`, `str`, determine whether the number of case-sensitive appearances of the word `is` equals the number of case-sensitive appearances of the word `not`. Return `false` if the following specifcations are not met.
* `str` must not be `null`

```
isNotEqual("is not is not is") returns false
isNotEqual("is not is not is not") returns true
isNotEqual(null) returns false
```

### Exercise 9 (`triplets`)

`triplets` shoud be a publicly available method that accepts a `String` as input, and returns an `int` as output.

Given a `String`, `str`, return the number of triplets. A triplet is defined as a case-sensitive sequence of 3 identical characters in a row. A triplet can overlap, meanning "AAAA" counts as 2 triplets. Return -1 if the following specifcations are not met.
* `str` must not be `null`
* `str` must not contain whitespace or non-alphabetic characters

```
triplets("abbbccccd") returns 3
triplets("aaabbbbccccc") returns 6
triplets(null) returns -1
triplets("abbb1ccc") returns -1
triplets("aaa bbb") returns -1
```

### Exercise 10 (`addMe`)

`addMe` shoud be a publicly available method that accepts a `String` and a `boolean` as input, and returns an `int` as output.

Given a `String`, `str`, compute and return either the sum of the digits or the sum of the numbers contained within `str`. If `digits` is true, then sum the digits individually. If it is false, sum the numbers. A number is defined as a 1 or more consecutive digits in `str`. Return -1 if the following specifcations are not met.
* `str` must not be `null`
* `str` must not contain whitespace characters

```
addme("a123b456c789", true) returns 45
addMe("a123b456c789", false) returns 1368
addMe(null) returns -1
addMe("abc 123 def") returns -1
```

## Deadline

Your Canvas submission is due at or before 11:59pm on Sunday, November 4, 2018.

### Submission Requirements

All that is required for submission is the URL to your [GitHub](https://github.com/) repository for this problem set.
