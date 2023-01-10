### Thompson Construction : 
- Use epsilon transitions
	- to glue together the machines of each piece of a regex
	- to form a machine that corresponds to whole expressions.
### Rules : 
- There is exactly 1 accepting state
- No transitions from accepting state
- No transitions into starting state.

##### Concatenation in Thompson:
- Connect them using epsilon : 
![[Pasted image 20230110022511.png]]
##### Choice in thompson :
- we add new start and new accept state and connect them using epsilon transition ex: 
![[Pasted image 20230110022644.png]]
#### Repetition : 
- add 2 new states start and accepting 
- the repitition is afforded by new transiton epsilon from accepting state of transition to its start state.
![[Pasted image 20230110023120.png]]
---
#### subset Construction:
- Convert NFA to DFA
##### Cases of non determinism: 
- Multiple transition on the same input symbol
- no transition on an input symbol
- epsilon transition : transition to a state without consuming any input
How to make it :
1. For every state in the NFA, determine all reachable states for every input symbol.
2. The set of reachable states constitute a single state in the converted DFA (Each state in the DFA corresponds to a subset of states in the NFA).
3. Find reachable states for each new DFA state, until no more new states can be found.
ex : 
![[Pasted image 20230110025456.png]]

---
