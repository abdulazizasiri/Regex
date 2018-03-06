# Regex
_The challenge of regualr expression is both matching what you want and only what you want_ 

These are some ways to use regex: 


1- String literal: You spcifically tye the string that one wants to match.

### Metacharacters

#### Wild card .

- The wildcard character is the dot (.) character. It accepts any character except the newline. 
 
  _Example 1:_
  ```
  /h.t/ This matches hat, hot or any one character.This will not match heat. It is more than one character. 
  
  ```
Warning: The wild character can fit any character even characters that you do not want so sometimes it is best to escape it. 



- Escaping character: \
You can use it to escape metacharacters in regex. 

_Example 1:_

```
/9\.00 /: This is an example for escaping a wildcard character. 
```

_Example 2:_

Escaping a backslash char

```
/\\Desktop\

```
- Special character: 

 Spaces: literal space

 tabs: \t 
 
 Line returns (\r, \n, or \r\n)
 
 Non-printable characters
 the bell (\a), escape (\e), form feed (\f), vertical tab (\v)

ASCII or ANSI



#### Character Set []

 - []. it uses the opening bracket [  and closing ]. In between, you can have any characters, but when matching, it only chooses one character inside the character set. 
 
 _Example 1:_
 
 ```
 /gr[ae]y/
  matches: gray or grey NOT great because it only chooses one char inside the charset.  
 ```

#### Character ranges -

Note: The metacharacter used in character ranges "-" works only inside the character set. Otherwise, it is used as a normal character when typed outside the character set.  

_example 1:_

```
a[a-z]t

matches: abt, act, abt, aat But not: abbbt
```

#### Negative charcter set ^




NOTE: the carrot used differently in regex, and in each case, it has a  different meaning. Here is the first meaning when it is used with a character set. 


. Negate a character set. it means include any things except whatever inside the charcter set. 


_Example 2:_

```
[^aeiou]: Anything Except these 

Matches: snb : Note this must have a space at the end. 

An edge case is there must be a space at the end. 
```


#### Metacharacters inside character sets.

All metacharacter inside the character set are escaped. 

Exceptions are for ], - ,^, \

The above metacharacters need to be explicitly escaped. 


#### shorthand character set: 


| Sharthand        | Meaning           | equivalent  |
| ------------- |:-------------:| -----:|
| \d     | Digit | [0-9]
| \w     | word character      |   [a-zA-Z0-9_] |
| \s | whitespace     |    [ \t \r\n] |
| \D | Not digit     |    [^0-9] |
| \W | Not word character     |    [^a-zA-Z0-9_] |
| \S | Not whitespace     |    [^ \t \r\n] |



_Examples:_
```
\w\w\w\w\: Matches: "ABCD" "1234" "A_1_"
\d\d\d\d: Matches: "2017", but not "text".
\w\s\w\w: Matchses: "I am" But not "Am I" 
[\w\-]: Mathces word character or hyphen
[^\d]: same as \D and [^0-9]
```

Be careful In these example cases

```
[^\d\s] : It is not the same as [\D\S]

It  means: It is not a digit OR white space character

[\D\S]: it means, it is either a digit or NOT space char. :(

123-abc-^% : Each char is either a not space or a not digit: 

1---> is it not a digit? NO, is it not a space? Yes (matches)
a --> is it not a digit? Yes (matches)
.
.
..
```


#### Repetition characters: 

These characters affect whatever comes after them.

| Character        | Meaning    |     
| ------------- |:-------------:|
| *             | preceding item zero or more times
| +             | preceding item one or more times
| ?             | preceding item zero or one time

The + sign requires that the char after it MUST exist. 


