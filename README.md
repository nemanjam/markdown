
For learning resources I used extensive _"Core Python learning path"_ on Pluralsight including _"Core Python 3: Getting-Started"_, _"Python 3: Beyond the Basics"_ and _"Advanced Python"_ by Austin Bingham and Robert Smallshire, _"Managing Python Packages and Virtual Environments"_ and _"Python Best Practices for Code Quality"_ from Reindert-Jan Ekker, and also _"Python Programming Tutorial for a JavaScript Developer"_ Youtube tutorial by Get it Done, _"Python for JavaScript Developers"_ blog article by Valentino Galigardi, _"Python Tutorials"_ Youtube playlist by Corey Schafer, _"Fullstack Flask - Build a Complete SaaS App with Flask"_ by Sumukh Sridhara, _"Python Crash Course For Beginners"_ and _"Pipenv Crash Course"_ Youtube tutorials by Brad Traversy, _"Python Tutorial for Programmers - Python Crash Course"_ Youtube tutorial by Mosh Hamedani, _"flask_for_startups"_ Github repository example by nuvic. There is real abundance of learning material for Python on internet.



### Big Picture

#### Why Python?

#### What is Python?

Python is general purpose, multi-paradigm, interpreted, garbage collected, dynamically typed language with comprehensive standard library, 

#### Python Pros and Cons

---

### Getting Started

#### Installing and Starting Python

#### Scalar Types, Operators, and Control Flow

_scalar types_ - all immutable, int, float, None, bool, _control flow_ - if, else, elif, _loops_ - while, for, _relational operators_, _and, or, not_ - logical operators, _in_ - membership operator, _is_ - identity operator, 

#### Introducing Strings, Collections, and Iteration

_str_ - immutable string type and literals, _bytes_ - binary type, encoding and literals, 

#### Modularity

_modules_ - .py files, _ __name__ attribute _ - detect if file is imported or executed in shell, _python execution model_ - function name is bound to definition at runtime, _sys.argv[...]_ - passing command line arguments, _main()_ - custom entry point for a python script, _shebang_ - run python file as shell script, _docstrings_ - singleline and multiline, 

#### Objects and Types

_object and type models_, _identity equality_ - defined on language level, _value equality_ - defined on type level, _all variables are references, not boxes_ - all variables including scalar types, _pass by reference_ - arguments and return values, _positional and keyword arguments_ - defined on invocation, _default arguments_ - called at bind time, must be immutable types, _strong, dynamic type system_ - types resolved at runtime,  no type coercion to match type, _4 levels scope - LEGB_ - local, enclosing, global, built in, _everything is an object_ - including scalar types, functions and modules, 

#### Built-in Collections

_built in collections_, _list [...]_ - mutable, indexed, ordered collection with duplicates, _tuple (...)_ - immutable, indexed, ordered collection with duplicates, _ranges_ - arithmetic progression of integers, _dictionary {key: val}_ - unordered, indexed, mutable collection without duplicates - associative array - JavaScript object equivalent, _set {...}_ - unordered, non-indexed, mutable collection of immutable elements without duplicates, _protocols_ - set of functions, interface, 

#### Exceptions

_try, except_ - exception handling, _raise_ - throwing exceptions, _finally_ - block for cleanup actions, _programmer errors_ - should not be handled, _exceptions are part of the function signature and protocols_, _EAFP_ - easier to ask forgiveness than permission - try catch, can not be ignored, _LBYL_ - look before you leap - if else without exception, error codes, silent,

#### Iteration and Iterables

_comprehensions_ - concise syntax to transform collections without side effects - consists of expression, for loop and optional predicate, _generator functions_ - iterables defined via functions, have yield keyword, evaluated lazily, can model infinite sequences, can maintain state in local variables, _iteration protocols_ - iter() and next(), _generator expressions_ - create generator objects  with comprehensions, use (...) braces, _itertools_ - module for working with iterators, 

#### Classes

_classes_ - custom types, classes are callable objects in Python, name bound to definition once at runtime, PascalCase naming, no new keyword, _self_ - equivalent to this in Java, simply assign class attributes without declaration, _ __init__() _ - initializer, not a constructor, for configuring already created object, _methods_ - first argument is self and passed explicitly, _no access modifiers_ - everything is public, underscore for private attributes, _invariants_ - constraints, validate attributes, _duck typing_ - argument fitness determined at runtime, not by inheritance hierarchy at compile time, _late binding_ - use object to resolve method calling at runtime, _polymorphism_ - through late binding, not through inheritance, _inheritance_ - used only for reusing implementation, 

#### File IO and Resource Managements

_files and file like objects_ - text and binary mode, support iterator and context manager protocols, _universal newline_ - OS independent, _bitwise operators_, _with block_ - syntactic sugar for try except structure for managing resources using objects that implement context manager protocol, 

---

### Beyond the Basics

#### Organizing Larger Programs

_packages_ - folders, _modules_ - files, _sys.path_ - list of all included directories with modules, _PYTHONPATH_ - OS level environment variable that is included in sys.path, _ __init__.py_ - index file that creates  a package from a folder, _subpackages_ - package can have hierarchy, _relative imports_ - from import syntax with a dot, _ __all__ _ - export only some variables from a module, _namespace packages_ - package composed from a few sibling folders, _ __main__.py_ - create executable directories, _recommended layout_ - recommended folder structure with source, test, index and setup files, _module singletons_ - variables defined in modules are singletons, 

