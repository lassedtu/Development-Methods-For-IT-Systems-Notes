An include relationship shows that one [[Use Case]] always incorporates the behavior of another [[Use Case]] as part of its execution

The included [[Use Case]] represents common functionality that is shared across multiple [[Use Case]]s, helping to avoid duplication and promote reuse

Include relationships are mandatory - the including [[Use Case]] cannot complete successfully without executing the included [[Use Case]]

## Characteristics

- **Always executed** - The included [[Use Case]] runs every time the including [[Use Case]] runs
- **Mandatory relationship** - The including [[Use Case]] requires the included [[Use Case]] to succeed
- **Shared functionality** - Represents common behavior used by multiple [[Use Case]]s
- **Factored out behavior** - Avoids duplicating the same steps across multiple [[Use Case]]s

## UML Notation

- **Arrow direction**: Points from the including [[Use Case]] to the included [[Use Case]]
- **Stereotype**: Labeled with `<<include>>`
- **Line type**: Dashed arrow
- **Reading**: "Base [[Use Case]] includes Extension [[Use Case]]"

## When to Use Include

### Common Scenarios
- **Authentication steps** that multiple [[Use Case]]s require
- **Data validation** that occurs in several different contexts  
- **Logging or auditing** that must happen for multiple operations
- **Common calculations** used across different business processes
- **Shared user interface flows** like confirmation dialogs

### Benefits
- **Eliminates duplication** - Write common functionality once
- **Improves maintainability** - Changes to common behavior only need to be made in one place  
- **Promotes consistency** - Ensures the same steps are followed every time
- **Simplifies [[Use Case]]s** - Main [[Use Case]]s focus on their unique logic

## Examples

### Example 1: User Authentication
**Including [[Use Case]]**: Create User Account
**Included [[Use Case]]**: Check User Exists

Before creating a new user account, the system must always check if a user with that email already exists. This check is required behavior that cannot be skipped.

### Example 2: E-commerce System
**Including [[Use Case]]s**: Place Order, Update Order, Cancel Order
**Included [[Use Case]]**: Validate Customer Account

All order-related operations must validate that the customer account is active and in good standing. This validation happens every time, regardless of which order operation is performed.

### Example 3: Banking System
**Including [[Use Case]]s**: Transfer Funds, Withdraw Cash, Pay Bill
**Included [[Use Case]]**: Verify Account Balance

Every financial transaction must verify sufficient funds before proceeding. This verification is mandatory for all monetary operations.

## Multiple Includes

A single [[Use Case]] can include multiple other [[Use Case]]s:

**[[Use Case]]**: Process Online Purchase
- **Includes**: Validate Payment Method
- **Includes**: Check Inventory Availability  
- **Includes**: Calculate Shipping Cost
- **Includes**: Generate Order Confirmation

Each included [[Use Case]] represents required functionality that must execute for the purchase to complete successfully.

## Include vs Other Relationships

### vs [[Extend Relationship]]
- **Include**: Always happens (mandatory)
- **[[Extend Relationship]]**: Sometimes happens (optional/conditional)

### vs Generalization
- **Include**: Incorporates another [[Use Case]]'s behavior
- **Generalization**: Inherits and specializes general behavior

## Common Mistakes

### Over-using Include
- Creating includes for every small common step
- Making [[Use Case]]s too granular and hard to understand
- Including behavior that isn't truly shared across multiple [[Use Case]]s

### Confusing Include with Extend
- Using include for optional behavior (should use [[Extend Relationship]])
- Using extend for mandatory behavior (should use include)

### Circular Dependencies
- Creating situations where [[Use Case]]s include each other
- Building complex chains of includes that are hard to follow

## Documentation Guidelines

### In [[Use Case]] Descriptions
- **Main Flow**: Reference the included [[Use Case]] at the appropriate step
- **Example**: "3. System includes Check User Exists to validate the email address"

### Include Points
- Clearly specify **where** in the main flow the include occurs
- Document **what data** is passed to the included [[Use Case]]
- Specify **what results** are expected back

## Design Considerations

### Interface Definition
- Define **input parameters** the included [[Use Case]] needs
- Specify **return values** or outcomes the including [[Use Case]] expects
- Document **error conditions** that might prevent successful inclusion

### Testing Strategy
- **Test included [[Use Case]]s independently** to verify they work correctly
- **Test including [[Use Case]]s** to ensure proper integration
- **Verify error handling** when included [[Use Case]]s fail

## Evolution During Development

- **[[Inception]]**: Identify obvious common functionality that could be included
- **[[Elaboration]]**: Refactor [[Use Case]]s to factor out shared behavior into includes
- **[[Construction]]**: Implement included [[Use Case]]s as reusable components
- **[[Transition]]**: Validate that include relationships work correctly in production

## Benefits for Implementation

- **Code reuse** - Common functionality can be implemented once and shared
- **Consistency** - Same behavior executes the same way across different contexts
- **Maintainability** - Changes to shared behavior only require updates in one place
- **Testing efficiency** - Shared functionality can be tested independently

Include relationships are powerful tools for managing complexity and promoting reuse in [[Use Case]] models, but they should be used judiciously to avoid over-complicating the model.
