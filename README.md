# Excel-and-Power_BI-Data-Analysis
At the beginning of the project, i noticed that there were a couple of blank cells and the likes in the execel dataset. So what i did, i assigned 0 to fill in the blanks in a numerical column and N/A to fill in the blanks in an alphabetical coloumn. 
For the power_bi dataset, some employees according to the dataset did not disclose their gender. For those set of people, i used the string "undisclosed" to identify them making it distint and easy to identify especially via the visualizations in the dashboard. This will help the organization easily identity and track the population of these set of people and making specific decisions conderning them.
For the excel dataset, a couple of calculated columns were creted before proceeding to solving the question. 
Below are the some of the questions solved with calculated columns.

Q1:  What is the average discount percentage by product category? 
    Applying the formula: J1*H1/J1*100
    ANS: A pivot table was used for this but before that, a calculated column was created applying the formula.
    
Q4: Which products have the highest average ratings? 
    ANS: The rating column was sorted in descending order and the top five products were selected.

    
Q6: Which products have the highest number of reviews?
    ANS: The rating count column was sorted in descending order and the top 5 products were selected.

    
Q7: How many products have a discount of 50% or more?
    Applying the formula: =IF(K1045>=50%,"Yes","No")
    ANS: 192. 

    
Q10: What is the number of unique products per price range bucket (e.g., <₹200, 
₹200–₹500, >₹500)? 
    Applying the formula: =IF(H1043<200,"<₹200",IF(OR(H1043=200,H1043<=500),"₹200 - ₹500",">₹500")) 
    ANS: <₹200 = 42, ₹200–₹500 = 103, >₹500 = 164.

    
Q9: What is the total potential revenue (actual_price × rating_count) by category? 
    Applying this formula: = (actual_price × rating_count)
    ANS: To get the total potential revenue, a calculated column named  total potential revenue was created by applying the formula.  
    
Q11:How does the rating relate to the level of discount? 
    Applying this formula:=IF(K1043<=10%,"0-10%",IF(K1043<=20%,"11-20%",IF(K1043<=30%,"21-30%",IF(K1043<=40%,"31-40%",IF(K1043<=50%,"41-50%",IF(K1043<=60%,"51-60%",IF(K1043<=70%,"61-70%",IF(K1043<=80%,"71-80%",IF(K1043<=90%,"81-90%","91-100%")))))))))
    ANS: This formula was applied and a sccatter chart was plotted. 
   ** Note: In my case, since i am dealing with a range of values (discount price bucket) in relation to a single value (rating), i represented the relationship using a histogram.**
   
  Q12: How many products have fewer than 1,000 reviews? 
      ANS: A filter was added to the review count column specifically to show the values below 1000. The count was applied and the answer gotten was 309.
      
  Q14: Identify the top 5 products in terms of rating and number of reviews combined. 
      ANS: The rating count column was sorted in descending order and the top 5 products were picked. The products are (using their product id):
        - B00ZRBWPA0
        - B09Y5FZK9N
        - B08QSC1XY8
        - B08QSDKFGQ
        - B09N3BFP4M

The two separate datasets were cleaned and analyzed using microsoft excel and power_bi respectively. Both analysis ended up with appealing and easy to understand visualizations.  
