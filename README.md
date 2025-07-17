# Previous_Step_Test
Checks if previous PCBA's test was performed in correct order. 
This VI is made in reusable way. Only by changing .ini file we can change how this VI behaves.


.INI file
<img width="477" height="697" alt="image" src="https://github.com/user-attachments/assets/896a26ee-4cfa-4761-9cd7-9d1162c9a51d" />

Enabled - 0 not revelant (ignored) / 1 revelant.

Path - path to file where logs are.

Search - Some data before SN of our product.




User Interface 
<img width="587" height="470" alt="image" src="https://github.com/user-attachments/assets/0048c499-fcd9-4abb-b78f-d9dc9f28c36d" />

Block Diagram:
.INI file handling
<img width="992" height="550" alt="image" src="https://github.com/user-attachments/assets/663c63ed-4ca5-4954-a5af-157a994f009a" />

Here we open ini file where all instructions are specified also files coresponding to each step is assiged to 2D array. By using this approach we can easily make changes between steps with use of one VI. 

Files sorting
<img width="1873" height="800" alt="image" src="https://github.com/user-attachments/assets/40ae6a0f-16d7-4f0b-83c1-f7c85f904e5d" />

In this part all files are sorted based on their creation date and latest log is checked to check wheather its passed. In last loop all results are gathered to display boolean array indicating which step is missing followed by message showing which log is missing. All that is displayed in single result indicating pass/fail.

