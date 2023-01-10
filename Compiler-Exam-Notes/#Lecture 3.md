### Finite automata :
- from it's apps : Lexical analysis of a typical compiler.
- Finite automata (finite-state machines) is a mathematical way of describing particular kinds of algorithms.
**Transitions** : Records change from one state to another by matching characters which is labeled with.
![[Pasted image 20230110015749.png]]
**Start State** :
- Where the recognition process begins.
- Drawing an unlabeled arrowed line to it coming “from nowhere”
- ![[Pasted image 20230110015801.png]]
**Accept state** :represent the end of recognition && draw double line border around.
ex :
![[Pasted image 20230110015808.png]]
total ex : 
![[Pasted image 20230110015708.png]]

---
### DFA (Deterministic Finite State):
- Automata where the next state is uniquely given by the current state and the current input character.
---
### NFA (NON-Deterministic Finite State):
- More than one transition from a state may exist for a particular character.
- Subset Construction Algorithm: Developing an algorithm for systematically turning these NFA into DFAs.
- Thompson’s Construction : a method for converting Regular Expressions to NFAs.
##### ε -TRANSITION IN NFA:
- A transition that may occur without consulting the input string (and
without consuming any characters)
ex : 
![[Pasted image 20230110021216.png]]
