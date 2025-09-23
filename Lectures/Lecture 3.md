# UC1: Get Movie Tickets
1. **User selects the movie**  
    This step is important because the user needs to choose which movie they want to watch. Without this choice the system cannot proceed to book tickets.

2. **User selects the number of persons**  
    Here the user tells the system how many people will attend. This is necessary so the system can reserve the correct number of seats.

3. **User selects date and time**  
    The user must pick when they want to see the movie. This ensures the tickets are for the right showtime.

4. **User selects the seats**  
    Choosing seats lets the user pick where they want to sit. This step is included because seat availability can vary and users often want specific seats.

5. **The system checks for errors and displays the selection**  
    This step is needed to make sure the user’s choices are valid. For example the seats might already be taken or the number of tickets might be too many. Showing the selection lets the user confirm everything is correct before payment.

6. **User completes payment and gets the ticket**  
    Finally the user pays for the tickets and receives confirmation. This step completes the process and allows the user to enter the cinema.


![[Actor Examples.png | center | 600]]
# Types of Actors
![[Types of Actors.png | center | 600]]

## Primary Actor
The primary actor initiates the use-case and the goals of this actor are met by the execution of the use case.

The primary actor in [[#UC1 Get Movie Tickets]] would be the User.

## Secondary Actor
The secondary actor supports the execution of the use case by providing services or resources needed by the primary actor. The goals of the secondary actor are not the main focus of the use case but their involvement is necessary for the use case to succeed.

Secondary actors in [[#UC1 Get Movie Tickets]]:
- Payment System
- Database for Movies

## Offstage Actor
The offstage actor influences the use case but does not directly interact with the system during its execution. The goals of the offstage actor may be affected by the use case but this actor remains outside the immediate flow of actions.

Offstage Actors in [[#UC1 Get Movie Tickets]]:
- Cinema Management Staff
- Marketing Team

# Relationships for Actors
![[Relationships for Actors.png | center | 600]]
## Association
Association represents a connection or link between two actors or between an actor and a use case. It shows that the actors communicate or interact in some way during the execution of the use case. This relation is important because it clarifies who participates in the use case and how they are involved.

For example in [UC1 Get Movie Tickets](app://obsidian.md/index.html#UC1%20Get%20Movie%20Tickets), the User has an association with the use case because they perform actions like selecting movies and making payments. The Payment System also has an association because it processes the payment when the user completes the purchase.

![[Association.png | center | 600]]

## Multiplicity
The picture shows a User connected to a use case called "Play Game" by a line. At the User end of the line there is a multiplicity of `2..*` and at the Play Game end there is a `1`. This means that each instance of the Play Game use case involves two or more Users participating together. In other words the game requires at least two users to play. On the other hand each User can be associated with one instance of the Play Game at a time. This example illustrates how multiplicity specifies the number of actors and use case instances that can be linked in a relationship.

![[Multiplicity.png | center | 600]]
(NOTE: add table properly)
![[Mutliplicity-meanings.png | 400 | center]]

## Inheritance & Generalisation
Inheritance means one actor or class is based on another actor or class. The child actor inherits the properties and behaviours of the parent actor. This is useful because it avoids repeating the same information many times. The child can also have extra features that make it different from the parent.

In software design inheritance helps to organise and simplify the system. For example a "Registered User" inherits from a general "User" and gets all the basic user features automatically. The "Registered User" can then add things like login details or preferences.

In UML inheritance is shown as a line with a hollow arrow pointing from the child to the parent. This shows the direction of inheritance.

A inherits from B: $B \Rightarrow A$

![[Inheritance.png | center | 600]]

### Generalisation
Generalisation is the process of finding common features or behaviours among several actors or classes and creating a more general actor or class that represents them all. It helps to simplify the model by grouping shared characteristics in one place.

In UML generalisation is shown as a line with a hollow arrow pointing from the more specific actors or classes to the more general one. This shows that the specific actors inherit from the general actor.

![[Generalisation.png | 400 | center]]


## Include relationship
An include relationship shows that one use case always uses the behaviour of another use case as part of its process. It means the included use case is a required step that happens every time the main use case runs. This helps to avoid repeating common actions in multiple use cases by putting them in a separate included use case.

![[Include Relationship.png | center | 600]]

The diagram shows two use cases: `Create User` and `CheckUserExists.` There is an arrow from `Create User` pointing to `CheckUserExists` labeled with `<<include>>`. This means that whenever the `Create User` use case runs, it always includes the behaviour of the `CheckUserExists` use case as a required step.

Before a user can be created, the system must check if the user already exists. This check is a common and necessary action that is separated into its own use case to avoid repeating it in multiple places.

The `<<include>>` relationship clarifies that `CheckUserExists` is not optional but always part of `Create User,` helping to keep the model clear and modular by reusing common functionality.

### Diagram with multiple use cases
![[Include Relationship 2.png | center | 600]]

## Extend relationship
An extend relationship is used when one use case adds optional or conditional behaviour to another use case. The extending use case inserts its behaviour at specific extension points defined in the base use case. These extension points are places in the base use case where extra behaviour can be added if certain conditions are met.

In UML the arrow points from the extending use case to the base use case and is labeled with `<<extend>>`.

![[Extend Relationship.png | center | 600]]

The diagram shows two use cases: `SignIn` and `AuthenticationError.` The `SignIn` use case is represented by a circle on the left with its name at the top. Inside the `SignIn` circle, there is a section labeled `extension points` with a specific extension point called `authenticationError.`

There is a dotted arrow labeled `<<extend>>` pointing from the `AuthenticationError` use case to the `SignIn` use case. This indicates that `AuthenticationError` is an extending use case that adds optional or conditional behaviour to `SignIn.`

The extension point `authenticationError` inside `SignIn` marks where the behaviour of `AuthenticationError` can be inserted if an authentication error occurs during the sign-in process. This means that normally the `SignIn` use case runs on its own, but if there is an authentication failure, the system extends the process by executing the `AuthenticationError` use case at that specific point.

This diagram illustrates how extend relationships allow optional or exceptional behaviour to be modularly added to a base use case without cluttering its main flow.

### Differences between `<<include>>` and `<<extend>>`

![[Include Extend Example.png | center | 600]]


| `<<include>>`                  | `<<extend>>`                               |
| ------------------------------ | ------------------------------------------ |
| B is required by A (Mandatory) | Y adds extra functionality to X (Optional) |

## Inheritance or Generalisation
Common behavior that is shared by multiple use cases can be extracted into a general or abstract use case. This general use case captures the common steps or functionality so it does not have to be repeated in each specific use case. The more specific use cases then inherit from this general use case, gaining its behavior automatically.

In UML this relationship is shown using an inheritance arrow (a solid line with a hollow arrowhead) pointing from the more specific use case (child) to the more general use case (parent). This arrow indicates that the child use case inherits the behavior of the parent use case.

![[Inheritance or Generalisation.png | center | 600]]

# Flows in a use case
![[Flows in a Use Case.png | center | 600]]
## Main flow
The main flow describes the typical sequence of steps that occur when the use case is executed successfully without any errors or exceptions (happy path / success scenario). It represents the standard or most common path that the user and system follow to achieve the primary goal of the use case. Documenting the main flow helps to clearly understand the core behaviour and expected interactions in the system.

## Alternative flow
The alternative flow describes the different paths the use case can take when things do not go as planned or when exceptions occur. These flows handle errors, special conditions, or optional behaviours that deviate from the main flow. Documenting alternative flows helps to capture how the system responds to unexpected situations and ensures robustness by covering all possible scenarios.