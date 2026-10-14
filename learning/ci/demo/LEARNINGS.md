\# CI Inventory Validation Lab — Learning Report



\## Objective



The objective of this lab was to learn how to validate JSON inventory data using Python and understand how exit codes help automated tools identify success or failure.



\## Implementation



I implemented validation rules in the `validate\_inventory` function to check that:



\- The inventory is a JSON list.

\- Each server is a JSON object.

\- Every server has a `name` field.

\- The name is a string containing at least one non-whitespace character.

\- Server names are unique.



The function collects validation errors and returns them as a list. File reading and output handling remain separate from the validation logic.



\## Additional Rule



I implemented a duplicate-name rule using a Python set called `seen\_names`. If a server name appears more than once, the program reports the duplicate and identifies the server containing it.



\## Testing



The tests performed include:



\- Valid inventory.

\- Invalid inventory with a missing or invalid name.

\- Malformed JSON.

\- Missing file.

\- Duplicate server names.



The invalid inventory test returned exit code 1. The malformed JSON test also returned a nonzero exit code. The duplicate-name test correctly reported `server 3: duplicate server name 'web-01'` and returned exit code 1.



The valid inventory is expected to return exit code 0.



\## What I Learned



I learned how to validate JSON data using Python, check data types, reject empty or whitespace-only strings, and detect duplicate values using a set.



I also learned that validation logic should be separated from file reading and output handling to make code easier to test and maintain.



Exit codes are important in Continuous Integration (CI) pipelines because automated tools use them to determine whether a command succeeded or failed.



\## Conclusion



This lab demonstrated how input validation helps prevent invalid infrastructure inventory data from progressing through an automated workflow. It also provided practical experience with error handling, testing, and exit codes in preparation for CI automation.

