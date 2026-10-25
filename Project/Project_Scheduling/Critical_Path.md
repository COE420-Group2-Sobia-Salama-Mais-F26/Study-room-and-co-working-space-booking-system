# Exercise 7: Critical Path

**Critical Path:**

- Path 1: T1 → T2 → T5 → T6 → T8 → T9 → T10 → T11
- Path 2: T1 → T3 → T5 → T6 → T8 → T9 → T10 → T11

**Activities on the Critical Path:**

Requirements Refinement (T1), Database Design (T2), User Interface Design (T3), Space Search and Selection Implementation (T5), Booking Management Implementation (T6), Administration Implementation (T8), System Integration (T9), System Testing and Bug Fixing (T10), Deployment Preparation and Final Documentation (T11).

**Expected Project Duration:**

3 + 4 + 6 + 7 + 6 + 4 + 6 + 3 = 39 days

(Both paths give 39 days, because T2 and T3 both take 4 days.)

**Explanation:**

We did a forward pass to get ES and EF for each task, and a backward pass from the project end (day 39) to get LS and LF. Slack was then calculated as LS − ES. Every activity on the two paths above has a slack of 0, so delaying any of them by even one day would delay the whole project.

T2 and T3 both take 4 days and both must finish before T5 can start. Neither can be delayed, which is why there are two critical paths instead of one.

T4 (User Management Implementation) and T7 (Availability and Notifications Implementation) are not on the critical path because each has 1 day of slack:

- T4 finishes on day 12, but T6 can’t start until T5 finishes on day 13.
- T7 finishes on day 25, but T9 can’t start until T8 finishes on day 26.
