The model view controller pattern is only useful if your system has a component of UI.

When using the MVC Pattern (Model View Controller Architecture Pattern) your UI should not directly interact with your system. There should be a kind of middleman (The Controller / Brain).
Conversely the system should not directly interact with the UI. All "communication" should flow through the Controller which as the diagram shows controls and decides how the data is displayed as well as modifies the data to normalise and clean it for usage on the system.

![[MVC Architecture Pattern.png | center | 600]]

In this diagram we have: User, View and Model. Following the Controller principle of GRASP we implement 2 Use Case Controllers ProcessSaleController and HandleReturnsController to process the sales and handle the returns. As seen on the diagram these formats and communicates the relevant information between the User, View and Model classes. Thereby indirectly letting the User and View classes interact with Model through the respective Controllers.

![[Use Case Controllers Class Diagram.png | center | 600]]

### Controller Bloat

Controller bloat occurs when a controller class takes on too many responsibilities, handling too much logic or coordinating too many tasks. This leads to low cohesion, making the controller hard to maintain, understand, and extend. It can also create tight coupling between unrelated parts of the system.

To avoid controller bloat, responsibilities should be distributed appropriately, often by creating multiple focused controllers or by delegating tasks to other classes. This keeps each controller manageable and aligned with the single responsibility principle.

**See the example below:**

![[Controller Bloat.png | center | 600]]

This design can be improved by creating unified controllers for similar classes:

![[Controller Bloat Fix.png | center | 600]]

The only difference here is that the unified controller takes in the `vendorId` as a parameter to differentiate between vendors.