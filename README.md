# Election_Analysis

## Project Overview
A Colorado Board of Elections employee has given you the following tasks to complete the audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Caclulate thetotal number of votes each candidate received.
4. Caclulate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.6.1, Visual Studio Code, 1.38.1

# Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election.
- The candidates were:
    - Diana DeGette
    - Charles Casper Stockham
    - Raymon Anthony Doane
- The candidate results were:
    - Diana DeGette: 73.8% (272,892)
    - Charles Casper Stockham: 23.0% (85,213)
    - Raymon Anthony Doane: 3.1% (11,606)
- The winner of the election was:
    - Diana DeGette, who received 73.8% of the vote with 272,892 votes.
## Challenge Overview
I used VS Code text editing software to write the code for Python because it can detect syntax errors, save written code and assist with formatting.  The biggest challenge of all was ipmlementing logical conditional loops within the code that behaved as expected.  Below is an example from the code of an 'if' statement nested within a 'for' loop, nested within a 'while' loop:
```
# Open the election results and read the file.
with open(file_to_load) as election_data:
    file_reader = csv.reader(election_data)
    # Read the header row.
    headers = next(file_reader)
    # Print each row in the CSV file.
    for row in file_reader:
        # Add to the total vote count.
        total_votes += 1
        # Get the candidate name from each row.
        candidate_name = row[2]
        # If the candidate does not match any existing candidate, add the
        # the candidate list.
        if candidate_name not in candidate_options:
            # Add the candidate name to the candidate list.
            candidate_options.append(candidate_name)
            # And begin tracking that candidate's voter count.
            candidate_votes[candidate_name] = 0
        # Add a vote to that candidate's count.
        candidate_votes[candidate_name] += 1
```
## Challenge Summary
As can be seen above, the code opens the source data file, in our case election_results.csv, and reads through each column of data row by row.  The code then checks which candidate received the vote, adding any unique candidate name to a list of candidates.  The total vote count is incremented by 1, and the appropriate candidate, likewise.  We can also verify that the data provided is clean and error-free.  We output the results of our analysis to a .txt file for backup.
