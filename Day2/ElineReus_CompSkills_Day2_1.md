## Description of a data format 1 
# **CSV files**

### Key characteristics: 
* Main formatting rules:
  * Each record is on one line
  * Comma-delimited
  * Double quotes are special
  * Double-quote escape sequence 
  * Header information
* Useful to transfer data from a spreadsheet to other software
* No information about the location of data in the file
* Does not show whether data values represents numbers or text or something else
* It stores each data character in the computer memory as 1 or 2 bytes 

(Murrel, 2003)

### Example:
*The image is retrieved from the course material of the Measurement Strategies course of Future Planet Studies at the University of Amsterdam.*

![CSV file: the respiration of vegetation](https://github.com/ElineReus/AML/blob/master/Day2/CSV_example.JPG?raw=true)

### History (with references): 
CSV exist for quite a long time, since 1972 (SQLizer, 2017). It solves a problem that exists in normal plain text files, namely that fields are in each row of the file (Murrel, 2003). CSV files are mostly used to transfer data between databases (SQLizer, 2017).

### Tools that are able to handle these files: 
* There exist some freely available CSV readers/viewers/editors, the first two are mainly for reading the files, while the last one also gives the option to edit the file. 
* Programming programs such as Matlab and R have the option to load in CSV files, they then get stored as different combined vectors in a dataset. Instead of the comma separation there are columns (as in a spreadsheet) then, which makes the data easy to view. Also it makes the data easy to use in for example calculations as you can pick out one vector (or column) of data. 

### References
Murrel, P. (2003). Introduction to data technologies. CRC press. 
SQLizer (2017). A brief history of the CSV file. Retrieved 31-01-2017, from http://blog.sqlizer.io/posts/csv-history/
