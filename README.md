# Compiler Design
The first two stages in compiler design have been implemented in the given code. The grammar used in the case of lexical and semantic analyzer has been written below.

## Tokens for Lexical Grammar
variable: [a-zA-Z_][a-zA-Z0-9_]*,    
integer: d*,   
real: d* . d*,  
type: integer | real,   
assignment: :=,   
operator: +-*^/,  
end: ;,    
Declaration: :,   
Open Parenthesis: (,   
Close Parenthesis: ),   
Separator: ,     

## Grammar for Semantic Analyzer
Numeric -> [0-9]*   
Operator -> *|+|-|/|^    
Variable -> [a-zA-Z_][A-Za-z_0-9]*  
Type -> integer | real   
Statement_list -> Statement*   
Statement -> Declaration | Assignment    
Declaration -> Variable* : Type ;   
Assignment -> Variable := Expression ;   
Expression -> Addition   
Addition -> Multiply(+|-)Multiply    
Multiply -> Exponent(*|/)Exponent    
Exponent-> Base(^)Base    
Base -> Expression | lambda (INTEGER | REAL | VARIABLE | OPEN PARENTHESIS | CLOSE PARENTHESIS)   
