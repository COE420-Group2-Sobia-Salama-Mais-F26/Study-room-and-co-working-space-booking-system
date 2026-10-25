# Gantt Chart

The activities below are the same as in the [WBS](../WBS.md). The project starts on **Monday 5 October 2026** and finishes on **Thursday 12 November 2026** (39 days). Each task starts at its Earliest Start, and days are counted as calendar days.

![Gantt Chart](Gantt_Chart.png)

Red bars are critical tasks (no slack). Blue bars (T4 and T7) are non-critical and have 1 day of slack. Arrow colour shows the predecessor task.

## Schedule

| ID | Task | Duration (days) | Start | Finish | Predecessors | Slack |
|---|---|---|---|---|---|---|
| T1 | Requirements Refinement | 3 | Mon 5 Oct | Wed 7 Oct | — | 0 |
| T2 | Database Design | 4 | Thu 8 Oct | Sun 11 Oct | T1 | 0 |
| T3 | User Interface Design | 4 | Thu 8 Oct | Sun 11 Oct | T1 | 0 |
| T4 | User Management Implementation | 5 | Mon 12 Oct | Fri 16 Oct | T2, T3 | 1 |
| T5 | Space Search and Selection Implementation | 6 | Mon 12 Oct | Sat 17 Oct | T2, T3 | 0 |
| T6 | Booking Management Implementation | 7 | Sun 18 Oct | Sat 24 Oct | T4, T5 | 0 |
| T7 | Availability and Notification Implementation | 5 | Sun 25 Oct | Thu 29 Oct | T6 | 1 |
| T8 | Administration Implementation | 6 | Sun 25 Oct | Fri 30 Oct | T4, T5, T6 | 0 |
| T9 | System Integration | 4 | Sat 31 Oct | Tue 3 Nov | T7, T8 | 0 |
| T10 | System Testing and Bug Fixing | 6 | Wed 4 Nov | Mon 9 Nov | T9 | 0 |
| T11 | Deployment Preparation and Final Documentation | 3 | Tue 10 Nov | Thu 12 Nov | T10 | 0 |

**Overall project duration: 39 days.**
