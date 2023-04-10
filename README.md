# CSLisp
An interpreter for The University of Alabama's Dr. Donald Yessick's flavor of the LISP language built in C#.

Contained within this directory is our implementation of the class’s version of Lisp. Test cases have been created to assess each feature required, as specified by the Lisp Spec sheet posted to Blackboard. These include: arithmetic expressions, variable assignment, function definition, function calls, and comparison expressions.

All comparison expressions have been created to output “True” for greater readability. For example, we would take the expression  
```(eq? (* 2 7) (- 14 1))		; False```  
and write it as  
```(nil? (eq? (* 2 7) (- 14 1)))	; True```  
so that there is not a mix of “True”s and “False”s that must be aligned with the output, should you choose to run the files    
#
# **Built-in Functions and Commands:**
\+  
\-  
\*  
\/  
\=  
<  
>  

DEFINE   
SET  
CONS  
COND  
CAR  
CDR  
NUMBER?  
SYMBOL?  
LIST?  
NIL?  
EQ?  
#
# **Built-in Function and Command Defintions
COND  
```(cond t1 r1 t2 r2 t3 r3)```  
if t1 is true returns r1...if t2 is true return r2...  
Most efficient if lazy evalauation is used.  
Behavior undefined if no tn is true. (probably return nil, buit exit(1) is also fine)   
SET  
```(set name exp)```  
The symbol name is associated with the value of exp

**\+**  
```(+ expr1 epr2)```  
* Returns the sum of expressions. The expressions must be numbers

\-
```(+ expr1 epr2)```  
* Returns the difference of expressions. The expressions must be numbers

\*
```(* expr1 epr2)```  
* Returns the product of expressions. The expressions must be numbers

\/
```(/ expr1 epr2)```  
* Returns the quotient. The expressions must be numbers

\=
```(= expr1 expr2)```  
* Compares the values of two atoms or (). Returns () when either expression is a larger list.

<
```(< expr1 expr2)```  
* Return t when expr1 is less than expr2. Expr1 and expr2 must be numbers.

>
```(> expr1 expr2)```  
* Return t when expr1 is greater  expr2. Expr1 and expr2 must be numbers.

CONS
```(cons expr1 expr2)```  
* Create a cons cell with expr1 as car and expr2 and cdr: ie: (exp1 . expr2)

CAR
```(car expr)```  
* Expr should be a non empty list. Car returns the car cell of the first cons cell

CDR
```(cdr expr)```  
* Expr should be a non empty list. Cdr returns the cdr cell of the first cons cell

NUMBER?
```(number? Expr)```  
* Returns T if the expr is numeric, () otherwise

SYMBOL?
```(symbol? Expr)```  
* Returns T if the expr is a name, () otherwise

LIST?
```(list? Expr)```  
* Returns T iff Expr is not an atom

NIL?
```(nil? Expr)```  
* Return T iff Expr is ()

Define
(define name (arg1 .. argN) expr)
Defines a function, name. Args is a list of formal parameters. When called the expression will be evualuated with the actual parameters replacing the formal parameters.
Informative: call syntax
(funname expr1 exprN)
Calling of function defined by funname. The expressions are evaluated and passed as arguments to the function.
