## **Lesson 1:- The 'IF' Command In Excel**
 
 - =IF (logical_test, [value_if_true], [value_if_false])
 -logical_test - A value or logical expression that can be evaluated as TRUE or FALSE.
 -value_if_true - [optional] The value to return when logical_test evaluates to TRUE.
 -value_if_false - [optional] The value to return when logical_test evaluates to FALSE.

## **Lesson 2:- The 'IF' Command In Excel Using Numerical Data**

 -Same as Lesson 1 but for Numerics...
 -Given the formula  =IF(A1>1000, 1000, A1)
 
 - Which of the following is true?
    If the value of A1 is -20, the formula will return 1000.
    If the value of A1 is 2000, the formula will return 2000.
    No matter the value of A1, the lowest value this formula will return is 0.
    No matter the value of A1, the highest value this formula will return is 1000.   (RIGHT)

## **Lesson 3:- The Nested 'IF' Command In Excel**
 
  - =IF (logical_test, [value_if_true], IF (logical_test, [value_if_true], [value_if_false]))

 ## **Lesson 4:- The 'VLOOKUP' Function in Excel**

  -=VLOOKUP(lookup_value,table_array,col_index_num,[range_lookup])
  -lookup_value- The value to search for in the first column of the table.
  -table_array- Two or more columns of data that is sorted in ascending order.
  -col_index_num-The column number in table from which the matching value must be returned. The first column is 1.
  -[range_lookup]-(Optional) Enter FALSE to find an exact match. Enter TRUE to find an approximate match. If this parameter is omitted,        TRUE is the default.
 
 -VLOOKUP formula, unlike the nested IF formulas, doesn't contain any actual data,this makes the formula much shorter and easier to           read.
 -I don't need to edit the formula to change the rules that determine the commission rate.
 -VLOOKUP has is transparency. 
 -Nested IF is better when you calculate for one condition, but not suitable for many conditions to check...this is when you use VLOOKUP.

 ## **Lesson 5:- Another VLOOKUP Example**

 -If in [range_lookup] its False and the data is not found it returns N/A; whereas when it is True the data to closer value(less than      given) will be returned.

 ## **Lesson 6:- The HLOOKUP Function In Excel**

 -=VLOOKUP(lookup_value,table_array,row_index_num,[range_lookup])
 -lookup_value- The value to search for in the first column of the table.
 -table_array- Two or more columns of data that is sorted in ascending order.
 -row_index_num-The column number in table from which the matching value must be returned.
 -[range_lookup]-(Optional) Enter FALSE to find an exact match. Enter TRUE to find an approximate match. If this parameter is omitted,         TRUE is the default.

## **Lesson 7:- Professor 'Know-it-all' Needs Help!**
 
 -The simulation enables the professor to call on students in a class at random.
 -Using RANDBETWEEN(bottom,top)....it generates a number randomly between the 2 given numbers.
 -We can have many Applications for this feature...where one example is being shown an directed in the video.

-Professor ‘Know-it-all’ wants to implement another system to call upon a group of students at random. She has created 4 groups:
1	GROUP 1
6	GROUP 2
11	GROUP 3
16	GROUP 4
Group 1: Students 1-5 Group 2: Students 6-10 Group 3: Students 11-15 Group 4: Students 16-20
    Her VLOOKUP function does not correctly return a random group. What is wrong with her function below?
  The lookup_value parameter should be “RANDBETWEEN(1,16)”.                 
  The table_array parameter should be “A3:B6”.                                                    
  The col_index_num parameter should be “1”.           =VLOOKUP(RANDBETWEEN(1,20),....,2.FALSE)                                           The [range_lookup] parameter should be “TRUE”.  (RIGHT)                              

**Final Assessment** 
 -Q8 Sol.=IF(OR($I2="Extra Large",$I2="XX Large",$I2="XXX Large"),($J2-$P2),$J2)
 -Q10 Sol.=IF(O2="Delivery Truck",($J2-$P2),$J2)
 
 **These are VLOOKUP TABLES...We can solve sums with multiple Conditions Using these Functions**

-Lookup Table 1	
 
 Order    Quantity	Type              
  

| Order |   Quantity	Type   |
| :---: | :---: | 
|  1	   |     Mini   |
|  6	   |   Extra Small    |
|  11	|       Small |
 | 16	  |   Small-Medium   |
 | 21    |  	Medium  |
 | 26	    |Medium-Large   |
 | 31	     |Large   |
 | 36	    |Extra Large  |
  | 41	   | XX Large   |
  | 46	    | XXX Large | 
 
   
    

