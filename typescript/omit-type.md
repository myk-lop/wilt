# Omit utility type

In TypeScript, the Omit utility type is used to create a new type from an existing type by excluding specific properties from it. It takes two type arguments: the first is the type you want to modify, and the second is a union of properties you want to omit from the original type. The Omit type helps create more specific types based on existing data structures without manually changing their properties.

```typescript
interface Todo {
  title: string;
  description: string;
  completed: boolean;
  createdAt: number;
}

type TodoPreview = Omit<Todo, 'description'>;

const todo: TodoPreview = {
  title: 'Clean room',
  completed: false,
  createdAt: 1615544252770,
};

todo;

const todo: TodoPreview;

type TodoInfo = Omit<Todo, 'completed' | 'createdAt'>;

const todoInfo: TodoInfo = {
  title: 'Pick up kids',
  description: 'Kindergarten closes at 5pm',
};

todoInfo;

const todoInfo: TodoInfo;
```
