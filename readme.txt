-- Readme

Steps for execution (Windows):
The 190101029.cpp ,  input.txt  and linker_loader.cpp  file should be present in same folder.
For compilation :
g++ -o ./190101029.exe 190101029.cpp

This will create an executive file: 
Running the exe file :
./190101029.exe input.txt

This will produce 3 files:
    listing.txt
    intermediate.txt 
    output.txt

Now, for linking all the parts of the program and trying to execute the code we got, 
We have the linker_loader
This will be compiled as:
g++ -o ./linker_loader.exe linker_loader.cpp

This will create an executive file: 
Running the exe file :
./linker_loader.exe output.txt

This will ask PROGADDR : which is the location where this program is going to get loaded.
Just type '0' when asked about PROGADDR. (can also type other addresses but for simplicity let us keep it 0).

This will create some results which are stored in files namely:
    line_by_line => contains all the instruction and corresponding addresses
    memory 
    modifications => contains the result of operations performed


--
-- Documentation:
Some specifications are done in code file itself.
Naming:
CSECT => Identifies the start or continuation of a subroutine.
masking(value, nbits) => for a negative number, it cyclically converts it into binary number with number of bits = nbits
optab => operation table 
hlist => header informations for output file
elist => ending informations for output file
text_list => same as last time 

How to evaluate an Expression:
Step 1: Create an operand stack.
Step 2: If the character is an operand, push it to the operand stack.
Step 3: If the character is an operator, pop two operands from the stack, operate and push the result back to the stack.
Step 4:After the entire expression has been traversed, pop the final result from the stack.
https://www.codingninjas.com/blog/2021/10/01/expression-evaluation-using-stack/#:~:text=Step%201%3A%20Create%20an%20operand,final%20result%20from%20the%20stack.

DMAS priority:
According to DMAS, Division is given highest priority and subtraction lowest. This is taken care of using the precedence function.