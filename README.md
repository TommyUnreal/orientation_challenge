# The Orientation Challenge
An assessment of your skills and knowledge related to a job in SW tool automation. The purpose is to give you an idea of what to expect in the role and how you might perform under certain circumstances.

## What User Does Manually
I begin by downloading data with data_downloader. The customer specifies what dataID I need to process. The data must be uncompressed.
In the Spreadsheet editor, I create a new file called <data_ID>_analysis. I create 5 columns: file_name, red, green, blue, and other.
- Using image_cruncher I run `image_cruncher.exe -i <path_to_image> -rgbo` to get analysis of each file. Then I copy the results from the screen to the table.
- When all files are ready (25 rows are filled in), I used the build in function to calculate the total averages of each column (for column B it will be `=(SUM(B2:B26)/SUM(B2:E26))*100)` and format as a percentage).
- Save the file as CVS. The result is ready to be sent to the customer.
- Any questions? 

## Challenge Details
- The assignment is to create a simple (Python) script with that will execute both scripts, collect the output from the second script, and perform simple operations, that are outputted into a human-readable format (a CSV table).
- Two executable files, as well as documentation for both scripts (both are in this repository), and user explanation for the process to be automated are given to the interviewee.
- Data downloader.exe, the first script, simulates the data download. It will produce files in a preset folder in accordance with the settings
- The second script (image cruncher.exe) manipulates the input data (counts the quantity of pixels in a particular color) and outputs the outcomes to cmd or in json format.
- The candidate should create a (Python) script that runs both programs, combines the output from the second script with the results of the first script, and compute total percentages of red, green, and blue pixels.
- If any command line arguments are required, the interviewee should clearly explain how to run their script in the instructions. The interviewee should also give a brief explanation of their code and any design choices they made.
