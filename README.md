# Data Analysis: Simple Election Results

# Tuple of Tuples: (Candidate Name, Party, Votes)
# Tuples are used because this data is 'locked' once the election is over.
ELECTION_RESULTS = (
    ("Rohan Sharma", "Green", 1520),
    ("Priya Verma", "Blue", 2150),
    ("Amit Singh", "Red", 1880)
)

highest_votes = 0
winner_name = ""
winner_party = ""

print("--- Election Results Analysis ---")

# Loop through the tuple of results
for candidate_data in ELECTION_RESULTS:
    # Tuple Unpacking: Get the details from the current tuple
    name, party, votes = candidate_data
    
    print(f"Candidate: {name:<15} | Party: {party:<5} | Votes: {votes}")
    
    # Simple IF logic to track the candidate with the highest votes
    if votes > highest_votes:
        highest_votes = votes
        winner_name = name
        winner_party = party

print("---------------------------------")
print("\n--- Final Result ---")
print(f"🥇 The WINNER is: **{winner_name}** ({winner_party})")
print(f"Total Votes secured: {highest_votes}")
print("--------------------")
