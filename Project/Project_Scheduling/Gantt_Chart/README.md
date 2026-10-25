# Gantt Chart

The activities below are the same as in the [WBS](../WBS.md). Days are counted from the project start (day 0), and each task starts at its Earliest Start.

![Gantt Chart](Gantt_Chart.png)

## Schedule

| ID | Task | Duration | Start (end of day) | Finish (end of day) | Predecessors |
|---|---|---|---|---|---|
| T1 | Requirements Refinement | 3 | 0 | 3 | — |
| T2 | Database Design | 4 | 3 | 7 | T1 |
| T3 | User Interface Design | 4 | 3 | 7 | T1 |
| T4 | User Management Implementation | 5 | 7 | 12 | T2, T3 |
| T5 | Space Search and Selection Implementation | 6 | 7 | 13 | T2, T3 |
| T6 | Booking Management Implementation | 7 | 13 | 20 | T4, T5 |
| T7 | Availability and Notifications Implementation | 5 | 20 | 25 | T6 |
| T8 | Administration Implementation | 6 | 20 | 26 | T4, T5, T6 |
| T9 | System Integration | 4 | 26 | 30 | T7, T8 |
| T10 | System Testing and Bug Fixing | 6 | 30 | 36 | T9 |
| T11 | Deployment Preparation and Final Documentation | 3 | 36 | 39 | T10 |

**Overall project duration: 39 days.**

## Timeline view

```
      0    0    1    1    2    2    3    3    
      0····5····0····5····0····5····0····5····
T1    ███
T2       ████
T3       ████
T4           ░░░░░
T5           ██████
T6                 ███████
T7                        ░░░░░
T8                        ██████
T9                              ████
T10                                 ██████
T11                                       ███
```
█ critical task   ░ non-critical task (1 day of slack)
