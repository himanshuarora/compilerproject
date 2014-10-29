
Full Project report : https://www.dropbox.com/s/06fkp1lr5ghcp96/Compiler%20Report%28comp%29.doc?dl=0
===============

USER FRIENDLY FORMATTING LANGUAGE

GRAMMAR

Input	       -> 	Input Line 
      	| ε
Line	       ->   END  
     	| Func END 
     	| Expression END 
Expression ->	 Value
		|	 Expression PLUS Expression	
		| 	Expression MINUS Expression	
		| 	Expression TIMES Expression	
		| 	Expression DIVIDE Expression	
		|	MINUS Expression %prec NEG	
		| 	Expression POWER Expression	
		| 	LEFT_PARENTHESIS Expression RIGHT_PARENTHESIS	
Func              ->	PI LEFT_PARENTHESIS List RIGHT_PARENTHESIS
             |	BARG LEFT_PARENTHESIS   List   RIGHT_PARENTHESIS 
             |	PLOT LEFT_PARENTHESIS    PointList    RIGHT_PARENTHESIS	
	             |	 TABLE NAME LEFT_PARENTHESIS RowDetail   RIGHT_PARENTHESIS	
List	         ->   NAME COMMA Value   List1
List1	         ->   COMMA NAME COMMA Value List1 
		| ε
PointList        ->   LEFT_PARENTHESIS OP COMMA OP RIGHT_PARENTHESIS PointList1 
PointList1      ->   COMMA LEFT_PARENTHESIS OP COMMA OP RIGHT_PARENTHESIS PointList1
		| ε

value           ->   OP
	            |NUMBERRowDetail:
	            | LEFT_PARENTHESIS ColList RIGHT_PARENTHESIS RowDetail1 		
  RowDetail1->   COMMA LEFT_PARENTHESIS ColList RIGHT_PARENTHESIS RowDetail1 		
	            |	ε		          
ColList 	       ->   MyValue Value1
 Value1	       ->   COMMA MyValue Value1
	            | ε	
MyValue     ->   OP	
	            | NUMBER	
	            | NAME	






