In the context of Linux [[shell|shells]], there are concepts of *interactive* and *login*:

| *Concept*                     | *Meaning*                                                                             |
| ----------------------------- | ------------------------------------------------------------------------------------- |
| Interactive / Non-interactive | refers to the interaction between the user and the shell                              |
| Login / Non-login             | Refers to the event of a user providing credentials,<br>such as username and password |

Both interactive and non-interactive shells can be either login or non-login and any combination of these types has its own use-cases.

## Interactive login shells

- Executed when user log into the system
- Dedicated for setting up user's environment

## Interactive non-login shells

- Opened by the user after logging into the system

## Non-interactive shells

- Don't require any kind of human interaction
- Use in automated scripts

![[shell-startup.png]]