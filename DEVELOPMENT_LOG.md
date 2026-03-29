# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

### Entry 1 - March 25, 2026, 3:30 PM
What I did:
Initial project setup

Details:
- Forked the repository to my GitHub account
- Cloned the project locally
- Explored the structure of Process and SchedulerSimulation classes

Challenges:
At first, I was confused about how the scheduling logic works

Solution:
I read through the code carefully and followed the execution flow step by step

Time spent: 1 hour

---

### Entry 2 - March 26, 2026, 6:00 PM
What I did:
Understanding the simulation behavior

Details:
- Ran the program multiple times
- Observed how processes move in the ready queue
- Focused on understanding Round-Robin scheduling

Challenges:
Understanding how processes return back to the queue after execution

Solution:
Tracked the output line by line and connected it to the code

Time spent: 1.5 hours

---

### Entry 3 - March 28, 2026, 5:30 PM
What I did:
Set student ID and updated code

Details:
- Updated student ID to 445052093
- Re-ran the program and verified output changes
- Committed changes to GitHub

Challenges:
Ensuring the random output is consistent with my ID

Solution:
Tested the program multiple times

Time spent: 1 hour

---

### Entry 4 - March 29, 2026, 7:00 PM
What I did:
Implemented Feature 1 and Feature 2

Details:
- Added priority attribute to processes
- Displayed priority in output
- Implemented context switch counter

Challenges:
Finding the correct place to increment context switches

Solution:
Placed it inside the scheduling loop and tested output

Time spent: 2 hours

---

### Entry 5 - March 29, 2026, 9:30 PM
What I did:
Implemented Feature 3 (Waiting Time)

Details:
- Added waiting time calculation
- Updated creationTime correctly
- Printed summary at the end

Challenges:
Placing the waiting time calculation correctly in run()

Solution:
Moved the calculation to the beginning of run() and tested results

Time spent: 2 hours

---

## Summary

**Total time spent on assignment**: [ 7.5 hours]

**Most challenging part**:Correctly implementing waiting time without compromising execution 

**Most interesting learning**: Knowing how CPU scheduling functions for threads

**What I would do differently next time**: Prior to integrating features, start early and test each one independently.
