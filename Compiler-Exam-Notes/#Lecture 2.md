### Recap:
- We said that **lexemes** are sequance of chars that are used to turn them into logical units called **Tokens**
---
- Tokens are logical entities defined as an enumerated type.
- ![[Pasted image 20230109233130.png]]
- Strings are called String Value Or **Lexeme of Tokens**.
- Some tokens have only one lexeme, such as reserved words.
---
- Atribute : Any Value associated to a token .
---
### Regular expressions :
- First lets Talk about Automata theory : 
	- It is the Study of Abstract Computing devices *Machines*
	- Automaton : abstract Computing device.
	- A Device doesn't need to be a physical hardware.
- Languages : A Language is a collection of sentences of finite length all constructed from a finite alphabet of symbols.
- Grammer :" grammar can be regarded as a device that enumerates the sentences of a language” - nothing more, nothing less
- Many infinite languages have finite descriptions:
	a) Define the language using a regular expression.
	b) Define the language using an automaton.
	c) Define the language using a grammar.
---
### Alphabet rules :
- We Use Sigma symbol to denote alphabets (∑):
	- Example : Binary: ∑ = {0,1}.
- Empty String : epsilon ( ε) 
- if he asked for |x|= the sum of numbers or strings without the epsilons.
- xy=> concat of xy.
- Regular expression : represent pattern of strings of characters.
	- completely defines by the set of strings it matches.
	- The set is called the language of r written as L(r)
___
### Regex Rules:
- we can use escape characters to turn of the special meaning ex : \*\*
- a matches the character a by writing L(a)={a},
- ε denotes the empty string, by L(ε)={ε}
- {} or Φ matches no string at all, by L(Φ)={ }
#### Operations : 
- Choice : among alternatives, indicated by the meta-character (|) **(OR)** ex :(A|Z).
- Concatenation : indecated by juxtaposition ex:(xy)
- Repetition or "Closure" : indecates by character (\*) and is used to match 0 or more
#### Choice :
- L(r|s)=L(r) U L(s).
- L(a|b)=L(a)U (b)={a, b}
#### Concatenation:
- L(a|b)c ={ac, bc}
#### Repetition:
- r* where r is a regex.
- The Regex r* matches any finite concate of string , each of which matches r.
- ex : a* = ε, a, aa, aaa,...
---
### Precedence of Operations : 
1. Repetition \*
2. Concatenation 
3. Choice is the lowest
Ex : a|bc* =>a|(b(c*))
Note: Parentheses is used to indicate a different precedence.

---
### Name of a regex :
- we can give a name to regular expression to use it easier Like :
- digit = 0|1|2|3|4......|9
-  (0|1|2|3......|9)(0|1|2|3......|9)* => digit digit*
---
7l:
1-(a|c)\*b(a|c)\*
2- (a|c)\*b(a|c)\*|(a|c)\*
3- (a|c|ba|bc)\*(b|epsilon).
4. (a|c|ba|bc)\* b?.
---
### List of New Operations : 
1. One or more : r+
2. a range of characters :\[0-9\] , \[a-zA-Z\]
3. any char period : .
Note => Data separator hya ele btost5dm 34an t2t3 el data fl date wkda.
4. Any Char not in a given set (~) ex : ~(a|b|c) not a or b or c.
5. Optional = r?