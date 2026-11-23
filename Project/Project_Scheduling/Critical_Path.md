# Exercise 7: Critical Path

## Gantt Chart

The Gantt chart in Figure 3.1 uses the same activities, durations, and dependencies as the WBS. The project runs from Monday 5 October to Thursday 12 November 2026 (39 days). Red bars are critical activities, and blue bars (T4 and T7) have one day of slack.

Gantt chart: [Gantt_Chart.png](Gantt_Chart/Gantt_Chart.png)

## Network Diagram and Critical Path

The task-on-node network diagram in Figure 3.2 shows each activity's expected time (E), earliest start and finish (ES, EF), latest start and finish (LS, LF), and slack. The critical path is highlighted in red.

Network diagram: [Network_Diagram.png](Network_Schedule/Network_Diagram.png)

A forward pass gave the ES and EF of each activity (ES = largest EF of the predecessors, EF = ES + E), and a backward pass from day 39 gave the LS and LF (LF = smallest LS of the successors, LS = LF − E). Slack was calculated as LS − ES. The resulting values are summarized in Table 3.2.

| **Task** | **Predecessor(s)** | **E** | **ES** | **EF** | **LS** | **LF** | **Slack** |
|----------|--------------------|-------|--------|--------|--------|--------|-----------|
| T1       | —                  | 3     | 0      | 3      | 0      | 3      | 0         |
| T2       | T1                 | 4     | 3      | 7      | 3      | 7      | 0         |
| T3       | T1                 | 4     | 3      | 7      | 3      | 7      | 0         |
| T4       | T2, T3             | 5     | 7      | 12     | 8      | 13     | 1         |
| T5       | T2, T3             | 6     | 7      | 13     | 7      | 13     | 0         |
| T6       | T4, T5             | 7     | 13     | 20     | 13     | 20     | 0         |
| T7       | T6                 | 5     | 20     | 25     | 21     | 26     | 1         |
| T8       | T4, T5, T6         | 6     | 20     | 26     | 20     | 26     | 0         |
| T9       | T7, T8             | 4     | 26     | 30     | 26     | 30     | 0         |
| T10      | T9                 | 6     | 30     | 36     | 30     | 36     | 0         |
| T11      | T10                | 3     | 36     | 39     | 36     | 39     | 0         |

**Table 3.2** Summary of scheduling values

**Critical Path:**

- Path 1: T1 → T2 → T5 → T6 → T8 → T9 → T10 → T11
- Path 2: T1 → T3 → T5 → T6 → T8 → T9 → T10 → T11

**Activities on the Critical Path:**

Requirements Refinement (T1), Database Design (T2), User Interface Design (T3), Space Search and Selection Implementation (T5), Booking Management Implementation (T6), Administration Implementation (T8), System Integration (T9), System Testing and Bug Fixing (T10), Deployment Preparation and Final Documentation (T11).

**Expected project duration:** 3 + 4 + 6 + 7 + 6 + 4 + 6 + 3 = 39 days. Both paths give 39 days because T2 and T3 both take 4 days.

**Explanation:** Every activity on the two paths has zero slack, so delaying any of them by even one day delays the whole project. There are two critical paths because T2 and T3 both take 4 days and must both finish before T5 can start. T4 (User Management Implementation) and T7 (Availability and Notification Implementation) are not critical because each has 1 day of slack: T4 finishes on day 12, but T6 cannot start until T5 finishes on day 13, and T7 finishes on day 25, but T9 cannot start until T8 finishes on day 26. The schedule was verified with a CPM spreadsheet in LibreOffice Calc, which gave the same 39-day duration and the same critical tasks.
