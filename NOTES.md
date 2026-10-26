# NOTES: Three Layers

Your name: TODO

Fill each TODO. Write plain, short sentences. Do not delete the headings.

## Part 1. Predict, then find [S1]

Write your prediction before you open any code. Then search. In the last column, write each file the search finds and what that file does.

| Action | Search word | My prediction (file) | Files found and what each does |
|---|---|---|---|
| Prints "Not yet. Try again." | `Not yet` | app.py | app.py prints the line out upon an incorrect answer |
| Decides that the second miss shows the answer | `reveal` | check.py | logic.py reveals answer when tries is greater than or equal to the max attempts |
| Saves one attempt | `save_attempt` | store.py | store.py saves one attempt using specific parameters (i.e. session id, attempts, etc.) |
| Refuses the 11th problem | `SetFull` | test_bank.py | bank.py refuses the 11th problem, since it is not in the self.members list |

Search command: `grep -rn "SEARCH WORD" --include=*.py .`

## Part 2. What the program remembered [S1]

After the restart, what did the program remember? The program remembered the last step that I was on.

Which file made that possible? dataman_store.json

## Part 3. The interface change [S1]

What did you change in `app.py`? I changed "Not Yet. Try Again." to read "EEE -- Try Again"

Why did no test need to change? The test is not looking for UI behavior.

## Part 4. The rule in the real library [S2]

The same 10-problem rule exists in the real library. Write the file and the function name. logic.py, class SetFull

## Part 5. The red test [S2]

With the rule removed from the library, what did the screen show? Showed the line: Failed: DID NOT RAISE <class 'dataman.logic.SetFull'>

With the rule removed, which test failed? test_eleventh_problem_is_refused

## Part 6. The data swap [S2]

A real database would replace which file? dataman_store.json

Which file holds the rules and does not change when the database changes? logic.py

## Reflection [S2]

In the logic layer of the program, I made it so the program properly checked when the Memory Bank problems were above 11, and that it would properly raise SetFull when it needed to. This change only effected the logic layer, so the data and interface layers were unaffected. I also made sure that it passed the associated pytest.

## Beta feedback (optional)

This bonus is a beta test. Which step took longer than its time? What confused you? Write it here. Your answer helps the next class.
