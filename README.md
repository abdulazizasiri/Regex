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

