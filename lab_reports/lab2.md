## Lab 2 : Boolean Operation 
## Task 1 : Simplify F(A,B,C)= A'BC + AB'C + ABC' + ABC
      F(A,B,C)= A'BC + AB'C + ABC' + ABC
              = A'BC + ABC + AB'C + ABC + ABC' + ABC
              = BC + AC + AB
              = AB + AC + BC
## Circuit simulation :
![t1]()
## Task 2 : Simplify F(A,B,C)= A(A+B) (A+B+C)
       F(A,B,C)= A(A+B)(A+B+C)
               = (A + AB)(A+B+C)
               = A + AB + AC + AB + AB + ABC
               = A + AB + AC + ABC
               = A + AB + AC
               = A(1 + B + C)
               = A
## Circuit simulation :
![t2]()
## Task 3 : Simplify F(A,B,C)= (A+(BC)')'(AB + ABC)
      F(A,B,C)= (A+(BC)')'(AB + ABC)
              = AB(A + (BC)')'
              = AB(A + B' + C')'
              = AB (A'BC)
              = 0
## Circuit simulation :
![t3]()
## Task 4 : Simplify F(A,B,C)= (A+(BC)')'(AB + ABC)
     F(A,B,C) = (B'(A+B) + (A+B)(A+B'))B'
              =  (AB' + A + AB' + AB)B'
              = (A + AB + AB')B'
              = AB'(1 + ...)
              = AB'
## Circuit simulation :
![t4]()
