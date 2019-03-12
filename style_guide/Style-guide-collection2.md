
# Coding Guide - Collection <2>

### Organizational and Policy Issues 

- Don't sweat the small stuff. (Or: Know what not to standardize.) 
- Compile cleanly at high warning levels. 
- Use an automated build system. 
- Use a version control system. 
- Invest in code reviews. 

### Design Style 

- Give one entity one cohesive responsibility. 
- Correctness, simplicity, and clarity come first. 
- Know when and how to code for scalability. 
- Don't optimize prematurely. 
- Don't pessimize prematurely. 
- Minimize global and shared data. 
- Hide information. 
- Know when and how to code for concurrency. 
- Ensure resources are owned by objects. Use explicit RAII and smart pointers. 

### Coding Style 2

- Prefer compile- and link-time errors to run-time errors. 
- Use const proactively.
- Avoid macros.
- Avoid magic numbers. 
- Declare variables as locally as possible. 
- Always initialize variables. 
- Avoid long functions. Avoid deep nesting.
- Avoid initialization dependencies across compilation units. 
- Minimize definitional dependencies. Avoid cyclic dependencies. 
- Make header files self-sufficient.
- Always write internal #include guards. Never write external #include guards.

### Functions and Operators

- Take parameters appropriately by value, (smart) pointer, or reference. 
- Preserve natural semantics for overloaded operators.
- Prefer the canonical forms of arithmetic and assignment operators.
- Prefer the canonical form of + + and --. Prefer calling the prefix forms. 
- Consider overloading to avoid implicit type conversions.
- Avoid overloading &&, ||, or , (comma). 
- Don't write code that depends on the order of evaluation of function arguments. 

### Class Design and Inheritance 

- Be clear what kind of class you're writing. 
- Prefer minimal classes to monolithic classes. 
- Prefer composition to inheritance. 
- Avoid inheriting from classes that were not designed to be base classes. 
- Prefer providing abstract interfaces.
- Public inheritance is substitutability. Inherit, not to reuse, but to be reused. 
- Practice safe overriding. 
- Consider making virtual functions nonpublic, and public functions nonvirtual. 
- Avoid providing implicit conversions. 
- Make data members private, except in behaviorless aggregates (C-style structs). 
- Don't give away your internals. 74
- Pimpl judiciously. 
- Prefer writing nonmember nonfriend functions. 
- Always provide new and delete together. 
- If you provide any class-specific new, provide all of the standard forms (plain,in-place, and nothrow).



### Construction, Destruction, and Copying 

- Define and initialize member variables in the same order.
- Prefer initialization to assignment in constructors. 
- Avoid calling virtual functions in constructors and destructors. 
- Make base class destructors public and virtual, or protected and nonvirtual. 
- Destructors, deallocation, and swap never fail. 
- Copy and destroy consistently.
- Explicitly enable or disable copying. 
- Avoid slicing. Consider Clone instead of copying in base classes. 
- Prefer the canonical form of assignment.
- Whenever it makes sense, provide a no-fail swap (and provide it correctly).

### Namespaces and Modules 

- Keep a type and its nonmember function interface in the same namespace.
- Keep types and functions in separate namespaces unless they're specifically intended to work together. 
- Don't write namespace usings in a header file or before an #include. 
- Avoid allocating and deallocating memory in different modules.
- Don't define entities with linkage in a header file. 
- Don't allow exceptions to propagate across module boundaries. 
- Use sufficiently portable types in a module's interface. 

### Templates and Genericity 

- Blend static and dynamic polymorphism judiciously. 
- Customize intentionally and explicitly.
- Don't specialize function templates.
- Don't write unintentionally nongeneric code. 

### Error Handling and Exceptions 

- Assert liberally to document internal assumptions and invariants. 
- Establish a rational error handling policy, and follow it strictly. 
- Distinguish between errors and non-errors. 
- Design and write error-safe code. 
- Prefer to use exceptions to report errors.
- Throw by value, catch by reference. 
- Report, handle, and translate errors appropriately.
- Avoid exception specifications. 



### STL: Containers 

- Use vector by default. Otherwise, choose an appropriate container. 
- Use vector and string instead of arrays.
- Use vector (and string::c_str) to exchange data with non-C++ APIs. 
- Store only values and smart pointers in containers. 
- Prefer push_back to other ways of expanding a sequence. 
- Prefer range operations to single-element operations. 
- Use the accepted idioms to really shrink capacity and really erase elements.

### STL: Algorithms 

- Use a checked STL implementation. 
- Prefer algorithm calls to handwritten loops.
- Use the right STL search algorithm. 
- Use the right STL sort algorithm. 
- Make predicates pure functions. 
- Prefer function objects over functions as algorithm and comparer arguments.
- Write function objects correctly.

### Type Safety

- Avoid type switching; prefer polymorphism. 
- Rely on types, not on representations. 
- Avoid using reinterpret_cast. 
- Avoid using static_cast on pointers. 
- Avoid casting away const. 
- Don't use C-style casts. 
- Don't memcpy or memcmp non-PODs. 
- Don't use unions to reinterpret representation. 
- Don't use varargs (ellipsis).
- Don't use invalid objects. Don't use unsafe functions. 
- Don't treat arrays polymorphically. 

***
