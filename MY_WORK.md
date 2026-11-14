📝 MY_WORK: Student Information, Development Log, Reflection & Answers
This is the only file your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be in your own words.

🛑 STOP: Read This Before You Do Anything Else
1️⃣ Read the whole README.md first
The README.md in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. If you skip it, you will lose marks.
2️⃣ Understand the full code before answering any question
Open SchedulerSimulationSync.java and read it from top to bottom. You must be able to explain what SharedStats, ReadyQueue, CpuWorker, RaceWindow.pause(), ReentrantLock and Semaphore do before you write a single answer in Parts B and C. Run the original starter first (it is intentionally broken) and save its output: you need it for Question 1 of Part C.
3️⃣ Use only the code of this repository
Work only on SchedulerSimulationSync.java from this repository. Do not copy or paste code from your previous assignments.
4️⃣ Commit many times, not once
A single commit, or all commits made in the last hour, costs you -0.5 mark. See the Commit Rules below.

How to use this file:
1. Fill in your Student Information (below) right now.
2. Follow the steps in the Work Roadmap in order.
3. Update the Development Log every time you work on the assignment, not at the end.
4. Do not delete any section header. Replace the [...] placeholders with your own text.
👤 Student Information
⚠️ WARNING: Fill this in first. Your name and ID must match the student ID you set in SchedulerSimulationSync.java (line 304) and the one you say in your video.

Field	Your Answer
Full Name	Anas saeed Alhijraf
Student ID	445050054
University Email	445050054@std.psau.edu.sa
GitHub Username	Anas05q
Repository Link	https://github.com/Anas05q/OS-Assignment3-Anas-Alhijraf


🎥 Video Link
Video Link: PENDING — add the accessible video link after uploading the recording
⚠️ WARNING: The video must be publicly accessible ("Anyone with the link can view") on Google Drive, YouTube (Unlisted or Public) or any other cloud file-sharing system. A private, restricted or broken link counts as a missing video (-1 mark).

💡 TIP: Open the link in a private/incognito window before you submit. If it asks you to log in or request access, it is not public.

📌 NOTE: The link goes in this file only (MY_WORK.md), not in README.md. Name your video file StudentID_Assignment3_Demo.mp4. It must last 2 to 3 minutes.

🗺️ Work Roadmap (follow in this order)
Step	What to do	Where	Marks
0	Read README.md, read the full code, run the original starter and save its output (it fails on purpose)	Your IDE	–
1	Fork, rename, keep the repo PUBLIC, set your student ID (line 304), commit	GitHub + code	Part 1 (1)
2	Feature 1: Mutex lock on the ready queue, commit	Code	Part 2 (0.25)
3	Feature 2: Mutex lock(s) on the shared statistics, commit	Code	Part 2 (0.25)
4	Feature 3: Counting semaphore instead of busy waiting, commit	Code	Part 2 (0.5)
5	Development Log (5+ entries, different dates)	This file, Part A	Part 3 (0.5)
6	Reflection (4 questions)	This file, Part B	Part 3 (0.5)
7	Technical Answers (4 questions)	This file, Part C	Part 3 (0.5)
8	Record the video, upload it, paste the link above	Video + this file	Part 4 (1.5)
9	Final check, then submit the repo link on Blackboard	Blackboard	–


💡 TIP: Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

🔁 Commit Rules (MANDATORY)
⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

Minimum: 4 meaningful commits. Aim for 7 or more.
#	Commit	Example message
1	Student ID set	Set my student ID: 441234567
2	Feature 1: Ready queue lock	Feature 1: Protected the ready queue with a ReentrantLock
3	Feature 2: Statistics locks	Feature 2: Added locks to the shared statistics counters
4	Feature 3: Semaphore	Feature 3: Replaced busy waiting with a counting semaphore
5	Development log entries	Docs: Added development log entries 1-3
6	Reflection and answers	Docs: Completed reflection and technical answers
7	Video link	Docs: Added demo video link


Rules:
- ✅ One commit per feature. Do not put all three features in one commit.
- ✅ Commit after each work session, and after each part of this file.
- ✅ Spread your commits over different dates. Not all in one day.
- ❌ Do not make all commits in the last hour before the deadline (November 14, 2026).
- ❌ No vague messages like done, update or final version.
💡 TIP: Your commit history is checked and you show it in your video (at least 4 commits visible). Your development log dates should match your commit dates.

