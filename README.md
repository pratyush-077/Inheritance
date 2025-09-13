# AIM:

 To study and implement Inheritance
SOFTWARE USED:

VS Code
OBJECTIVE:

1. Code Reusability
   - Inheritance allows us to reuse the functionality of existing classes 
     in new classes without rewriting the same code.

2. Data Hiding and Access Control
   - By using private, protected, and public modes, inheritance provides 
     controlled access to data and methods.

3. Extensibility
   - Existing classes can be extended to add new features 
     without modifying the original code.

4. Hierarchical Classification
   - Helps in representing real-world relationships (IS-A relationship).
     Example: Student IS-A Person, Car IS-A Vehicle.

5. Polymorphism
   - Enables runtime polymorphism using virtual functions, 
     supporting method overriding for flexible and dynamic behavior.

6. Maintainability
   - Easier to maintain and update code since changes in base class 
     are automatically reflected in derived classes.

7. Readability and Organization
   - Inheritance improves program structure and makes it more logical 
     and organized by separating general and specific features.
THEORY:

DEFINITION

Inheritance is an OOP mechanism where a class (derived) acquires properties and behaviors (members) from another class (base). It expresses "IS-A" relationships and enables reuse and extension of code.
WHY USE INHERITANCE

Code reusability: reuse base class implementation in derived classes.
Extensibility: extend behavior without modifying original class.
Logical modelling: represent real-world hierarchical relationships.
Polymorphism support: enables runtime binding via virtual functions.
Maintainability: central place (base) to update common functionality.
MAIN TYPES

Single : Derived class from one base class.
Multiple : Derived class from two or more base classes.
Multilevel : Chain of inheritance A -> B -> C (derived from derived).
Hierarchical : Several derived classes inherit from one base.
Hybrid : Combination of two or more of the above.
MODES OF INHERITANCE

public : base public -> derived public; base protected -> derived protected
protected: base public/protected -> derived protected
private : base public/protected -> derived private
IMPORTANT CONCEPTS & BEHAVIOR

Constructor / Destructor order: Base class constructors run first (top to bottom), destructors run in reverse.
Name hiding: Derived functions can hide base functions with same name — use using-declaration.
Virtual functions: Enable polymorphism. Call to overridden functions resolve at runtime when accessed via base pointers/references.
Pure virtual (abstract) classes: class with one or more pure virtual functions => interface-like behavior.
Diamond problem: When two base classes share a common ancestor, a derived class may get duplicate copies of the ancestor members. Resolve using virtual inheritance: class B : virtual public A { ... };
COMMON PITFALLS

Unintended access level changes with protected/private inheritance.
Ambiguity in multiple-inheritance (same member name in different bases).
Overuse of inheritance instead of composition (favor composition when "has-a").
Slicing: assigning derived object to base object by value slices off derived parts.
PRACTICAL USAGE & GUIDELINES

Prefer public inheritance only when there is an IS-A relationship.
Use composition (member objects) for code reuse when relationship is not IS-A.
Make destructor virtual in base classes intended for polymorphic deletion.
Keep interfaces small and cohesive; avoid deep inheritance trees when possible.
FLOWCHART [Base Class] |

| | | [D1] [D2] [D3] (hierarchical)

or multilevel: [A] -> [B] -> [C]

or multiple: [B] [C] \ / [D]

EXAMPLE SCENARIOS (where inheritance helps)
GUI frameworks: Widget -> Button, TextBox, CheckBox (hierarchical)
File systems: FileBase -> TextFile -> LogFile (multilevel)
Multiple inheritance: combining interfaces (e.g., Drawable, Serializable)
# CONCLUSION:

- Inheritance is a central OOP mechanism that organizes and reuses code by
  modelling IS-A relationships. It encourages modular design and enables
  polymorphism, which is key to creating flexible and extensible APIs.
- However, inheritance is not a silver bullet: it introduces complexity
  (ambiguities, multiple-inheritance issues, and access-level subtleties).
  Design carefully: prefer composition for "has-a" relationships, make base
  classes' intent explicit (interfaces vs concrete bases), and use virtual
  inheritance to avoid the diamond problem where appropriate.
- In real-world projects, combine inheritance for abstraction and polymorphism
  with co
