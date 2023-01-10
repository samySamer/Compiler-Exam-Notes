### What is compiler ? 
- it takes source program and turn it into target program.
### why study complier ?
- increase understand of language semantics.
- Teach good language design.
- Seeing the machine code generate for language construct helps understand performance issues for language.
- New Device may need device specific languages.
- New business field may need domain-specific language.
---
#### 1. preprocessor:
- Delete comments
- include other files by #include
- perform macro substitions.
---
#### 3. assembler : 
- a translator from target code to object code(machine code).
---
#### 4. Linker :
- Collect all object files into one directly excutable file.
- Depends on processor and Os.
---
#### 5.Loader:
- A part of operating systems responsible for loading programs and libraries in memory.
- one of the essential stages of program.
- it loads the files in memory and execute them.
---
#### 6. Editor:
- The IDE.
- may include some operations of a compiler,like informing the developer with some syntax errors.
---
#### 7.Debugger : 
- Used to determine runtime error in a complier.
---
#### 8. Profile: 
- Collect statistics on the behavior of an object program during execution.
- % of execution time.
- used to improve the execution speed of the program.
---
#### 9. Project Manager : 
- Coordinate the files being worked on by different people , maintain coherent version of program.
- Two examples : 
	- SccS 
	- RCS
---
### Compiler Vs Interpreter :
##### Compiler : 
- Turn Source code all at once into target Code.
- Ex : C , C++
- Intermediate code generation
##### Interpreter : 
- Turn statement(line by line) by statement and interpret it into execution.
- Ex : Basic, Lisp
- speed of execution slower.
---
### The whole comparison: 
![[Pasted image 20230109223658.png]]

---

#### Java : uset Jit (Just in time):
start complied and then turn interpreted.

---
### Complier Views : 
- First View Of A complier : 
![[Pasted image 20230109223840.png]]
Second View Of a complier More Important than first view : 
- first  three steps are the analysis at the first view
- then synthesis
![[Pasted image 20230109224040.png]]
Sourcecode=>(Scanner)=>Tokens
Tokens=>(Parser)=> Syntax tree.
Syntax Tree=>(Symantics analyzer)=>annoted tree.
annoted Tree =>Source Code Optimizer=>intermediate Code(IR)
IR=>(Code generator)=>Target Code
Target Code => (Target Code Optimizer)=>Optimized Target code.
## All these phases use these tables :
#### 1.Literal Table : Strings & Constants
#### 2. Symbol Table : Asami el functions and variables.
#### 3. Error handler : Byt3amel m3 el errors.
 ---
### 1. Lexical analysis : 
- byt3amel m3 lexeme w token.
	- lexeme : Sequance of Characters.
	- Token : maping lexemes into meaningful units.
---
#### 2. Parser (syntax analyzer):
- Syntax analysis : it determine structure of program.
- The result of syntax analysis is a **parse tree** or a **syntax tree**.
- Parse tree ex : 
![[Pasted image 20230109225337.png]]
- Syntax tree The more simple one : 
![[Pasted image 20230109225420.png]]
#### Syntax tree Vs Parse tree Comparison:
![[Pasted image 20230109225508.png]]

---
#### 3. Symantic analyzer:
- It is the meaning of code 
- Static symantics : declerations and type checking.
- Ex : annotated syntax tree=>the red things after symantic
![[Pasted image 20230109225853.png]]
---
#### Source Code Optimizer : 
- optimized annotated tree.
- it depends only in optimization on source code
- ex : 
![[Pasted image 20230109230035.png]]
---
#### 5. The Code Generator : 
- it takes The IR (intermediate Code) and generates code for target machine.
- ex :
![[Pasted image 20230109230241.png]]
---
#### 6. Target code optimization : 
- it improves the Target Code generated.
- ex : ![[Pasted image 20230109230320.png]]
---
