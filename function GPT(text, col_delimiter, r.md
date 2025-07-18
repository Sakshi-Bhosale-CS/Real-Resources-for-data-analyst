function GPT(text, col\_delimiter, row\_delimiter) {

&nbsp; // Check if the text is provided

&nbsp; if (text == undefined) {

&nbsp;   return \[\['']];

&nbsp; }

&nbsp; 

&nbsp; // Split the text into rows

&nbsp; var rows = text.split(row\_delimiter);

&nbsp; 

&nbsp; // Split each row into columns

&nbsp; var result = rows.map(function(row) {

&nbsp;   return row.split(col\_delimiter);

&nbsp; });

&nbsp; 

&nbsp; return result;

}



Save the script with a name like “GPTFunction”.



How to Use the Custom GPT Function

The syntax for using the GPT function you created will be:



=GPT(text, col\_delimiter, row\_delimiter)



Example Usage:



#### **Example 1: Splitting text into columns**



Suppose you have the text string “Apple, Banana, Cherry” in cell A1 and you want to split it into separate columns based on the comma delimiter.



=GPT(A1, ", ", ";")

This will result in:



Apple     

Banana     

Cherry



#### **Example 2: Splitting text into rows**



If you have a text string “Apple; Banana; Cherry” in cell A1 and you want to split it into separate rows based on the semicolon delimiter.



=GPT(A1, ",", "; ")

This will result in:



Apple

Banana

Cherry



#### **Example 3: Splitting text into both rows and columns**



For a more complex scenario, if you have a text string “Apple, Banana; Cherry, Date” in cell A1 and want to split it into both rows and columns using commas for columns and semicolons for rows:



=GPT(A1, ", ", "; ")

This will result in:



Apple     Banana

Cherry    Date





###### **Notes:**



**Error Handling:** The custom function includes a simple check to handle cases where the input text is undefined, returning an empty cell in such cases.



**Flexibility:** You can further customize the script to handle more complex scenarios or additional features such as ignoring empty cells or trimming spaces.

This custom function in Google Sheets should help you achieve similar functionality to the TEXTSPLIT function in Excel, allowing you to split text based on specified delimiters.

