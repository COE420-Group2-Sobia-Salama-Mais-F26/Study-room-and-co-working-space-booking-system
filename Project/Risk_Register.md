## Exercise 3: Project Risks and Risk Management *Mais Abudaqqa g00099729*

Identify potential risks that may affect your software project.

For each identified risk, provide the following information:

| Risk ID | Risk Description                                                                                                                                                                                                                                                                                | Possible Cause                                                                                                               | Probability | Impact | Mitigation/Response Strategy                                                                                                                                                                                                                                                                                                         |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|-------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| R1      | Requirements may change during the project.                                                                                                                                                                                                                                                     | Features may need to be added or modified as the platform is developed.                                                      | Medium      | Medium | Discuss requirements early and agree on the main features before development.                                                                                                                                                                                                                                                        |
| R2      | The project may not be completed on time.                                                                                                                                                                                                                                                       | Some tasks may take longer than expected or team members may fall behind.                                                    | Medium      | High   | Divide the project into smaller tasks, set deadlines, and regularly monitor progress.                                                                                                                                                                                                                                                |
| R3      | Communication problems may occur between team members.                                                                                                                                                                                                                                          | Team members may misunderstand tasks or fail to communicate progress.                                                        | Medium      | Medium | Hold regular meetings and use a shared platform to track tasks and updates.                                                                                                                                                                                                                                                          |
| R4      | User or booking data could be exposed or lost.                                                                                                                                                                                                                                                  | Weak passwords, database security problems, or incorrect handling of user information.                                       | Low         | High   | Use secure authentication, protect the database, validate user input, and maintain backups.                                                                                                                                                                                                                                          |
| R5      | The DeskOS API integration may fail or return errors, so the platform cannot show spaces or make bookings. | DeskOS is down, the login token (lasts for 1 hour only) expires, the request limit is reached, or the operator has not joined DeskOS. | Medium      | High   | Test early on the DeskOS staging server. Save space data, get a new token when it expires, wait and retry when the request limit is reached, and check the booking status if a callback is missed. |

R2 and R5 combine a medium probability with a high impact, so they are the highest-priority risks. R4 is unlikely but would have a high impact, so it is still addressed from the start.

Your team should identify **at least five potential risks** related to the project.

Possible areas to consider include:

- Changing or unclear requirements

- Technical difficulties

- Lack of required skills

- Team member availability

- Schedule delays

- Integration problems

- Resource limitations

- Communication problems

- Security or privacy concerns

- Stakeholder or customer availability

For each risk, assess its potential probability and impact, and describe how the team will attempt to mitigate or respond to it.
