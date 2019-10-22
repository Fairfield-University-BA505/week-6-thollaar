# Part 2: Dictionaries
## Theory: You should know ...
* How dictionaries are used for structured records
* How file operations work in Python

## Practice: You be able to ...
* Store and retrieve data from a dictionary
* Write a CSV file

## Instructions
1. __Open the `HealthStatsPart2.ipynb` file in Jupyter.__ The file already has the corrected Python code from the last class.
Answer Tony: done
2. __Scroll down to the cell that starts with `# Goal: Scrub and convert the data`__ This cell uses a list for each row of the table. In practice we would not do it that way. It's too easy to mess up the column indexes when trying to interpret each row. Is the `Waist` in column 1 or column 2?
Answer Tony: Column 2, because the w2h_data.csv shows the data and when printing 'print(raw_rows)' you can see the 2nd element in the list is the 'Waist'
3. __Modify the cell so that each row is stored as a dictionary instead of a list.__ The keys should be 'ID','Waist','Hip', and 'Gender'. the rows variable should have a list of dictionaries instead of list of lists.
Answer Tony (see code below): 
    row_dict = dict(zip(keys, row)) #code Tony: create a new dictionary with name 'row_dict' and the list 'keys' is for the keys, 'row' for the values
    rows.append(row_dict)           #code Tony: within the loop add each row to the previous rows iterated through from the loop
4. __In the next cell, modify the code so that it uses your the new dictionaries (instead of lists).__ You will need to know how to add the two new (key,value) pairs to each dictionary.
done (see file for code)
5. __Modify the last cell to use dictionaries instead of lists.__ You saw this coming, right?
used my list of dictionaries: 'list_all' in the code
6. __Now for a real challenge: Use Python to write the HTML table to a file called `StatsResults.html`.__ If you did this correctly, you should be able to open the file in a web browser and see the HTML table without Jupyter.
created 'StatsResults.html' in my Jupyter Notebook and can be viewed by right-clicking on the file and selecting: 'Open in New Browser Tab'
