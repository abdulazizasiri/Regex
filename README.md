# Regex
_The challenge of regualr expression is both matching what you want and only what you want_ 

These are some ways to use regex: 


1- String literal: You spcifically tye the string that one wants to match.

### Metacharacters

#### Wild card

- The wildcard character is the dot (.) character. It accepts any character except the newline. 
 
  _Examples:_
  ```
  /h.t/ This matches hat, hot or any one character.This will not match heat. It is more than one character. 
  
  ```
Warning: The wild character can fit any character even characters that you do not want so sometimes it is best to escape it. 



- Escaping character: \
You can use it to escape metacharacters in regex. 

_Examples:_

```
/9\.00 /: This is an example for escaping a wildcard character. 
```


