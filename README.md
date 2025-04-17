# python-week-4-assign
python file_processor.py
Please enter the name of the file to process: my_document.txt
Attempting to read from: 'my_document.txt'
Output will be written to: 'my_document_modified.txt'

Processing file...

Success! File processed.
Read 3 lines from 'my_document.txt'.
Modified content written to 'my_document_modified.txt'.

Output file my_document_modified.txt:

1: This is the first line.
2: This is the second line.
3: And a third line here.python file_processor.py

###  File not found error

Please enter the name of the file to process: non_existent_file.txt
Attempting to read from: 'non_existent_file.txt'
Output will be written to: 'non_existent_file_modified.txt'

--- Error ---
The file 'non_existent_file.txt' was not found.
Please check the filename and its location.

### Permission Error (Conceptual Example)
***(This error depends on your actual file system permissions.)***
python file_processor.py
Please enter the name of the file to process: restricted_file.txt
Attempting to read from: 'restricted_file.txt'
Output will be written to: 'restricted_file_modified.txt'

--- Error ---
Permission denied.
Could not read 'restricted_file.txt' or could not write to 'restricted_file_modified.txt'.
Check file/folder permissions.

##Code Explanation

process_file(input_filename) Function
Encapsulates the core logic.
Takes the input filename as an argument.
Determines the output filename automatically.
Uses a try...except block to handle file operations and catch potential errors (FileNotFoundError, PermissionError, IOError, general Exception).
Uses with open(...) to ensure both input and output files are properly closed, even if errors occur.
Iterates through the input file line by line.
Formats the modified line (adding the line number) and writes it to the output file.
Prints status messages (processing, success, or error details).
Main Execution Block (if __name__ == "__main__":)
Ensures the code runs only when the script is executed directly.
Prompts the user to enter the filename.
Calls the process_file function to perform the file processing and error handling.
