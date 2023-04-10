# CSLisp
An interpreter for The University of Alabama's Dr. Donald Yessick's flavor of the LISP language built in C#.

Contained within this directory is our implementation of the class’s version of Lisp. Test cases have been created to assess each feature required, as specified by the Lisp Spec sheet posted to Blackboard. These include: arithmetic expressions, variable assignment, function definition, function calls, and comparison expressions.

All comparison expressions have been created to output “True” for greater readability. For example, we would take the expression  
```(eq? (* 2 7) (- 14 1))		; False```  
and write it as  
```(nil? (eq? (* 2 7) (- 14 1)))	; True```  
so that there is not a mix of “True”s and “False”s that must be aligned with the output, should you choose to run the files
