# TypeScript Style Guide

## Table of Contents

1. [Imports](#imports)
1. [Naming](#naming)
1. [Functions](#functions)

## Imports

```ts
// Good: choose between two options as appropriate (see below).
import * as ng from "@angular/core";
import { Foo } from "./foo";

// Only when needed: default imports.
import Button from "Button";

// Sometimes needed to import libraries for their side effects:
import "jasmine";
import "@polymer/paper-button";
```

- Import paths

```ts
import { Symbol1 } from "path/from/root";
import { Symbol2 } from "../parent/file";
import { Symbol3 } from "./sibling";

// It's better use: @/
import { Symbol1 } from "@/path/from/root";
```

- Renaming imports
  Three examples where renaming can be helpful:
  1. If it's necessary to avoid collisions with other imported symbols.
  2. If the imported symbol name is generated.

```ts
import { SomeThing as SomeOtherThing } from "SomeThing";
```

## Naming

- Naming Conventions

```ts
// bad
const x = 10; // Unclear variable name.

// good
const numberOfItems = 10; // Clearly communicates the purpose of the variable.
```

- Constants

```ts
// bad
const api_url = "";

// good
const API_URL = "";
```

- Types

```ts
// bad
interface todoItem {
  id: number;
  value: string;
}

// good
interface TodoItem {
  id: number;
  value: string;
}
```

```ts
// bad
type todoList = TodoItem[];

// good
type TodoList = TodoItem[];
```

- Files

```ts
// bad
//    todoItem.tsx
//    todo_item.tsx
//    todo-item.tsx
//    Todoitem.tsx

// good
//    TodoItem.tsx

// good
//    Todo.tsx
```

## Functions

- Utility functions

```ts

```

**[⬆ back to top](#table-of-contents)**
