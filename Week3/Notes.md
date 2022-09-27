### Input Buffer 

#### std::ignore                  
The std::basic_istream::ignore is used to extracts characters from the input string and discards them including delimiting character, i.e.,
if the end of the file is reached this function stops extracting characters. The delimiting character is the new line character i.e ‘\n’.
This function will also stop extracting characters if the end-of-file is reached if the input is taken using a file.        
**Syntax**
```
istream& ignore(size N,int delim = EOF);
```
Parameters: It accepts the following parameters:              
                    

N: It represent maximum number of characters to extract.                   
delim: It is used for where stop the extraction.                     

