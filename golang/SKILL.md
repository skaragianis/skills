---
name: golang
description: Use when user wants to write Go code.
---

- use go version 1.26 or higher
- prefer the standard library over external packages
- don't over-abstract with generics
- use raw SQL with pgx
- the database must generate primary key UUIDs
- struct fields of type string must have an enforced and sensible min and max length
- Every struct field that has constraints must be a dedicated type (not a primitive) with a constructor that validates on creation. The struct's own constructor must parse all fields through their constructors. If a value exists, it's valid — no downstream checks needed. This will often live in a packages types.go file.
- use table driven tests, and ensure 100% test coverage
- use the cmd/, pkg/, and internal/ structure
- internal packages must include separate handler.go, repository.go, types.go, and service.go files, plus whatever else is needed. One package per domain entity
- package names must be singular in name
- the service layer must manage transactions, passing them to the repository layer
- add context.Context to all blocking functions
- use constructor injection; accept interface, return struct
- handle all errors explicitly
- wrap errors with %w when crossing package boundaries, or when the call site isn't obvious from the error message alone. Don't wrap when the original error is already descriptive
- prefer any, over interface{}
- acronyms in uppercase e.g. ID, URL
- use internal/logging for all logging
- if return is the last statement in a function, and not on the only statement in a function, put a newline before it