#### Beyond Basic Functions

_positional and keyword arguments_ - determined in the function call, _default arguments_ - evaluated only once at import time, must not be mutable value, _callable instances_ - their class has __call__() method defined, used as stateful functions, _callables_ - functions, classes, callable objects, lambdas, _conditional expressions_ - ternary expression equivalent, _lambdas_ - single expression anonymous functions, _extended formal and actual arguments syntax_ - def fn(*args, **kwargs), fn(*args), fn(**args) - equivalent to rest and spread syntax in JavaScript, unpacking - destructuring, _global functions_ - definition bound to name at runtime (import time), _local functions_ - redefined on each parent function call, _LEGB scopes_ - local, enclosing, global (module), built in, _function are first class citizens_ - can be passed, returned, assigned, _closures_ - maintain references from parent scopes, prevent garbage collection,

#### Closures and Decorators

_ __closure__ _ - reference to the closure variables, _function factories_ - functions that returns new specialized functions, _nonlocal and global keywords_ - reuse variables frm parent and global scope, _decorators_ - syntactic sugar for higher oder functions, accepts callable and returns callable, can be nested, _@functools.wraps()_ - helper decorator for forwarding metadata of the decorated function, _instance attributes_ - per instance, 

#### Properties and Class Methods

_class attributes_ - per class, same for all instances, _@staticmethod_ - does not reference neither class nor self, _@classmethod_ - references only class, _@property_ - property getter, _@name.setter_ - property setter, 

#### Strings and Representations

_str()_ - simple string representation, calls __str__(), meant for users, called on print(), _repr()_ - verbose string representation, calls __repr__(), required, meant for developers, _format()_ - calls __format__(), optional, _ascii(), ord(), chr()_ - helpers for escaping and translating ascii to unicode strings, 

#### Numeric and Scalar Types

_int_ - unlimited precision signed integer, _float_ - 64 bits floating point, _Decimal_ - configurable finite precision decimal floating point, _Fraction_ - rational numbers, _complex()_ - complex numbers, _abs(), round()_ - built in math helpers, _bin(), oct(), hex(), int()_ - number base conversion helpers, _datetime module_ - time(), datetime(), timedelta(), timezone() for working with time, 

#### Iterables and Iteration

_advanced comprehensions_ - multiple input sequences - nested loops, if clauses, in the result expression of a comprehension - multidimensional result, _map()_ - returns iterable, lazy, _filter()_ - accepts predicate, returns iterable, lazy, _reduce()_ - summation generalization, _iter(iterable)_ - requires __iter__(), iterable protocol, _next(iterator)_ - requires __next__() and __iter__(), iterator protocol, _ __getitem__()__ - iterable protocol for subsequent indexes, _iter(callable, sentinel)_ - extended iter format, 

#### Inheritance and Subtype Polymorphism

_single inheritance_, _multiple inheritance_, _isinstance() and issubclass()_ - helper methods, _method resolution order - MRO_ - search order of inheritance graph, Class.__mro__ and mro(), calculated by C3 algorithm, which base class method will be called, _super()_ - returns bound class or instance proxy object in class or instance methods, returns base class in single inheritance, _inheritance usage_ - not for type hierarchy but for reusing implementation, 

#### Implementing Collections

_collection protocols_ - container, sized, iterable, sequence, set, string representation and value equality protocols, _collections.abc_ - module with base implementations for collection protocols, 

#### Exceptions and Errors

_standard exception hierarchy_, _custom exceptions_ - should extend from Exception class, _implicit chaining exceptions_ - handling new exceptions in except block, __context__ attribute, _explicit chaining exceptions_ - raise new exceptions from except block, __cause__ attribute, _traceback objects_ - stack trace, print_tb() and format_tb() for printing, _asserts_ - check assumptions, raise AssertionError for False, useful for return values,

#### Defining Context Managers

_context manager_ - object used in with statement, used for unmanaged resources, _context manager protocol_ - __enter__(), __exit__() - setup, teardown methods, for creating custom context managers, _@contextlib.contextmanager_ - decorator for creating context managers, _multiple context managers_ - nested, 

#### Introspection

_introspection_ - programs can inspect their own structure and state, types, objects, scopes, _easier to ask forgiveness than permission - EAFP_ - optimistic philosophy, preferred, _look before you leap - LBYL_ - pessimistic philosophy, _dir(), getattr(), hasattr(), callable()_ - introspecting objects, _globals(), locals()_ - introspecting scopes, _inspect module_ - standard library module for introspecting objects, 

---

### Advanced Python

#### Advanced Flow Control

_while else, for else clauses_ - no-break exit from a loop, _try else clause_ - no exception block, _emulating switch statements_ - if, elif, elif, else or dictionary of functions,

#### Byte-oriented Programming

_bitwise operators_ - and, or, xor, not, left and right shift, _bin() and to_bytes()_ - convert integers to bits and bytes, _bytes type_ - immutable sequence of bytes, _bytearray type_ - mutable sequence of bytes, _reading C structures_, _memoryview, memory mapped files_ - copy free working with binary data, C buffer protocol,

#### Object Internals and Custom Attributes

#### Descriptors

#### Instance Creation

#### Metaclasses

#### Class Decorators

#### Abstract Base Classes




























