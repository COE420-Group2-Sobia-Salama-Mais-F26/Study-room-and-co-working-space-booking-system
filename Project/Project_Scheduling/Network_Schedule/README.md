# Exercise 6: Network-Based Scheduling

![Network Diagram](Network_Diagram.png)

## Calculations

Forward pass: ES = largest EF of the predecessors, EF = ES + E.
Backward pass: LF = smallest LS of the successors, LS = LF − E.
Slack = LS − ES.

| Task | E | ES | EF | LS | LF | Slack |
|---|---|---|---|---|---|---|
| T1 | 3 | 0 | 3 | 0 | 3 | 0 |
| T2 | 4 | 3 | 7 | 3 | 7 | 0 |
| T3 | 4 | 3 | 7 | 3 | 7 | 0 |
| T4 | 5 | 7 | 12 | 8 | 13 | 1 |
| T5 | 6 | 7 | 13 | 7 | 13 | 0 |
| T6 | 7 | 13 | 20 | 13 | 20 | 0 |
| T7 | 5 | 20 | 25 | 21 | 26 | 1 |
| T8 | 6 | 20 | 26 | 20 | 26 | 0 |
| T9 | 4 | 26 | 30 | 26 | 30 | 0 |
| T10 | 6 | 30 | 36 | 30 | 36 | 0 |
| T11 | 3 | 36 | 39 | 36 | 39 | 0 |
