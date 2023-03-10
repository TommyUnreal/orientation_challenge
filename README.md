# The Orientation Challenge
An assessment of your skills and knowledge related to a job in SW tool automation. The purpose is to give you an idea of what to expect in the role and to give us and idea how you might perform under certain circumstances.

## Challenge Details
- The assignment is to create a simple (Python, batch) script with that will automate the user process up to generating an output in a human-readable format (a CSV table).
- The repository contains two executable files, as well as documentation for both, and user explanation for the process to be automated.
- The first script, **data_downloader.exe**, simulates the data download. It will produce files in a preset folder in accordance with the settings.
- The second script, **image_cruncher.exe**, analyzes the input data (counts the quantity of pixels in a particular color) and returns the outcomes to cmd or in json format.
- If any command line arguments in your script are required, you should clearly explain how to run your script in the instructions. You should also give a brief explanation of your code and any design choices you made.
  
## What User Does Manually
- I begin by downloading data with data_downloader. The customer specifies what dataID I need to process. The data must be uncompressed.
In the Spreadsheet editor, I create a new file. I create 5 columns: `Filename`, `Red`, `Green`, `Blue`, and `Other`.
- Using image_cruncher I run `image_cruncher.exe -i <path_to_image> -rgbo` to get analysis of each file. Then I copy the results from the screen to the table.
- When all files are ready (25 rows are filled in), I used the build in function to calculate the total averages of each column (for column B it will be `=(SUM(B2:B26)/SUM(B2:E26))*100)` and format the cell as a percentage).
- Save the file as CVS. I usually name it `<dataID>_analysis.csv`. This is the result and it is ready to be sent to the customer. Here is an example:

![335459513](https://user-images.githubusercontent.com/45427816/224297997-d65428b1-a0ad-43b3-896c-8a92ce050a87.png)
- Do you have any questions about my process? 
