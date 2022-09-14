# ***Election Analysis with Python***

## **Project Overview:**

### Overview:

A Colorado Board of Elections employee gave us the task to analyze and report back the election audit results to the local congressional election. They facilitated us a csv file that contains the turnout of the votes obtained from mail-in ballots, punch cards, and DRE counting machines. In this report, we are expected to do the following and report back our results:

- Calculate the total number of votes cast.
- Get a commplete list of candidates who recieved votes.
- Calculate the total number of votes each candidate recieved.
- Calculate the percentage of votes each candidate won.
- Determine the winner of the election based on populat vote.
- Calculate the voter turnout of each county.
- Calculate the percentag of votes from each county out of the total count.
- Determine the county with the highest turnout.

### Purpose:

We are instructed to use Python to expedite our report and save our findings to a txt file titled election_analysis. In this file, we will report the following in this order:
- The total amount of votes for the election
- A list of the counties with its percentage of votes and its total amount of votes
- The name of the county with the largest county turn over
- A list of the candidates with its percentage of votes followed by its total amount of votes
- A short summary of the winner candidate followed by it's percentage and total amout of votes.

## **Resources:**

We are using the following resources to complete our analysis:

- Data source: election_results.csv
- Software: Python *3.6.1* , Visual Studio Code

## **Summary and Results**

### Election-Audit Results:
The analysis of the election votes show the following results:

 - There were *369,711* total votes cast in the election.
  
  - The data for each county:
    - Jefferson with 10.5% of the vote and *38,855* votes in total
    - Denver with 82.8% of the vote and *306,055* votes in total
    - Arapahoe with 6.7% of the vote and *24,801* votes in total
    
  - The county with the largest turn over was Denver 
  
  - The Candidates were:
      - Charles Casper Stockham
      - Diana DeGette
      - Raymon Anthony Doane
      
  - The results for each candidate were as follow:
      - Charles Casper Stockham recieved 23.0% of the vote and *85,213* votes in total
      - Diana DeGette recieved 73.8% of the vote and *272,892* votes in total
      - Raymon Anthony Doane recieved 3.1% of the vote and *11,606* votes in total
      
  - The winner of the election with an overwhelming support was:
      - Diana DeGette, who recieved 73.8% of the vote and *272,892* votes in total
    
    These results were saved in the election_analysis.txt file as follow:
    
    ![Results](https://user-images.githubusercontent.com/111034667/190249791-be46c7cc-6339-40ff-8e90-b36e566762ea.png)
    
### Election-Audit Summary:

The code created to return these results can be reused for future elections. There are small changes that need to be done to our code in order to reuse it for future elections and they are as follow:

At the beginning of our code, we declare these two variables to open our data file and open our txt file where we will record our results:
```
# Assign a variable to load a file from a path.
file_to_load = os.path.join("Resources", "election_results.csv")
# Assign a variable to save the file to a path.
file_to_save = os.path.join("analysis", "election_analysis.txt")
```
For future elections,when we declare the variable file_to_load and file_to_save, it will be necessary to change the os.path.join() expressions to match our new folders. We will have to change the expression inside our () to match the new folder (in this case Resources is our folder), the new csv file(which is in our Resources folder), and the new txt file (which is in our newly created folder "analysis").

For example, if our new files are in a folder 'Results', our csv file is called 'election_2022_results.csv',our new folder to hold our txt file is 'results2022' and our txt file is '2022_results', we can modify our code to be the following:
```
# Assign a variable to load a file from a path.
file_to_load = os.path.join("Results", "election_2022_results.csv")
# Assign a variable to save the file to a path.
file_to_save = os.path.join("results2022", "2022_results.txt")
```
This code will work as long as our folders are within the same folder. If we have our Python file outside of the folder containing all of our resources, then it would be neccesary to do the following changes:

```
# Assign a variable to load a file from a path.
file_to_load = os.path.join("..","Results", "election_2022_results.csv")
# Assign a variable to save the file to a path.
file_to_save = os.path.join("results2022", "2022_results.txt")
```
By adding "..", before the name of our folder, we are able to locate the folders and open them without a problem.
