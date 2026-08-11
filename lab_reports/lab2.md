## Lab 2 : Boolean Operation 
## Task 1 : Simplify F(A,B,C)= A'BC + AB'C + ABC' + ABC
      F(A,B,C)= A'BC + AB'C + ABC' + ABC
              = A'BC + ABC + AB'C + ABC + ABC' + ABC
              = BC + AC + AB
              = AB + AC + BC
## Circuit simulation :
![t1](https://github.com/Shabib145/ECE-2112_2410006/blob/main/lab_reports/images/l2/DT_l2_T1.png?raw=true)
## Task 2 : Simplify F(A,B,C)= A(A+B) (A+B+C)
       F(A,B,C)= A(A+B)(A+B+C)
               = (A + AB)(A+B+C)
               = A + AB + AC + AB + AB + ABC
               = A + AB + AC + ABC
               = A + AB + AC
               = A(1 + B + C)
               = A
## Circuit simulation :
![t2](https://github.com/Shabib145/ECE-2112_2410006/blob/main/lab_reports/images/l2/DT_l2_T2.png?raw=true)
## Task 3 : Simplify F(A,B,C)= (A+(BC)')'(AB + ABC)
      F(A,B,C)= (A+(BC)')'(AB + ABC)
              = AB(A + (BC)')'
              = AB(A + B' + C')'
              = AB (A'BC)
              = 0
## Circuit simulation :
![t3](https://github.com/Shabib145/ECE-2112_2410006/blob/main/lab_reports/images/l2/DT_l2_T3.png?raw=true)
## Task 4 : Simplify F(A,B,C)= (A+(BC)')'(AB + ABC)
     F(A,B,C) = (B'(A+B) + (A+B)(A+B'))B'
              =  (AB' + A + AB' + AB)B'
              = (A + AB + AB')B'
              = AB'(1 + ...)
              = AB'
## Circuit simulation :
![t4](https://github.com/Shabib145/ECE-2112_2410006/blob/main/lab_reports/images/l2/DT_l2_T4.png?raw=true)
