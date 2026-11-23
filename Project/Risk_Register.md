# 2.3. Risk Analysis

The team identified five main risks that could affect the project. Table
2.2 describes each risk and its possible cause.

| **ID** | **Risk**                                                                                                   | **Possible Cause**                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| R1     | Requirements may change during the project.                                                                | Features may need to be added or modified as the platform is developed.                                                               |
| R2     | The project may not be completed on time.                                                                  | Some tasks may take longer than expected or team members may fall behind.                                                             |
| R3     | Communication problems may occur between team members.                                                     | Team members may misunderstand tasks or fail to communicate progress.                                                                 |
| R4     | User or booking data could be exposed or lost.                                                             | Weak passwords, database security problems, or incorrect handling of user information.                                                |
| R5     | The DeskOS API integration may fail or return errors, so the platform cannot show spaces or make bookings. | DeskOS is down, the login token (lasts for 1 hour only) expires, the request limit is reached, or the operator has not joined DeskOS. |

**Table 2.2** Identified project risks

### 2.3.1 Probability

Each risk was rated by how likely it is to occur during the project.

| **ID** | **Risk**                                               | **Probability** |
|--------|--------------------------------------------------------|-----------------|
| R1     | Requirements may change during the project.            | Medium          |
| R2     | The project may not be completed on time.              | Medium          |
| R3     | Communication problems may occur between team members. | Medium          |
| R4     | User or booking data could be exposed or lost.         | Low             |
| R5     | The DeskOS API integration may fail or return errors.  | Medium          |

**Table 2.3** Risk probability

### 2.3.2 Impact

Each risk was also rated by how seriously it would affect the project if
it occurred.

| **ID** | **Risk**                                               | **Impact** |
|--------|--------------------------------------------------------|------------|
| R1     | Requirements may change during the project.            | Medium     |
| R2     | The project may not be completed on time.              | High       |
| R3     | Communication problems may occur between team members. | Medium     |
| R4     | User or booking data could be exposed or lost.         | High       |
| R5     | The DeskOS API integration may fail or return errors.  | High       |

**Table 2.4** Risk impact

R2 and R5 combine a medium probability with a high impact, so they are
the highest-priority risks. R4 is unlikely but would have a high impact,
so it is still addressed from the start.

### 2.3.3 Mitigation

| **ID** | **Mitigation / Response Strategy**                                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R1     | Discuss requirements early and agree on the main features before development.                                                                                                                      |
| R2     | Divide the project into smaller tasks, set deadlines, and regularly monitor progress.                                                                                                              |
| R3     | Hold regular meetings and use a shared platform to track tasks and updates.                                                                                                                        |
| R4     | Use secure authentication, protect the database, validate user input, and maintain backups.                                                                                                        |
| R5     | Test early on the DeskOS staging server. Save space data, get a new token when it expires, wait and retry when the request limit is reached, and check the booking status if a callback is missed. |

**Table 2.5** Risk mitigation and response strategies
