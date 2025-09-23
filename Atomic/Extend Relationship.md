An extend relationship is used when one [[Use Case]] adds optional or conditional behavior to another [[Use Case]]

The extending [[Use Case]] inserts its behavior at specific extension points in the base [[Use Case]], but only when certain conditions are met

Extend relationships handle exceptions, special cases, or optional functionality that doesn't always occur

## Characteristics

- **Optional execution** - The extending [[Use Case]] only runs when specific conditions are met
- **Conditional behavior** - Depends on circumstances during base [[Use Case]] execution
- **Exception handling** - Often used for error conditions or alternative scenarios
- **Extension points** - Base [[Use Case]] defines where extending behavior can be inserted

## UML Notation

- **Arrow direction**: Points from the extending [[Use Case]] to the base [[Use Case]]
- **Stereotype**: Labeled with `<<extend>>`  
- **Line type**: Dashed arrow
- **Extension points**: Listed inside the base [[Use Case]]
- **Reading**: "Extension [[Use Case]] extends Base [[Use Case]]"

## Extension Points

Extension points are specific locations within the base [[Use Case]] where extending behavior can be inserted:

- **Named locations** in the main flow of the base [[Use Case]]
- **Defined by the base [[Use Case]]** to allow for extensions
- **Conditional insertion** - Extensions only occur when conditions are met
- **Multiple points** - A base [[Use Case]] can have several extension points

## When to Use Extend

### Common Scenarios
- **Error handling** - What happens when something goes wrong
- **Alternative flows** - Different paths based on user choices or conditions
- **Optional features** - Additional functionality that some users might want
- **Special cases** - Behavior that only occurs in specific circumstances
- **Business rule variations** - Different handling based on user type or context

### Benefits
- **Keeps base [[Use Case]] simple** - Main scenario isn't cluttered with exceptions
- **Modular design** - Extensions can be developed and maintained separately
- **Flexibility** - Easy to add new extensions without modifying base [[Use Case]]
- **Clear separation** - Normal flow separated from exceptional flow

## Examples

### Example 1: User Authentication
**Base [[Use Case]]**: Sign In
- **Extension point**: authenticationError
**Extending [[Use Case]]**: Handle Authentication Error

The sign-in process normally completes successfully, but if authentication fails, the error handling extends the basic sign-in flow at the specified extension point.

### Example 2: Shopping Cart
**Base [[Use Case]]**: Checkout Order  
- **Extension point**: applyDiscount
**Extending [[Use Case]]**: Apply Coupon Code

Most customers checkout without using coupons, but when a coupon code is entered, the discount calculation extends the normal checkout process.

### Example 3: Library System
**Base [[Use Case]]**: Borrow Book
- **Extension point**: membershipExpired  
**Extending [[Use Case]]**: Handle Expired Membership

Usually book borrowing proceeds normally, but if the member's account has expired, special handling extends the borrowing process to address the membership issue.

## Complex Extend Examples

### Multiple Extension Points
**Base [[Use Case]]**: Process Payment
- **Extension points**: 
  - insufficientFunds
  - cardExpired
  - fraudDetected
**Extending [[Use Case]]s**:
- Handle Insufficient Funds (extends at insufficientFunds)
- Handle Expired Card (extends at cardExpired)  
- Handle Fraud Alert (extends at fraudDetected)

### Conditional Extensions
**Condition**: If payment amount > $1000
**Base [[Use Case]]**: Make Purchase
**Extension point**: highValueTransaction
**Extending [[Use Case]]**: Require Manager Approval

## Extend vs Other Relationships

### vs [[Include Relationship]]
- **[[Include Relationship]]**: Always happens (mandatory)
- **Extend**: Sometimes happens (optional/conditional)

### vs Alternative Flows
- **Alternative flows**: Part of the same [[Use Case]]
- **Extend**: Separate [[Use Case]] that extends another

## Documentation Format

### Extension Points in Base Use Case
```
Use Case: Sign In
Extension Points:
- authenticationError: After step 3, if authentication fails
- accountLocked: After step 3, if account is locked after multiple failures
```

### Extending Use Case
```
Use Case: Handle Authentication Error
Extends: Sign In
Extension Point: authenticationError
Condition: When user credentials are invalid
```

## Common Mistakes

### Over-using Extend
- Creating extends for every minor variation
- Making the model too complex with too many optional paths
- Using extend when the behavior should be part of the main flow

### Confusing Extend with Include
- Using extend for mandatory behavior (should use [[Include Relationship]])
- Using include for optional behavior (should use extend)

### Poor Extension Point Definition
- Not clearly defining where extensions can occur
- Making extension points too granular or too broad
- Not documenting the conditions that trigger extensions

## Design Considerations

### Base Use Case Design
- **Define clear extension points** where alternative behavior might be needed
- **Keep main flow simple** and focused on the typical scenario
- **Document conditions** that would trigger extensions

### Extending Use Case Design  
- **Specify clear conditions** for when the extension should occur
- **Define the insertion point** clearly in terms of the base [[Use Case]] steps
- **Handle return to main flow** - what happens after the extension completes

## Implementation Implications

### Code Structure
- Base [[Use Case]] functionality can be implemented as the main path
- Extensions can be implemented as separate modules or plugins
- Conditional logic determines when to invoke extensions

### Testing Strategy
- **Test base [[Use Case]] independently** without extensions
- **Test each extension** separately with appropriate conditions
- **Test integration** to ensure extensions integrate properly at extension points

## Evolution During Development

- **[[Inception]]**: Identify major exceptions and special cases that might need extends
- **[[Elaboration]]**: Define extension points and detail extending [[Use Case]]s
- **[[Construction]]**: Implement extensible architecture to support extend relationships
- **[[Transition]]**: Validate that extend relationships work correctly under real conditions

## Benefits for System Design

- **Separation of concerns** - Normal and exceptional behavior are separated
- **Maintainability** - Extensions can be modified without changing base functionality
- **Flexibility** - New extensions can be added without modifying existing [[Use Case]]s
- **Clarity** - Main scenarios remain uncluttered by exceptional cases

Extend relationships are particularly valuable for handling the complexity of real-world systems where exceptions and special cases are common but shouldn't obscure the primary functionality.