💡 TIP: Use VS Code (see Recommended Development Environment in README.md for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. Pushing matters: commits that are not pushed to GitHub are invisible to the instructor.

Part A: Development Log (0.5 mark)
⚠️ WARNING: Minimum 5 entries, spread over different dates. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be between the start of the assignment and the deadline (November 14, 2026).

💡 TIP: Write an entry at the end of each work session, while you still remember what happened. It takes 5 minutes.

💡 TIP: Be specific. "Worked on the code" is a weak entry. "Added a ReentrantLock queueLock to ReadyQueue and wrapped the body of poll() in lock() / try / finally { unlock() }" is a strong one.

📌 NOTE: Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

Example Entry (do not copy it, write your own)
Entry 1 - [November 2, 2026, 4:30 PM]
What I did: Forked the repository, set my student ID, and ran the original starter

Details:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked P1, then IllegalThreadStateException and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: Set my student ID: 441234567
Challenges: I did not understand why the same process was picked by three CPUs

Solution: Read ReadyQueue.poll() again and found the RaceWindow.pause() between reading the head and removing it

Time spent: 45 minutes
Your Development Log
Entry 1 - November 14, 2026 (exact time not recorded)
What I did: Set up and reviewed the synchronization assignment.

Details: Worked with the Assignment 3 repository and configured student ID 445050054 as the random seed. Reviewed the shared ready queue, CPU workers, and verification requirements.

Challenges: The starter code contains multiple shared resources accessed by concurrent threads.

Solution: Identified queue operations, shared counters, and waiting behavior as the three areas requiring synchronization.

Time spent: Part of the approximately 5 hours spent on the assignment today; individual session duration was not recorded.
Entry 2 - November 14, 2026 (exact time not recorded)
What I did: Implemented ready-queue mutual exclusion (Feature 1).

Details: Used a ReentrantLock in ReadyQueue and protected add(), poll(), processOf(), and snapshot() with try/finally unlock blocks.

Challenges: Several CPU workers can access or modify the same linked list and map at the same time.

Solution: Protected the critical sections so only one worker manipulates queue state at a time.

Time spent: Part of the approximately 5 hours spent on the assignment today; individual session duration was not recorded.
Entry 3 - November 14, 2026 (exact time not recorded)
What I did: Protected shared statistics (Feature 2).

Details: Added one statsLock to protect the three counters and their accessor methods. Kept RaceWindow.pause() inside the protected updates.

Challenges: A read-modify-write update can lose increments when threads interleave.

Solution: Used the same mutex for each counter update and read, with finally ensuring unlock.

Time spent: Part of the approximately 5 hours spent on the assignment today; individual session duration was not recorded.
Entry 4 - November 14, 2026 (exact time not recorded)
What I did: Replaced busy waiting with a semaphore (Feature 3).

Details: Added a counting Semaphore(0) to the queue, released a permit when adding work, and acquired a permit before polling. Added wake-up permits for CPU shutdown.

Challenges: An earlier run still reported 13 busy-waiting polls, and the downloaded Java file initially had the wrong filename.

Solution: Corrected the Java filename, compiled again, and confirmed the busy-waiting counter reached zero.

Time spent: Part of the approximately 5 hours spent on the assignment today; individual session duration was not recorded.
Entry 5 - November 14, 2026 (exact time not recorded)
What I did: Verified and pushed the final implementation.

Details: Ran the completed program five consecutive times. Every run reported 29 context switches, 16 completed processes, 65024 ms total service time, and 0 busy-waiting polls. Committed the corrected implementation as b27e834 and verified the branch was up to date with origin/main.

Challenges: Needed to ensure the corrected file was the one compiled and committed.

Solution: Used javac, java, PowerShell output filtering, and git status to verify the results and repository state.

Time spent: Part of the approximately 5 hours spent on the assignment today; individual session duration was not recorded.
Entry 6 - Optional (not used)
No sixth work session recorded.
Development Log Summary
💡 TIP: Fill this in last, after all entries are written.

Total time spent on assignment: Approximately 5 hours on November 14, 2026

Most challenging part: Getting the semaphore-based queue to terminate correctly without busy waiting.

Most interesting learning: Locks protect critical sections, while a semaphore also lets workers sleep until work is available.

What I would do differently next time: Start earlier, keep the starter output, and document each work session immediately.
Part B: Reflection (0.5 mark)
🛑 STOP: Do not start this part until you have read the README.md, read the entire SchedulerSimulationSync.java, run it, and finished the three features.

⚠️ WARNING: Each answer must be 5 to 7 sentences, in your own words. Copied or AI-generated answers without understanding get 0 marks for the whole assignment. You may be asked to explain them in person.

💡 TIP: Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.

💡 TIP: Draft your answer in a few bullet points first, then turn them into sentences.

Question 1: What did you learn about synchronization?
💡 TIP: Talk about race conditions (read-modify-write), critical sections, mutual exclusion with ReentrantLock and try/finally, the role of a counting semaphore, and what surprised you when the starter failed.

Your Answer: (5-7 sentences)

I learned that synchronization is necessary when multiple CPU threads access the same data. The ready queue is a critical section because workers can remove and add processes concurrently. I used ReentrantLock to make those queue operations mutually exclusive. I also protected the shared statistics so increments would not overwrite one another. The try/finally pattern ensures a lock is released even if an operation fails. A semaphore serves a different purpose: it lets a CPU wait for available work instead of repeatedly checking an empty queue.
Question 2: What was the most challenging part of this assignment?
💡 TIP: Pick one specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say why it was hard.

Your Answer: (5-7 sentences)

The hardest part was removing busy waiting without leaving CPU threads blocked forever. At first, a test still showed 13 busy-waiting polls, so the third feature was not finished. I needed to understand how a semaphore permit corresponds to a queued process. I also had to consider what happens when all processes are completed and some CPU workers are waiting. A filename mismatch caused a separate compilation problem because Java could not find SchedulerSimulationSync.java. Fixing both problems took more careful checking than I expected.
Question 3: How did you overcome the challenges you faced?
💡 TIP: Describe your method: reading the slides and the documentation, adding System.out.println to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

Your Answer: (5-7 sentences)

I worked through the problems by checking the program output rather than assuming a commit meant the feature worked. I searched the Java file for the old busy-wait counter and the semaphore implementation. After correcting the filename, I compiled the program with javac and ran it again. I compared the four verification values with their expected results. I then ran the program five times to make sure the result was repeatable. Finally, I committed the corrected code and checked that Git reported a clean branch synchronized with origin/main.
Question 4: Where can synchronization concepts be applied in real-world applications?
💡 TIP: Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

Your Answer: (5-7 sentences)

Synchronization is useful in banking systems where two transactions must not update an account balance incorrectly. A lock can prevent two threads from changing the same balance at the same time. Ticket-booking systems need similar protection so the same seat is not sold twice. A semaphore can control access to a limited number of resources, such as database connections. In this assignment, the semaphore represented work available in the ready queue. These examples helped me see why correct coordination matters beyond a classroom simulation.
Optional: What would you like to learn more about?
Semaphore fairness and deadlock detection.
Optional: How confident do you feel about synchronization concepts now?
Intermediate: I understand mutexes and counting semaphores, but I need more practice with fairness and deadlock.
Optional: Feedback on the assignment
The assignment made thread synchronization more concrete through executable tests.
Part C: Technical Answers (0.5 mark)
🛑 STOP: You cannot answer these questions without understanding the code. Re-read SchedulerSimulationSync.java and run it first. Your answers must reference your own code and your own output (your student ID makes your output and your expected values unique).

⚠️ WARNING: Each answer must be 3 to 5 sentences, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.

💡 TIP: Keep the output of the original starter and the output of your final version in text files or screenshots, so you can copy real snippets for Question 1.

Question 1: Race Condition in Your Own Output
Question: Run the original starter (before any fix) and paste the verification block of that run. Which value was wrong (expected vs observed)? Explain step by step, with two named threads/CPUs, how one lost update happens on one of the shared variables (read, RaceWindow.pause(), write). Why can the same bug happen on a real machine even without RaceWindow, and why is it hard to detect?
⚠️ WARNING: The snippet must come from your own run (with your student ID), not from a classmate or from this README.

💡 TIP: Use a small timeline: CPU-1 reads contextSwitchCount = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost. If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

Your Answer: (3-5 sentences)

The original starter is designed to demonstrate a race condition, but I did not save its verification output before making the fixes. In an unprotected read-modify-write operation, CPU-1 and CPU-2 can read the same counter value and both write the same incremented result. This loses one update even though two operations took place. RaceWindow.pause() makes the interleaving easier to reproduce, but real thread scheduling can cause the same problem without it. My final version produced the correct verification values in five runs.

Verification block of the original starter:
PENDING: Original starter output was not saved. Do not substitute a fabricated result.

Verification block of my final version:
Context switches (quanta executed)     expected 29       observed 29
Completed processes                    expected 16       observed 16
Total service time (ms)                expected 65024    observed 65024
Busy-waiting polls (must be 0)         expected 0        observed 0

Explanation of the timeline: Example interleaving: CPU-1 reads contextSwitchCount = 12; CPU-2 also reads 12; CPU-1 writes 13; CPU-2 writes 13. The correct result after two increments is 14, but the actual result is 13. This is an illustration, not a captured starter trace.
Question 2: Critical Sections and Lock Granularity
Question: List the critical sections you protected (variables and methods) and the lock(s) you used. Lock granularity: did you use one lock for the three statistics or one lock per variable? Why, and what is the trade-off? Why is the ready queue protected by a different lock than the statistics? Explain how your solution provides mutual exclusion, and discuss progress and bounded waiting (a default ReentrantLock is not fair: what does that imply?).
💡 TIP: The three counters are independent: does updating contextSwitchCount need to block an update of totalServiceTime? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the same lock and a thread held it while doing something slow.

Your Answer: (3-5 sentences)

I protected ReadyQueue.add(), poll(), processOf(), and snapshot() with the queue lock, and protected all three SharedStats counters and their getters with statsLock. I chose one lock for the three statistics because it is simpler to reason about, although separate locks could allow more concurrency. The queue uses a different lock so its operations do not unnecessarily block statistics updates. These locks provide mutual exclusion and allow progress once the current holder releases the lock. Because the default ReentrantLock is non-fair, strict bounded waiting is not guaranteed.
Critical section (variable / method)	Lock used	Why it needs protection
ReadyQueue.add(), poll()	lock	Prevent concurrent queue mutations and duplicate removal
ReadyQueue.processOf(), snapshot()	lock	Protect shared map and list reads
SharedStats increments and getters	statsLock	Prevent lost updates and inconsistent counter reads


Question 3: Busy Waiting vs Semaphore
Question: Describe the busy waiting of the starter and its cost (give the Busy-waiting polls number from your starter run). What does the value of your semaphore represent? What is its initial value and why? What is its value right after the numProcesses initial add() calls? Why does the last CPU call release(totalCPUs) at the end, and what would happen if it did not?
💡 TIP: Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in acquire() when no process will ever be added again.

Your Answer: (3-5 sentences)

The starter repeatedly checked the queue and slept when it found no work; one earlier incomplete run of my modified code still recorded 13 busy-waiting polls, but I do not have the original starter count. My final queue uses a counting semaphore initialized to zero, representing permits for processes that have been added but not yet acquired. After the initial numProcesses calls to add() and before CPUs start acquiring, it has numProcesses permits. Each added process releases a permit, and a CPU acquires one before taking work. At completion, releasing totalCPUs wake-up permits prevents blocked workers from waiting forever after no more processes will arrive.
Question 4: Classical Problems and Deadlock
Question: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. Name it, and say who plays the producer and the consumer roles (careful: here the CPUs also re-enqueue processes). If the ready queue were bounded (capacity K), name the three semaphores you would need and their initial values. Describe a deadlock scenario that appears if a thread acquired the mutex before waiting on the semaphore (or if two locks were acquired in different orders), and say which of the four necessary conditions you would break to prevent it.
💡 TIP: Recall the bounded-buffer solution of the slides (empty, full, mutex) and the order of wait() calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

Your Answer: (3-5 sentences)

Classical problem and roles: Producer-consumer: the main thread adds initial processes; CPU workers consume and may re-enqueue unfinished processes.

Semaphores for a bounded queue (name and initial value): empty = K, full = 0, mutex = 1.

Deadlock scenario and prevention: Holding mutex while waiting for empty can block the consumer from freeing a slot; acquire empty before mutex to prevent circular waiting.
Summary
Key concepts I understood through these questions: 1. Mutual exclusion 2. Counting semaphores 3. Lost updates and deadlock prevention.

Concepts I need to study more: 1. Fairness and bounded waiting 2. More complex deadlock scenarios.
✅ Final Checklist (complete before submitting)
⚠️ WARNING: Go through every line. Blackboard does not accept submissions after the deadline, which is November 14, 2026.

Repository
- Repository is PUBLIC (Settings → Danger Zone → Visibility)
- Repository is renamed to OS-Assignment3-YourFirstName-YourLastName
- GitHub account uses the university email (std.psau.edu.sa)
Code
- Student ID is set in SchedulerSimulationSync.java (line 304)
- My code is based only on the starter of this repository (nothing copied from previous assignments)
- Code compiles and runs with no errors, and terminates by itself (no ⛔ WATCHDOG)
- Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- The four verification lines are ✔ in 5 consecutive runs
- Every lock is released in a finally block
- RaceWindow, Config, the verification block and the watchdog are unchanged
- Each feature has clear comments
Commits
- At least 4 meaningful commits, ideally 7 or more
- One commit per feature
- Commits are spread over different dates (not all in the last hour)
- Everything is pushed to GitHub
This file (MY_WORK.md)
- Full name and student ID filled in at the top
- Development log has 5+ entries on different dates
- Reflection: 4 questions, 5-7 sentences each
- Technical answers: 4 questions, 3-5 sentences each, with examples from your output (starter output and final output pasted in Question 1)
- No [...] placeholders left
- No section headers deleted
Video
- 2-3 minutes long, named StudentID_Assignment3_Demo.mp4
- Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- Link is public (tested in an incognito window) and pasted in the Video Link section above
Blackboard
- Submit only the link to your public GitHub repository
